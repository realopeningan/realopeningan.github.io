[디바이스 프로토콜 정의 - v220110](../README.md) / [Modules](../modules.md) / [ZigbangDeviceShadow](../modules/ZigbangDeviceShadow.md) / ZThingShadowStatusSiren

# Class: ZThingShadowStatusSiren

[ZigbangDeviceShadow](../modules/ZigbangDeviceShadow.md).ZThingShadowStatusSiren

ZThingShadow 포멧중 사이렌 센서 포멧입니다.

ZThingShadow의 사이렌 센서는 아래 properties값을 가질 수 있습니다.  자세한 내용은 Properties 항목을 참조하세요.

* alarm_switch : 현재 경보 상태를 나타냅니다.
* temper_alarm : 현재 접지 상태를 나타냅니다.
* alarm_volume : 사이렌 음량을 나타냅니다.

example)
 ```typescript
{
  "state": {
    "reported": {
      "v220110": {
        "tuya": {
          "is_connected": true,
          "battery_percentage": 100,
          "alarm_volume": "middle",
          "alarm_switch": false,
          "temper_alarm": false
        },
        "tuyaStatusesLast": [
          {
            "code": "alarm_switch",
            "value": false,
            "createdAt": 1648565098329,
            "bridgedAt": 1648565098500
          },
          {
            "code": "temper_alarm",
            "value": false,
            "createdAt": 1648565098329,
            "bridgedAt": 1648565098500
          }
        ]
      }
    }
  }
}
```

## Hierarchy

- [`ZThingBaseShadow`](ZigbangDeviceShadow.ZThingBaseShadow.md)

  ↳ **`ZThingShadowStatusSiren`**

## Properties

### alarm\_switch

• `Private` **alarm\_switch**: `undefined` \| { `value`: `any` ; `t`: `number`  } = `undefined`

현재 경보상태를 나타냅니다. 아래의 값이 전달됩니다.
* true : 경보 발생
* false : 경보 해제

___

### temper\_alarm

• `Private` **temper\_alarm**: `undefined` \| { `value`: `any` ; `t`: `number`  } = `undefined`

현재 사이렌 센서의 접지 상태를 나타냅니다. 아래의 값이 전달됩니다.
* true : 접지 분리
* false : 접지 상태

___

### alarm\_volume

• `Private` **alarm\_volume**: `undefined` \| { `value`: `any` ; `t`: `number`  } = `undefined`

현재 사이렌 센서의 음량 상태를 나타냅니다. 아래의 값이 전달됩니다.
* "high" : 음량 높음
* "middle" : 음량 중간
* "low" : 음량 낮음
* "mute" : 음소거
