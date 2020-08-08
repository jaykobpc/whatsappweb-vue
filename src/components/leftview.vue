<template>
  <div class="leftview">
      <Headerview />
      <Notification />
      <Searchview />
      <ChatContainer />
  </div>
</template>

<script>
import Headerview from './Widgets/leftHeader';
import Notification from './Widgets/Notification';
import Searchview from './Widgets/SearchWidget';
import ChatContainer from './Widgets/ChatContainer';

export default {
  name: "Leftview",
  components: {
    Headerview,
    Notification,
    Searchview,
    ChatContainer,
  }
};
</script>

<style lang="scss">
.leftview {
  flex: 30%;

  display: flex;
  flex-direction: column;
  height: 100%;
  border-right: 1px solid #dde;
}
</style>