# 简单安卓应用

这是一个使用GitHub Actions进行自动构建的简单安卓应用程序。

## 功能特点

- 简单的点击计数器应用
- 现代化的Material Design界面
- 自动构建和测试流程

## 项目结构

```
.
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/example/simpleapp/
│   │   │   │   └── MainActivity.java
│   │   │   ├── res/
│   │   │   │   ├── layout/
│   │   │   │   │   └── activity_main.xml
│   │   │   │   ├── values/
│   │   │   │   │   └── strings.xml
│   │   │   │   └── mipmap-*/
│   │   │   └── AndroidManifest.xml
│   │   └── test/
│   └── build.gradle
├── .github/
│   └── workflows/
│       └── android-build.yml
├── gradle/
│   └── wrapper/
├── build.gradle
├── settings.gradle
├── gradle.properties
└── gradlew
```

## 本地构建

1. 确保已安装JDK 11或更高版本
2. 克隆项目
3. 运行以下命令：

```bash
chmod +x gradlew
./gradlew build
```

## GitHub Actions

项目配置了GitHub Actions工作流，会在以下情况自动触发：
- 推送到main/master分支
- 创建拉取请求

工作流会执行以下操作：
1. 构建应用
2. 运行单元测试
3. 上传构建产物（APK文件）

## 应用功能

- 显示欢迎消息
- 点击按钮增加计数
- 显示Toast提示

## 技术栈

- **语言**: Java
- **最低SDK版本**: 21 (Android 5.0)
- **目标SDK版本**: 33 (Android 13)
- **构建工具**: Gradle
- **UI框架**: Android原生组件 + Material Design