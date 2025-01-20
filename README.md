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


# 스캠 3일차

## ChatGPT 주요 개념

### Transformer

- 문장 속의 단어 간 관계를 추적해 맥락과 의미를 학습
- 인간처럼 일관되고 연관성이 높은 언어를 구사하여 대화형 작업에 강점

### 트랜스포머

문장의 맥락을 효과적으로 이해하고 처리 → Attention 메커니즘

## Transformer 주요 개념

- self-Attention 메커니즘
- 병렬처리 가능
- 스케일링 가능

GPT 모델은 특히 Transformer의 디코더 부분만을 사용

## Interface

서로 다른 두개의 시스템이 정보를 교환할 때, 그 사이에 존재하는 접점

→ 사용자가 기기를 쉽게 동작 시키거나, 기계와 기계가 통신할 때 필요한 ‘약속된 방식’

### UI

사람이 소프트웨어에 접근하는 그래픽적, 화면적 요소

### 눈에 보이지 않는 영역의 통신

- 실제로는 기계와 기계, 시스템과 시스템 사이에서도 수많은 ‘인터페이스’를 통해 정보를 주고받고 있음
- 여기서는 화면(UI)이 없을 뿐, 약속된 방식으로 데이터를 주고 받음

### 클라이언트

서비스를 요청하는 쪽

→ 예) 사용자의 웹 브라우저, 모바일 앱

### 서버

요청을 받아서 처리하고, 결과를 응답해주는 쪽

→ 예) 웹 서버, 데이터베이스 서버

### API(Application Programming Interface)

두 소프트웨어(또는 시스템)가 서로 통신할 수 있게 하는 메커니즘

→ ‘약속된 방식의 인터페이스’로, 특정 규칙에 따라  데이터를 요청하고 응답하는 규칙을 제공

### Application

특정 기능을 수행하는 모든 소프트웨어

→ 웹, 모바일, 데스크톱 앱 등, 우리가 만든 서비스나 프로그램도 모두 앱의 일종

### API Key

API에게 요청을 보내는 애플리케이션을 구별하기 위한 고유한 식별 문자열

### API Key 사용 시 주의사항

- 공개된 곳에 노출하지 말 것
- 키가 유출될 경우 무단 사용 위함 → 정기 갱신 필요
- 서버-클라이언트 구조에서 키를 안전하게 저장하는 방법들 고려

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/33d937a3-18ca-42b8-87dd-c3acc0d91519/6a2660a6-ce02-4d51-b38c-b4f5240e3842/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/33d937a3-18ca-42b8-87dd-c3acc0d91519/25c555e4-2544-4a54-996d-0207babf9d01/image.png)

### 필수 파라미터

- model
- messages

### 응답 다양성 제어

- temperature
- top_p
  
---

# Python 수업 1일차 요약
**SW 개발자 특강 핵심**

- 지속적으로 프로젝트를 만들고 실제 적용하는 것이 중요함
- 프론트/백엔드 구분이 흐려지며, 전체를 조율하는 능력이 중요해질 것

**Python 기초**

- Python은 쉽고 간결한 문법으로 다양한 분야에서 활용 가능한 언어
- 프로그래밍의 핵심은 문제 해결을 위한 연산 정의와 조합

**데이터 타입과 변수**

- 변수는 값을 참조하기 위한 이름이며, 메모리 주소를 가짐
- 데이터 타입은 값의 종류와 가능한 연산을 결정하는 중요한 속성

**문자열과 코딩 스타일**

- 문자열은 변경 불가능한 시퀀스 타입으로, f-string을 통해 효과적으로 문자열 보간 가능
- 일관성 있는 코드를 위해 스타일 가이드를 준수하고 적절한 주석 사용 필요

원문: https://www.notion.so/Python-1-25-01-20-180bc9547a7d803791addf6791c6e9cb