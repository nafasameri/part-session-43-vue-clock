<template>
  <div class="mobile__digitalclock">
    <div class="mobile__digitalclock__hour">04</div>
    :
    <div class="mobile__digitalclock__min">08</div>
    :
    <div class="mobile__digitalclock__sec">51</div>
  </div>
  <div class="mobile__description">
    Select a section from digital clock then change value from analog clock
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.mobile {
  &__digitalclock {
    display: flex;
    padding: 5px;
    font-family: "roboto";
    font-size: 50px;
    position: relative;

    &__hour::after + &__hour:active {
        content: '';
        background-color: darkblue;
        width: 33%;
        height: 3px;
        position: absolute;
        left: 0px;
        bottom: 0px;
        border-radius: 3px;
    }

    &__min::after + &__min:hover{
        content: '';
        background-color: darkblue;
        width: 33%;
        height: 3px;
        position: absolute;
        left: 33%;
        bottom: 0px;
        border-radius: 3px;
    }

    &__sec::after {
        content: '';
        background-color: darkblue;
        width: 33%;
        height: 3px;
        position: absolute;
        left: 66%;
        bottom: 0px;
        border-radius: 3px;
    }
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
</style>