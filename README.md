# AndroidSDKPackagesDownloader
Download missing Android SDK packages automatically via Gradle (from dummy project dependencies)

## Purpose

[Auto-download missing packages with Gradle](https://developer.android.com/studio/intro/update.html#download-with-gradle)

> When you run a build from the command line, Gradle can automatically download missing SDK packages that a project depends on, as long as the corresponding SDK license agreements have already been accepted using the SDK Manager.

Downloading SDK packages via Gradle is much easier than downloading by `android update sdk` command.

With `android update sdk` command, every time you have to compose a super long unreadable command, e.g.:

```console
echo "y" | android update sdk --no-ui --all --filter tools,platform-tools,extra-android-m2repository,build-tools-25.0.0,android-25
```

While by Gradle, you just specify all dependencies one by one in [`build.gradle`](https://github.com/thyrlian/AndroidSDKPackagesDownloader/blob/master/app/build.gradle).
