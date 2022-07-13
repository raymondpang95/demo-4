<template>
  <div class="setting">
    <a-layout id="components-layout-demo-top-side-2">
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

      <a-layout-header class="header">
        <div class="header-pc">
          <div class="" type="flex" justify="center" align="middle">
            <div class="header-row px-1">
              <a-row type="flex" justify="center" align="top">
                <a-col :xs="0" :sm="2" :md="2" :lg="2" class="">
                  <NuxtLink to="/">
                    <a-button class="" icon="home" />
                  </NuxtLink>
                </a-col>
                <a-col :xs="16" :sm="20" :md="20" :lg="20" class="">
                  <div class="xs-pl-2">
                    <a-input-search
                      style="text-align: left"
                      placeholder="Input Product Name"
                      @search="onSearch"
                    />
                  </div>
                </a-col>
                <a-col :xs="4" :sm="2" :md="2" :lg="2" class="xs-pl-1">
                  <NuxtLink to="/cart/cart-list">
                    <a-button type="primary" icon="shopping-cart" />
                  </NuxtLink>
                </a-col>
                <a-col :xs="4" :sm="2" :md="2" :lg="2" class="xs-pl-1">
                  <NuxtLink to="/account">
                    <a-icon type="user" style="color: white" />
                  </NuxtLink>
                </a-col>
              </a-row>
            </div>
          </div>
        </div>

        <div class="header-mobile">
          <a-row style="text-align: center">
            <a-col :xs="2" :sm="2" :md="0" :lg="0" class="">
              <NuxtLink to="/">
                <a-icon
                  style="color: white; font-size: 20px"
                  class="pl-2"
                  type="left"
                />
              </NuxtLink>
            </a-col>
            <a-col :xs="18" :sm="20" :md="0" :lg="0" class="">
              <h3 style="color: white">Setting</h3>
            </a-col>
            <a-col :xs="4" :sm="2" :md="0" :lg="0" class="">
              <a-button type="primary" @click="showDrawer">
                <a-icon style="font-size: 20px" type="menu-fold" />
              </a-button>
            </a-col>
          </a-row>

          <a-drawer
            title="Setting"
            placement="right"
            :closable="false"
            :visible="visible"
            :after-visible-change="afterVisibleChange"
            @close="onClose"
          >
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
          </a-drawer>
        </div>
      </a-layout-header>

      <a-layout-content style="min-height: 500px" class="p-4 xs-p-0">
        <a-layout class="content-pc" style="padding: 24px 0; background: #fff">
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

        <a-layout class="content-mobile xs-p-1" style="background: #fff">
          <a-layout-content>
            <nuxt></nuxt>
          </a-layout-content>
        </a-layout>
      </a-layout-content>
    </a-layout>
  </div>
</template>

<script>
export default {
  data() {
    return {
      visible: false,
    }
  },
  methods: {
    onSearch(value) {},
    afterVisibleChange(val) {
      console.log('visible', val)
    },
    showDrawer() {
      this.visible = true
    },
    onClose() {
      this.visible = false
    },
  },
}
</script>

<style lang="scss">
.setting {
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
    .content-mobile {
      display: none;
    }
  }

  @media only screen and (max-width: 576px) {
    .content-pc {
      display: none;
    }
    .header-pc {
      display: none;
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
.layout-footer-background {
  border: solid 1px red;
}

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
