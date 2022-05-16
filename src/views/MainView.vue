<template>
  <transition name="fade">
    <div id="app">
        <div class="logo">
            <img src="/public/aqo.svg"/>
            <span>Aqo</span>
        </div>
        <hr>
        <span class="bot-desc">
            🌟 Бот, который упростит управление вашим рабочим чатом
        </span>
        <div class="flex-row">
            <a class="btn" href="https://t.me/AqoTgBot" target="_blank">
                🛠 Перейти к боту
            </a>

            <router-link to="/info" class="btn">
                ℹ️ Подробнее
            </router-link>
        </div>
    </div>
  </transition>
</template> 

<style scoped>
    #app {
        justify-content: center !important;
    }
    hr {
        width: 100%;
    }
    .logo {
        display: flex;
        flex-direction: column;
        filter: drop-shadow(0px 0px 15px rgba(255, 255, 255, 0.25));
    }
    .logo img {
        height: 128px;
    }
    .logo span {
        font-weight: 400;
        text-align: center;
        font-size: 64px;
    }
    .bot-desc {
        display: flex;
        justify-content: center;
        text-align: center;
        max-width: 400px;
    }
</style>