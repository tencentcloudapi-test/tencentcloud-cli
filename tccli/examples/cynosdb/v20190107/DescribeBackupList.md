**Example 1: 查询备份文件列表**



Input: 

```
tccli cynosdb DescribeBackupList --cli-unfold-argument  \
    --ClusterId cynosdbpg-ilgo90hu \
    --Offset 0 \
    --Limit 10
```

Output: 
```
{
    "Response": {
        "TotalCount": 1,
        "BackupList": [
            {
                "SnapshotId": 10000,
                "SnapshotTime": "xx",
                "FileName": "snap",
                "FileSize": 20190215,
                "StartTime": "2019-01-20 01:10:12",
                "FinishTime": "2019-01-20 02:10:12",
                "BackupType": "snapshot",
                "BackupMethod": "auto",
                "BackupStatus": "success"
            }
        ],
        "RequestId": "6EF60BEC-0242-43AF-BB20-270359FB54A7"
    }
}
```

