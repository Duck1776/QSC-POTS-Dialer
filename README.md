# QSC POTS Dialer Module Fix

## Overview

This repository contains a fixed version of the QSC POTS Dialer module for the Q-SYS Designer software. The original module had several issues that prevented proper functionality, particularly when trying to dial numbers.

## Issues Identified

1. **Extra Period in Named Controls**: Most buttons in the S-3.1:Keypad and S-4:Functions folders had an extra period in their Named Control fields.
   - S-3.1.1 was incorrectly set to `Dialer..BTN.KP.1` instead of `Dialer.BTN.KP.1`
   - S-3.1.2 was incorrectly set to `Dialer..BTN.KP.2` instead of `Dialer.BTN.KP.2`
   - etc.

3. **Swapped Keypad Buttons**: The Named Controls for keypad buttons 4 and 6 were swapped:
   - S-3.1.5 was incorrectly set to `Dialer..BTN.KP.6` instead of `Dialer..BTN.KP.4`
   - S-3.1.7 was incorrectly set to `Dialer..BTN.KP.4` instead of `Dialer..BTN.KP.6`

4. **Reversed Connect/Disconnect Buttons**: The Named Controls for the Connect and Disconnect buttons were reversed:
   - S-4.1 was incorrectly set to `Dialer.BTN.HookON` instead of `Dialer.BTN.HookOFF`
   - S-4.2 was incorrectly set to `Dialer.BTN.HookOFF` instead of `Dialer.BTN.HookON`

## Fixes Applied

1. Removed the extra period from all Named Control fields in the S-3.1:Keypad and S-4:Functions folders.
2. Corrected the Named Controls for keypad buttons 4 and 6.
3. Swapped the Named Controls for the Connect and Disconnect buttons.

## Usage

1. Download the fixed module from this repository.
2. Import the module into your Q-SYS Designer project.
3. The POTS Dialer functionality should now work correctly, including all keypad buttons and the Connect/Disconnect functions.

## Original Issue

The original module had non-functional keypad buttons, with only the Backspace and Clear buttons working. Additionally, the Dial/Answer and End/Ignore buttons were reversed.

## Verification

To verify the fix:
1. Open the module in Q-SYS Designer.
2. Navigate to the Named Controls section.
3. Check that all Named Controls in the S-3.1:Keypad and S-4:Functions folders are correct and do not contain extra periods.
4. Ensure that the Named Controls for keypad buttons 4 and 6 are correctly assigned.
5. Verify that the Connect and Disconnect buttons have the correct Named Controls.

## Contributing

If you find any additional issues or have suggestions for improvements, please open an issue or submit a pull request.

## Acknowledgements

Special thanks to the user who identified and fixed these issues, spending considerable time troubleshooting the module.
