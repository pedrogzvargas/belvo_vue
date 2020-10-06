<template>
  <div>
    <div id="belvo"></div>
    <input type="button" @click="openWidget" value="Abrir Widget">
  </div>
</template>

<script>

export default {
  name: 'belvo',
  head() {
    return {
      script: [
        {src: 'https://cdn.belvo.io/belvo-widget-1-stable.js'},
      ]
    }
  },
  methods: {
    openWidget() {
      let access_token = "token";
      // eslint-disable-next-line no-undef
      belvoSDK.createWidget(access_token, {
        locale: 'es', // 'en' for English or 'pt' for Portuguese
        company_name: "ACME Corp", // the name of the company to be displayed in the first screen
        //institution: 'banamex_mx_retail', // to start the widget directly on a specific institution credentials page
        //institution_types: ['fiscal', 'retail', 'business', 'gig'], // to select the type of institution to show in the widget
        // access_mode: "recurrent", // to specify the type of link to be created from the widget
        country_codes: ['MX', 'CO', 'BR'],
        // callback: (link, institution) => this.successCallbackFunction(link, institution),
        // onExit: (data) => this.onExitCallbackFunction(data),
        // onEvent: (data) => this.onEventCallbackFunction(data)
      }).build();
    }
  }
}
</script>