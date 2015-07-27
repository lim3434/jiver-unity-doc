Setup JIVER
============================
### 1. Import JIVER 
JIVER SDK를 Asset Store에서 다운로드하여 쉽게 Unity 프로젝트에 포함시킬 수 있습니다.

다운로드 받은 파일을 Unity Project에서 Import 합니다. 

[Download JIVER Unity Plugin >][jia-latest]

![img-import]


### 2. Directory Structure
``` xml
.
| Plugins
    | Android
        | jiver-android-*.jar               // JIVER Adnroid SDK
    | iOS
        | JiveriOS.*                        // JIVER iOS Plugin
    | JIVER
        | Assets
            | *                             // Jiver common Assets
        | Sample
            | JiverMain.cs                  // Jiver Sample Main Class
            | JIVERMain.prefab              // Sample Prefab object with the JiverMain class
        | SDK
            | Jiver.cs                      // Jiver SDK class
            | JIVER.prefab                  // JIVER SDK Prefab with Jiver class
            | JiverUI.cs                    // Prebuilt Jiver Responder class
            | JIVERUI.prefab                // Prebuilt Jiver UI prefab with JiverUI class.
            | SimpleJSON.cs                 // JSON Library for JIVER
        | Themes
            | ...                           // Jiver UI Theme Assets
```

### 3. Create JIVER Prefab Object
![img-create-jiver-prefab]

### 4. Create Prebuilt JIVER UI
![img-create-jiver-ui-prefab]

### 5. Choose UI Theme
![Theme1](/developer/files/unity/unity_ui_tn_beige_crema.jpg)
![Theme2](/developer/files/unity/unity_ui_tn_candy_sky.jpg)
![Theme3](/developer/files/unity/unity_ui_tn_fantasy.jpg)
![Theme4](/developer/files/unity/unity_ui_tn_purple_mania.jpg)
![Theme5](/developer/files/unity/unity_ui_tn_space_dark.jpg)
![Theme6](/developer/files/unity/unity_ui_tn_village.jpg)

![img-choose-ui-theme]

### 6. Initialize JIVER.
![img-create-jiver-main-prefab]

``` java
/* JiverMain.cs */
void Start ()
{
    string appId = "A7A2672C-AD11-11E4-8DAA-0A18B21C2D82";  /* Sample Jiver Application */
    string userId = SystemInfo.deviceUniqueIdentifier;      /* User ID */
    string userName = "Unity-" + userId.Substring (0, 5);   /* User Name */
    string channelUrl = "jia_test.Unity3d";                 /* Channel URL */

    Jiver.Init (appId);
    Jiver.Login (userId, userName);
    Jiver.Join (channelUrl);
    Jiver.Connect ();
}
```
 * **APP_ID**: JIVER 앱에 할당된 APP_ID. *** 예) X951XA51-AXAE-1XE4-8XC1-10DDXXDX1X5F ***
 * **USER_ID**: JIVER 사용자를 식별하기 위한 UUID. 앱의 사용자 ID 또는 기기별 할당된 유일값.
 * **USER_NAME**: 대화에 사용될 사용자의 이름
 * **CHANNEL_URL**: JIVER 앱에서 생성한 채널의 URL. *** 예) jiver.test_channel_1 ***

### 6. Enjoy JIVER.

JIVER 연동이 완료되었습니다.

iOS빌드를 위해서 몇가지 세팅을 더 수정해야 합니다. iOS Integration 섹션을 확인해 주세요.

