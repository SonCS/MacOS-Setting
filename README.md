# MacOS-Setting
MacOS Setting 관련 내용 정리

## MacOS 관련 설정
### 전원
* 잠자기에서 대기모드로 전환되는 시점 늦추기
```bash
# 현재 설정 상태 확인 명령어
pmset -g |grep standbydelay

# 설정 값 변경 명령어
sudo pmset -a standbydelay `원하는시간(밀리초)`
Passwoad: `사용자 비밀번호 입력`
Warning: Idle sleep timings for "Battery Power" may not behave as expected.
- Disk sleep should be non-zero whenever system sleep is non-zero.
```

### Dock 가리기 속도 개선
* 커서를 Dock 위치에 둔 후 Dock이 모습을 나타내기까지 소요되는 대기시간 수정
```bash
# 대기시간 변경 명령어
defaults write com.apple.Dock autohide-delay -float '대기시간(0~1)'; killall Dock

# 초기상태 복구 명령어
defaults write com.apple.Dock autohide-delay; killall Dock
```

* Dock 애니메이션 효과 속도 변경
```bash
# 애니메이션 속도 변경 명령어
defaults write com.apple.dock autohide-time-modifier -float '애니메이션속도(0-1)';killall Dock
애니메이션 속도를 0으로 설정 시 애니메이션 효과를 완전히 삭제할 수 있습니다. 
커서를 Dock 위치에 가지고 가면 뿅하고 나타납니다.

# 초기상태 복구 명령어
defaults delete com.apple.dock autohide-time-modifier;killall Dock
```

### LaunchPad 아이콘 크기 및 개수 조절
```bash
# 크기 변경 명령어
defaults write com.apple.dock springboard-columns -int [가로]
defaults write com.apple.dock springboard-rows -int [세로]
killall dock

# 복구 명령어
defaults delete com.apple.dock springboard-columns
defaults delete com.apple.dock springboard-rows
killall Dock
```

## 유틸리티
### Rectangle
* 화면 분할 (기존 Spectacle 업데이트 중지로 인해 대체 프로그램)
* IDE에서 정상동작함. :)
* 다운로드URL : https://rectangleapp.com/


### WinArchiver Lite
* Windows에서 한글이 깨지지 않도록 압축해주는 프로그램
* 다운로드URL : https://itunes.apple.com/kr/app/winarchiver-lite/id414855915?mt=12


### NameChanger
* 파일이름을 쉽게 변경
* 다운로드URL : https://mrrsoftware.com/namechanger/


### OnyX
* 최적화 유틸리티
* 다운로드URL : https://www.titanium-software.fr/en/index.html

### Karabiner-Elements
* 키보드 커스터마이징 키맵핑 프로그램
* 한영키 딜레이 이슈 해결 방안

## TODO LIST
* Mail.app 서명 설정 내용 정리


