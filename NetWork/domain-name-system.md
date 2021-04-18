# DNS (DomainNameSystem)

## DNS 개요
![image](https://user-images.githubusercontent.com/41819129/115143158-9d490b00-a080-11eb-9871-260a5bd8c065.png)
- DNS 서버가 해당 아이피의 도메인 주소를 등록한다.
- 클라이언트가 도메인 주소를 입력하게 되면 로컬의 'hosts' 파일을 먼저 확인하고 없다면 DNS 서버에서 확인 후 해당 아이피로 연결 후 통신

## Public DNS
-  구글, 1.1.1.1과 같이 무료로 DNS Server를 이용할 수 있도록했다.

## 도메인 이름의 구조
![image](https://user-images.githubusercontent.com/41819129/115147580-9fb65f80-a096-11eb-9de5-c4bd662e7edd.png)
- 사용자가 도메인 주소를 조회했을 때 기본적으로 등록되어 있는 Root DNS 서버에게 해당 도메인 주소를 아이피를 물어본다.
- Root DNS 서버는 해당 도메인 주소를 모르기 때문에 'com'을 관리하는 Top-level DNS 서버를 알려준다.
- 같은 방식으로 순차적으로 접근해서 Sub DNS 서버에 접근하게 되고 해당 도메인 주소에 ip를 알고있는 Sub DNS 서버가 ip를 알려준다.
- 이러한 DNS 서버의 계층적 구조로 인해 전세계의 도메인 주소의 ip를 알 수 있다.
