**Example 1: 创建投递任务**



Input: 

```
tccli cls CreateConsumer --cli-unfold-argument  \
    --TopicId xxx-xxx-xxx-xxx \
    --Ckafka.Vip 10.123.123.123 \
    --Ckafka.Vport 8888 \
    --Ckafka.InstanceId xxxxx \
    --Ckafka.InstanceName myname \
    --Ckafka.TopicId xxxxx \
    --Ckafka.TopicName xxxxx \
    --Content.EnableTag True \
    --Content.MetaFields __SOURCE__ \
    --NeedContent True
```

Output: 
```
{
    "Response": {
        "RequestId": "6ef60xxx-0xxx-4xxx-bxxx-270359fb5xxx"
    }
}
```

