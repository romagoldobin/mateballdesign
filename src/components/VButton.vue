<template>
  <button class="button button_bGreen">
      <div class="button__content button__content_bgGreen">
        <slot></slot>
      </div>
    </button>
</template>

<script>
export default {
  name: 'Vbutton',
  props: {
    type: String,
  },
};
</script>

<style lang="scss" scoped>
.button {
  all: unset;
  border-radius: 5px;
  cursor: pointer;
  color: var(--White);
  display: inline-flex;
  flex-direction: column;
  min-width: 10ch;
  font-size: 0.875em;
  font-weight: bold;
  text-transform: uppercase;
  overflow: hidden;
  min-height: 44px;
}

.button:active:not(:disabled) {
  transform: scale(0.9);
}

.button:disabled {
  opacity: 0.8;
  cursor: not-allowed;
}

.button_bGreen {
  background: linear-gradient(275deg, var(--Green200) 5%, var(--Green100) 95%);
}

.button:hover {
  transition: 0.2s linear;
}

.button_bGreen:hover:not(:disabled) {
  box-shadow: 0px 4px 15px rgba(10, 200, 50, 0.5);
}

.button_bYellow {
  background: linear-gradient(
    275deg,
    var(--Yellow200) 5%,
    var(--Yellow100) 95%
  );
}

.button_bYellow:hover:not(:disabled) {
  box-shadow: 0px 4px 15px rgba(255, 183, 15, 0.5);
}

.button__content {
  align-items: center;
  display: flex;
  justify-content: center;
  border-radius: 2px;
  flex: 1;
  padding: 0.5em 1em;
  margin: 4px;
}

.button__content_bgGreen {
  background: linear-gradient(275deg, var(--Green100) 5%, var(--Green200) 95%);
}

.button__content_bgYellow {
  background: linear-gradient(
    275deg,
    var(--Yellow100) 5%,
    var(--Yellow200) 95%
  );
}
</style>
