<div align="center">
    <a href="https://github.com/MatterCoder/Matterflow">
        <img width="200" height="150" src="addons/matterflow/logo.png">
    </a>
    <div style="display: flex;"><h1>Matterflow</h1></div>
    <br>
    <br>
    <div style="display: flex;">
        <a href="https://github.com/MatterCoder/Matterflow/releases">
            <img src="https://img.shields.io/github/release/MatterCoder/Matterflow.svg">
        </a>
        <a href="https://github.com/MatterCoder/Matterflow/stargazers">
            <img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/Mattercoder/Matterflow">
        </a>
        <a href="https://matterflow.slack.com">
            <img src="https://img.shields.io/badge/Slack-channel-red?logo=slack">
        </a>
    </div>
    <!-- HTML snippet to my README -->
    <div style="display: flex;">
        <a href="https://matterflow.cloud/docs/intro" style="background-color: #0070f3;border: 1px solid #0070f3;border-radius: 4px;cursor: pointer;font-size: 14px;font-weight: 500;line-height: 1.5;padding: 8px 16px;text-align: center;text-decoration: none;color: #ffffff;transition: color 0.3s ease, background 0.3s ease, border-color 0.3s ease;display: inline-block;white-space: nowrap;">
        Matterflow Tutorial - 5min ⏱️
        </a>    
    </div>

    <h1>Home Assistant Add-on: Matter Data Pipeline</h1>
</div>

## Overview

Matterflow is a powerful Home Assistant add-on that simplifies working with data from **Matter-enabled IoT devices**. With Matterflow, you can **Transform** and **Stream** IoT Data to Cloud and AI Applications. It seamlessly integrates with your Home Assistant setup to:

- Automatically **receive and process IoT data**.
- Transform and model data for use in various formats like **CSV** or **JSON**.
- Send processed data to the **Cloud** and **AI applications** or store it locally for further analysis.

This add-on is ideal for developers, data scientists, and IoT enthusiasts looking to unlock the full potential of their smart devices.

---

## Installation

### Prerequisites

1. Ensure your Home Assistant installation is up and running.
2. The Matter server addon is required for communication with Matter devices. If you don't have that installed follow these instructions:

### Prepare Matter Server

In Home Assistant, have the Matter integration installed.
1. Go to Settings > Devices & services.
2. Add the Matter (BETA) integration.
- When prompted to Select the connection method:
  * If you run Home Assistant OS in a regular setup: select Submit. This will install the official Matter server add-on. Note that the official Matter server add-on is not supported on 32-bit platforms.
  * If you are already running the Matter server in another add-on, in or a custom container, Deselect the checkbox, then select Submit. In the next step, provide the URL to your Matter server.


### Add the Repository

1. Go to the **Add-on store** in Home Assistant.
2. Click **⋮ → Repositories**, and paste the following URL:
   
[https://github.com/MatterCoder/addon-matterflow](https://github.com/MatterCoder/addon-matterflow)

Click **Add → Close**, or click the button below to add the repository directly:  
[![Add Repository](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2FMattercoder%2Faddon-matterflow)

3. Select the add-on and click **Install**.

### Post Installation

1. After installation, open the Web UI to verify the add-on is running.  
- If it shows `502: Bad Gateway`, wait a moment and refresh the page.
- Check the **Log** tab for errors if the add-on doesn't start.

---

## Features

- **Automatic Pipeline Run**: Automatically run local pipelines.
- **Data Transformation**: Supports custom rules for transforming incoming data.
- **Storage Options**: Save data locally as **CSV** or **JSON**, or send it to a remote server.
- **AI-Ready**: Seamlessly export data for machine learning or AI-driven analysis.

---

## Troubleshooting

### Common Issues

- **No data received from devices**:
- Ensure your Matter server is running and configured correctly.
- Verify device connectivity and compatibility with Matter.

- **Add-on fails to start**:
- Check the logs for configuration errors.
- Ensure dependencies like the Matter server are installed and running.

### Logs

View detailed logs in the **Log** tab of the add-on to diagnose issues.

---

## Documentation

Comprehensive documentation is available in the [docs website](https://Matterflow.cloud). Topics include:

- Advanced configuration
- Custom data transformation rules
- Sending data to cloud platforms

---

## Contributing

We welcome contributions! Check out the [contribution guidelines](https://github.com/MatterCoder/Matterflow/blob/main/CONTRIBUTING.md) to get started. Issues and pull requests are always appreciated.

---

## Changelog

All notable changes will be documented in [CHANGELOG.md](CHANGELOG.md). The versioning follows the format:

- Stable releases: `X.Y.Z`
- Development versions: `X.Y.Z-Dev`

---

## License

This project is licensed under the [Apache License](LICENSE).

## Credits

- [ivobrett](https://github.com/oidebrett)


[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[armhf-shield]: https://img.shields.io/badge/armhf-yes-green.svg
[armv7-shield]: https://img.shields.io/badge/armv7-yes-green.svg
[i386-shield]: https://img.shields.io/badge/i386-yes-green.svg
