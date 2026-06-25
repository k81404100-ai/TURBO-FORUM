<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Форум Матрешка РП</title>

    <style>
        :root {
            --bg-color: #FFF8E1;
            --card-bg: #FFE0B2;
            --accent: #FFB343;
            --accent-dark: #FF9500;
            --text-main: #19191a;
            --text-secondary: #5c5c5c;
        }

        body {
            margin: 0;
            padding: 12px;
            font-family: -apple-system, BlinkMacSystemFont, Roboto, "Segoe UI", sans-serif;
            background-color: var(--bg-color);
            color: var(--text-main);
        }

        .container {
            max-width: 640px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 24px;
        }

        h1 {
            font-size: 28px;
            color: var(--accent-dark);
            margin: 0;
        }

        .forum-list {
            list-style: none;
            padding: 0;
            margin: 0;
        }

        .forum-item {
            background: var(--card-bg);
            border-radius: 12px;
            padding: 16px;
            margin-bottom: 12px;
            box-shadow: 0 2px 6px rgba(0,0,0,0.08);
        }

        .forum-title {
            font-size: 18px;
            font-weight: 600;
            color: var(--text-main);
            margin: 0 0 8px 0;
        }

        .forum-meta {
            font-size: 13px;
            color: var(--text-secondary);
            margin-bottom: 8px;
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
        }

        .forum-meta span {
            background: #FFCC80;
            padding: 2px 8px;
            border-radius: 16px;
        }

        .forum-desc {
            font-size: 14px;
            color: var(--text-main);
            line-height: 1.5;
            margin-bottom: 12px;
        }

        .forum-action {
            display: inline-block;
            background: var(--accent);
            color: #fff;
            padding: 8px 16px;
            border-radius: 20px;
            text-decoration: none;
            font-weight: 500;
            font-size: 14px;
        }

        .forum-action:active {
            background: var(--accent-dark);
        }

        .empty-state {
            text-align: center;
            padding: 40px;
            color: var(--text-secondary);
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Форум Матрешка РП</h1>
        </header>

        <ul class="forum-list" id="forum-list">
            <!-- Сюда JS добавит темы -->
        </ul>
    </div>

    <script>
        // Пример данных форума (в будущем можно брать с сервера)
        const topics = [
            {
                title: 'Как вступить в семью?',
                author: 'Admin',
                date: 'Сегодня, 10:15',
                replies: 42,
                desc: 'Инструкция для новичков: куда нажать, какие команды использовать и что делать после спавна.'
            },
            {
                title: 'Жалобы на игроков',
                author: 'Moderator',
                date: 'Вчера, 18:30',
                replies: 137,
                desc: 'Здесь можно оставить жалобу на игрока. Обязательно указывайте ник, сервер и суть проблемы.'
            },
            {
                title: 'Баги и ошибки игры',
                author: 'TechSupport',
                date: 'Вчера, 12:05',
                replies: 29,
                desc: 'Если игра вылетает, текстуры не грузятся или не работают команды — пишите сюда.'
            },
            {
                title: 'Предложения по развитию проекта',
                author: 'Admin',
                date: '2 дня назад',
                replies: 8,
                desc: 'Хочешь, чтобы в игре появилась новая механика? Расскажи об этом здесь — мы читаем все предложения.'
            }
        ];

        function renderForum() {
            const list = document.getElementById('forum-list');
            if (topics.length === 0) {
                list.innerHTML = '<div class="empty-state">Пока нет тем на форуме</div>';
                return;
            }

            list.innerHTML = topics.map(topic => `
                <li class="forum-item">
                    <h3 class="forum-title">\${escapeHtml(topic.title)}</h3>
                    <div class="forum-meta">
                        <span>👤 \${escapeHtml(topic.author)}</span>
                        <span>📅 \${escapeHtml(topic.date)}</span>
                        <span>💬 \${topic.replies}</span>
                    </div>
                    <p class="forum-desc">\${escapeHtml(topic.desc)}</p>
                    <a href="#" class="forum-action">Перейти к теме</a>
                </li>
            `).join('');
        }

        // Простая защита от XSS
        function escapeHtml(text) {
            if (!text) return '';
            return text
                .replace(/&/g, "&amp;")
                .replace(/</g, "&lt;")
                .replace(/>/g, "&gt;")
                .replace(/"/g, "&quot;")
                .replace(/'/g, "&#039;");
        }

        // Запускаем отрисовку сразу, как только скрипт загрузится
        renderForum();
    </script>
</body>
</html>
