# 1. 로컬 환경 구축

- origin : 메인 repository
  - https://github.com/KoreanNationalElection/KoreaGeneralElection.git
- local : repository를 로컬로 clone

### 1) dev 브랜치 생성
- remote : web gui에서 생성 후 default branch로 지정

### 2) repository를 로컬로 clone
```console
$ git clone https://github.com/KoreanNationalElection/KoreaGeneralElection.git
```
아래의 명령어를 합한 것이다
```console
$ git init
$ git remote add origin https://github.com/KoreanNationalElection/KoreaGeneralElection.git
$ git fetch origin master
```

<br>

# 2. 기본 루틴

### 1) 새로운 기능 개발을 위해 branch 생성
```console
$ git checkout -b <branch-name> dev # dev 브랜치에서 생성
```
아래의 명령어를 합한 것이다
```console
$ git branch <branch-name> dev
$ git checkout <branch-name>
```

### 2) 파일 수정
기능 개발을 위해 파일을 수정한다

### 2) 새로운 기능 브랜치를 커밋 후 원격 저장소에 push
```console
$ git commit -a -m "Commit Message" # 스테이징 + 커밋 동시에
$ git push -u origin <branch-name>
```

### 3) Pull Request 요청
기능 브랜치 -> dev 브랜치로의 merge를 요청한다

### 4) 원격 저장소와 로컬 저장소를 동기화
```console
$ git checkout dev # 현재 dev 브랜치가 아니라면 dev로 이동
$ git pull origin dev # 원격의 dev 브랜치에서 받아옴
```

### 5) 이전 브랜치 삭제
기능 추가 작업을 완료했다면 로컬에서 이전 작업 브랜치는 삭제한다
```console
$ git branch -d <branch-name>
$ git push --delete origin <branch-name> # 원격 브랜치 삭제
```

<br>

# 4. 참고
- https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow
- https://gmlwjd9405.github.io/2017/10/27/how-to-collaborate-on-GitHub-1.html
- https://gmlwjd9405.github.io/2018/05/12/how-to-collaborate-on-GitHub-3.html