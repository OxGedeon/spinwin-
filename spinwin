<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SpinWin Game</title>

<style>
body{
    margin:0;
    font-family: Arial;
    text-align:center;
    background: linear-gradient(135deg,#111,#222);
    color:white;
}

h1{
    margin-top:20px;
    color:gold;
}

#wheel{
    width:300px;
    height:300px;
    margin:20px auto;
    border-radius:50%;
    border:10px solid gold;
    position:relative;
    overflow:hidden;
    transition: transform 3s ease-out;
}

.slice{
    position:absolute;
    width:50%;
    height:50%;
    transform-origin:100% 100%;
    background:red;
}

button{
    padding:12px 25px;
    font-size:18px;
    border:none;
    border-radius:10px;
    background:gold;
    cursor:pointer;
    margin-top:10px;
}

#points{
    font-size:20px;
    margin-top:10px;
}

#result{
    margin-top:10px;
    font-size:18px;
    color:lightgreen;
}
</style>
</head>

<body>

<h1>🎡 SpinWin Game</h1>

<div id="points">🪙 Points: 0</div>

<div id="wheel"></div>

<button onclick="spin()">SPIN</button>

<div id="result"></div>

<script>
let rewards = [0, 10, 20, 50, 100, 200];
let points = 0;

let wheel = document.getElementById("wheel");

// create wheel slices
for(let i=0;i<rewards.length;i++){
    let slice = document.createElement("div");
    slice.className = "slice";
    slice.style.transform = "rotate(" + (i*60) + "deg) skewY(-30deg)";
    slice.style.background = i%2==0 ? "#ff4d4d" : "#4d79ff";
    wheel.appendChild(slice);
}

function spin(){
    let random = Math.floor(Math.random()*360 + 720);
    wheel.style.transform = "rotate(" + random + "deg)";

    let index = Math.floor((360 - (random % 360)) / 60);
    let win = rewards[index];

    points += win;

    document.getElementById("points").innerText = "🪙 Points: " + points;

    if(win > 0){
        document.getElementById("result").innerText = "🎉 Watsindiye: " + win + " points!";
    }else{
        document.getElementById("result").innerText = "😢 Ntacyo watsindiye, ongera ugerageze!";
    }
}
</script>

</body>
</html><div style="margin:15px auto; padding:10px; background:#333; border:1px solid gold; width:90%; border-radius:10px;">
    <p style="color:gold;">📢 Advertisement</p>

    <!-- Ad placeholder (izahinduka AdMob later) -->
    <div id="ad-container">
        <p style="color:white;">Your Ad will appear here</p>
    </div>
</div><script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>

<script>
  (adsbygoogle = window.adsbygoogle || []).push({});
</script><ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-XXXXXXXXXXXX"
     data-ad-slot="1234567890"
     data-ad-format="auto"></ins><button onclick="watchAd()" style="background:limegreen;">
🎁 Watch Ad = +1 Spin
</button>

<p id="spinCount">🎡 Bonus Spins: 0</p>let bonusSpins = 0;

function watchAd(){
    // simulate ad watching
    alert("🎬 Watching Ad... please wait");

    setTimeout(function(){
        bonusSpins += 1;
        document.getElementById("spinCount").innerText = 
            "🎡 Bonus Spins: " + bonusSpins;

        alert("🎉 You earned +1 bonus spin!");
    }, 3000);
}

// modify spin function to use bonus spins
function spin(){
    if(bonusSpins <= 0){
        alert("❌ No bonus spins. Watch ad first!");
        return;
    }

    bonusSpins--;

    document.getElementById("spinCount").innerText = 
        "🎡 Bonus Spins: " + bonusSpins;

    let random = Math.floor(Math.random()*360 + 720);
    wheel.style.transform = "rotate(" + random + "deg)";

    let index = Math.floor((360 - (random % 360)) / 60);
    let win = rewards[index];

    points += win;

    document.getElementById("points").innerText = "🪙 Points: " + points;

    document.getElementById("result").innerText =
        "🎉 Watsindiye: " + win + " points!";
}
