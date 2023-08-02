## 우선 우리는 JWT 토큰 방식으로 관리를 하기 위해 JWT토큰 방식에 대해 알아야 한다.

# 🔑 JWT

- JWT(JSON Web Token)란 인증에 필요한 정보들을 암호화시킨 JSON 토큰을 의미한다. 그리고 JWT기반 인증은 JWT 토큰(Access Token)을 HTTP헤더에 실어 서버가 클라이언트를 식별하는 방식이다.
- JWT JSON 데이터를 Base64 URL -safe Encode를 통해 인코딩하여 직렬화한 것이며, 토큰 내부에는 위변조 방지를 위해 개인크를 통한 전자서명도 들어있다. 따라서 사용자가 JWT를 서버로 전송하면 서버는 서명을 검증하는 과정을 거치게 되며 검증이 완료되면 요청한 응답을 돌려준다.
- Base64 URL -safe Encode는 일반적인 Base64 Encode에서 URL에서 오류없이 사용하도록 +, /를 각각 -, \_ 로 표현한 것이다.

## 🔑JWT 구조

JWT는 .을 구분자로 나누어지는 세 가지 문자열의 조합이다.
.을 기준으로 좌측부터 Header, Payload, Signature을 의미한다.
<br>
<img width="1099" alt="스크린샷 2023-07-03 오후 12 23 03" src="https://github.com/jaynamm/playground-react/assets/123732776/dd8a1497-902e-4afc-9ca2-f44b482c089d">
<br>
Header에는 JWT에서 사용할 타입과 해시 알고리즘의 종류가 담겨 있으며, Payload는 서버에서 첨부한 사용자 권한 정보와 데이터가 담겨있다. Signature에는 Header, Payload를 Base64 URL -safe Encode를 한 이후 Header에 명시된 해시함수를 적용하고, 개인키(Private Key)로 서명한 전자서명이 담겨 있다.

## 🔑 JWT 인증과정

- 사용자가 ID, PW를 입력하여 서버에 로그인 인증을 요청한다.
- 서버에서 클라이언트로부터 인증요청을 받으면, Header,. PayLoad, Signature를 정의한다.
- Header, PayLoad, Signature를 각각 Base64로 한 번 더 암호화하여 JWT를 생성하고 이를 쿠키에 담아 클라이언트에게 발급한다.
- 클라이언트는 서버로부터 받은 JWT를 localStorage 저장한다. (쿠키나 다른 곳에도 저장 가능 보통 localStorage에 저장을 한다. )
- API를 서버에 요청할 때 Authorization header에 AccessToken을 담아서 보낸다.
- 서버가 할 일은 클라이너트가 Header에 담아서 보낸 JWT가 내 서버에서 발행한 토큰인지 여부를 확인하여 일차한다면 인증을 통과시켜주고 아니라면 통과시키지 않으면 된다. 인증이 통과되었으면 페이로드에 들어있는 유저의 정보들을 select해서 클라이언트에게 돌려준다.
- 클라이언트가 서버에 요청을 했는데, 만일 AccessToken의 시간이 만료되면 클라이언트는 RefreshToken을 이용해서 서버로부터 새로운 엑세스 토큰을 발급받는다.

## ✅ JWT의 장점

- Header와 Payload를 가지고 Signature를 생성하므로 데이터 위변조를 막을 수 있다.
- 인증정보에 대한 별도에 저장소가 필요없다.
- JWT는 토큰에 대한 기본정보와 전달할 정보 및 토큰이 검증됬음을 증명하는 서명 등 필요한 모든 정보를 자체적으로 지니고 있다.
- 클라이언트 인증정보를 저장하는 세션과 다르게, 서버는 무상태가 되어 서버 확장성이 우수해질 수 있다.
- 토큰 기반으로 다른 로그인 시스템에 접근 및 권한 공유가 가능하다. (쿠키와 차이)
- OAuth의 경우 FaceBook, Google, Kakao 등 소셜계정을 이용하여 다른 웹 서비스에서도 로그인을 할 수 있다.
- **모바일 어플리케이션 환경에서도 잘 동작한다.** (모바일은 Session 사용이 불가능하다.)

## 🚨 JWT의 단점

- Self-contained : 토큰 자체의 정보를 담고 있으므로 양날의 검이 될 수 있다.
- 토큰 길이 : 토큰의 Payload에 3종류의 클레임을 저장하기 때문에, 정보가 많아질수록 토큰의 길이가 늘어나 네트워크에 과부화를 줄 수 있다.
- Payload 인코딩 : playload자체는 암호화 된 것이 아니라 Base64로 인코됭 된 것이기 때문에, 중간에 Payload를 탈취하여 디코딩하면 데이터를 볼 수 있으므로, playload에 중요 데이터를 넣지 않아야 한다.
- Store Token : stateless 특징을 가지기 때문에, 토큰은 클라이언트 측에서 관리하고 저장한다. 때문에 토큰 자체를 탈취당하면 대체하기가 어렵게 된다.

# 🔒 Access Token & Refresh Token

JWT도 제 3자에게 토큰 탈취의 위험성이 있기 때문에, 그대로 사용하는 것이 아닌 AccessToken, Refresh Token으로 이중으로 나누어 인증을 하는 방식을 현업에선 취한다.
Access Token과 Refresh Token은 둘다 똑같은 JWT이다. 다만 토큰이 어디에 저장되고 관리되느냐에 따른 사용 차이일 뿐이다.

### 🔒 **Access Token** : 클라이언트가 갖고있는 실제로 유저의 정보가 담긴 토큰으로, 클라이언트에서 요청이 오면 서버에서 해당 토큰에 있는 정보를 활용하여 사용자정보에 맞게 응답을 진행

### 🔒 **Refresh Token** : 새로운 Access Token을 발급해주기 위해 사용하는 토큰으로 짧은 수명을 가지고 있는 Access Token에게 새로운 토큰을 발급해주기 위해 사용. 토큰은 보통 데이터베이스에 유저정보와 같이 기록.

Access Token은 접근에 관여하는 토큰
Refresh Token은 재발급에 관여하는 토큰의 역할로 사용
