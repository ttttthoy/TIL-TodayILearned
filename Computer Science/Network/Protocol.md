## 프로토콜 (Protocol)
기기들 간의 원활한 데이터 교환을 위해 표준화한 통신 규약
<br/>

### 주기능

- 단편화와 재결합
- 캡슐화 : 데이터에 송수신지 주소, 오류 검출 코드, 제어정보 등을 부가하는 것
- 흐름제어 : 전송량이나 속도 
  - 정지대기, 슬라이딩 윈도우방식
- 오류제어
- 동기화 : 송,수신측 같은 상태 유지하도록 타이밍 맞춤
- 순서제어 : 전송순서 부여. 연결 위주의 데이터 전송 방식에만 사용
- 주소지정 
- 다중화 : 한 개의 통신 회선을 여러 가입자들이 동시에 사용하도록
- 경로제어

### TCP/IP
인터넷에 연결된 서로 다른 컴퓨터가 데이터를 주고받을 수 있는 표준 프로토콜 <br/>
UNIX의 기본 프로토콜로 사용되었고, 현재는 인터넷 범용 프로토콜.

> TCP (Transmission Control Protocol)
- OSI 7계층 전송계층에 해당
- 연결형 서비스 제공
- 패킷의 다중화, 순서제어, 오료제어, 흐름제어 기능 제공
- 스트림(Stream) 전송 기능 제공
- 헤더에 시퀀스 번호, 포트번호, checksum 등이 포함됨

> IP (Internet Protocol)
- OSI 7계층 전송계층에 해당
- 데이터그램 기반의 비연결형 서비스 제공
- 패킷의 분해, 조립, 주소지정, 경로선택 기능 제공
- 헤더길이 : 20Byte ~ 60Byte
- 헤더에 버전, 헤더길이, 전체 패킷 길이, checksum, ip주소, 목적지 ip주소 등 포함
