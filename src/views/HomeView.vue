<template>
  <div class="home">
    <h1 v-for="(number, index) in numbers" :key="index">
      <lengthCheck :numberForCheck="number"></lengthCheck> 
      <!-- ei file a number variable and other file a numberForCheck name nibe -->
    </h1>
  </div>
</template>

<script>
import lengthCheck from '@/components/lengthCheck.vue'

export default {
  name: 'HomeView',
  components: {
    lengthCheck
  },
  data(){
    return {
      numbers: [[1, 2, 3], [4, 5, 6, 7], [8, 9, 10]]
    }
  }
}
</script>
