<template>
    <!--TODO This needs to be made into a component-->
    <div id="Tilstand" class="card content">
        <div class="card-header">
            <h2>{{mainType}}</h2>
            <div>
            <button type="button" class="anv-code btn-all-reset" @click="showModal">
                <img src="@/assets/tool.png">
            </button>
            <keyCode v-show="isModalVisible" @close="closeModal"/>
            <div class="dropdown is-hoverable">
                <div class="dropdown-trigger">
                    <button class="button is-primary" aria-haspopup="true" aria-controls="dropdown-menu4">+ Tilføj Kategori</button>
                </div>
                <div class="dropdown-menu" id="dropdown-menu4" role="menu">
                    <div class="dropdown-content">
                        <div class="dropdown-item">
                            <h4>Kategorier</h4>
                            <label class="checkbox"><input type="checkbox" name="value1" v-model="isValue1">
                                Teknisk Anlæg
                            </label>
                            <label class="checkbox"><input type="checkbox" name="value2" v-model="isValue2">
                                Udv. belægning
                            </label>
                            <label class="checkbox"><input type="checkbox" name="value3" v-model="isValue3">
                                Facade og Murværk
                            </label>
                        </div>

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
            <keyResults
                         keyID="categori1"
                         v-show="isValue1"
                         keyValue1="4"
                         keyValue2="8"
                         keyValue3="16"
            >
            </keyResults>

            <keyResults
                    keyID="categori2"
                    v-show="isValue2"
                    keyValue1="4"
                    keyValue2="8"
                    keyValue3="16"
            >
            </keyResults>

            <keyResults
                    keyID="categori3"
                    v-show="isValue3"
                    keyValue1="4"
                    keyValue2="8"
                    keyValue3="16"
            >
            </keyResults>

            </tbody>
            <tfoot>
                <tr>
                    <th>Samlet Resultat</th>
                    <th><div>{{resultValue1}}</div></th>
                    <th><div>{{resultValue2}}</div></th>
                    <th></th>
                    <th>{{resultValue3}}</th>
                </tr>
            </tfoot>
        </table>

    </div>
</template>

<script>
    import keyResults from './keyResults.vue'
    import keyCode from './keyCode.vue'

    export default {
        name: "Tilstand",
        components: {
            keyResults,
            keyCode
        },
        props:{
            mainType: String
        },
        data(){
            return{
                isValue1: true,
                isValue2: true,
                isValue3: true,

                resultValue1: 100,
                resultValue2: 123,
                resultValue3: 1000,

                isModalVisible: false
            }

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
    .card-header{
        justify-content: space-between;
        padding: 10px 15px 0px 15px;
    }

    .btn-all-reset {
        all: unset;
        cursor: pointer;
        margin-right: 30px;}

    img {
        height: 50px;
    }


    .column-costum {
        display: flex;
        align-items: center;
        justify-content: flex-end;

    }
</style>