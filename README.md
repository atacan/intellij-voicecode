# IntelliJ support for VoiceCode (IDE plugin)

<!-- Plugin description -->

This plugin adds a small web server which supports a Talon module, but can be used generically as an
HTTP based RPC driven by any system on the same machine.

<!-- Plugin description end -->

This adds [VoiceCode](https://voicecode.io) support for IntelliJ, in tandem with [this VoiceCode package](https://github.com/anonfunc/voicecode-intellij).

This should support:

- Android Studio
- AppCode
- CLion
- DataGrip
- GoLand
- MPS
- PhpStorm
- PyCharm (Professional and Community editions)
- RubyMine
- WebStorm

## IDE Major Version Update

Change the following according to the versions found in the URL in the file gradle.properties

```yaml
pluginSinceBuild = 231
pluginUntilBuild = 231.*
...
platformVersion = 2023.2
```

Change the plugin version in the file `build.gradle.kts`

```kotlin
// Gradle IntelliJ Plugin
id("org.jetbrains.intellij") version "1.13.3"
// Gradle Changelog Plugin
id("org.jetbrains.changelog") version "2.0.0"
```

## Building

```bash
./gradlew build
```

## Installing

The above build command generates a zip file in `build/distributions/`. You can install this zip file in IntelliJ by going to `File > Settings > Plugins > Install Plugin from Disk...`.

## Testing uncommitted changes

    ./gradlew runIde
