<template>
  <div class="chatcontainer">
    <ChatCard v-for="data in chatListData" :key="data.id" :chat="data" />
  </div>
</template>

<script>
import ChatCard from "./ChatCard";

export default {
  name: "ChatContainer",
  computed: {
    chatListData() {
      return this.$store.state.chatList;
    }
  },
  components: {
    ChatCard
  }
};
</script>

<style lang="scss">
.chatcontainer {
  display: flex;
  flex-direction: column;
  overflow-y: auto;
  z-index: 1;
  position: relative;
  background-color: #fff;
  height: 100%;
}
</style>