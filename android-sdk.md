# Android SDK

The [Android SDK](https://developer.android.com/tools) is composed of multiple packages that are required for Android application development.

## Optional: Relocate user-specific files

User-specific files, especially large virtual device files, can be relocated using [environment variables](https://developer.android.com/tools/variables):

```powershell
[System.Environment]::SetEnvironmentVariable('ANDROID_USER_HOME','<.android folder path>', 'User')
[System.Environment]::SetEnvironmentVariable('ANDROID_EMULATOR_HOME','%ANDROID_USER_HOME%', 'User')
```

## Command-line tools

[Android SDK Command-line tools](https://developer.android.com/tools) can be installed using [Scoop](scoop.md):

```shell
scoop install main/android-clt
```

## Build tools and target platforms

Android [build tools](https://developer.android.com/tools/releases/build-tools) and target [platform](https://developer.android.com/guide/platform) can be installed using [sdkmanager](https://developer.android.com/tools/sdkmanager):

```shell
sdkmanager --install "build-tools;35.0.0" "platforms;android-35" "sources;android-35"
```

## Emulator and virtual devices

Android [emulator](https://developer.android.com/studio/run/emulator-commandline), [platform tools](https://developer.android.com/tools/releases/platform-tools) and [system images](https://developer.android.com/guide/platform) can be installed using [sdkmanager](https://developer.android.com/tools/sdkmanager):

```shell
sdkmanager --install "emulator" "platform-tools" "system-images;android-35;google_apis;x86_64"
```

A virtual device can be created using [avdmanager](https://developer.android.com/tools/avdmanager):

```shell
avdmanager create avd --name phone --device medium_phone --package "system-images;android-35;google_apis;x86_64"
avdmanager create avd --name tablet --device medium_tablet --package "system-images;android-35;google_apis;x86_64"
```

A virtual device can be started using [emulator](https://developer.android.com/studio/run/emulator-commandline):

```shell
& $Env:ANDROID_HOME\emulator\emulator -avd phone
& $Env:ANDROID_HOME\emulator\emulator -avd tablet
```
