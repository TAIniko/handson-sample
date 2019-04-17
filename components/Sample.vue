<template lang="html">
  <div class="sample">
    <h1>{{ title }}</h1>
    Hello I'm {{ name }}!
    <button type="button" name="button" @click="plus">
      click times:{{ num }}
    </button>
    <div>
      {{ reverse }}
    </div>
    <div :class="['hide',{ seven: num === 7}]">
      Click 7 times !
    </div>
    <div class="slot">
      <slot />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Default title'
    }
  },
  data() {
    return {
      name: 'Sumi',
      num: 0
    }
  },
  computed: {
    reverse() {
      return this.name.split('').reverse().join('')
    }
  },
  mounted() {
    console.log('mounted')
  },
  methods: {
    plus() {
      this.num++
    }
  }
}
</script>

<style lang="css" scoped>
.hide{
  display:none;
  }
  .seven{
    display:block;
  }
  .slot{
    color:red;
  }
</style>
