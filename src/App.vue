<template>
  <div id="fixed-headbar">
    <div id="fixed-headbar-content">
      <FixedHeadbar />
    </div>
  </div>

</template>

<script>
import FixedHeadbar from './components/head/FixedHeadBar.vue'

export default {
  components: {
    FixedHeadbar
  },

  data () {
    return {
      user: null
    }
  }
}
</script>

<style scoped>
  #fixed-headbar {
    position: relative;
    height: 32px;
    width: 100%;
    background-color: #f2f2f2;
    border-bottom: 1px solid #e5e5e5;
  }

  #fixed-headbar-content {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    display: flex;
    justify-content: space-between;
    width: 80%;
    margin: auto;
    height: 24px;
    min-width: 1000px;
  }
</style>
