<template>

  <div>
    <h1>{{ apiValue }}</h1>
    <Tutorial/>
  </div>
</template>

<script>
export default {
  data () {
    return {
      apiValue: '',
    }
  },
  mounted(){
    this.backendData()
  },
  methods:{
    backendData(){
      this.$axios.get('/demo').then(res => {
        this.apiValue = res.data
      })
    }
  }
}
</script>
