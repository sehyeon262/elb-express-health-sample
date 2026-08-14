# ELB Express Health Sample

> AWS ELB 헬스체크를 위한 Express 서버 샘플입니다.

## Tech Stack

- Node.js
- Express 4

## Endpoints

| Method | Path | Description |
| --- | --- | --- |
| `GET` | `/` | `Hello World!` 응답 |
| `GET` | `/health` | HTTP 상태 코드 `200` 응답 |

## Run Locally

```bash
npm install
node app.js
```
서버는 기본적으로 `http://localhost:3000`에서 실행됩니다.
```bash
curl -i http://localhost:3000/health
```
정상 동작하면 200 OK 응답을 반환합니다.


## ELB Health Check
ELB 대상 그룹의 헬스체크 경로로 `/health`를 사용합니다.
```
Protocol: HTTP
Path: /health
Success codes: 200
Port: Traffic port
```

## Related Learning
- ELB 헬스체크 동작 방식
- 대상 그룹(Target Group) 상태 확인
- Express 서버를 활용한 헬스체크 엔드포인트 구현
