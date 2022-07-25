
<template>
<div class="Container">
    <div class="div row col-12 col-xl-4 text-center d-flex flex-column d-grid gap-4 mx-auto text-bg-secondary p-3">
        <h1 class="mb-10">Vue備忘錄</h1>
        <div class="col">
            <span class="col-1">內容:</span> 
            <input class="col-9" type="text" v-model="todotext">
        </div>
        <div class="col">
            <span class="co-1">日期:</span> 
            <input class="col-4" type="date" v-model="tododate">
            <span class="co-1">時間:</span> 
            <input class="col-4" type="time" v-model="todotime">
        </div>
        <div class="col"> 
            <button @click="addtodolist(todotext,tododate,todotime)" class="btn btn-dark col-10">新增</button>
        </div>
    </div>
</div>
</template>

<script>
    export default {
        name:"todoinput",
        data() {
            return {
                todotext:'',
                tododate:'',
                todotime:'',
            }
        },
        methods:{
            addtodolist(todotext,tododate,todotime){
                let tododata  = {text:todotext, date:tododate, time:todotime}
                if(todotext != ''){
                    this.$store.commit("addtodo",tododata)
                }
            }
        },
    }

</script>