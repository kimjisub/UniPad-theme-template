
# UniPad theme template
유니패드에 적용할 수 있는 테마 앱의 탬플릿입니다.

## 수정해야 될 것들
<img src="img1.png" alt="img1" width="300px"/>

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

## btn.png (32x32)

<img src="/app/src/main/res/drawable/btn.png" alt="btn" width="50px"/>

`버튼의 기본 색상`

## btn_.png (32x32)

<img src="/app/src/main/res/drawable/btn_.png" alt="btn_" width="50px"/>

`버튼이 눌렸을 때의 색상`

---

```
일반모드 : chain.png, chain_.png, chain__.png
chainled 모드 : chainled.png
체인에 LED 이벤트를 지원하기 위해서는 chainled 모드를 사용하여야 합니다.
chainled 파일이 없으면 chain, chain_, chain__ 시스템을 사용합니다.
```

## chainled (180x180)

<img src="/app/src/main/res/drawable/chainled.png" alt="chainled" width="50px"/>

`led 표시를 지원하기 위해서 배경이 채워진 체인`

## chain (180x180)

<img src="/app/src/main/res/drawable/chain.png" alt="chain" width="50px"/>

`기본 체인`

## chain_ (180x180)

<img src="/app/src/main/res/drawable/chain_.png" alt="chain_" width="50px"/>

`선택된 체인`

## chain__ (180x180)

<img src="/app/src/main/res/drawable/chain__.png" alt="chain__" width="50px"/>

`연습모드로 표기될 체인`

---

## prev, play, pause, next, prev_, play_, pause_, next_ (180x180)

```
언더바(_)가 붙지 않은 이미지는 터치되지 않았을 때
언더바가 붙은 이미지는 터치가 됐을 때
```

<img src="/app/src/main/res/drawable/prev.png" alt="prev" width="50px"/><img src="/app/src/main/res/drawable/play.png" alt="play" width="50px"/><img src="/app/src/main/res/drawable/pause.png" alt="pause" width="50px"/><img src="/app/src/main/res/drawable/next.png" alt="next" width="50px"/>

<img src="/app/src/main/res/drawable/prev_.png" alt="prev_" width="50px"/><img src="/app/src/main/res/drawable/play_.png" alt="play_" width="50px"/><img src="/app/src/main/res/drawable/pause_.png" alt="pause_" width="50px"/><img src="/app/src/main/res/drawable/next_.png" alt="next_" width="50px"/>

---

## phantom (180x180)

```
phantom_.png 가 없으면 phantom.png 적용
16*16 이상으로 넘어가면 phantom 적용 X
가로 및 세로의 개수가 모두 짝수이여야 적용
```

<img src="/app/src/main/res/drawable/phantom.png" alt="phantom" width="50px"/>

`버튼 위에 씌우는 이미지`

## phantom_ (180x180)

<img src="/app/src/main/res/drawable/phantom_.png" alt="phantom_" width="50px"/>

`중앙 4개의 버튼 위에 씌우는 이미지`

---

## playbg (unfixed)

<img src="/app/src/main/res/drawable/playbg.png" alt="playbg" width="400px"/>

`배경에 사용될 이미지`

---

## appicon (512x512)

<img src="/app/src/main/res/drawable/appicon.png" alt="appicon" width="200px"/>

`스킨을 나타내는 아이콘, 스킨 앱 아이콘으로 사용됨`

---

## theme_ic (512x512)

<img src="/app/src/main/res/drawable/theme_ic.png" alt="theme_ic" width="200px"/>

`스킨을 나타내는 아이콘, 스킨 선택 창에서 보여짐`

---