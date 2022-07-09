<template>
  <div>
    <h2>Account</h2>
    <a-card>
      <a-row>
        <a-col :span="24">
          <a-form layout="vertical" :form="form" @submit="handleSubmit">
            <a-form-item label="E-mail">
              <a-input
                v-decorator="[
                  'email',
                  {
                    rules: [
                      {
                        type: 'email',
                        message: 'The input is not valid E-mail!',
                      },
                      {
                        required: true,
                        message: 'Please input your E-mail!',
                      },
                    ],
                  },
                ]"
              />
            </a-form-item>
            <a-form-item label="Change Password" has-feedback>
              <a-input
                v-decorator="[
                  'password',
                  {
                    rules: [
                      {
                        required: true,
                        message: 'Please input your password!',
                      },
                    ],
                  },
                ]"
                type="password"
              />
            </a-form-item>
            <a-form-item>
              <span slot="label">
                Nickname&nbsp;
                <a-tooltip title="What do you want others to call you?">
                  <a-icon type="question-circle-o" />
                </a-tooltip>
              </span>
              <a-input
                v-decorator="[
                  'nickname',
                  {
                    rules: [
                      {
                        required: true,
                        message: 'Please input your nickname!',
                        whitespace: true,
                      },
                    ],
                  },
                ]"
              />
            </a-form-item>

            <a-form-item>
              <span slot="label"> Address: </span>
              <a-textarea
                v-decorator="[
                  'address',
                  {
                    rules: [
                      {
                        required: true,
                        message: 'Please input your address!',
                        whitespace: true,
                      },
                    ],
                  },
                ]"
              />
            </a-form-item>

            <a-form-item label="Phone Number">
              <a-input
                v-decorator="[
                  'phone',
                  {
                    rules: [
                      {
                        required: true,
                        message: 'Please input your phone number!',
                      },
                    ],
                  },
                ]"
                style="width: 100%"
              >
                <a-select
                  slot="addonBefore"
                  v-decorator="['prefix', { initialValue: '86' }]"
                  style="width: 70px"
                >
                  <a-select-option value="86"> +86 </a-select-option>
                  <a-select-option value="87"> +87 </a-select-option>
                </a-select>
              </a-input>
            </a-form-item>

            <a-form-item>
              <a-button type="primary" html-type="submit"> Update </a-button>
            </a-form-item>
          </a-form>
        </a-col>
      </a-row>
    </a-card>
  </div>
</template>
<script>
export default {
  layout: 'setting',

  beforeCreate() {
    this.form = this.$form.createForm(this, { name: 'register' })
  },
  methods: {
    handleSubmit(e) {
      e.preventDefault()
      this.form.validateFieldsAndScroll((err, values) => {
        if (!err) {
          console.log('Received values of form: ', values)
        }
      })
    },
  },
}
</script>
