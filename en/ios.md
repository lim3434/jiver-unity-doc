iOS Integration
=======================
### 1. Install from CocoaPods
You can install the JIVER framework using CocoaPods.

#### PodFiles
Add below into your Podfile on Xcode.
```
pod 'JiverSDK'
```

Install JIVER Framework through CocoaPods.
```
# pod install
```

Now you can see installed JIVER framework by inspecting *YOUR_PROJECT*.xcworkspace.


### 2. Manual Install
### Framework requirements
You need the following frameworks to use JIVER Framework.

* libicucore.dylib
* MobileCoreServices.framework
* Foundation.framework
* Security.framework
* CFNetwork.framework
* QuartzCore.framework

### Install Framework
1\. Download [JIVER iOS Framework](download_sdk.html) and drag and drop JiverSDK.framework in the .tar.gz on to Xcode's Project navigator.


~~2\.Select Build Settings tab, Set $(OTHER_LDFLAGS) -ObjC values to Other Linker Flags for Linking.~~

~~[Refer to: How do I fix "selector not recognized" runtime exceptions when trying to use category methods from a static library?](https://developer.apple.com/library/mac/qa/qa1490/_index.html)~~**(v1.1.28 and later don't require this option.)**


### 3. Enable ARC (required for Manual/CocoaPods)
Enable JIVER Automatic Reference Counting(ARC) in order to use the Framework. Go to your project's **Build Settings**, then either

1) **Objective-C Automatic Reference Counting**'s value to **Yes** in the **Apple LVMM 6.1 - Language - Objective C** 

or, 

2) Go to **Build Phases** and **Compile Sources** then add **-fobjc-arc** to the Compiler Flags in the source file that will be using JIVER Framework.

![Set ARC](https://raw.githubusercontent.com/smilefam/jiver-igaw-ios-doc/master/file/jiver-sdk-006.png)
