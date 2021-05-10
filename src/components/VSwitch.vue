<template>
  <label class="Switch">
    <input type="checkbox" checked class="Input" />
    <div class="Switch__Slider">
      <div class="Toggle__Outer"><div class="Toggle__Inner"></div></div>
    </div>
  </label>
</template>

<script>
export default {
  name: 'VSwitch',
};
</script>

<style lang="scss" scoped>
.Switch {
  --labelWidth: 100px;
  position: relative;
  display: inline-flex;
  cursor: pointer;
  width: var(--labelWidth);
  height: calc(var(--labelWidth) / 2);
}

.Switch__Slider {
  display: flex;
  background: var(--Black);
  border-radius: 25px;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
}

.Input:checked + .Switch__Slider {
  background: var(--Green);
}

.Input:checked + .Switch__Slider > .Toggle__Outer {
  transform: translateX(calc(var(--labelWidth) / 2));
  transition: transform 0.3s ease-in-out;
}

.Label {
  --labelWidth: 100px;
  cursor: pointer;
  display: flex;
  background: var(--Black);
  border-radius: 25px;
  width: var(--labelWidth);
  height: calc(var(--labelWidth) / 2);
  margin-bottom: 20px;
}

.Input {
  display: none;
}

.Toggle__Outer {
  transition: transform 0.3s ease-out;
  display: flex;
  background: var(--Grey200);
  border-radius: 50%;
  width: calc(var(--labelWidth) / 2);
}

.Toggle__Inner {
  background: linear-gradient(300deg, var(--Grey100) 17%, var(--Grey200) 80%);
  border-radius: 50%;
  width: 65%;
  height: 65%;
  margin: auto;
}

.Input:checked + .Toggle__Outer {
  transform: translateX(calc(var(--labelWidth) / 2));
  transition: transform 0.3s ease-in-out;
}
</style>
