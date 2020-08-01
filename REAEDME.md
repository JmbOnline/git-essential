# Git 버전 관리 에센셜 트레이닝

Git을 사용해 프로젝트 버전 관리하는 방법을 살펴봅니다. CLI 또는 GUI 환경에서 Git을 사용하는 방법을 비교해봅니다.

## Git 워크플로우

Git을 사용해 프로젝트 버전을 관리하는 흐름을 표현하면 다음과 같습니다.

```sh
           - add →        - commit →           - push →
+-------------+---------------+-------------------+-------------+
| Working dir | Index (Stage) | Local repo (HEAD) | Remote repo |
+-------------+---------------+-------------------+-------------+
         ← checkout -                         ← fetch -
```

## Git 버전 확인

`--version` 옵션 플래그를 사용하면 설치 된 `git` 버전이 출력됩니다.

```sh
$ git --version
```

## Git 초기화

프로젝트를 Git으로 관리하려면 초기화 과정이 필요합니다.

```sh
$ git init
```

## 관리 상태 확인

현재 관리 중인 상태를 확인하려면 `status` 명령을 사용합니다.

```sh
$ git status
```

## Index에 추가

워킹 디렉토리(Project Folder)에서 스테이징 에이리어로 인덱싱(Index) 하려면 `add` 명령을 사용합니다.

```sh
$ git add .
```

## 관리 예외 추가

버전 관리에서 제외할 예외를 추가하려면 `.gitignore` 파일을 만든 후 예외 항목을 추가합니다.

```sh
# Photoshop 파일 제외
*.psd

# Mac OS 시스템 파일 제외
.DS_Store
```

## HEAD에 커밋

인덱스(Index)에 추가 된 변경사항을 HEAD에 확정(기록) 하려면? `commit` 명령을 사용합니다.

```sh
$ git commit -m "확정(commit) 메시지 작성"
```

## 되돌리기

```sh
$ git reset
```

```sh
$ git reset --soft 7cc40cf
```

```sh
$ git reset --hard 7cc40cf
```