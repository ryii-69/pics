
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Do You Like Me? ❤️</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, sans-serif;
}

body{
    display:flex;
    justify-content:center;
    align-items:center;
    min-height:100vh;
    background:#ffe6f0;
    overflow:hidden;
}

.wrapper{
    text-align:center;
}

.question{
    color:#ff4d88;
    margin-bottom:20px;
}

.gif{
    width:250px;
    height:auto;
    margin-bottom:20px;
}

.btn-group{
    display:flex;
    justify-content:center;
    align-items:center;
    gap:20px;
    margin-top:20px;
}

button{
    padding:10px 25px;
    font-size:18px;
    border:none;
    border-radius:10px;
    cursor:pointer;
    transition:0.3s;
}

.yes-btn{
    background:#ff66b3;
    color:white;
}

.no-btn{
    background:#808080;
    color:white;
}
</style>
</head>
<body>

<div class="wrapper">

    <h2 class="question">Do you like me? ❤️</h2>

    <img class="gif"
    src="https://raw.githubusercontent.com/ryii-69/pics/7fa096dd795151815b4e1662a0b99df09db08962/cutie.gif"
    alt="cat">

    <div class="btn-group">
        <button class="yes-btn">Yes </button>
        <button class="no-btn">No </button>
    </div>

</div>

<script>
const yesBtn = document.querySelector(".yes-btn");
const noBtn = document.querySelector(".no-btn");
const question = document.querySelector(".question");
const gif = document.querySelector(".gif");

let noCount = 0;
let yesSize = 18;

yesBtn.addEventListener("click", () => {

    gif.src = "https://raw.githubusercontent.com/ryii-69/pics/7fa096dd795151815b4e1662a0b99df09db08962/blushing%20cat.gif";

    question.innerHTML = "Yay!! I knew it! ❤️🥰";

    yesBtn.style.display = "none";
    noBtn.style.display = "none";
});

noBtn.addEventListener("click", () => {

    noCount++;
    yesSize += 10;

    // Palakihin ang Yes button
    yesBtn.style.fontSize = yesSize + "px";
    yesBtn.style.padding =
        (10 + noCount * 5) + "px " +
        (25 + noCount * 10) + "px";

    // Gawing absolute ang No button para makagalaw
    noBtn.style.position = "absolute";

    // Random position sa screen
    let x = Math.random() * (window.innerWidth - 120);
    let y = Math.random() * (window.innerHeight - 60);

    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";

    // Palitan ang GIF at message
    if (noCount == 1) {

        gif.src = "https://raw.githubusercontent.com/ryii-69/pics/7fa096dd795151815b4e1662a0b99df09db08962/crying%20cat.gif";

        question.innerHTML = "Please think again...";
    }

    else if (noCount == 2) {

        gif.src = "https://raw.githubusercontent.com/ryii-69/pics/7fa096dd795151815b4e1662a0b99df09db08962/sulking%20cat.gif";

        question.innerHTML = "Are you sure about your decision?";
    }

    else if (noCount == 3) {

        gif.src = "https://raw.githubusercontent.com/ryii-69/pics/7fa096dd795151815b4e1662a0b99df09db08962/mad%20cat.gif";

        question.innerHTML = "Are you sure sure? think again";
    }

    else if (noCount >= 4) {

        gif.src = "https://raw.githubusercontent.com/ryii-69/pics/7fa096dd795151815b4e1662a0b99df09db08962/cat%20with%20g.gif";

        question.innerHTML = "GRRRR!! Last chance! Do you like me now?";
    }

});
</script>

</body>
</html>
