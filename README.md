<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Garfield Character Selector</title>

<style>

body{
    font-family: Arial, sans-serif;
    text-align:center;
    background-color:#f5f5f5;
    margin-top:50px;
}

h1{
    color:#333;
}

select{
    font-size:16px;
    padding:8px;
}

img{
    margin-top:20px;
    width:300px;
    border-radius:10px;
    border:2px solid #ccc;
}

</style>

</head>

<body>

<h1>Garfield Character Selector</h1>

<label>Select Character:</label>

<select id="characterSelect">
</select>

<br>

<img id="characterImage" src="images/Garfield.jpg" alt="Character Image">

<script>

// Character list
const characters = ["Garfield","Odie","Nermal","Pooky","Jon"];

// Select elements
const selectBox = document.getElementById("characterSelect");
const image = document.getElementById("characterImage");

// Fill selection box
characters.forEach(function(character){

    const option = document.createElement("option");

    option.value = character;
    option.text = character;

    selectBox.appendChild(option);

});

// Change image when selection changes
selectBox.addEventListener("change", function(){

    const selectedCharacter = selectBox.value;

    image.src = "images/" + selectedCharacter + ".jpg";

});

</script>

</body>
</html>
