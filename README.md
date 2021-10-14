<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/v/@nestjs/core.svg" alt="NPM Version" /></a>
<a href="https://circleci.com/gh/nestjs/nest" target="_blank"><img src="https://img.shields.io/circleci/build/github/nestjs/nest/master" alt="CircleCI" /></a>
<a href="https://coveralls.io/github/nestjs/nest?branch=master" target="_blank"><img src="https://coveralls.io/repos/github/nestjs/nest/badge.svg?branch=master#9" alt="Coverage" /></a>

## Local 환경에서 Docker를 통해 실행을 하는 방법 

#### 미리 설치 해야 할 것

- Node.js 14 이상 & npm
- yarn 1.0 이상
- Docker Deskop
- docker-compose

1. yarn 이 깔려있지 않다면, 다음 명령어를 실행합니다.

```bash
# 아무대서나 실행 가능
$ npm install -g yarn
```

**yarn을 깔 때 빼곤 `npm` 명령어를 사용할 일이 없으니 유의해주세요.**



#### Docker 컨테이너를 통해 서버와 DB를 띄우는 방법

2. yarn 및 docker-compose 가 잘 설치 되었나 확인

```bash
$ yarn --version
1.22.5 # 이렇게 버전 명이 뜨면 성공 (꼭 이 버전과 일치하지 않아도 무방)

$ docker-compose --version
docker-compose version 1.29.1, build c34c88b2 # # 이렇게 버전 명이 뜨면 성공 (꼭 이 버전과 일치하지 않아도 무방)
```



3. 패키지 의존성 설치 (package.json이 바뀔 때 마다 해주어야 함 )

```bash
# 디렉토리 루트에서 실행
$ yarn
```

이러면 패키지들이  깔리고, 이미 다 깔려있다면 `Already up to date` 라 뜨게 됨



4. Docker compose를 통해 컨테이너를 띄우고 정해진 명령어를 미리 실행해 서버와 디비를 띄웁니다. (따라서 우리는 따로 서버와 디비를 킬 필요가 없음)

```bash
# 주의 프로젝트 루트 디렉토리에서 실행해야함!
$ docker-compose -f docker-compose.dev.yml up
```



5. 개발을 마치고 종료할 때 (터미널에서 도커 환경을 끄고 싶을 때)

```bash
Ctrl+C 누르면 됨 (Mac & Windows 동일함)
```





## Local 환경에서 서버만 띄우는 방법 

#### TBD....



## Installation

```bash
$ yarn
```



## Running the app

```bash
# development
$ yarn start

# watch mode
$ yarn start:dev

# production mode
$ yarn start:prod
```

