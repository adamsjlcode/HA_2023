
---

# Home Assistant Automations

This folder contains various automations used in my Home Assistant setup. Each automation is designed to streamline and automate different aspects of the home environment, from lighting to media control.

## Table of Contents

- [Home Assistant Automations](#home-assistant-automations)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Automation List](#automation-list)
    - [1. Adjust Brightness of On Lights Except Screens](#1-adjust-brightness-of-on-lights-except-screens)
    - [2. Turn Off Lights on No Motion](#2-turn-off-lights-on-no-motion)
  - [How to Contribute](#how-to-contribute)
  - [License](#license)

## Introduction

The automations in this repository are organized based on their purpose, such as lighting, media control, and security. This README file documents each automation's purpose, triggers, actions, and conditions to help understand how they function.

## Automation List

### 1. Adjust Brightness of On Lights Except Screens

**Description**:  
This automation adjusts the brightness of all lights that are currently on, except for screen-related lights, whenever the input_number for brightness changes.

- **Triggers**: Changes in `input_number.home_light_brightness`.
- **Actions**: Adjust brightness of all on lights (except those related to screens) to match the input_number value.
- **Conditions**: None.
- **Dependencies**: Lights that are turned on and exclude "_screen" in their entity ID.

### 2. Turn Off Lights on No Motion

**Description**:  
This automation turns off lights in various areas of the home when no motion is detected for a specified amount of time, with room-specific delays. The delays are controlled by `input_number` entities.

- **Triggers**: No motion detected in rooms like the bedroom, kitchen, stairs, and media room, or when front or back doors are closed for a certain period of time.
- **Actions**: Turn off the lights in the corresponding room when no motion is detected.
- **Conditions**: Runs only if `input_boolean.sync_music_lights` and `input_boolean.theme_mode` are both off.
- **Dependencies**: Lights in the respective rooms, controlled by motion or contact sensors.

## How to Contribute

Contributions are welcome! To add new automations or improve existing ones, please follow these steps:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature-automation`.
3. Add your changes and document the automation in this README.
4. Commit your changes: `git commit -m 'Add new automation: [Automation Name]'`.
5. Push to the branch: `git push origin feature-automation`.
6. Open a pull request.

## License

This project is licensed under the MIT License.

---
