<template>
  <div class="panel">
    <a-layout id="components-layout-demo-top-side-2" class="">
      <div class="top-header" type="flex" justify="center" align="middle">
        <a-row class="py-1 top-header-row xs-py-0">
          <a-col :xs="0" :sm="12" :md="8" :lg="20" class=""></a-col>
          <a-col :xs="0" :sm="4" :md="4" :lg="4" class="">
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

      <a-layout-header class="header-pc">
        <div class="" type="flex" justify="center" align="middle">
          <div class="header-row px-1">
            <a-row type="flex" justify="center" align="top">
              <a-col :xs="0" :sm="0" :md="2" :lg="2" class="">
                <NuxtLink to="/">
                  <a-button class="" icon="home" />
                </NuxtLink>
              </a-col>
              <a-col :xs="0" :sm="0" :md="20" :lg="20" class="">
                <div class="xs-pl-2">
                  <a-input-search
                    style="text-align: left"
                    placeholder="Input Product Name"
                    @search="onSearch"
                  />
                </div>
              </a-col>
              <a-col :xs="0" :sm="0" :md="2" :lg="2" class="xs-pl-1">
                <NuxtLink to="/cart/cart-list">
                  <a-button type="primary" icon="shopping-cart" />
                </NuxtLink>
              </a-col>
            </a-row>
          </div>
        </div>
      </a-layout-header>

      <a-layout-header class="header-mobile">
        <a-col :xs="2" :sm="2" :md="0" :lg="0" class="pl-1">
          <NuxtLink to="/">
            <a-button class="back-button" shape="circle" icon="left" />
          </NuxtLink>
        </a-col>
        <a-col :xs="18" :sm="20" :md="0" :lg="0" class="">
          <h3 style="color: white"></h3>
        </a-col>
        <a-col :xs="4" :sm="2" :md="0" :lg="0" class=""></a-col>
      </a-layout-header>

      <a-layout class="mx-auto layout">
        <div class="content-row">
          <a-layout-content>
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
.panel {
  overflow: hidden;
  width: 100%;
  .top-header-row {
    width: 1200px;
  }
  .header-row {
    width: 1200px;
  }
  .content-row {
    margin: 0;
    min-height: 400px;
    width: 1200px;
  }
  @media only screen and (min-width: 1364px) {
    .header-mobile {
      display: none;
    }
  }
  @media only screen and (max-width: 576px) {
    .header-pc {
      display: none;
    }
    .header-mobile {
      background-color: transparent;
      position: fixed;
      top: 0;
      left: 0;
      z-index: 101;
      width: 100%;
      .back-button {
        background: rgba(0, 0, 0, 0.26) !important;
        color: white;
      }
    }
    .d-none {
      display: none;
    }
    .top-header-row {
      width: 100%;
    }
    .header-row {
      width: 100%;
    }
    .layout {
      margin: 0;
      .content-row {
        width: 100%;
        max-width: 100%;
      }
    }
  }
}
.border {
  // border: solid #f5f5f5 1px;
  border: solid red 1px !important;
}
</style>
