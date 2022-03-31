[디바이스 프로토콜 정의 - v220110](../README.md) / [Modules](../modules.md) / [ZigbangDeviceShadow](../modules/ZigbangDeviceShadow.md) / ZThingShadowStatusContact

# Class: ZThingShadowStatusContact

[ZigbangDeviceShadow](../modules/ZigbangDeviceShadow.md).ZThingShadowStatusContact

ZThingShadow 포멧중 도어센서 포멧입니다.

ZThingShadow의 도어센서는 아래 properties값을 가질 수 있습니다.  자세한 내용은 Properties 항목을 참조하세요.

* doorcontact_state : 문열림 상태를 나타냅니다.
* temper_alarm : 도어 센서 접지 상태를 나타냅니다.

example)
 ```typescript
{
  "state": {
    "reported": {
      "v220110": {
        "tuya": {
          "is_connected": true,
          "battery_percentage": 100,
          "doorcontact_state": true,
          "temper_alarm": true
        },
        "tuyaStatusesLast": [
          {
            "code": "doorcontact_state",
            "value": true,
            "createdAt": 1648650740372,
            "bridgedAt": 1648650740536
          }
        ]
      }
    }
  }
}
```

## Hierarchy

- [`ZThingBaseShadow`](ZigbangDeviceShadow.ZThingBaseShadow.md)

  ↳ **`ZThingShadowStatusContact`**

## Properties

### doorcontact\_state

• `Private` **doorcontact\_state**: `undefined` \| { `value`: `any` ; `t`: `number`  } = `undefined`

문열림 상태를 나타냅니다. 아래의 값이 전달됩니다.
* true : 문열림
* false : 문닫힘

___

### temper\_alarm

• `Private` **temper\_alarm**: `undefined` \| { `value`: `any` ; `t`: `number`  } = `undefined`

도어센서의 접지 상태 변화를 나타냅니다. 아래의 값이 전달됩니다.
* true : 접지 분리 상태
* false : 접지 상태
