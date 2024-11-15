# Fresco SVG Support

## Gradle

```kotlin
implementation("com.facebook.fresco:fresco:3.4.0")
implementation("com.facebook.fresco:middleware:3.4.0")
implementation("com.caverock:androidsvg:1.4")
```

## Init

```kotlin
val imageDecoderConfig = ImageDecoderConfig.newBuilder()
            .addDecodingCapability(
                SvgDecoderExample.SVG_FORMAT,
                SvgDecoderExample.SvgFormatChecker(),
                SvgDecoderExample.SvgDecoder()
            )
            .build()
        val config = ImagePipelineConfig.newBuilder(this)
            .setDownsampleEnabled(true)
            .setImageDecoderConfig(imageDecoderConfig)
            .build()
        val draweeConfig = DraweeConfig.newBuilder()
            .addCustomDrawableFactory(SvgDecoderExample.SvgDrawableFactory())
            .build()
        Fresco.initialize(this, config, draweeConfig)
```

["SvgDecoderExample" Source Code](https://github.com/facebook/fresco/blob/main/samples/showcase/src/main/java/com/facebook/fresco/samples/showcase/imageformat/svg/SvgDecoderExample.java)

## proguard-rules.pro

```
-keep class com.caverock.androidsvg.** { *; }
-dontwarn com.caverock.androidsvg.**
```

## Ref

https://code.luasoftware.com/tutorials/android/android-fresco-load-svg-drawable/
https://github.com/facebook/fresco/issues/2714
