<template>
  <div class="text-center">
    <h2 class="text-3xl font-bold">{{text}}</h2>
    <div class="text-2xl mt-4 mb-10">{{timestamp}} </div>

  </div>
</template>

<script>
import { format, parseISO } from 'date-fns'
export default {
name: 'DataTitle',
props: ['text', 'dataDate'],
computed: {
  timestamp: function(){
    console.log(this.dataDate)
    return format(parseISO(this.dataDate), 'MMMM do yyyy p')
  }
}
}
</script>