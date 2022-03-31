[디바이스 프로토콜 정의 - v220110](../README.md) / [Modules](../modules.md) / [TuyaDeviceProtocol](../modules/TuyaDeviceProtocol.md) / TuyaBizNameUpdateMessage

# Class: TuyaBizNameUpdateMessage

[TuyaDeviceProtocol](../modules/TuyaDeviceProtocol.md).TuyaBizNameUpdateMessage

투야 클라우드로 부터 전달되는 Biz 메시지중 nameUpdate의 bizData 포멧을 설명합니다.

nameUpdate는 Tuya Cloud에 연결된 IoT 기기의 이름이 변경되면 전달됩니다.

nameUpdate는 bizCode값으로 "nameUpdate" 가 전달됩니다.

자세한 내용은 아래 링크를 참조하세요.
* https://developer.tuya.com/en/docs/iot/message-type?id=Kavqerli65a1u#title-6-Change%20the%20device%20name

bizData는 아래 포멧으로 전달됩니다.
```typescript
{
		"protocol": 20,
		"pv": string,
		"sign": string,
		"t": number,
		"data": {
		    "devId": string,
		    "productKey": string,
		    "bizCode": "nameUpdate",
		    "bizData": {
						"devId": string,
						"uid": string,
						"name": string
		    }
				"ts": number,
				"uuid": string
		}
}
```

example)
 ```typescript
{
    "protocol": 20,
    "pv": "2.0",
    "sign": "666b6269e1c39357dcf63322d03dfb4d",
    "t": 1647409399467,
    "data": {
		    "devId": "ebeef921338a60f2ccy5ij",
		    "productKey": "33uazzfa",
		    "bizCode": "nameUpdate",
		    "bizData": {
		        "devId": "ebeef921338a60f2ccy5ij",
		        "uid": "az1647409049981pgW4t",
		        "name": "텐플 온습도 센서 36/4113510300100170002/B동/3010호/서재현"
		    },
		    "ts": 1647409399467,
		    "uuid": "b4e3f9fffe0e4009"
		}
}
```

## Hierarchy

- [`TuyaBizBaseMessage`](TuyaDeviceProtocol.TuyaBizBaseMessage.md)

  ↳ **`TuyaBizNameUpdateMessage`**

## Properties

### devId\_

• **devId\_**: `undefined` \| `string` = `undefined`

* 디바이스 아이디

___

### uid

• **uid**: `undefined` \| `string` = `undefined`

* 디바이스에 연결된 사용자 아이디

___

### name

• **name**: `undefined` \| `string` = `undefined`

* 디바이스 이름(수정된 이름)
