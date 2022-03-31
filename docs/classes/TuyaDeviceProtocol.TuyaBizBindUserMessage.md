[디바이스 프로토콜 정의 - v220110](../README.md) / [Modules](../modules.md) / [TuyaDeviceProtocol](../modules/TuyaDeviceProtocol.md) / TuyaBizBindUserMessage

# Class: TuyaBizBindUserMessage

[TuyaDeviceProtocol](../modules/TuyaDeviceProtocol.md).TuyaBizBindUserMessage

투야 클라우드로 부터 전달되는 Biz 메시지중 bindUser의 bizData 포멧을 설명합니다.

bindUser는 Tuya Cloud에 연결된 IoT 기기와 사용자 계정이 연결된 경우 전달되는 이벤트 메시지입니다.

(즉 디바이스 페어링이 완료된 시점에 전달됩니다.)

bindUser는 bizCode값으로 "bindUser" 가 전달됩니다.

자세한 내용은 아래 링크를 참조하세요.
* https://developer.tuya.com/en/docs/cloud/General-Capability-of-public-area?id=Kb6fv4gj2j2a7#title-6-Pairing%20event

참고로, 지그비허브와 지그비허브에 연결된 하위 디바이스는 bizData의 object에 약간의 차이가 있습니다.

지그비 허브의 경우 아래 포멧으로 전달됩니다.
```typescript
{
    "protocol": 20,
    "pv": string,
    "sign": string,
    "t": number,
    "data": {
				"devId": string,
				"productKey": string,
				"bizCode": "bindUser",
				"bizData": {
				    "devId": string,
				    "uuid": string,
					"onwerId": string,
				    "uid": string,
				    "token": string
				},
				"ts": number,
				"uuid": string
		}
}
```

지그비 허브에 연결된 하위 디바이스는 아래 포멧으로 전달됩니다.
```typescript
{
    "protocol": 20,
    "pv": string,
    "sign": string,
    "t": number,
    "data": {
				"devId": string,
				"productKey": string,
				"bizCode": "bindUser",
				"bizData": {
				    "devId": string,
				    "uuid": string,
					"onwerId": string,
				    "uid": string,
				    "parentDevId": string
				},
				"ts": number,
				"uuid": string
		}
}
```
example) - 지그비 허브
 ```typescript
{
    "protocol": 20,
    "pv": "2.0",
    "sign": "fa07ba15bb10f11d18652b7f3ab6fafe",
    "t": 1647422214311,
    "data":	{
		    "devId": "eb5d42e1b89b409e9atcjd",
		    "productKey": "yacg23r2ew8vxosz",
		    "bizCode": "bindUser",
		    "bizData": {
		        "devId": "eb5d42e1b89b409e9atcjd",
		        "uid": "az1646801177666RDDPg",
		        "ownerId": "57807164",
		        "uuid": "b534e1f767c67ad1",
		        "token": "txehdBPc"
		    },
		    "ts": 1647422214311,
		}
}
```

example) - 지그비 허브에 연결된 하위 디바이스
 ```typescript
{
    "protocol": 20,
    "pv": "2.0",
    "sign": "cfe1683be1372e4db1df1eaaf700fec5",
    "t": 1647422322141,
    "data": {
		    "devId": "eb89119d660ec93319pcwl",
		    "productKey": "ktge2vqt",
		    "bizCode": "bindUser",
		    "bizData": {
		        "devId": "eb89119d660ec93319pcwl",
		        "uid": "az1646801177666RDDPg",
		        "parentDevId": "eb5d42e1b89b409e9atcjd",
		        "ownerId": "57807164",
		        "uuid": "60a423fffe3d4191"
		    },
		    "ts": 1647422322141,
		    "uuid": "60a423fffe3d4191"
		}
}
```

## Hierarchy

- [`TuyaBizBaseMessage`](TuyaDeviceProtocol.TuyaBizBaseMessage.md)

  ↳ **`TuyaBizBindUserMessage`**

## Properties

### devId\_

• **devId\_**: `undefined` \| `string` = `undefined`

* 디바이스 아이디

___

### uuid\_

• **uuid\_**: `undefined` \| `string` = `undefined`

* 디바이스 고유번호

___

### ownerId

• **ownerId**: `undefined` \| `string` = `undefined`

* 디바이스가 속한 홈 아이디

___

### uid

• **uid**: `undefined` \| `string` = `undefined`

* 디바이스에 연결된 사용자 아이디

___

### parentDevId

• **parentDevId**: `undefined` \| `string` = `undefined`

* 디바이스가 연결된 허브의 아이디

___

### token

• **token**: `undefined` \| `string` = `undefined`

* 디바이스 페이렁 토큰
