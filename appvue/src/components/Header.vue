<template>
    <header>
        <h1>{{title}}</h1>
        <Button  
            :title="showAddTask ? 'close Task': 'add Task'"  
            :color="showAddTask ? 'red': 'green'" 
            @btn-click="$emit('toggle')">
        </Button>
        <!-- <Button title="update Task" color="blue"></Button>
        <Button title="Delete Task" color="red"></Button> -->
    </header>
</template>


<script>
    import Button from "./Button"

    export default {
        name: "Header",
        props: {
            title:String,
            showAddTask:Boolean,
            
        },
        components:{
            Button
        }
    }
</script>

<style scoped>
    header{
        display:flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }

</style>
