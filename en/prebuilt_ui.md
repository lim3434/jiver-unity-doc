Setup JIVER
============================
### 1. Import JIVER 
You can download JIVER from hrer. [Download JIVER Unity Plugin](download_sdk.html)

![import](https://raw.githubusercontent.com/smilefam/jiver-unity-doc/master/file/import.jpg)

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
![jiver-prefab](https://raw.githubusercontent.com/smilefam/jiver-unity-doc/master/file/jiver_prefab.jpg)

### 4. Create Prebuilt JIVER UI
![ui-prefab](https://raw.githubusercontent.com/smilefam/jiver-unity-doc/master/file/ui_prefab.jpg)

### 5. Choose UI Theme
![Theme1](https://raw.githubusercontent.com/smilefam/jiver-unity-doc/master/file/th_beige_crema.jpg)
![Theme2](https://raw.githubusercontent.com/smilefam/jiver-unity-doc/master/file/th_candy_sky.jpg)
![Theme3](https://raw.githubusercontent.com/smilefam/jiver-unity-doc/master/file/th_fantasy.jpg)
![Theme4](https://raw.githubusercontent.com/smilefam/jiver-unity-doc/master/file/th_purple_mania.jpg)
![Theme5](https://raw.githubusercontent.com/smilefam/jiver-unity-doc/master/file/th_space_dark.jpg)
![Theme6](https://raw.githubusercontent.com/smilefam/jiver-unity-doc/master/file/th_village.jpg)

![choose-theme](https://raw.githubusercontent.com/smilefam/jiver-unity-doc/master/file/choose_theme.jpg)

### 6. Initialize JIVER.
![main-prefab](https://raw.githubusercontent.com/smilefam/jiver-unity-doc/master/file/main_prefab.jpg)

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
 * **APP_ID**: JIVER APP_ID. *** e.g.) X951XA51-AXAE-1XE4-8XC1-10DDXXDX1X5F ***
 * **USER_ID**: JIVER User UUID. Unique ID for Users
 * **USER_NAME**: User Nickname
 * **CHANNEL_URL**: JIVER Channel URL. *** e.g.) jiver.test_channel_1 ***

### 6. Enjoy JIVER.
JIVER is ready to run into your game. Enjoy JIVER.

P.S. You need a few extra steps to complete integration for iOS. Check out iOS Integration.
[Jump to iOS integration](ios.html)
