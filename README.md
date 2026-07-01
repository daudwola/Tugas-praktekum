# PRAKTIKUM 1 Kalkulator foto copy 

<img width="1080" height="969" alt="181011" src="https://github.com/user-attachments/assets/8262854c-7bf5-4dc8-a7b7-84618f8321d2" />



<!DOCTYPE html>
<html>
<head>
<title>Program Fotocopy</title>

<style>
body{
    font-family: Arial;
    background:#f2f2f2;
    padding:20px;
}

.container{
    background:white;
    width:320px;
    padding:20px;
    margin:auto;
    border-radius:10px;
    box-shadow:0 0 10px gray;
}

h2{
    text-align:center;
}

input{
    width:95%;
    padding:10px;
    margin:10px 0;
    font-size:16px;
}

button{
    width:100%;
    padding:10px;
    background:blue;
    color:white;
    border:none;
    border-radius:5px;
    font-size:16px;
}

.hasil{
    margin-top:20px;
    background:#e8f5e9;
    padding:15px;
    border-radius:8px;
}
</style>

</head>

<body>


<div class="container">

<h2>Harga Fotocopy</h2>

<p>Jumlah lembar fotocopy:</p>

<input type="number" id="lembar" placeholder="Masukkan jumlah lembar">


<button onclick="proses()">Proses</button>


<div class="hasil" id="hasil">
Hasil muncul disini
</div>


</div>



<script>

function proses(){

let jumlah = document.getElementById("lembar").value;

let harga;
let total;


// kondisi If Else

if(jumlah < 100){

    harga = 150;

}

else if(jumlah >= 100 && jumlah <= 200){

    harga = 100;

}

else{

    harga = 80;

}


// menghitung biaya

total = jumlah * harga;



document.getElementById("hasil").innerHTML =

"Jumlah fotocopy : " + jumlah + " lembar <br>" +

"Harga per lembar : Rp " + harga + "<br>" +

"Total biaya : Rp " + total;


}


</script>


</body>
</html>
