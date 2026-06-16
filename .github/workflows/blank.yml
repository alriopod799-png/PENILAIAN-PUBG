<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Penilaian Pemain PUBG</title>

<style>
body{
    font-family: Arial, sans-serif;
    background:#121212;
    color:white;
    display:flex;
    justify-content:center;
    align-items:center;
    height:100vh;
}

.container{
    width:400px;
    background:#1e1e1e;
    padding:20px;
    border-radius:10px;
}

input,select,button{
    width:100%;
    padding:10px;
    margin:5px 0;
    border:none;
    border-radius:5px;
}

button{
    background:#00c853;
    color:white;
    cursor:pointer;
}

.result{
    margin-top:15px;
    padding:10px;
    background:#333;
    border-radius:5px;
}
</style>
</head>

<body>

<div class="container">
    <h2>Penilaian Pemain PUBG</h2>

    <input type="text" id="nama" placeholder="Nama Pemain">

    <input type="number" id="kd" step="0.1" placeholder="K/D Ratio">

    <input type="number" id="winrate" placeholder="Win Rate (%)">

    <select id="rank">
        <option value="10">Bronze</option>
        <option value="20">Silver</option>
        <option value="30">Gold</option>
        <option value="40">Platinum</option>
        <option value="50">Diamond</option>
        <option value="60">Crown</option>
        <option value="70">Ace</option>
        <option value="80">Conqueror</option>
    </select>

    <button onclick="hitung()">Hitung Nilai</button>

    <div class="result" id="hasil"></div>
</div>

<script>
function hitung(){

let nama = document.getElementById("nama").value;
let kd = parseFloat(document.getElementById("kd").value) || 0;
let winrate = parseFloat(document.getElementById("winrate").value) || 0;
let rank = parseInt(document.getElementById("rank").value);

let skor = (kd * 20) + (winrate * 0.5) + rank;

let kategori = "";

if(skor >= 130){
    kategori = "PRO PLAYER";
}else if(skor >= 100){
    kategori = "SANGAT BAIK";
}else if(skor >= 70){
    kategori = "BAIK";
}else{
    kategori = "PEMULA";
}

document.getElementById("hasil").innerHTML =
`
<b>Nama:</b> ${nama}<br>
<b>Skor:</b> ${skor.toFixed(2)}<br>
<b>Kategori:</b> ${kategori}
`;
}
</script>
