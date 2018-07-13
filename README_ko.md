# UniPad theme template
Templates for theme apps that can be applied to UniPad.

## Files to remake
<img src="images/img1.png" alt="img1" width="300px"/>

## Theme Structure
<img src="images/unipad-ui-structure-extended.png" alt="unipad-ui-structure-extended" width="500px"/>

---

## string.xml
```xml
<resources>
	<string name="app_name">UniPad theme template</string>

	<string name="theme_name">UniPad - Theme template</string>
	<string name="theme_description">This is theme template</string>
	<string name="theme_author">UniPad</string>
</resources>
```

---

## color.xml
```xml
<resources>
	<!--skin-->
	<color name="checkbox">#a6b4c9</color>
	<color name="trace_log">#161e2b</color>
	<color name="option_window">#FFFFFF</color>
	<color name="option_window_checkbox">#414F66</color>
	<color name="option_window_btn">#d6d8d7</color>
	<color name="option_window_btn_text">#0f0f0f</color>
	
	<!--app color-->
	<color name="app_orange">#ff8f00</color>
	<color name="app_blue">#00b8d4</color>
	<color name="app_blue_dark">#009db5</color>
</resources>
```

---

## build.gradle (Module: app)
```javascript
apply plugin: 'com.android.application'

android {
    compileSdkVersion 26
    defaultConfig {
        applicationId "com.kimjisub.launchpad.theme.template"   //change this
        minSdkVersion 16
        targetSdkVersion 26
        versionCode 1                                           //change this
        versionName "1.0.0"                                     //change this
        testInstrumentationRunner "android.support.test.runner.AndroidJUnitRunner"
    }
    buildTypes {
        release {
            minifyEnabled false
            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
        }
    }
}
```

---

## btn (32x32)

<img src="/app/src/main/res/drawable/btn.png" alt="btn" width="50px"/>

`The default color of the pad`

## btn_ (32x32)

<img src="/app/src/main/res/drawable/btn_.png" alt="btn_" width="50px"/>

`The color when the button is pressed`

---

```
Put only resources for the system you are using.
If all 4 resources are present, it will work by chainled mode.
```

## chain, chain_, chain__ (180x180) Normal Mode

<img src="/app/src/main/res/drawable/chain.png" alt="chain" width="50px"/><img src="/app/src/main/res/drawable/chain_.png" alt="chain_" width="50px"/><img src="/app/src/main/res/drawable/chain__.png" alt="chain__" width="50px"/>

`The basic chain, the selected chain, the chain to be marked as the practice mode`

## chainled (180x180) Chainled Mode

<img src="/app/src/main/res/drawable/chainled.png" alt="chainled" width="50px"/>

`To support the LED display, the background filled chain image`

---

## prev, play, pause, next, prev_, play_, pause_, next_ (180x180)

```
aaaa  : not touched yet.
aaaa_ : While touching.
```

<img src="/app/src/main/res/drawable/prev.png" alt="prev" width="50px"/><img src="/app/src/main/res/drawable/play.png" alt="play" width="50px"/><img src="/app/src/main/res/drawable/pause.png" alt="pause" width="50px"/><img src="/app/src/main/res/drawable/next.png" alt="next" width="50px"/>

<img src="/app/src/main/res/drawable/prev_.png" alt="prev_" width="50px"/><img src="/app/src/main/res/drawable/play_.png" alt="play_" width="50px"/><img src="/app/src/main/res/drawable/pause_.png" alt="pause_" width="50px"/><img src="/app/src/main/res/drawable/next_.png" alt="next_" width="50px"/>

---

## phantom (180x180)

```
If Phantom_.png is not exist, apply phantom.png
If the unipack size is over 16 * 16, it will not apply
Both horizontal and vertical numbers must be even number
```

<img src="/app/src/main/res/drawable/phantom.png" alt="phantom" width="50px"/>

`Image over pad`

## phantom_ (180x180)

<img src="/app/src/main/res/drawable/phantom_.png" alt="phantom_" width="50px"/>

`Images put over the center 4 pad`

---

## playbg (unfixed)

<img src="/app/src/main/res/drawable/playbg.png" alt="playbg" width="400px"/>

`Images to be used in the background`

## custom_logo (unfixed)

<img src="/app/src/main/res/drawable/custom_logo.png" alt="custom_logo" width="200px"/>

`Logo on top right, disappear when not exist this file`

---

## appicon (512x512)

<img src="/app/src/main/res/drawable/appicon.png" alt="appicon" width="200px"/>

`Icons representing skin, used as skin app icons`

---

## theme_ic (512x512)

<img src="/app/src/main/res/drawable/theme_ic.png" alt="theme_ic" width="200px"/>

`Icon representing skin, shown in skin selection window`

---
