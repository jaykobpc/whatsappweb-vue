<template>
  <div class="wxnotification">
      <div class="wxnotification__container">
          <div class="wxnotification__iconview">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 48 48" width="48" height="48"><path fill="currentColor" d="M24.154 2C11.919 2 2 11.924 2 24.165S11.919 46.33 24.154 46.33s22.154-9.924 22.154-22.165S36.389 2 24.154 2zm-.744 15.428v-.618c0-.706.618-1.324 1.324-1.324s1.323.618 1.323 1.324v.618c2.559.618 4.412 2.823 4.412 5.559v3.176l-8.294-8.294a5.056 5.056 0 0 1 1.235-.441zm1.323 15.706a1.77 1.77 0 0 1-1.765-1.765h3.529a1.768 1.768 0 0 1-1.764 1.765zm7.236-.883l-1.765-1.765H17.233v-.882l1.765-1.765v-4.853a5.56 5.56 0 0 1 .794-2.912l-2.559-2.559 1.147-1.147 14.735 14.736-1.146 1.147z"></path></svg>
          </div>
          <div class="wxnotification__textview">
              <h3 class="wxnotification__textview--title">Get notified of new messages</h3>
              <p class="wxnotification__textview--smtext">Turn on desktop notification</p>
          </div>
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.wxnotification {
    padding: 13px 12px 14px 13px;
    background-color: #9de1fe;
    z-index: 1;

    &__container {
        display: flex;
        align-items: center;
        min-height: 62px;
    }

    &__iconview {
        margin-right: 1.5rem;
        color: #f5fcff;
    }

    &__textview {
        text-decoration: none;
        cursor: pointer;
        
        &--title {
            font-size: 1.6rem;
            line-height: 21px;
            font-weight: 400;
            color: #46555b;
        }

        &--smtext {
            font-size: 1.4rem;
            line-height: 19px;
            font-weight: 400;
            color: #46555b;
            transition: all 0.3s;

            &:hover {
                text-decoration: underline;
            }
        }
    }
}
</style>