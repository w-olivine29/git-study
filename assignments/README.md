# GitHub PR 실습

### 과제 내용

GitHub를 사용하여 브랜치(branch)를 생성하고, 변경 사항을 커밋한 후, 풀 리퀘스트(Pull Request, PR)를 통해 메인 브랜치에 병합하는 워크플로우를 실습합니다.

GitHub에서 PR을 진행하며 각 단계별로 스크린샷을 촬영하고, 해당 스크린샷 이미지들을  제출합니다.

---

### 과정

1. 새로운 브랜치 생성 및 전환:
   git checkout -b feature/add-file

2. feature/add-file 브랜치에서 info.txt 파일 생성, 내용 입력(예: "This is my first PR!").

   git add info.txt

   git commit -m "Add info.txt in feature branch"

   git push origin feature/add-file

3. GitHub 웹사이트에서 풀 리퀘스트 생성:

   저장소 페이지로 이동, feature/add-file → main으로 PR 생성.

   PR 제목: "Add info.txt to project"

   PR 설명: "Added info.txt with a simple message."

4. PR을 검토 후 main 브랜치에 병합(merge)하고, feature/add-file 브랜치 삭제(웹 UI에서 가능).

5. 로컬에서 main 브랜치로 전환(git checkout main)하고, git pull로 최신 변경 사항 동기화.
