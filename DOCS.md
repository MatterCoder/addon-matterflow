# Home Assistant Add-on: Matterflow

## Installation

Follow these steps to get the add-on installed on your system:

1. Navigate in your Home Assistant frontend to **Settings** -> **Add-ons** -> **Add-on store**.
2. Find the "Matterserver" add-on and click it.
3. Click on the "INSTALL" button.

## How to use

The add-on has a couple of options available. To get the add-on running:

1. Start the add-on.
2. Have some patience and wait a couple of minutes.
3. Check the add-on log output to see the result.

## Configuration

Add-on configuration:

```yaml
ports:
  5173/tcp: 5173
  9001/tcp: 9001
```
## Accessing files

Matterflow runs within a docker container. When writing or reading from the local filesystem, the `/share` folder can used to access files from the Docker container on the host, or on the host filesystem under `/usr/share/hassio/share`.

## Support

Got questions?

You have several options to get them answered:

- The Matterflow [Community Forum][forum].

In case you've found a bug, please [open an issue on our GitHub][issue].

[slack]: https://matterflow.slack.com
[issue]: https://github.com/MatterCoder/matterflow/issues
[repository]: https://github.com/MatterCoder/matterflow
[docs]: https://matterflow.cloud/