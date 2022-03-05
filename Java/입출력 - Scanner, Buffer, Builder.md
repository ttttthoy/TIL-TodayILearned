### Scanner 

- Scanner 버퍼크기 : 1024 chars
- BufferedReader 버퍼크기 : 8192 chars

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;BufferedReader가 더많은 버퍼를 차지하고 더 많은 입력을 처리할 수 있음<br/>

- Scanner 는 int, short, long, float, double, String을 구분지어 읽어들임
- BufferedReader는 String밖에 읽어들이지 못함
- Scanner 는 정규식으로 값을 파싱함. nextInt(), nextLong(), nextDouble() 등의 함수 사용
- BufferedReader는 문자열만 읽어들이므로 readLine() 만 사용


### BufferedReader
- Scanner와 달리 동기화를 사용하므로 스레드간에 개체를 공유할 수 있다.
- Scanner는 싱글 쓰레드 이므로 buffer보다는 빠르지만 정규식 사용으로 인해 실제 속도차이 에서는 BufferedReader가 앞선다.

### BufferedWriter

### StringBuilder

