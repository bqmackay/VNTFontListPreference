VNTFontListPreference
=====================

[![Build Status](https://travis-ci.org/vanniktech/VNTFontListPreference.svg?branch=master)](https://travis-ci.org/vanniktech/VNTFontListPreference?branch=master)
[![Codecov](https://codecov.io/github/vanniktech/VNTFontListPreference/coverage.svg?branch=master)](https://codecov.io/github/vanniktech/VNTFontListPreference?branch=master)
[![API](https://img.shields.io/badge/API-14%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=14)
<a href="http://www.methodscount.com/?lib=com.vanniktech%3Avntfontlistpreference%3A1.0.0"><img src="https://img.shields.io/badge/Methods count-75-e91e63.svg"></img></a>
<a href="http://www.methodscount.com/?lib=com.vanniktech%3Avntfontlistpreference%3A1.0.0"><img src="https://img.shields.io/badge/Size-10 KB-e91e63.svg"></img></a>
[![License](http://img.shields.io/:license-apache-blue.svg)](http://www.apache.org/licenses/LICENSE-2.0.html)
[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-VNTFontListPreference-brightgreen.svg?style=flat)](https://android-arsenal.com/details/1/798)
[![Jit Pack](https://img.shields.io/github/tag/vanniktech/VNTFontListPreference.svg?label=JitPack%20Maven)](https://jitpack.io/#vanniktech/VNTFontListPreference)
[![](https://img.shields.io/badge/AndroidWeekly-%23111-blue.svg)](http://androidweekly.net/issues/issue-111)

This is an easy to use custom preference, which opens a dialog with a list of available fonts. The selected font gets automatically saved and you are able to set the font directory as well as the defaultValue.

```xml
<com.vanniktech.vntfontlistpreference.VNTFontListPreference
    android:defaultValue="@string/font_face_default_value"
    android:key="preference_font_face"
    android:title="@string/font_face"
    app:vnt_fontDirectory="@string/font_face_font_directory" />
```

`vntfontlistpreference:vnt_fontDirectory` can be something like `fonts`. This means that the dialog will list all fonts, that have the ending `ttf` or `otf` under `assets/fonts`. If there are no fonts under the provided directory it will throw an exception during initialization.

# Download Sample App

[![Get it on Google Play](https://developer.android.com/images/brand/en_generic_rgb_wo_45.png)](https://play.google.com/store/apps/details?id=com.vanniktech.vntfontlistpreference.sample)

or scan the code on your mobile

![Google Play QR link](http://api.qrserver.com/v1/create-qr-code/?color=000000&bgcolor=FFFFFF&data=https%3A%2F%2Fplay.google.com%2Fstore%2Fapps%2Fdetails%3Fid%3Dcom.vanniktech.vntfontlistpreference.sample&qzone=1&margin=0&size=150x150&ecc=L)

or download it [directly](sample.apk)

# Setup

**build.gradle**

```groovy
compile 'com.vanniktech:vntfontlistpreference:1.0.0'
compile 'com.vanniktech:vntfontlistpreference:1.0.1-SNAPSHOT'
```

Modules are located on [Maven Central](https://oss.sonatype.org/#nexus-search;quick~vntfontlistpreference).

Go to your preference XML file and insert the above mentioned XML tag. Afterwards you are good to go and can run your project!

# Get default font

```java
final SharedPreferences sharedPreferences = PreferenceManager.getDefaultSharedPreferences(this);
final String defaultFont = sharedPreferences.getString("preference_font_face", this.getString(R.string.font_face_default_value));
final Typeface typeface = Typeface.createFromAsset(this.getAssets(), font);
```

# Proguard

No configuration needed.

# Preview

<img src="app/src/main/res/drawable-nodpi/preview.png" alt="Image of VNTFontListPreference" width="320">

# License

Copyright (C) 2014-2016 Vanniktech - Niklas Baudy

Licensed under the Apache License, Version 2.0