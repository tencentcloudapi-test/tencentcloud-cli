**Example 1: 创建 rum 项目**



Input: 

```
tccli rum CreateProject --cli-unfold-argument  \
    --Name '测试项目' \
    --Desc '项目描述' \
    --InstanceID "taw-123" \
    --Type web \
    --URL 'http://www.qq.com' \
    --Repo 'http://github.com/xxx' \
    --Rate "10" \
    --EnableURLGroup 1
```

Output: 
```
{
    "Response": {
        "ID": 1,
        "Key": "RlOmCVbPrKd4",
        "RequestId": "65a8fec7-2b39-4b11-893f-3715279d235f"
    }
}
```

