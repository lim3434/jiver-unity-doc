iOS Integration
=======================

JIVER Framework을 다운로드 받아서 사용하려면 몇 가지 추가 설정이 필요합니다.

#### 필수 Framework 설치
JIVER Framework을 사용하기 위해서 Xcode 프로젝트에 다음의 Framework을 추가해야 합니다.

* libicucore.dylib
* AdSupport.framework
* MobileCoreServices.framework
* Foundation.framework
* Security.framework
* CFNetwork.framework
* QuartzCore.framework

#### JIVER Framwork 설치
다운로드한 [JIVER Framework](https://github.com/smilefam/jiver-unity-sample/tree/master/iOSFramework)를 Xcode 프로젝트에 추가합니다.

### 공통 설정
JIVER Framework을 사용하기 위해서 Automatic Reference Counting(ARC)를 활성화해야 합니다. 

**Build Phases**의 **Compile Sources**에서 JIVER Framework를 **JiveriOS.mm** 파일의 Compiler Flags에 **-fobjc-arc**를 추가합니다.
