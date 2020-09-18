<template>
  <q-page class="flex flex-center">
    <q-btn color="primary" icon="facebook" label="Get Details" @click="getDetails" />
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  methods:{
    getDetails(){
      facebookConnectPlugin.login(['public_profile','email'],function(success){
        alert(JSON.stringify(success));
      },function(failure){
        alert('Failure!');
      })
    }
  }
}
</script>
