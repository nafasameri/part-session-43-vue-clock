<template>
  <div class="mobile">
    <AnalogClock />
    <DigitalClock />
  </div>
</template>

<script>
import AnalogClock from "./AnalogClock.vue";
import DigitalClock from "./DigitalClock.vue";
export default {
  data() {
    return {
      value: "",
    };
  },
  components: { DigitalClock, AnalogClock },
};
</script>

<style lang="scss">
body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: lightsteelblue;
  margin: 0;

  .mobile {
    $mobile-color: rgb(234, 234, 234);
    display: flex;
    justify-content: center;
    align-items: center;
    width: 300px;
    height: 600px;
    background-color: $mobile-color;
    border-radius: 10px;
    padding: 10px;
    border: 1px solid white;
    -moz-box-shadow: inset 10px 10px 10px rgba(255, 255, 255, 0.4),
      inset -10px -10px 10px rgba(0, 0, 0, 0.4);
    -webkit-box-shadow: inset 10px 10px 10px rgba(255, 255, 255, 0.4),
      inset -10px -10px 10px rgba(0, 0, 0, 0.4);
    box-shadow: inset 10px 10px 10px rgba(255, 255, 255, 0.4),
      inset -10px -10px 10px rgba(0, 0, 0, 0.4);
    margin: 0;
    flex-wrap: wrap;

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

    &__digitalclock {
      padding: 5px;
      font-family: "roboto";
      font-size: 50px;
    }

    &__description {
      padding: 18px;
      font-family: "roboto";
      text-align: center;
      font-weight: bold;
      font-size: 16px;
      color: gray;
    }
  }
}
</style>