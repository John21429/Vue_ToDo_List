<template>
    <div>
        <ul class="p-0 mt-1" >
            <li v-for="(todo,index) in todolist" class="div d-flex justify-content-center align-content-center text-center w-25 mx-auto d-grid gap-4 border-bottom border-secondary text-bg-secondary p-3">
                <p>{{todo.todotext}}</p>
                <p>{{todo.tododate}}</p>
                <p>{{todo.todotime}}</p>
                <button @click="deletetodo" type="button" class="btn-close btn-close-white" aria-label="Close"></button>
            </li>
        </ul>
    </div>
</template>

<script>

export default {
    name:"item",
    data() {
        return {
            todolist : this.$store.state.todolist
        }
    },
    computed:{

    },
    methods: {
        deletetodo(e){
            console.log(e.target.parentNode)
            let todoLi = e.target.parentNode
            todoLi.remove();
        }
    },
}
    window.addEventListener('load',()=>{
        let div = document.querySelectorAll('div');
        for(let i = 0; i <= div.length; i++){
            if(window.innerWidth < 576){
                // console.log(div);
                div[i].classList.toggle("w-25");
            }
        }

    })
</script>

<style>
ul{
    box-sizing: border-box;
}
li:first-child{
    box-sizing: border-box;
    border-top: 1px solid darkgray;
}
@media (max-width: 576px){
    .div{
        width: 100% !important;
    }
}
@media screen and (max-width: 576px){
        .div{
        width: 100% !important;
    }
}
</style>