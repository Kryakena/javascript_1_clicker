# 🏆Игра кликер на JavaScript🏆

![2024-12-02_11-06-34](https://github.com/user-attachments/assets/1354500c-21a9-4445-b2b2-590410d60752)

1. Создать файлы и папки в указанном порядке

![2024-12-01_23-11-47](https://github.com/user-attachments/assets/d0a063c0-4a6e-4425-9b29-c18b8b34d817)

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

![2024-12-02_23-19-56](https://github.com/user-attachments/assets/55a99f74-ffed-4c4b-b1cf-3af5fee575bf)

3. В файле Click_CSS.css пусто

![2024-12-01_23-14-30](https://github.com/user-attachments/assets/f38c956b-4e37-41ee-a579-f379e175f77b)


4. В файле Click_JS.js

```JavaScript
var click = 0;  
  
function increment(e) {  
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

![2024-12-02_23-18-51](https://github.com/user-attachments/assets/bc6e617c-c057-4a9d-ac4f-f5f632f45b1b)


