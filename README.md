![rand.ac](/static/github.png)

# rand.ac

![GitHub Workflow Status (with branch)](https://img.shields.io/github/actions/workflow/status/HyeokjinKang/rand.ac/build.yml?branch=main)
![GitHub Workflow Status (with branch)](https://img.shields.io/github/actions/workflow/status/HyeokjinKang/rand.ac/build.yml?branch=develop&label=dev)
![GitHub license](https://img.shields.io/github/license/HyeokjinKang/rand.ac)
![GitHub issues](https://img.shields.io/github/issues/HyeokjinKang/rand.ac?color=yellow)

> [rand.ac](https://rand.ac), problem solving is now a game.

This repository is currently operated in Korean. For English documents, please wait.

rand.ac는 [Baekjoon Online Judge](https://www.acmicpc.net/)의 문제를 **온라인 게임 형식**으로 풀 수 있는 사이트입니다.  
구데기컵 카페의 미니게임과 랜덤 디펜스 브라우저 익스텐션에서 영감을 받아 제작되었습니다.  
**로컬 플레이**와 **온라인 플레이**를 지원할 예정입니다.

## 로컬 플레이

로컬 플레이의 모든 모드는 별개의 랭킹으로 기록되며, 로컬 플레이에서도 랭킹을 통한 경쟁이 가능합니다.

- 랜덤 디펜스
  - 랜덤으로 주어지는 문제를 원하는 만큼 풀 수 있는 모드입니다.
  - 사용자가 원하는 난이도와 시간제한을 설정할 수 있습니다.
- 무한 디펜스
  - 정해진 시간동안 최대한 많은 문제를 풀어야하는 모드입니다.
  - 문제를 풀 때마다 시간이 추가되며, 시간이 끝나면 게임이 종료됩니다.
- 타임 어택
  - 랜덤으로 주어지는 문제를 최대한 빨리 풀어야하는 모드입니다.
  - 난이도별로 기본 제한시간이 주어지며, 제한시간 내에 문제를 풀지 못하면 게임이 종료됩니다.

## 온라인 플레이

온라인 플레이도 로컬 플레이와 마찬가지로 별개의 랭킹으로 기록되며, 랭킹을 통한 경쟁이 가능합니다.  
온라인 매칭은 **자동매칭** 방식을 이용합니다.

- 무한 디펜스
  - 매칭된 상대와 동일한 문제를 풀며, 정해진 시간동안 더 많은 문제를 푼 사람이 승리합니다.
  - 로컬 플레이와 달리 문제를 풀 때마다 시간이 추가되지 않습니다.
- 타임 어택
  - 매칭된 상대와 동일한 문제를 풀며, 문제를 더 빨리 푼 사람이 승리합니다.
  - 난이도별로 기본 제한시간이 주어지며, 게임 참여자가 모두 문제를 풀지 못하면 무승부로 판정합니다.

## 개발

### 설치

이 저장소를 `clone`한 후, 다음 명령어를 실행합니다.

```bash
foo@bar:~$ npm install
```

### 실행

개발모드로 실행하려면 다음 명령어를 실행합니다.

```bash
foo@bar:~$ npm run dev
```

프리뷰모드로 실행하려면 다음 명령어를 실행합니다.

```bash
foo@bar:~$ npm run preview
```

### 빌드

다음 명령어를 실행하면 `build` 폴더에 빌드 결과물이 생성됩니다.

```bash
foo@bar:~$ npm run build
```

## 참고사항

### branch 관리

본 프로젝트는 `gitflow`전략을 약간 수정하여 사용합니다.

- 모든 기능은 각각의 `branch`에서 개발되며, 기능 개발이 완료되면 `develop` 브랜치에 `merge`됩니다.
- `develop` 브랜치에서, 모든 기능은 충분한 테스트를 거쳐야합니다.
- `develop` 브랜치에서 충분한 테스트를 거친 기능은 `main` 브랜치에 `merge`되면 배포됩니다.
- 핫픽스가 필요한 경우 `hotfix` 브랜치를 사용합니다. 마찬가지로, `hotfix` 브랜치에서 개발된 기능은 `main` 브랜치에 `merge`되면 배포됩니다.

### 커밋 메시지

모든 커밋 메시지는 다음과 같은 형식으로 작성합니다.

```
Add: Add new feature
Fix: Fix bug
Update: Update feature
Remove: Remove feature
```
