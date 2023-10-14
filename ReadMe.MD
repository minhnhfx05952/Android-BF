# Android PIN Bruteforce with HID Keyboard
![License](https://img.shields.io/badge/License-GNU-blue.svg)
Welcome to the Android PIN Bruteforce project, where I share my personal discoveries and online research in a colorful and educational manner. Please remember that this project is for educational purposes only, and I assume no responsibility for any issues or legal consequences that may arise from its use.

**Note:** To get started, ensure that you have a rooted device and have installed Nethunter. If you lack an alternative means to set up USB functionality, this is an essential prerequisite.

## 🌈 How it Works

This project harnesses the power of a USB OTG cable to connect a locked Android phone to a Nethunter device. It beautifully emulates a keyboard, automatically attempting PIN combinations and gracefully pausing after multiple incorrect attempts. The setup looks like this:

[Nethunter phone] <--> [USB cable] <--> [USB OTG adaptor] <--> [Locked Android phone]

The USB HID Gadget driver enables your Android Nethunter device to artfully simulate keyboard input to the locked phone, much like plugging in a physical keyboard and elegantly entering PINs.

## 📋 Requirements

1. A rooted device.
2. The installation of Nethunter (if no other USB functionality setup is available).

## 🚀 Installation (Step 1)

1. Begin your colorful journey by downloading and installing the [NetHunter Store](https://store.nethunter.com/).

2. Next, let's install NetHunter and NetHunter Terminal; make sure to configure them beautifully.

3. Let's add a touch of flair by installing Termux. Opt for the GitHub version or another source, and steer clear of the mundane Google Play Store version.

4. Now, let's add a burst of color to your terminal with these commands in both NetHunter Terminal and Termux:

   ```shell
   apt update
   apt upgrade
   ```

5. Return to Nethunter and choose "USB Arsenal." For a colorful experience, select your target: "Win" or "Linux," and go for a target with HID support. Don't forget to enable ADB and set USB Function.

## ⚙️ Installation in Terminal (Step 2)

You have the choice of using either Termux or Terminal, but for a truly vibrant experience, I recommend the Nethunter Terminal.

1. Let's paint your terminal with colors by cloning the repository:

   ```shell
   git clone https://github.com/minhnhfx05952/Android-BF.git
   ```

2. Dive into the colorful world of this project by navigating to the cloned directory:

   ```shell
   cd Android-BF
   cd hid_gadget_test
   ```

3. Get ready to compile the HID Gadget Test binary. Keep in mind that you must compile this binary on the device itself; transferring a precompiled binary just won't do:

   ```shell
   gcc hid_gadget_test.c
   ```

4. Now, let's make the binary executable. A touch of color adds the right flair:

   ```shell
   make
   ```

5. Return to the vibrant heart of the project:

   ```shell
   cd ..
   cd Android-PIN-Bruteforce
   ```

6. It's time to add some personal flair. Edit the configuration file using your preferred text editor. Modify the `HID_KEYBOARD` variable to point to the `hid_gadget_test` binary on your device. For example:

   ```shell
   nano config
   ```

   Transform `HID_KEYBOARD` into something like `HID_KEYBOARD=~/Download/hid_gadget_test`.

7. Now, let's connect two devices and make the magic happen.

8. If you know the number of digits in the PIN (from 1 to 10 digits), use the following command to crack it. For example, to crack a 4-digit PIN:

   ```shell
   ./android-pin-bruteforce crack --length 4
   ```

9. If you're in the mood for a colorful surprise and don't know the number of digits, use this command:

   ```shell
   ./android-pin-bruteforce crack
   ```

Remember, add your own personal touch to this project and use it responsibly and ethically. Use it only on devices for which you have explicit permission to perform such tests.

🎨 **Add More Colors and Icons!** 🌟