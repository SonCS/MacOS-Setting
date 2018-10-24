# MacOS-Setting
MacOS Setting 관련 내용 정리

## 전원
* 잠자기에서 대기모드로 전환되는 시점 늦추기
```
# 현재 설정 상태 확인 명령어
pmset -g |grep standbydelay

# 설정 값 변경 명령어
sudo pmset -a standbydelay `원하는시간(밀리초)`
Passwoad: `사용자 비밀번호 입력`
Warning: Idle sleep timings for "Battery Power" may not behave as expected.
- Disk sleep should be non-zero whenever system sleep is non-zero.
```

## 유틸리티
### Spectacle
* 화면 분할
* 다운로드URL : https://www.spectacleapp.com/
### WinArchiver Lite
* Windows에서 한글이 깨지지 않도록 압축해주는 프로그램
* 다운로드URL : https://itunes.apple.com/kr/app/winarchiver-lite/id414855915?mt=12
### InsomniaX
* 상단을 닫았을 때 잠자기모드 전환 방지
* 다운로드URL : http://semaja2.net/ye-ol-projects/insomniaxinfo/
### NameChanger
* 파일이름을 쉽게 변경
* 다운로드URL : https://mrrsoftware.com/namechanger/

## TODO LIST
* Mail.app 서명 설정 내용 정리


