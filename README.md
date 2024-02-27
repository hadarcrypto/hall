<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HALELEY</title>
    <style>
        body {
            background-color: black;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            flex-direction: column;
        }
        .button {
            background-color: #D2AA5C; /* Гірчичний колір */
            color: black;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        .button:hover {
            background-color: #B98A42; /* Темніший гірчичний колір при наведенні */
        }
    </style>
</head>
<body>
    <button class="button" onclick="location.href='what.html';">ЩО ТАКЕ HALELEY</button>
    <button class="button" onclick="location.href='subs.html';">ОФОРМИТИ ПІДПИСКУ</button>
    <button class="button" onclick="window.open('https://t.me/+_CI5lQFGZf02ZDZi');">СПІЛЬНОТА</button>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HALELEY</title>
    <style>
        body {
            background-color: black;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            flex-direction: column;
            text-align: center;
        }
        .inputField, .submitBtn {
            background-color: rgba(255, 255, 255, 0.5); /* Напівпрозорий білий */
            color: black;
            padding: 10px;
            border-radius: 5px;
            border: none;
            width: 80%; /* Ширина для полів і кнопки */
            max-width: 500px; /* Максимальна ширина, щоб елементи не ставали занадто широкими на великих екранах */
            margin-top: 10px;
            cursor: pointer; /* Змінює курсор, показуючи, що елемент можна натискати */
        }
        .submitBtn {
            background-color: #D2AA5C; /* Колір кнопки */
            color: white; /* Колір тексту на кнопці */
            transition: background-color 0.3s; /* Анімація зміни кольору */
        }
        .submitBtn:hover {
            background-color: #B98A42; /* Колір кнопки при наведенні */
        }
        .label {
            margin-bottom: 8px;
        }
        .hidden {
            display: none; /* Сховати елемент */
        }
    </style>
</head>
<body>
    <div class="content">
        <div class="label">Клікніть для копіювання адреси гаманця:</div>
        <input type="text" value="TTCYrrTLH15FBqikxYYxgakiDJZAe5J4VZ" class="inputField" id="walletAddress" readonly onclick="copyAddress()">
        
        <div class="label">Введіть хеш транзакції у поле нижче (64 символи):</div>
        <input type="text" placeholder="Введіть хеш транзакції тут" class="inputField" id="transactionHash" maxlength="64">
        
        <button class="submitBtn" id="submitBtn">SUBS</button>
    </div>
    <div id="message" class="hidden">
        ЗВЕРНІТЬСЯ ДО АДМІНІСТРАТОРА @katoshi_haleley
    </div>
    
    <script>
        function copyAddress() {
            var inputField = document.getElementById('walletAddress');
            inputField.select();
            document.execCommand("copy");
            alert("Скопійовано: " + inputField.value);
        }

        document.getElementById('submitBtn').addEventListener('click', function() {
            var hash = document.getElementById('transactionHash').value;
            if(hash.length === 64) {
                document.querySelector('.content').classList.add('hidden');
                document.getElementById('message').classList.remove('hidden');
            } else {
                alert('Хеш транзакції має складатися з 64 символів');
            }
        });
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HALELEY</title>
    <style>
        body {
            background-color: black; /* Зміна кольору фону на чорний */
            color: white; /* Зміна кольору тексту на білий */
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            padding: 2vh;
            box-sizing: border-box;
        }
        .container, .button {
            background-color: rgba(255, 255, 255, 0.5); /* Білий напівпрозорий колір */
            border-radius: 1vh; /* Закруглені кути */
            padding: 1.5vh; /* Зменшення відступів */
            text-align: center;
            margin-bottom: 1.5vh; /* Зменшення відступу між контейнерами і кнопкою */
            font-size: 0.9rem; /* Зменшення розміру шрифту */
        }
        .button {
            border: none; /* Видалення рамки кнопки */
            cursor: pointer; /* Зміна курсору при наведенні */
            width: 15vh; /* Зменшення ширини кнопки */
            transition: background-color 0.3s; /* Плавна зміна кольору */
            color: white; /* Колір тексту кнопки */
        }
        .button:hover {
            background-color: rgba(255, 255, 255, 0.7); /* Зміна кольору при наведенні */
        }
    </style>
</head>
<body>
    <div class="container">
        HALELEY - алгоритм для оптимізованого пошуку криптоактивностей, аірдропів, тестнетів!
    </div>
    <div class="container">
        Алгоритм використовує всі доступні джерела в інтернеті для пошуку актуальних криптоактивностей. Після чого наша команда тестує їх на проходимість і час. Якщо дроп перспективний і виконання займає не більше 5 хвилин, то ми додаємо його у спільноту, де ти можеш його виконати.
    </div>
    <div class="container">
        Безумовно, ти можеш самостійно шукати активності в інтернеті, але пошук, перевірка і участь у одному дропі можуть зайняти до години часу. Таким чином, ти не зможеш масштабувати цю нішу, використовуючи якомога менше часу.
    </div>
    <div class="container">
        Існують 2 підписки: на рік і назавжди! Щоб оплатити на рік, перейди до меню "ОФОРМИТИ ПІДПИСКУ" і надішли 55 USDT на вказану адресу, після чого слідуй інструкціям. Якщо бажаєш оформити підписку назавжди, то на ту ж адресу надішли 77 USDT і також слідуй інструкціям.
    </div>
    <a href="haleley.html" class="button">BACK</a> <!-- Кнопка BACK -->
</body>
</html>
