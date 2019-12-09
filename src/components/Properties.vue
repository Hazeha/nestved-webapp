<template>
    <div class="container">
        <!--TODO Anvendelses kode skal videregives så koden kan anvendes-->
<h1>Filter din søgning</h1>

        <Tilstand mainType="Tilstand"></Tilstand>
        <Tilstand mainType="Energi"></Tilstand>
        <Tilstand mainType="Helpdesk"></Tilstand>
        <!--TODO Samlet Resultat - Skal der laves funktioner til.-->
        <totalResult></totalResult>
        <!--TODO Lste over ejendomme, Skal laves så de rigtige boliger kommer frem via søgningen-->
        <div class="content">
            <h2>Liste over Ejendomme</h2>
            <div class="card">
                <h3 class="card-header">Ringstedgade 25F</h3>
                <div class="card-content prop-card">
                    <img src="@/assets/house1.jpg" class="prop-img">
                    <table>
                        <thead>
                            <tr>
                                <th>Tilstand</th>
                                <th>Vedligeholdelse</th>
                                <th>Forurening</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>El - <strong>35 kr. pr kv2</strong></td>
                                <td>El - <strong>35 kr. pr kv2</strong></td>
                                <td>El - <strong>35 kr. pr kv2</strong></td>
                            </tr>
                            <tr>
                                <td>Vand - <strong>35 kr. pr kv2</strong></td>
                                <td>Vand - <strong>35 kr. pr kv2</strong></td>
                                <td>Vand - <strong>35 kr. pr kv2</strong></td>
                            </tr>
                            <tr>
                                <td>Varme - <strong>35 kr. pr kv2</strong></td>
                                <td>Varme - <strong>35 kr. pr kv2</strong></td>
                                <td>Varme - <strong>35 kr. pr kv2</strong></td>
                            </tr>
                            <tr>
                                <td>Teknisk - <strong>35 kr. pr kv2</strong></td>
                                <td>Teknisk - <strong>35 kr. pr kv2</strong></td>
                                <td>Teknisk - <strong>35 kr. pr kv2</strong></td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>
            <div class="card">
                <h3 class="card-header">Ringstedgade 25F</h3>
                <div class="card-content prop-card">
                    <img src="@/assets/house1.jpg" class="prop-img">
                    <table>
                        <thead>
                        <tr>
                            <th>Tilstand</th>
                            <th>vedligeholdelse</th>
                            <th>Forurening</th>
                        </tr>
                        </thead>
                        <tbody>
                        <tr>
                            <td>El - <strong>35 kr. pr kv2</strong></td>
                            <td>El - <strong>35 kr. pr kv2</strong></td>
                            <td>El - <strong>35 kr. pr kv2</strong></td>
                        </tr>
                        <tr>
                            <td>Vand - <strong>35 kr. pr kv2</strong></td>
                            <td>Vand - <strong>35 kr. pr kv2</strong></td>
                            <td>Vand - <strong>35 kr. pr kv2</strong></td>
                        </tr>
                        <tr>
                            <td>Varme - <strong>35 kr. pr kv2</strong></td>
                            <td>Varme - <strong>35 kr. pr kv2</strong></td>
                            <td>Varme - <strong>35 kr. pr kv2</strong></td>
                        </tr>
                        <tr>
                            <td>Teknisk - <strong>35 kr. pr kv2</strong></td>
                            <td>Teknisk - <strong>35 kr. pr kv2</strong></td>
                            <td>Teknisk - <strong>35 kr. pr kv2</strong></td>
                        </tr>
                        </tbody>
                    </table>
                </div>
            </div>
        </div>
    </div>


</template>

<script>

    import Tilstand from './properties/Tilstand.vue'
    import totalResult from './properties/totalResult.vue'
    export default {
        name: "Properties",
        components: {
            Tilstand,
            totalResult
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
    .prop-card{
        display: flex;
        justify-content: space-evenly;
    }
    .prop-list{
        list-style: none;
    }
    .prop-img{
        width: 25%;
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









