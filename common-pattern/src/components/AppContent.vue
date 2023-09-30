<template>
  <div>
    <ul v-for="(item) in items" :key="item.id">
        <li> {{ item.id }} - {{ item.num }}</li>
    </ul>
    <button @click="$emit('increase')">renew items</button>
    <button @click="num++">add num</button> {{  num }}
  </div>
</template>

<script>
export default {
    data() {
        return {
            num :0
        }
    },
    props: {
        items: {
            type: Array,
            required: true,
        }
    },
}
</script>

<style>

</style>