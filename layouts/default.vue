<template>
  <div>
    <a-layout id="components-layout-demo-top-side-2">
      <a-layout-header class="header">
        <div type="flex" justify="center" align="middle"></div>
      </a-layout-header>

      <a-layout>
        <div class="m-auto content">
          <a-layout-content
            :style="{
              margin: 0,
              minHeight: '800px',
              width: '1200px',
            }"
          >
            <nuxt></nuxt>
          </a-layout-content>
        </div>
      </a-layout>
    </a-layout>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss">
.border {
  border: solid #fff 1px;
}
</style>
