<template>
  <div class="cart-list">
    <a-row>
      <a-col :span="24" class="my-2 xs-mt-0 xs-mb-1">
        <a-card class="p-2">
          <a-row>
            <a-col :xs="1" :sm="1" :md="1" :lg="1">
              <a-checkbox @change="onChange"> </a-checkbox>
            </a-col>
            <a-col class="pl-1" :xs="3" :sm="3" :md="3" :lg="3">
              <p>Product</p></a-col
            >
            <a-col :xs="0" :sm="0" :md="6" :lg="6" :span="6"> </a-col>
            <a-col :xs="0" :sm="0" :md="5" :lg="5"> </a-col>
            <a-col :xs="0" :sm="0" :md="2" :lg="2">
              <p>Unit Price</p>
            </a-col>
            <a-col :xs="0" :sm="0" :md="3" :lg="3">
              <p>Quantity :</p>
            </a-col>
            <a-col :xs="0" :sm="0" :md="2" :lg="2">
              <p>Total Price</p>
            </a-col>
            <a-col :xs="0" :sm="0" :md="2" :lg="2">
              <p>Actions</p>
            </a-col>
          </a-row>
        </a-card>
      </a-col>
      <a-col class="my-1 xs-my-0" :span="24">
        <a-card class="p-2 mb-1">
          <a-row>
            <a-col class="" :xs="2" :sm="2" :md="1" :lg="1">
              <a-checkbox @change="onChange"> </a-checkbox>
            </a-col>
            <a-col class="xs-pr-1" :xs="6" :sm="6" :md="3" :lg="3">
              <a-card>
                <img
                  style="width: 100%; height: 100%"
                  slot="cover"
                  alt="example"
                  src="https://os.alipayobjects.com/rmsportal/QBnOOoLaAfKPirc.png"
                />
              </a-card>
            </a-col>
            <a-col :xs="16" :sm="16" :md="5" :lg="5">
              <p>
                XIAOMI MI SMARTPHONE 12 SERIES XIAOMI MI SMARTPHONE 12 SERIES
              </p>
            </a-col>
            <a-col :xs="24" :sm="24" :md="5" :lg="5">
              <p><strong>Product Options: </strong> Gray,8GB , 256GB</p>
            </a-col>
            <a-col :xs="12" :sm="12" :md="2" :lg="2">
              <h4 style="color: #ee4d2d">RM 200</h4>
            </a-col>
            <a-col :xs="12" :sm="12" :md="3" :lg="3">
              <div>
                <a-input-number
                  id="inputNumber"
                  v-model="value1"
                  :min="1"
                  :max="10"
                  @change="onChange1"
                  size="small"
                />
              </div>
            </a-col>
            <a-col :xs="0" :sm="0" :md="2" :lg="2">
              <p>RM 600</p>
            </a-col>
            <a-col class="xs-pb-1" :xs="0" :sm="0" :md="2" :lg="2">
              <a-button type="link" block :size="small"> Remove </a-button>
            </a-col>
          </a-row>
        </a-card>
        <a-card class="p-2 mb-1">
          <a-row>
            <a-col class="" :xs="2" :sm="2" :md="1" :lg="1">
              <a-checkbox @change="onChange"> </a-checkbox>
            </a-col>
            <a-col class="xs-pr-1" :xs="6" :sm="6" :md="3" :lg="3">
              <a-card>
                <img
                  style="width: 100%; height: 100%"
                  slot="cover"
                  alt="example"
                  src="https://os.alipayobjects.com/rmsportal/QBnOOoLaAfKPirc.png"
                />
              </a-card>
            </a-col>
            <a-col :xs="16" :sm="16" :md="5" :lg="5">
              <p>
                XIAOMI MI SMARTPHONE 12 SERIES XIAOMI MI SMARTPHONE 12 SERIES
              </p>
            </a-col>
            <a-col :xs="24" :sm="24" :md="5" :lg="5">
              <p><strong>Product Options: </strong> Gray,8GB , 256GB</p>
            </a-col>
            <a-col :xs="12" :sm="12" :md="2" :lg="2">
              <h4 style="color: #ee4d2d">RM 200</h4>
            </a-col>
            <a-col :xs="12" :sm="12" :md="3" :lg="3">
              <div>
                <a-input-number
                  id="inputNumber"
                  v-model="value1"
                  :min="1"
                  :max="10"
                  @change="onChange1"
                  size="small"
                />
              </div>
            </a-col>
            <a-col :xs="0" :sm="0" :md="2" :lg="2">
              <p>RM 600</p>
            </a-col>
            <a-col class="xs-pb-1" :xs="0" :sm="0" :md="2" :lg="2">
              <a-button type="link" block :size="small"> Remove </a-button>
            </a-col>
          </a-row>
        </a-card>
        <a-card class="p-2 mb-1">
          <a-row>
            <a-col class="" :xs="2" :sm="2" :md="1" :lg="1">
              <a-checkbox @change="onChange"> </a-checkbox>
            </a-col>
            <a-col class="xs-pr-1" :xs="6" :sm="6" :md="3" :lg="3">
              <a-card>
                <img
                  style="width: 100%; height: 100%"
                  slot="cover"
                  alt="example"
                  src="https://os.alipayobjects.com/rmsportal/QBnOOoLaAfKPirc.png"
                />
              </a-card>
            </a-col>
            <a-col :xs="16" :sm="16" :md="5" :lg="5">
              <p>
                XIAOMI MI SMARTPHONE 12 SERIES XIAOMI MI SMARTPHONE 12 SERIES
              </p>
            </a-col>
            <a-col :xs="24" :sm="24" :md="5" :lg="5">
              <p><strong>Product Options: </strong> Gray,8GB , 256GB</p>
            </a-col>
            <a-col :xs="12" :sm="12" :md="2" :lg="2">
              <h4 style="color: #ee4d2d">RM 200</h4>
            </a-col>
            <a-col :xs="12" :sm="12" :md="3" :lg="3">
              <div>
                <a-input-number
                  id="inputNumber"
                  v-model="value1"
                  :min="1"
                  :max="10"
                  @change="onChange1"
                  size="small"
                />
              </div>
            </a-col>
            <a-col :xs="0" :sm="0" :md="2" :lg="2">
              <p>RM 600</p>
            </a-col>
            <a-col class="xs-pb-1" :xs="0" :sm="0" :md="2" :lg="2">
              <a-button type="link" block :size="small"> Remove </a-button>
            </a-col>
          </a-row>
        </a-card>
        <a-card class="p-2 mb-1">
          <a-row>
            <a-col class="" :xs="2" :sm="2" :md="1" :lg="1">
              <a-checkbox @change="onChange"> </a-checkbox>
            </a-col>
            <a-col class="xs-pr-1" :xs="6" :sm="6" :md="3" :lg="3">
              <a-card>
                <img
                  style="width: 100%; height: 100%"
                  slot="cover"
                  alt="example"
                  src="https://os.alipayobjects.com/rmsportal/QBnOOoLaAfKPirc.png"
                />
              </a-card>
            </a-col>
            <a-col :xs="16" :sm="16" :md="5" :lg="5">
              <p>
                XIAOMI MI SMARTPHONE 12 SERIES XIAOMI MI SMARTPHONE 12 SERIES
              </p>
            </a-col>
            <a-col :xs="24" :sm="24" :md="5" :lg="5">
              <p><strong>Product Options: </strong> Gray,8GB , 256GB</p>
            </a-col>
            <a-col :xs="12" :sm="12" :md="2" :lg="2">
              <h4 style="color: #ee4d2d">RM 200</h4>
            </a-col>
            <a-col :xs="12" :sm="12" :md="3" :lg="3">
              <div>
                <a-input-number
                  id="inputNumber"
                  v-model="value1"
                  :min="1"
                  :max="10"
                  @change="onChange1"
                  size="small"
                />
              </div>
            </a-col>
            <a-col :xs="0" :sm="0" :md="2" :lg="2">
              <p>RM 600</p>
            </a-col>
            <a-col class="xs-pb-1" :xs="0" :sm="0" :md="2" :lg="2">
              <a-button type="link" block :size="small"> Remove </a-button>
            </a-col>
          </a-row>
        </a-card>
      </a-col>
    </a-row>
  </div>
</template>

<script>
export default {
  layout: 'panel',
  data() {
    return {
      value1: 3,
    }
  },
  methods: {
    onChange(e) {
      console.log(`checked = ${e.target.checked}`)
    },
    onChange1(value1) {
      console.log('changed', value1)
    },
  },
}
</script>
