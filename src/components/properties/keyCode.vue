-<template>
    <transition name="modal-fade">
        <div class="modal-backdrop">
            <div class="modal" role="dialog" aria-labelledby="modalTitle" aria-describedby="modalDescription">
                <div class="modal-background"></div>
                <div class="modal-card">
                    <header class="modal-card-head" id="modalTitle">
                        <slot name="modal-card-title">
                            <h1>Anvendelseskode</h1>

                            <button type="button" class="delete" @click="close" aria-label="Close modal">
                                x
                            </button>
                        </slot>
                    </header>
                    <section class="modal-card-body" id="modalDescription">
                        <div name="body">
                            <a class="prop-code button">
                                <h2>Skole</h2>
                                <h3>#444</h3>
                            </a>

                            <a class="prop-code button">
                                <h2>Skole</h2>
                                <h3>#444</h3>
                            </a>
                            <a class="prop-code button">
                                <h2>Skole</h2>
                                <h3>#444</h3>
                            </a>
                        </div>
                    </section>
                    <footer class="modal-card-foot">
                        <slot name="footer">

                            <button class="button is-success">Brug (Kode)</button>
                        </slot>
                    </footer>
                </div>

            </div>
        </div>
    </transition>
</template>

<script>
    export default {
        name: "keyCode",

        methods: {
            close() {
                this.$emit('close');
            },
        },
    }


</script>


<!--TODO Need fix of background-->

<style scoped>

    .modal-backdrop {
        position: fixed;
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
        background-color: rgba(0, 0, 0, 0.07);
        display: flex;
        justify-content: center;
        align-items: center;
        z-index: 100;
    }

    .modal {
        background: #ffffff;
        box-shadow: 2px 2px 20px 1px;
        overflow-x: auto;
        display: flex;
        flex-direction: column;
    }
    .modal-card-head{
        justify-content: space-between;
    }
    .modal-card-foot{
        justify-content: space-between;
    }
    .prop-code{
        display: flex;
        justify-content: space-between;
        margin: 10px;
    }
    .modal-fade-enter,
    .modal-fade-leave-active {
        opacity: 0;
    }

    .modal-fade-enter-active,
    .modal-fade-leave-active {
        transition: opacity 0.5s ease;
    }
</style>