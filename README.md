<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width" />
<head>
   <title>Parking Master LVL. 1</title>
</head>
<body>
   <h3 id="header-style">Parking Master</h3>
<p class="paraGraph1">How to play:</p>
<ol id="directions">
   <p>1. drive into the Green Outlined Square</p>
   <p>2. do not crash through the process or the game ends!</p>
   <p>3. press "<span><button style="position: relative;
top: -3px;
color: #11fc05;
border: 2px double #11fc05; width: 1.2em; height: 1.2em;"><span style="position: absolute; left: 4px;top: 0px; font-size: 0.6em;">Park</span></button></span>" when you parked in the correct spot.</p>
</ol>
</body>
<link rel="stylesheet" href="style.css">
<!--Game-->
<canvas id="myCanvas" width="600" height="400"
style="border:1px solid #c3c3c3;">
Your browser does not support the canvas element.
</canvas>

<button style="position:absolute;left:550px;top:600px;" class="buttonDrive" onmousedown="moveup()" onmouseup="stopMove()" onclick="carDraw()">Drive</button>

<div id="divCarBody">
<script>
function carDraw() {
var x = 100;
var canvas = document.getElementById("myCanvas");
var ctx = canvas.getContext("2d");
// The Body
ctx.fillStyle = "#000000";
ctx.fillRect(x, 100, 90, 145);

// The wheels
ctx.fillStyle = "000000";
ctx.fillRect(x - 8, 105, 10, 40);
ctx.fillRect(x - 8, 200, 10, 40);
ctx.fillRect(x + 87, 105, 10, 40);
ctx.fillRect(x + 87, 200, 10, 40);

// The lights
ctx.fillStyle = "FFFFFF";
ctx.fillRect(x + 2, 97, 30, 5);
ctx.fillRect(x + 58, 97, 30, 5);
x = x + 3;
};
</script>
</div>
<button class="buttonPark" onclick="parkDetector()" style="position: absolute;left: 550px; top: 540px;"><strong>Park</strong></button>
<script>
var carBody = document.getElementById("divCarBody");

function parkDetector() {
  if (carBody > 176) {
  function carIsParked();
}
  if (carBody < 176) {
  function carIsNotParked();
}
// Direct the car
var p = '<div></div>';

// If the car Parked in the correct spot
function carIsParked() {
alert("You Parked!");
document.body.innerHTML+=p;
document.body.innerHTML+='<button onclick="nextLevel()">Next Level</button>';
}

// If the car is not parked in the correct spot
function carIsNotParked() {
alert("Hmm... it doesn't seem like you parked!");
}

// Redirect to Next Level
function nextLevel() {
window.onload = function() {
    location.href = "https://sites.google.com/view/parking-master-lvl2";
}
</script>
