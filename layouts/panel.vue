<template>
  <div>
    <a-layout id="components-layout-demo-top-side-2 ">
      <div class="top-header" type="flex" justify="center" align="middle">
        <a-row
          :style="{
            width: '1200px',
          }"
          class="py-1"
        >
          <a-col :span="20" class=""></a-col>
          <a-col :span="4" class="">
            <NuxtLink to="/login">
              <a-icon type="login" />
            </NuxtLink>
            <span class="mx-2">
              <a-icon type="question-circle" />
            </span>
            <NuxtLink to="/account">
              <a-icon type="user" />
              Peter Tan
            </NuxtLink>
          </a-col>
        </a-row>
      </div>
      <a-layout-header class="header">
        <div class="" type="flex" justify="center" align="middle">
          <div
            :style="{
              width: '1200px',
            }"
          >
            <a-row type="flex" justify="center" align="top">
              <a-col :span="2">
                <NuxtLink to="/">
                  <a-button class="" icon="home" />
                </NuxtLink>
              </a-col>
              <a-col class="py-2" :span="20"
                ><a-input-search
                  placeholder="input search text"
                  enter-button
                  @search="onSearch"
              /></a-col>
              <a-col class="" :span="2">
                <NuxtLink to="/cart/cart-list">
                  <a-button type="primary" class="" icon="shopping-cart" />
                </NuxtLink>
              </a-col>
            </a-row>
          </div>
        </div>
      </a-layout-header>

      <a-layout>
        <div class="mx-auto">
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
export default {
  methods: {
    onSearch(value) {},
  },
}
</script>

<style lang="scss">
.border {
  // border: solid #f5f5f5 1px;
  border: solid red 1px;
}
</style>
