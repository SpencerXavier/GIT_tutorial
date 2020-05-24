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
- 首先，點選那個綠綠的 Clone or download
![alt text](https://miro.medium.com/max/1400/1*3mYhpf1uoC236w9XOWMjkg.png)

