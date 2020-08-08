<template>
  <div class="root-container">
    <Leftview />
    <Rightview />
  </div>
</template>

<script>
import Leftview from './leftview';
import Rightview from './rightview';

export default {
  name: "AppView",
  components: {
    Rightview,
    Leftview
  }
};
</script>

<style lang="scss">
.root-container {
  position: absolute;
  display: flex;
  flex-direction: row;
  width: 100%;
  height: 100%;
  top: 0;
  background-color: #f6f6f6;
}
</style>