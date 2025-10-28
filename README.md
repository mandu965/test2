# Git 개념 정리

## 1. Git이란?

* **분산 버전 관리 시스템 (DVCS, Distributed Version Control System)**
* 코드나 문서의 **변경 이력(History)** 을 추적하고, 여러 명이 동시에 협업 가능하게 하는 도구
* 대표적 호스팅 서비스: GitHub, GitLab, Bitbucket

---

## 2. 주요 개념

| 용어                   | 설명                                                |
| -------------------- | ------------------------------------------------- |
| **Repository (저장소)** | 프로젝트의 모든 파일과 변경 이력을 저장하는 공간                       |
| **Local Repo**       | 내 컴퓨터에 있는 저장소                                     |
| **Remote Repo**      | 서버(GitHub 등)에 있는 저장소                              |
| **Commit**           | 변경 내용을 하나의 버전으로 저장                                |
| **Branch**           | 독립된 개발 라인. main(또는 master) 외에 새로운 기능을 분리 개발할 때 사용 |
| **Merge**            | 브랜치를 합치는 작업                                       |
| **Clone**            | 원격 저장소를 로컬로 복제                                    |
| **Pull**             | 원격 저장소의 최신 내용을 가져오기                               |
| **Push**             | 로컬의 커밋을 원격 저장소로 업로드                               |

---

## 3. 기본 명령어

| 명령어                   | 설명                 | ex)                                          |
| --------------------- | ------------------ | -------------------------------------------- |
| `git init`            | 새 Git 저장소 생성       | `git init`                                   |
| `git clone [URL]`     | 원격 저장소 복제          | `git clone https://github.com/user/repo.git` |
| `git status`          | 현재 변경 상태 확인        | `git status`                                 |
| `git add [파일명]`       | 변경 파일을 스테이징        | `git add main.py`                            |
| `git commit -m "메시지"` | 변경 내용 저장           | `git commit -m "fix: login bug"`             |
| `git log`             | 커밋 기록 보기           | `git log --oneline`                          |
| `git branch`          | 브랜치 목록 보기          | `git branch`                                 |
| `git checkout [브랜치명]` | 브랜치 이동             | `git checkout dev`                           |
| `git merge [브랜치명]`    | 브랜치 병합             | `git merge feature`                          |
| `git pull`            | 원격 저장소에서 최신 내용 받기  | `git pull origin main`                       |
| `git push`            | 로컬 커밋을 원격 저장소로 업로드 | `git push origin main`                       |

---

## 4. Git 작업 흐름

1. `git clone` 또는 `git init` 으로 저장소 준비
2. 코드 수정
3. `git add` → 변경사항 스테이징
4. `git commit` → 버전 기록
5. `git push` → 원격 저장소에 반영
6. 협업자는 `git pull` 로 최신 코드 반영

---

## 5. 협업 시 주의점

* **브랜치 전략**

  * `main`: 항상 배포 가능한 안정 버전
  * `develop`: 개발 통합 브랜치
  * `feature/*`: 기능별 작업용 브랜치
  * `hotfix/*`: 긴급 수정용 브랜치
* 커밋 메시지 컨벤션 (ex: Angular style)

  * `feat:` 새로운 기능
  * `fix:` 버그 수정
  * `docs:` 문서 수정
  * `refactor:` 리팩토링
  * `test:` 테스트 코드

---

## 6. Git과 GitHub 차이

| 항목 | Git | GitHub |
|--|--|
| 역할 | 버전 관리 도구 | 원격 저장소 서비스 |
| 설치 위치 | 로컬(내 컴퓨터) | 클라우드 서버 |
| 연결 방식 | `git remote add origin [URL]` | GitHub 계정 / repo 사용 |

---

원하면 `Git 기본 실습 예제`나 `브랜치 전략 예시(flow chart)`도 만들어줄 수 있음.
필요해?
