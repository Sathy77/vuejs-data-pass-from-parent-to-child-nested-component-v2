<template>
    <div class="lengthCheck">
        {{checkLenth()}}
        <h1 v-for="(number, index) in numberForCheck" :key="index">
            <checkEvenOdd :numberCheckEvenOdd="number"></checkEvenOdd>

        </h1>
    </div>
</template>
  
<script>
  import checkEvenOdd from '@/components/checkEvenOdd.vue'
  export default {
    name: "lengthCheck",
    components: {
        checkEvenOdd
 },
    props: ["numberForCheck"],
    
    methods: {
        checkLenth() {
            return this.numberForCheck.length
        }
    }
}
</script>
  