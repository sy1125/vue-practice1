<template>
    <div>
        <button type="button" @click="showData">부모버튼</button>
        <ChildComponent ref="child_component" />
    </div>
</template>
<script>
    import ChildComponent from './ChildComponent'; 

    export default{
        name:'',
        components:{ChildComponent},
        data() {
            return{

            }; 
        },
        computed: {
            msg(){
                return this.$refs.child_component.msg;
            }
        },
        setup() {},
        created() {},
        mounted() {},
        unmounted() {},
        methods:{
            showData(){
                alert(this.msg);
            }
        }
    }
</script>
