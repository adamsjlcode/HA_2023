# Home Assistant Automations

This folder contains various automations used in my Home Assistant setup. Each automation is designed to streamline and automate different aspects of the home environment, from lighting to media control.

## Table of Contents

- [Home Assistant Automations](#home-assistant-automations)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
    - [Automation List](#automation-list)
  - [How to Contribute](#how-to-contribute)
  - [License](#license)

## Introduction

### Automation List

**Adjust Brightness of On Lights Except Screens**

**Description**:  
This automation adjusts the brightness of all lights that are currently on, except for screen-related lights, whenever the input_number for brightness changes.

- **Triggers**: Changes in `input_number.home_light_brightness`.
- **Actions**: Adjust brightness of all on lights (except those related to screens) to match the input_number value.
- **Conditions**: None.
- **Dependencies**: Lights that are turned on and exclude "\_screen" in their entity ID.

**Turn Off Lights on No Motion**

**Description**:  
This automation turns off lights in various areas of the home when no motion is detected for a specified amount of time, with room-specific delays. The delays are controlled by input_number entities.

- **Triggers**: No motion detected in rooms like the bedroom, kitchen, stairs, and media room, or when front or back doors are closed for a certain period of time.
- **Actions**: Turn off the lights in the corresponding room when no motion is detected.
- **Conditions**: Runs only if `input_boolean.sync_music_lights` and `input_boolean.theme_mode` are both off.
- **Dependencies**: Lights in the respective rooms, controlled by motion or contact sensors.

**Switch: Bedroom All Lights Off (Long Press)**

**Description**:  
This automation turns off all bedroom lights when the user long presses the off button on the bedroom Hue dimmer switch.

- **Triggers**: Long press on the off button for the specified bedroom Hue dimmer switch.
- **Actions**: Turns off all bedroom lights with a smooth 5-second transition.
- **Conditions**: None.

**Switch: Bedroom All Lights On (Long Press)**

**Description**:  
This automation turns on all bedroom lights to full brightness and a warm color temperature when the user long presses the on button on the bedroom Hue dimmer switch.

- **Triggers**: Long press on the on button for the specified bedroom Hue dimmer switch.
- **Actions**: Turns on all bedroom lights with a 60-second transition, setting brightness to 100% and color temperature to 228.
- **Conditions**: None.

**Switch: Bedroom Lights On (Short Press)**

**Description**:  
This automation turns on the bedroom lights when the user short presses the on button on the bedroom Hue dimmer switch.

- **Triggers**: Short press on the on button for the specified bedroom Hue dimmer switch.
- **Actions**: Turns on specified bedroom lights with a 5-second transition, setting brightness to 100% and color temperature to 234.
- **Conditions**: None.

**Switch: Bedroom Lights Off (Short Press)**

**Description**:  
This automation turns off the bedroom lights when the user short presses the off button on the bedroom Hue dimmer switch.

- **Triggers**: Short press on the off button for the specified bedroom Hue dimmer switch.
- **Actions**: Turns off specified bedroom lights with a smooth 5-second transition.
- **Conditions**: None.

**Switch: Downstairs Lights On (Short Press)**

**Description**:  
This automation turns on specified lights downstairs to full brightness with a cool color temperature when the user short presses the on button on the downstairs Hue dimmer switch.

- **Triggers**: Short press on the on button for the specified downstairs Hue dimmer switch.
- **Actions**: Turn on specified downstairs lights with a 15-second transition, setting brightness to 100% and color temperature to 412.
- **Conditions**: None.

**Switch: Downstairs Lights Off (Short Press)**

**Description**:  
This automation turns off the specified downstairs lights when the user short presses the off button on the downstairs Hue dimmer switch.

- **Triggers**: Short press on the off button for the specified downstairs Hue dimmer switch.
- **Actions**: Turns off specified downstairs lights with a smooth 5-second transition.
- **Conditions**: None.

Here’s the breakdown for your **Toggle Sleep Sensor** automation:

**Toggle Sleep Sensor (Long Press)**

**Description**:  
This automation toggles the `input_boolean.someone_sleeping` when the user long presses the middle button (subtype 3) on the bedroom Hue dimmer switch.

- **Triggers**: Long press on the middle button (subtype 3) of the specified Hue dimmer switch.
- **Actions**: Toggles the `input_boolean.someone_sleeping`.
- **Conditions**: None.

**Door Open TTS Alert**

**Description**:  
This automation sends a TTS alert through selected speakers when the front or back door is opened, indicating which door was triggered.

- **Triggers**: The back door or front door contact sensor changes to "on" (opened).
- **Actions**: Sets volume and sends a TTS message to both speakers indicating which door was opened.
- **Conditions**: None.
- **Set Light to Selected Color**

**Description**:  
This automation sets all lights to the color selected in the `input_select.light_color` dropdown. It disables normal lighting and sync music lighting and enables color mode.

- **Triggers**: A change in the selected color from the `input_select.light_color` dropdown.
- **Actions**:
  - Turns off the normal lights and sync music lighting input booleans.
  - Enables color mode.
  - Sets all lights to the color selected in `input_select.light_color`.
- **Conditions**: None.

**Outdoor Night Light**

**Description**:  
This automation toggles the outdoor light when the back door is opened after sunset. The light stays on for 15 minutes before turning off again.

- **Triggers**: The back door contact sensor changes from "off" to "on" (opened).
- **Actions**:
  - Toggles the outdoor light when the back door is opened.
  - Delays for 15 minutes.
  - Toggles the outdoor light off after the delay.
- **Conditions**: Only runs after sunset.

**Normal Light On**

**Description**:  
This automation turns off the color mode, sync music lights, and theme mode when the normal lights input boolean is switched on.

- **Triggers**: The `input_boolean.normal_lights` changes from "off" to "on".
- **Actions**:
  - Turns off color mode, sync music lights, and theme mode input booleans.
- **Conditions**: None.

**Theme is off**

**Description**:  
This automation turns on the normal lights input boolean when the theme mode is turned off.

- **Triggers**: The `input_boolean.theme_mode` changes from "on" to "off".
- **Actions**: 
  - Turns on the normal lights input boolean.
- **Conditions**: None.

**Sync Sengled with Hue - Dynamic Palette**

**Description**:  
This automation mimics the Hue dynamic scenes on Sengled lights by matching the brightness and RGB color attributes of various Hue lights with the Sengled lights.

- **Triggers**: A change in the dynamics attribute of the Hue lights.
- **Actions**: 
  - Synchronizes the brightness and RGB color of the Sengled lights with the corresponding Hue lights.
- **Conditions**: None.

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
