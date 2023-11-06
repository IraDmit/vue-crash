<template>
  <nav class="footer-panel">
    <div class="item">
      <img src="@/assets/img/home.png" alt="home" class="icon" />
      <div class="title">Home</div>
    </div>
    <div class="item">
      <img src="@/assets/img/gift.png" alt="gift" class="icon" />
      <div class="title">Bonus</div>
    </div>
    <div class="item">
      <img src="@/assets/img/logo.png" alt="logo" class="icon" />
      <div class="title active">Crash</div>
    </div>
    <div class="item">
      <img src="@/assets/img/chat.png" alt="chat" class="icon" />
      <div class="title">Chat</div>
    </div>
    <div class="item">
      <img src="@/assets/img/page_list.png" alt="page_list" class="icon" />
      <div class="title">Pages</div>
    </div>
  </nav>
</template>

<script setup></script>

<style lang="scss" scoped>
.footer-panel {
  position: fixed;
  bottom: 0;
  display: none;
  justify-content: space-around;
  align-items: center;
  width: 100%;
  height: 130px;
  border-radius: 70px 70px 0 0;
  background-color: #252a37;
  .item {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 5px;
    .icon {
      width: 40px;
    }
    .title {
      font-size: 21.6px;
      font-weight: 700;
      color: #42495b;
    }
    .active {
      color: #fff;
    }
  }
  @media (max-width: 768px) {
    display: flex;
  }
  @media (max-width: 376px) {
    height: 105px;

    .item {
      .icon {
        width: 30px;
      }
      .title {
        font-size: 18px;
      }
    }
  }
}
</style>
