<template>
    <div class="main">
        <div class="main-input">
            <input type="text" v-model="inputToDo" v-on:keyup.enter="onEnter" />
        </div>
        <div class="container">
            <ul>
                <ListItem v-for="el in toDoList">{{ el }}</ListItem>
            </ul>
        </div>
    </div>
</template>
<script>
import ListItem from '../components/listItem.vue'
import listItem from '../components/listItem.vue'
export default{
    components: [
        listItem
    ],
    data() {
        return {
            inputToDo: "",
            toDoList: []
        };
    },
    methods: {
        onEnter() {
            this.toDoList.unshift(this.inputToDo);
            this.inputToDo = "";
        }
    },
    components: { ListItem }
}
</script>
<style>
body{
    background-color: #EEEEEE;
}
input{
    height: 25%;
    width: 70%;
}
.main{
    width: 90vw;
    height: 100vh;
}
.main-input{
    display: flex;
    width: 100%;
    height: 20%;
    
    align-items: center;
    justify-content: center;
}
li{
    margin: 1%;
    font-size: large;
    font-weight: bold;

    display: flex;
    padding-top:3vh;
    padding-bottom:3vh;
    padding-left: 1vw;
    padding-right: 1vw;
    list-style: none;

    border: 1px solid black;

    font-size: large;
    justify-content: space-between;
}
</style>