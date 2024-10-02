Here is the updated README content that you can copy and upload without removing anything from your original file:

````markdown
# Home Assistant Configuration

This repository contains the configuration files for my Home Assistant setup. The configuration includes various scenes and their corresponding entity pictures.

## Table of Contents

- [Project Overview](#project-overview)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Configuration](#configuration)
- [Usage](#usage)
  - [Scenes](#scenes)
  - [Automations](#automations)
- [Integrations](#integrations)
- [Hardware](#hardware)
- [Contributing](#contributing)
  - [Pull Requests](#pull-requests)
  - [Reporting Bugs](#reporting-bugs)
  - [Feedback and Suggestions](#feedback-and-suggestions)
- [License](#license)

## Project Overview

This project is a configuration setup for Home Assistant, a popular open-source home automation platform. The configuration includes various scenes with custom entity pictures to enhance the visual representation within the Home Assistant UI. Additionally, it integrates several smart devices and automations to simplify daily routines and security.

## Getting Started

### Prerequisites

Before you begin, ensure you have met the following requirements:

- You have installed Home Assistant.
- You have access to the Home Assistant configuration directory.

### Installation

1. **Clone the repository**:
   ```bash
   git clone [https://github.com/adamsjlcode/HassioConfig2023.git]
   cd home-assistant-config/
   ```
````

2. **Copy the configuration files** to your Home Assistant configuration directory. Be cautious and make backups of your existing configuration files if necessary.

3. **Restart Home Assistant** to apply the new configuration:
   ```bash
   docker restart home-assistant
   ```
   Or use the restart option within the Home Assistant UI.

### Configuration

The main configuration file is `configuration.yaml`, which includes the setup for various scenes with custom entity pictures.

#### Sample Configuration Snippet

```yaml
homeassistant:
  customize_glob:
    scene.*lake_mist:
      entity_picture: /local/hue_scene_icons/lake_mist.png
      # Add other scenes similarly
```

### Scenes

The following scenes are configured with custom entity pictures:

- adrift
- amber_bloom
- amethyst_valley
- arctic_aurora
- autumn_gold
- beginnings
- blood_moon
- blossom
- blue_lagoon
- energize
- fairfax
- first_light
- forest_adventure
- frosty_dawn
- galaxy
- golden_pond
- hal
- hazy_days
- honolulu
- horizon
- ibiza
- lake_mist
- lake_placid
- lily
- magneto
- majestic_morning
- memento
- meriete
- miami
- midsummer_sun
- midwinter
- misty_ridge
- moonlight

Each scene is associated with an entity picture located in the `/local/hue_scene_icons/` directory. Simply activate a scene in Home Assistant to see the corresponding entity picture.

### Automations

This configuration also includes automations that simplify daily routines:

- **Morning Routine**: Lights gradually turn on in the morning, and the coffee maker starts after motion is detected in the kitchen.
- **Media Control**: When Plex playback starts, the lights automatically dim; they return to normal once the media ends.
- **Security Alerts**: When motion is detected, notifications are sent, and video footage is captured using security cameras.

## Integrations

This configuration includes the following integrations:

- **Philips Hue**: Smart lighting control for automations based on time of day and motion detection.
- **TP-Link Kasa**: Control of smart plugs and switches for automated energy management.
- **Plex Media Server**: Automates lighting based on media playback.
- **YouTube Sensor**: Detects live YouTube streams from selected channels to trigger automations.
- **Google Assistant**: Voice control for managing devices and automations.
- **Zigbee2MQTT**: Manages Zigbee-based smart devices.
- **Frigate NVR**: Provides real-time security monitoring using motion detection from cameras.
- **Mobile App**: Allows for mobile tracking and location-based automations.
- **MQTT**: Integrates various IoT devices using MQTT protocol.

## Hardware

This setup is running on the following hardware:

- **Unraid VM**: Home Assistant is deployed in a virtual machine on Unraid.
- **Philips Hue Bridge**: Centralized lighting control.
- **TP-Link Kasa Smart Plugs**: Used for device control and energy monitoring.
- **Security Cameras**: Monitored via Frigate NVR.

## Contributing

Contributions are welcome! Please follow the guidelines below to contribute to the project.

### Pull Requests

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

### Reporting Bugs

To report a bug, open an issue on GitHub and include details about the bug and steps to reproduce it.

### Feedback and Suggestions

Feedback and suggestions are always welcome. Feel free to open an issue on GitHub to discuss any ideas or improvements.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

```

This version retains all the original content and adds sections for automations, integrations, and hardware as discussed earlier. You can now upload this as your new `README.md` file.
```
