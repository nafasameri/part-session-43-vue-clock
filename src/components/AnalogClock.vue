<template>
  <div class="clock mobile__analogclock">
    <div class="mobile__analogclock__cycle"></div>
    <div class="mobile__analogclock__hour-hand"></div>
    <div class="mobile__analogclock__minute-hand"></div>
    <div class="mobile__analogclock__second-hand"></div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.mobile {
  &__analogclock {
    display: flex;
    justify-content: center;
    align-items: center;
    $clock-color: rgb(239, 239, 239);
    width: 200px;
    height: 200px;
    background-color: $clock-color;
    border-radius: 50%;
    border: 1px solid white;
    margin: 20px;
    position: relative;
    box-shadow: -1px -1px 2px 1px rgba(0, 0, 0, 0.49);
    -webkit-box-shadow: -1px -1px 2px 1px rgba(0, 0, 0, 0.49);
    -moz-box-shadow: -1px -1px 2px 1px rgba(0, 0, 0, 0.49);

    &__cycle {
      width: 7px;
      height: 7px;
      border: 3px solid red;
      border-radius: 50%;
      background-color: $clock-color;
      z-index: 999;
    }

    &__hour-hand {
      background-color: black;
      width: 4px;
      height: 60px;
      border-radius: 2px;
      transform: rotate(130deg);
      position: absolute;
      top: 88px;
      left: 120px;
    }

    &__minute-hand {
      background-color: black;
      width: 3px;
      height: 80px;
      border-radius: 2px;
      transform: rotate(60deg);
      position: absolute;
      top: 41px;
      left: 130px;
    }

    &__second-hand {
      background-color: red;
      width: 3px;
      height: 90px;
      border-radius: 2px;
      transform: rotate(320deg);
      position: absolute;
      top: 20px;
      left: 70px;
    }
  }
}
</style>
