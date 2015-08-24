iOS Integration
=======================
### 1. CocoaPods으로 설치
JIVER Framework은 CocoaPods을 통해서 설치할 수 있습니다. CocoaPods를 사용하면 직접 다운로드하는 과정은 보실 필요가 없습니다. CocoaPods 설치 및 사용법은 [CocoaPods 웹사이트](https://guides.cocoapods.org/using/using-cocoapods.html)에서 확인하시기 바랍니다.

#### Podfiles
Xcode 프로젝트 디렉토리의 Podfile에 아래와 같이 추가합니다.
```
pod 'JiverSDK'
```

CocoaPods을 통해서 JIVER Framework을 설치합니다.
```
# pod install
```

*YOUR_PROJECT*.xcworkspace를 열면 JIVER Framework이 설치된 것을 확인할 수 있습니다.

### 2. 직접 다운로드
CocoaPods을 사용할 수 없는 경우, JIVER Framework을 [이곳](https://github.com/smilefam/jiver-ios-framework)에서 받을 수 있습니다.

JIVER Framework을 다운로드 받아서 사용하려면 몇 가지 추가 설정이 필요합니다.

#### 필수 Framework 설치
JIVER Framework을 사용하기 위해서 Xcode 프로젝트에 다음의 Framework을 추가해야 합니다.

* libicucore.dylib
* MobileCoreServices.framework
* Foundation.framework
* Security.framework
* CFNetwork.framework
* QuartzCore.framework

#### JIVER Framwork 설치
1\. 다운로드한 JIVER Framework를 Xcode 프로젝트에 추가합니다.

~~2\. **Build Settings** 탭을 선택한 후, **Linking**의 **Other Linker Flags**에 **$(OTHER_LDFLAGS) -ObjC** 값을 설정합니다.
[참고 자료: How do I fix "selector not recognized" runtime exceptions when trying to use category methods from a static library?](https://developer.apple.com/library/mac/qa/qa1490/_index.html)
~~(v1.1.28 버전부터 이 옵션을 추가할 필요가 없습니다.)

### 3. 공통 설정
JIVER Framework을 사용하기 위해서 Automatic Reference Counting(ARC)를 활성화해야 합니다. 프로젝트의 **Build Settings**에서 **Apple LVMM 6.1 - Language - Objective C**의 **Objective-C Automatic Reference Counting**을 **Yes**로 변경하거나, **Build Phases**의 **Compile Sources**에서 JIVER Framework를 사용하는 소스 파일의 Compiler Flags에 **-fobjc-arc**를 추가합니다.

![ARC 설정](https://raw.githubusercontent.com/smilefam/jiver-igaw-ios-doc/master/file/jiver-sdk-006.png)
