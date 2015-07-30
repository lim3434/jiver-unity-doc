iOS Integration
=======================
### Framework 요구 사항
JIVER Framework를 사용하기 위해서 다음의 Framework가 필요합니다.

* libicucore.dylib
* MobileCoreServices.framework
* Foundation.framework
* Security.framework
* CFNetwork.framework
* QuartzCore.framework

[Figure 1. 필수 Framework]

![Figure 1. 필수 Framework](https://raw.githubusercontent.com/smilefam/jiver-ios-doc/master/file/jiver-sdk-001.png)


### Install Framework
1\. [JIVER iOS Framework][jia-latest] 또는 [JIVER iOS Framework with Prebuilt UI][jia-prebuilt-latest] 를 다운받은 후, 압축 파일에 포함된 JiverSDK.framework를 Project navigator에 추가합니다.

[Figure 2. Jiver SDK Framework 추가]

![Figure 2. Jiver SDK 추가](https://raw.githubusercontent.com/smilefam/jiver-ios-doc/master/file/jiver-sdk-002.png)

2\. **Build Settings** 탭을 선택한 후, **Linking**의 **Other Linker Flags**에 **$(OTHER_LDFLAGS) -ObjC** 값을 설정합니다.
[참고 자료: How do I fix "selector not recognized" runtime exceptions when trying to use category methods from a static library?](https://developer.apple.com/library/mac/qa/qa1490/_index.html)

[Figure 3. Other Linker Flags 값 설정]

![Figure 3. Other Linker Flags 값 설정](https://raw.githubusercontent.com/smilefam/jiver-ios-doc/master/file/jiver-sdk-003.png)

3\. JIVER Framework와 Prebuilt-UI를 사용하기 위해서 Automatic Reference Counting(ARC)를 활성화해야 합니다. 프로젝트의 **Build Settings**에서 **Apple LVMM 6.1 - Language - Objective C**의 **Objective-C Automatic Reference Counting**을 **Yes**로 변경하거나, **Build Phases**의 **Compile Sources**에서 JIVER Framework를 사용하는 소스 파일의 Compiler Flags에 **-fobjc-arc**를 추가합니다.

[Figure 4. ARC 설정]

![Figure 4. ARC 설정](https://raw.githubusercontent.com/smilefam/jiver-ios-doc/master/file/jiver-sdk-006.png)

