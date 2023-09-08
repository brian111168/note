# git 版本管理筆記
## git 區域分類
![local分區]( /Users/zhangchenwei/Desktop/note/pics/git分區.png)
1. workspace：寫程式的區域
2. staging area：準備push到本地資料庫的區域
3. local repository master：本地資料庫

## git 資料庫初始化
### 1.git init
建立資料庫分區，workspace、staging area、local repository master
### 2.git status
檢視在workspace、staging內檔案的狀態
## git tig
可以下載tig用以查看commit

## local commit

![local分區轉換指令](/Users/zhangchenwei/Desktop/分區轉換指令.png)
1. git add<檔案名稱> 新增該檔案至staging
2. git add . 將全部未新增的檔案新增至staging
3. git add - 逐項新增至staging

### 執行git commit後，輸入Issuse#1＋"註解內容"，表示第一次commit更改的內容


## local reset
![local分區轉換指令]( /Users/zhangchenwei/Desktop/stages.png)

### local repository -> workspace
git reset --mixed 'HEAD^'，這是預設，可以不用加 --mixed

### local repository -> staging area
git reset --soft 'HEAD^'

### 直接刪除該commit
git reset --hard 'HEAD^'通常不會用，檔案會直接不見

## git chechkout
用來回覆簡單的測試程式碼

## local to cloud 
### git push -u origin master
’-u‘ 第一次做push要加
![push]( /Users/zhangchenwei/Desktop/push.png)


## cloud to local
### git fetch
從Remote上下載hash下載站存在local
![fetch]( /Users/zhangchenwei/Desktop/fetch.png)


## git branch
### git branch develop
建立新的master開發環境
![branch]( /Users/zhangchenwei/Desktop/branch.png)
### git checkout -b
從develop切換回master
### git merge develop
在master環境下，將develop內容合併
### git merge develop --ff
直接將master移動至最新的develop
### git merge develop --no-ff
建立一個新的commit並將master轉移至該commit

### git rebase develop
以最新develop為基準，對commit進行更新

## merge pull
![merge]( /Users/zhangchenwei/Desktop/merge.png)




