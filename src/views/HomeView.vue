<template>
  <div class="home">
    <button @click="setShow">Click for pop up</button>
    <PopUpSubs v-if="show" @setShow="setShow"/>
  </div>
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

<style lang="scss" scoped>
.home {
  display: flex;
  height: 100vh;
  align-items: center;
  justify-content: center;

  button {
    font-size: 24px;
    padding: 15px;
  }
}

</style>
