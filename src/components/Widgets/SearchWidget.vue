<template>
  <div class="searchview">
    <div class="searchview__container">
      <div class="searchview__container--iconview">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24">
          <path
            fill="currentColor"
            d="M15.009 13.805h-.636l-.22-.219a5.184 5.184 0 0 0 1.256-3.386 5.207 5.207 0 1 0-5.207 5.208 5.183 5.183 0 0 0 3.385-1.255l.221.22v.635l4.004 3.999 1.194-1.195-3.997-4.007zm-4.808 0a3.605 3.605 0 1 1 0-7.21 3.605 3.605 0 0 1 0 7.21z"
          />
        </svg>
      </div>
      <input
        type="text"
        placeholder="Search or start new chat"
        class="searchview__container--input"
        autocomplete="false"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "Searchview"
};
</script>

<style lang="scss">
.searchview {
  background-color: #f6f6f6;
  height: 49px;
  position: relative;
  z-index: 1;
  padding-bottom: 1rem;

  &__container {
    padding: 0rem 1.3rem;

    &--iconview {
      position: absolute;
      top: 1.2rem;
      left: 2.4rem;
      color: #919191;
    }

    &--input {
        width: 100%;
        border: none;
        outline: none;
        border-radius: 1.8rem;
        height: 3.5rem;
        margin-top: 0.7rem;
        padding-left: 7rem;
        color: #999;
        font-size: 1.4rem;
        font-family: inherit;
        white-space: nowrap;
        line-height: 2rem;
    }
  }
}
</style>