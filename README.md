<!DOCTYPE html>
<html lang="zh-Hant">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>魔幻影Sksnki介紹網頁</title>
<style>
body { margin:0; font-family:"Microsoft JhengHei",sans-serif; text-align:center; background:linear-gradient(135deg,#74b9ff,#a29bfe); padding:20px; }
h1{margin:20px 0;}
button{padding:12px 25px;border:none;border-radius:8px;background:#0984e3;color:#fff;margin:10px;cursor:pointer;}
button:hover{background:#74b9ff;}
#about-section,#more-section{display:none;margin-top:20px;}
img{max-width:90%;border-radius:10px;margin-top:15px;}
iframe{width:100%;height:215px;border-radius:10px;}
.clown{position:absolute;width:80px;transition:transform .5s;}
</style>
</head>
<body>
<h1>🎩 魔幻影Sksnki</h1>
<p>嗨嗨，我是魔幻影Sksnki，是台灣的 YouTube。<br>主要拍 ROBLOX，有時會舉辦抽獎，記得訂閱我！</p>

<button onclick="showAbout()">關於我</button>

<div id="about-section">
  <h2>關於我</h2>
  <img src="https://drive.google.com/uc?export=view&id=1q3jMHRMPkKXMPcdJyN-ztFbgAN2EyVST" alt="魔幻影Sksnki的照片">
  <p>嗨嗨，我是魔幻影Sksnki，是一位台灣的 YouTube。<br>我主要拍 ROBLOX，有時候會舉辦一些抽獎。<br>大家記得訂閱我喔！</p>
  <button onclick="showMore()">更多</button>
</div>

<div id="more-section">
  <h2>🎬 魔幻影Sksnki的影片</h2>
  <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ?autoplay=1" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div>

<script>
function showAbout(){
  document.getElementById("about-section").style.display="block";
}
function showMore(){
  document.getElementById("more-section").style.display="block";
  spawnClowns(5);
}
function spawnClowns(count){
  for(let i=0;i<count;i++){
    const c=document.createElement("img");
    c.src="https://i.imgur.com/6f6k6lX.png"; // 嘲諷小丑梗圖片
    c.className="clown";
    c.style.top=Math.random()*(window.innerHeight-100)+"px";
    c.style.left=Math.random()*(window.innerWidth-80)+"px";
    document.body.appendChild(c);
    setInterval(()=>{
      c.style.transform=`translate(${Math.random()*20-10}px,${Math.random()*20-10}px)`;
    },500);
  }
}
</script>
</body>
</html>
