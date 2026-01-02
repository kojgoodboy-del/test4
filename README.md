# Simple Board Site — JSON 저장 버전 (운영자만 글작성)

이 버전은 **SQLite/better-sqlite3를 제거**해서 Windows에서 `npm install` 에러(node-gyp/SDK) 없이 바로 됩니다.

## 1) 설치
PowerShell에서 (npm이 막히면 아래 "PowerShell 보안" 먼저)

```powershell
npm.cmd install
```

### PowerShell 보안(스크립트 실행 차단) 때문에 npm이 안 되면
```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

## 2) 실행(포트 8888 권장)
```powershell
$env:PORT="8888"
$env:ADMIN_USERNAME="admin"
$env:ADMIN_PASSWORD="1234"
$env:SESSION_SECRET="change-me-please"
npm.cmd start
```

- 홈: http://localhost:8888
- 관리자: http://localhost:8888/admin.html

## 3) 데이터 저장
- 글은 `data.json` 파일에 저장됩니다.
- 서버 껐다 켜도 유지됩니다.
