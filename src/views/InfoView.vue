<script>
import MessageBubble from '../components/MessageBubble.vue'
export default {
  components: {
    MessageBubble
  }
}

</script>


<template>
    <div class="main">
        <p style="text-align: center">
            🚀 Aqo - бот, который поможет вам в управлении рабочим чатом: выдача поручений, соблюдение дисциплины и некоторые дополнительные функции.
        </p>

        <div class="flex-row">
            <div class="col desc">
                <h2>🔇 /ban</h2>
                <p>Команда для блокировки пользователя в чате. Для блокировки ответьте на сообщение пользователя, напишите /ban, а после причину при её наличии.</p>
            </div>
            <div class="col">
                <MessageBubble 
                    senderName="Нарушитель2004" 
                    messageText="Я нарушаю правила 😎"/>

                <MessageBubble 
                    senderName="ЛучшийАдмин2012" 
                    messageText="/ban Нарушение правил" 
                    senderLeft="True" 
                    replyText="Я нарушаю правила 😎" 
                    replyName="Нарушитель2004"/>

                <MessageBubble 
                    senderName="🚀 AqoBot" 
                    messageText="Пользователь БигБоб2004 заблокирован по причине: Нарушение правил"/>
            </div>
        </div>

        <div class="flex-row reverse">
            <div class="col">
                <MessageBubble 
                    senderName="РаботникМесяца1996" 
                    messageText="Я хочу работать!"/>

                <MessageBubble 
                    senderName="Начальник1985" 
                    messageText="/task Приготовить документы" 
                    senderLeft="True" 
                    replyText="Я хочу работать!" 
                    replyName="РаботникМесяца1996"/>

                <MessageBubble 
                senderName="🚀 AqoBot" 
                messageText="Поручение выдано пользователю РаботникМесяца1996: Приготовить документы"/>
            </div>
            <div class="col desc">
                <h2>✍️ /task</h2>
                <p>Команда используются для выдачи поручений пользователю (максимум 5). Для того чтобы выдать поручение: нужно ответить на сообщение нужного участника чата, написать команду и в сообщении с командой указать задачу для пользователя. Если вы хотите случайно выбрать пользователя, то просто напишите: /task Название поручения, без ответа на сообщение.</p>
            </div>
        </div>

        <div class="flex-row">
            <div class="col desc">
                <h2>🗒 /tasks</h2>
                <p>Просто отправьте команду /tasks в чат или личные сообщения бота и проследуйте по понятной и лёгкой инструкции.</p>
            </div>
        </div>

        <div class="flex-row">
            <div class="col desc">
                <h2>🤬 /filter</h2>
                <p>Команда для включения/отключения фильтрации сообщений чата. Напишите команду в чате или личных сообщениях бота и также проследуйте по понятной и лёгкой инструкции.</p>
            </div>
        </div>

        <div class="flex-row reverse">
            <div class="col">
                <MessageBubble 
                    senderLeft="True"
                    senderName="Савелий" 
                    messageText="/weather"/>

                <MessageBubble 
                senderName="🚀 AqoBot" 
                messageText="Погода в сыктывкаре..."/>
            </div>
            <div class="col desc">
                <h2>🌥 /weather</h2>
                <p>Команда для того, чтобы узнать погоду в реальном времени по вашей геолокации. Просто отправьте команду в чате или личных сообщениях бота и проследуйте по понятной и лёгкой инструкции.</p>
            </div>
        </div>

        <div class="flex-row">
            <div class="col desc">
                <h2>👋 /reg</h2>
                <p>Команда для добавления вас в базу данных. Отправьте её в чате и всё.</p>
            </div>

            <div class="col">
                <MessageBubble 
                    senderLeft="True"
                    senderName="Савелий" 
                    messageText="/reg"/>

                <MessageBubble 
                senderName="🚀 AqoBot" 
                messageText="Вы зарегестрированы!"/>
            </div>
        </div>

        <router-link to="/" class="btn">
            ◀️ Назад
        </router-link>
    </div>
</template> 

<style scoped>
    .main {
        display: flex;
        flex-direction: column;
        justify-content: center;
        max-width: 1280px;
    }
    .desc {
        margin: 15px;
    }
    .btn {
        max-width: 200px;
        justify-content: center;
        margin-bottom: 15px;
    }
</style>