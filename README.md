# announcement

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>🎂 A Birthday Surprise!</title>

<style>

* {
    box-sizing: border-box;
}

body {
    margin: 0;
    min-height: 100vh;
    overflow: hidden;
    font-family: Arial, sans-serif;
    background:
        linear-gradient(
            135deg,
            #ff9a9e,
            #fad0c4,
            #fbc2eb,
            #a6c1ee,
            #84fab0
        );
    background-size: 400% 400%;
    animation: backgroundMove 12s ease infinite;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #4b3b52;
}

.container {
    width: min(92%, 700px);
    text-align: center;
    position: relative;
    z-index: 5;
}

#loading {
    font-family: monospace;
    font-size: 17px;
}

#loadingText {
    margin-bottom: 18px;
}

.progress {
    width: 100%;
    height: 14px;
    background: rgba(255,255,255,.65);
    border-radius: 20px;
    overflow: hidden;
}

.progressBar {
    width: 0%;
    height: 100%;
    background: linear-gradient(
        90deg,
        #ff4ecd,
        #7c4dff,
        #00d4ff,
        #00e676
    );
    border-radius: 20px;
    transition: width .15s;
}

#birthday {
    display: none;
    animation: appear 1.5s ease;
}

.emoji {
    font-size: 65px;
    animation: bounce 1.5s infinite;
}

h1 {
    font-size: clamp(40px, 10vw, 78px);
    margin: 10px 0;
    background: linear-gradient(
        90deg,
        #ff1493,
        #7b2cff,
        #0099ff,
        #00b894,
        #ff1493
    );
    background-size: 300%;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    animation: rainbowText 5s linear infinite;
}

.subtitle {
    font-size: 21px;
    line-height: 1.6;
}

.card {
    margin-top: 28px;
    padding: 28px;
    border-radius: 30px;
    background: rgba(255,255,255,.72);
    backdrop-filter: blur(8px);
    box-shadow:
        0 15px 50px rgba(80,50,100,.2);
}

.message {
    margin: 13px 0;
    font-size: 17px;
}

.highlight {
    margin-top: 22px;
    font-size: 23px;
    font-weight: bold;
    color: #e84393;
}

.cake {
    margin-top: 28px;
    font-size: 75px;
    animation: cakeBounce 2s infinite;
}

.small {
    margin-top: 20px;
    font-size: 14px;
    opacity: .75;
}

#confetti,
#balloons {
    position: fixed;
    inset: 0;
    pointer-events: none;
    overflow: hidden;
}

.confetti {
    position: absolute;
    top: -20px;
    width: 10px;
    height: 16px;
    animation: fall linear forwards;
}

.balloon {
    position: absolute;
    bottom: -100px;
    font-size: 45px;
    animation: balloonRise linear forwards;
}

/* Animations */

@keyframes backgroundMove {

    0% {
        background-position: 0% 50%;
    }

    50% {
        background-position: 100% 50%;
    }

    100% {
        background-position: 0% 50%;
    }

}

@keyframes appear {

    from {
        opacity: 0;
        transform: scale(.8) translateY(30px);
    }

    to {
        opacity: 1;
        transform: scale(1) translateY(0);
    }

}

@keyframes bounce {

    0%,100% {
        transform: translateY(0);
    }

    50% {
        transform: translateY(-12px);
    }

}

@keyframes cakeBounce {

    0%,100% {
        transform: translateY(0) rotate(0deg);
    }

    50% {
        transform: translateY(-8px) rotate(2deg);
    }

}

@keyframes rainbowText {

    0% {
        background-position: 0%;
    }

    100% {
        background-position: 300%;
    }

}

@keyframes fall {

    from {
        transform: translateY(0) rotate(0deg);
        opacity: 1;
    }

    to {
        transform: translateY(110vh) rotate(720deg);
        opacity: 0;
    }

}

@keyframes balloonRise {

    from {
        transform: translateY(0) rotate(-5deg);
        opacity: 0;
    }

    15% {
        opacity: 1;
    }

    to {
        transform: translateY(-120vh) rotate(10deg);
        opacity: 0;
    }

}

</style>
</head>

<body>

<div id="confetti"></div>
<div id="balloons"></div>

<div class="container">

    <div id="loading">

        <div id="loadingText">
            Preparing birthday surprise...
        </div>

        <div class="progress">
            <div
                class="progressBar"
                id="bar">
            </div>
        </div>

    </div>


    <div id="birthday">

        <div class="emoji">
            🎉
        </div>

        <div style="
            font-size:14px;
            letter-spacing:4px;
            font-weight:bold;
        ">
            OFFICIAL BIRTHDAY ANNOUNCEMENT
        </div>

        <h1>
            HAPPY BIRTHDAY! 🎂
        </h1>

        <div class="subtitle">
            Today is officially your day. 💖
        </div>


        <div class="card">

            <div class="message">
                🎈 May your day be filled with laughter.
            </div>

            <div class="message">
                ✨ May good things find you unexpectedly.
            </div>

            <div class="message">
                🌷 May you have more reasons to smile this year.
            </div>

            <div class="message">
                💫 May your dreams slowly become reality.
            </div>

            <div class="message">
                🥰 And may you always remember how loved you are.
            </div>

            <div class="highlight">
                Another year older.
                <br>
                Another year of being wonderfully you. 💗
            </div>

        </div>


        <div class="cake">
            🎂
        </div>

        <div class="highlight">
            Make a wish! 🌟
        </div>

        <div class="small">
            Warning: excessive happiness may occur. 😂
        </div>

    </div>

</div>


<script>

const bar =
    document.getElementById("bar");

const loadingText =
    document.getElementById("loadingText");

const loading =
    document.getElementById("loading");

const birthday =
    document.getElementById("birthday");


const messages = [

    "Preparing birthday surprise...",

    "Inflating virtual balloons...",

    "Collecting confetti...",

    "Baking digital cake...",

    "Lighting imaginary candles...",

    "Downloading happiness...",

    "Calculating birthday vibes...",

    "Preparing maximum celebration...",

    "Almost ready... 🎉"

];


let progress = 0;


const timer = setInterval(() => {

    progress += 2;

    bar.style.width =
        progress + "%";


    const index =
        Math.min(
            Math.floor(progress / 12),
            messages.length - 1
        );


    loadingText.innerText =
        messages[index];


    if (progress >= 100) {

        clearInterval(timer);

        setTimeout(() => {

            loading.style.display =
                "none";

            birthday.style.display =
                "block";

            startConfetti();
            startBalloons();

        }, 700);

    }

}, 70);



function startConfetti() {

    setInterval(() => {

        const piece =
            document.createElement("div");

        piece.className =
            "confetti";

        piece.style.left =
            Math.random() * 100 + "%";

        piece.style.width =
            (5 + Math.random() * 9) + "px";

        piece.style.height =
            (8 + Math.random() * 14) + "px";

        piece.style.background =
            [
                "#ff4ecd",
                "#7c4dff",
                "#00d4ff",
                "#00e676",
                "#ffd32a",
                "#ff6b6b"
            ][
                Math.floor(
                    Math.random() * 6
                )
            ];

        piece.style.animationDuration =
            (3 + Math.random() * 4) + "s";

        document
            .getElementById("confetti")
            .appendChild(piece);


        setTimeout(() => {
            piece.remove();
        }, 7000);

    }, 100);

}



function startBalloons() {

    setInterval(() => {

        const balloon =
            document.createElement("div");

        balloon.className =
            "balloon";

        balloon.innerText =
            [
                "🎈",
                "🎈",
                "🎈",
                "💖",
                "🌈"
            ][
                Math.floor(
                    Math.random() * 5
                )
            ];

        balloon.style.left =
            Math.random() * 100 + "%";

        balloon.style.animationDuration =
            (7 + Math.random() * 6) + "s";

        document
            .getElementById("balloons")
            .appendChild(balloon);


        setTimeout(() => {
            balloon.remove();
        }, 13000);

    }, 900);

}

</script>

</body>
</html>
