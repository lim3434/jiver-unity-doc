iOS Integration
=======================
### Framework requirements
You need the following frameworks to use JIVER Framework.

* libicucore.dylib
* AdSupport.framework
* MobileCoreServices.framework
* Foundation.framework
* Security.framework
* CFNetwork.framework
* QuartzCore.framework

### Install Framework
Download [JIVER iOS Framework](https://github.com/smilefam/jiver-unity-sample/tree/master/iOSFramework) and drag and drop JiverSDK.framework on to Xcode's Project navigator.


### Enable ARC (required for Manual/CocoaPods)
Enable JIVER Automatic Reference Counting(ARC) in order to use the Framework.

Go to **Build Phases** and **Compile Sources** then add **-fobjc-arc** to the Compiler Flags of **JiveriOS.mm**.
