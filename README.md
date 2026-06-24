<div align="center">

# 🚀 NURIK | Full-Stack Developer

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&color=667EEA&center=true&vCenter=true&width=435&lines=Full-Stack+Web+Developer;Mobile+App+Creator;2%2B+Years+Experience;Building+Digital+Solutions" alt="Typing SVG" />

[![Profile Views](https://komarev.com/ghpvc/?username=Nurikgg77&color=blueviolet&style=flat-square)](https://github.com/Nurikgg77)
[![GitHub Followers](https://img.shields.io/github/followers/Nurikgg77?label=Followers&style=social)](https://github.com/Nurikgg77)

</div>

---

## 🎨 3D Interactive Profile Card

<details open>
<summary><b>💫 Click to interact with my 3D profile card</b></summary>

<!DOCTYPE html>
<html>
<head>
<style>
body { margin: 0; padding: 20px; background: #0f0f23; font-family: 'Segoe UI', sans-serif; }
.container { max-width: 600px; margin: 0 auto; perspective: 1200px; }
.card { width: 100%; height: 500px; position: relative; cursor: pointer; transform-style: preserve-3d; transition: transform 0.8s cubic-bezier(0.68, -0.55, 0.265, 1.55); }
.card.flipped { transform: rotateY(180deg); }
.card-face { width: 100%; height: 100%; position: absolute; backface-visibility: hidden; border-radius: 24px; display: flex; flex-direction: column; justify-content: space-between; padding: 2.5rem; box-shadow: 0 20px 60px rgba(102, 126, 234, 0.3); border: 2px solid rgba(102, 126, 234, 0.2); }
.front { background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 100%); color: white; }
.back { background: linear-gradient(135deg, #f5576c 0%, #f093fb 50%, #667eea 100%); transform: rotateY(180deg); color: white; }
.header { text-align: center; }
.avatar { font-size: 80px; margin-bottom: 1rem; animation: float 3s ease-in-out infinite; }
@keyframes float { 0%, 100% { transform: translateY(0px); } 50% { transform: translateY(-20px); } }
.name { font-size: 32px; font-weight: 700; margin: 0; text-shadow: 0 2px 10px rgba(0,0,0,0.2); }
.title { font-size: 13px; opacity: 0.9; letter-spacing: 2px; margin: 0.5rem 0 0 0; text-transform: uppercase; }
.divider { width: 60px; height: 3px; background: rgba(255,255,255,0.4); margin: 1.5rem auto; border-radius: 2px; }
.stats { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 1.5rem; }
.stat { text-align: center; }
.stat-num { font-size: 24px; font-weight: 700; display: block; }
.stat-label { font-size: 11px; opacity: 0.85; display: block; margin-top: 0.3rem; }
.hint { font-size: 12px; opacity: 0.75; margin-top: 1.5rem; }
.skills-section { }
.skills-title { font-size: 20px; font-weight: 700; text-align: center; margin-bottom: 1.5rem; }
.skill-tags { display: flex; flex-wrap: wrap; gap: 0.7rem; justify-content: center; margin-bottom: 1.5rem; }
.skill-tag { background: rgba(255,255,255,0.15); padding: 0.5rem 1rem; border-radius: 25px; font-size: 12px; font-weight: 600; backdrop-filter: blur(10px); border: 1px solid rgba(255,255,255,0.2); }
.tech-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
.tech-item { background: rgba(255,255,255,0.1); padding: 1rem; border-radius: 12px; text-align: center; border: 1px solid rgba(255,255,255,0.15); }
.tech-icon { font-size: 28px; margin-bottom: 0.5rem; }
.tech-name { font-size: 12px; font-weight: 600; }
.mouse-hint { position: absolute; bottom: 10px; left: 50%; transform: translateX(-50%); font-size: 11px; opacity: 0.5; white-space: nowrap; }
</style>
</head>
<body>
<div class="container">
<div class="card" id="card3d">
<div class="card-face front">
<div class="header">
<div class="avatar">👨‍💻</div>
<h1 class="name">NURIK</h1>
<p class="title">Full-Stack Developer</p>
</div>
<div class="divider"></div>
<div class="stats">
<div class="stat"><span class="stat-num">2+</span><span class="stat-label">Лет опыта</span></div>
<div class="stat"><span class="stat-num">10+</span><span class="stat-label">Проектов</span></div>
<div class="stat"><span class="stat-num">100%</span><span class="stat-label">Качество</span></div>
</div>
<div class="hint">💡 Нажми чтобы увидеть навыки</div>
</div>

<div class="card-face back">
<div class="skills-section">
<div class="skills-title">Мой Tech Stack</div>
<div class="skill-tags">
<div class="skill-tag">JavaScript</div>
<div class="skill-tag">PHP</div>
<div class="skill-tag">Laravel</div>
<div class="skill-tag">React</div>
<div class="skill-tag">Flutter</div>
<div class="skill-tag">MySQL</div>
<div class="skill-tag">Python</div>
<div class="skill-tag">Node.js</div>
</div>
<div class="tech-grid">
<div class="tech-item"><div class="tech-icon">🎨</div><div class="tech-name">Frontend</div></div>
<div class="tech-item"><div class="tech-icon">⚙️</div><div class="tech-name">Backend</div></div>
<div class="tech-item"><div class="tech-icon">📱</div><div class="tech-name">Mobile</div></div>
<div class="tech-item"><div class="tech-icon">🗄️</div><div class="tech-name">Databases</div></div>
</div>
</div>
<div class="hint">💡 Нажми еще раз</div>
</div>
<div class="mouse-hint">Также крути мышкой 👆</div>
</div>
</div>
<script>
const card = document.getElementById('card3d');
let isFlipped = false;
card.addEventListener('click', () => {
isFlipped = !isFlipped;
card.classList.toggle('flipped');
});
document.addEventListener('mousemove', (e) => {
if (isFlipped) return;
const rect = card.getBoundingClientRect();
const x = e.clientX - rect.left;
const y = e.clientY - rect.top;
const centerX = rect.width / 2;
const centerY = rect.height / 2;
const rotateX = (y - centerY) / 15;
const rotateY = (centerX - x) / 15;
card.style.transform = `rotateX(${rotateX}deg) rotateY(${rotateY}deg)`;
});
document.addEventListener('mouseleave', () => {
if (!isFlipped) {
card.style.transform = 'rotateX(0) rotateY(0)';
}
});
</script>
</body>
</html>
```

</details>

---

## 👋 Обо Мне

Привет! Я **Nurik** - Full-Stack разработчик из **Ашхабата, Туркменистан** 🇹🇲 с более чем 2 годами опыта в создании высокопроизводительных веб-приложений и кроссплатформенных мобильных решений.

### 🎯 Мой Фокус:
- 🏗️ Создание чистого, масштабируемого кода
- ⚡ Оптимизация производительности
- 🎨 Исключительный UX/UI дизайн
- 🔐 Безопасность и защита данных
- 🤝 Командная работа и коммуникация

---

## 💻 Tech Stack

### 🎨 Frontend
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Tailwind](https://img.shields.io/badge/Tailwind-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

### ⚙️ Backend
![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)

### 📱 Mobile
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)

### 💾 Databases & Tools
![MySQL](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

---

## 📝 Мой Блог - Инструмент для создания статей

<details open>
<summary><b>✍️ Создавай и управляй своими статьями</b></summary>

<!DOCTYPE html>
<html>
<head>
<style>
* { margin: 0; padding: 0; box-sizing: border-box; }
body { font-family: 'Segoe UI', sans-serif; background: linear-gradient(135deg, #0f0f23 0%, #1a0a3f 100%); color: #fff; padding: 20px; }
.blog-container { max-width: 900px; margin: 0 auto; }
.blog-header { text-align: center; margin-bottom: 40px; }
.blog-title { font-size: 36px; font-weight: 700; background: linear-gradient(135deg, #667eea, #764ba2, #f093fb); -webkit-background-clip: text; -webkit-text-fill-color: transparent; margin-bottom: 10px; }
.blog-subtitle { color: #888; font-size: 14px; }

.blog-tabs { display: flex; gap: 1rem; margin-bottom: 2rem; border-bottom: 2px solid rgba(102, 126, 234, 0.2); }
.tab-btn { background: none; border: none; color: #aaa; padding: 12px 24px; cursor: pointer; font-size: 14px; font-weight: 600; border-bottom: 3px solid transparent; transition: all 0.3s; }
.tab-btn.active { color: #667eea; border-bottom-color: #667eea; }
.tab-btn:hover { color: #667eea; }

.tab-content { display: none; }
.tab-content.active { display: block; animation: fadeIn 0.3s; }
@keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

.form-group { margin-bottom: 1.5rem; }
.form-label { display: block; margin-bottom: 0.5rem; font-weight: 600; color: #ddd; }
.form-input, .form-textarea { width: 100%; padding: 12px; background: rgba(255,255,255,0.05); border: 2px solid rgba(102, 126, 234, 0.3); border-radius: 8px; color: #fff; font-family: inherit; font-size: 14px; transition: all 0.3s; }
.form-input:focus, .form-textarea:focus { outline: none; border-color: #667eea; background: rgba(102, 126, 234, 0.1); }
.form-textarea { resize: vertical; min-height: 150px; }

.btn-publish { background: linear-gradient(135deg, #667eea, #764ba2); color: white; border: none; padding: 12px 32px; border-radius: 8px; font-weight: 600; cursor: pointer; transition: all 0.3s; width: 100%; font-size: 14px; }
.btn-publish:hover { transform: translateY(-2px); box-shadow: 0 8px 24px rgba(102, 126, 234, 0.4); }

.blog-posts { display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr)); gap: 2rem; }
.post-card { background: rgba(255,255,255,0.05); border: 2px solid rgba(102, 126, 234, 0.2); border-radius: 12px; padding: 1.5rem; transition: all 0.3s; cursor: pointer; }
.post-card:hover { border-color: rgba(102, 126, 234, 0.6); transform: translateY(-8px); box-shadow: 0 8px 32px rgba(102, 126, 234, 0.2); }
.post-date { font-size: 12px; color: #888; margin-bottom: 0.5rem; }
.post-title { font-size: 18px; font-weight: 700; margin-bottom: 0.8rem; color: #fff; }
.post-content { font-size: 14px; color: #bbb; line-height: 1.6; margin-bottom: 1rem; display: -webkit-box; -webkit-line-clamp: 3; -webkit-box-orient: vertical; overflow: hidden; }
.post-category { display: inline-block; background: rgba(102, 126, 234, 0.2); color: #667eea; padding: 4px 12px; border-radius: 20px; font-size: 12px; font-weight: 600; }

.btn-delete { background: rgba(245, 87, 108, 0.2); color: #f5576c; border: 1px solid #f5576c; padding: 6px 12px; border-radius: 6px; font-size: 12px; cursor: pointer; transition: all 0.3s; }
.btn-delete:hover { background: #f5576c; color: white; }

.empty-state { text-align: center; padding: 3rem 2rem; color: #666; }
.empty-icon { font-size: 48px; margin-bottom: 1rem; }

.stats-box { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1rem; margin-bottom: 2rem; }
.stat-item { background: rgba(102, 126, 234, 0.1); border: 1px solid rgba(102, 126, 234, 0.3); border-radius: 8px; padding: 1rem; text-align: center; }
.stat-number { font-size: 24px; font-weight: 700; color: #667eea; }
.stat-label { font-size: 12px; color: #888; margin-top: 0.5rem; }
</style>
</head>
<body>
<div class="blog-container">
<div class="blog-header">
<h1 class="blog-title">📖 Мой Блог</h1>
<p class="blog-subtitle">Делись знаниями и опытом разработки</p>
</div>

<div class="stats-box">
<div class="stat-item">
<div class="stat-number" id="totalPosts">0</div>
<div class="stat-label">Статей написано</div>
</div>
<div class="stat-item">
<div class="stat-number" id="totalViews">0</div>
<div class="stat-label">Просмотров</div>
</div>
<div class="stat-item">
<div class="stat-number" id="totalLikes">0</div>
<div class="stat-label">Нравится</div>
</div>
</div>

<div class="blog-tabs">
<button class="tab-btn active" onclick="showTab('create')">✍️ Создать статью</button>
<button class="tab-btn" onclick="showTab('posts')">📚 Все статьи</button>
</div>

<div class="tab-content active" id="create">
<form onsubmit="publishPost(event)">
<div class="form-group">
<label class="form-label">Заголовок</label>
<input type="text" class="form-input" id="postTitle" placeholder="Введи заголовок статьи..." required>
</div>

<div class="form-group">
<label class="form-label">Категория</label>
<input type="text" class="form-input" id="postCategory" placeholder="например: JavaScript, Web Development..." required>
</div>

<div class="form-group">
<label class="form-label">Содержание</label>
<textarea class="form-textarea" id="postContent" placeholder="Напиши свою статью здесь..." required></textarea>
</div>

<button type="submit" class="btn-publish">📤 Опубликовать статью</button>
</form>
</div>

<div class="tab-content" id="posts">
<div class="blog-posts" id="postsList">
<div class="empty-state">
<div class="empty-icon">📝</div>
<p>Статей еще нет. Создай первую статью!</p>
</div>
</div>
</div>
</div>

<script>
const posts = JSON.parse(localStorage.getItem('blogPosts')) || [];

function showTab(tabName) {
document.querySelectorAll('.tab-content').forEach(tab => tab.classList.remove('active'));
document.querySelectorAll('.tab-btn').forEach(btn => btn.classList.remove('active'));
document.getElementById(tabName).classList.add('active');
event.target.classList.add('active');
if (tabName === 'posts') renderPosts();
}

function publishPost(e) {
e.preventDefault();
const title = document.getElementById('postTitle').value;
const category = document.getElementById('postCategory').value;
const content = document.getElementById('postContent').value;

if (!title || !category || !content) return;

const post = {
id: Date.now(),
title,
category,
content,
date: new Date().toLocaleDateString('ru-RU'),
views: 0,
likes: 0
};

posts.unshift(post);
localStorage.setItem('blogPosts', JSON.stringify(posts));

document.getElementById('postTitle').value = '';
document.getElementById('postCategory').value = '';
document.getElementById('postContent').value = '';

alert('✅ Статья опубликована!');
updateStats();
renderPosts();
showTab('posts');
}

function renderPosts() {
const postsList = document.getElementById('postsList');
if (posts.length === 0) {
postsList.innerHTML = '<div class="empty-state"><div class="empty-icon">📝</div><p>Статей еще нет. Создай первую!</p></div>';
return;
}

postsList.innerHTML = posts.map(post => `
<div class="post-card">
<div class="post-date">📅 ${post.date}</div>
<h3 class="post-title">${post.title}</h3>
<p class="post-content">${post.content}</p>
<div style="display: flex; justify-content: space-between; align-items: center;">
<span class="post-category">${post.category}</span>
<button class="btn-delete" onclick="deletePost(${post.id})">🗑️ Удалить</button>
</div>
</div>
`).join('');
}

function deletePost(id) {
const index = posts.findIndex(p => p.id === id);
if (index > -1) {
posts.splice(index, 1);
localStorage.setItem('blogPosts', JSON.stringify(posts));
renderPosts();
updateStats();
}
}

function updateStats() {
document.getElementById('totalPosts').textContent = posts.length;
document.getElementById('totalViews').textContent = (posts.length * 10 + Math.floor(Math.random() * 100));
document.getElementById('totalLikes').textContent = (posts.length * 5 + Math.floor(Math.random() * 50));
}

renderPosts();
updateStats();
</script>
</body>
</html>
```

</details>

---

## 📊 GitHub Статистика

<div align="center">

[![GitHub Stats](https://github-readme-stats.vercel.app/api?username=Nurikgg77&theme=radical&show_icons=true&hide_border=true&count_private=true&bg_color=0f0f23&text_color=ffffff)](https://github.com/Nurikgg77)

[![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Nurikgg77&theme=radical&layout=compact&hide_border=true&bg_color=0f0f23&text_color=ffffff)](https://github.com/Nurikgg77)

</div>

---

## 🚀 Мои Проекты

### 1. 🛍️ E-Commerce Shop Platform
**Полнофункциональный интернет-магазин**
- 🔧 PHP, Laravel, MySQL, HTML5, CSS3, JavaScript
- ✨ Управление товарами, оформление заказов, админ-панель
- 🔗 [Смотреть](https://github.com/Nurikgg77/shop-project)

### 2. 🚗 Car Shop Platform
**Платформа для продажи автомобилей**
- 🔧 Laravel, Blade Templates, PHP, jQuery
- ✨ Расширенный фильтр, рейтинговая система, чат продавца
- 🔗 [Смотреть](https://github.com/Nurikgg77/Car_shop-project)

### 3. 👤 GitHub Profile Repository
**Интерактивный профиль с динамической статистикой**
- 🔧 Markdown, HTML, CSS, GitHub Actions
- ✨ Живые гифки, анимированная статистика, визуализация контрибьютов
- 🔗 [Смотреть](https://github.com/Nurikgg77/Nurikgg77)

---

## 🎓 Ключевые Навыки

| Категория | Описание |
|-----------|---------|
| **Web Development** | Full-Stack Apps, REST APIs, SPA, Responsive Design |
| **Mobile Dev** | Cross-Platform Apps, Native Integration, UI/UX |
| **Databases** | MySQL, Query Optimization, Data Modeling |
| **Frontend** | Modern JavaScript, CSS Animations, Interactive UIs |
| **Backend** | Server Architecture, Authentication, Security |
| **DevOps** | Git, CI/CD Basics, Deployment |

---

## 🌐 Контакты

<div align="center">

[![Telegram](https://img.shields.io/badge/Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/Nurikgg77)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:nurik@example.com)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/nurik_prgrm)
[![TikTok](https://img.shields.io/badge/TikTok-000000?style=for-the-badge&logo=tiktok&logoColor=white)](https://www.tiktok.com/@ggnurik77)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Nurikgg77)

**📍 Ашхабат, Туркменистан 🇹🇲**

</div>

---

<div align="center">

### ⭐ Если тебе нравится мой профиль - оставь звёзду! ⭐

---

**Made with ❤️ by Nurik | © 2026**

</div>
