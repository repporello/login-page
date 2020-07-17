<template>
  <q-page class="flex flex-center bg-grey-1">
    <MainPanel 
      :responsive="responsive"
      :minWidth="minWidth" 
      :title="title"
      > 
      <div class="text-left">
        <CTextfield 
          :label="textfields[0].title"
          :placeholder="textfields[0].placeholder"
        />
      </div> 
      <div class="text-left q-pt-md">
        <CTextfield 
          :label="textfields[1].title"
          :placeholder="textfields[1].placeholder"
          :isPwd="textfields[1].isPwd"
          :withLink="textfields[1].withLink"
          :linkText="textfields[1].linkText"
        />
      </div>
      <div class="q-pt-lg text-left">
        <CCheckbox :label="checkboxes[0].label" />
      </div>
      <div class="q-pt-lg">
        <CButton 
          :label="buttons[0].title"
          :bgColor="buttons[0].bgColor"
        />
      </div>
      <div class="q-pt-lg">
        <span>Don't have an account yet? </span> 
        <CLink :label="links[0].label" />.
      </div>
      <div class="row q-pt-xl q-col-gutter-sm">
        <div class="col-12 col-sm-6">
          <CButton 
            :label="buttons[1].title"
            :bgColor="buttons[1].bgColor"
          />
        </div>
        <div class="col-12 col-sm-6">
          <CButton 
            :label="buttons[2].title"
            :bgColor="buttons[2].bgColor"
          />
        </div>
      </div>
    </MainPanel>
  </q-page>
</template>

<script>
import MainPanel from 'components/common/MainPanel.vue';
import CButton from 'components/common/forms/CButton.vue';
import CTextfield from 'components/common/forms/CTextfield.vue';
import CLink from 'components/common/typography/CLink.vue';
import CCheckbox from 'components/common/forms/CCheckbox.vue';

export default {
  name: 'PageIndex',
  components: {
    MainPanel,
    CButton,
    CTextfield,
    CLink,
    CCheckbox
  },

  data () {
    return {
      buttons: [
        {
          title: 'Sign In',
          bgColor: $negativ
        },
        {
          title: 'Sign in with Facebook',
          bgColor: '#3F68B6'
        },
        {
          title: 'Sign in with Google',
          bgColor: '#EC4235'
        }
      ],
      textfields: [
        {
          title: 'Email address: *',
          placeholder: 'Your email address (... @ ...)'
        },
        {
          title: 'Password: *',
          placeholder: '* * * * * * * *',
          isPwd: true,
          linkText: 'Forgot password?',
          withLink: true
        }
      ],
      staySignedIn: false,
      responsive: true,
      minWidth: '560px',
      title: 'Login',
      links: [
        {
          label: 'Register'
        }
      ],
      checkboxes: [
        {
          label: 'Stay signed in'
        }
      ]
    }
  }
}
</script>

