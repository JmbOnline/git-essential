[← 뒤로](./README.md)

# <img src="./assets/icon-git-1.png" alt style="width: 30px; vertical-align: -5px"> Git 버전 관리 에센셜 PART 03

Git을 사용해 프로젝트 버전 관리하는 방법을 살펴봅니다. [[CLI]]와 [[GUI]] 환경에서 Git을 사용하는 방법을 비교해봅니다.

<a href="https://bit.ly/GIT_ESSENTIAL" target="_blank"><img src="./assets/00-COVER.jpg" alt /></a>

<br>

<!-- ----------------------------------------------------------------------- -->

## <img src="./assets/icon-git-2.png" alt style="width: 20px; vertical-align: -1px"> 브랜치 생성 및 조회하기

기존 코드와 분리해서 독립적으로 개발을 진행할 수 있도록 Git에서는 브랜치 라는 개념을 제공합니다. `master` 역시 브랜치이며 코드를 별도로 개발할 수 있는 영역인 새로운 브랜치를 생성할 수 있습니다.  브랜치의 생성 및 조회는 `branch` 명령을 사용할 수 있습니다.   

#### CLI 명령어 환경 —

`branch` 명령 또는 `switch -c` 명령을 사용해 독립된 브랜치를 생성할 수 있습니다. 이때 `switch -c` 명령은 Git 2.23 버전 이후부터 사용이 가능합니다.  

```sh
$ git branch <브랜치명> 
$ git switch -c <브랜치명>
```

`branch` 명령을 사용해 현재 Git이 관리하는 프로젝트 내 브랜치를 조회할 수 있습니다. 
```sh
$ git branch
```

#### GUI 그래픽 환경 —

...

![](assets/파일명.png)

<br>

<!-- ----------------------------------------------------------------------- -->

## <img src="./assets/icon-git-2.png" alt style="width: 20px; vertical-align: -1px"> 브랜치로 이동하기

브랜치로 이동하기 위해서는 Git 2.23 버전 이전은 `checkout` 명령을 Git 2.23 버전은 `checkout` 또는 `switch` 명령을 사용할 수 있습니다. 

#### CLI 명령어 환경 —

브랜치로 이동하기 위해서는 `checkout` 또는 `switch` 명령을 사용할 수 있습니다.

```sh
$ git checkout <브랜치명>
$ git switch <브랜치명>
```

#### GUI 그래픽 환경 —

...

![](assets/파일명.png)

<br>
<!-- ----------------------------------------------------------------------- -->

## <img src="./assets/icon-git-2.png" alt style="width: 20px; vertical-align: -1px"> 브랜치 병합하기

브랜치 병합은 `merge` 명령어로 실행합니다. 예를 들어 버그 해결을 위해 별도로 `bugfix` 브랜치를 생성하고 개발을 완료한 경우 이를 `master` 브랜치에 병합하고자 할 경우 우선 `master` 브랜치로 이동 후 `bugfix` 브랜치를 병합하면 됩니다.  

#### CLI 명령어 환경 —

`merge` 명령을 사용해 특정 브랜치를 다른 브랜치에 병합할 수 있습니다. 

```sh
$ git merge <브랜치명>
```

#### GUI 그래픽 환경 —

...

![](assets/파일명.png)

<br>
<!-- ----------------------------------------------------------------------- -->

## <img src="./assets/icon-git-2.png" alt style="width: 20px; vertical-align: -1px"> 브랜치 삭제하기

독립된 브랜치에 개발한 코드를 `master` 브랜치에 병합한 후 기존 브랜치를 제거하고자 할 경우 `branch -d` 또는 `branch --delete` 명령을 사용합니다. 그러나 작업 내용이 남아있는 경우에는 브랜치를 삭제할 수 없을 것입니다. 이때는 브랜치를 강제로 삭제하여야 하며 브랜치를 강제로 삭제하기 위해서는 `branch -D` 명령을 사용해야 합니다. 

#### CLI 명령어 환경 —

`branch -d`, `branch --delete`, `branch -D` 명령을 사용해 특정 브랜치를 삭제할 수 있습니다. 

```sh
$ git branch -d <브랜치명>
$ git branch --delete <브랜치명>
$ git branch -D <브랜치명>
```

#### GUI 그래픽 환경 —

...

![](assets/파일명.png)

<br>
<!-- ----------------------------------------------------------------------- -->
