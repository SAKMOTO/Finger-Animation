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

**7. Manually Changing the Files**🔍
- If the animation is still not working, follow these steps to change the files manually:
- Go to ```/system/priv-app``` and extract the BiometricSetting APK.
- Ensure the extracted files are placed in internal storage for clarity.
- Open the BiometricSetting folder, navigate to the /assets folder.
- In the assets folder, you will find different files, but the key animation files are:
- ```indisplay_fingerprint_touch_effect_green_circle.json```
- ```indisplay_fingerprint_touch_effect_white_circle.json```
- ```indisplay_fingerprint_touch_effect_ripple_circle.json```
- You might need this file or other variants (depending on your fingerprint sensor type, like green, white, or ultrasonic).


**Step 8: Replace Fingerprint Animation Files** 📲
In this step, you'll need to extract the fingerprint animation ZIP you downloaded earlier and replace the required animation files in the correct folder. Here's how to do it:
Steps:
- Go to the Fingerprint Animation Folder:
- Open the ZIP file containing the fingerprint animation files you downloaded.
- Extract the contents to a folder on your computer or internal storage.
- Navigate to the Assets Folder:
- Inside the extracted folder, look for the assets folder. This is where the fingerprint animation files are located.
- Locate the Animation File:
- In the assets folder, look for the following animation file:
- ```indisplay_fingerprint_touch_effect_green_circle.json```
- ```indisplay_fingerprint_touch_effect_white_circle.json```
- ```indisplay_fingerprint_touch_effect_ripple_circle.json```
- Copy the Animation File:
- example purpose Copy the indisplay_fingerprint_touch_effect_green_circle.json file from the animation folder.
- and navigate to ```root/system/priv-app``` and open BiometricSetting.apl and explore or extract it
- navigate to ```/assets``` and replace it that you copy that one
- and replace it 
- You might need this file or other variants (depending on your fingerprint sensor type, like green, white, or ultrasonic).


**Step 9: to Re-Build the BiometricSetting APK**🔨
Hi there! Here’s a complete guide on how to rebuild the BiometricSetting APK after replacing the fingerprint animation files. Please follow the steps below carefully to avoid any issues during the process.
- **Folder Structure Overview**🔩
- After replacing the fingerprint animation files (indisplay_fingerprint_touch_effect_green_circle.json), you should have the following folder structure for your BiometricSetting APK:

- ```/assets:``` Contains assets like fingerprint animation files.

- ```/kotlin:``` Contains Kotlin code files (for app logic).

- ```/META-INF:``` Contains the app’s metadata and signature information.

- ```/res:``` Contains the resources like layout files, images, and UI components.

- ```/SEC-INF:``` Contains security-related files, including signatures.

- ```/AndroidManifest.xml:``` The manifest file defining app permissions and configurations.

- ```/BiometricSetting.apk:``` The main APK file.

- ```/classes.dex:``` The compiled classes in DEX format.

- ```/DebugProbesKt.bin:``` Debugging information (may not be needed for production).

- ```/resource.arsc:``` Contains compiled resources for the app.

- **Steps to Re-Build the APK:**
- Navigate to the Folder Structure
- After modifying the fingerprint animation files, you should have the full folder structure as mentioned above. Ensure you have all the files in their correct locations.
- Compress and Rename the Files
- Select all the files and folders mentioned (i.e., /assets, /kotlin, /META-INF, /res, /SEC-INF, AndroidManifest.xml, BiometricSetting.apk, classes.dex, DebugProbesKt.bin, and resource.arsc).
- Once selected, compress them into a ZIP file.
- After compressing the files, rename the ZIP file to BiometricSetting.apk. This is crucial because the file must have the .apk extension for it to be recognized as an Android APK file.
- **Set the Correct Permissions**
- Ensure that the compressed file has the read/write permissions set correctly.
- Use the following command to set the permissions (if you are using a terminal or command line):
- bash
- Copy code
- ```chmod 755 BiometricSetting.apk```
- This command ensures the file has read/write permissions for the owner and read-only permissions for others
- ```(i.e., rw-r--r--).```
- Store the Compressed APK in Internal Storage
- Make sure to complete all the processes in your internal storage, not in the root directory. This will help avoid potential issues or damage to system files.
- **Rebuild the APK**
- Once you've compressed and set the permissions on the file, your BiometricSetting.apk is ready to be rebuilt.
- Ensure the file is in internal storage before proceeding to the next step.
- Replace the APK in the Root Folder
- - After successfully rebuilding the BiometricSetting APK, you can replace the old BiometricSetting.apk in the /system/priv-app folder with the newly built one.
- Make sure your device is rooted and you have root access before replacing the file.

- **Important Notes:**
- Backup: Before making any changes, always back up your original files to prevent data loss.
- Root Access: This process requires root access to modify system files.
- Permissions: Ensure that all file permissions are set properly to avoid installation issues.

**Thank you for visiting my GitHub page!** :heart:
- I hope you found this process easy to follow and that it helped you understand how to implement the changes. If you liked this project, please feel free to show your support, and I will continue 
 to improve and share more content.

Thank you once again, and your support means a lot to me! You can also connect with me on @Bomb_read.


