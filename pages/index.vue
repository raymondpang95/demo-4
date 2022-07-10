<template>
  <div type="flex" justify="center" align="middle">
    <div
      :style="{
        width: '1200px',
      }"
    >
      <div class="content-top my-4">
        <a-row>
          <a-col :span="6">
            <div class="category mx-2">
              <a-menu style="width: 256px" mode="vertical" @click="handleClick">
                <a-sub-menu key="sub1">
                  <span slot="title"><span>Display Panel</span></span>
                  <a-menu-item key="3"> Option 3 </a-menu-item>
                  <a-menu-item key="4"> Option 4 </a-menu-item>
                </a-sub-menu>
                <a-sub-menu key="sub2">
                  <span slot="title"><span>Home Audio</span></span>
                  <a-menu-item key="7"> Option 7 </a-menu-item>
                  <a-menu-item key="8"> Option 8 </a-menu-item>
                  <a-menu-item key="9"> Option 9 </a-menu-item>
                  <a-menu-item key="10"> Option 10 </a-menu-item>
                </a-sub-menu>
                <a-sub-menu key="sub2">
                  <span slot="title"><span>Computer</span></span>
                </a-sub-menu>
                <a-sub-menu key="sub2">
                  <span slot="title"><span>Smart Phone</span></span>
                </a-sub-menu>
              </a-menu>
            </div>
          </a-col>

          <a-col :span="18">
            <div class="banner mx-2">
              <a-carousel arrows>
                <div
                  slot="prevArrow"
                  class="custom-slick-arrow"
                  style="left: 10px; z-index: 1"
                >
                  <a-icon type="left-circle" />
                </div>
                <div
                  slot="nextArrow"
                  class="custom-slick-arrow"
                  style="right: 10px"
                >
                  <a-icon type="right-circle" />
                </div>
                <div><h3>1</h3></div>
                <div><h3>2</h3></div>
                <div><h3>3</h3></div>
                <div><h3>4</h3></div>
              </a-carousel>
            </div>
          </a-col>
        </a-row>
      </div>
      <div class="content-middle my-4">
        <div class="product-list p-2">
          <a-card title="Product Name" :bordered="true">
            <a-row>
              <a-col :xs="24" :sm="12" :md="8" :lg="4">
                <NuxtLink to="/products/detail">
                  <a-card class="mx-1" hoverable>
                    <img
                      style="width: 100%; height: 100%"
                      slot="cover"
                      alt="example"
                      src="https://myhartono.com/images/thumbnails/80/80/detailed/288/RMX2020_3-32_RED.jpg"
                    />
                    <a-card-meta title="Europe Street beat">
                      <template slot="description">
                        www.instagram.com
                      </template>
                    </a-card-meta>
                  </a-card>
                </NuxtLink>
              </a-col>
              <a-col :xs="24" :sm="12" :md="8" :lg="4">
                <NuxtLink to="/products/detail">
                  <a-card class="mx-1" hoverable>
                    <img
                      slot="cover"
                      alt="example"
                      src="https://myhartono.com/images/thumbnails/80/80/detailed/288/RMX2020_3-32_RED.jpg"
                    />
                    <a-card-meta title="Europe Street beat">
                      <template slot="description">
                        www.instagram.com
                      </template>
                    </a-card-meta>
                  </a-card>
                </NuxtLink>
              </a-col>
              <a-col :xs="24" :sm="12" :md="8" :lg="4">
                <NuxtLink to="/products/detail">
                  <a-card class="mx-1" hoverable>
                    <img
                      slot="cover"
                      alt="example"
                      src="https://myhartono.com/images/thumbnails/80/80/detailed/288/RMX2020_3-32_RED.jpg"
                    />
                    <a-card-meta title="Europe Street beat">
                      <template slot="description">
                        www.instagram.com
                      </template>
                    </a-card-meta>
                  </a-card>
                </NuxtLink>
              </a-col>
              <a-col :xs="24" :sm="12" :md="8" :lg="4">
                <NuxtLink to="/products/detail">
                  <a-card class="mx-1" hoverable>
                    <img
                      slot="cover"
                      alt="example"
                      src="https://myhartono.com/images/thumbnails/80/80/detailed/288/RMX2020_3-32_RED.jpg"
                    />
                    <a-card-meta title="Europe Street beat">
                      <template slot="description">
                        www.instagram.com
                      </template>
                    </a-card-meta>
                  </a-card>
                </NuxtLink>
              </a-col>
              <a-col :xs="24" :sm="12" :md="8" :lg="4">
                <NuxtLink to="/products/detail">
                  <a-card class="mx-1" hoverable>
                    <img
                      slot="cover"
                      alt="example"
                      src="https://myhartono.com/images/thumbnails/80/80/detailed/288/RMX2020_3-32_RED.jpg"
                    />
                    <a-card-meta title="Europe Street beat">
                      <template slot="description">
                        www.instagram.com
                      </template>
                    </a-card-meta>
                  </a-card>
                </NuxtLink>
              </a-col>
              <a-col :xs="24" :sm="12" :md="8" :lg="4">
                <NuxtLink to="/products/detail">
                  <a-card class="mx-1" hoverable>
                    <img
                      slot="cover"
                      alt="example"
                      src="https://myhartono.com/images/thumbnails/80/80/detailed/288/RMX2020_3-32_RED.jpg"
                    />
                    <a-card-meta title="Europe Street beat">
                      <template slot="description">
                        www.instagram.com
                      </template>
                    </a-card-meta>
                  </a-card>
                </NuxtLink>
              </a-col>
            </a-row>
          </a-card>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'panel',
  name: 'IndexPage',
  methods: {
    handleClick(e) {
      console.log('click ', e)
    },
  },
}
</script>
<style lang="scss">
.ant-carousel {
  .slick-slide {
    text-align: center;
    height: 160px;
    line-height: 160px;
    background: #364d79;
    overflow: hidden;
  }
}

.ant-carousel {
  .custom-slick-arrow {
    width: 25px;
    height: 25px;
    font-size: 25px;
    color: #fff;
    background-color: rgba(31, 45, 61, 0.11);
    opacity: 0.3;
  }
}
.ant-carousel {
  .custom-slick-arrow:before {
    display: none;
  }
}
.ant-carousel {
  .custom-slick-arrow:hover {
    opacity: 0.5;
  }
}

.ant-carousel {
  .slick-slide h3 {
    color: #fff;
  }
}
</style>
