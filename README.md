<html>
<head>
<meta charset="UTF-8">
<title>美術部</title>

<style>
body{
  margin:0;
  height:100vh;
  display:flex;
  justify-content:center;
  align-items:center;
  text-align:center;
  font-family:sans-serif;
  background:#f5f5ff;
}

.box{
  background:white;
  padding:40px;
  border-radius:20px;
  box-shadow:0 10px 30px rgba(0,0,0,0.15);
}

h1{
  font-size:2em;
}

p{
  font-size:1.2em;
}
</style>

</head>

<body>

<div class="box">
<h1>おめでとう！</h1>

<p>
あなたは美術部の勧誘ポスターを見つけました！<br>
ツイッター、インスタもちゃんとあります。<br>
探してみてください。
</p>

<p id="counter"></p>

</div>

<script>
let count = localStorage.getItem("visitCount");

if(!count){
  count = 1;
}else{
  count = Number(count) + 1;
}

localStorage.setItem("visitCount",count);

document.getElementById("counter").innerText =
"この端末でのアクセス回数：" + count;
</script>

</body>
</html>
