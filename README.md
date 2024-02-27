//deklarasi variabel
const tombol = document.querySelector(".container-tombol");
const layar = document.querySelector("#layar");

//jika tombol angka di klik oleh user
tombol.addEventListener("click" function(e)){
 let tomboldiClick = e.target;
 let nilaiTombol = tomboldiClick.innerText;

//jika tombol C di klik oleh user
if(nilaiTombol == "C"){
  layar.value = "";
}else if(nilaiTombol == "DEL"){
  layar.value = layar.value.slice(0, -1);
}else if(nilaiTombol == "="){
  layar.value = eval(layar.value);
}else{
  layar.value = layar.value + nilaiTombol;
 }
}};

App.js
