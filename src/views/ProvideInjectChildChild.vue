<template>
    <div>Item Length: {{this.items.length}}</div>
</template>
<script>
    export default{
        inject:["itemLength","items"],
    };
</script> 