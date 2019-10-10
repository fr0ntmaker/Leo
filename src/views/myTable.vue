<template>
    <div>
<!--        <p>{{msg}}</p>-->
<!--        <h2>{{tableData}}</h2>-->
        <tableData/>
    </div>
</template>

<script>
    import axios from 'axios'
    import tableData from '../components/tableData'
    export default {
        name: "myTable",
        components: {
            tableData
        },
        data(){
            return {
                msg: 'Table should appear here... Soon',
                // tableData: null
            }
        },
        // computed: {
        //     allTable(){
        //         return this.$store.getters.allTable
        //     }
        // },
        // mounted() {
        //     axios
        //         .get('http://192.168.1.17:1717/private/data')
        //         .then(response => {
        //         this.tableData = response.data;
        //     })
        // }
    }
</script>

<style scoped>
p {
    font-size: small;
    color: #7e0c00;
}
</style>