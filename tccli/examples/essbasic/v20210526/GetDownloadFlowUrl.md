**Example 1: 生成批量下载控制连接地址**



Input: 

```
tccli essbasic GetDownloadFlowUrl --cli-unfold-argument  \
    --Agent.ProxyAppId c17bdf9c2a7bdcb32611f4d0200fef3d \
    --Agent.ProxyOrganizationOpenId d7c13a8b81340cce9e3968c0ee248f04 \
    --Agent.ProxyOperator.OpenId 00498cc8500be9cxxxxxxx3aff766cac \
    --Agent.AppId 65fb0c591044be8a1f60aa382cc5ed0e \
    --DownLoadFlows.0.FlowIdList test-flow-id1 test-flow-id2 \
    --DownLoadFlows.0.FileName 文件夹1 \
    --DownLoadFlows.1.FlowIdList test-flow-id3 test-flow-id4 \
    --DownLoadFlows.1.FileName 文件夹2
```

Output: 
```
{
    "Response": {
        "DownLoadUrl": "https://xxx.xxxx.tencent.com/template-preview?channel=PROXYCHANNEL&expiredTime=1639587153&code=yDxjKUUgydjf9pruUuO4zjES4adWk38k&token=yDxjKUUgydjf9pruUuO4zjES4adWk38k&operate=downloadFlow",
        "RequestId": "s16221xxx14775648"
    }
}
```

