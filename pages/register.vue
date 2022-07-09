<template>
  <div class="register">
    <a-row class="py-10">
      <a-col span="8" class=""></a-col>
      <a-col span="8" class="">
        <a-card>
          <h3>Register New Account</h3>
          <div>
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
              <a-form-item label="Password" has-feedback>
                <a-input
                  v-decorator="[
                    'password',
                    {
                      rules: [
                        {
                          required: true,
                          message: 'Please input your password!',
                        },
                        {
                          validator: validateToNextPassword,
                        },
                      ],
                    },
                  ]"
                  type="password"
                />
              </a-form-item>
              <a-form-item label="Confirm Password" has-feedback>
                <a-input
                  v-decorator="[
                    'confirm',
                    {
                      rules: [
                        {
                          required: true,
                          message: 'Please confirm your password!',
                        },
                      ],
                    },
                  ]"
                  type="password"
                  @blur="handleConfirmBlur"
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
              <a-form-item v-bind="tailFormItemLayout">
                <a-checkbox
                  v-decorator="['agreement', { valuePropName: 'checked' }]"
                >
                  I have read the
                  <a href=""> agreement </a>
                </a-checkbox>
              </a-form-item>
              <a-form-item v-bind="tailFormItemLayout">
                <a-button type="primary" html-type="submit">
                  Register
                </a-button>
              </a-form-item>
            </a-form>
          </div>
        </a-card>
      </a-col>
      <a-col span="8" class=""></a-col>
    </a-row>
  </div>
</template>

<script>
export default {
  layout: 'default',

  data() {
    return {
      confirmDirty: false,
      autoCompleteResult: [],
      formItemLayout: {
        labelCol: {
          xs: { span: 24 },
          sm: { span: 8 },
        },
        wrapperCol: {
          xs: { span: 24 },
          sm: { span: 16 },
        },
      },
      tailFormItemLayout: {
        wrapperCol: {
          xs: {
            span: 24,
            offset: 0,
          },
          sm: {
            span: 16,
            offset: 8,
          },
        },
      },
    }
  },

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
    handleConfirmBlur(e) {
      const value = e.target.value
      this.confirmDirty = this.confirmDirty || !!value
    },
    // compareToFirstPassword(rule, value, callback) {
    //   const form = this.form
    //   if (value && value !== form.getFieldValue('password')) {
    //     callback('Two passwords that you enter is inconsistent!')
    //   } else {
    //     callback()
    //   }
    // },
    validateToNextPassword(rule, value, callback) {
      const form = this.form
      if (value && this.confirmDirty) {
        form.validateFields(['confirm'], { force: true })
      }
      callback()
    },
    handleWebsiteChange(value) {
      let autoCompleteResult
      if (!value) {
        autoCompleteResult = []
      } else {
        autoCompleteResult = ['.com', '.org', '.net'].map(
          (domain) => `${value}${domain}`
        )
      }
      this.autoCompleteResult = autoCompleteResult
    },
  },
}
</script>

<style lang="scss"></style>
