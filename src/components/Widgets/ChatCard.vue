<template>
  <div class="chatcard">
    <div class="chatcard__imageview">
      <img
        draggable="false"
        :src="require(`@/assets/Images/${chat.image}`)"
        alt="Card"
        class="chatcard__imageview--img"
      />
    </div>
    <div class="chatcard__textview">
      <div class="chatcard__titleview">
        <span :title="chat.name" :class="{ 'fw-500': chat.is_read }" class="chatcard__titleview--title">{{ chat.name }}</span>
        <p class="chatcard__titleview--smtext">{{ chat.time }}</p>
      </div>
      <div class="chatcard__wxtext">
        <div class="chatcard__wxleft">
          <div v-if="chat.is_receiver" :class="{ 'blue-read': chat.is_read }">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 18 18" width="18" height="18">
              <path
                fill="currentColor"
                d="M17.394 5.035l-.57-.444a.434.434 0 0 0-.609.076l-6.39 8.198a.38.38 0 0 1-.577.039l-.427-.388a.381.381 0 0 0-.578.038l-.451.576a.497.497 0 0 0 .043.645l1.575 1.51a.38.38 0 0 0 .577-.039l7.483-9.602a.436.436 0 0 0-.076-.609zm-4.892 0l-.57-.444a.434.434 0 0 0-.609.076l-6.39 8.198a.38.38 0 0 1-.577.039l-2.614-2.556a.435.435 0 0 0-.614.007l-.505.516a.435.435 0 0 0 .007.614l3.887 3.8a.38.38 0 0 0 .577-.039l7.483-9.602a.435.435 0 0 0-.075-.609z"
              />
            </svg>
          </div>
          <span :title="chat.text" :class="{ 'fw-500': chat.counter > 0, 'darker-tx': chat.counter > 0 }" class="chatcard__wxleft--text">{{ chat.text }}</span>
        </div>
        <div class="chatcard__wxright">
          <div v-if="chat.counter != 0" class="chatcard__wxright--badge">
            <span class="chatcard__wxright--text">{{ chat.counter }}</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ChatCard",
  props: {
    chat: {
      type: Object,
      require: false
    }
  }
};
</script>

<style lang="scss">
.chatcard {
  width: 100%;
  display: flex;
  align-items: center;
  height: 7.2rem;
  position: relative;
  transition: all 0.3s;
  cursor: pointer;
  pointer-events: all;
  padding: 1.1rem 0rem;

  &:not(:last-child) {
    border-bottom: 1px solid #f2f2f2;
  }

  &:hover {
    background-color: #f5f5f5;
  }

  &::after {
    content: "";
    width: 100%;
    height: 0;
    position: absolute;
    bottom: -1px;
  }

  &__imageview {
    padding: 0 15px 0 13px;
    margin-top: -1px;
    flex: none;

    &--img {
      object-fit: cover;
      height: 4.9rem;
      width: 4.9rem;
      border-radius: 50%;
    }
  }

  &__textview {
    display: flex;
    flex-direction: column;
    width: 100%;
    padding-right: 1.5rem;
    justify-content: center;
    flex-grow: 1;
    min-width: 0;
    flex-basis: auto;
  }

  &__titleview {
    display: flex;
    flex-direction: row;
    align-items: center;

    &--title {
      margin-right: auto;
      font-family: inherit;
      overflow: hidden;
      white-space: nowrap;
      text-overflow: ellipsis;
      color: #000;
      font-size: 1.65rem;
      font-weight: 400;
      line-height: 2.1rem;
    }

    &--smtext {
      margin-top: 0.3rem;
      margin-left: 0.6rem;
      line-height: 1.4rem;
      color: rgba(0, 0, 0, 0.45);
      font-size: 1.2rem;
      font-weight: 500;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
      max-width: 100%;
    }
  }

  &__wxtext {
    display: flex;
    flex-direction: row;
    align-items: center;
    margin-top: 0.2rem;
    color: rgba(0, 0, 0, 0.8);
  }

  &__wxleft {
    display: flex;
    flex-direction: row;
    align-items: center;
    flex: 1;
    color: rgba(0, 0, 0, 0.3);
    overflow: hidden;

    &--text {
      margin-left: 2px;
      color: rgba(0, 0, 0, 0.6);
      font-size: 1.3rem;
      font-weight: 400;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
      width: 90%;
    }
  }

  &__wxright {
    &--badge {
      padding: 0.3em 0.4em 0.4em;
      text-align: center;
      background-color: #06d755;
      border-radius: 1.1em;
    }

    &--text {
      display: inline-block;
      min-width: 0.9em;
      min-height: 1em;
      color: #fff;
      font-weight: 600;
      font-size: 12px;
      line-height: 1em;
      vertical-align: top;
    }
  }
}

.blue-read {
  color: #00a5f4;
}

.fw-500 {
  font-weight: 500;
}

.darker-tx {
  color: rgba(0, 0, 0, 0.8);
}
</style>