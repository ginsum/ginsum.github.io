---
layout : post
title : "사이드프로젝트01-1 - react native navigation01(next 버전)"
comments: true
---

### 리액트 네이티브 - 네비게이션 설치 

(이전 버선 설치해서 next 버전으로 다시 설치했습니다.)
<br/>
<br/>
##### install

[참고 페이지]("https://reactnavigation.org/docs/en/next/getting-started.html")

<br/>
<br/>
```
yarn add @react-navigation/native@next
```

createStackNavigator 을 위한 사용하기 위해 설치

<br/>
```
yarn add @react-navigation/native@next @react-navigation/stack@next @react-native-community/masked-view

```
Now we need to install react-native-gesture-handler, react-native-screens and react-native-safe-area-context
<br/>
expo 사용 안해서 다음과 같이 설치
```
yarn add react-native-gesture-handler react-native-screens react-native-safe-area-context
```

<br/>
React Native 0.60 and higher
android/app/build.gradle 파일에 추가

```
implementation 'androidx.appcompat:appcompat:1.1.0-rc01'
implementation 'androidx.swiperefreshlayout:swiperefreshlayout:1.1.0-alpha02'

```

<br/>
<br/>

MainActivity.java 파일 수정

```

package com.reactnavigation.example;

import com.facebook.react.ReactActivity;
+ import com.facebook.react.ReactActivityDelegate;
+ import com.facebook.react.ReactRootView;
+ import com.swmansion.gesturehandler.react.RNGestureHandlerEnabledRootView;

public class MainActivity extends ReactActivity {

  @Override
  protected String getMainComponentName() {
    return "Example";
  }

+  @Override
+  protected ReactActivityDelegate createReactActivityDelegate() {
+    return new ReactActivityDelegate(this, getMainComponentName()) {
+      @Override
+      protected ReactRootView createRootView() {
+       return new RNGestureHandlerEnabledRootView(MainActivity.this);
+      }
+    };
+  }
}

```
<br/>
<br/>

createBottomTabNavigator

```
yarn add @react-navigation/native@next @react-navigation/bottom-tabs@next
```

<br/>
<br/>

-> stack 과 botoomtap 네비까지 설치 




