**Example 1: 创建特殊采集配置任务**



Input: 

```
tccli cls CreateConfigExtra --cli-unfold-argument  \
    --Name testname \
    --TopicId xxxxxx-xxx-xxxxxx \
    --Type host_file \
    --HostFile.LogPath /var/log/tmep \
    --HostFile.FilePattern *.log \
    --HostFile.CustomLabels key1=value1 key=value2 \
    --LogType minimalist_log \
    --ExtractRule.TimeKey date \
    --ExtractRule.TimeFormat %Y-%m-%d %H:%M:%S \
    --ExtractRule.Delimiter | \
    --ExtractRule.LogRegex .* \
    --ExtractRule.BeginRegex ^ \
    --ExtractRule.Keys date  content \
    --ExtractRule.FilterKeyRegex.0.Key xxx \
    --ExtractRule.FilterKeyRegex.0.Regex ssss \
    --ExtractRule.UnMatchLogKey testlog \
    --ExtractRule.UnMatchUpLoadSwitch True \
    --ExtractRule.Backtracking -1 \
    --ExcludePaths.0.Type xx \
    --ExcludePaths.0.Value xx \
    --UserDefineRule xxxxxx \
    --GroupId xxxxx \
    --ConfigFlag label_k8s \
    --LogsetId xxxxx \
    --LogsetName xxxxxx \
    --TopicName xxxxxxxx
```

Output: 
```
{
    "Response": {
        "ConfigExtraId": "xxxx-xx-xx-xx-xxxxxxxx",
        "RequestId": "6ef60bec-0242-43af-bb20-270359fb54a7"
    }
}
```

