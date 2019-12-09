<template>
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

        <Diagram />



    </div>
</template>

<script>
    export default {
        name: "totalResult"
    }
</script>

<style scoped>

</style>