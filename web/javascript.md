# jacaScript Knowledge

# Basic

## Array
### Array Definition
```
var 配列名1 = new Array(要素1, 要素2);
var 配列名2 = [要素1, 要素2];
```

## Dictionary
### Array Definition
```
var 辞書(連想配列)名1 = new Object(要素1, 要素2);
var 辞書名2 = {key1 : value1, key2 : value2};
```

### Reference about for Dictionary
[MDN](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Object)


## Class
### Class Definition
```
class クラス名{
    constructor(){
        this.プロパティ = 初期値;
    }

    メソッド名(){
        処理;
    }
}
```

## const / let / var
[参考](https://qiita.com/cheez921/items/7b57835cb76e70dd0fc4)  
|             | const |  let  |    var    |
|:-----------:|:-----:|:-----:|:---------:|
|再宣言       |x      |x      |o          |
|再代入       |x      |o      |o          |
|スコープ     |ブロック|ブロック|関数       |
|ホイスティング|エラー  |エラー  |undefined |

*ブロック : {中身}  
**ホイスティング : 変数宣言前に参照したらどうなるか

# Event
## Event at Load a page
`window.AddEventListener('load', (無名)関数);`

# Graph
[html.md #graph](html.md#graph)

## Draw a Square
```
var ctx = canvas.getContent("2d");
ctx.fillStyle = "rgba(赤,青,緑,alpha)";
ctx.fillRect(左辺位置, 上辺位置, 幅, 高さ);
```

## Draw a Line
[参考](https://developer.mozilla.org/ja/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes)
```
ctx.beginPath();
ctx.moveTo(x座標, y座標);
ctx.lineTo(x座標, y座標);
ctx.lineTo(x座標, y座標);
```
線を引く場合
```
ctx.stroke();
```
塗りつぶす場合
```
ctx.fill();
```
線を閉じる
```
ctx.closePath()
```
線に色を付ける
```
ctx.strokeStyle = "rgba(red, green, blue, alpha)";
```

# Input
## Get All Buttons from HTML
```
const buttons = document.querySelectorAll('button');
```
## Call Function as Input "Button" Clicked Event
```
function buttonClicked(){
    function contents
}

buttons = document.querySelectorAll("input")
for(let i = 0; i < buttons.length; i++){
    buttons[i].addEventListener('click', calling function)
}
```
`querySelectorAll()`の引数はCSSセレクタ (`p`とか`input`など<>の先頭で定義されるやつ) ->
[参照](https://developer.mozilla.org/ja/docs/Web/API/Document/querySelectorAll)

## Read Textbox Value
```
テキストボックスエレメント.value
```

## Read HTML
```
const f = document.getElementById('inputFile');
f.addEventListener('change', evt =>{
    const input = evt.target;
    
})
```

# Control HTML
## Re-write HTML element
`HTML要素.innerHTML = '書き換える文字列'`  
Note: `<script>`は実行されないようになっている

## Re-write HTML element 2
`HTML要素.textContent = 書き換える文字列'`

## Inset New Element
`親要素.insertBefor(挿入要素, 挿入場所の一つ後ろの要素)`  
挿入したい場所がある要素の後ろの場合は, 2番目の引数に`.nextElementSibling`を付ける

## Make Element in JavaScript
```
const 新要素 = docment.createElement('cssセレクタ');
```