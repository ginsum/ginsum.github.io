---
layout : post
title : "사이드프로젝트02 - react native navigation02"
comments: true
---

### 리액트 네이티브 - 네비게이션 구현 


<br/>
<br/>
##### Stack navigation

[참고 페이지]("https://reactnavigation.org/docs/en/next/stack-navigator.html")

<br/>
<br/>
```
import {createStackNavigator} from '@react-navigation/stack';

const Stack = createStackNavigator();
function LoginStack() {
  return (
    <Stack.Navigator>
      <Stack.Screen name="login" component={Login} />
      <Stack.Screen name="signup" component={Signup} />
    </Stack.Navigator>
  );
}
```

##### Bottom Tab navigation

[참고 페이지]("https://reactnavigation.org/docs/en/next/bottom-tab-navigator.html")

<br/>
<br/>
```
import {createBottomTabNavigator} from '@react-navigation/bottom-tabs';
const Tab = createBottomTabNavigator();

const HomeTab = () => {
  return (
    <Tab.Navigator>
      <Tab.Screen name="home" component={Home} />
      <Tab.Screen name="tab1" component={Tab1} />
    </Tab.Navigator>
  );
};
```

##### Navigation Container

[참고페이지]("https://reactnavigation.org/docs/en/next/hello-react-navigation.html")

<br/>
<br/>
```
import * as React from 'react';
import { View, Text } from 'react-native';
import { NavigationNativeContainer } from '@react-navigation/native';
import { createStackNavigator } from '@react-navigation/stack';

function HomeScreen() {
  return (
    <View style={{ flex: 1, alignItems: 'center', justifyContent: 'center' }}>
      <Text>Home Screen</Text>
    </View>
  );
}

const Stack = createStackNavigator();

function App() {
  return (
    <NavigationNativeContainer>
      <Stack.Navigator>
        <Stack.Screen name="Home" component={HomeScreen} />
      </Stack.Navigator>
    </NavigationNativeContainer>
  );
}

export default App;
```

