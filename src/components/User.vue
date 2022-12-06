<template>
    <div>
       <user-list v-for="(item , index) in items" :key="item.pnum" :item="item" :index="index" @delete-item="deleteItem" v-show="index >0"></user-list>
    </div>
</template>

<script>

import UserList from  './UserList.vue';

export default {
    props: ['items'],
    components: {
        UserList,
    },
    methods: {
        deleteItem(item){
            const itemIndex = this.items.indexOf(item);
            this.items.splice(itemIndex ,1);
            console.log('text')
        },
       
    },
}
</script>

<style>

</style>