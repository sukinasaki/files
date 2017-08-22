# 本講義の目的
 - [スピリチュアルプログラミング紹介](http://blog.mirakui.com/entry/20100301/1267464280)
 - gitの概念の理解
 - gitハンズオン
 - gitを使ったチーム開発をするために...

## [gitとは](https://gyazo.com/c905923f32ca65fe9d1ae4324facd8df)
 - 配布資料をつかって説明(内容下記)
	- 随時質問受付ます
 1. git(使用時の注意)
 2. branch
 3. team開発
 4. どうしたら慣れて行くのか？

	>[まとめさいと](https://matome.naver.jp/odai/2136491451473222801)

	> [git入門スライドまとめ](https://mayonez.jp/topic/1452)

	> [GIT 教材](https://git-scm.com/book/ja/v2)

	> [git 教材](http://k.swd.cc/learnGitBranching-ja/)


## git HandsOn

~git clone http://github.com/fumihumi/git_course_repo.git~

git clone https://github.com/fumihumi/git_practice_repo.git

	//githubにsshkeyを登録している場合はっsshを使ってください
browserにてリポジトリの作成

```
#git config settings

git config --global user.name "<NAME>"
git config --global user.email "<EMAIL>"
 //gitのusername && email の設定

git config --global user.name  ->ちゃんと表示されていればおk
git config --global user.email ->ちゃんとひょうじされていればおk

```

git init #ローカルのgitリポジトリ作成

git remote add  "alias" URL (remote repo の登録)

~git remote add origin git@github.com:fumihumi/"repo_name"~

git remote -v

	vim git_course_test.txt #管理下にfile作成
	"edit"

	vim readme.md "what"s this repo? why make this?"
	vim .gitignore (oinfig git setting)
	vim ignored_file.txt (ignored file setting)
git status (states of this directory-tree )
	vim ignoredfile (change this file)

git add  git_course_test.txt (adding staging area)
git commit -m'test message' (commiting file && message)

git push (to pushiing remote repos)

1. [git とは](http://qiita.com/TKR/items/f27932612a2209a0746b)

	> https://gyazo.com/169fe427d8a1a49b06dafd69ac0f0a98

	> https://gyazo.com/7e39a83be46e09f1c249bcfedabf6ab8

	> https://gyazo.com/359c229a225ec09e829dfed6e1cfe916


2. gitのlocalrepo && remoterepo

	> https://gyazo.com/b481bc94317d24a0e1564ecdc6cf436f

3. workingTree , stagingArea(index),gitDirectory ,Stash,Local&Remote Repository

	> https://gyazo.com/f8f9568bfa450de91f0643500c20e1f7

	> https://gyazo.com/568792e84d71adf72df037bb4f5bddb6
	> https://gyazo.com/6eb83b12d212cf798920ac53ef710175
	>https://gyazo.com/14627a3541fba148f40ca0e89f89a3ba

	> https://gyazo.com/4b653d6eb9fcebb4b4dc8116225b4f24
	> https://gyazo.com/31e0bfc7e630c43baebd24516ef5a35b
	> https://gyazo.com/85fe1258ba79f505de82bbfa8a47374f
vim git_course_test.txt (cahges file)
```
git status
	#ここでの結果は編集したファイル
git diff (file_name)
	# git diff git_course_test.txt
	#ファイル内の編集内容を表示

git add ~~
git commit -m "commit message"
git push
```


基本的には上記のような
add -> commit -> push
が基本原則。


git branch make_indexPage (create new branch "make_indexPage")
git checkout make_indexPage(chenge local branch "master TO make_indexPage")

4. branchの考え方

	> https://gyazo.com/738bdacdc841d663730142f63b54091b

	> https://gyazo.com/b5d2b485b2158b70298e9de2c6e7d4b7

	>https://gyazo.com/60fb4ed35d1cd7cf58ac09a57c9122ea
	>https://gyazo.com/d7b87617b456a20075c8237ff59c2d05
	>https://gyazo.com/39276da850758f04fd0d1ffe8b882fcc
s
5. conflict

```
git checkout -b test_conflict(create && checkout branch)
echo hey > hello.txt (edit this file)
git add hello.txt (staging )
git commit -m "commit on test_conflict branch" (commit )
git checkout master(checkout master)
echo hi!!!!!!!! > hello.txt (edit file)
git commit -am"commit on master branch"
git marge test_conflict
vim hello.txt
git add hello.txt
git commit -m "fix conflict"
```

その時他のコマンドを知っているともっとgitが便利に使えます。
```
git log
git status
git stash
git reset
git rm
git revert
git rebase
git show
git branch
git checkout
git log --oneline --decorate --graph
```

[GIT CHEAT SHEET](https://services.github.com/on-demand/downloads/github-git-cheat-sheet.pdf)

gitはまだまだ奥が深いです。実際に触って苦しんでいるときに成長します

Let's gït lífè

### readmeにおける画像出展

[TKRさんのQiita記事](http://qiita.com/TKR/items/f27932612a2209a0746b)

[あさちゅんのブログ](http://kray.jp/blog/git-why-explanation/)

[A successful Git branching model](http://nvie.com/posts/a-successful-git-branching-model/)

[A successful Git branching model（翻訳版）](http://keijinsonyaban.blogspot.jp/2010/10/a-successful-git-branching-model.html)

[こっそり始めるGit／GitHub超入門（終）](http://www.atmarkit.co.jp/ait/articles/1708/01/news015.html)

[はじめようgit](https://www.slideshare.net/techscore/git-27770654)

[いつやるの？git](https://www.slideshare.net/matsukaz/git-28304397)
