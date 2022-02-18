<template>
    <modal-layout>
        <template v-slot:header>
            <h1>팝업 타이틀</h1>
        </template>
        <template v-slot:main>
            <p>팝업 컨텐츠1</p>
            <p>팝업 컨텐츠2</p>
        </template>
        <template v-slot:footer>
            <button type="button">닫기</button>
        </template>
    </modal-layout>
    <Example />
</template>
<script>
import SlotModalLayout from "./SlotModalLayout";
import Example from "./Example";
export default{
    components:{
        "modal-layout": SlotModalLayout,Example
    },
};
</script>