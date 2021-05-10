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

      </div>
    </section>
    <section class="inventory__body"></section>
    <section class="inventory__footer"></section>
  </article>
</template>

<script>
export default {
  name: 'Inventory',
};
</script>

<style lang="scss" scoped>
.inventory {
  flex: 1;
  display: grid;
  grid-template-rows: auto 1fr auto;
  padding: 15px;
}

.inventory__header {
  display: grid;
  grid-template-columns: repeat(2, 2fr);
  grid-column-gap: 20px;
  padding-bottom: 10px;
  margin-bottom: 10px;

  &_border {
    border-bottom: 1px solid rgba(var(--WhiteRgb), .2);
  }
}

.inventory__body {

}

.inventory__footer {
 padding: 20px;
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
    @include media-font(14px, 14px, 16px, 18px);
    color: var(--Green100);
  }

  &_acc {
    @include media-font(14px, 10px, 12px, 14px);
    color: var(--Grey100);
  }
}

.inventory__switchAll {

}
</style>
