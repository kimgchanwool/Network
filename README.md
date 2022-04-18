# Network

# 2022-04-18
![](https://velog.velcdn.com/images/soe8192/post/c7cc3d82-63ee-409b-95e6-439cbe8420df/image.png)
* by https://microchipdeveloper.com/tcpip:tcp-vs-udp



## TCP
- 3way handshake
![3way handshake](https://velog.velcdn.com/images/soe8192/post/294064a7-581a-4a9e-8532-4809256e5677/image.png)
 - 4way handshake
![4way handshake](https://velog.velcdn.com/images/soe8192/post/1744b97e-8d6d-4668-b9d9-bf69237c320b/image.png)

TCP는 그림에서처럼 1대1 통신이며
상대와의 연결과 해지에 각각 3way handshake 4way handshake를 사용한다.

3way handshake는 연결에 쓰이며
c)접속하고 싶어
s)생각해봤는데 괜찮네 접속해
c)접속했어
라고 생각하면 편하고
4way handshake는
c)해제하고 싶어
s)음 일단 기다려봐 고민좀 하고 올게 
s)그래 해제하던지
s)해제할게~
의 구조이다.
근데 tcp를 해제한 이후에 도착하는 패킷이 있을 수도 있다.
이 패킷은 연결된 동안 보내진 패킷이기에(재전송의 사유나 문제등으로)
클라이언트는 이를 받기 위한 유예의 240초를 가진다.(이동안의 데이터는 유실되지 않고 클라이언트에 잘 전달된다.

### 특징
1. 연결성
2. 보안성
3. 속도가 대신 UDP보다 느림
4. UDP처럼 다대 다 또는 1대 다가 안된다.
-> 파일 전송에 주로 사용된다.
현재는 대부분이 TCP이다.
(속도문제가 해결된다면 굳이 UDP를 쓸 필요가 없다..)

## UDP

이는 보안보다는 속도에 치중하여
상대와 연결되지 않은 상태에서도 데이터를 보낸다.
(받을 수 있을 지는 모르는 상황이다.)
-> 스트리밍에 주로 사용된다.
(현재는 잘 사용하지 않음)

### 특징
1. 비연결성
2. 보안성이 안좋음
3. 속도가 빠름
4. 1대 다 또는 다대 다 통신이 가능


https://mindnet.tistory.com/entry/%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC-%EC%89%BD%EA%B2%8C-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0-22%ED%8E%B8-TCP-3-WayHandshake-4-WayHandshake
해당 글을 참조하여 제작된 게시글입니다.
