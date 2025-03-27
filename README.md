#**Guide to Implementing Fingerprint (FP) Animation on One UI Devices**:smile:

Hi there! It's great that you're interested in developing One UI features, particularly fingerprint (FP) animations. This kind of animation is especially useful for apps that implement biometric authentication systems (like fingerprint unlocking). In this guide, I'll walk you through the basic steps to implement fingerprint animation on One UI.

#**Basic Requirements for Fingerprint Animation (FP Animation)** 👾

#**Knowledge Required** 🧠

Lottie JSON Files: You should have some understanding of Lottie JSON files and how they work. These files are used to store vector animations which are lightweight and scalable. You can use them to implement fingerprint animations.

Root Access: This process requires root access to your device.

System Format: The system partition must be in EXT4 format. If your system partition is in EROFS format, this method will not work. Please ensure your system is EXT4.

Important Note:
Backup Everything: Before proceeding, back up all your files and photos. This process involves working with system files, and there's always a risk of issues arising. I'm not responsible for any damage to your device.

#**GUIDE** 😉

**1 Steps to Implement Fingerprint Animation**
** Backup Biometric Settings**
Before making any changes, you need to back up the BiometricSetting.apk. Follow these steps:

Navigate to the following directory:

bash
Copy code
```/system/priv-app```
Inside the priv-app folder, you will find the BiometricSetting folder.

Copy the folder and paste it wherever you want as a backup.

If the fingerprint animation doesn't work or if you encounter any issues, you can always replace the modified file with the original one from the backup.

** Recognize Your Fingerprint Sensor Type** 
**2 In Samsung devices, there are typically three types of fingerprint sensors:**

- ##**Green**(Optical Sensor)

- ##**White** (Optical Sensor)

- ##**Ultra Sonic Sensor**

Make sure you identify the correct sensor type for your device. This will help in selecting the appropriate animation and configuration.

**3. Extract Fingerprint Animation Files**  🔑 
https://t.me/c/2342857187/99/602 👈🏻
**link to download here** 
##**Credits**
This method was developed with the help of contributions from **@MrDexx.**
   
You can use the FP Animation ZIP file. After extracting it, you will have the required Lottie JSON files for the fingerprint animation.

**4. Install Lottie Files APK** 🧬
To view and test the animations, you'll need to install the Lottie Files APK. You can get it either from the Google Play Store or by downloading it directly from a browser (such as Chrome). Once installed, open the Lottie Files app, where you'll be able to see the types of animations available.

You can open the extracted Lottie JSON files in the Lottie Files app to view the available animation types.

**5. Applying the Fingerprint Animation** 🎊
Once you've set up everything, proceed to apply the fingerprint animation on your device. This step may require replacing system files, so ensure you have root access and backups.
- Replace the required animation file in the appropriate system folder.
- Reboot your device.
If the fingerprint animation appears, you have successfully implemented the animation!

**6. Troubleshooting** 🛠
If your fingerprint sensor is disabled or not recognized by the system, and the animation is not working, you may need to replace the modified files with the backup BiometricSetting.apk.
- Steps:
- Go to /system/priv-app and restore the original BiometricSetting.apk file from your backup.
- Reboot the device and check if the fingerprint sensor works again.

**7. Manually Changing the Files**
- If the animation is still not working, follow these steps to change the files manually:
- Go to ```/system/priv-app``` and extract the BiometricSetting APK.
- Ensure the extracted files are placed in internal storage for clarity.
- Open the BiometricSetting folder, navigate to the /assets folder.
- In the assets folder, you will find different files, but the key animation files are:
- bash ```indisplay_fingerprint_touch_effect_green_circle.json```
