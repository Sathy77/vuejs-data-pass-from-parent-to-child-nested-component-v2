<template>
    <div class="CheckOddEven">
        {{evenOrOdd()}}
        <PrimeCheck :numberPrimeCheck="numberCheckEvenOdd"></PrimeCheck>
    </div>
</template>
  
<script>
  import PrimeCheck from './PrimeCheck.vue'
  
  export default {
    name: "CheckOddEven",
    props: ["numberCheckEvenOdd"],
    components: {
        PrimeCheck
    },
    methods: {
        evenOrOdd() {
                if (this.numberCheckEvenOdd % 2 == 0) {
                    return `${this.numberCheckEvenOdd} even`;
                }
                else {
                    return `${this.numberCheckEvenOdd} odd`;
                }
            
            
        }
    }
}
</script>
  