<template>
    <div class="container">
        <!--TODO Anvendelses kode skal videregives så koden kan anvendes-->
<h1>Filter din søgning</h1>

        <Tilstand mainType="Tilstand"></Tilstand>
        <Tilstand mainType="Energi"></Tilstand>
        <Tilstand mainType="Helpdesk"></Tilstand>
        <Diagram/>
        <totalResult/>
        <searchResult/>

    </div>


</template>

<script>

    import Tilstand from './properties/Tilstand.vue'
    import totalResult from './properties/totalResult.vue'
    import Diagram from "./Diagram";
    import searchResult from './properties/searchResult.vue'
    export default {
        name: "Properties",
        components: {
            Diagram,
            Tilstand,
            totalResult,
            searchResult
        },
        data(){
            return{
                isModalVisible: false};
        },
        methods:{
            showModal(){
                this.isModalVisible = true;
            },
            closeModal(){
                this.isModalVisible = false;
            }
        }
    }





</script>

<style lang="scss" scoped>



h1 {
    font-size: 2rem;
    margin: 40px 0px;
}

 .main-element{
     display: flex;
     justify-content: space-evenly;
 }

    .card-header{
        justify-content: space-between;
        padding: 40px 20px;
        align-items: center;
        box-shadow: none;
        position: relative;

        &::after {
            position: absolute;
            height: 1px;
            width: calc(100% - 70px);
            content:'';
            bottom: 20px;
            left: 35px;
            background-color: black;

        }
    }
    .anv-code{
        margin: 40px 0px;
    }


    .btn-all-reset {
        all: unset;
        cursor: pointer;
        margin-right: 30px;
        img {
            height: 50px;
        }
    }

    .column-costum {
        display: flex;
        align-items: center;
        justify-content: flex-end;

    }
</style>









