디바이스 프로토콜 정의 / [Modules](modules.md)

# ZIOT-BRIDGE

## Gateway

Gateway는 3rd party cloud(ex. Tuya)에 연결되어 IoT 디바이스로 부터 전달되는 메시지를 수신받습니다.

[자세히 살펴보기](./gateway/README.md)

## Lambda

Lambda는 Gateway에서 전달된 메시지를 수신받아 처리합니다.

혹은 3rd party cloud에 디바이스 제어 API를 호출하여 IoT 디바이스를 제어합니다.

[자세히 살펴보기](./lambda/bridge/README.md)

## Zthing-message-converter

Zthing-message-converter는 Gateway에서 전달된 메시지를 파싱하고, 직방에서 정의한 메시지 포멧으로 변환하는 모듈입니다.

Lambda에서는 zthing-message-converter를 이용하여 메시지를 처리합니다.

[자세히 살펴보기](./zthing-message-converter/docs/README.md)
