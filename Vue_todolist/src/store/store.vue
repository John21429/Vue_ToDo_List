
<script>
import Vue from "vue";
import Vuex from 'vuex';

Vue.use(Vuex);

const store = new Vuex.Store({
    state:{
        todolist:[
            {todotext:'打籃球',tododate:'2022-07-25',todotime:'21:30'},
            ],

    },
    actions:{

    },
    mutations:{
        addtodo:function(state,tododata){
            // console.log(tododata)
            state.todolist.push({
                todotext:tododata.text,tododate:tododata.date,todotime:tododata.time
            })
        },
        deletetodolist(){

        },
    },
    getters:{
        
    },
});
export default store;
</script>
