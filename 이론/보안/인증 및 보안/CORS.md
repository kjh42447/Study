# CORS
Cross Origin Resource Sharing의 약자로, 어플리케이션 간의 출처가 다른 경우 스크립트 기반의 HTTP 통신을 통한 접근이 제한되는 정책인 SOP(Same Origin Policy)의 예외 조항으로써, 사전 설정을 통해 리소스에 선택적으로 접근할 수 있는 권한을 부여하도록 브라우저에 알려주는 정책이다. 즉 브라우저는 SOP에 의해 기본적으로 다른 출처의 리소스 공유를 차단하지만, CORS를 통해 접근 권한을 얻을 수 있게 되는 것이다.

### CORS 정책 동작 방식
- 프리플라이트 요청 : 실제 요청을 보내기 전, OPTIONAL 메소드로 사전 요청을 보내 해당 출처 리소스에 접근 권한이 있는지부터 확인하는 방식이다.
- 단순 요청 : 특정 조건이 만족되면 프리플라이트 요청을 생략하고 요청을 보내는 방식이다.
- 인증 정보를 포함한 요청(Credentialed Request) : 요청 헤더에 인증 정보를 담아 보내는 요청이다. 출처가 다를 경우에는 별도의 설정을 하지 않으면 쿠키를 보낼 수 없다. 이 경우 프론트, 서버 양측 모두 CORS 설정이 필요하다.

### CORS 정책 설정 방법
- 애너테이션을 이용하여 컨트롤러에서 설정
- Global 설정 클래스를 이용하여 특정 도메인에 모두 적용