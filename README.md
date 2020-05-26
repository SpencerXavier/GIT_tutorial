# GIT_tutorial and Markdown syntax
## Markdown syntax
### Title
```
- # H1
- ## H2
- ### H3
- #### H4
- ##### H5
- ###### H6
```

### 強調語法
```
*asterisks*  //斜體
**asterisks** //粗體
```


### 清單
```
* 无序列表一  //可以使用星號建立無序清單
- 无序列表二  //或是短橫線（負號）
+ 无序列表三  //使用半形加號也可以
1. 有序列表一
2. 有序列表二
3. 有序列表三

```

### 連結設定
```
[行內連結名稱](https://www.google.com)
[帶有標題的行內連結名稱](https://www.google.com "Google's Homepage")
//滑鼠放在連結上會顯示 Google's Homepage
[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[這段文字連到參考項目]: http://www.reddit.com

```
### 圖片
```
行內格式：
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo 標題文字範例一")
參考連結格式：
![alt text][logo]
[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo 標題文字範例二"
```

### 程式代碼與語法高亮標示
```
整段獨立呈現的代碼必須使用成對的三個 back-ticks ``` 包裹起來，或是使用四個空格縮排。建議使用第一種方法，因為那能讓代碼顯著標示。
```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
```python
s = "Python syntax highlighting"
print s
```
```
No language indicated, so no syntax highlighting.
But let's throw in a <b>tag</b>.

```
### 表格
```
| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |
最外圍的豎線（|）不是絕對需要，在原始文檔中你可以不要太在意美觀，實際轉成網頁或電子書時會呈現得很好。你也可以在表格內使用行內格式。
Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3

```

### 引言
```
> 引言（Blockquotes）常常出現在電子郵件中，表示摘錄來信原句並回覆。
> 這一行是引言的一部分。
Quote break.
> 這是一段非常長的引言區塊，只要在句首使用了正確的符號與空格，你可以持續不間斷的撰寫，整段文字都還是會被包含在引言區塊中。當然你依舊可以在引言區塊中 *使用* **Markdown** 的行內格式標記語法。
```


### 行內 HTML
```
<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>
  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>
```

### 水平分隔線
```
---
短橫線（Hyphens）
***
半形星號（Asterisks）
___
下底線（Underscores）
```


### 空行分隔段落
```
習慣或熟悉 Markdown 如何進行分段是很重要的，基本上空行代表前後的文字都會是段落
```


### 代辦事項
```
- [ ] 代辦事項
- [x] 已完成事項
```


### 列表縮進
```
文章
: 轻轻的我走了， 正如我轻轻的来； 我轻轻的招手， 作别西天的云彩。
  那河畔的金柳， 是夕阳中的新娘； 波光里的艳影， 在我的心头荡漾。
  软泥上的青荇， 油油的在水底招摇； 在康河的柔波里， 我甘心做一条水草！
```

### 跳脫字元
```
加上反引號 (\)，用來跳過特殊字元的特殊功能

```


## Git
### procedure
```
a. git clone < url > -  clone the project 
b. git add . or git add file  - add to staging area:
c. git status - check status (optional)
d. git commit -a -m  - a stands for add , m stands for message, commit to repository
e. git log - check  commit record (optional)
f. git push - push 意即將本機端的檔案推向 server端
g. pull request - 點擊 Compare & pull request+  按下 Create pull reques +  按下 Merge pull request
h.git pull -p - 同步遠端後，接著要同步本地端，這個時候就要用到 pull , -p 可以更新分支以外，也可以順便同步分支的狀況，刪掉在遠端被刪除的分支
i. git log check現在的狀況 ，發現同步成功(僅一行紅字 origin/master , origin/head,沒有2個head)




```
### clone the repo
![alt text](https://miro.medium.com/max/1400/1*3mYhpf1uoC236w9XOWMjkg.png)
```
cd ~/Desktop
git clone <url> 
```

### add, commit ,push 
![alt text](https://miro.medium.com/max/1400/1*_KPtphNY_dqN5nQlbah9iw.png)

```
- 加到 暫存區 （集貨倉的概念）
- 放到儲存庫，也就是會生成一個 commit （出貨）

*add
我們一般的作業區是 “working directory”
- git status 來查看目前 Git 的狀態
- git add file 把檔案存到 staging area

```
![alt text](https://miro.medium.com/max/1400/1*2uJSUpVN0EEV1fCu5jAHHw.png)


```
*commit
當然也可以不用add，直接 git commit -a -m"(註解我們做了什麼改變)"
git commit -a -m file 把檔案加入 repo
如果沒有加 -m的話會跑到自己設定的編譯系統（ex. vim）用於需要詳細說明的情況
那要離開vim是要按 :再按 wq
```

```
*log
git log 來查看目前的紀錄
git log 中，有標明 head 的那行代表最新更新的意思
可以發現我有兩個 commit，但遠端和本地端已經開是不同步了

```
![alt text](https://miro.medium.com/max/1400/1*4i4u3e3cYK-QlCOA-3Wx9Q.png)


```
*push 
git push - push 意即將本機端的檔案推向 server端

*branch 概念補充
我們一開始會擁有一個 “主幹” 叫做 master ，我們每push一個新的commit就會多一個節點，主幹就會越長越高像樹一樣(ﾉ>ω<)ﾉ
那 branch 顧名思義就是從主幹岔開的分支！

但如果是這樣那要 分支（branch）幹嘛？直接推上 master 不就好了嗎！？

但是當今天是多人協作的時候或是要嘗試新東西、debug的時候
我們如果新增一個branch並在上面做更改、嘗試，不僅可以有效管理分支、保留最原始的檔案，也能讓紀錄妥善保存才不會亂掉！

git branch cat - 新增了cat的分支
git branch - 查看自己在哪個branch 
前面有 *的就是目前所在的branch

```
![alt text](https://miro.medium.com/max/1400/1*fVc_Zn5Cx8M2rWA6Rg1YZw.png)

```
*branch 實測
git checkout cat - 切到cat branch

現在我們會利用commit -m 註解我們更改的項目，也學會利用 branch來管理我們嘗試、分工、debug的紀錄
接下來我們就可以開始push了！

git push origin cat
```
![alt text](https://miro.medium.com/max/1400/1*KqaNZV-bOniIG4rBOJLi8A.png)
![alt text](https://miro.medium.com/max/1400/1*T5ubxhh79WK7aZKcvoAJCw.png)

```
我們現在來看一下 Git 的狀態
可以發現遠端的 Head 與本地端 Head 還是不同步
``
雖然 push 了，但遠端沒有改變 (｡ŏ_ŏ) 
要怎麼讓遠端和本地端同步更新呢？
```
![alt text](https://miro.medium.com/max/1400/1*spIDAJUlune8owYiFrdkYA.png)


```
*pull request (同步遠端)
1.打開我們的 repo 查看
發現只有一個 commit 和 一條 branch，還沒有完全更新好( ´•̥̥̥ω•̥̥̥` )
不過仔細一看！多了一個按鈕！

2.點擊 Compare & pull request
提醒你的協作夥伴：「我 push 一個 commit 囉」
3. 按下 Create pull request
4. 在右手邊，可以選擇 tag 其他人 review 或 assign
這個內容主要是要讓你的主管（？？總之是這個 repo 的主要負責者審核、確定內容用的
有種提交檔案更新申請書的感覺
注意上面的 branch 是 cat 合併到主幹 master，順序反了 cat 就變成主幹了，會不好管理

5. 按下 Merge pull request
這個動作主要會將 cat 更新的內容合併到 master 裡
由於這是我測試用的，沒有人跟我協作，所以我們就自己幫自己審核通過嚕

```
![alt text](https://miro.medium.com/max/1400/1*_zaz1jY5GcppqYP2bNmtxw.png)

![alt text](https://miro.medium.com/max/1400/1*7N-EMaN1-rsgdPev9wGoRw.png)

![alt text](https://miro.medium.com/max/1400/1*JVv5SC-u2mXoKojQ1x3rwA.png)

![alt text](https://miro.medium.com/max/1400/1*T_Q0B38lDiUgrg5m5T4pIQ.png)


```
*merge完成就可以刪掉branch
6. 點擊 Delete branch
Wait ! Wait ! Wait ! 為什麼我要刪掉我的 cat branch？
這是一個工作流程叫做 GitHub Flow
是一個統一的工作 SOP 讓工作更有效率！d(d＇∀＇)

```
![alt text](https://miro.medium.com/max/1400/1*DZUvL_ALNDVCfipX1vWyCQ.png)
![alt text](https://miro.medium.com/max/1400/1*yedGvdFbcgvfGjlBpH6BFA.gif)


#### 重點回顧
```
第一步：Create branch
也就是我們剛剛的 cat
第二步：Add commits
也就是 git commit -m"add hello"
第三步：Open a Pull Request
我們回到 repo 點擊的綠色按鈕（Compare & pull request）
第四步：Discuss and Review your code
也就是在按 merge 前，討論串的地方
第五步：Depoly
驗證新增的這條分支的功能是否符合期待
若有問題，可以從 master 拉之前的檔案回復上一動
第六步：Merge
確定這條分支 ok，合併至 master 並刪除該分支

```

```
*pull
同步遠端後，接著要同步本地端，這個時候就要用到 pull
pull 是 Fetch 加上 Merge
為什麼我還要同步？我的本地端就是最新的啊？
忘記剛剛我們剛剛刪掉一個 branch 了嗎？
而且搞不好有人有更新檔案也說不定～


打開終端機
git checkout master
先切換到主要要更新的分支 （master）
git pull -p
-p 可以更新分支以外，也可以順便同步分支的狀況，刪掉在遠端被刪除的分支


或者
git checkout master
git pull
git branch -d cat
git log check現在的狀況 ，發現同步成功(僅一行紅字 origin/master , origin/head)
````

![alt text](https://miro.medium.com/max/1400/1*oWXreh5aohWB1OGZmiyVPw.png)


```
*突發狀況
如果是要 pull 其他 repo 的檔案更新在我的 repo 呢？
git checkout -b sync
這個動作是： branch sync+ checkout sync
git pull (SSH Key) (分支名)
git push origin sync
發 PR（Merge + 刪除分支）
git checkout master
git pull -p



*找錯誤
git blame hello
也可以指定行數 ex. git blame -L 5,10 hello列出第5-10行的意思
但知道是誰寫錯又有什麼用呢？
這時候git又派上用場了！ git 不僅可以看程式碼是誰寫的，還可以回溯你每一個commit ！


*回朔檔名
還記得上面提到的 git checkout 嗎？
沒錯！除了移動分支以外，checkout 還能回溯到之前的 commit
也就是 git checkout HEAD~* 檔名
那我們要怎麼知道我們要回去哪一版呢？
還記得上面講過的 git log嗎？
如果只想看特定檔案的紀錄的話：git log 檔名，就能馬上看到他之前的 commit


1. git checkout HEAD~* 檔名
＊為第幾個版本以前，也就是說:
回到上一版是 git checkout 檔名
回到上上一版是 git checkout HEAD~2 檔名
reset
當然除了這個方法也可以使用 git reset
首先我們可以透過git log 來看之前commit的 “代號”

然後輸入 git reset 代號 一樣可以跳轉到那一版
或是一樣打 git reset HEAD~*
```


```
git checkout vs git reset
git checkout 比較像是移動 head 並將暫存更改為某一版的 commit
如果此時再做分支就會從那一版岔開
git checkout 示意圖：
-A - B - C (master)
       \
        D (HEAD, new-branch)
        
但是 git reset 比較像是拆掉前面的 commit 重來
git reset 示意圖：
- A - B - C (HEAD, master)
如果使用了git reset B則會變成
- A - B (HEAD, master)

```
##### 參考資料
```
https://medium.com/@angela52799/為你自己學-git-筆記-github-應用篇-f2332fc59198
```

