<template>
  <div class="default">
    <a-layout id="components-layout-demo-top-side-2">
      <a-layout-header class="header">
        <div type="flex" justify="center" align="middle"></div>
      </a-layout-header>

      <a-layout>
        <div class="m-auto">
          <a-layout-content class="content" :style="{}">
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
.default {
  overflow: hidden;
  width: 100%;
}
.border {
  // border: solid red 1px;
}

.content {
  margin: 0;
  min-height: 800px;
  width: 1200px;
  @media only screen and (max-width: 576px) {
    width: 100px;
  }
}
</style>
