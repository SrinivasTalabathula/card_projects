<!DOCTYPE html>
<html>
    <head>
        <title>Glassmorphism</title>
        <style>
            *{
                font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
                margin:0;
                padding:0;
                box-sizing: border-box;
            }
            body{
                display:flex;
                justify-content:center;
                align-items:center;
                min-height:100vh;/*vh=viewport height*/
                background-color: #161623;
            }
            body::before
            {
                content: '';
                position:absolute;
                top:0;
                left:0;
                width:100%;/*covers the whole -page*/ 
                height:100%;
                background: linear-gradient(#f00,#f0f);
                clip-path: circle(30% at right 70%);
            }
            body::after
            {
                content: '';
                position:absolute;
                top:0;
                left:0;
                width:100%;/*covers the whole -page*/ 
                height:100%;
                background:linear-gradient(#2196f3,#e91e63);
                clip-path: circle(20% at 10% 10%);
            }
            .container{
                position: relative;
                display:flex;
                justify-content: center;
                align-items:center;
                max-width:1200px;
                flex-wrap: wrap;
                z-index: 1;
            }
            .container .card{
                position: relative;
                width: 280px;
                height: 400px;
                margin:30px;
                box-shadow: 20px 20px 50px rgba(0,0,0,0.5);
                border-radius: 30px;
                background: rgba(255,255,255,0.1);
                overflow:hidden;
                align-items:center;
                display:flex;
                justify-content:center;
                border-top: 1px solid rgba(255,255,255,0.1);
                border-left: 1px solid rgba(255,255,255,0.1);
            }
            .container .card .content{
                padding: 20px;
                text-align:center;
                transform:translateY(100px);
                opacity: 0;
                transition: 0.5s;
            }
            .container .card:hover .content{
                transform: translateY(opx);
                opacity: 1;
            }
            .container .card .content h2{
                position:absolute;
                top: -20px;
                right: 10px;
                font-size: 8em;
                color: rgba(255,255,255,0.05);
                pointer-events: none;
            }
            .container .card .content h3{
                font-size: 1.8em;
                color:aliceblue;
                z-index:1;
            }
            .container .card .content p{
                font-size:1em;
                color:aliceblue;
                font-weight: 300;
            }
            .container .card .content a{
                position:relative;
                display:inline-block;
                padding: 8px 20px;
                margin-top: 15px;
                background: #fff;
                color: #000;
                border-radius: 20px;
                font-weight:500;
                box-shadow: 0 5px 15px rgba(0,0,0,0.5);
            }
            
        </style>
    </head>
    <body>
        <div class="container">
        <div class="card">
        <div class="content">
            <h2>01</h2>
            <h3>Google</h3>
            <p>Here you will find the google browser you can search your content
                you will find the google browser in this card
            </p>
            <a href="https://www.google.com/">Read More</a>
        </div>
        </div>
        <div class="card">
            <div class="content">
                <h2>02</h2>
                <h3>Youtube</h3>
                <p>Here you will find the youtube you can search your content
                    you will find the youtube content in this card</p>
                <a href="https://www.youtube.com/">Read More</a>
            </div>
            </div>
            <div class="card">
                <div class="content">
                    <h2>03</h2>
                    <h3>Github</h3>
                    <p>where you can browse required codes
                        you'll find different types of code while you click in this card </p>
                    <a href="https://github.com/">Read More</a>
                </div>
                </div>
        </div>
    </body>
</html>
