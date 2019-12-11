<template>
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
</template>

<script>
    export default {
        name: "searchResult"
    }
</script>

<style scoped>
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