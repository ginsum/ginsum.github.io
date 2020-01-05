---
layout : post
title : "사이드프로젝트01 - react native navigation01"
comments: true
---

### 리액트 네이티브 - 네비게이션 설치 


<br/>
<br/>
##### install

[참고 페이지]("https://reactnavigation.org/docs/en/getting-started.html")

<br/>
<br/>
```
yarn add react-navigation

```

expo 사용하지 않고 진행하고 있기 때문에 아래같이 추가 설치

<br/>
```
yarn add react-native-reanimated react-native-gesture-handler react-native-screens react-native-safe-area-context

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
마지막에 에러코드 떠서 추가 설치

```
npm i @react-native-community/masked-view

```
<br/>
<br/>
-> Stack Navigator 는 잘 뜨는 것을 확인




