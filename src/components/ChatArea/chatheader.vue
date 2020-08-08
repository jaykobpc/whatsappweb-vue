<template>
  <div class="cxheader">
    <div class="cxheader__imageview">
      <img draggable="false" src="@/assets/Images/image5.jpeg" alt="Profile Image" class="cxheader__imageview--image" />
    </div>
    <div class="cxheader__textview">
      <h3 class="cxheader__textview--title">Jaykob</h3>
      <p class="cxheader__textview--smtext">last seen today at 21:15</p>
    </div>
    <div class="cxheader__iconview">
      <div class="cxheader__iconview--icon">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24">
          <path
            fill="currentColor"
            d="M15.9 14.3H15l-.3-.3c1-1.1 1.6-2.7 1.6-4.3 0-3.7-3-6.7-6.7-6.7S3 6 3 9.7s3 6.7 6.7 6.7c1.6 0 3.2-.6 4.3-1.6l.3.3v.8l5.1 5.1 1.5-1.5-5-5.2zm-6.2 0c-2.6 0-4.6-2.1-4.6-4.6s2.1-4.6 4.6-4.6 4.6 2.1 4.6 4.6-2 4.6-4.6 4.6z"
          />
        </svg>
      </div>
      <div class="cxheader__iconview--icon">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24">
          <path
            fill="currentColor"
            d="M1.816 15.556v.002c0 1.502.584 2.912 1.646 3.972s2.472 1.647 3.974 1.647a5.58 5.58 0 0 0 3.972-1.645l9.547-9.548c.769-.768 1.147-1.767 1.058-2.817-.079-.968-.548-1.927-1.319-2.698-1.594-1.592-4.068-1.711-5.517-.262l-7.916 7.915c-.881.881-.792 2.25.214 3.261.959.958 2.423 1.053 3.263.215l5.511-5.512c.28-.28.267-.722.053-.936l-.244-.244c-.191-.191-.567-.349-.957.04l-5.506 5.506c-.18.18-.635.127-.976-.214-.098-.097-.576-.613-.213-.973l7.915-7.917c.818-.817 2.267-.699 3.23.262.5.501.802 1.1.849 1.685.051.573-.156 1.111-.589 1.543l-9.547 9.549a3.97 3.97 0 0 1-2.829 1.171 3.975 3.975 0 0 1-2.83-1.173 3.973 3.973 0 0 1-1.172-2.828c0-1.071.415-2.076 1.172-2.83l7.209-7.211c.157-.157.264-.579.028-.814L11.5 4.36a.572.572 0 0 0-.834.018l-7.205 7.207a5.577 5.577 0 0 0-1.645 3.971z"
          />
        </svg>
      </div>
      <div class="cxheader__iconview--icon">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24">
          <path
            fill="currentColor"
            d="M12 7a2 2 0 1 0-.001-4.001A2 2 0 0 0 12 7zm0 2a2 2 0 1 0-.001 3.999A2 2 0 0 0 12 9zm0 6a2 2 0 1 0-.001 3.999A2 2 0 0 0 12 15z"
          />
        </svg>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ChatHeader"
};
</script>

<style lang="scss">
.cxheader {
  display: flex;
  align-items: center;
  flex-direction: row;
  padding: 1rem 1.6rem;
  background-color: #ededed;
  z-index: 1000;
  position: relative;
  width: 100%;
  height: 59px;

  &__imageview {
    padding: 0 15px 0 0;
    margin-top: -1px;
    cursor: pointer;

    &--image {
      object-fit: cover;
      height: 4rem;
      width: 4rem;
      border-radius: 50%;
    }
  }

  &__textview {
    display: flex;
    flex-direction: column;
    flex-grow: 1;
    justify-content: center;
    min-width: 0;
    cursor: pointer;
    overflow: hidden;
    white-space: nowrap;

    &--title {
      text-overflow: ellipsis;
      font-weight: 400;
      font-size: 1.6rem;
      line-height: 2.1rem;
      color: #000;
    }

    &--smtext {
      min-height: 20px;
      color: rgba(0, 0, 0, 0.6);
      font-size: 13px;
      line-height: 20px;
    }
  }

  &__iconview {
    margin-left: 2rem;
    display: flex;
    flex-direction: row;
    align-items: center;

    &--icon {
      padding: 0.8rem 0.9rem;
      border-radius: 50%;
      transition: background-color 0.3s ease;
      position: relative;
      color: #919191;
      margin-left: 1rem;
      cursor: pointer;
      transition: background-color 0.3s ease;

      &:hover {
          background-color: #dde;
      }
    }
  }
}
</style>