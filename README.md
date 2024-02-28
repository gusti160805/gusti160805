<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8"/>
        <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
        <title>Calculator</title>
        <link rel="stylesheet" href="style.css" type="text/css"/>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-4bw+/aepP/YC94hEpVNVgiZdgIC5+VKNBQNGCHeKRQN+PtmoHDEXuppvnDJzQIu9" crossorigin="anonymous"/>
        <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.5/font/bootstrap-icons.css">
    </head>
    <body>
        <div class="calculator">
         <h1><font color="purple">kalkulator</font></h1>
            <input type="text" id="layar"/>
            <div class="container-tombol">
                <span class="tombol" id="operator">C</span>
                <span class="tombol" id="operator">/</span>
                <span class="tombol" id="operator">*</span>
                <span class="tombol" id="operator">DEL</span>
                <span class="tombol">1</span>
                <span class="tombol">2</span>
                <span class="tombol">3</span>
                <span class="tombol" id="operator">-</span>
                <span class="tombol">4</span>
                <span class="tombol">5</span>
                <span class="tombol">6</span>
                <span class="tombol" id="operator">+</span>
                <span class="tombol">7</span>
                <span class="tombol">8</span>
                <span class="tombol">9</span>
                <span class="tombol" id="operator">.</span>
                <span class="tombol">00</span>
                <span class="tombol" id="nol">0</span>
                <span class="tombol" id="hitung">=</span>
            </div>
            <footer>
                <div class="container">
                    <div class="row">
                        <div class="col text-center">
                            <ul class="mt-3"><li></li>
                            </ul>
                        </div>
                    </div>
                </div>
            </footer>
        </div>
    </body>
    <script src="app.js"></script>
</html>


.calculator{
    width:300px;
    background-color: #d410a3;
    margin: 50px auto 10px auto;
    padding: 7px;
    border-radius: 5px;
    display: block;

}


h1{
    text-align: center;
}

#layar{
    width: 100%;
    box-sizing: border-box;
    border: 1px solid #f113d4;
    font-size: 50px;
    font-weight: bold;
    color: rgb(118, 118, 139);
    padding: 7px 5px;
    text-align: right;
    outline: none;
}

.container-tombol{
    display: flex;
    flex-wrap: wrap;
}

.tombol{
    display: flex;
    width: 25%;
    font-size: 20px;
    color: rgb(24,23,23);
    font-weight: bold;
    height: 70px;
    border: 1px solid #cecece;
    box-sizing: border-box;
    justify-content: center;
    align-items: center;
}

.tombol:nth-child(4n+1){
    border-left: 1px solid#cecece;
}

.tombol:hover{
    background-color: #d8d8d8;
    cursor: pointer;
}
#nol{
    flex-grow: 2;
}
#operator{
    background-color: #d8d8d8;
}

#hitung{
    background-color: #f80daa;
    cursor: white;
}

#hitung:hover{
    background-color: #ffa64a;
    cursor: pointer;
}

footer{
    padding: 5px;
}
footer li{
    list-style: none;
}
footer a{
    color: black;
}

/*PHP*/
@media(max-width:576px){
    .calculator{
        width: 50%;
        height: 50%;
    }
}











//deklarasi variabel
const tombol = document.querySelector(".container-tombol");
const layar = document.querySelector("#layar");

//jika tombol angka di klik oleh user
tombol.addEventListener("click", function(e){
    let tomboldiClick = e.target;
    let nilaiTombol = tomboldiClick.innerText;

    //jika tombol C di klik oleh user
    if (nilaiTombol == "C"){
        layar.value = "";
    }else if (nilaiTombol == "DEL"){
        layar.value = layar.value.slice(0,-1);
    }else if (nilaiTombol == "="){
    layar.value = eval(layar.value);
    }else{
        layar.value = layar.value + nilaiTombol;
    }
});
