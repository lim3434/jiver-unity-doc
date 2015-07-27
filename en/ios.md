iOS Integration
=======================
You need to setup some frameworks and options to work JIVER properly on iOS.

### Framework Requirements
You need the following frameworks to use JIVER Framework.

* libicucore.dylib
* MobileCoreServices.framework
* Foundation.framework
* Security.framework
* CFNetwork.framework
* QuartzCore.framework

[Figure 1. Framework requirements]

![Figure 1. Framework requirements](/developer/img/jiver-sdk-001.png)

### 1. Add JIVER iOS Framework
Download [JIVER iOS Framework][jia-ios-latest] and drag and drop JiverSDK.framework in the .tar.gz on to Xcode's Project navigator.

[Figure 2. Add Jiver SDK Framework]

![Figure 2. Add Jiver SDK](/developer/img/jiver-sdk-002.png)

### 2. Set -ObjC Linker Flag 
Select **Build Settings** tab, Set **$(OTHER_LDFLAGS) -ObjC** values to **Other Linker Flags** for **Linking**.

[Figure 3. Set Other Linker Flags]

![Figure 3. Set Other Linker Flags](/developer/img/jiver-unity-sdk-001.png)

### 3. Enabled Automatic Reference Counting(ARC)

You need to ** enable ARC ** on JiveriOS.mm.

[Figure 4. Set ARC]

![Figure 4. Set ARC](/developer/img/jiver-unity-sdk-002.png)

### 4. Done

** jiver is ready to go on ios. **
