<template>
  <div class="header">
    <div class="left">
      <img src="@/assets/img/logo_h.png" alt="logo_h" class="logo" />
      <div class="title">Banter</div>
    </div>
    <div class="right">
      <img src="@/assets/img/profile.png" alt="profile" class="icon-profile" />
      <div class="item">
        <div class="balance">8923.44</div>
        <div class="menu"><img src="@/assets/img/plus.png" alt="plus" /></div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
.header {
  width: 100%;
  display: none;
  justify-content: space-between;
  padding-bottom: 37px;
  .left {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 200px;
    .logo {
      width: 41px;
      height: 66px;
    }
    .title {
      font-size: 45px;
      line-height: 90px;
      font-weight: 700;
      color: #fff;
    }
  }
  .right {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 245px;
  }
  .icon-profile {
    width: 61px;
    height: 61px;
  }
  .item {
    width: 175px;
    height: 61px;
    border-radius: 24px;
    background-color: #252a37;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px;
    .balance {
      font-size: 21px;
      line-height: 67px;
      font-weight: 700;
      color: #fff;
    }
    .menu {
      width: 43px;
      height: 43px;
      border-radius: 17px;
      background-color: #2d3341;
      padding: 13px;
      img {
        width: 100%;
      }
    }
  }
  @media (max-width: 768px) {
    display: flex;
  }
  @media (max-width: 376px) {
    padding-bottom: 0;

    .left {
      width: 160px;
      .title {
        font-size: 35px;
      }
    }

    .right {
      width: 165px;
      .icon-profile {
        width: 41px;
        height: 41px;
      }
      .item {
        padding: 8px;
        width: 115px;
        height: 45px;
        .balance {
          font-size: 16px;
        }
        .menu {
          width: 30px;
          height: 30px;
          border-radius: 10px;
          background-color: #2d3341;
          padding: 8px;
        }
      }
    }
  }
}
</style>
