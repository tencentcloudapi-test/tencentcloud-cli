**Example 1: 创建实例询价-成功返回**



Input: 

```
tccli lighthouse InquirePriceRenewInstances --cli-unfold-argument  \
    --InstanceIds lhins-11110001 \
    --InstanceChargePrepaid.RenewFlag NOTIFY_AND_AUTO_RENEW \
    --InstanceChargePrepaid.Period 1
```

Output: 
```
{
    "Response": {
        "Price": {
            "InstancePrice": {
                "OriginalBundlePrice": 60.0,
                "OriginalPrice": 1440.0,
                "Discount": 100,
                "DiscountPrice": 1440.0
            }
        },
        "RequestId": "96d188f2-caf0-4d63-ba6f-474d22a8b344",
        "DataDiskPriceSet": [
            {
                "Discount": 0.0,
                "OriginalDiskPrice": 0.0,
                "OriginalPrice": 0.0,
                "DiskId": "xx",
                "DiscountPrice": 0.0
            }
        ]
    }
}
```

