<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Форум Матрешка РП</title>

    <style>
        :root {
            --bg-color: #000000;
            --card-bg: #2b2b2b;
            --border-color: #4a4a4a;
            --text-main: #ffffff;
            --text-secondary: #aaaaaa;
            --accent: #ff5555;
            --btn-bg: #8a2be2;
            --btn-hover: #7a1cb9;
        }

        body { margin: 0; padding: 20px; font-family: -apple-system, BlinkMacSystemFont, Roboto, sans-serif; background-color: var(--bg-color); color: var(--text-main); min-height: 100vh; position: relative; }
        .container { max-width: 640px; margin: 0 auto; }

        /* Кнопка регистрации (видна, если нет аккаунта) */
        .register-btn {
            position: fixed; top: 20px; right: 20px;
            background-color: var(--btn-bg); color: #fff;
            padding: 10px 20px; border-radius: 20px; text-decoration: none;
            font-weight: 600; font-size: 14px;
            box-shadow: 0 4px 12px rgba(138, 43, 226, 0.4);
            z-index: 1000; transition: all 0.2s ease;
        }
        .register-btn:hover { background-color: var(--btn-hover); transform: translateY(-2px); }

        /* Иконка профиля (видна, если есть аккаунт) */
        .profile-icon {
            position: fixed; top: 20px; right: 20px;
            width: 44px; height: 44px; border-radius: 50%;
            background: var(--btn-bg); color: #fff;
            display: none; align-items: center; justify-content: center;
            font-weight: bold; font-size: 18px;
            box-shadow: 0 4px 12px rgba(138, 43, 226, 0.4);
            z-index: 1000; cursor: pointer; transition: all 0.2s ease;
        }
        .profile-icon.visible { display: flex; }
        .profile-icon:hover { transform: translateY(-2px); box-shadow: 0 6px 16px rgba(138, 43, 226, 0.6); }
        
        header { text-align: center; margin-bottom: 30px; }
        h1 { font-size: 32px; color: var(--text-main); margin: 0; letter-spacing: 1px; text-transform: uppercase; }

        .forum-wrapper {
            background-color: var(--card-bg); border: 1px solid var(--border-color);
            border-radius: 12px; padding: 24px; box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
        }

        /* Форма */
        .registration-form {
            display: none; background: #3a3a3a; padding: 20px;
            border-radius: 8px; margin-top: 20px; animation: slideDown 0.3s ease-out;
            border: 1px solid #555;
        }
        .registration-form.visible { display: block; }
        @keyframes slideDown { from { opacity: 0; transform: translateY(-10px); } to { opacity: 1; transform: translateY(0); } }

        .form-group { margin-bottom: 12px; }
        .form-label { display: block; margin-bottom: 6px; color: var(--text-secondary); font-size: 13px; }
        .form-input {
            width: 100%; padding: 10px; background: #222; border: 1px solid #444;
            border-radius: 6px; color: #fff; font-size: 14px; box-sizing: border-box;
        }
        .form-input:focus { outline: none; border-color: var(--btn-bg); }

        .submit-btn {
            display: inline-block; background-color: var(--btn-bg); color: #fff;
            padding: 10px 20px; border-radius: 20px; text-decoration: none;
            font-weight: 600; font-size: 14px; box-shadow: 0 4px 12px rgba(138, 43, 226, 0.4);
            transition: all 0.2s ease; width: auto; cursor: pointer; border: none;
        }
        .submit-btn:hover { background-color: var(--btn-hover); transform: translateY(-2px); }

        .empty-state { text-align: center; padding: 40px 20px; color: var(--text-secondary); }
        .empty-state h2 { margin: 0 0 12px 0; color: var(--text-main); font-size: 20px; }
        .add-topic-btn {
            display: inline-block; margin-top: 20px; background: var(--accent); color: #fff;
            padding: 10px 20px; border-radius: 20px; text-decoration: none;
            font-weight: 500; font-size: 14px; transition: background 0.2s ease;
        }
        .add-topic-btn:hover { background: var(--accent-hover); }
    </style>
</head>
<body>

    <!-- Кнопка (видна, если НЕТ аккаунта) -->
    <a href="#" class="register-btn" id="reg-trigger">Зарегистрироваться</a>

    <!-- Иконка (видна, если ЕСТЬ аккаунт) -->
    <div class="profile-icon" id="profile-trigger" title="Профиль"></div>

    <div class="container">
        <header>
            <h1>Форум Матрешка РП</h1>

            <!-- Форма регистрации -->
            <div class="registration-form" id="registration-form">
                <div class="form-group">
                    <label class="form-label" for="username">Имя пользователя</label>
                    <input type="text" id="username" class="form-input" placeholder="Придумайте никнейм">
                </div>
                <div class="form-group">
                    <label class="form-label" for="password">Пароль</label>
                    <input type="password" id="password" class="form-input" placeholder="Минимум 6 символов">
                </div>
                <!-- Поле префикса удалено -->
                <button type="button" class="submit-btn" onclick="handleRegister()">Зарегистрироваться</button>
            </div>
        </header>

        <div class="forum-wrapper">
            <div id="forum-content">
                <!-- Темы форума -->
            </div>
        </div>
    </div>

    <script>
        const topics = [];

        // --- ЛОГИКА АВТОРИЗАЦИИ ---
        function initAuth() {
            const user = localStorage.getItem('forum_user');
            const btn = document.getElementById('reg-trigger');
            const icon = document.getElementById('profile-trigger');

            if (user) {
                // Аккаунт есть -> показываем иконку, скрываем кнопку
                btn.style.display = 'none';
                icon.classList.add('visible');
                
                const data = JSON.parse(user);
                icon.textContent = data.username.charAt(0).toUpperCase();
            } else {
                // Аккаунта нет -> показываем кнопку
                btn.style.display = 'block';
                icon.classList.remove('visible');
            }
        }

        function handleRegister() {
            const username = document.getElementById('username').value.trim();
            const password = document.getElementById('password').value.trim();

            if (!username || !password) {
                alert('Пожалуйста, заполните имя и пароль.');
                return;
            }

            // Сохраняем в localStorage (в реальном проекте пароли хешируют!)
            const userData = { username, password };
            localStorage.setItem('forum_user', JSON.stringify(userData));

            alert(`Добро пожаловать, ${username}!`);

            initAuth(); // Перерисовываем интерфейс

            // Скрываем форму
            document.getElementById('registration-form').classList.remove('visible');
            
            // Очищаем поля
            document.getElementById('username').value = '';
            document.getElementById('password').value = '';
        }

        // Клик по кнопке "Зарегистрироваться" (вызывает форму)
        document.getElementById('reg-trigger').addEventListener('click', function(e) {
            e.preventDefault();
            const form = document.getElementById('registration-form');
            form.classList.toggle('visible');
        });

        // Клик по иконке профиля
        document.getElementById('profile-trigger').addEventListener('click', function() {
            const user = JSON.parse(localStorage.getItem('forum_user'));
            alert(`Профиль:\nНик: ${user.username}`);
        });

        // --- ФОРУМ ---
        function renderForum() {
            const container = document.getElementById('forum-content');
            if (topics.length === 0) {
                container.innerHTML = `
                    <div class="empty-state">
                        <h2>Тем пока нет</h2>
                        <p>Будь первым — создай новую тему на форуме.</p>
                        <a href="#" class="add-topic-btn">Создать тему</a>
                    </div>`;
                return;
            }
            const listHtml = topics.map(topic => `
                <div style="padding: 16px 0; border-bottom: 1px solid var(--border-color);">
                    <div style="font-size: 18px; font-weight: 600; color: var(--text-main); margin-bottom: 8px;">
                        ${escapeHtml(topic.title)}
                    </div>
                    <div style="font-size: 13px; color: var(--text-secondary); margin-bottom: 8px; display: flex; gap: 12px; flex-wrap: wrap;">
                        <span style="background: #3a3a3a; padding: 2px 8px; border-radius: 16px;">${escapeHtml(topic.author)}</span>
                        <span style="background: #3a3a3a; padding: 2px 8px; border-radius: 16px;">${escapeHtml(topic.date)}</span>
                        <span style="background: #3a3a3a; padding: 2px 8px; border-radius: 16px;">💬 ${topic.replies}</span>
                    </div>
                    <p style="font-size: 14px; color: var(--text-secondary); line-height: 1.5; margin-bottom: 16px;">
                        ${escapeHtml(topic.desc)}
                    </p>
                    <a href="#" style="display: inline-block; background: var(--accent); color: #fff; padding: 8px 16px; border-radius: 20px; text-decoration: none; font-weight: 500; font-size: 14px;">
                        Перейти к теме
                    </a>
                </div>`).join('');
            container.innerHTML = `<ul style="list-style: none; padding: 0; margin: 0;">${listHtml}</ul>`;
        }

        function escapeHtml(text) {
            if (!text) return '';
            return text.replace(/&/g, "&amp;").replace(/</g, "&lt;").replace(/>/g, "&gt;").replace(/"/g, "&quot;").replace(/'/g, "&#039;");
        }

        initAuth();
        renderForum();
    </script>
</body>
</html>
