**Example 1: 通过交易ID查询**



Input: 

```
tccli tbaas QueryChainMakerTransaction --cli-unfold-argument  \
    --ChainId chain_dcwtt \
    --ClusterId chainmaker-j1juwsmndn \
    --TxID f6cf450f9b0b496f9ee6d332e739b8b182fe1e3b34ed446ab068a151f1ee8cbe
```

Output: 
```
{
    "Response": {
        "RequestId": "d25c24d9-4bb9-44bc-b084-5a25af34bb14",
        "Result": {
            "Code": 0,
            "CodeMessage": "",
            "Message": "",
            "TxId": "f6cf450f9b0b496f9ee6d332e739b8b182fe1e3b34ed446ab068a151f1ee8cbe",
            "Timestamp": 1627267173,
            "GasUsed": 230871,
            "BlockHeight": 2,
            "ContractEvent": ""
        }
    }
}
```

