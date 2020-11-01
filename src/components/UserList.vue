<template>
  <div class="user-list">
    <h3>用户列表</h3>
    <ul>
      <li
        v-for="(user, index) in userList"
        :key="user.id"
        @click="chooseUser(index)"
      >
        <img :src="user.img" alt="" />
        <span>{{ user.name }}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "UserList",
  props: ["userList"],
  data() {
    return {};
  },
  methods: {
    chooseUser(index) {
      this.$emit("choose-user", index);
    },
  },
};
</script>

<style scoped>
.user-list {
  width: 300px;
  height: 700px;
  background: skyblue;
}
.user-list ul {
  padding: 0 0 0 10px;
}
.user-list ul li {
  display: flex;
  align-items: center;
  cursor: pointer;
}
.user-list ul li img {
  width: 80px;
  height: 80px;
}
</style>