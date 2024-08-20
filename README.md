<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Birthday Wishes</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            color: #333;
            text-align: center;
            margin: 0;
            padding: 0;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }
        h1 {
            color: #FFC0CB;
        }
        p {
            font-size: 18px;
            line-height: 1.6;
        }
        .hidden {
            display: none;
        }
		#birthdayImage {
		    width:300px;
			height:auto;
    </style>
</head>
<body>
    <div class="container">
        <h1>Enter Password to View Birthday Wishes</h1>
        <input type="password" id="password" placeholder="Enter Password">
        <button onclick="checkPassword()">Submit</button>
        <p id="message" style="color: pink;"></p>
        <img id="birthdayImage" class="hidden" src="https://b0.bdstatic.com/ugc/39Joi8c7QK2F0NonYpjtWg212b0c554cf99f4074f44d2c78e89540.gif@h_1280" alt=":D">
        <audio id="birthdaySong" class="hidden" autoplay loop>
            <source src="C:\Users\lxq\Music\黄昏之时.mp3" type="audio/mpeg">
            Your browser does not support the audio element.
        </audio>
        <p id="wishes1" class="hidden">To Mr.Hu:happy 18th birthday!^-^</p>
		<p id="wishes2" class="hidden">Wishing you a day filled with love, happiness, and peace.</p>
        <p id="wishes3" class="hidden">This is my first time making a program.</p>
		<p id="wishes4" class="hidden">May be a little simple, please understand.</p>
	    <p id="wishes5" class="hidden">May all your dreams and wishes will come true!</p>
        <p id="wishes6" class="hidden">My greatest blessing is that I hope you can be happy forever.^~^</p>
		<p id="wishes7" class="hidden">May you be admitted to your ideal university and have a bright future.</p>
		<p id="wishes8" class="hidden">fighting!</p>
		<p id="wishes9" class="hidden">You are still special to me.</p>
		<p id="wishes10" class="hidden">Thanks for watching</p>
		
    </div>
    <script>
        var index = 1;

        function checkPassword() {
            var password = document.getElementById('password').value;
            var message = document.getElementById('message');
            var currentWish = document.getElementById('wishes' + index);
            var birthdayImage = document.getElementById('birthdayImage');
            var birthdaySong = document.getElementById('birthdaySong');

            if (password === '20061106') { // 替换 'yourpassword' 为你设置的密码
                message.textContent = ''; // 清空提示消息
                birthdayImage.classList.remove('hidden'); // 显示图片
                birthdaySong.classList.remove('hidden'); // 播放音乐
                showWish(currentWish);
                index++;
            } else {
                message.textContent = 'Incorrect password. Please try again.'; // 显示密码错误提示消息
            }
        }

        function showWish(wish) {
            if (wish) {
                wish.classList.remove('hidden');
		     
                setTimeout(function() {
                    window.scrollTo(0, document.body.scrollHeight);
                    wish.classList.add('hidden');
                    checkPassword();
                }, 5000); // 每隔 2 秒显示下一条祝福语
            }
        }
    </script>
</body>
</html>
