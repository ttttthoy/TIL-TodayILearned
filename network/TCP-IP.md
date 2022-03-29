###  IP(Internet Protocol)
OSI 7계층 중 3계층(네트워크 계층)에서 사용되는 논리적인 주소. 32bits의 길이, 네트워크 ID와 호스트 ID로 구성되어 있음

- ifconfig 명령 : 현재 설치된 네트워크 설정내용 출력
```
# ifconfig [인터페이스명][옵션]
```
- ip 명령
  - addr : 네트워크 인터페이스 정보 출력,추가,삭제
  - route : 라우팅 테이블 정보
  - link : 네트워크 인터페이스 상태 출력,관리

### 서브네팅

IPv4 주소의 고갈로 인해 하나의 네트워크를 여러 개의 서브 네트워크로 나누어 낭비를 막기위한 방법 
- 서브넷 마스크(Subnet mask) 
  - IP 주소를 네트워크 주소와 호스트 주소로 구분하기 위한 주소

###  TCP(Transmission Control Protocol)
신뢰적이고 연결지향적인 프로토콜 <br/>
전이중(full-duplex) 통신 : 동시에 양방향 전달 가능

### 네트워크 명령
- netstat 명령 : 네트워크 상태정보 출력
  - -a : 모든 정보
  - -n : 호스트이름을 ip주소로 출력
  - -l : 현재 listen 상태인 소켓
  - -p : 프로세스 이름과 PID 
  - -t, -u : tcp/udp 
 
- ping : 목적지에 ICMP 패킷보내 상태 점검
- traceroute : 목적지까지 패킷이 지나가는 경로 출력

### DNS
- /etc/resolv.conf 파일 : 네임서버 정의되어 있는 파일
- /etc/hosts 파일 : 도메인/호스트명과 ip주소 매핑정보 저장된 파일




