<template>
  <footer class="cxfooter">
    <div class="cxfooter__container">
      <div class="cxfooter__iconview">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24">
          <path
            fill="currentColor"
            d="M9.153 11.603c.795 0 1.439-.879 1.439-1.962s-.644-1.962-1.439-1.962-1.439.879-1.439 1.962.644 1.962 1.439 1.962zm-3.204 1.362c-.026-.307-.131 5.218 6.063 5.551 6.066-.25 6.066-5.551 6.066-5.551-6.078 1.416-12.129 0-12.129 0zm11.363 1.108s-.669 1.959-5.051 1.959c-3.505 0-5.388-1.164-5.607-1.959 0 0 5.912 1.055 10.658 0zM11.804 1.011C5.609 1.011.978 6.033.978 12.228s4.826 10.761 11.021 10.761S23.02 18.423 23.02 12.228c.001-6.195-5.021-11.217-11.216-11.217zM12 21.354c-5.273 0-9.381-3.886-9.381-9.159s3.942-9.548 9.215-9.548 9.548 4.275 9.548 9.548c-.001 5.272-4.109 9.159-9.382 9.159zm3.108-9.751c.795 0 1.439-.879 1.439-1.962s-.644-1.962-1.439-1.962-1.439.879-1.439 1.962.644 1.962 1.439 1.962z"
          />
        </svg>
      </div>
      <div class="cxfooter__textview">
        <input
          type="text"
          autocomplete="off"
          placeholder="Type a message"
          class="cxfooter__textview--input"
        />
      </div>
      <div class="cxfooter__iconview">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24">
          <path
            fill="currentColor"
            d="M11.999 14.942c2.001 0 3.531-1.53 3.531-3.531V4.35c0-2.001-1.53-3.531-3.531-3.531S8.469 2.35 8.469 4.35v7.061c0 2.001 1.53 3.531 3.53 3.531zm6.238-3.53c0 3.531-2.942 6.002-6.237 6.002s-6.237-2.471-6.237-6.002H3.761c0 4.001 3.178 7.297 7.061 7.885v3.884h2.354v-3.884c3.884-.588 7.061-3.884 7.061-7.885h-2z"
          />
        </svg>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "ChatFooter"
};
</script>

<style lang="scss">
.cxfooter {
  position: relative;
  z-index: 1;
  flex: none;
  order: 3;
  box-sizing: border-box;
  width: 100%;
  background-color: #f0f0f0;

  &__container {
      width: 100%;
      position: relative;
      z-index: 2;
      display: flex;
      flex-direction: row;
      align-items: flex-end;
      box-sizing: border-box;
      max-width: 100%;
      min-height: 62px;
      align-items: center;
  }

  &__iconview {
    padding: 5px 10px;
    color: #919191;
  }

  &__textview {
    width: 100%;
    margin: 5px 10px;

      &--input {
          width: 100%;
          padding: 9px 12px 11px;
          border-radius: 2.1rem;
          min-height: 20px;
          font-weight: 400;
          font-size: 15px;
          line-height: 20px;
          outline: none;
          border: none;
          background-color: #fff;
          color: #4a4a4a;
          will-change: width;
      }
  }
}
</style>