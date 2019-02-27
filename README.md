# msadev-config
MSA config

---------

* 스프링클라우드 컨피그(config) 서버 생성.
* 스프링클라우드 기반 마이크로서비스 프로젝트 생성 . 라이센스서비스
* 스프링클라우드 유레카(Eureka) 서버 생성.
* 라이센스 서비스에 유레카 클라이언트 추가하여 유레카 서버와 연결.
* spring boot Admin 의존성을 기존 컨피그 프로젝트에 추가. yml 설정파일 수정. context-path설정.
* 게이트웨이(zuul) 서비스 추가 구성 (새로운 프로젝트로)
** asd

### 서버 작동 순서
```
1. 컨피그 서버 실행 (스프링 부트 어드민 포함)
2. 유레카 서버 실행
3. 마이크로서비스 서버 실행
```
### 호출 url
* [컨피그서버 http://localhost:8888/config/licensingservice/default](http://localhost:8888/config/licensingservice/default)
* [스프링부트어드민 http://localhost:8888/admin](http://localhost:8888/admin)
* [라이센스 서비스 호출 http://desktop-9hcaj4p:8082/v1/org/IFD/licenses/20190001 서비스명은 가변적임](http://desktop-9hcaj4p:8082/v1/org/IFD/licenses/20190001)
* [Zuul 게이트웨이 호출 http://localhost:8087/api/license/v1/org/USARMY/licenses/CS_098722](http://localhost:8087/api/license/v1/org/USARMY/licenses/CS_098722)
* [zuul 서비스되고 있는 routes 확인 http://localhost:8087/actuator/routes](http://localhost:8087/actuator/routes)
