iOS Integration
=======================
JIVER Unity를 iOS에서 실행하기 위해 iOS 프레임워크와 몇가지 옵션들을 수정해야 합니다.

### Framework Requirements
다음의 Framework들이 필요합니다.

* libicucore.dylib
* MobileCoreServices.framework
* Foundation.framework
* Security.framework
* CFNetwork.framework
* QuartzCore.framework

[Figure 1. Framework requirements]

![Figure 1. Framework requirements](/developer/img/jiver-sdk-001.png)

### 1. Add JIVER iOS Framework
다음 파일을 다운로드 하여 JiverSDK.framework 파일을 Xcode 프로젝트에 추가해 주세요.

[JIVER iOS Framework][jia-ios-latest]

[Figure 2. Add Jiver SDK Framework]

![Figure 2. Add Jiver SDK](/developer/img/jiver-sdk-002.png)

### 2. Set -ObjC Linker Flag 
**Other Link Flags**에 -ObjC 옵션이 추가되어야 합니다.

[Figure 3. Set Other Linker Flags]

![Figure 3. Set Other Linker Flags](/developer/img/jiver-unity-sdk-001.png)

### 3. Enabled Automatic Reference Counting(ARC)
**ARC** 기능을 JiveriOS.mm 파일에 적용합니다.

[Figure 4. Set ARC]

![Figure 4. Set ARC](/developer/img/jiver-unity-sdk-002.png)

### 4. Done

** JIVER Unity를 iOS에서 실행하기 위한 준비가 모두 완료되었습니다. **
