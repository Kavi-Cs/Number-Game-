<html>
    <head>
        <title>Random Number Game </title>
        <style>
            body{
                font-family: Verdana;
                text-align:center;
                padding: 50px;
                background: -webkit-gradient();
                background-color: blanchedalmond;
                margin: auto;
            }
            p{
                color:blueviolet;
                font-family: Verdana, Geneva, Tahoma, sans-serif;
                font-size: 100%;
            }
            button {
                margin-top: 15px;
                padding: 12px 20px;
                font-size: 16px;
                font-family: 'Gill Sans';
                font-weight: bolder;
                border: 2cm;
                cursor: pointer;

            }
            .message{
                margin-top: 15px;
                font-size: 20px;
                font-weight: bold;
                color: darkblue;
                animation:cubic-bezier(0.95, 0.05, 0.795, 0.035)
            }

            .NumberGame{
                background: -moz-repeating-linear-gradient();
                max-width: 500px;
                margin: auto;
                padding: 30px;
                border-radius: 16px;
                box-shadow:0 12px 25px rgba(0, 0, 0, 0.15); 
                border:  2px solid;
            }
   
        </style>

    </head>
    <body>
        <div class = "NumberGame" >
            <p> <b>Enter your Random Number Between (1-100) </b> </p>
            <p><input type = "text" id  = "guess" placeholder="Enter your guess" min = "0" max = "100" > </p>
            <button id = "guess check"> Guess! </button>
            <p>Do you want restart the Game ? </p>
            <p> Please click <b><i>Restart</i></b> button below  </p>
            <p class = "message" id = "message"> </p>
            <button id = "restart Game"> Restart! </button>

        </div>
        
        <script type = "text/javascript">

            document.getElementById("guess check").onclick = function(){
              var randomNumber = Math.random();
              randomNumber = randomNumber*101;
              randomNumber = Math.floor(randomNumber);
              randomNumber = Math.floor(randomNumber);
              var messageE1 = document.getElementById("message")

            if (document.getElementById("guess").value < 0 || document.getElementById("guess").value > 100){
                messageE1.textContent = "Please Enter a number between 0 and 100";  
            }
            else if (document.getElementById("guess").value < randomNumber){
                messageE1.textContent = "Your number is Too Low!"
            }
            else if (document.getElementById("guess").value > randomNumber){
                messageE1.textContent = "your number is Too High!"
            }
            else{
                messageE1.textContent = "Well done!"
            }
            
            }
            
            document.getElementById("restart Game").onclick = function(){
              var randomNumber = Math.random();
              randomNumber = randomNumber*101;
              randomNumber = Math.floor(randomNumber);
              var messageE1 = document.getElementById("message")

              document.getElementById("guess").value =" ";
              messageE1.textContent = "New number generated! & Try again"
            }

        </script>
    </body>
</html>
              
