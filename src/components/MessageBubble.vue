<script>
export default {
  props: {
    senderName: String,
    senderLeft: Boolean,
    messageText: String,
    replyName: String,
    replyText: String
  }
}
</script>

<template>
  <div v-bind:class = "(senderLeft)?'sender-left':'sender-right'">
    <span class="sender-name">
      {{ senderName }}
    </span>
    <span v-bind:class = "(replyText)?'reply-text':'none'">
      <b>{{ replyName }}</b>
      {{ replyText }}
    </span>
    <span class="message-text">
      {{ messageText }}
    </span>
  </div>
</template>

<style scoped>
  .sender-left {
    margin-right: 50px;
  }
  .sender-right {
    margin-left: 50px;
  }
  div {
    background: linear-gradient(95.89deg, #3D6EB8 0%, rgba(85, 166, 224, 0.49) 100%);
    border-radius: 15px;
    color: white;
    padding: 5px;
    margin: 5px;
    display: flex;
    flex-direction: column;
    min-width: 250px;
    max-width: 500px;
  }
  .sender-name {
    font-weight: 500;
    display: flex;
    justify-content: right;
    margin-right: 5px;
    color: #d3d3d3;
  }
  .message-text {
    padding: 3px;
  }
  .reply-text {
    border-left: 1px solid white;
    padding: 3px;
    margin-left: 5px;
    padding: 5px;
    display: flex;
    flex-direction: column;
  }
  .none {
    display: none;
  }
</style>