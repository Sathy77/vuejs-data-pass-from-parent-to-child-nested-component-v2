<template>
    <div class="PrimeCheck">

        {{prime()}}
    </div>
</template>
  
<script>
export default {
    name: 'PrimeCheck',
    props: ['numberPrimeCheck'],
    methods:{
        prime(){
            if (this.numberPrimeCheck==1)
            {
                return `${this.numberPrimeCheck} not prime`
            }
            else if (this.numberPrimeCheck==2)
            {
                return `${this.numberPrimeCheck} prime`
            }
    
            else {
                if( this.numberPrimeCheck%2==1)
                {
                    for(var x = 2; x < this.numberPrimeCheck/2; x++)
                    {
                        if(this.numberPrimeCheck % x === 0)
                        {
                            return `${this.numberPrimeCheck} not prime`
                        }
                    }
                    return `${this.numberPrimeCheck} prime`
                }
                else {
                return `${this.numberPrimeCheck} not prime`
                }
            }
            
        }
    }
  }
</script>
  