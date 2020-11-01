<template>
  <div id="app">
    <div class="content">
      <chat-com :current-user="currentUser"></chat-com>
      <user-list :user-list="userList" @choose-user="toggleUser"></user-list>
    </div>
  </div>
</template>

<script>
import ChatCom from "@/components/ChatCom.vue";
import UserList from "@/components/UserList.vue";

export default {
  name: "App",
  components: {
    ChatCom,
    UserList,
  },
  data() {
    return {
      userList: [
        {
          name: "卡莎",
          img: require("./assets/img/1.jpg"),
        },
        {
          name: "阿卡丽",
          img: require("./assets/img/2.jpg"),
        },
        {
          name: "卡莎",
          img: require("./assets/img/3.jpg"),
        },
        {
          name: "阿卡丽",
          img: require("./assets/img/4.jpg"),
        },
        {
          name: "阿卡丽",
          img: require("./assets/img/5.jpg"),
        },
      ],
      currentUser: {},
    };
  },
  methods: {
    toggleUser(index) {
      this.currentUser = this.userList[index];
    },
  },
};
</script>

<style scoped>
.content {
  display: flex;
  width: 800px;
  height: 700px;
  margin: 0 auto;
  background: #fcfcfc;
  border: 1px dotted #eee;
}
</style>
