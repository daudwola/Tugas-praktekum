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





# praktikum 2

<img width="1080" height="1049" alt="181030" src="https://github.com/user-attachments/assets/ba80c1f6-31c2-47a3-94d5-a9bf75250c50" />


<!DOCTYPE html>
<html>
<head>
    <title>Kategori Nilai</title>

    <style>
        body {
            font-family: Arial;
            padding: 30px;
            background: #f2f2f2;
        }

        .box {
            background: white;
            width: 300px;
            padding: 20px;
            border-radius: 10px;
            margin: auto;
            box-shadow: 0 0 10px gray;
        }

        h2 {
            text-align: center;
        }

        label {
            font-size: 18px;
        }

        input {
            width: 90%;
            padding: 8px;
            margin: 10px;
            font-size: 16px;
        }

        button {
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
        }

        #hasil {
            margin-top: 15px;
            font-weight: bold;
        }
    </style>

</head>

<body>

<div class="box">

<h2>TUGAS PRAKTIKUM #2</h2>

<label>Nilai:</label>
<input type="number" id="nilai">


<label>Kategori:</label>
<input type="text" id="kategori" readonly>


<br>

<button onclick="proses()">Proses</button>


<div id="hasil"></div>

</div>


<script>

function proses(){

let nilai = document.getElementById("nilai").value;
let kategori;


if(nilai >= 90){
    kategori = "A";
}
else if(nilai >= 80){
    kategori = "B";
}
else if(nilai >= 70){
    kategori = "C";
}
else if(nilai >= 60){
    kategori = "D";
}
else{
    kategori = "E";
}


document.getElementById("kategori").value = kategori;

document.getElementById("hasil").innerHTML =
"Nilai " + nilai + " termasuk kategori " + kategori;

}

</script>


</body>
</html>


# praktekum 3


<img width="1080" height="1271" alt="181034" src="https://github.com/user-attachments/assets/afdcdef2-dfca-440c-a172-fd07e112326f" />


<!DOCTYPE html>
<html>
<head>
    <title>Tugas Praktikum #3</title>

    <style>
        body {
            font-family: Arial, sans-serif;
            background: #f2f2f2;
            padding: 40px;
        }

        .box {
            background: white;
            width: 300px;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 0 10px gray;
        }

        h2 {
            text-align: center;
        }

        label {
            display: block;
            margin-top: 15px;
            font-size: 18px;
        }

        input {
            width: 95%;
            padding: 8px;
            margin-top: 5px;
            font-size: 16px;
        }

        button {
            margin-top: 20px;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
        }

        #hasil {
            margin-top: 15px;
            font-weight: bold;
        }
    </style>

</head>

<body>

<div class="box">

<h2>TUGAS PRAKTIKUM #3</h2>

<label>Total Belanja:</label>
<input type="number" id="belanja">

<label>Diskon (%):</label>
<input type="number" id="diskon">

<label>Total Bayar:</label>
<input type="text" id="bayar" readonly>


<button onclick="hitung()">Hitung</button>


</div>


<script>

function hitung(){

    let total = document.getElementById("belanja").value;
    let diskon = document.getElementById("diskon").value;


    let potongan = total * diskon / 100;

    let bayar = total - potongan;


    document.getElementById("bayar").value = 
    "Rp " + bayar.toLocaleString();

}

</script>


</body>
</html>
