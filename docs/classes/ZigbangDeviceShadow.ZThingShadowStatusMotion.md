[디바이스 프로토콜 정의 - v220110](../README.md) / [Modules](../modules.md) / [ZigbangDeviceShadow](../modules/ZigbangDeviceShadow.md) / ZThingShadowStatusMotion

# Class: ZThingShadowStatusMotion

[ZigbangDeviceShadow](../modules/ZigbangDeviceShadow.md).ZThingShadowStatusMotion

ZThingShadow 포멧중 모션센서 포멧입니다.

ZThingShadow의 모션센서는 아래 properties값을 가질 수 있습니다.  자세한 내용은 Properties 항목을 참조하세요.

* pir : 움직임 상태를 나타냅니다.

example)
 ```typescript
{
  "state": {
    "reported": {
      "v220110": {
        "tuya": {
          "is_connected": true,
          "battery_percentage": 100,
          "pir": "none"
        },
        "tuyaStatusesLast": [
          {
            "code": "pir",
            "value": "none",
            "createdAt": 1648647788665,
            "bridgedAt": 1648647788839
          }
        ]
      }
    }
  }
}
```

## Hierarchy

- [`ZThingBaseShadow`](ZigbangDeviceShadow.ZThingBaseShadow.md)

  ↳ **`ZThingShadowStatusMotion`**

## Properties

### pir

• `Private` **pir**: `undefined` \| { `value`: `any` ; `t`: `number`  } = `undefined`

움직임 감지를 나타냅니다. 아래의 값이 전달됩니다.
* "pir" : 움직임 발생 감지
* "none" : 움직임 발생 이후 1~2분간 움직임 감지되지 않음
