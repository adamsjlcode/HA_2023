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

- AccuWeather: Provides weather data for automations based on weather conditions.
- Android Debug Bridge: Failed setup, will retry.
- Anniversaries: Tracks and notifies about important dates and anniversaries.
- Blitzortung: Lightning detection integration.
- BodyMiScale: For monitoring body metrics.
- Browser Mod: Extends Home Assistant's frontend by enabling control of the browser.
- ColorExtractor: Extracts prominent colors from images for use in Home Assistant.
- Custom Panel: Allows custom UI panels in Home Assistant.
- Dwains Dashboard: Custom Home Assistant dashboard interface.
- Favicon: Custom favicon for your Home Assistant instance.
- FontAwesome: Integration for using FontAwesome icons.
- Frigate: NVR solution with real-time object detection.
- GeoNet NZ Quakes: Earthquake detection from GeoNet New Zealand.
- GeoNet NZ Volcano: Volcano monitoring integration.
- Google Cast: Control Chromecast devices.
- Google Translate Text-to-Speech: Provides text-to-speech capabilities.
- HACS: Home Assistant Community Store for custom components.
- Harmony AC: Control for Harmony AC.
- Home Assistant Supervisor: Manages the Home Assistant instance.
- IQVIA: Provides healthcare-related data.
- LG WebOS Smart TV: Control LG WebOS TV.
- Local To-do: Local to-do list management.
- Logitech Harmony Hub: Integration for controlling devices via Logitech Harmony Hub.
- Media Extractor: Extracts media metadata.
- Meteorologisk Institutt (Met.no): Weather service integration.
- Mobile App: Connect mobile devices for geolocation and notifications.
- Moon: Provides moon phase data.
- MQTT: Communicates with IoT devices over the MQTT protocol.
- NETGEAR: Network monitoring and control for NETGEAR devices.
- NWS Alerts: National Weather Service alerts.
- NOAA Aurora Sensor: Aurora borealis sensor from NOAA.
- NPM Switches: Control npm packages as switches.
- OpenUV: Provides UV index data.
- Oral-B: Monitor Oral-B smart toothbrush.
- Passive BLE Monitor: Monitors Bluetooth Low Energy devices.
- Philips Hue: Smart lighting control.
- Plex Media Server: Automates media control with Plex.
- Plex Recently Added: Triggers actions based on newly added media in Plex.
- Powercalc: Calculate power consumption for devices.
- Radio Browser: Browse and stream radio stations.
- Reolink IP NVR/Camera: Surveillance camera control and monitoring.
- RESTful: Integration for making RESTful API calls.
- Season: Track the current season and use it in automations.
- Shopping List: Manage a shopping list.
- SmartThings: Integrate Samsung SmartThings for device control.
- Sonarr: Media library management.
- Spook: Mystery integration.
- Steam Wishlist: Monitor and track Steam wishlist items.
- System Monitor: Monitor system performance and statistics.
- Tautulli: Failed setup, will retry.
- Team Tracker: Track sports teams and their schedules.
- Thread: Communication protocol for IoT devices.
- TP-Link Smart Home: Smart device control for TP-Link devices.
- U.S. Geological Survey (USGS) Earthquake Hazards: Earthquake detection and data.
- Universal Media Player: Unified media control.
- Variables+History: Stores and tracks custom variables with history.
- VLC Media Player via Telnet: Control VLC media player remotely.
- Weatheralerts: Provides weather alerts for your location.
- World Air Quality Index (WAQI): Air quality monitoring data.
- Worldclock: Provides world time data.
- Xbox: Integration for Xbox console.
- YouTube Sensor: Tracks live YouTube events.
- YouTube Media Player: YouTube media player control.
- Zodiac: Provides zodiac sign data.

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
