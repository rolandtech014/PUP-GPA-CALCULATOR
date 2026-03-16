<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>R Code! – Ultimate PUP 2076 GPA Portal</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&display=swap" rel="stylesheet">
<style>
*{box-sizing:border-box;margin:0;padding:0;font-family:'Orbitron',sans-serif;}
body{
    background:#0a0a0a;
    min-height:100vh;
    overflow-x:hidden;
    color:white;
    perspective:1000px;
}

/* PARTICLE BACKGROUND */
body::before{
    content:'';
    position:fixed;
    top:0;left:0;width:100%;height:100%;
    background:radial-gradient(circle at 50% 50%, #330000, #0a0a0a);
    z-index:-3;
    animation:bgPulse 15s infinite alternate;
}
@keyframes bgPulse{
    0%{background-position:0 0;}100%{background-position:100% 100%;}
}

/* HEADER */
header{
    display:flex;
    align-items:center;
    gap:20px;
    background:rgba(128,0,0,0.5);
    backdrop-filter:blur(20px);
    padding:20px 40px;
    border-radius:25px;
    box-shadow:0 0 50px #800000;
    transform-style:preserve-3d;
}
header img{
    width:70px;
    animation:spin 12s linear infinite;
    filter:drop-shadow(0 0 30px #ffd700);
}
header h1{
    font-size:30px;
    text-shadow:0 0 20px #ffd700;
    color:#f0e68c;
}

/* ANIMATIONS */
@keyframes spin{
    0%{transform:rotateY(0deg);}100%{transform:rotateY(360deg);}
}
@keyframes bgPulse{
    0%{background-position:0 0;}100%{background-position:100% 100%;}
}
@keyframes glowPulse{
    0%,100%{text-shadow:0 0 10px #ffd700;}50%{text-shadow:0 0 30px #ffd700;}
}

/* CONTAINER */
.container{
    width:95%;
    max-width:1200px;
    margin:60px auto;
    display:flex;
    flex-direction:column;
    gap:50px;
    transform-style:preserve-3d;
}

/* CARDS */
.card{
    background:rgba(255,255,255,0.05);
    backdrop-filter:blur(30px);
    border-radius:30px;
    padding:40px;
    box-shadow:0 0 80px rgba(255,0,0,0.5);
    transition:transform 0.3s ease, box-shadow 0.3s ease;
}
.card:hover{
    transform:translateY(-20px) rotateX(5deg) rotateY(5deg);
    box-shadow:0 0 100px #ffd700,0 0 60px #f0e68c;
}

/* INPUTS */
input, select{
    width:calc(50% - 14px);
    padding:16px;
    margin:6px;
    border-radius:15px;
    border:none;
    background:rgba(255,255,255,0.05);
    color:white;
    font-weight:bold;
    font-size:16px;
    transition:0.3s;
}
input:focus, select:focus{
    outline:none;
    box-shadow:0 0 30px #ffd700;
}

/* BUTTONS NEON */
button{
    padding:16px 35px;
    background:linear-gradient(45deg,#f0e68c,#800000);
    border:none;
    border-radius:20px;
    color:white;
    font-weight:bold;
    font-size:16px;
    cursor:pointer;
    text-shadow:0 0 8px #fff;
    transition:0.3s;
    animation:bounce 2s infinite;
}
button:hover{
    transform:scale(1.2);
    box-shadow:0 0 40px #ffd700,0 0 60px #f0e68c,0 0 100px #800000;
}
@keyframes bounce{0%,100%{transform:translateY(0);}50%{transform:translateY(-10px);}}

/* PROFILE */
.profile{
    display:flex;
    flex-direction:column;
    align-items:center;
    gap:15px;
    transform-style:preserve-3d;
}
.name{
    font-size:40px;
    font-weight:bold;
    color:#f0e68c;
    animation:glowPulse 2s infinite;
}
.id{font-size:16px;color:#00ccff;}
.program{font-size:32px;color:white;}

/* GPA PANEL */
.gpaPanel{
    background:rgba(255,255,255,0.05);
    backdrop-filter:blur(25px);
    border-radius:30px;
    padding:40px;
    text-align:center;
    box-shadow:0 0 100px #ffd700;
    transform-style:preserve-3d;
}
.gpaPanel h2{
    font-size:40px;
    color:#f0e68c;
    animation:glowPulse 2s infinite;
    text-shadow:0 0 30px #ffd700;
}
.message{
    margin-top:15px;
    font-weight:bold;
    font-size:22px;
    color:#ffd700;
    text-shadow:0 0 25px #ffd700;
}

/* TABLE */
table{
    width:100%;
    border-collapse:collapse;
    margin-top:25px;
    backdrop-filter:blur(20px);
}
th{
    background:#800000;
    color:white;
    padding:15px;
    text-transform:uppercase;
    letter-spacing:1px;
}
td{
    border:1px solid #ddd;
    padding:14px;
    text-align:center;
    transition:0.3s;
    background:rgba(255,255,255,0.05);
}
tbody tr:hover{
    transform:scale(1.05) rotateX(2deg) rotateY(2deg);
    background:rgba(255,255,0,0.15);
}

/* PAGE CONTROL */
#page2{display:none;}

/* CURSOR PARALLAX */
body{
    perspective:1500px;
}
.card, .gpaPanel{
    transform-style:preserve-3d;
    transition:transform 0.1s;
}
</style>
</head>
<body>

<header>
<img src="https://upload.wikimedia.org/wikipedia/en/4/48/Polytechnic_University_of_the_Philippines_logo.svg">
<h1>R Code! – Ultimate VR PUP 2076 GPA Portal</h1>
</header>

<div class="container">

<!-- PAGE 1 -->
<div id="page1" class="card">
<h2>Student Information</h2>
<div style="display:flex; flex-wrap:wrap; gap:20px;">
<input id="name" placeholder="Full Name">
<input id="age" placeholder="Age">
<select id="gender"><option>Gender</option><option>Male</option><option>Female</option></select>
<input id="idnum" placeholder="Student ID Number">
<input id="program" placeholder="Program">
<input id="semester" placeholder="Semester">
<input id="year" placeholder="Year">
<input id="campus" placeholder="Campus">
</div>
<button onclick="start()">Continue</button>
</div>

<!-- PAGE 2 -->
<div id="page2" class="card">

<div class="profile">
<div class="name" id="sname"></div>
<div class="id" id="sid"></div>
<div class="program" id="sprogram"></div>
</div>

<div class="gpaPanel">
<h2>GPA: <span id="gpa">0.00</span></h2>
<div class="message" id="message"></div>
</div>

<table>
<tr>
<th>Subject Code</th>
<th>Subject Name</th>
<th>Units</th>
<th>Final Grade</th>
<th>Remarks</th>
</tr>
<tbody id="subjects"></tbody>
</table>

<div style="margin-top:20px;display:flex;gap:15px;flex-wrap:wrap;">
<button onclick="addSubject()">➕ Add Subject</button>
<button onclick="removeSubject()">➖ Remove Subject</button>
<button onclick="compute()">Compute GPA</button>
</div>

</div>
</div>

<script>
/* generate default 8 subjects */
function generateRows(n=8){
let rows="";
for(let i=0;i<n;i++){
rows+=`<tr>
<td><input></td>
<td><input></td>
<td><input type="number" class="units"></td>
<td><input type="number" class="grade" step="0.01"></td>
<td class="remark"></td>
</tr>`;
}
document.getElementById("subjects").innerHTML=rows;
}
generateRows();

/* add/remove subjects dynamically */
function addSubject(){
let tbody=document.getElementById("subjects");
let row=document.createElement("tr");
row.innerHTML=`<td><input></td><td><input></td><td><input type="number" class="units"></td><td><input type="number" class="grade" step="0.01"></td><td class="remark"></td>`;
tbody.appendChild(row);
}
function removeSubject(){
let tbody=document.getElementById("subjects");
if(tbody.rows.length>1) tbody.deleteRow(tbody.rows.length-1);
}

/* page transition */
function start(){
document.getElementById("page1").style.display="none";
document.getElementById("page2").style.display="flex";
document.getElementById("sname").innerText=document.getElementById("name").value;
document.getElementById("sid").innerText=document.getElementById("idnum").value;
document.getElementById("sprogram").innerText=document.getElementById("program").value;
}

/* dynamic GPA computation */
function compute(){
let units=document.querySelectorAll(".units");
let grades=document.querySelectorAll(".grade");
let remarks=document.querySelectorAll(".remark");
let totalUnits=0,totalPoints=0;

for(let i=0;i<units.length;i++){
let u=parseFloat(units[i].value);
let g=parseFloat(grades[i].value);
if(!isNaN(u)&&!isNaN(g)){
totalUnits+=u;
totalPoints+=u*g;
remarks[i].innerText=(g<=3)?"Passed":"Failed";
}
}

let gpa=(totalPoints/totalUnits).toFixed(2);
document.getElementById("gpa").innerText=gpa;

let msg="";
if(gpa>=1.00 && gpa<=1.50) msg="🏆 President's Lister – Future Legend!";
else if(gpa>=1.51 && gpa<=1.75) msg="🎖 Dean's Lister – Keep Shining!";
else msg="Keep going, aim for the stars!";
document.getElementById("message").innerText=msg;
}

/* CURSOR PARALLAX */
document.addEventListener("mousemove",(e)=>{
let cards=document.querySelectorAll(".card,.gpaPanel");
cards.forEach(card=>{
    let x=(window.innerWidth/2-e.clientX)/50;
    let y=(window.innerHeight/2-e.clientY)/50;
    card.style.transform=`rotateY(${x}deg) rotateX(${y}deg)`;
});
});
</script>
</body>
</html>
