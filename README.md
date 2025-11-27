# TikTok-active-slide
Interactive phone mockup slide for L&amp;D project
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>TikTok Interactive Slide</title>

<style>
    body {
        margin: 0;
        font-family: Arial, sans-serif;
        background: #ffffff;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
    }

    .container {
        position: relative;
        width: 400px;
    }

    .phone {
        width: 100%;
        border-radius: 40px;
        overflow: hidden;
        box-shadow: 0 0 20px rgba(0,0,0,0.2);
    }

    .phone img {
        width: 100%;
        display: block;
    }

    .bubble-group {
        position: absolute;
        top: -40px;
        width: 100%;
        display: flex;
        justify-content: space-between;
    }

    .bubble {
        width: 90px;
        height: 90px;
        border-radius: 50%;
        background: linear-gradient(45deg, #7f5cff, #00c8ff);
        display: flex;
        justify-content: center;
        align-items: center;
        color: white;
        font-weight: bold;
        cursor: pointer;
        transition: 0.3s ease;
    }

    .bubble:hover {
        transform: scale(1.1);
    }

    .text-box {
        position: absolute;
        top: 40%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 75%;
        padding: 15px;
        background: white;
        border-radius: 12px;
        box-shadow: 0 0 10px rgba(0,0,0,0.2);
        opacity: 0;
        pointer-events: none;
        transition: 0.3s;
        text-align: center;
    }

    .text-box.show {
        opacity: 1;
        pointer-events: auto;
    }
</style>

</head>
<body>

<div class="container">
    <div class="bubble-group">
        <div class="bubble" onclick="showText(1)">Hook</div>
        <div class="bubble" onclick="showText(2)">Visuals</div>
        <div class="bubble" onclick="showText(3)">Audio</div>
    </div>

    <div class="phone">
        <img src="https://i.imgur.com/kVwS4Yb.png" alt="phone" />
    </div>

    <div id="text1" class="text-box">A strong hook grabs attention in the first 3–5 seconds.</div>
    <div id="text2" class="text-box">Use clean, bold visuals to keep learners engaged.</div>
    <div id="text3" class="text-box">Clear, crisp audio keeps watchers from scrolling away.</div>
</div>

<script>
function showText(num) {
    document.querySelectorAll('.text-box').forEach(t => t.classList.remove('show'));
    document.getElementById('text' + num).classList.add('show');
}
</script>

</body>
</html>
