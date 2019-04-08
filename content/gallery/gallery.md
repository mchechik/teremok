---
title: 'Gallery'
date: 2018-11-19T10:47:58+10:00
draft: false
weight: 1
---

<html>
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
<link rel="stylesheet" href="style.css">
<style>
.mySlides {display:none}
</style>
<body>

<div class="w3-content" style="max-width:800px">
  <img alt-text="Image not found" class="mySlides rotate180" src="/images/IMG_0050.JPG" style="width:100%">
  <img alt-text="Image not found" class="mySlides rotate180" src="/images/IMG_0052.JPG" style="width:100%">
  <img alt-text="Image not found" class="mySlides" src="/images/house.jpg" style="width:100%">
  <img alt-text="Image not found" class="mySlides" src="/images/IMG_0043.JPG" style="width:100%">  
  <img alt-text="Image not found" class="mySlides rotate180" src="/images/IMG_0055.JPG" style="width:100%">
  <img alt-text="Image not found" class="mySlides rotate180" src="/images/IMG_0057.JPG" style="width:100%">
  <img alt-text="Image not found" class="mySlides rotate180" src="/images/IMG_0081.JPG" style="width:100%">
</div>

<div class="w3-center">
  <div class="w3-section">
    <button class="w3-button w3-light-grey" onclick="plusDivs(-1)">❮ Prev</button>
    <button class="w3-button w3-light-grey" onclick="plusDivs(1)">Next ❯</button>
  </div>
</div>

<script>
var slideIndex = 1;
showDivs(slideIndex);

function plusDivs(n) {
  showDivs(slideIndex += n);
}

function currentDiv(n) {
  showDivs(slideIndex = n);
}

function showDivs(n) {
  var i;
  var x = document.getElementsByClassName("mySlides");
  var dots = document.getElementsByClassName("demo");
  if (n > x.length) {slideIndex = 1}    
  if (n < 1) {slideIndex = x.length}
  for (i = 0; i < x.length; i++) {
    x[i].style.display = "none";  
  }
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace(" w3-red", "");
  }
  x[slideIndex-1].style.display = "block";  
  dots[slideIndex-1].className += " w3-red";
}
</script>

</body>
</html>
