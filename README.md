<p align="center">
    <img width="200px;" src="https://raw.githubusercontent.com/woowacourse/atdd-subway-admin-frontend/master/images/main_logo.png"/>
</p>
<p align="center">
  <img alt="npm" src="https://img.shields.io/badge/npm-6.14.15-blue">
  <img alt="node" src="https://img.shields.io/badge/node-14.18.2-blue">
  <a href="https://edu.nextstep.camp/c/R89PYi5H" alt="nextstep atdd">
    <img alt="Website" src="https://img.shields.io/website?url=https%3A%2F%2Fedu.nextstep.camp%2Fc%2FR89PYi5H">
  </a>
</p>

<br>

# 지하철 노선도 미션
[ATDD 강의](https://edu.nextstep.camp/c/R89PYi5H) 실습을 위한 지하철 노선도 애플리케이션

<br>

## 🚀 Getting Started

### Install
#### npm 설치
```
cd frontend
npm install
```
> `frontend` 디렉토리에서 수행해야 합니다.

### Usage
#### webpack server 구동
```
npm run dev
```
#### application 구동
```
./gradlew bootRun
```

### step0
- 컨트롤러 테스트라고 볼 수 있는데, response 검증은 하지 않아도 되는지?

### step1 생각해보기
- 상황은 기존 서비스가 잘 돌아가는 상황에서 최소 시간 경로를 조회하는 기능을 추가해달라고 요청이 온 상황.
- 우선은 도메인에서 가능한지를 먼저 볼 것 같음.
- 가능하다는 생각이 들면, 인수 테스트 작성. - 새로운 기능 추가이므로 인수 테스트 추가.
- 작성한 이후, 문서화 테스트를 작성하고, 컨트롤러 구현 - Service에 관한 것은 stubbing을 통해서 컨트롤러만 테스트하도록 한다.(요청을 받고 응답을 하는 테스트)
- 우선 여기까지.

### step1
- Steps클래스는 단계를 나타내는 역할로 알고 있는데, parameter를 만드는 메서드를 둬도 되는지? ex) LineSteps.createSectionCreateParams()메서드.
- 문서화실습 맨 마지막에 중복 제거가 있는데 PathSteps처럼 하는 게 맞는지 잘 모르겠음.

### step2 생각해보기
- 경로 조회 결과에 요금 정보도 추가된다.
- 경로 조회 결과를 Sections로 가지고 있고, 요금 정보를 계산하기 위한 정보(거리)를 ~~Sections가 가지고 있으므로 책임을 위임한다?~~ 요금을 계산하는 역할을 줄 객체를 만든다.