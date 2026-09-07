# 프로그램 정리 목록

`제어판 → 프로그램 및 기능`에서 확인한다. 아래는 중고 PC에서 실제로 자주 발견되는 것들이다.

## 목차

- [제거 대상: 한국 금융 보안 프로그램](#제거-대상-한국-금융-보안-프로그램)
- [제거 대상: 제조사 유틸리티](#제거-대상-제조사-유틸리티)
- [절대 제거하지 말 것](#절대-제거하지-말-것)
- [남기는 것](#남기는-것)
- [판단이 갈리는 것](#판단이-갈리는-것)
- [발견되면 문제인 것](#발견되면-문제인-것)
- [정리 순서](#정리-순서)

---

## 제거 대상: 한국 금융 보안 프로그램

은행·정부·증권 사이트에 접속하면 강제로 설치되는 것들이다. 열 개 가까이 깔려 있는 경우가 흔하다.

| 프로그램 | 제작사 |
|---|---|
| nProtect Online Security | INCA Internet |
| TouchEn nxKey (with E2E) | RaonSecure |
| KeySharp CertRelay | RaonSecure |
| WIZVERA Process Manager | WIZVERA |
| WIZVERA Veraport (보안모듈 관리) | WIZVERA |
| WIZVERA Delfino | WIZVERA |
| CROSSCERT UniCRSV | Crosscert |
| iniLINE CrossEX Service | iniLINE |
| IPinside LWS Agent | interezen |
| REPORTX | DigitalZone |
| AhnLab Safe Transaction | 안랩 |
| INISAFE CrossWeb EX | 이니텍 |
| XecureWeb | 소프트포럼 |

### 제거하는 이유

**백그라운드에서 상주하며 시스템 자원을 계속 쓴다.** 부팅 시간이 늘어나고 전반적으로 무거워진다.

**키보드 입력을 가로채는 방식으로 동작한다.** 목적은 보안이지만 구조적으로는 키로거와 같다. 필요하지 않은 PC에 둘 이유가 없다.

**호환성 문제를 일으킨다.** 게임이나 다른 프로그램과 충돌하는 사례가 있다.

### 제거 후 영향

**해당 은행·정부 사이트는 안 될 수 있다.** 다만 필요해지면 그 사이트에서 다시 설치하라고 안내가 나오므로 되돌릴 수 있다.

자녀용·게임용 PC라면 애초에 쓸 일이 없다. 사용자가 그 PC로 금융 업무를 볼 계획이 있는지만 확인하고 진행한다.

---

## 제거 대상: 제조사 유틸리티

메인보드나 그래픽카드에 딸려오는 묶음이다. 오버클럭, 팬 제어, 바이오스 업데이트, RGB 제어용이다.

### 기가바이트

APP Center, EasyTune, EasyTuneEngineService, @BIOS, SIV, GService, Smart Backup, RGB Fusion

### ASUS

Armoury Crate, AI Suite, Aura Sync, ASUS Framework Service

### MSI

MSI Center, Dragon Center, Mystic Light, Live Update

### ASRock

ASRock Motherboard Utility (A-Tuning), Polychrome RGB, Restart to UEFI

### 제거하는 이유

일반 사용에는 필요 없고, **업데이트 알림을 자주 띄우며 자기 구성 요소를 계속 추가한다.** APP Center와 Armoury Crate는 특히 무겁고 광고성 알림이 있다.

**바이오스 업데이트는 제조사 사이트에서 파일을 받아 직접 하는 게 더 안전하다.** 유틸리티를 통한 업데이트는 실패 사례가 있다.

**RGB 제어가 필요하면 남긴다.** 케이스나 램에 LED가 있고 사용자가 색을 바꾸고 싶어 하면 해당 프로그램만 유지한다.

---

## 절대 제거하지 말 것

### Microsoft Visual C++ 재배포 패키지

목록에 이런 식으로 여러 개가 보인다.

```
Microsoft Visual C++ 2012 Redistributable (x86) - 11.0.61030
Microsoft Visual C++ 2012 Redistributable (x64) - 11.0.61030
Microsoft Visual C++ 2013 Redistributable (x86) - 12.0.21005
Microsoft Visual C++ 2015-2022 Redistributable (x86) - 14.42.34433
Microsoft Visual C++ 2015-2022 Redistributable (x64) - 14.44.35211
```

**이름이 반복돼 중복처럼 보이지만 버전별·아키텍처별로 다 필요하다.** 게임과 프로그램이 각각 특정 버전을 요구한다. 지우면 실행이 안 되고 "VCRUNTIME140.dll을 찾을 수 없습니다" 같은 오류가 난다.

### .NET Framework / .NET Runtime

같은 이유로 남긴다. 여러 버전이 공존하는 것이 정상이다.

### DirectX

게임에 필요하다.

---

## 남기는 것

| 프로그램 | 이유 |
|---|---|
| NVIDIA / AMD 그래픽 드라이버 | 필수 |
| NVIDIA HD 오디오 드라이버 | HDMI·DP 음성 출력 |
| Realtek Audio Driver | 내장 사운드 |
| 칩셋 드라이버 (AMD / Intel) | 필수 |
| Google Chrome, Microsoft Edge | 브라우저 |
| CrystalDiskInfo | 나중에 SSD 점검용으로 유용 |

---

## 판단이 갈리는 것

**NVIDIA App (구 GeForce Experience)** — 드라이버 업데이트와 게임 설정 관리용이다. 편하면 남기고 알림이 거슬리면 지운다. 드라이버 본체와는 별개라 지워도 그래픽은 정상 동작한다.

**OneDrive** — 사용자가 마이크로소프트 클라우드를 쓰지 않으면 지운다. 자동 동기화가 저장 공간을 차지하는 경우가 있다.

**한컴오피스 / Microsoft Office** — 라이선스가 정품인지 먼저 확인한다. 윈도우가 우회 인증이었으면 이것도 같은 경로일 확률이 높다.

정품 확인은 프로그램 안에서 한다. 한글은 `도움말 → 한컴오피스 정보` 또는 `등록 정보`에서 제품 종류(정품/체험판/기업용)와 등록된 조직명을 볼 수 있다. **모르는 회사명이 뜨면 기업용 볼륨 라이선스를 유출해 쓴 것이다.**

Office는 계정 구독 방식이라 판매자 계정이 빠지면 며칠 안에 읽기 전용으로 잠긴다.

**게임 클라이언트 (Steam, Epic, 배틀넷 등)** — 이전 소유자 계정으로 로그인돼 있으면 로그아웃하고, 다운로드된 게임 파일이 용량을 차지하면 정리한다.

---

## 발견되면 문제인 것

### 채굴 소프트웨어

NiceHash, PhoenixMiner, T-Rex Miner, lolMiner, Claymore, XMRig, TeamRedMiner, HiveOS 관련 도구

**발견되면 그래픽카드가 채굴에 쓰였다는 직접 증거다.** 이미 구매한 뒤라면 크리스탈디스크인포로 SSD 사용 시간을 확인해 실제 가동량을 추정하고, 그래픽카드 상태를 부하 테스트로 점검한다.

### 정품 인증 우회 도구

KMSpico, KMSAuto, Microsoft Toolkit, MAS(Microsoft Activation Scripts), HWIDGen, AAct

이름이 목록에 남아 있지 않은 경우가 많다. **윈도우 정품 인증 화면에 볼륨 라이선스 만료일이 뜨는 것이 더 확실한 증거다.**

이런 도구는 백신 예외 설정과 시스템 스케줄러를 심어두는 경우가 있다. **포맷이 가장 확실한 해결책**이고, 포맷하지 않으려면 최소한 작업 스케줄러와 윈도우 디펜더 예외 목록을 확인한다.

### 원격 제어 도구

TeamViewer, AnyDesk, ChromeRemoteDesktop 등이 설정된 상태로 남아 있으면 지운다. 이전 소유자가 접속할 수 있는 상태일 수 있다.

---

## 정리 순서

1. **제거 전에 목록을 캡처해둔다.** 뭔가 안 될 때 되돌릴 근거가 된다
2. 금융 보안 프로그램부터 제거 (개수가 많고 효과가 크다)
3. 제조사 유틸리티 제거
4. 게임 클라이언트와 계정 정리
5. **재부팅** — 잔여 서비스가 정리된다
6. 시작 프로그램 확인 — 작업 관리자 → 시작 프로그램 탭에서 불필요한 것을 사용 안 함으로

### 정리 후 체감

부팅 시간이 눈에 띄게 줄고 유휴 상태 자원 사용이 내려간다. 다만 **직후에는 오히려 무겁게 느껴질 수 있다.** 제거 과정에서 잔여 파일 정리와 레지스트리 갱신이 돌기 때문이다. 재부팅 후 판단한다.

### 포맷과 비교

프로그램이 열 개 넘게 정리 대상이면 **포맷이 더 빠르고 확실하다.** 특히 우회 인증 도구가 의심되면 포맷이 유일한 확실한 해결책이다.

포맷 후에는 칩셋 드라이버와 그래픽 드라이버 두 개만 깔면 된다. 나머지는 필요할 때 추가하면 훨씬 가벼운 상태를 유지할 수 있다.
