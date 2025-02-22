**Example 1: 同步调用设备行为**

当行为返回成功时，该值是 succ。

Input: 

```
tccli iotexplorer CallDeviceActionSync --cli-unfold-argument  \
    --ProductId TOIDHQ3AOQ \
    --DeviceName light1 \
    --ActionId actid \
    --InputParams {"vol":3}
```

Output: 
```
{
    "Response": {
        "ClientToken": "0fe1260b7a724b67ba873ca7df703e0d",
        "OutputParams": "{\"brightness\":1,\"color\":1,\"light_switch\":1}",
        "RequestId": "235fe48b-0c31-4a7c-aaf6-83ba3e9s4bcf",
        "Status": "succ"
    }
}
```

**Example 2: 同步调用设备行为，设备不在线。**

当设备不在线或未订阅相关 topic 时，设备返回情况如样例所示。

Input: 

```
tccli iotexplorer CallDeviceActionSync --cli-unfold-argument  \
    --ProductId TOIDHQ3AOQ \
    --DeviceName light1 \
    --ActionId actid \
    --InputParams {"brightness":3}
```

Output: 
```
{
    "Response": {
        "ClientToken": "",
        "OutputParams": "",
        "RequestId": "b2621fc1-d6d9-4929-af0b-3fb0e919658a",
        "Status": "FailedOperation.ActionUnreachable|动作消息不可达"
    }
}
```

**Example 3: 同步调用设备行为，设备超时**

当设备响应时间过长时，设备返回情况如样例所示。

Input: 

```
tccli iotexplorer CallDeviceActionSync --cli-unfold-argument  \
    --ProductId TOIDHQ3AOQ \
    --DeviceName light1 \
    --ActionId actid \
    --InputParams {"brightness":3}
```

Output: 
```
{
    "Response": {
        "RequestId": "b1de7dcf-5029-4d70-b6b5-d1ad0f785552"
    }
}
```

