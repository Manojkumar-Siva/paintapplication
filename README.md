# Web Page for Paint Application

## AIM:

To design a static website for Paint Application using HTML5 canvas.

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML,CSS and canvas.

### Step 3:

Write javascript to capture move events.

### Step 4:

Perform the drawing operation based on the user input.

### Step 5:

Validate the layout in various browsers.

### Step 6:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html>
<body id="fire">
    <div id="water">
<canvas id="myCanvas" width="1000" height="1000" onclick="showCoords(event)"></canvas></div>
<center>
<button onclick="shape=2" id="air">Circle</button>
<button onclick="shape=4" id="air">Square</button>
<button onclick="shape=6" id="air">Triangle</button>
<br>
<button onclick="size()" id="air" >Change size</button></center>
<center>
<button onclick="change_color(this)" id="wind" style="background: white;"></button>
<button onclick="change_color(this)" id="wind" style="background: rgb(255, 72, 72);"></button>
<button onclick="change_color(this)" id="wind" style="background: rgb(255, 115, 1);"></button>
<button onclick="change_color(this)" id="wind" style="background: rgb(252, 255, 60);"></button>
<button onclick="change_color(this)" id="wind" style="background: rgb(0, 0, 0);"></button>
</center>

<script>


const canvas = document.getElementById("myCanvas");
const ctx = canvas.getContext("2d");
ctx.fillStyle = "#FF0000";
canvas.height = canvas.width;
ctx.transform(1, 0, 0, -1, 0, canvas.height);
let xMax = canvas.height;
let yMax = canvas.width;
let csize= 20;
let sqsize= 50;
let tsize=30;
let tatakae="black";
function size()
{   
if (shape==1 ||shape==2){
    let c= prompt("Please enter size of Circle", "ex:50,20");
    csize=c;
} 
if (shape==3 ||shape==4){
    let s = prompt("Please enter size of Square", "ex:50,20");
    sqsize=s;
}
if (shape==5 || shape==6){
    let t= prompt("Please enter size of Triangle","ex:50,84");
    tsize=t;
}
}
function change_color(element){
    tatakae=element.style.background;
}

    function showCoords(event)

    {
    var x = event.clientX-545;
    var y = yMax-event.clientY;
    var coords = "X coords: " + x + ", Y coords: " + y;
    document.getElementById("demo").innerHTML = coords;
    
        if (shape==1){
            ctx.beginPath();
            ctx.arc(x, y, csize, 0, 2 * Math.PI);
            ctx.fillStyle=tatakae;
            ctx.fill();
        }
        if (shape==2){
            ctx.beginPath();
            ctx.arc(x, y, csize, 0, 2 * Math.PI);
            ctx.strokeStyle=tatakae;
            ctx.stroke();
        }
        if (shape==3){
            ctx.beginPath();
            ctx.rect(x-(sqsize/2),y-(sqsize/2), sqsize,sqsize);
            ctx.fillStyle=tatakae;
            ctx.fill();
        }
        if (shape==4){
            ctx.beginPath();
            ctx.rect(x-(sqsize/2),y-(sqsize/2), sqsize,sqsize);
            ctx.strokeStyle=tatakae;
            ctx.stroke();
        }
        if (shape==6){
            ctx.beginPath();
            ctx.moveTo(x, y);
            ctx.lineTo(x-(tsize/2),y-(tsize*0.86602));
            ctx.lineTo(x+(tsize/2),y-(tsize*0.86602));
            ctx.lineTo(x,y)
            ctx.strokeStyle=tatakae
            ctx.stroke();
        }
        if (shape==5){
            ctx.beginPath();
            ctx.moveTo(x, y);
            ctx.lineTo(x-(tsize/2),y-(tsize*0.86602));
            ctx.lineTo(x+(tsize/2),y-(tsize*0.86602));
            ctx.fillStyle=tatakae
            ctx.fill();
        }
    
    
    }

</script>
<center><p id="demo" style="color: white;"></p></center>
<p style="color:darkgrey;font-size: 50px;text-align:end; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;" >Done By <b>S.MANOJ KUMAR</b></p>
<style>

#water{
    padding-left: 545px;
   
}
#myCanvas{
    background-color:lightblue;
    box-shadow: inset 0 0 5px #b6b6b6;
    backdrop-filter: blur(15px);
    border-radius: 10px;
    border: 1px solid #ffffff;
    align-content: center;
    position:relative;
        left:400px;
        right:300px;

}
#air{
    background-color:chocolate;
    border: 2px solid black;
    border-radius: 20px;
    color: white;
    padding: 15px 32px;
    text-align: center;
    display: inline-block;
    font-size: 25px;
    margin: 4px 2px;
    cursor: pointer;
}
#air:hover{
    background-color:#ffffff36;
    transition: 0.5s;
}
#fire{
    background-color: blanchedalmond;
    position: relative;
        top:100px;

}
#wind{
    border: 2px solid #ffffff;
    border-radius: 25px;
    padding: 25px 25px;
    text-align: center;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
}
#wind:hover{
    opacity: 20%;
    transition: 0.21s;
}
</style>
</body>
</html>    
``` 


## OUTPUT:
![1](./output01.jpg)
![2](./output02.jpg)


## RESULT:

Thus a website is designed and validated for paint application using HTML5 canvas.
