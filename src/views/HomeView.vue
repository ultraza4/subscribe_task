<template>
  <button @click="setShow">Click for pop up</button>
  <PopUpSubs v-if="show" @setShow="setShow"/>
</template>


<script>
import PopUpSubs from '@/components/PopUpSubs.vue';

export default {
  data() {
    return {
      show: false
    }
  },
  components: {
    PopUpSubs
  },

  methods: {
    setShow() {
      return this.show = this.show ? false : true
    }
  }
}
</script>
