# sa-sdk-android-plugin

The official Android SDK Plugin for Sensors Analytics

## 快速集成

__Gradle 编译环境（Android Studio）__

(1）在 <font color=red size=4 >  **project**  </font>级别的 build.gradle 文件中添加 android-gradle-plugin 依赖：

```android
buildscript {
    repositories {
        jcenter()
    }
    dependencies {
        classpath 'com.android.tools.build:gradle:2.2.3'
        //添加 android-gradle-plugin 依赖
        classpath 'com.sensorsdata.analytics.android:android-gradle-plugin2:1.0.2'
    }
}

allprojects {
    repositories {
        jcenter()
    }
}
```

（2）在 <font color=red size=4 > **主 module** </font>的 build.gradle 文件中添加 com.sensorsdata.analytics.android 插件、Sensors Analytics SDK 依赖及指定 weave 哪些 module：

```android
apply plugin: 'com.android.application'
//添加 com.sensorsdata.analytics.android 插件
apply plugin: 'com.sensorsdata.analytics.android'

dependencies {
   compile 'com.android.support:appcompat-v7:25.1.1'
   //添加 Sensors Analytics SDK 依赖
   compile 'com.sensorsdata.analytics.android:SensorsAnalyticsSDK:1.8.6'
}
```

*注*：
1、由于 SDK 会依赖 appcompat-v7 处理下面几个控件：

* android.support.v7.widget.SwitchCompat
* android.support.v7.app.AlertDialog

需要添加下面依赖( 如果项目中已引入了 v7包，可以不添加 )：

```android
compile 'com.android.support:appcompat-v7:25.1.1'
```

## 感谢
[hugo](https://github.com/JakeWharton/hugo)

[gradle_plugin_android_aspectjx](https://github.com/HujiangTechnology/gradle_plugin_android_aspectjx)

[gradle-android-aspectj-plugin](https://github.com/uPhyca/gradle-android-aspectj-plugin)

[tracklytics](https://github.com/orhanobut/tracklytics)

## To Learn More

See our [full manual](http://www.sensorsdata.cn/manual/android_sdk.html)

## License

Copyright 2015－2017 Sensors Data Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.gradle_plugin_android_aspectjx
