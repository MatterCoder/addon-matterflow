ARG BUILD_FROM
FROM $BUILD_FROM as base

ENV LANG C.UTF-8

WORKDIR /matterflow

RUN apk add --update --no-cache npm dumb-init git python3 py3-pip python3-dev && \
    echo "Installing MatterFlow"

RUN git clone https://github.com/MatterCoder/matterflow.git /matterflow && \
    mkdir /matterflow/dist && \
    jq -n --arg commit $(eval cd /matterflow;git rev-parse --short HEAD) '$commit' > /matterflow/dist/.hash ; \
    echo "Installed MatterFlow @ version $(cat /matterflow/dist/.hash)" 

# Move into the api directory
WORKDIR /matterflow/api

ENV VIRTUAL_ENV=./venv
RUN python3 -m venv $VIRTUAL_ENV
ENV PATH="$VIRTUAL_ENV/bin:$PATH"

RUN $VIRTUAL_ENV/bin/pip install pipenv

# Install dependencies:
RUN . /matterflow/api/venv/bin/activate && pipenv install

# Install supervisord:
RUN $VIRTUAL_ENV/bin/pip install supervisor

# Set up not so Secret Key
RUN echo "SECRET_KEY=tmp" > mf/.environment

# Set up the address for the Matter python server websocket
RUN echo "MATTER_SERVER=core-matter-server.local.hass.io" >> mf/.environment

# Set up the path for the sqlite3 db to be the tmp which we have mapped to /config 
RUN echo "DB_DIR_PATH='/tmp'" >> mf/.environment

# Install Web front end
WORKDIR /matterflow/web

RUN npm install
RUN npm run build

# Copy data for add-on
COPY run.sh .
RUN chmod +x run.sh

CMD ["./run.sh"]


