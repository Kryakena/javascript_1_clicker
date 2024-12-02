# 🏆Игра кликер на JavaScript🏆

![2024-12-02_11-06-34](https://github.com/user-attachments/assets/f45d0566-0a39-4442-b8dd-a6c4a2c100fe)


1. Создать файлы и папки в указанном порядке

![2024-12-01_23-11-47](https://github.com/user-attachments/assets/4a5bfb48-85cd-4711-a705-010dcf553cce)

2. В файле Click_HTML.html

```HTML
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Кликер</title>  
    <canvas id="Canvas" width="480" height="320"></canvas>  
</head>  
<body>  
<script src="scripts/Click_JS.js"></script>  
</body>  
</html>
```
![2024-12-01_23-13-48](https://github.com/user-attachments/assets/631f8e39-a874-4734-a048-55b4538d8e8d)

3. В файле Click_CSS.css пусто

![2024-12-01_23-14-30](https://github.com/user-attachments/assets/d76921f5-dba4-42ce-abea-b6675e308c4e)

4. В файле Click_JS.js

```JavaScript
var click = 0;  
  
function increment() {  
    var x = e.clientX - 240;  
    var y = e.clientY - 160;  
    var dist = Math.sqrt(y * y + x * x);  
    if (dist < 50) {  
        click++;  
        redraw();  
    }  
}  
var c = document.getElementById("Canvas");  
c.addEventListener("click", increment); //обработчик кликов  
var ctx = c.getContext("2d");  
  
function redraw() {  
    ctx.clearRect(0,0,c.width,c.height);  
    ctx.font="20px Verdana";  
    ctx.fillText ("Клики: " + click,190,20);  
    ctx.beginPath();  
    ctx.fillStyle = "red";  
    ctx.arc(c.width/2, c.height /2, 50, 0, 2*3.14);  
    ctx.fill();  
}  
redraw()
```
![2024-12-01_23-15-31](https://github.com/user-attachments/assets/2b270806-c526-4ddf-9acb-b53c4dc600e9)

