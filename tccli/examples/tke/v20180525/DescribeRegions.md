**Example 1: 获取地域列表**

获取地域列表

Input: 

```
tccli tke DescribeRegions --cli-unfold-argument ```

Output: 
```
{
    "Response": {
        "TotalCount": 1,
        "RegionInstanceSet": [
            {
                "Status": "xx",
                "Remark": "xx",
                "RegionId": 0,
                "FeatureGates": "xx",
                "Alias": "xx",
                "RegionName": "xx"
            }
        ],
        "RequestId": "eac6b301-a322-493a-8e36-83b295459398"
    }
}
```

