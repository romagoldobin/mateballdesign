<template>
  <article class="inventory">
    <section class="inventory__header inventory__header_border">
      <div class="inventory--info">
        <div class="inventory--info__header">
          <span>Выбрано:</span>
        </div>
        <div class="inventory--info__values">
          <span class="inventory--info__value inventory--info__value_selected">
            $ 222.25
          </span>
          <span class="inventory--info__value inventory--info__value_acc">
             / $ 1010.42
          </span>
        </div>
      </div>
      <div class="inventory--switchAll">
        <span class="inventory--switchAll__text">Выбрать все:</span>
        <VSwitch />
      </div>
    </section>
    <section class="inventory__body"></section>
    <section class="inventory__footer">
      <VButton color="Grey">Вывести</VButton>
      <VButton color="Green">Маркет</VButton>
    </section>
  </article>
</template>

<script>
import VSwitch from './VSwitch.vue';
import VButton from './VButton.vue';

export default {
  name: 'Inventory',
  components: {
    VSwitch,
    VButton,
  },
};
</script>

<style lang="scss" scoped>
.inventory {
  flex: 1;
  display: grid;
  grid-template-rows: auto 1fr auto;
  padding: 15px;

  @media (min-width: 1920px) {
    padding: 20px;
  }
}

.inventory__header {
  display: grid;
  grid-template-columns: repeat(2, 2fr);
  grid-column-gap: 10px;
  padding-bottom: 10px;
  margin-bottom: 10px;

  &_border {
    border-bottom: 1px solid rgba(var(--WhiteRgb), .2);
  }

  @media (min-width: 1920px) {
    padding-bottom: 15px;
    margin-bottom: 15px;
  }
}

.inventory__body {

}

.inventory__footer {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-column-gap: 14px;
  padding-top: 10px;
}

.inventory--info {

}

.inventory--info__header {
  @include media-font(10px, 10px, 12px, 14px);
  margin-bottom: 8px;
}

.inventory--info__values {
  font-weight: 600;
}

.inventory--info__value {
  &_selected {
    @include media-font(14px, 12px, 14px, 18px);
    color: var(--Green100);
  }

  &_acc {
    @include media-font(14px, 10px, 12px, 14px);
    color: var(--Grey100);
  }
}

.inventory--switchAll {
  @include media-font(8px, 8px, 10px, 12px);
  display: flex;
  align-items: center;
  justify-content: flex-end;

  .Switch {
     @media (min-width: 1440px) {
      --labelWidth: 36px;
    }

    @media (min-width: 1920px) {
      --labelWidth: 40px;
    }
  }
}

.inventory--switchAll__text {
  @include media-font(10px, 8px, 12px, 14px);
  margin-right: 8px;
  text-overflow: ellipsis;
  white-space: nowrap;
  overflow: hidden;
}
</style>
