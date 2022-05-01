# HTML knowledge
# Reference
## MDN
[MDN](https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/HTML_basics)

# Words


# Basic Structure
```
<!DOCUTYPE html>
<html>
    <head>
        めた情報
        <meta charset = "utf-8">
        <title> title </title>
        <link href="<cssパス>" rel=<"参照の名前">>
    </head>
    <body>
        本文
    </body>
</html>
```

# Basic
## Paragraph
段落  
`<p> text </p>`

## New Line
"  "(スペース2つ)

## Table
```
<table>
    <thead>
        <tr>
            <th colspan="2">The table header</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>The table body</td>
            <td>with two columns</td>
        </tr>
    </tbody>
</table>
```
複数列の場合は`colspan=値`, 複数行は`rowspan=値`を`td`タグに入れる 
[ref](https://dream-html-seminar.com/html_css_contents/html_css_chapter7/html_css_703/)

## Insert Imange
`<img src="path" alt="代替テキスト" height="画像高さ">`


## Execute JavaScript file
`<script type="text/javascript" src="パス"></script>`

## Use List
```
<ul>
    <li>item1</li>
    <li>item2</li>
</ul>
```

## Preformatted Text
```
<pre>テキスト</pre>
```
テキストの位置関係を等幅フォントで崩さず表示する

# Input
## Ref of Input
[MWD](https://developer.mozilla.org/ja/docs/Web/HTML/Element/input)

## Input Text
`<input type="text" id="id name" size="width">`  
[javascriptでの入力内容の読み取り](javascript.md#read-textbox-value)

## Input Multiple Lines Text
```
<textarea id="id" wrap="off">
    デフォルト表示内容
</textarea>
```

## Button
`<input type="button" id="button name" value="表示text">`
- 注意
  - 属性として`click="js function"` (or `onclick`)を記載しないこと
  - js側でhtmlのbuttonを取得し, クリック時の操作を記述する方がコードがシンプルになるため
    - [参考](https://developer.mozilla.org/ja/docs/Learn/JavaScript/First_steps/What_is_JavaScript#inline_javascript_handlers)

## Read Files
[参照](https://javascript.keicode.com/newjs/how-to-read-file-with-file-api.php)  
HTML
```
<input type="file" id="inputFile">
```
複数ファイル入力時は`multiple`を加える.  
filteringは`accept=".拡張子, .拡張子"`  
- 入力欄をカスタマイズする 
  - [qiita](https://qiita.com/d0ne1s/items/dd0ffa707ffe051969d7)
  - [???](https://into-the-program.com/customize-input-type-file/)
- フォルダを選択して読み込む場合
  - `webkitdirectory`属性を加

JavaScript
```
const f = document.getElementById('inputFile');
f.addEventListener('change', evt =>{
    const input = evt.target;
    var reader = new FileReader();
    reader.onload() = () =>{
        console.log(rader.result);
    };
    rader.readAsText(f)
})
```

# Style

## Apply CSS file
head部に `<link href="css path" rel="stylesheet">`

## Apply Style to 

Each Element

# Graph
`<canvas>`を使用

[参照](https://developer.mozilla.org/ja/docs/Web/API/Canvas_API/Tutorial/Basic_usage)

HTML
```
<canvas id="canvasId" width="150" height="150"></canvas>
```

JavaScript
```
var canvas = document.getElementById("canvasId");
if(canvas.getContent){
    var ctx = canvas.getContent("2d");
}
```

[詳細](javascript.md#graph)

