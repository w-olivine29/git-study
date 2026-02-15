# Git 충돌해결 실습

### 과제 내용

두 브랜치에서 동일한 파일을 수정하여 충돌을 유발한 후, 로컬에서 git merge로 충돌을 해결합니다

충돌이 발생한 상황에서 다음 3개 상황의 캡쳐를 제출합니다.

- 스크린샷 1: 충돌 상황 (goals.txt의 충돌 마커 표시).
- 스크린샷 2: 충돌 해결 후 goals.txt 최종 내용.

스크린샷 3: GitHub 커밋 히스토리 (충돌 해결 커밋 포함, feature/goal-update 브랜치).\*\*

---

### 과정

1. GitHub에서 비공개 저장소 conflict-resolution 생성.

2. 로컬에서 저장소 복제:
   - git clone <GitHub 저장소 URL>

3. 메인 브랜치(main)에 goals.txt 파일 생성, 내용 입력:
   - 내용: Goal: Master Git basics
   - git add goals.txt
   - git commit -m "Add goals.txt"
   - git push origin main

4. 브랜치 feature/goal-update 생성:
   - git checkout -b feature/goal-update
   - goals.txt 수정: Goal: Master Git branching
   - git add goals.txt
   - git commit -m "Update goal to branching"
   - git push origin feature/goal-update

5. 메인 브랜치로 전환:
   - git checkout main
   - goals.txt 수정: Goal: Master Git merging
   - git add goals.txt
   - git commit -m "Update goal to merging"
   - git push origin main

6. 충돌 유발 및 해결:
   - feature/goal-update 브랜치로 전환: git checkout feature/goal-update
   - git merge main 실행 → 충돌 발생.
   - 스크린샷 1: 충돌 상황 캡처 (텍스트 편집기에서 goals.txt의 충돌 마커(<<<<<<<, =======, >>>>>>>) 표시).
   - goals.txt 편집하여 충돌 해결: Goal: Master Git branching and merging
   - git add goals.txt
   - git commit -m "Resolve merge conflict"
   - 스크린샷 2: 충돌 해결 후 goals.txt 내용 캡처 (최종 텍스트 확인).
   - git push origin feature/goal-update
