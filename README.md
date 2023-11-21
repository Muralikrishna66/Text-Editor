<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Text Editor</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.1/font/bootstrap-icons.css">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN" crossorigin="anonymous">

    <script>
        function Customcaps(){
            var textbox = document.getElementById("CustomText");
            textbox.value = textbox.value.toUpperCase();

        }
        function Submit(){
                document.getElementById("txtoutput").innerHTML=`${document.getElementById("CustomText").value}`;
            }

        function SizeChange(){
            document.getElementById("txtoutput").style.fontSize=document.getElementById("TextSlider").value+"px";
        }
        function SetShadow(){
            document.getElementById("txtoutput").style.textShadow=`${document.getElementById("RightSlider").value}px 
            ${document.getElementById("DownSlider").value}px 
            ${document.getElementById("BlurnessSlider").value}px
            ${document.getElementById("ColorPicker").value}`;

        }
        function RightBlurness(){
            SetShadow();
        }
        function DownBlurness(){
            SetShadow();
        }
        function BlurnessChange(){
            SetShadow();
        }
        function ColorChange(){
            SetShadow();
        }
        function LetterSpace(){
            document.getElementById("txtoutput").style.letterSpacing = `${document.getElementById("LetterSpaceSlider").value}px`;
        }    
</script>
</head>
<body class="container-fluid">
    <h3 id="input">Enter Your Text : <input type="text" placeholder="Capitals" onkeyup="Customcaps()"  id="CustomText"> <button class="btn btn-success" type="submit" onclick="Submit()"> Submit</button></h3>
        <div class="row">
            <div class="col"><h3 align="center" style="font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;"> Text Style <i class="bi bi-palette"></i></h3></div>
        </div>
        <div class="row">
            <div class="col">
                <dt>Text Size </dt><dd><input type="range" min="1" max="100" value=15 onchange="SizeChange()" id="TextSlider"></dd>
            </div>
            <div class="col">
                <dt> Backgound Text Color</dt>
                <dd><input type="color" onchange="ColorChange()" id="ColorPicker"></dd>
            </div>
            <div class="col">
                <dt>Right Move</dt>
                <dd><input type="range" min="1" max="50" value="1" onchange="RightBlurness()" id="RightSlider"></dd>
            </div>
            <div class="col">
                <dt>Down Move</dt>
                <dd><input type="range" min="1" max="50" value="1" onchange="DownBlurness()" id="DownSlider"></dd>
            </div>
            <div class="col">
                <dt>Text Blurness</dt>
                <dd><input type="range" min="1" max="10" value="1" onchange="BlurnessChange()" id="BlurnessSlider"></dd>
            </div>
            <div class="col">
                <dt>Letter Spacing</dt>
                <dd><input type="range" min="1" max="7" onchange="LetterSpace()" id="LetterSpaceSlider"></dd>
            </div>
        </div>
        <div align="center" id="txtoutput"> </div>
        <h3 style="text-align: center;">Result <i class="bi bi-emoji-sunglasses"></i></h3>
    
    <script href="./script.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-C6RzsynM9kWDrMNeT87bh95OGNyZPhcTNXj1NW7RuBCsyN/o0jlpcV8Qyq46cDfL" crossorigin="anonymous"></script>
</body>
</html>
