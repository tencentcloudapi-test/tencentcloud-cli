**Example 1: 图片内容识别**

图片内容安全识别

Input: 

```
tccli ims ImageModeration --cli-unfold-argument  \
    --FileUrl https://xxx.jpg \
    --DataId 1213 \
    --BizType test_1001
```

Output: 
```
{
    "Response": {
        "RequestId": "a61237dd-c2a0-43e7-a3da-d27022d39ba7",
        "DataId": "a61237dd-c2a0-43e7-a3da-d27022d39ba7",
        "BizType": "test_1001",
        "Suggestion": "Block",
        "FileMD5": "",
        "Label": "Porn",
        "SubLabel": "SexBehavior",
        "Score": 90,
        "LabelResults": [
            {
                "Scene": "Porn",
                "Suggestion": "Block",
                "Label": "Porn",
                "SubLabel": "SexBehavior",
                "Score": 90,
                "Details": []
            }
        ],
        "ObjectResults": [
            {
                "Scene": "QrCode",
                "Suggestion": "Block",
                "Label": "Ad",
                "SubLabel": "",
                "Score": 100,
                "Names": [
                    "QRCODE"
                ],
                "Details": [
                    {
                        "Id": 0,
                        "Name": "QRCODE",
                        "Score": 100,
                        "Location": {
                            "X": 155.01746,
                            "Y": 396.01746,
                            "Width": 769.9824,
                            "Height": 769.98254,
                            "Rotate": 0
                        }
                    }
                ]
            }
        ],
        "OcrResults": [],
        "LibResults": [],
        "Extra": ""
    }
}
```

