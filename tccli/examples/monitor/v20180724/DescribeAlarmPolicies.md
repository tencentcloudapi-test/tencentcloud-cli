**Example 1: 查询告警策略列表**



Input: 

```
tccli monitor DescribeAlarmPolicies --cli-unfold-argument  \
    --Module monitor \
    --PageSize 10 \
    --PageNumber 1
```

Output: 
```
{
    "Response": {
        "Policies": [
            {
                "PolicyId": "policy-pvnj4u7h",
                "PolicyName": "Test-2",
                "UseSum": 0,
                "Remark": "For-Test-2",
                "MonitorType": "MT_QCE",
                "Enable": 1,
                "RuleType": "STATIC",
                "TagInstances": null,
                "IsDefault": 0,
                "ProjectId": 0,
                "ProjectName": "",
                "Namespace": "cvm_device",
                "ConditionTemplateId": "",
                "Condition": {
                    "IsUnionRule": 0,
                    "Rules": [
                        {
                            "MetricName": "CpuUsage",
                            "Description": "CPU利用率",
                            "Period": 60,
                            "Operator": "gt",
                            "Value": "0",
                            "ContinuePeriod": 1,
                            "NoticeFrequency": 86400,
                            "IsPowerNotice": 0,
                            "Filter": {
                                "Type": "",
                                "Dimensions": "[]"
                            }
                        }
                    ]
                },
                "EventCondition": {
                    "Rules": []
                },
                "NoticeIds": [
                    "notice-esrwma09"
                ],
                "Notices": [
                    {
                        "Id": "notice-esrwma09",
                        "Name": "Notice-Test-2",
                        "UpdatedAt": "2020-10-19 20:56:50",
                        "UpdatedBy": "1500000685",
                        "NoticeType": "OK",
                        "UserNotices": [
                            {
                                "ReceiverType": "GROUP",
                                "UserIds": null,
                                "GroupIds": [
                                    3877
                                ],
                                "StartTime": 0,
                                "EndTime": 1,
                                "NoticeWay": [
                                    "EMAIL"
                                ],
                                "PhoneOrder": null,
                                "PhoneCircleTimes": 2,
                                "PhoneInnerInterval": 60,
                                "PhoneCircleInterval": 60,
                                "NeedPhoneArriveNotice": 1
                            }
                        ],
                        "URLNotices": [
                            {
                                "URL": "https://www.abc.com",
                                "IsValid": 0
                            }
                        ],
                        "IsPreset": 0
                    }
                ],
                "TriggerTasks": [],
                "OriginId": "1314081",
                "ConditionsTemp": {
                    "TemplateName": "",
                    "Condition": null,
                    "EventCondition": null
                },
                "LastEditUin": "1500000685",
                "UpdateTime": 1603114100,
                "InsertTime": 1603114100,
                "Region": [
                    "bj",
                    "ca",
                    "cd",
                    "cq",
                    "de",
                    "fzec",
                    "gz",
                    "gzopen",
                    "hk",
                    "hzec",
                    "in",
                    "jnec",
                    "jp",
                    "kr",
                    "nj",
                    "ru",
                    "sg",
                    "sh",
                    "shjr",
                    "szjr",
                    "szx",
                    "th",
                    "tpe",
                    "tsn",
                    "use",
                    "usw"
                ],
                "FilterDimensionsParam": "",
                "NamespaceShowName": "云服务器-基础监控",
                "CanSetDefault": 1,
                "InstanceGroupId": 0,
                "InstanceGroupName": "",
                "InstanceSum": 0
            }
        ],
        "RequestId": "p7gicv4fb-4euztbaaczrsj4vz-s28g-",
        "TotalCount": 1
    }
}
```

**Example 2: 搜索一个云服务器绑定的告警策略**

按照实例过滤策略，需要填入监控类型、策略类型、实例的维度信息。我们以搜索两个云服务器为例，假设他们的实例 ID 分别为 `ins-qr8d555g`,  `ins-qr8d555h`。

MonitorTypes 指定为 `MT_QCE`

Namespaces 指定为 `cvm_device`

Dimensions 的 JSON 字符串为

```
[
    {
        "Dimensions": {
            "unInstanceId": "ins-qr8d555g"
        }
    },
     {
        "Dimensions": {
            "unInstanceId": "ins-qr8d555h"
        }
    }
]
```

不同云产品参数示例详见 [维度信息Dimensions列表](https://cloud.tencent.com/document/product/248/50397)

Input: 

```
tccli monitor DescribeAlarmPolicies --cli-unfold-argument  \
    --Module monitor \
    --PageSize 10 \
    --PageNumber 1 \
    --MonitorTypes MT_QCE \
    --Namespaces cvm_device \
    --Dimensions [{"Dimensions": { "unInstanceId": "ins-qr8d555g"}},{ "Dimensions": { "unInstanceId": "ins-qr8d555h"}}]
```

Output: 
```
{
    "Response": {
        "Policies": [
            {
                "PolicyId": "policy-pvnj4u7h",
                "PolicyName": "Test-2",
                "UseSum": 0,
                "Remark": "For-Test-2",
                "MonitorType": "MT_QCE",
                "Enable": 1,
                "RuleType": "STATIC",
                "TagInstances": null,
                "IsDefault": 0,
                "ProjectId": 0,
                "ProjectName": "",
                "Namespace": "cvm_device",
                "ConditionTemplateId": "",
                "Condition": {
                    "IsUnionRule": 0,
                    "Rules": [
                        {
                            "MetricName": "CpuUsage",
                            "Description": "CPU利用率",
                            "Period": 60,
                            "Operator": "gt",
                            "Value": "0",
                            "ContinuePeriod": 1,
                            "NoticeFrequency": 86400,
                            "IsPowerNotice": 0,
                            "Filter": {
                                "Type": "",
                                "Dimensions": "[]"
                            }
                        }
                    ]
                },
                "EventCondition": {
                    "Rules": []
                },
                "NoticeIds": [
                    "notice-esrwma09"
                ],
                "Notices": [
                    {
                        "Id": "notice-esrwma09",
                        "Name": "Notice-Test-2",
                        "UpdatedAt": "2020-10-19 20:56:50",
                        "UpdatedBy": "1500000685",
                        "NoticeType": "OK",
                        "UserNotices": [
                            {
                                "ReceiverType": "GROUP",
                                "UserIds": null,
                                "GroupIds": [
                                    3877
                                ],
                                "StartTime": 0,
                                "EndTime": 1,
                                "NoticeWay": [
                                    "EMAIL"
                                ],
                                "PhoneOrder": null,
                                "PhoneCircleTimes": 2,
                                "PhoneInnerInterval": 60,
                                "PhoneCircleInterval": 60,
                                "NeedPhoneArriveNotice": 1
                            }
                        ],
                        "URLNotices": [
                            {
                                "URL": "https://www.abc.com",
                                "IsValid": 0
                            }
                        ],
                        "IsPreset": 0
                    }
                ],
                "TriggerTasks": [],
                "OriginId": "1314081",
                "ConditionsTemp": {
                    "TemplateName": "",
                    "Condition": null,
                    "EventCondition": null
                },
                "LastEditUin": "1500000685",
                "UpdateTime": 1603114100,
                "InsertTime": 1603114100,
                "Region": [
                    "bj",
                    "ca",
                    "cd",
                    "cq",
                    "de",
                    "fzec",
                    "gz",
                    "gzopen",
                    "hk",
                    "hzec",
                    "in",
                    "jnec",
                    "jp",
                    "kr",
                    "nj",
                    "ru",
                    "sg",
                    "sh",
                    "shjr",
                    "szjr",
                    "szx",
                    "th",
                    "tpe",
                    "tsn",
                    "use",
                    "usw"
                ],
                "FilterDimensionsParam": "",
                "NamespaceShowName": "云服务器-基础监控",
                "CanSetDefault": 1,
                "InstanceGroupId": 0,
                "InstanceGroupName": "",
                "InstanceSum": 0
            }
        ],
        "RequestId": "p7gicv4fb-4euztbaaczrsj4vz-s28g-",
        "TotalCount": 1
    }
}
```

