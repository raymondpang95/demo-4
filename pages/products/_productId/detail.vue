<template>
  <div class="product-detail">
    <div class="mt-4 mb-2">
      <a-breadcrumb>
        <a-breadcrumb-item>Home</a-breadcrumb-item>
        <a-breadcrumb-item><a href="">Category</a></a-breadcrumb-item>
        <a-breadcrumb-item><a href="">Product Name</a></a-breadcrumb-item>
      </a-breadcrumb>
    </div>
    <a-card class="py-2">
      <a-row type="flex">
        <a-col class="py-2 px-1 border" :span="10">
          <a-carousel arrows dots-class="slick-dots slick-thumb">
            <a slot="customPaging" slot-scope="props">
              <img :src="getImgUrl(props.i)" />
            </a>
            <div v-for="item in 4" :key="item.index">
              <img :src="baseUrl + 'abstract0' + item + '.jpg'" />
            </div>
          </a-carousel>
        </a-col>
        <a-col :span="14" class="px-1">
          <a-row>
            <a-col class="border" :span="24">
              <h2>Sony WI-XB400 Extra Bass Wireless In-Ear Headphones</h2>
            </a-col>
            <a-col class="border" :span="24">
              <a-row>
                <a-col class="border p-1" :span="8">
                  4.9 <a-rate v-model="value" />
                </a-col>
                <a-col class="border p-1" :span="8"> 400 Ratings </a-col>
                <a-col class="border p-1" :span="8"> 500 Pre Order </a-col>
              </a-row>
              <a-col class="border" :span="24">
                <a-card class="my-1">
                  <h2>$ 180.00</h2>
                  <p>
                    <a-icon type="check-circle" class="mr-1" /> 100% Authentic
                    Guarantee
                  </p>
                </a-card>
              </a-col>
              <a-col class="border my-1" :span="24"
                >Protection : Extended Warranty
              </a-col>
              <a-col class="border my-1" :span="24"
                >Shipping : Free shipping
              </a-col>

              <a-col class="border my-1" :span="24"
                >Product Options :
                <div class="py-2">
                  <a-radio-group default-value="a" size="default">
                    <a-radio-button value="a"> A </a-radio-button>
                    <a-radio-button value="b"> B </a-radio-button>
                    <a-radio-button value="c"> C </a-radio-button>
                    <a-radio-button value="d"> D </a-radio-button>
                  </a-radio-group>
                </div>
              </a-col>

              <a-col class="border my-1" :span="24">
                <div class="py-2">
                  Quantity :
                  <a-input-number
                    id="inputNumber"
                    v-model="value1"
                    :min="1"
                    :max="10"
                    @change="onChange"
                  />
                  {{ value1 }}
                </div>
              </a-col>

              <a-col class="border my-1" :span="24">
                <a-button size="large" class="mr-1" icon="shopping-cart">
                  Add to Cart
                </a-button>
                <a-button size="large" type="primary"> BUY NOW </a-button>
              </a-col>

              <a-col class="border my-1" :span="24">
                <a-row>
                  <a-col class="border" :span="8">
                    <a-tag color="blue" class="">
                      <a-icon type="safety" />
                      100% Authentic
                    </a-tag>
                  </a-col>

                  <a-col class="border" :span="8">
                    <a-tag color="blue" class="">
                      <a-icon type="undo" />
                      15 Days Return
                    </a-tag>
                  </a-col>

                  <a-col class="border" :span="8">
                    <a-tag color="blue" class="">
                      <a-icon type="safety" />
                      Free Shipping
                    </a-tag>
                  </a-col>
                </a-row>
              </a-col>
            </a-col>
          </a-row>
        </a-col>
      </a-row>
    </a-card>

    <a-card class="my-2 p-2">
      <div style="background-color: #fafafa" class="specifications-title p-2">
        <h3>Product Specifications</h3>
      </div>
      <div class="specifications-content p-2">
        <p>Brand Sony</p>
        <p>Connection Type Wireless</p>
        <p>Earphone, Headphone, & Headset Type In Ear</p>
        <p>Audio Compatibility Mobile</p>
      </div>
    </a-card>

    <a-card class="my-2 p-2">
      <div style="background-color: #fafafa" class="description-title p-2">
        <h3>Product Description</h3>
      </div>
      <div class="description-content p-2">
        <p>
          SPECIFICATIONS & FEATURES : The WI-XB400 are fully wireless,
          effortlessly portable and deliver a deep, punchy sound. The headphones
          have up to 15 hours of battery life and a neckband style, so they’ll
          slip right into your pocket or bag. - EXTRA BASS™ for deep, punchy
          sound - Bluetooth® wireless technology for unrestricted movement - Up
          to 15 hours battery life and quick charging - Easy hands-free calling
          and voice assistant commands with microphone - Comfortable neckband
          style with magnetic buds for easy carrying
        </p>
      </div>
    </a-card>

    <a-card class="my-2 p-2">
      <div
        type="blue"
        style="background-color: #fafafa"
        class="rating-title p-2"
      >
        <h3>Product Ratings</h3>
      </div>
      <div class="rating-content p-2">
        <a-row>
          <a-col class="border" :span="24">
            <a-comment>
              <template slot="actions">
                <span key="comment-basic-like"> </span>
              </template>
              <a slot="author">Han Solo</a>
              <a-avatar
                slot="avatar"
                src="https://zos.alipayobjects.com/rmsportal/ODTLcjxAfvqbxHnVXCYX.png"
                alt="Han Solo"
              />

              <p slot="content">
                <a-rate style="font-size: 14px" v-model="value" />
                We supply a series of design principles, practical patterns and
                high quality design resources (Sketch and Axure), to help people
                create their product prototypes beautifully and efficiently.
              </p>
              <a-tooltip
                slot="datetime"
                :title="moment().format('YYYY-MM-DD HH:mm:ss')"
              >
                <span>{{ moment().fromNow() }}</span>
              </a-tooltip>
            </a-comment>
          </a-col>
          <a-col class="border" :span="24">
            <a-comment>
              <template slot="actions">
                <span key="comment-basic-like"> </span>
              </template>
              <a slot="author">Han Solo</a>

              <a-avatar
                slot="avatar"
                src="https://zos.alipayobjects.com/rmsportal/ODTLcjxAfvqbxHnVXCYX.png"
                alt="Han Solo"
              />
              <p slot="content">
                <a-rate style="font-size: 14px" v-model="value" />
                We supply a series of design principles, practical patterns and
                high quality design resources (Sketch and Axure), to help people
                create their product prototypes beautifully and efficiently.
              </p>
              <a-tooltip
                slot="datetime"
                :title="moment().format('YYYY-MM-DD HH:mm:ss')"
              >
                <span>{{ moment().fromNow() }}</span>
              </a-tooltip>
            </a-comment>
          </a-col>
        </a-row>
      </div>

      <a-pagination v-model="current" :total="50" show-less-items />
    </a-card>

    <div class="product-list">
      <a-card title="Similar Product" :bordered="true">
        <a-row>
          <a-col :span="4">
            <a-card class="mx-1" hoverable>
              <img
                slot="cover"
                alt="example"
                src="https://os.alipayobjects.com/rmsportal/QBnOOoLaAfKPirc.png"
              />
              <a-card-meta title="Europe Street beat">
                <template slot="description"> www.instagram.com </template>
              </a-card-meta>
            </a-card>
          </a-col>

          <a-col :span="4">
            <a-card class="mx-1" hoverable>
              <img
                slot="cover"
                alt="example"
                src="https://os.alipayobjects.com/rmsportal/QBnOOoLaAfKPirc.png"
              />
              <a-card-meta title="Europe Street beat">
                <template slot="description"> www.instagram.com </template>
              </a-card-meta>
            </a-card>
          </a-col>

          <a-col :span="4">
            <a-card class="mx-1" hoverable>
              <img
                slot="cover"
                alt="example"
                src="https://os.alipayobjects.com/rmsportal/QBnOOoLaAfKPirc.png"
              />
              <a-card-meta title="Europe Street beat">
                <template slot="description"> www.instagram.com </template>
              </a-card-meta>
            </a-card>
          </a-col>

          <a-col :span="4">
            <a-card class="mx-1" hoverable>
              <img
                slot="cover"
                alt="example"
                src="https://os.alipayobjects.com/rmsportal/QBnOOoLaAfKPirc.png"
              />
              <a-card-meta title="Europe Street beat">
                <template slot="description"> www.instagram.com </template>
              </a-card-meta>
            </a-card>
          </a-col>

          <a-col :span="4">
            <a-card class="mx-1" hoverable>
              <img
                slot="cover"
                alt="example"
                src="https://os.alipayobjects.com/rmsportal/QBnOOoLaAfKPirc.png"
              />
              <a-card-meta title="Europe Street beat">
                <template slot="description"> www.instagram.com </template>
              </a-card-meta>
            </a-card>
          </a-col>

          <a-col :span="4">
            <a-card class="mx-1" hoverable>
              <img
                slot="cover"
                alt="example"
                src="https://os.alipayobjects.com/rmsportal/QBnOOoLaAfKPirc.png"
              />
              <a-card-meta title="Europe Street beat">
                <template slot="description"> www.instagram.com </template>
              </a-card-meta>
            </a-card>
          </a-col>
        </a-row>
      </a-card>
    </div>
  </div>
</template>

<script>
import moment from 'moment'
const baseUrl =
  'https://raw.githubusercontent.com/vueComponent/ant-design-vue/master/components/vc-slick/assets/img/react-slick/'
export default {
  layout: 'panel',
  data() {
    return {
      baseUrl,
      value: 2,
      value1: 3,
      moment,
      current: 2,
    }
  },
  methods: {
    getImgUrl(i) {
      return `${baseUrl}abstract0${i + 1}.jpg`
    },
    onChange(value) {
      console.log('changed', value)
    },
  },
}
</script>
<style lang="scss">
.border {
  border: solid #fff 1px;
}

.product-detail {
  .ant-carousel {
    .slick-dots {
      height: auto;
    }
    .slick-slide {
      height: 100%;
      width: 100%;
      background-color: #fff;
      img {
        display: block;
        margin: auto;
        width: 100%;
        height: 100%;
      }
    }
  }
}

.ant-carousel {
  .slick-thumb {
    // bottom: -60px;
  }
}
.ant-carousel {
  .slick-thumb li {
    width: 60px;
    height: 45px;
  }
}
.ant-carousel {
  .slick-thumb li img {
    width: 100%;
    height: 100%;
    filter: grayscale(100%);
  }
}
.ant-carousel {
  .slick-thumb li.slick-active img {
    filter: grayscale(0%);
  }
}
</style>
