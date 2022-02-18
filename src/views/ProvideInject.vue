<template>
    <div>
        <ProvideInjectChild />
        <Search />
    </div>
</template>
<script>
    import ProvideInjectChild from "./ProvideInjectChild";
    import Search from "./Search";
    export default{
        components:{ ProvideInjectChild, Search },
        data() {
            return{
                items: ["A", "B"],
            };
        },
        provide(){
            return{
                itemLength:this.items.length,
                items:this.items,
            };
        },
    };
</script>