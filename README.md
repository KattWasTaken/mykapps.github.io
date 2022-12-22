
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>MyKapps</title>
        <style>
            body{
              margin: 0;
              padding: 0;
              font-family: sans-serif;
            }
            main{
              margin: 5vh 15%;
            }
            h1{
              font-size: 40px;
              font-weight: 400;
              text-align: center;
            }
            img{
              width:50%;
              height:auto;
            }
            p{
              font-size: 18px;
            }
            label{
                position: absolute;
                width: 45px;
                height: 22px;
                right: 20px;
                top: 20px;
                border: 2px solid;
                border-radius: 20px;
            }
            label:before{
                position: absolute;
                content: '';
                width:20px;
                height: 20px;
                left: 1px;
                top: 1px;
                border-radius: 50%;
                background: #000;
                cursor: pointer;
                transition: 0.4s;
            }
            label.active:before{
                left: 24px;
                background: #fff;
            }
            body.night{
                background: #000;
                color: #fff;
            }
            @media screen and (min-width:900px) {
              .respon{
                display: flex;
              }
              img{
                height:50%;
                width:auto;
                padding-top: 3vh;
                padding-right: 5%;
              }
              p{
                max-width: 100%;
              }
            }
        </style>
    </head>
    <body>
        <header>
            <label id="dark-change"></label>
        </header>
        <main>
            <h1>Welcome to mykapps.</h1>
            <p style="text-align: center">See that switch at the top of the page? If you click it you can enable dark mode.</p>
            <div id="respond">
            </div>
        </main>
        <script>
        var content = document.getElementsByTagName('body')[0];
        var darkMode = document.getElementById('dark-change');
        darkMode.addEventListener('click', function(){
            darkMode.classList.toggle('active');
            content.classList.toggle('night');
        })
        </script>
    </body>
</html>
