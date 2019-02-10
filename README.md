# Android Image Slider [![](https://jitpack.io/v/Mikhail57/AndroidImageSlider.svg)](https://jitpack.io/#Mikhail57/AndroidImageSlider)

This is based on daimajia's work. I changed it to use frescolib, and fixed some memory leaks.
 
This is an amazing image slider for the Android platform. I decided to open source this because there is really not an attractive, convenient slider widget in Android.
 
You can easily load images from any resource using the URI. As it is based on frescolib, read more at http://frescolib.org/docs/supported-uris.html#_

And there are many kinds of amazing animations you can choose. :-D
 
## Demo
 
![](https://giant.gfycat.com/AncientAmusedChinchilla.webm)

[Download Apk](https://github.com/Mikhail57/AndroidImageSlider/releases/download/v1.1.6-beta/demo.apk)
 
## Usage

### Step 1

#### Gradle

Add it in your root build.gradle at the end of repositories:

```groovy
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
```

Step 2. Add the dependency

```groovy
dependencies {
    implementation 'com.github.Mikhail57:AndroidImageSlider:1.1.6-beta'
}
```


### Step 2

Add permissions (if necessary) to your `AndroidManifest.xml`

```xml
<!-- if you want to load images from the internet -->
<uses-permission android:name="android.permission.INTERNET" /> 

<!-- if you want to load images from a file OR from the internet -->
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
```

**Note:** If you want to load images from the internet, you need both the `INTERNET` and `READ_EXTERNAL_STORAGE` permissions to allow files from the internet to be cached into local storage.

If you want to load images from drawable, then no additional permissions are necessary.

### Step 3

Add the Slider to your layout:
 
```xml
<com.daimajia.slider.library.SliderLayout
        android:id="@+id/slider"
        android:layout_width="match_parent"
        android:layout_height="200dp"
/>
```        
 
There are some default indicators. If you want to use a provided indicator:
 
```xml
<com.daimajia.slider.library.Indicators.PagerIndicator
        android:id="@+id/custom_indicator"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:gravity="center"
        />
```

[Code example](https://github.com/chan32167/AndroidImageSlider/blob/master/demo%2Fsrc%2Fmain%2Fjava%2Fcom%2Fdaimajia%2Fslider%2Fdemo%2FMainActivity.java)
 
====
 
## Advanced usage

Please visit [Wiki](https://github.com/Mikhail57/AndroidImageSlider/wiki)
 
## Thanks

- [FrescoLib](https://www.frescolib.org)
- [ViewPagerTransforms](https://github.com/ToxicBakery/ViewPagerTransforms)
