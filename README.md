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
### clone the repo
權限搞定也生成 repo 後，要怎麼把 repo 的檔案抓下來呢？
- step 1，點選那個綠綠的 Clone or download
![alt text](https://miro.medium.com/max/1400/1*3mYhpf1uoC236w9XOWMjkg.png)

- step 2，git clone 綠色的URL
```
cd ~/Desktop
git clone <url> 
```

### basic command
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

```
我們現在來看一下 Git 的狀態
可以發現遠端的 Head 與本地端 Head 還是不同步

雖然 push 了，但遠端沒有改變 (｡ŏ_ŏ) 
要怎麼讓遠端和本地端同步更新呢？
```

![alt text](https://miro.medium.com/max/1400/1*KqaNZV-bOniIG4rBOJLi8A.png)













