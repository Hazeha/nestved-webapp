<template>
    <tr>
        <td>{{keyID}}</td>
        <td><div>{{keyValue1}}</div></td>
        <td><div>{{keyValue2}}</div></td>
        <td><input name="ranger" type="range" min="0" max="100" step="1" value="keyRange" v-model="keyRange" > {{keyRange}}%</td>
        <td><div>{{keyValue3}}</div></td>
    </tr>
</template>

<script>
    export default {
        name: "keyResults",

        props: {
            keyID: String,
            keyValue1: String,
            keyValue2: String,
            keyValue3: String
        },
        data(){
            return{
                keyRange: 40
            }
        }
    }
</script>

<style scoped>

</style>