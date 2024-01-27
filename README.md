# Netflixlogo
HTML CODE:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Netflix Logo</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="netflix">
        <span class="left"></span>
        <span class="center"></span>
        <span class="right"></span>
    </div>
</body>
</html>

CSS CODE:
*{
    margin: 0;
    height: 0;
    box-sizing: border-box;
}
body{
    background: black;
}
.netflix{
    width: 150px;
    height: 250px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    

}
.netflix span{

    width: 50px;
    height: 0;
    background: #db0001;
    position: absolute;


}

.left{
    left: 0;
    bottom: 0;
    animation: anim 1s linear forwards;
    animation-delay: 1s;

}
 .center{
    top: 0;
    left: 0;
    transform: skewX(22deg);
    transform-origin: top left;
    animation: anim 1s linear forwards;
    animation-delay: 2s;

}
.right{
    right: 0;
    bottom: 0;
    animation: anim 1s linear forwards;
    animation-delay: 3s;

}
.netflix::after{
    content:'';
    width: 120%;
    height: 20px;
    border-radius: 50%;
    background:black;
    position: absolute;
    left: -10%;
    bottom: -10px;
    z-index: 5;

}
@keyframes anim{
    100%{
        height: 100%;

    }

}
