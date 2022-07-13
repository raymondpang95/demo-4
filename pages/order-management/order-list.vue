<template>
  <div class="py-4">
    <a-card :bordered="false">
      <h2>Order Status</h2>

      <a-tabs default-active-key="1" @change="callback">
        <a-tab-pane key="1" tab="All">
          <a-card class="my-2 xs-p-1">
            <a-row>
              <a-col ::xs="8" :sm="8" :md="4" :lg="4">
                <img
                  style="width: 120px; height: 120px; display: block"
                  class="m-auto xs-ms-0"
                  src="https://myhartono.com/images/thumbnails/400/400/detailed/286/RMX2030_4-64_GREEN.jpg"
                />
              </a-col>
              <a-col :xs="24" :sm="24" :md="18" :lg="18">
                <div>
                  <h4>REALME SMARTPHONE 5I SERIEaaaaaaS</h4>
                </div>
                <div>
                  <h5>64GB x1</h5>
                </div>
              </a-col>
              <a-col :xs="16" :sm="16" :md="18" :lg="18">
                <h4>RM 2362.00</h4>
              </a-col>
              <a-col :span="24">
                <a-row>
                  <a-divider />
                  <a-col :xs="0" :sm="16" :md="20" :lg="20"></a-col>
                  <a-col
                    :xs="24"
                    :sm="8"
                    :md="4"
                    :lg="4"
                    style="text-align: left"
                  >
                    <h4>Total : RM 2362.00</h4>
                  </a-col>
                </a-row>
              </a-col>
            </a-row>
          </a-card>
          <a-card class="my-2 xs-p-1">
            <a-row>
              <a-col ::xs="8" :sm="8" :md="4" :lg="4">
                <img
                  style="width: 120px; height: 120px; display: block"
                  class="m-auto xs-ms-0"
                  src="https://myhartono.com/images/thumbnails/400/400/detailed/286/RMX2030_4-64_GREEN.jpg"
                />
              </a-col>
              <a-col :xs="24" :sm="24" :md="18" :lg="18">
                <div>
                  <h4>REALME SMARTPHONE 5I SERIEaaaaaaS</h4>
                </div>
                <div>
                  <h5>64GB x1</h5>
                </div>
              </a-col>
              <a-col :xs="16" :sm="16" :md="18" :lg="18">
                <h4>RM 2362.00</h4>
              </a-col>
              <a-col :span="24">
                <a-row>
                  <a-divider />
                  <a-col :xs="0" :sm="16" :md="20" :lg="20"></a-col>
                  <a-col
                    :xs="24"
                    :sm="8"
                    :md="4"
                    :lg="4"
                    style="text-align: left"
                  >
                    <h4>Total : RM 2362.00</h4>
                  </a-col>
                </a-row>
              </a-col>
            </a-row>
          </a-card>
        </a-tab-pane>
        <a-tab-pane key="2" tab="To Pay" force-render>
          <a-card class="my-2 xs-p-1">
            <a-row>
              <a-col ::xs="8" :sm="8" :md="4" :lg="4">
                <img
                  style="width: 120px; height: 120px; display: block"
                  class="m-auto xs-ms-0"
                  src="https://myhartono.com/images/thumbnails/400/400/detailed/286/RMX2030_4-64_GREEN.jpg"
                />
              </a-col>
              <a-col :xs="24" :sm="24" :md="18" :lg="18">
                <div>
                  <h4>REALME SMARTPHONE 5I SERIEaaaaaaS</h4>
                </div>
                <div>
                  <h5>64GB x1</h5>
                </div>
              </a-col>
              <a-col :xs="16" :sm="16" :md="18" :lg="18">
                <h4>RM 2362.00</h4>
              </a-col>
              <a-col :span="24">
                <a-row>
                  <a-divider />
                  <a-col :xs="0" :sm="16" :md="20" :lg="20"></a-col>
                  <a-col
                    :xs="24"
                    :sm="8"
                    :md="4"
                    :lg="4"
                    style="text-align: left"
                  >
                    <h4>Total : RM 2362.00</h4>
                  </a-col>
                </a-row>
              </a-col>
            </a-row>
          </a-card>
          <a-card class="my-2 xs-p-1">
            <a-row>
              <a-col ::xs="8" :sm="8" :md="4" :lg="4">
                <img
                  style="width: 120px; height: 120px; display: block"
                  class="m-auto xs-ms-0"
                  src="https://myhartono.com/images/thumbnails/400/400/detailed/286/RMX2030_4-64_GREEN.jpg"
                />
              </a-col>
              <a-col :xs="24" :sm="24" :md="18" :lg="18">
                <div>
                  <h4>REALME SMARTPHONE 5I SERIEaaaaaaS</h4>
                </div>
                <div>
                  <h5>64GB x1</h5>
                </div>
              </a-col>
              <a-col :xs="16" :sm="16" :md="18" :lg="18">
                <h4>RM 2362.00</h4>
              </a-col>
              <a-col :span="24">
                <a-row>
                  <a-divider />
                  <a-col :xs="0" :sm="16" :md="20" :lg="20"></a-col>
                  <a-col
                    :xs="24"
                    :sm="8"
                    :md="4"
                    :lg="4"
                    style="text-align: left"
                  >
                    <h4>Total : RM 2362.00</h4>
                  </a-col>
                </a-row>
              </a-col>
            </a-row>
          </a-card>
        </a-tab-pane>
        <a-tab-pane key="3" tab="Completed">
          <a-card class="my-2 xs-p-1">
            <a-row>
              <a-col ::xs="8" :sm="8" :md="4" :lg="4">
                <img
                  style="width: 120px; height: 120px; display: block"
                  class="m-auto xs-ms-0"
                  src="https://myhartono.com/images/thumbnails/400/400/detailed/286/RMX2030_4-64_GREEN.jpg"
                />
              </a-col>
              <a-col :xs="24" :sm="24" :md="18" :lg="18">
                <div>
                  <h4>REALME SMARTPHONE 5I SERIEaaaaaaS</h4>
                </div>
                <div>
                  <h5>64GB x1</h5>
                </div>
              </a-col>
              <a-col :xs="16" :sm="16" :md="18" :lg="18">
                <h4>RM 2362.00</h4>
              </a-col>
              <a-col :span="24">
                <a-row>
                  <a-divider />
                  <a-col :xs="0" :sm="16" :md="20" :lg="20"></a-col>
                  <a-col
                    :xs="24"
                    :sm="8"
                    :md="4"
                    :lg="4"
                    style="text-align: left"
                  >
                    <h4>Total : RM 2362.00</h4>
                  </a-col>
                </a-row>
              </a-col>
            </a-row>
          </a-card>
          <a-card class="my-2 xs-p-1">
            <a-row>
              <a-col ::xs="8" :sm="8" :md="4" :lg="4">
                <img
                  style="width: 120px; height: 120px; display: block"
                  class="m-auto xs-ms-0"
                  src="https://myhartono.com/images/thumbnails/400/400/detailed/286/RMX2030_4-64_GREEN.jpg"
                />
              </a-col>
              <a-col :xs="24" :sm="24" :md="18" :lg="18">
                <div>
                  <h4>REALME SMARTPHONE 5I SERIEaaaaaaS</h4>
                </div>
                <div>
                  <h5>64GB x1</h5>
                </div>
              </a-col>
              <a-col :xs="16" :sm="16" :md="18" :lg="18">
                <h4>RM 2362.00</h4>
              </a-col>
              <a-col :span="24">
                <a-row>
                  <a-divider />
                  <a-col :xs="0" :sm="16" :md="20" :lg="20"></a-col>
                  <a-col
                    :xs="24"
                    :sm="8"
                    :md="4"
                    :lg="4"
                    style="text-align: left"
                  >
                    <h4>Total : RM 2362.00</h4>
                  </a-col>
                </a-row>
              </a-col>
            </a-row>
          </a-card>
        </a-tab-pane>
      </a-tabs>
    </a-card>
  </div>
</template>

<script>
export default {
  layout: 'setting',

  methods: {
    callback(key) {
      console.log(' ' + key)
    },
  },
}
</script>
