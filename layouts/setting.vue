<template>
  <a-layout id="components-layout-demo-top-side-2">
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
            Peter Song
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
                <a-icon type="home" />
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

    <a-layout-content style="padding: 50px">
      <a-layout style="padding: 24px 0; background: #fff">
        <a-layout-sider width="200" style="background: #fff">
          <a-menu
            mode="inline"
            :default-selected-keys="['1']"
            style="height: 100%"
          >
            <a-menu-item key="1">
              <span>
                <NuxtLink to="/account"> Profile </NuxtLink>
              </span>
            </a-menu-item>
            <a-menu-item key="2">
              <span>
                <NuxtLink to="/card-info"> Banks & Cards </NuxtLink>
              </span>
            </a-menu-item>
            <a-menu-item key="3">
              <span>
                <NuxtLink to="/order-management/order-list">
                  My Purchase
                </NuxtLink>
              </span>
            </a-menu-item>
          </a-menu>
        </a-layout-sider>
        <a-layout-content :style="{ padding: '0 24px', minHeight: '280px' }">
          <nuxt></nuxt>
        </a-layout-content>
      </a-layout>
    </a-layout-content>
  </a-layout>
</template>

<script>
export default {
  methods: {
    onSearch(value) {},
  },
}
</script>

<style lang="scss">
#components-layout-demo-top-side {
  .logo {
    width: 120px;
    height: 31px;
    background: rgba(255, 255, 255, 0.2);
    margin: 16px 28px 16px 0;
    float: left;
  }
}
</style>
