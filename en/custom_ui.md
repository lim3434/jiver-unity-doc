Setup JIVER with custom UI
========================
### 1. Remove default JiverUI 
Remove JIVERUI prefab GameObject.

### 2. Add custom UI script
Add Plugins/JIVER/SDK/JiverCustomUI.cs script to your UI GameObject.

### 3. Customize JIVER UI
Below sample code(Plugins/JIVER/SDK/JiverCustomUI.cs) is a simplest skeleton code to receive events from JIVER SDK.
You can customize UI with the code below.

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
