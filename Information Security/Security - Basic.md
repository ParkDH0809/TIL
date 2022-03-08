기술이 발달함에 따라 정보보안은 필수 요소이다.
=====
이러한 정보보안의 기초에 대해 알아보자.
-----
**content**
1. [CIA](#CIA)
2. [Secutiry Threats](#Security-Threats)
***
### CIA
#### CIA : 보안의 3대 요소
1. Confidentiality (기밀성)  
  권한이 없는 자가 정보를 읽을 수 없어야 한다. (ex-암호화)  
  공격 방법 : Snooping(스누핑) 등
  
2. Integrity (무결성)  
  권한이 없는 자가 정보를 변경 및 변조할 수 없어야 한다. (ex-전자서명)  
  공격 방법 : Virus 등
  
3. Availability (가용성)  
  사용자가 원하는 정보에 접근하고자 할 때 안전하게 Access할 수 있어야 한다.   
  즉, 사용자에게 정상적인 서비스를 제공할 수 있어야 한다.  
  공격 방법 : DoS, DDoS 등
    
    
#### 인증(Authentication)과 인가(Authorization)
1. 인증(Authentication) : 사용자가 누구인지 확인하는 것 (본인인증 등)  
Network가 포함된 인증 방법에선 공격을 받을 위협이 있으므로 보안 프로토콜과 암호학적 기술이 필요하다.  
<img src="/assets/images/Security_Authentication.PNG" width="350" height="220">

2. 인가(Authorization) : 인증한 사용자의 권한을 제어.  
사용자가 이용 가능한 서비스의 정도를 제어한다. 
예를 들어 블로그의 경우  

|  |블로그 주인|그 외|
|:---:|:---:|:---:|
|글 쓰기|O|X|
|글 읽기|O|O|

위와 같이 인가에 따라 권한 차이가 있는 것이다.  
이러한 보안 메커니즘은 SW 상에서 구현 된다. 이 때, Bugs, Virus, worm, OS secutiry 등 문제가 발생할 수 있으므로 주의해야 한다.

***
### Security Threats
보안 사고 발생 원인

