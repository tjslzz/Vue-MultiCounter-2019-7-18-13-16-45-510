<template>
  <div id = "each">
    <p >{{count}}</p>
    <button v-on:click="$emit('addnum')" @click="count ++">我加</button>
    <button  v-on:click="$emit('subnum')" @click="count --">我减</button>
  </div>
</template>
<script>
export default {
    name: 'each',
  data:function(){
    return {
      count : 8,
    }
  }
}
</script>
