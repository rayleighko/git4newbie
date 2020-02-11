# Git Basic 실습

## GitHub

실습 전에 GitHub의 계정을 만들어 실습을 위한 원격 레포지토리를 만들어야 합니다.

GitHub을 통해 원격 레포지토리를 만들었다면, 다음 실습을 진행합니다.

## Init Or Clone

원격 저장소의 내용을 내려 받고 싶다면, 두 가지 명령을 사용할 수 있습니다. 최초로 프로젝트를 시작해야 하는 상황이라면 git init을, 기존의 프로젝트를 내려 받아야 한다면 git clone을 사용하면 됩니다.

```sh
// git init

$ cd testProject
$ git init
$ git remote add origin <your-remote-repository-url>
```

```sh
// git clone

$ git clone <your-remote-repository-url>
```

## Add

- text.txt를 만들어 Working Directory의 내용을 Index(Staging Area)로 옮겨봅시다.

```sh
$ touch text.txt
// git add <file-path>

$ git add text.txt
```

## Commit

- Index(Staging Area)에 있는 text.txt를 이용해 하나의 커밋을 만들어 Local Repository에 기록합시다.

```sh
// choose only one way

// for open editor
$ git commit -e 

// for minimal commit
$ git commit -m "commit title"
```


## Push

- Local Repository에 기록된 커밋을 Remote Repository로 옮겨 버전을 변경해봅시다.

```sh
// origin is remote repository address
// if not found origin, you do 'git remote add origin <your-repository-address>'
$ git push origin master
```

## Pull

- 직접 gitHub에서 프로젝트를 직접 수정해보거나 기존의 프로젝트에서 수정된 다른 사람의 코드를 받아봅시다.

```sh
// origin is remote repository address
// if not found origin, you do 'git remote add origin <your-repository-address>'

editing...
$ git pull origin master
```
