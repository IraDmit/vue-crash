<template>
  <aside>
    <div class="top">
      <div class="info-block">
        <div class="icon">
          <img src="@/assets/img/peaple.png" alt="peaple" />
        </div>
        <div class="info">
          <div class="title">Players</div>
          <div class="subtitle" id="player">0</div>
        </div>
      </div>
      <div class="info-block">
        <div class="icon">
          <img src="@/assets/img/wallet.png" alt="wallet" />
        </div>
        <div class="info">
          <div class="title">Bets</div>
          <div class="subtitle" id="bets">0.00</div>
        </div>
      </div>
    </div>
    <div class="rates">
      <div class="rate">
        <div class="info-block">
          <div class="icon">
            <img src="@/assets/img/icon-player-1.png" alt="player" />
          </div>
          <div class="info">
            <div class="title">Poposha</div>
            <div class="subtitle">752.05</div>
          </div>
        </div>
        <div class="factor">x 1.65</div>
        <div class="bid">731.15</div>
      </div>
      <div class="rate">
        <div class="info-block">
          <div class="icon">
            <img src="@/assets/img/icon-player-2.png" alt="player" />
          </div>
          <div class="info">
            <div class="title">Poposha</div>
            <div class="subtitle">752.05</div>
          </div>
        </div>
        <div class="factor green">x 1.65</div>
        <div class="bid">731.15</div>
      </div>
      <div class="rate">
        <div class="info-block">
          <div class="icon">
            <img src="@/assets/img/icon-player-3.png" alt="player" />
          </div>
          <div class="info">
            <div class="title">Poposha</div>
            <div class="subtitle">752.05</div>
          </div>
        </div>
        <div class="factor">x 1.65</div>
        <div class="bid">731.15</div>
      </div>
      <div class="rate">
        <div class="info-block">
          <div class="icon">
            <img src="@/assets/img/icon-player-4.png" alt="player" />
          </div>
          <div class="info">
            <div class="title">Poposha</div>
            <div class="subtitle">752.05</div>
          </div>
        </div>
        <div class="factor red">x 1.65</div>
        <div class="bid">731.15</div>
      </div>
      <div class="rate">
        <div class="info-block">
          <div class="icon">
            <img src="@/assets/img/icon-player-5.png" alt="player" />
          </div>
          <div class="info">
            <div class="title">Poposha</div>
            <div class="subtitle">752.05</div>
          </div>
        </div>
        <div class="factor">x 1.65</div>
        <div class="bid">731.15</div>
      </div>
      <div class="rate">
        <div class="info-block">
          <div class="icon">
            <img src="@/assets/img/icon-player-6.png" alt="player" />
          </div>
          <div class="info">
            <div class="title">Poposha</div>
            <div class="subtitle">752.05</div>
          </div>
        </div>
        <div class="factor">x 1.65</div>
        <div class="bid">731.15</div>
      </div>
      <div class="rate">
        <div class="info-block">
          <div class="icon">
            <img src="@/assets/img/icon-player-7.png" alt="player" />
          </div>
          <div class="info">
            <div class="title">Poposha</div>
            <div class="subtitle">752.05</div>
          </div>
        </div>
        <div class="factor">x 1.65</div>
        <div class="bid">731.15</div>
      </div>
      <div class="rate">
        <div class="info-block">
          <div class="icon">
            <img src="@/assets/img/icon-player-8.png" alt="player" />
          </div>
          <div class="info">
            <div class="title">Poposha</div>
            <div class="subtitle">752.05</div>
          </div>
        </div>
        <div class="factor blue">x 1.65</div>
        <div class="bid">731.15</div>
      </div>
      <div class="disable">Bets are displayed selectively</div>
    </div>
  </aside>
</template>

<script setup></script>

<style lang="scss" scoped>
aside {
  grid-column: 2/3;
  grid-row: 1/3;
  top: 135px;
  border-radius: 70px;
  background-color: #1d212c;
  width: 400px;
  height: 862px;
  padding: 56px 53px 46px 54px;
  display: flex;
  flex-direction: column;
  gap: 54px;
  .top {
    width: 293px;
    height: 42px;
    display: flex;
    justify-content: space-between;
  }
  .info-block {
    display: flex;
    gap: 10px;
  }
  .icon {
    border-radius: 17px;
    background-color: #252a37;
    width: 42px;
    height: 42px;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .info {
    display: flex;
    flex-direction: column;
  }
  .title {
    color: #42495b;
    font-size: 18px;
    font-weight: 700;
  }
  .subtitle {
    color: #fff;
    font-size: 20px;
    font-weight: 700;
  }
}

.rates {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.rate {
  display: flex;
  border-radius: 29px;
  background-color: #252a37;
  width: 292px;
  height: 65px;
  gap: 20px;
  align-items: center;
  padding: 10px 26px 10px 10px;
}
.rate .info-block {
  display: flex;
  gap: 10px;
}
.rate .icon {
  border-radius: 21px;
  width: 45px;
  height: 45px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.rate .info {
  display: flex;
  flex-direction: column;
}
.rate .title {
  color: #fff;
  font-size: 17px;
  font-weight: 700;
}
.rate .subtitle {
  color: #42495b;
  font-size: 15px;
  font-weight: 700;
}
.rate .factor {
  display: flex;
  color: #fff;
  font-size: 15px;
  font-weight: 700;
  border-radius: 13px;
  background-color: #2d3343;
  width: 56px;
  height: 26px;
  align-items: center;
  justify-content: center;
}
.rate .green {
  background-color: #35dc64;
}
.rate .red {
  background-color: #ec4242;
}
.rate .blue {
  background-color: #83aff8;
}
.rate .bid {
  color: #fff;
  font-size: 15px;
  font-weight: 700;
}
.disable {
  margin: 0 auto;
  margin-top: 33px;
  border-radius: 14px;
  background-color: #252a37;
  width: 230px;
  height: 31px;
  color: #fff;
  font-size: 15px;
  font-weight: 400;
  display: flex;
  align-items: center;
  justify-content: center;
}
@media (max-width: 1730px) {
  aside {
    grid-row: auto;
    grid-column: auto;
  }
}
@media (max-width: 376px) {
  aside {
    height: 782px;
    padding: 0;
    justify-content: center;
    align-items: center;
    width: 100%;
    gap: 20px;
  }
  aside .disable {
    margin-top: 10px;
  }
}
</style>
