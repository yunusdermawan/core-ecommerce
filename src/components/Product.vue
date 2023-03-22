<template>
    <div class="product"
    v-for="item in listItems"
    :key="item.id"
    :price="price"
    >
       <div class="product-inner">
        <div class="product-text-wrap">
            <h2 class="bg-text">{{item.title}}</h2>
        </div>
       </div>
    </div>
</template>
<script>
 export default {
    data() {
        return {
            listItems: []
        }
    },
    methods: {
        async getData() {
            const res = await fetch('https://fakestoreapi.com/products')
            const finalRes = await res.json()
            this.listItems = finalRes
        }
    },
    mounted() {
        this.getData()
    }
 }
</script>
