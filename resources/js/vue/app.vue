<template>
<div class="todoListContainer">
    <div class="heading">
        <h2 id="title">Todo List</h2>
        <add-item-form @reloadlist="getList()"/>
    </div>

    <button @click="getList">click this to gewy</button>
    <list-view
        :items="items"
        @reloadlist="getList()"
    />
</div>
</template>

<script>
import addItemForm from "./addItemForm";
import listView from "./listView";
export default {
    components: {
        addItemForm,
        listView
    },
    data(){
        return{
            items: []
        }
    },
    methods:{
        getList () {
            axios.get('api/items')
            .then( response => {
                this.items = response.data;
            })
            .catch( error =>{
                console.log(error);
            })
        },
    },
    beforeMount(){
        this.getList()
    },
}
</script>

<style scoped>
    .todoListContainer{
        width: 350px;
        margin: auto;
    }

    .heading{
        background: #e6e6e6;
        padding: 10px;
    }

    #title{
        text-align: center;
    }
</style>
