<template>
    <div>
        <ul class="p-0 mt-1" >
            <li v-for="(todo,index) in todolist" class="div col-12 col-xl-4 d-flex justify-content-center align-content-center text-center mx-auto d-grid gap-4 border-bottom border-white text-bg-secondary p-3">
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
</script>