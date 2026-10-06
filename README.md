```html
<!DOCTYPE html>
<html lang="ar" dir="rtl">

<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Her şeyim ❤️</title>

<style>

*{
    box-sizing:border-box;
    margin:0;
    padding:0;
}

html,
body{
    width:100%;
    height:100%;
}

body{
    overflow:hidden;
    font-family:Arial,Tahoma,sans-serif;
    color:white;

    background:
        radial-gradient(
            circle at center,
            #351322 0%,
            #160811 45%,
            #050205 100%
        );
}


/* =========================
   المشاهد
========================= */

.scene{
    position:fixed;
    inset:0;

    width:100%;
    height:100%;

    display:none;

    align-items:center;
    justify-content:center;

    padding:25px;

    text-align:center;

    opacity:0;

    z-index:10;
}

.scene.active{
    display:flex;

    opacity:1;

    animation:
        sceneIn
        .7s
        ease
        forwards;
}

@keyframes sceneIn{

    from{
        opacity:0;

        transform:
            scale(.96)
            translateY(20px);
    }

    to{
        opacity:1;

        transform:
            scale(1)
            translateY(0);
    }
}


/* =========================
   المحتوى
========================= */

.content{
    width:min(700px,92vw);

    position:relative;

    z-index:100;
}


/* =========================
   القلب الصغير
========================= */

.small-heart{

    font-size:75px;

    color:#ff3f78;

    margin-bottom:15px;

    animation:
        beat
        1.4s
        infinite;

    text-shadow:
        0 0 15px #ff3f78,
        0 0 40px #ff3f78;
}


/* =========================
   العناوين
========================= */

h1{

    font-size:
        clamp(45px,10vw,90px);

    margin-bottom:20px;

    text-shadow:
        0 0 15px #ff3f78,
        0 0 40px
        rgba(255,63,120,.5);
}

h1 span{
    color:#ff3f78;
}

h2{

    font-size:
        clamp(27px,6vw,48px);

    line-height:1.5;

    margin-bottom:20px;
}

p{

    color:#ead0d9;

    font-size:19px;

    line-height:2;
}


/* =========================
   الأزرار
========================= */

.main-button,
.second-button{

    position:relative;

    z-index:200;

    border:none;

    border-radius:50px;

    padding:
        15px 30px;

    margin-top:30px;

    font-size:18px;

    font-family:inherit;

    cursor:pointer;

    pointer-events:auto;

    touch-action:manipulation;

    transition:
        .3s ease;
}


.main-button{

    color:white;

    background:
        linear-gradient(
            135deg,
            #ff5687,
            #ff174f
        );

    box-shadow:
        0 10px 30px
        rgba(255,23,79,.35);
}


.main-button:hover{

    transform:
        translateY(-4px)
        scale(1.04);

    box-shadow:
        0 15px 40px
        rgba(255,23,79,.6);
}


.second-button{

    color:white;

    background:
        rgba(255,255,255,.08);

    border:
        1px solid
        rgba(255,255,255,.2);
}


.second-button:hover{

    background:
        rgba(255,255,255,.16);
}


.buttons{

    display:flex;

    justify-content:center;

    align-items:center;

    gap:15px;

    flex-wrap:wrap;
}


/* =========================
   المشهد الثاني
========================= */

.number{

    color:#ff5687;

    font-size:14px;

    letter-spacing:6px;

    margin-bottom:15px;
}

#noMessage{

    min-height:40px;

    color:#ff9ab7;
}


/* =========================
   المشهد الثالث
========================= */

#wordCloud{

    position:fixed;

    inset:0;

    overflow:hidden;

    pointer-events:none;

    z-index:1;
}


.word{

    position:absolute;

    color:
        rgba(255,120,160,.65);

    white-space:nowrap;

    pointer-events:none;

    animation:
        wordFloat
        6s
        ease-in-out
        infinite;
}


.center-box{

    padding:40px 25px;

    border-radius:30px;

    background:
        rgba(8,2,6,.5);

    backdrop-filter:
        blur(8px);

    border:
        1px solid
        rgba(255,80,130,.12);

    z-index:100;
}


.glowing-heart{

    font-size:70px;

    color:#ff3f78;

    animation:
        beat
        1.4s
        infinite;

    text-shadow:
        0 0 20px #ff3f78,
        0 0 50px #ff3f78;
}


/* =========================
   المشهد الرابع
========================= */

.big-question{

    font-size:
        clamp(25px,6vw,42px);

    color:white;

    margin:20px 0;
}


/* =========================
   الرسالة
========================= */

.envelope{

    font-size:60px;

    margin-bottom:15px;
}


.letter{

    max-width:600px;

    min-height:220px;

    margin:
        20px auto;

    padding:25px;

    border-radius:20px;

    background:
        rgba(255,255,255,.05);

    border:
        1px solid
        rgba(255,80,130,.2);
}


#typedMessage{

    white-space:
        pre-line;

    color:#f7dfe7;

    font-size:18px;

    line-height:2;
}


.cursor{

    color:#ff477d;

    animation:
        blink
        .7s
        infinite;
}


/* =========================
   النهاية
========================= */

.big-heart{

    position:relative;

    z-index:200;

    border:none;

    background:transparent;

    font-size:120px;

    cursor:pointer;

    pointer-events:auto;

    touch-action:manipulation;

    margin:25px;

    animation:
        beat
        1.2s
        infinite;

    filter:
        drop-shadow(
            0 0 15px #ff477d
        )
        drop-shadow(
            0 0 45px #ff477d
        );

    transition:.3s;
}


.big-heart:hover{

    transform:
        scale(1.15);
}


.click-text{

    opacity:.6;

    font-size:14px;
}


#finalMessage{

    display:none;

    animation:
        finalIn
        1.2s
        ease
        forwards;
}


#finalMessage h1{

    font-size:
        clamp(45px,10vw,85px);
}


.infinity{

    color:#ff477d;

    font-size:70px;

    margin-top:15px;
}


/* =========================
   النقاط
========================= */

.progress{

    position:fixed;

    bottom:25px;

    left:50%;

    transform:
        translateX(-50%);

    display:flex;

    gap:8px;

    z-index:1000;

    pointer-events:none;
}


.dot{

    width:8px;
    height:8px;

    border-radius:50%;

    background:
        rgba(255,255,255,.25);

    transition:.3s;
}


.dot.active{

    width:25px;

    border-radius:10px;

    background:#ff477d;
}


/* =========================
   قلوب الخلفية
========================= */

.bg-heart{

    position:fixed;

    bottom:-50px;

    color:
        rgba(255,70,120,.12);

    font-size:25px;

    pointer-events:none;

    z-index:0;

    animation:
        rise
        linear
        infinite;
}


/* =========================
   زر الاختبار
========================= */

#testButton{

    position:fixed;

    top:10px;

    left:10px;

    z-index:99999;

    border:1px solid
        rgba(255,255,255,.2);

    border-radius:20px;

    padding:6px 10px;

    color:#fff;

    background:
        rgba(0,0,0,.45);

    font-size:11px;

    cursor:pointer;

    opacity:.5;
}

#testButton:hover{
    opacity:1;
}


/* =========================
   الحركات
========================= */

@keyframes beat{

    0%,100%{
        transform:scale(1);
    }

    50%{
        transform:scale(1.12);
    }
}


@keyframes blink{

    50%{
        opacity:0;
    }
}


@keyframes wordFloat{

    0%,100%{

        transform:
            translateY(0);

        opacity:.3;
    }

    50%{

        transform:
            translateY(-25px);

        opacity:.9;
    }
}


@keyframes rise{

    from{

        transform:
            translateY(0)
            rotate(0deg);

        opacity:0;
    }

    20%{
        opacity:1;
    }

    to{

        transform:
            translateY(-120vh)
            rotate(30deg);

        opacity:0;
    }
}


@keyframes finalIn{

    from{

        opacity:0;

        transform:
            scale(.5);
    }

    to{

        opacity:1;

        transform:
            scale(1);
    }
}


/* =========================
   الهاتف
========================= */

@media(max-width:600px){

    .content{
        width:94vw;
    }

    h2{
        font-size:27px;
    }

    p{
        font-size:16px;
    }

    .main-button,
    .second-button{

        font-size:16px;

        padding:
            13px 23px;
    }

    .letter{

        max-height:310px;

        overflow-y:auto;
    }

    #typedMessage{
        font-size:17px;
    }

    .big-heart{
        font-size:100px;
    }
}

</style>
</head>


<body>


<!-- =========================
     المشهد الأول
========================= -->

<section
    class="scene active"
    id="scene1">

    <div class="content">

        <div class="small-heart">
            ♡
        </div>

        <h1>
            Her şeyim
            <span>❤️</span>
        </h1>

        <p>
            في حاجة صغيرة عايزة أقولها ليك...
        </p>

        <button
            type="button"
            class="main-button"
            id="startButton"
            onclick="goToScene(1)">

            اضغطي هنا ♡

        </button>

    </div>

</section>


<!-- =========================
     المشهد الثاني
========================= -->

<section
    class="scene"
    id="scene2">

    <div class="content">

        <div class="number">
            02
        </div>

        <h2>
            عارفة إنتِ بالنسبة لي شنو؟ 👀
        </h2>

        <p id="noMessage">
            فكري كويس قبل ما تجاوبي...
        </p>

        <div class="buttons">

            <button
                type="button"
                class="main-button"
                onclick="goToScene(2)">

                أكيد ❤️

            </button>

            <button
                type="button"
                class="second-button"
                id="noButton"
                onclick="goToScene(2)"
                onmouseenter="moveNoButton()">

                ما عارفة

            </button>

        </div>

    </div>

</section>


<!-- =========================
     المشهد الثالث
========================= -->

<section
    class="scene"
    id="scene3">

    <div id="wordCloud"></div>

    <div class="content center-box">

        <div class="glowing-heart">
            ♥
        </div>

        <h2>
            Her şeyim.
        </h2>

        <p>
            كل شيء جميل في أيامي ❤️
        </p>

        <button
            type="button"
            class="main-button"
            onclick="goToScene(3)">

            كملي... ✨

        </button>

    </div>

</section>


<!-- =========================
     المشهد الرابع
========================= -->

<section
    class="scene"
    id="scene4">

    <div class="content">

        <div class="number">
            04
        </div>

        <h2>
            لو رجع بي الزمن...
        </h2>

        <p class="big-question">
            حتفتكريني أختارك تاني؟
        </p>

        <div class="buttons">

            <button
                type="button"
                class="main-button"
                onclick="goToScene(4)">

                أختارك كل مرة ❤️

            </button>

            <button
                type="button"
                class="second-button"
                onclick="goToScene(4)">

                أكيد ❤️

            </button>

        </div>

    </div>

</section>


<!-- =========================
     المشهد الخامس
========================= -->

<section
    class="scene"
    id="scene5">

    <div class="content">

        <div class="envelope">
            💌
        </div>

        <h2>
            إلى أعز إنسانة عندي...
        </h2>

        <div class="letter">

            <span id="typedMessage"></span>

            <span class="cursor">
                |
            </span>

        </div>

        <button
            type="button"
            class="main-button"
            onclick="goToScene(5)">

            كملي الرسالة 💌

        </button>

    </div>

</section>


<!-- =========================
     المشهد السادس
========================= -->

<section
    class="scene"
    id="scene6">

    <div class="content">

        <p>
            عندي مفاجأة صغيرة ليك...
        </p>

        <button
            type="button"
            class="big-heart"
            id="bigHeart"
            onclick="finishLove()">

            ❤️

        </button>

        <p
            class="click-text"
            id="clickText">

            اضغطي على القلب

        </p>

        <div id="finalMessage">

            <h1>
                Her şeyim ❤️
            </h1>

            <p>
                أحبك أكثر مما تستطيع الكلمات أن تقول.
            </p>

            <div class="infinity">
                ∞
            </div>

        </div>

    </div>

</section>


<!-- =========================
     النقاط
========================= -->

<div class="progress">

    <span class="dot active"></span>
    <span class="dot"></span>
    <span class="dot"></span>
    <span class="dot"></span>
    <span class="dot"></span>
    <span class="dot"></span>

</div>


<!-- =========================
     زر اختبار
========================= -->

<button
    id="testButton"
    type="button"
    onclick="runTest()">

    اختبار

</button>


<script>

/* =====================================================
   النظام الرئيسي
===================================================== */

var scenes =
    document.querySelectorAll(".scene");

var dots =
    document.querySelectorAll(".dot");

var currentScene = 0;


/* =====================================================
   الانتقال بين المشاهد
===================================================== */

function goToScene(number){

    if(
        number < 0 ||
        number >= scenes.length
    ){
        return;
    }

    for(
        var i = 0;
        i < scenes.length;
        i++
    ){

        scenes[i].classList.remove("active");

    }

    scenes[number].classList.add("active");


    for(
        var j = 0;
        j < dots.length;
        j++
    ){

        dots[j].classList.remove("active");

    }

    if(dots[number]){
        dots[number].classList.add("active");
    }


    currentScene = number;


    if(number === 2){
        createWords();
    }


    if(number === 4){
        startTyping();
    }
}


/* =====================================================
   الانتقال التالي
===================================================== */

function nextScene(){

    if(
        currentScene <
        scenes.length - 1
    ){

        goToScene(
            currentScene + 1
        );

    }
}


/* =====================================================
   زر "ما عارفة"
===================================================== */

var noCount = 0;


function moveNoButton(){

    var button =
        document.getElementById("noButton");

    var message =
        document.getElementById("noMessage");


    noCount++;


    if(noCount <= 5){

        var x =
            Math.random() * 160 - 80;

        var y =
            Math.random() * 100 - 50;


        button.style.transform =
            "translate(" +
            x +
            "px," +
            y +
            "px";


        var messages = [

            "لااا 😂",

            "جربي تاني ❤️",

            "ما بتمشي كدا 😭",

            "إنتِ عارفة طبعاً...",

            "خلاص ما عندك مهرب 😂❤️"

        ];


        message.textContent =
            messages[
                noCount - 1
            ];

    }

    else{

        button.style.transform =
            "translate(0,0)";

        button.textContent =
            "خلاص عارفة ❤️";

        message.textContent =
            "أهو عرفتي 😌❤️";
    }
}


/* =====================================================
   كلمات الحب
===================================================== */

var wordCloud =
    document.getElementById(
        "wordCloud"
    );


var loveWords = [

    "Her şeyim",

    "I love you",

    "Forever",

    "Always",

    "My love",

    "My person",

    "Canım",

    "Love",

    "For you",

    "Always you",

    "Sweetheart",

    "Forever us",

    "أحبك",

    "أعز الناس",

    "دائماً",

    "معاك",

    "إنتِ",

    "♡",

    "❤"

];


var wordsCreated = false;


function createWords(){

    if(
        wordsCreated ||
        !wordCloud
    ){
        return;
    }


    wordsCreated = true;


    for(
        var i = 0;
        i < 55;
        i++
    ){

        var word =
            document.createElement(
                "span"
            );


        word.className =
            "word";


        word.textContent =
            loveWords[
                Math.floor(
                    Math.random() *
                    loveWords.length
                )
            ];


        word.style.left =
            Math.random() * 92 +
            "%";


        word.style.top =
            Math.random() * 90 +
            "%";


        word.style.fontSize =
            10 +
            Math.random() * 15 +
            "px";


        word.style.animationDelay =
            Math.random() * 4 +
            "s";


        wordCloud.appendChild(
            word
        );
    }
}


/* =====================================================
   الرسالة
===================================================== */

var typedMessage =
    document.getElementById(
        "typedMessage"
    );


var loveLetter =
`ما عارفة كيف أشرح ليك مكانتك عندي،
لكن عارفة إن وجودك في حياتي
من الحاجات البتخلي الأيام أحلى.

يمكن الكلام ما يكفي،
ويمكن مهما كتبت ما أقدر أوصف
كل الحاجات البتعنيها لي.

بس في حاجة واحدة متأكدة منها...

إنتِ من أجمل الحاجات الحصلت لي. ❤️`;


var typingStarted = false;


function startTyping(){

    if(
        typingStarted ||
        !typedMessage
    ){
        return;
    }


    typingStarted = true;


    var index = 0;


    function typeCharacter(){

        if(
            index <
            loveLetter.length
        ){

            typedMessage.textContent +=
                loveLetter[index];

            index++;


            setTimeout(
                typeCharacter,
                35
            );
        }
    }


    typeCharacter();
}


/* =====================================================
   النهاية
===================================================== */

function finishLove(){

    var bigHeart =
        document.getElementById(
            "bigHeart"
        );


    var clickText =
        document.getElementById(
            "clickText"
        );


    var finalMessage =
        document.getElementById(
            "finalMessage"
        );


    bigHeart.style.display =
        "none";


    clickText.style.display =
        "none";


    finalMessage.style.display =
        "block";


    explodeHearts();
}


/* =====================================================
   انفجار القلوب
===================================================== */

function explodeHearts(){

    var symbols = [
        "❤",
        "♡",
        "♥",
        "✦"
    ];


    for(
        var i = 0;
        i < 50;
        i++
    ){

        var heart =
            document.createElement(
                "div"
            );


        heart.textContent =
            symbols[
                Math.floor(
                    Math.random() *
                    symbols.length
                )
            ];


        heart.style.position =
            "fixed";


        heart.style.left =
            "50%";


        heart.style.top =
            "50%";


        heart.style.zIndex =
            "9999";


        heart.style.pointerEvents =
            "none";


        heart.style.color =
            "#ff477d";


        heart.style.fontSize =
            15 +
            Math.random() * 25 +
            "px";


        document.body.appendChild(
            heart
        );


        var x =
            (Math.random() * 2 - 1) *
            45;


        var y =
            (Math.random() * 2 - 1) *
            45;


        var animation =
            heart.animate(

                [

                    {
                        transform:
                            "translate(-50%,-50%) scale(.2)",

                        opacity:1
                    },

                    {

                        transform:
                            "translate(" +
                            "calc(-50% + " +
                            x +
                            "vw)," +
                            "calc(-50% + " +
                            y +
                            "vh)) scale(1.5)",

                        opacity:0
                    }

                ],

                {

                    duration:
                        900 +
                        Math.random() *
                        900,

                    easing:
                        "ease-out"

                }
            );


        animation.onfinish =
            function(){

                heart.remove();

            };
    }
}


/* =====================================================
   قلوب الخلفية
===================================================== */

function createBackgroundHearts(){

    for(
        var i = 0;
        i < 25;
        i++
    ){

        var heart =
            document.createElement(
                "div"
            );


        heart.className =
            "bg-heart";


        heart.textContent =
            Math.random() > .5
            ? "♡"
            : "♥";


        heart.style.left =
            Math.random() * 100 +
            "%";


        heart.style.fontSize =
            12 +
            Math.random() * 25 +
            "px";


        heart.style.animationDuration =
            8 +
            Math.random() * 12 +
            "s";


        heart.style.animationDelay =
            -(Math.random() * 15) +
            "s";


        document.body.appendChild(
            heart
        );
    }
}


/* =====================================================
   اختبار النظام
===================================================== */

function runTest(){

    var message =
        document.createElement(
            "div"
        );


    message.textContent =
        "✓ الأزرار و JavaScript يعملان";


    message.style.position =
        "fixed";


    message.style.top =
        "50%";


    message.style.left =
        "50%";


    message.style.transform =
        "translate(-50%,-50%)";


    message.style.zIndex =
        "999999";


    message.style.padding =
        "20px 30px";


    message.style.borderRadius =
        "20px";


    message.style.background =
        "#ff477d";


    message.style.color =
        "white";


    message.style.fontSize =
        "18px";


    message.style.boxShadow =
        "0 10px 40px rgba(0,0,0,.5)";


    document.body.appendChild(
        message
    );


    setTimeout(
        function(){

            message.remove();

        },
        1800
    );
}


/* =====================================================
   التشغيل الأول
===================================================== */

createBackgroundHearts();

goToScene(0);

</script>

</body>
</html>
```
