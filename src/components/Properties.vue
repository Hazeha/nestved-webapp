<template>
    <div class="container">
        <!--TODO Anvendelses kode skal videregives så koden kan anvendes-->
        <button type="button" class="button is-primary is-large anv-code" @click="showModal">
            Anvendelseskode
        </button>

        <UseageCode v-show="isModalVisible" @close="closeModal"/>

        <!--TODO This needs to be made into a component-->
        <div class="card content">
            <div class="card-header">
                <h2>Tilstand</h2>

                <div class="dropdown is-hoverable">
                    <div class="dropdown-trigger">
                        <button class="button is-primary" aria-haspopup="true" aria-controls="dropdown-menu4">+ Tilføj Kategori</button>
                    </div>
                    <div class="dropdown-menu" id="dropdown-menu4" role="menu">
                        <div class="dropdown-content">
                            <div class="dropdown-item">
                                <h4>Kategorier</h4>
                                <label class="checkbox"><input type="checkbox">
                                    Teknisk Anlæg
                                </label>
                                <label class="checkbox"><input type="checkbox">
                                    Udv. belægning
                                </label>
                                <label class="checkbox"><input type="checkbox">
                                    Facade og Murværk
                                </label>
                                <label class="checkbox"><input type="checkbox">
                                    Tag
                                </label>
                                <label class="checkbox"><input type="checkbox">
                                    Udhæng og gavle
                                </label>
                                <label class="checkbox"><input type="checkbox">
                                    Tagdækning
                                </label>
                                <label class="checkbox"><input type="checkbox">
                                    Tagrender
                                </label>
                                <label class="checkbox"><input type="checkbox">
                                    Vinduer og udv. døre
                                </label>
                                <label class="checkbox"><input type="checkbox">
                                    Fundament og sokkel
                                </label>
                            </div>

                        </div>
                    </div>
                </div>
            </div>

            <table class="table card-content">
                <thead>
                <tr>
                    <th title="Faktor">Faktor</th>
                    <th title="Indmeldinger">Indmeldinger</th>
                    <th title="Point">Point</th>
                    <th title="Vægtning">Vægtning</th>
                    <th title="Resultat">Resultat</th>
                </tr>
                </thead>
                <tbody>
                <tr>
                    <td>Tagrender m. Nedløb</td>
                    <td>3</td>
                    <td>68</td>
                    <td><input type="range"> 20%</td>
                    <td>68</td>
                </tr>
                <tr>
                    <td>Vinduer & udv. Døre</td>
                    <td>3</td>
                    <td>68</td>
                    <td><input type="range"> 20%</td>
                    <td>68</td>
                </tr>
                <tr>
                    <td>Fundament & Sokkel</td>
                    <td>3</td>
                    <td>68</td>
                    <td><input type="range"> 20%</td>
                    <td>68</td>
                </tr>
                </tbody>
            </table>

        </div>
        <!--TODO This needs to be made into a component-->
        <div class="card content">
            <div class="card-header">
                <h2>Energi</h2>
                <button class="button is-primary level-item">+ Tilføj Kategori</button>
            </div>
            <table class="table card-content">
                <thead>
                <tr>
                    <th title="Faktor">Faktor</th>
                    <th title="Indmeldinger">Indmeldinger</th>
                    <th title="Point">Point</th>
                    <th title="Vægtning">Vægtning</th>
                    <th title="Resultat">Resultat</th>
                </tr>
                </thead>
                <tbody>
                <tr>
                    <td>Tagrender m. Nedløb</td>
                    <td>3</td>
                    <td>68</td>
                    <td><input type="range"> 20%</td>
                    <td>68</td>
                </tr>
                <tr>
                    <td>Vinduer & udv. Døre</td>
                    <td>3</td>
                    <td>68</td>
                    <td><input type="range"> 20%</td>
                    <td>68</td>
                </tr>
                <tr>
                    <td>Fundament & Sokkel</td>
                    <td>3</td>
                    <td>68</td>
                    <td><input type="range"> 20%</td>
                    <td>68</td>
                </tr>
                </tbody>
            </table>
        </div>
        <!--TODO This needs to be made into a component-->
        <div class="card content">
            <div class="card-header">
                <h2>Helpdesk</h2>
                <button class="button is-primary level-item">+ Tilføj Kategori</button>

            </div>
            <table class="table card-content">
                <thead>
                <tr>
                    <th title="Faktor">Faktor</th>
                    <th title="Indmeldinger">Indmeldinger</th>
                    <th title="Point">Point</th>
                    <th title="Vægtning">Vægtning</th>
                    <th title="Resultat">Resultat</th>
                </tr>
                </thead>
                <tbody>
                <tr>
                    <td>Tagrender m. Nedløb</td>
                    <td>3</td>
                    <td>68</td>
                    <td><input type="range"> 20%</td>
                    <td>68</td>
                </tr>
                <tr>
                    <td>Vinduer & udv. Døre</td>
                    <td>3</td>
                    <td>68</td>
                    <td><input type="range"> 20%</td>
                    <td>68</td>
                </tr>
                <tr>
                    <td>Fundament & Sokkel</td>
                    <td>3</td>
                    <td>68</td>
                    <td><input type="range"> 20%</td>
                    <td>68</td>
                </tr>
                </tbody>
            </table>
        </div>

        <!--TODO Samlet Resultat - Skal der laves funktioner til.-->
        <div class="card content">
            <div class="card-header">
                <h2>Samlet Resultat</h2>
            </div>

            <table class="table card-content">
                <thead>
                <tr>
                    <th title="Faktor">Faktor</th>
                    <th title="Indmeldinger">Point</th>
                    <th title="Point">Vægtning</th>
                    <th title="Vægtning">Samlet Point</th>
                    <th title="Resultat">Resultat</th>
                </tr>
                </thead>
                <tbody>
                <tr>
                    <td>Tilstand</td>
                    <td>3</td>
                    <td><input type="range"> 20%</td>
                    <td>68</td>
                    <td><h1 style="color: green">⦿</h1></td>
                </tr>
                <tr>
                    <td>Energi</td>
                    <td>3</td>
                    <td><input type="range"> 20%</td>
                    <td>68</td>
                    <td><h1 style="color: red">⦿</h1></td>
                </tr>
                <tr>
                    <td>Helpdesk</td>
                    <td>3</td>
                    <td><input type="range"> 20%</td>
                    <td>68</td>
                    <td><h1 style="color: yellow">⦿</h1></td>
                </tr>
                </tbody>
            </table>

            <h4>Antal Ejendomme</h4>
            <div class="progress-container">
         
            <progress class="progress is-success" value="60" max="100"></progress>
            
            <progress class="progress is-warning" value="30" max="100">75%</progress>
            
            <progress class="progress is-danger" value="10" max="100">90%</progress>
            </div>
            
        </div>
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
    import UseageCode from './properties/UseageCode.vue'


    export default {
        name: "Properties",

        components: {
            UseageCode
        },
        data(){
            return{
                isModalVisible: false
            };
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

<style scoped>
 .main-element{
     display: flex;
     justify-content: space-evenly;
 }

    .card-header{
        justify-content: space-between;
        padding: 10px 15px 0px 15px;
    }
    .anv-code{
        margin: 25px;
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
</style>