# network

## Router (공유기)
![image](https://user-images.githubusercontent.com/41819129/115110106-9e146b00-9fb4-11eb-85a3-2486164b61c8.png)
- WAN(Wide Area Network)와 LAN(Local Area Network)를 이어주는, 중개해주는 역활은 하는 것이 라우터이다.
- 스마트폰, PC등 장비들을 무선 또는 유선으로 라우터에 연결하면 네트워크를 사용할 수 있다.
- WAN으로 할당받은 주소를 'public ip address'. LAN으로 할당받은 주소를 'private ip address' 라고 한다.

## NAT (NetWork Address Translation)
- 클라인어트가 라우터를 거쳐 네트워크를 사용할 때 자신의 Private ip를 Public ip로 변경하는 기술이다.
- 이것을 통해 외부의 네트워크와 접속이 가능해진다.

## Port
- 외부에서 라우터를 통해 접속이 들어왔을 때 연결 될 서버를 알려주기 위해 Port를 명시한다.
- 서버가 활성화 상태라면 서버는 해당 Port에서 연결을 리스닝하고 있다.
![image](https://user-images.githubusercontent.com/41819129/115110861-67405400-9fb8-11eb-90de-512c434cf39a.png)
- 0~1023까지 포트는 이미 지정된 포트이다.

## Port Forwarding
- 라우터로 들어온 포트 번호를 미리 설정해서 내부 네트워크에 있는 특정 포트로 요청을 포워딩 할 수 있다.

## 유동아이피, 고정아이피
- ipv4 체계에서 할당할 수 있는 ip의 수가 부족하다.
- 유동아이피는 주기적으로 ip가 변경 될 수 있다.
- 고정아이피는 변경되지 않는다.

## DHCP (Dynamic Host Configuration Protocol)
- 자동으로 라우터에 연결된 장비에 ip주소를 할당해주는 프로토콜이다.
- ip를 할당받은 장비는 네트워크 접속이 가능해진다.
- DHCP는 MAC주소를 기반으로 임대를 해주는데 여기서 MAC주소는 물리적인 기계(단만기)를 구별하기 위한 것이다. (Physical Address)
