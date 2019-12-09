<template>
    <!--TODO This needs to be made into a component-->
    <div id="Tilstand" class="card content">
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
                            <label class="checkbox"><input type="checkbox" name="teknisk" v-model="isTeknik">
                                Teknisk Anlæg
                            </label>
                            <label class="checkbox"><input type="checkbox" name="belægning" v-model="isBelægning">
                                Udv. belægning
                            </label>
                            <label class="checkbox"><input type="checkbox" name="facade" v-model="isFacade">
                                Facade og Murværk
                            </label>
                            <label class="checkbox"><input type="checkbox" name="tag" v-model="isTag">
                                Tag
                            </label>
                            <label class="checkbox"><input type="checkbox" name="gavl" v-model="isGavl">
                                Udhæng og gavle
                            </label>
                            <label class="checkbox"><input type="checkbox" name="tagdækning" v-model="isTagdækning">
                                Tagdækning
                            </label>
                            <label class="checkbox"><input type="checkbox" name="tagrender" v-model="isTagrender">
                                Tagrender
                            </label>
                            <label class="checkbox"><input type="checkbox" name="vinduer" v-model="isVinduer">
                                Vinduer og udv. døre
                            </label>
                            <label class="checkbox"><input type="checkbox" name="fundament" v-model="isFundament">
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
            <tr id="divForTeknisk" v-show="isTeknik">
                <td>Tagrender m. Nedløb</td>
                <td><div>{{meldingTeknik}}</div></td>
                <td><div>{{pointTeknik}}</div></td>
                <td><input type="range" min="0" max="100" step="1" v-model="rangeTeknik"> {{rangeTeknik}}%</td>
                <td><div>{{resultTeknik}} Points</div></td>
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
            <tfoot>
                <tr>
                    <th>Samlet Resultat</th>
                    <th><div>{{meldingResult}}</div></th>
                    <th><div>{{pointResult}}</div></th>
                    <th></th>
                    <th>{{resultResult}}</th>
                </tr>
            </tfoot>
        </table>

    </div>
</template>

<script>
    export default {
        name: "Tilstand",

        data(){
            return{
                isTeknik: true,
                meldingTeknik: 6,
                pointTeknik: 10,
                rangeTeknik: 20,
                resultTeknik: 75,


                meldingResult: 100,
                pointResult: 123,
                resultResult: 1000
            }

        },
    }




</script>

<style scoped>
    .card-header{
        justify-content: space-between;
        padding: 10px 15px 0px 15px;
    }
</style>