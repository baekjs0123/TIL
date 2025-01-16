### Staging Area

중간준비 영역

### Repository

버전 이력과 파일들이 영구적으로 저장되는 영역

버전 = commit 

### Commit

변경된 내용들을 저장하는 행위, snapshot이라고도 한다.

### git init

로컬 저장소 설정 초기화

git 저장소로 쓰겠다는 뜻

→  git 버전관리를 시작할 디렉토리에서 진행

### git add

변경사항이 있는 파일을 staging area에 추가

### git commit

staging area에 있는 파일들을 저장소에 기록

→ 해당 시점의 버전을 생성하고 변경 이력을 남기는 것

git은 로컬 저장소 내 모든 파일의 변경사항을 감시하고 있다.

git commit -m “” : 커밋 메세지 입력하는 법

### git status

현재 로컬 저장소의 파일 상태 보기

### git log

commit history 보기

### git log —oneline

commit 목록 한 줄로 보기

### git config — global -l

git global 설정 정보 보기

# git 로컬 저장소 안에는 또 다른 git 로컬 저장소를 만들지 않는다.

### git commit 수정하기

git commit —amend

1. Commit 메시지 수정
2. Commit 전체 수정

# 2일차 수업 시작

### 원격 저장소

코드와 버전 관리 이력을 온라인 상의 특정 위치에 저장하여 여러 개발자가 협업하고 코드를 공유할 수 있는 저장 공간

git remote add origin remote_repo_url

origin = 저장소 이름

remote_repo_url = 원격 저장소 위치

clone은 맨처음 한번 가져올 때 쓴다.

그 이후 변경사항은 pull을 쓴다.

git clone remote_repo_url

원격 저장소 전체를 복제(다운로드)

### gitignore

Git에서 특정 파일이나 디렉토리를 추적하지 않도록 설정하는데 사용되는 텍스트파일

### gitignore 주의사항

이미 git 의 관리를 받은 이력이 있는 파일이나 디렉토리는 나중에 gitignore 에 작성해도 적용되지 않음

(git rm —cached 명령어를 통해 git 캐시에서 삭제 필요)

### Git revert

특정 commit을 없었던 일로 만드는 작업

git revert <commit id>

- 변경사항을 안전하게 실행 취소 할 수 있도록 도와주는 순방향 실행 취소 작업

### Git reset

특정 commit으로 되돌아가는 작업

git reset[옵션] <commit id>

- 되돌리기
- 시계를 과거로 돌리는 듯한 행위
- 특정 commit으로 되돌아 갔을 때, 되돌아간 commit 이후의 commit은 모두 삭제

### git restore

Modified 상태의 파일 되돌리기