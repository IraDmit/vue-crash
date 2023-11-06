<template>
  <section class="menu">
    <div class="panel-menu first">
      <div class="bid">
        <input type="text" placeholder="50" id="bid-player" maxlength="3" value="50" />
        <div class="icon">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
            <path
              fill="var(--ci-primary-color, currentColor)"
              d="M291.75,308.1a105.8,105.8,0,1,0,0-211.6H136v32h39.943V276.1H136v32h39.943V352H136v32h39.943v56h32V384H304V352H207.943V308.1ZM207.943,128.5H291.75a73.8,73.8,0,1,1,0,147.6H207.943Z"
              class="ci-primary"
            />
          </svg>
        </div>
      </div>
      <div class="block-bid">
        <div class="item">1.2</div>
        <div class="item">2</div>
        <div class="item">Min</div>
        <div class="item">Max</div>
      </div>
      <div class="factor">X 2</div>
      <div class="block-factor">
        <div class="item">1.2</div>
        <div class="item">2</div>
        <div class="item">Auto</div>
      </div>
      <button class="btn active-btn" id="play" @click="play">Play</button>
    </div>
    <div class="panel-menu second">
      <div class="bid">
        50
        <div class="icon">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
            <path
              fill="var(--ci-primary-color, currentColor)"
              d="M291.75,308.1a105.8,105.8,0,1,0,0-211.6H136v32h39.943V276.1H136v32h39.943V352H136v32h39.943v56h32V384H304V352H207.943V308.1ZM207.943,128.5H291.75a73.8,73.8,0,1,1,0,147.6H207.943Z"
              class="ci-primary"
            />
          </svg>
        </div>
      </div>
      <div class="block-bid">
        <div class="item">1.2</div>
        <div class="item">2</div>
        <div class="item">Min</div>
        <div class="item">Max</div>
      </div>
      <div class="factor">X 2</div>
      <div class="block-factor">
        <div class="item">1.2</div>
        <div class="item">2</div>
        <div class="item active-item">Auto</div>
      </div>
      <button class="btn">Waiting</button>
    </div>
    <div class="wrap">
      <div class="encryption"><span>256-bit </span>encryption</div>
    </div>
  </section>
</template>

<script setup>
let money = 0,
  value = 0,
  players = 0
const play = () => {
  const playerBid = document.querySelector('#bid-player'),
    bet = document.querySelector('#bets')

  if (+playerBid.value !== 0) {
    let i = playerBid.value
    if (i > 100) {
      let inco = setInterval(() => {
        bet.textContent = `${value}.00`

        if (money == +i) {
          clearInterval(inco)
          money = 0
        }
        value++
        money++
      }, 0.1)
    } else {
      let inco = setInterval(() => {
        bet.textContent = `${value}.00`

        if (money == +i) {
          clearInterval(inco)
          money = 0
        }
        value++
        money++
      }, 30)
    }
    playerBid.value = ''
    players++
    document.querySelector('#player').textContent = players
  }
}
</script>

<style lang="scss" scoped>
.menu {
  width: 100%;
  grid-row: 2/3;
  display: flex;
  flex-direction: column;
  gap: 19px;
}
.panel-menu {
  position: relative;
  overflow: hidden;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 32px 32px 32px 50px;
  width: 100%;
  height: 130px;
  border-radius: 45px;
  background-color: #1d212c;
  .item {
    border-radius: 21px;
    background-color: #252a37;
    width: 70px;
    height: 42px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #42495b;
    font-size: 15px;
    font-weight: 700;
    cursor: pointer;
  }
  .active-item {
    background-color: #3f4658;
    color: #fff;
  }
  .btn {
    border: none;
    border-radius: 30px;
    background-color: #252a37;
    color: #fff;
    font-size: 20px;
    font-weight: 700;
    width: 186px;
    height: 66px;
    cursor: pointer;
  }
  .active-btn {
    background-color: #83aff8;
  }
  .bid,
  .factor {
    color: #fff;
    font-size: 23px;
    font-weight: 700;
    cursor: pointer;
    display: flex;
    align-items: center;
    gap: 5px;
  }
  .bid .icon,
  .factor .icon {
    display: flex;
    align-items: center;
  }
  .bid .icon svg,
  .factor .icon svg {
    width: 25px;
    height: 30px;
  }
  .bid .icon svg path,
  .factor .icon svg path {
    fill: #798393;
  }
  .bid::before {
    content: 'Bid';
    position: absolute;
    top: 15px;
    font-size: 18px;
    color: #61687a;
  }
  .factor::before {
    content: 'Factor';
    position: absolute;
    top: 15px;
    font-size: 18px;
    color: #61687a;
  }
}

#bid-player {
  width: 40px;
  background-color: #1d212c;
  border: none;
  color: #fff;
  font-size: 23px;
  font-weight: 700;
  &:focus {
    outline: 0;
  }
}

.wrap {
  display: flex;
  justify-content: end;
}
#bets {
  width: 100px;
}
.encryption {
  position: relative;
  color: #fff;
  font-size: 15px;
  font-weight: 400;
  line-height: 60px;
  span {
    font-weight: 700;
  }
  &::before {
    content: url(@/assets/img/padlock.png);
    position: absolute;
    left: -25px;
    top: 50%;
    transform: translateY(calc(-50% + 3px));
  }
}
.block-bid {
  width: 160px;
  row-gap: 10px;
  justify-content: space-around;
}
.block-bid .item {
  width: 60px;
}
.block-bid .item:last-child {
  width: 60px;
}

.block-factor {
  width: 180px;
  row-gap: 10px;
  justify-content: space-around;
}
.block-factor .item {
  width: 60px;
}
.block-factor .item:last-child {
  width: calc(100% - 20px);
}
@media (max-width: 1050px) {
  .wrap {
    display: none;
  }
  .panel-menu {
    padding: 15px 13px 15px 34px;
  }
  .panel-menu .bid::before {
    content: '';
  }
  .panel-menu .factor::before {
    content: '';
  }
  .panel-menu .btn {
    width: 100px;
    height: 100%;
  }
  .block-bid {
    width: 250px;
    row-gap: 10px;
    justify-content: space-around;
  }
  .block-bid .item:last-child {
    width: 100%;
  }
  .block-factor {
    width: 170px;
    row-gap: 10px;
    justify-content: space-around;
  }
  .block-factor .item:last-child {
    width: 100%;
  }
}
@media (max-width: 768px) {
  .block-bid {
    width: 160px;
    row-gap: 10px;
    justify-content: space-around;
  }
  .block-bid .item {
    width: 60px;
  }
  .block-bid .item:last-child {
    width: 60px;
  }
  .block-factor {
    width: 180px;
    row-gap: 10px;
    justify-content: space-around;
  }
  .block-factor .item {
    width: 60px;
  }
  .block-factor .item:last-child {
    width: calc(100% - 20px);
  }
  .panel-menu .btn {
    width: 80px;
    font-size: 16px;
  }
  .panel-menu .factor {
    width: 30px;
    font-size: 17px;
  }
  .panel-menu #bid-player,
  .panel-menu .bid {
    font-size: 17px;
  }
  .panel-menu #bid-player {
    width: 28px;
  }
}
</style>
