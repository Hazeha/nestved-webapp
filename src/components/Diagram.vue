



<template>
    <div class="progress_bar_wrapper">
        <h4>Antal Ejendomme</h4>
        <div class="progress_align">
            <p>Diagram Value 1</p>
            <p>Diagram Value 2</p>
            <p>Diagram Value 3</p>
        </div>
        <div class="progress_align container">

            
            <div class="progress-container">
                
                <progress class="progress is-success" value="60" max="100"></progress>
           
                <progress class="progress is-warning" value="30" max="100"></progress>
            
                <progress class="progress is-danger" value="10" max="100"></progress>
            </div>
        </div>
    </div>
</template>









<script>
    export default {
        name: "Diagram"
    }
</script>


<style lang="scss" scoped>

    .progress{

    }

</style>