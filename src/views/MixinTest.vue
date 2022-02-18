<template>
    <div>
        <button type="button" @click="getProductList">조회</button>
        <table>
            <thead>
                <tr>
                    <th>제품명</th>
                    <th>가격</th>
                    <th>배송료</th>
                    <th>카테고리</th>
                </tr>
            </thead>
            <tbody>
                <tr :key="i" v-for="(product,i) in productList">
                    <td>{{product.product_name}}</td>
                    <td>{{product.price}}</td>
                    <td>{{product.delivery_price}}</td>
                    <td>{{product.category}}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>
<script>
    import MonitoringMixin from '../monitoring.js';

    export default{
        name:'',
        mixins:[MonitoringMixin],
        components:{},
        data() {
            return{
                productList:[]
            };
        },
        setup() {},
        beforecreate(){

        },
        created() {},
        beforemount(){

        },
        mounted() {
            console.log('컴포넌트 mounted()');
        },
        beforeupdate(){},
        updated(){},
        beforeunmount(){},
        unmounted() {},
        methods:{
            async getProductList(){
                this.productList = await this.$api('http://localhost:8080/ServerData','get',{});
                console.log(this.productList);
            },
        }
    }
</script>