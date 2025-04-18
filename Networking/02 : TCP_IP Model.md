# 📚 TCP/IP 모델이란?
- **컴퓨터와 네트워크가 데이터를 주고받는 기본 프로토콜**
- **인터넷을 포함한 대부분의 네트워크에서 사용**
- **IP: 데이터 전송 경로 지정, TCP: 안정적인 데이터 전송 담당**
- **이메일, 파일 전송, 원격 로그인 등 주요 네트워크 기능 지원**
- **하드웨어나 운영체제에 상관없이 작동하는 유연한 구조**

<img src="./image/2_1.png" alt="설명" width="400" style="display: block; margin: auto;">
<br>

## 📖 TCP/IP 4계층 모델

### 1. 네트워크 접근 계층
- **데이터 단위:** 프레임  
- **전송 주소:** MAC 주소  
- **역할:**  
  - 데이터를 실제 네트워크를 통해 전송하는 물리적 기능 수행  
  - 다른 컴퓨터로 데이터를 직접 송신 및 수신  
- **대표 프로토콜:** Ethernet, Wi-Fi, PPP  

### 2. 인터넷 계층
- **데이터 단위:** 패킷  
- **전송 주소:** IP 주소  
- **역할:**  
  - 패킷을 출발지에서 목적지로 전달  
  - 라우팅, 주소 지정, 패킷 포워딩 수행  
- **대표 프로토콜:** IP, ICMP, ARP  

### 3. 전송 계층
- **데이터 단위:** 세그먼트  
- **전송 주소:** 포트 번호  
- **역할:**  
  - 애플리케이션 간 논리적 통신 제공  
  - 데이터의 정확한 전송을 보장 (흐름 제어, 오류 제어, 혼잡 제어 수행)  
- **대표 프로토콜:** TCP, UDP  

### 4. 응용 계층
- **데이터 단위:** 데이터/메시지  
- **역할:**  
  - 사용자와 네트워크 간의 인터페이스 제공  
  - 암호화, 사용자 인증 등의 보안 기능 수행  
  - 애플리케이션이 네트워크를 통해 데이터를 송수신할 수 있도록 지원  
- **대표 프로토콜:** HTTP, FTP, SMTP, DNS, Telnet  

## 📖 TCP 통신
> 한 컴퓨터에서 다른 컴퓨터로 전송되는 모든 데이터가 오류나 결함 없이 올바른 순서로 성공적으로 수신되도록 하기 위한 것

### 통신 방식
1. 한 컴퓨터(발신자)가 수신 컴퓨터에게 초기 메시지를 보내 연결 설정을 공식적으로 요청합니다. 이를 SYN 메시지(동기화의 줄임말)라고 합니다.
2. 그런 다음 수신 컴퓨터는 SYN에 대한 승인(SYN-ACK 메시지라고 함)을 보내야 합니다. 
3. 마지막으로 발신자가 확인을 승인해야 합니다(수신 확인 메시지라고 함).

<img src="./image/2_2.png" alt="설명" width="400" style="display: block; margin: auto;">
<br>

## 📖 UDP 통신
> 한 컴퓨터에서 다른 컴퓨터로 전송되는 모든 데이터를 빠르게 전달하지만, 오류 검출이나 순서 보장 없이 수신하도록 하기 위한 것

### 통신 방식
1. 발신 컴퓨터가 데이터를 바로 전송합니다. 연결을 설정하는 과정이 없습니다.  
2. 수신 컴퓨터는 데이터를 받지만, 이를 확인하거나 순서를 보장하지 않습니다.  
3. 발신 컴퓨터는 수신 확인을 기다리지 않고 계속해서 데이터를 전송합니다.  

<img src="./image/2_3.png" alt="설명" width="500" style="display: block; margin: auto;">