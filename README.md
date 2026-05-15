<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Birthday Card</title>

<style>
    body{
        margin:0;
        height:100vh;
        display:flex;
        justify-content:center;
        align-items:center;
        background:#dff6ff;
        font-family:Arial, sans-serif;
        overflow:hidden;
    }

    .card-container{
        perspective:1200px;
    }

    .card{
        width:320px;
        height:420px;
        position:relative;
        transform-style:preserve-3d;
        transition:transform 1s;
        cursor:pointer;
    }

    .card.open{
        transform:rotateY(-180deg);
    }

    .front, .inside{
        position:absolute;
        width:100%;
        height:100%;
        border-radius:20px;
        backface-visibility:hidden;
        box-shadow:0 10px 25px rgba(0,0,0,0.2);
    }

    .front{
        background:#9edcff;
        display:flex;
        flex-direction:column;
        justify-content:center;
        align-items:center;
        color:white;
    }

    .front h1{
        font-size:32px;
        margin:0;
    }

    .front p{
        margin-top:10px;
        font-size:18px;
    }

    .inside{
        background:#cfefff;
        transform:rotateY(180deg);
        padding:30px;
        box-sizing:border-box;
        color:#3b4d61;
        display:flex;
        flex-direction:column;
        justify-content:center;
        text-align:center;
    }

    .inside h2{
        font-size:28px;
        margin-bottom:20px;
    }

    .inside p{
        font-size:18px;
        line-height:1.6;
    }

    .heart{
        font-size:40px;
        margin-top:20px;
    }
</style>
</head>

<body>

<div class="card-container">
    <div class="card" id="birthdayCard">

        <!-- Front -->
        <div class="front">
            <h1>Happy Birthday 🎂</h1>
            <p>Click to open</p>
        </div>

        <!-- Inside -->
        <div class="inside">
            <h2>To Someone Special 💙</h2>

            <p>
                Wishing you endless happiness,  
                beautiful memories, and lots of smiles today.  
                May your year be filled with love, peace, and success.
            </p>

            <div class="heart">🩵</div>
        </div>

    </div>
</div>

<script>
    const card = document.getElementById("birthdayCard");

    card.addEventListener("click", () => {
        card.classList.toggle("open");
    });
</script>

</body>
</html>
