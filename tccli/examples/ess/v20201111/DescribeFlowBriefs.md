**Example 1: 拉取流程列表**



Input: 

```
tccli ess DescribeFlowBriefs --cli-unfold-argument  \
    --Operator.UserId yDxM6UyK********QDV8dJUuO4zjEu \
    --Operator.ClientIp 8.8.8.8 \
    --Operator.Channel  \
    --Operator.OpenId  \
    --Operator.ProxyIp  \
    --FlowIds c7b5ca37ae*******2b4c6644 61a82f0c1******d0d807
```

Output: 
```
{
    "Response": {
        "RequestId": "s123456789",
        "FlowBriefs": [
            {
                "FlowId": "c7b5ca37ae*******2b4c6644",
                "FlowName": "测试合同-1",
                "FlowDescription": "测试流程的描述信息",
                "FlowType": "合同",
                "FlowStatus": 1,
                "CreatedOn": 1604910798,
                "FlowMessage": ""
            },
            {
                "FlowId": "61a82f0c1******d0d807",
                "FlowName": "测试合同-2",
                "FlowDescription": "测试流程的描述信息",
                "FlowType": "合同",
                "FlowStatus": 1,
                "CreatedOn": 1604910797,
                "FlowMessage": ""
            }
        ]
    }
}
```

