# 설치용 패키지

`skills/` 아래 소스를 그대로 묶은 설치 파일이다. `.skill`은 폴더 구조를 담은 zip이며, Claude에 첨부하면 저장 버튼이 뜬다.

| 파일 | 내용 |
|---|---|
| `used-pc-listing-check.skill` | SKILL.md + 등급표·사진판독·질문템플릿 3개 |
| `pc-buying-brief.skill` | SKILL.md + 판단틀·브리프템플릿 |
| `used-pc-handover.skill` | SKILL.md + 프로그램 정리목록 |

## 설치

**Claude에 스킬로 저장** — `.skill` 파일을 대화에 첨부하면 **Save skill** 버튼이 나타난다. 저장하면 이후 모든 대화에서 자동으로 발동한다. 매물 스펙이나 스크린샷만 올려도 판독이 시작된다.

버튼이 안 보이면 조직 설정에서 스킬 생성이 비활성화된 경우다. 아래 방법을 쓴다.

**프로젝트 지식에 넣기** — 프로젝트를 만들고 `SKILL.md`와 `references/` 파일들을 프로젝트 지식에 업로드한다. 그 프로젝트 안의 모든 대화가 규칙을 알고 시작하며, 검토 이력도 같은 곳에 쌓인다. 반복적으로 매물을 볼 거면 이쪽이 더 편하다.

**링크로 불러오기** — 새 대화에서 raw URL을 주고 읽으라고 한다.

```
https://raw.githubusercontent.com/gyuber/computer/main/skills/used-pc-listing-check/SKILL.md
```

## 다시 묶는 방법

소스를 수정한 뒤 패키지를 갱신하려면 skill-creator의 스크립트를 쓴다.

```bash
python -m scripts.package_skill <경로>/skills/used-pc-listing-check
```

읽기 전용 위치에서는 실패하므로 쓰기 가능한 디렉터리에 복사해서 실행한다.

## 갱신이 필요한 시점

`part-tiers.md`의 앵커 시세는 **2026년 9월** 기준이다. 램·SSD 대란이 진행 중인 시기라서 전략 자체가 그 상황을 전제로 한다.

값이 정상화되면 다음 전제들을 다시 봐야 한다.

- "중고가 신품보다 유리하다" — 대란 전 가격 부품이 박혀 있다는 전제
- "램은 슬롯 비워두고 시작하라" — 지금 사면 손해라는 전제
- "DDR5 플랫폼은 예산 밖" — DDR5 32GB가 70만원이라는 전제

스킬은 시세를 검색으로 조회하도록 설계했지만, 위 전략 문장들은 본문에 있으므로 수동 갱신이 필요하다.
