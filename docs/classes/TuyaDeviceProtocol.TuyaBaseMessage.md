[디바이스 프로토콜 정의 - v220110](../README.md) / [Modules](../modules.md) / [TuyaDeviceProtocol](../modules/TuyaDeviceProtocol.md) / TuyaBaseMessage

# Class: TuyaBaseMessage

[TuyaDeviceProtocol](../modules/TuyaDeviceProtocol.md).TuyaBaseMessage

투야 클라우드로 부터 전달되는 디바이스 데이터는 아래 해더를 가지고 있습니다.

각 필드에 대한 설명은 Properties 항목을 참고해주세요.

```typescript
{
  "protocol": number
  "pv" : string
  "sign" : string
  "t": number
  "data": string
}
```

example)
 ```typescript
{
	"protocol": 20,
	"pv": "2.0",
	"sign": "164b9a206cafcd0968759d9db999f6eb",
	"t": 1647327358747,
	"data": "{\"bizCode\":\"bindUser\",\"bizData\":{\"devId\":\"ebc9dba5109cccbbeahzsp\",\"uid\":\"az1646801177666RDDPg\",\"ownerId\":\"57807164\",\"uuid\":\"b534e1f767c67ad1\",\"token\":\"0DYGgz0D\"},\"devId\":\"ebc9dba5109cccbbeahzsp\",\"productKey\":\"yacg23r2ew8vxosz\",\"ts\":1647327358747,\"uuid\":\"b534e1f767c67ad1\"}",
}
```


## Properties

### protocol

• `Private` **protocol**: `undefined` \| `number` = `undefined`

```typescript
투야 클라우드 공통 해더
```
* 프로토콜 번호

* 참조 : https://developer.tuya.com/en/docs/iot/message-type?id=Kavqerli65a1u#title-2-Protocol%20number

___

### pv

• `Private` **pv**: `undefined` \| `string` = `undefined`

```typescript
투야 클라우드 공통 해더
```
*  프로토콜 버전

* 참조 : https://developer.tuya.com/en/docs/iot/integrate-mq?id=Kavqdgattt1y2#title-4-Data%20attribute%20and%20example

___

### sign

• `Private` **sign**: `undefined` \| `string` = `undefined`

```typescript
투야 클라우드 공통 해더
```
* 시그니쳐값

___

### t\_

• `Private` **t\_**: `undefined` \| `number` = `undefined`

```typescript
투야 클라우드 공통 해더 (주의! 상속된 하위 class에서 보입니다.)
```
* 타임스탬프

___

### data\_

• `Private` **data\_**: `undefined` \| `string` = `undefined`

```typescript
투야 클라우드 공통 해더 (주의! 상속된 하위 class에서 보입니다.)
```
* 데이터
