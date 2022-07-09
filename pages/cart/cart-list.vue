<template>
  <div class="cart-list">
    <a-row>
      <a-col :span="24" class="my-2">
        <a-card>
          <a-row>
            <a-col :span="1">
              <a-checkbox @change="onChange"> </a-checkbox>
            </a-col>
            <a-col :span="3"> <p>Product</p></a-col>
            <a-col :span="6"> </a-col>
            <a-col :span="5"> </a-col>
            <a-col :span="2">
              <p>Unit Price</p>
            </a-col>
            <a-col :span="3">
              <p>Quantity :</p>
            </a-col>
            <a-col :span="2">
              <p>Total Price</p>
            </a-col>
            <a-col :span="2">
              <p>Actions</p>
            </a-col>
          </a-row>
        </a-card>
      </a-col>
      <a-col :span="24" class="my-1">
        <a-card>
          <a-row>
            <a-col :span="1">
              <a-checkbox @change="onChange"> </a-checkbox>
            </a-col>
            <a-col :span="3"> Image </a-col>
            <a-col :span="6">
              <p>XIAOMI MI SMARTPHONE 12 SERIES</p>
            </a-col>
            <a-col :span="5">
              <p>Product Options: Gray,8GB , 256GB</p>
            </a-col>
            <a-col :span="2">
              <p>RM 200</p>
            </a-col>
            <a-col :span="3">
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
            <a-col :span="2">
              <p>RM 600</p>
            </a-col>
            <a-col :span="2">
              <a-button type="link" block :size="small"> Delete </a-button>
            </a-col>
          </a-row>
        </a-card>
      </a-col>
      <a-col class="my-1" :span="24">
        <a-card>
          <a-row>
            <a-col :span="1">
              <a-checkbox @change="onChange"> </a-checkbox>
            </a-col>
            <a-col :span="3"> Image </a-col>
            <a-col :span="6">
              <p>XIAOMI MI SMARTPHONE 12 SERIES</p>
            </a-col>
            <a-col :span="5">
              <p>Product Options: Gray,8GB , 256GB</p>
            </a-col>
            <a-col :span="2">
              <p>RM 200</p>
            </a-col>
            <a-col :span="3">
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
            <a-col :span="2">
              <p>RM 600</p>
            </a-col>
            <a-col :span="2">
              <a-button type="link" block :size="small"> Delete </a-button>
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
