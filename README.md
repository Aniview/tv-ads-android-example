# TV-Ads Example

This project contains a minimal example application to start displaying Ads with Aniview's TV-Ads library.


## How to configure fresh project
Here are steps to configure a fresh project:

1. Add Maven repository in the `settings.gradle.kts` file:
```kts
dependencyResolutionManagement {
    repositories {
        maven("https://us-central1-maven.pkg.dev/mobile-sdk-fd2e4/adservr-maven")
    }
}
```

2. Add Maven dependencies in the app's `build.gradle.kts` file:
```kts
dependencies {
    implementation("com.adservrs:tv-ads:1.0.0-beta01")
}
```

3. Add `TvAdView` in the code:
```kotlin
val view = TvAdView(context)
view.load(AdaConfig(
    pubId = "published id",
    tagId = "tag id",
))
parent.addView(view)
```

4. Add Google Mobile Ads application ID to `AndroidManifest.xml`:
```xml
<manifest>
    <application>
        <meta-data
            android:name="com.google.android.gms.ads.APPLICATION_ID"
            android:value="ca-app-pub-6746653557725812~6678258028"/>
    </application>
</manifest>
```
