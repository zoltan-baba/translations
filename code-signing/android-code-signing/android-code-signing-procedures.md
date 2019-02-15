---
title: Android のコード署名の手続き
menu:
  android-code-signing:
    weight: 1
---
[Google Play Store](https://play.google.com/store/apps)でアプリを配布する前に、APKファイルに署名をする必要があります。

code signingの設定は、Android Studioで記述することも、Gradleに手動で記述することも出来ます。Bitrise Workflow Editorで`sign-apk` stepを使用することで、APKを自動で署名することも出来ます。  

様々なAndroid code signingの方法

* [Android Studio でコード署名](/code-signing/android-code-signing/android-code-signing-with-android-studio/)
* [Gradle でコード署名](/code-signing/android-code-signing/android-code-signing-in-gradle/) 
* [Bitrise Sign APK ステップを使用したコード署名](/code-signing/android-code-signing/android-code-signing-using-bitrise-sign-apk-step/)
