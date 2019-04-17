<template lang="html">
  <div>
    <sample :title="indexTitle">
      <div class="come">
        slot example
      </div>
      <nuxt-link to="/about">
        ABOUT
      </nuxt-link>
    </sample>
  </div>
</template>

<script>
export default {
}
</script>

<style lang="css" scoped>
</style>

<script>
import Sample from '~/components/Sample.vue'

export default {
  components: {
    Sample
  },
  data(){
    return{
      indexTitle:'Nuxt.js data'
    }
  }
}
</script>

<style>

</style>
