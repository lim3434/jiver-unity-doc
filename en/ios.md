Install JIVER Framework 
=======================
### Framework requirements
You need the following frameworks to use JIVER Framework.

* libicucore.dylib
* MobileCoreServices.framework
* Foundation.framework
* Security.framework
* CFNetwork.framework
* QuartzCore.framework

[Figure 1. Framework requirements]

![Figure 1. Framework requirements](https://raw.githubusercontent.com/smilefam/jiver-ios-doc/master/file/jiver-sdk-001.png)

### Install Framework
1\. Download [JIVER iOS Framework](download_sdk.html) or [JIVER iOS Framework with Prebuilt UI](download_sdk.html) and drag and drop JiverSDK.framework in the .tar.gz on to Xcode's Project navigator.

** For Prebuilt UI **

You can copy either JiverMessagingViewController.\*, or JiverChatViewController.\*, or both into your project depending on features you want to use. 
** JiverCommon.* must be included for the view controllers. **

[Figure 2. Add Jiver SDK Framework]

![Figure 2. Add Jiver SDK](https://raw.githubusercontent.com/smilefam/jiver-ios-doc/master/file/jiver-sdk-002.png)

2\.Select **Build Settings** tab, Set **$(OTHER_LDFLAGS) -ObjC** values to **Other Linker Flags** for **Linking**.
[Refer to: How do I fix "selector not recognized" runtime exceptions when trying to use category methods from a static library?](https://developer.apple.com/library/mac/qa/qa1490/_index.html)

[Figure 3. Set Other Linker Flags]

![Figure 3. Set Other Linker Flags](https://raw.githubusercontent.com/smilefam/jiver-ios-doc/master/file/jiver-sdk-003.png)

3\. Enable JIVER Automatic Reference Counting(ARC) in order to use the Framework and Prebuilt-UI. Go to your project's **Build Settings**, then either 1) **Objective-C Automatic Reference Counting**'s value to **Yes** in the **Apple LVMM 6.1 - Language - Objective C** or, 2) Go to **Build Phases** and **Compile Sources** then add **-fobjc-arc** to the Compiler Flags in the source file that will be using JIVER Framework.

[Figure 4. Set ARC]

![Figure 4. Set ARC](https://raw.githubusercontent.com/smilefam/jiver-ios-doc/master/file/jiver-sdk-006.png)
