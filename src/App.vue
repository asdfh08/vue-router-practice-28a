<template>
  <div id="app">
    <header class="app-header">
      <h1>Vue Router Практика - Занятие 28</h1>
      <p>Изучаем маршрутизацию в Vue.js</p>
    </header>

    <nav class="main-nav">
      <router-link to="/" class="nav-link">Главная</router-link>
      <router-link to="/profile" class="nav-link">Профиль</router-link>
      <router-link to="/settings" class="nav-link">Настройки</router-link>
      <router-link to="/profile/1" class="nav-link">Профиль #1</router-link>
      <router-link to="/profile/2" class="nav-link">Профиль #2</router-link>
      <router-link to="/non-existent-page" class="nav-link">404 Тест</router-link>
    </nav>

    <main class="main-content">
      <router-view></router-view>
    </main>

    <footer class="app-footer">
      <p>Vue 3 + Vue Router • Практическое занятие 28</p>
      <p>Кафедра Индустриального программирования • 2025/2026 учебный год</p>
    </footer>
  </div>
</template>

<script setup>
// Composition API без дополнительной логики
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: #f5f5f5;
  color: #333;
  line-height: 1.6;
}

#app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.app-header {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 2rem;
  text-align: center;
}

.app-header h1 {
  margin-bottom: 0.5rem;
  font-size: 2.5rem;
}

.app-header p {
  opacity: 0.9;
  font-size: 1.1rem;
}

.main-nav {
  background-color: #2c3e50;
  padding: 1rem 2rem;
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
  justify-content: center;
}

.nav-link {
  color: white;
  text-decoration: none;
  padding: 0.75rem 1.5rem;
  border-radius: 25px;
  transition: all 0.3s ease;
  border: 2px solid transparent;
}

.nav-link:hover {
  background-color: #34495e;
  transform: translateY(-2px);
}

.nav-link.router-link-active {
  background-color: #42b883;
  border-color: #42b883;
}

.main-content {
  flex: 1;
  padding: 2rem;
  max-width: 1200px;
  margin: 0 auto;
  width: 100%;
}

.app-footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 1.5rem;
  margin-top: auto;
}

.app-footer p {
  margin: 0.25rem 0;
  opacity: 0.9;
}
</style>