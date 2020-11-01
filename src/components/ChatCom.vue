<template>
  <div class="chat-com">
    <h3>聊天框</h3>
    <p>{{ currentUser.name }}</p>
  </div>
</template>

<script>
export default {
  name: "ChatCom",
  props: ["currentUser"],
};
</script>

<style scoped>
.chat-com {
  width: 500px;
}
</style>