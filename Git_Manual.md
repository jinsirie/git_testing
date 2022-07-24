

++

## 1.기본 git 사용

1. git bash가 설치되어있다고 가정

2. 사전작업

```shell
git config --global user.name "jinsirie"
git config --global user.email "123456678@Gmail.com"
```

3. GitHub에 있는 저장소 가져오기 (Clone) -- SSH 적용 시 ssh-keygen 확인해야함

```shell
git clone https://github.com/jinsirie/git_testing.git
```

4. Commit 한 후

```shell
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)
```





## 2. Branch 사용 / Push 방법

1. Branch 만들기

```shell
git branch devel
```

2. Devel Branch에만 올리기

```shell
git push origin devel
```

3. devel에만 push 하니 Open a pull request 가 뜬다 우왕



![image-20220723215216636](C:\Users\User\AppData\Roaming\Typora\typora-user-images\image-20220723215216636.png)







- Staged 상태의 파일을 수정하여 다시 status 확인할 경우 modifed 와 to be committed 상태 동시 파일이 볼 수 있다.

![image-20220724192828442](C:\Users\User\AppData\Roaming\Typora\typora-user-images\image-20220724192828442.png)





## 3. 궁금한 점

Q1./Repository /하위 폴더/만 당겨올 수 있을까?

Q2. merge ,pull, push,checkout,switch,commit, branch 응용 문구들 정리하기 (-d , -m,)

pull 한 후---> push 하기

checkout : 브랜치 in

switch : 브랜치 Change



Q3. 오류메세지 확인

```c
$ git add  git_add_devel
warning: LF will be replaced by CRLF in git_add_devel.
The file will have its original line endings in your working directory
```

> OS의  Character set 오류로 확인



Q4. 오류메세지 확인

```shell
$ git push origin
fatal: The current branch master has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin master

```

> Pull 하지 않아서 생기는 문제

#Reference

https://git-scm.com/book/ko/v2



#Ref1

https://subicura.com/git/guide/github-flow.html#github-flow-%E1%84%87%E1%85%A1%E1%86%BC%E1%84%89%E1%85%B5%E1%86%A8