<template>
  <div class="py-8 xs-py-2">
    <a-card class="my-1" title="Credit / Debit Card" :bordered="false">
      <a-button slot="extra" type="primary" @click="showModal">
        Add New Card
      </a-button>
    </a-card>

    <a-card :bordered="false">
      <a-row>
        <a-col :xs="4" :sm="4" :md="4" :lg="4">
          <img
            style="width: 80px; height: 80px; display: block"
            class="m-auto"
            src="https://thefinanser.com/wp-content/uploads/2021/09/bank.jpeg"
          />
        </a-col>
        <a-col style="text-align: center" :xs="16" :sm="16" :md="16" :lg="16">
          <a-row>
            <a-col :xs="24" :sm="24" :md="8" :lg="24">
              <div>may bank</div>
            </a-col>
            <a-col :xs="24" :sm="24" :md="8" :lg="24">
              <div>peter tan</div>
            </a-col>
            <a-col :xs="24" :sm="24" :md="8" :lg="24">*1234</a-col>
          </a-row>
        </a-col>
        <a-col style="text-align: center" :xs="4" :sm="4" :md="4" :lg="4">
          <a-button type="link" block> Delete </a-button>
        </a-col>
      </a-row>
    </a-card>

    <a-modal
      okText="Submit"
      v-model="visible"
      title="New Card Info"
      @ok="handleOk"
    >
      <a-alert
        message="Your card details are protected."
        description="Your card details are protected.
We partner with CyberSource, a VISA company to ensure that your card details are kept safe and secure. Shopee will not have access to your card info."
        type="info"
        show-icon
      />

      <div class="my-2">
        <a-form
          layout="vertical"
          :form="form"
          :label-col="{ span: 24 }"
          :wrapper-col="{ span: 24 }"
          @submit="handleSubmit"
        >
          <a-form-item label="Card Number">
            <a-input
              v-decorator="[
                'card-number',
                {
                  rules: [
                    {
                      required: true,
                      message: 'Please input your card number',
                    },
                  ],
                },
              ]"
            />
          </a-form-item>
          <a-form-item label="Expiry Date (MM/YY)">
            <a-input
              v-decorator="[
                'expiry-date',
                {
                  rules: [
                    {
                      required: true,
                      message: 'Please input your Expiry Date (MM/YY)',
                    },
                  ],
                },
              ]"
            />
          </a-form-item>
          <a-form-item label="CVV">
            <a-input
              v-decorator="[
                'cvv',
                {
                  rules: [
                    {
                      required: true,
                      message: 'Please input your CVV',
                    },
                  ],
                },
              ]"
            />
          </a-form-item>
          <a-form-item label="Name on Card">
            <a-input
              v-decorator="[
                'name-on-card',
                {
                  rules: [
                    {
                      required: true,
                      message: 'Please input your Name on Card',
                    },
                  ],
                },
              ]"
            />
          </a-form-item>
          <a-form-item label="Billing Address">
            <a-input
              v-decorator="[
                'billing-address',
                {
                  rules: [
                    {
                      required: true,
                      message: 'Please input your Billing Address',
                    },
                  ],
                },
              ]"
            />
          </a-form-item>
          <h4>Save card?</h4>
          <p>
            I acknowledge that my card information is saved securely on my
            Shopee account and One Time Password (OTP) might not be required for
            future transactions on Shopee.
          </p>
          <a-switch default-checked @change="onChange" />
          <!-- <a-form-item class="mt-1" style="width: 100%">
            <a-button type="primary" html-type="submit"> Submit </a-button>
          </a-form-item> -->
        </a-form>
      </div>
    </a-modal>
  </div>
</template>
<script>
export default {
  layout: 'setting',
  data() {
    return {
      visible: false,
      form: this.$form.createForm(this, { name: 'coordinated' }),
    }
  },
  methods: {
    onChange(checked) {
      console.log(`a-switch to ${checked}`)
    },
    showModal() {
      this.visible = true
    },
    handleOk(e) {
      console.log(e)
      this.visible = false
    },
    handleSubmit(e) {
      e.preventDefault()
      this.form.validateFields((err, values) => {
        if (!err) {
          console.log('Received values of form: ', values)
        }
      })
    },
  },
}
</script>
