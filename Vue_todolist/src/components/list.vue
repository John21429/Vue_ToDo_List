<script>
import todoinput from './todoinput.vue'
import item from './item.vue'

export default{
    name:"list",
    data() {
        return {
            task:[],
        }
    },
    components:{
        todoinput,
        item,
    }
}
</script>

<template>
    <div >
        <todoinput />
        <item />
    </div>
</template>