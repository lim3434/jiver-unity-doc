Setup JIVER with custom UI
========================
### 1. Remove default JiverUI 
JIVERUI Prefab GameObject를 제거합니다.

### 2. Add custom UI script

Plugins/JIVER/SDK/JiverCustomUI.cs 스크립트를 새롭게 구성할 UI GameObject에 추가합니다.

### 3. Customize JIVER UI
Plugins/JIVER/SDK/JiverCustomUI.cs 스크립트는 JIVER UI를 구성하기 위한 최소한의 이벤트 함수들이 포함되어 있습니다.
이 스크립트를 기본으로 CustomUI를 제작하실 수 있습니다.

``` java
/* JiverCustomUI.cs */
using UnityEngine;
using System.Collections;
using System.Collections.Generic;
using JiverModel;

public class JiverCustomUI : JiverResponder {
    private List<System.Object> messages = new List<System.Object>();
    private List<Channel> channels = new List<Channel>();

    #region implemented abstract members of JiverResponder
    public override void OnConnect (JiverModel.Channel channel)
    {
        Debug.Log ("Connect to " + channel.GetName ());
        string channelName = "#" +  channel.GetUrlWithoutAppPrefix();
        string channelUrl = channel.GetUrl ();
    }
    public override void OnError (int errorCode)
    {
        Debug.Log ("JIVER Error: " + errorCode);
    }
    public override void OnMessageReceived (JiverModel.Message message)
    {
        messages.Add (message);
    }
    public override void OnSystemMessageReceived (JiverModel.SystemMessage message)
    {
        messages.Add (message);
    }

    public override void OnBroadcastMessageReceived (JiverModel.BroadcastMessage message)
    {
        messages.Add (message);
    }

    public override void OnQueryChannelList (List<Channel> channels)
    {
        this.channels = channels;
    }
    
    #endregion

    void Awake() {
    }


    void Submit() {
        //Jiver.SendMessage(inputString);
    }


}
```
