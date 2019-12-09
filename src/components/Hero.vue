<template>
    <div class="hero is-primary">

            <nav class="container level">
                <a class="level-left level-item logo-link" href="#">
                    <img class="logo-img" src="@/assets/logo.png" alt="næstved logo"/>
                </a>

                <ul class="level-right">
                    <li class="level-item"><a href="#">Helpdesk</a></li>
                    <li class="level-item"><a href="#">Opgaver</a></li>
                    <li class="level-item"><a href="#">Ejendomme</a></li>
                    <li class="level-item"><a class="button is-success" href="#">Login</a></li>
                </ul>
            </nav>

    </div>
</template>

<script>
    export default {
        name: "Hero"
    }
</script>

<style scoped>


    .logo-link{
        width: 5rem;
    }
    .logo-img{
        width: 10rem;
    }
    .hero{
        display: block;
        padding: 2rem;
    }



</style>