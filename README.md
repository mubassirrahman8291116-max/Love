DOCTYPE html>
<html lang="bn">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For You ❤️</title>

<style>
*{box-sizing:border-box}

body{
    margin:0;
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    font-family:"Segoe UI",sans-serif;
    background:linear-gradient(135deg,#ff758c,#ff7eb3,#8e2de2);
    overflow:hidden;
}

.box{
    width:90%;
    max-width:420px;
    background:rgba(255,255,255,.15);
    backdrop-filter:blur(15px);
    border:1px solid rgba(255,255,255,.3);
    border-radius:25px;
    padding:30px;
    text-align:center;
    color:white;
    box-shadow:0 15px 40px rgba(0,0,0,.25);
}

h1{
    margin-bottom:10px;
    font-weight:600;
}

p{
    font-size:15px;
    opacity:.95;
}

input{
    width:100%;
    padding:14px;
    border:none;
    outline:none;
    border-radius:15px;
    margin:15px 0;
    text-align:center;
    font-size:16px;
}

button{
    border:none;
    padding:13px 30px;
    border-radius:25px;
    background:white;
    color:#e91e63;
    font-weight:600;
    font-size:16px;
    cursor:pointer;
    transition:.3s ease;
}

button:hover{
    transform:scale(1.05);
}

#letter{
    display:none;
    animation:openLetter 1.2s ease;
}

.letter{
    background:rgba(255,255,255,.95);
    color:#444;
    padding:25px;
    border-radius:20px;
    text-align:left;
    line-height:1.7;
    box-shadow:0 10px 30px rgba(0,0,0,.2);
}

.heart{
    font-size:45px;
    animation:heartbeat 1.2s infinite;
}

.error{
    color:#ffe0e0;
    margin-top:10px;
    display:none;
    font-size:14px;
}

@keyframes openLetter{
    from{
        opacity:0;
        transform:scale(.5) rotate(-5deg);
    }
    to{
        opacity:1;
        transform:scale(1) rotate(0);
    }
}

@keyframes heartbeat{
    0%,100%{transform:scale(1)}
    50%{transform:scale(1.25)}
}

.floating{
    position:fixed;
    font-size:25px;
    animation:float 6s linear infinite;
    opacity:.7;
}

@keyframes float{
    from{
        transform:translateY(100vh);
        opacity:0;
    }
    20%{
        opacity:.8;
    }
    to{
        transform:translateY(-10vh);
        opacity:0;
    }
}
</style>
</head>

<body>

<div class="floating" style="left:10%;animation-delay:0s;">❤️</div>
<div class="floating" style="left:30%;animation-delay:2s;">💕</div>
<div class="floating" style="left:60%;animation-delay:1s;">💖</div>
<div class="floating" style="left:85%;animation-delay:3s;">💗</div>

<div class="box" id="passwordBox">

    <div class="heart">💌</div>

    <h1>❤️শুধু তোমার জন্য❤️</h1>

    <p>
        বার্তাটি দেখতে অনুগ্রহ করে পাসওয়ার্ড দাও 🥰
    </p>

    <input
        type="password"
        id="password"
        placeholder="Password লিখুন..."
    >

    <button onclick="checkPassword()">
        Open Letter 💖
    </button>

    <div class="error" id="error">
        ভুল Password! অনুগ্রহ করে আবার চেষ্টা করুন।
    </div>

</div>


<div class="box" id="letter">

    <div class="heart">❤️</div>

    <div class="letter">

        <h2>প্রিয় বউ, 💕</h2>

        <p>
            আমার উপরে এখনো তুমি রাগ করে থাকবা?
        </p>

        <p>
            তুমি রাগ করে থাকলে আমার কিছুই ভালো লাগে না গো।
        </p>

        <p>
            আর রাগ করে থেকো না গো...🥺❤️
        </p>

        <p>
            Love you so much amr future bou..❤️💞
        </p>

    </div>

</div>


<script>

function checkPassword(){

    const password =
        document.getElementById("password").value;

    const correctPassword =
        "mubin+mihi 143";

    if(password === correctPassword){

        document.getElementById("passwordBox")
        .style.display = "none";

        document.getElementById("letter")
        .style.display = "block";

    }else{

        document.getElementById("error")
        .style.display = "block";

    }

}

</script>

</body>
</html># Love
