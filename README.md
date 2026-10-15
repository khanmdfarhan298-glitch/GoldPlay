# Gold Club Android starter (Kotlin)

This is an original, BDG-Win-inspired visual prototype. It is not affiliated with BDG Win. It contains no real-money betting, no real wallet, no payment processing, and no backend.

## Open and run
1. Download and unzip `GoldClubAndroid.zip`.
2. Install Android Studio (current stable version).
3. In Android Studio choose **Open** and select the unzipped `GoldClubAndroid` folder (the one containing `settings.gradle.kts`).
4. Allow Gradle sync to finish. If Android Studio asks to install Android SDK Platform 35 or a compatible build tools version, accept.
5. Create an emulator via **Tools > Device Manager > Create Device**, or connect an Android phone with USB debugging enabled.
6. Press the green **Run ▶** button and select the `app` configuration/device.
7. To create an APK: **Build > Build Bundle(s) / APK(s) > Build APK(s)**. Android Studio will show a link to the generated APK.

## Add your own QR image (UI only)
1. Put your payment QR image in `app/src/main/res/drawable/` and name it `my_payment_qr.png` (lowercase filename).
2. In `MainActivity.kt`, replace the placeholder `TextView` in `depositPage()` with an `ImageView` using `resources.getDrawable(R.drawable.my_payment_qr, theme)`.
3. This only displays the QR. It does not verify that payment arrived. For a live payment flow, use a compliant payment provider and verify payment server-side. Never store UPI PINs, OTPs, or bank passwords in the app.

## Troubleshooting
- If Gradle sync fails, check internet access and use Android Studio's suggested compatible Gradle/JDK setup.
- The project uses Android Gradle Plugin 8.7.3 and Kotlin 2.0.21; Android Studio may suggest updating plugin versions if your installation is much newer.
