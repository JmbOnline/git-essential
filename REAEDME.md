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

## 기록 된 히스토리

버전 관리 중인 히스토리를 확인하려면 `log` 명령을 사용합니다.

```sh
$ git log
```

그래프 또는 한 줄로 히스토리를 표시하려면 `--graph`, `--oneline` 옵션 플래그를 추가합니다.

```sh
$ git log --graph --oneline
```

## 스테이징 취소

인덱스에 추가 된 변경사항을 언 스테이지(Working Directory)로 되돌리려면 `reset` 명령을 사용합니다.

```sh
$ git reset
```

특정 파일만 스테이징 취소하려면 [[파일_이름]]을 명시적으로 작성합니다.

```sh
$ git reset <파일_이름>
```

## 마지막 커밋 취소

최종 커밋 된 내용을 취소하려면 `reset --soft HEAD^` 명령을 사용합니다.

```sh
$ git reset --soft HEAD^
```

## 특정 커밋 위치로 되돌리기

기록 된 커밋의 특정 위치(커밋 해시) 값을 입력해 되돌릴 수 있습니다.

```sh
$ git reset --hard 7cc40cf
```

