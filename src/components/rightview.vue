<template>
  <div id="rightView" class="rightview">
    <div class="rightview__bg"></div>
    <div class="rightview__container">
      <ChatHeader />
      <ChatContainer />
      <ChatFooter />
      <div id="contextMenu" class="contextMenu">
        <div class="contextMenu__tab">
          <span class="contextMenu__tab--text">Contact info</span>
        </div>
        <div class="contextMenu__tab">
          <span class="contextMenu__tab--text">Select messages</span>
        </div>
        <div class="contextMenu__tab">
          <span class="contextMenu__tab--text">Mute notifications</span>
        </div>
        <div class="contextMenu__tab">
          <span class="contextMenu__tab--text">Clear messages</span>
        </div>
        <div class="contextMenu__tab">
          <span class="contextMenu__tab--text">Delete chat</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ChatHeader from "./ChatArea/chatheader";
import ChatContainer from "./ChatArea/chatcontainer";
import ChatFooter from "./ChatArea/chatFooter";

export default {
  name: "Rightview",
  components: {
    ChatHeader,
    ChatContainer,
    ChatFooter
  },
  methods: {
    disableContextMenu() {
      var rightView = document.getElementById("rightView");
      rightView.addEventListener("contextmenu", e => {
        e.preventDefault();
      });
    }
  }
};
</script>

<style lang="scss">
.rightview {
  flex: 70%;
  background-color: #e5ddd5;
  overflow-x: hidden;

  &__bg {
    background-image: url("../assets/Images/whatsappbg.png");
    background-repeat: repeat;
    opacity: 0.06;

    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    overflow-x: hidden;
    z-index: 0;
  }

  &__container {
    display: flex;
    flex-direction: column;
    height: 100%;
  }
}
</style>