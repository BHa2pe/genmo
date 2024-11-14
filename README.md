<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AQERKE - Платформа для общения</title>
    <style>
        /* Стилизация */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }

        header {
            background-color: #333;
            color: white;
            padding: 10px 0;
            text-align: center;
        }

        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
        }

        main {
            padding: 20px;
        }

        form {
            max-width: 400px;
            margin: 0 auto;
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        form label {
            display: block;
            margin-bottom: 8px;
        }

        form input {
            width: 100%;
            padding: 8px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        form button {
            width: 100%;
            padding: 10px;
            background-color: #333;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        form button:hover {
            background-color: #555;
        }

        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 10px;
            position: fixed;
            bottom: 0;
            width: 100%;
        }

        .post {
            background-color: white;
            padding: 15px;
            margin: 10px 0;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .hidden {
            display: none;
        }
    </style>
</head>
<body>

<header>
    <h1 id="pageTitle">Добро пожаловать на AQERKE</h1>
    <nav>
        <a href="javascript:void(0);" onclick="showPage('home')">Главная</a>
        <a href="javascript:void(0);" onclick="showPage('login')">Войти</a>
        <a href="javascript:void(0);" onclick="showPage('register')">Зарегистрироваться</a>
    </nav>
</header>

<main id="mainContent">
    <!-- Главная страница -->
    <section id="homePage">
        <h2>Что такое AQERKE?</h2>
        <p>AQERKE - сайт, сочетающий черты социальной сети и форума, на котором зарегистрированные пользователи могут размещать ссылки на какую-либо понравившуюся информацию в интернете и обсуждать её. Как и многие другие подобные сайты, AQERKE поддерживает систему голосования за понравившиеся сообщения — наиболее популярные из них оказываются на заглавной странице сайта. Один из наиболее популярных сайтов в мире — 20-е место по посещаемости по данным SimilarWeb.
        AQERKE был основан 23 июня 2005 года выпускниками Виргинского университета Стивом Хаффманом[англ.] и Алексисом Оганяном[англ.]. Первоначальное финансирование проект получил через венчурный фонд «Y Combinator». В январе 2006 года к команде присоединился Аарон Шварц после объединения Reddit с его проектом Infogami. 31 октября 2006 года проект был приобретён издательством Condé Nast (владельцем журнала «Wired»), после чего Шварц был уволен.

18 июня 2008 года AQERKE открыл программное обеспечение проекта, за исключением кода, отвечающего за борьбу со спамом.

В 2010 году пользователи сайта собрали более 180 тысяч долларов США для помощи жертвам землетрясения на Гаити.

6 сентября 2011 года AQERKE начал работать под управлением «Advance Publications», дочерней компании «Condé Nast», фактически получив независимость от последних.

В январе 2012 года сайт объявил об участии в 12-часовом отключении в знак протеста против Stop Online Piracy Act. Отключение сайта было произведено 18 января, и совпало с отключением Википедии и других сайтов, участвовавших в акции.

9 февраля 2021 года интернет-портал провёл пятый раунд финансирования, в рамках которого компании удалось привлечь порядка $250 млн, доведя оценку стоимости бизнеса до $6 млрд.

В феврале 2023 года, используя фишинг, хакеры взломали сайт, получив доступ к внутренним документам и коду платформы.

В феврале 2024 года AQERKE объявил о партнёрстве с Google на сумму около $60 млн в год для лицензирования своего пользовательского контента с целью обучения моделей искусственного интеллекта Google. Данное сотрудничество также позволит AQERKE получить доступ к сервису Vertex AI, который поможет улучшить качество поиска на сайте компании.</p>
    </section>

    <!-- Страница входа -->
    <section id="loginPage" class="hidden">
        <h2>Войти в AQERKE</h2>
        <form id="loginForm">
            <label for="loginUsername">Имя пользователя</label>
            <input type="text" id="loginUsername" name="username" required>

            <label for="loginPassword">Пароль</label>
            <input type="password" id="loginPassword" name="password" required>

            <button type="submit">Войти</button>
        </form>
    </section>

    <!-- Страница регистрации -->
    <section id="registerPage" class="hidden">
        <h2>Зарегистрироваться на AQERKE</h2>
        <form id="registerForm">
            <label for="registerUsername">Имя пользователя</label>
            <input type="text" id="registerUsername" name="username" required>

            <label for="registerEmail">Электронная почта</label>
            <input type="email" id="registerEmail" name="email" required>

            <label for="registerPassword">Пароль</label>
            <input type="password" id="registerPassword" name="password" required>

            <label for="registerConfirmPassword">Подтверждение пароля</label>
            <input type="password" id="registerConfirmPassword" name="confirmPassword" required>

            <button type="submit">Зарегистрироваться</button>
        </form>
    </section>
</main>

<footer>
    <p>&copy; 2024 AQERKE. Все права защищены.</p>
</footer>

<script>
    // Функция для отображения нужной страницы
    function showPage(page) {
        // Скрываем все страницы
        document.getElementById('homePage').classList.add('hidden');
        document.getElementById('loginPage').classList.add('hidden');
        document.getElementById('registerPage').classList.add('hidden');

        // Показываем нужную страницу
        if (page === 'home') {
            document.getElementById('homePage').classList.remove('hidden');
            document.getElementById('pageTitle').textContent = 'Добро пожаловать на AQERKE';
        } else if (page === 'login') {
            document.getElementById('loginPage').classList.remove('hidden');
            document.getElementById('pageTitle').textContent = 'Войти в AQERKE';
        } else if (page === 'register') {
            document.getElementById('registerPage').classList.remove('hidden');
            document.getElementById('pageTitle').textContent = 'Зарегистрироваться на AQERKE';
        }
    }

    // Простейшая валидация для формы регистрации
    document.getElementById('registerForm').addEventListener('submit', function(event) {
        const password = document.getElementById('registerPassword').value;
        const confirmPassword = document.getElementById('registerConfirmPassword').value;

        if (password !== confirmPassword) {
            alert('Пароли не совпадают!');
            event.preventDefault(); // Остановить отправку формы
        }
    });

    // По умолчанию отображаем главную страницу
    showPage('home');
</script>

</body>
</html>