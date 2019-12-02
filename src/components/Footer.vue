<template>
    <footer class="footer content">
        <div class="level is-mobile  container">
            <div class="level-item info-box">
                <div>
                    <h2>Borgerservice på <br>Bibliotekerne</h2>
                    <p>i Næstved, Fuglebjerg, Glumsø, Fensmark og Brøderup.</p>
                    <p>Læs om bestilling af pas og kørekort, samt hvordan med NemID og andre vejledninger m.m.</p>
                    <p>Borgerservice på lokalbibliotekerne.</p>
                    <a href="#">Bestil tid til Borgerservice</a>
                </div>
            </div>
            <div class="level-item info-box">
                <div>
                    <h2>Åbningstider i <br>Administrationen</h2>
                    <p>Sagsbehandling m.m. Rådmandshaven 20</p>
                    <ul>
                        <li>Mandag 10-15</li>
                        <li>Tirsdag 10-15</li>
                        <li>Onsdag Lukket</li>
                        <li>Torsdag 10-17</li>
                        <li>Fredag 10-13</li>
                    </ul>
                </div>
            </div>
            <div class="level-item info-box">
                <div>
                    <h2>EAN og CVR <br>EAN-numre</h2>
                    <ul class="ean-list">
                        <li>Tilmeld Betalingsservice</li>
                        <li>CVR-nummer 29189625</li>
                        <li>Bankkonto: 4343 10183758</li>
                        <li>IBAN-nr.: DK3630000010183758</li>
                        <li>NemKonto: 4343 10191467</li>
                        <li>IBAN-nr.: DK5530000010191467</li>
                    </ul>
                    <p>Begge konti har SWIFT-koden: <br/>DABADKK</p>
                    <a>Databeskyttelse</a><br>
                    <a>Ansat i kommunen</a>
                </div>
            </div>
        </div>
        <div class="has-text-centered">
            <hr>
            <p>Næstved Kommune - Rådmandshaven 20, 4700 Næstved - 5588 5588</p>
        </div>
    </footer>
</template>

<script>
    export default {
        name: "Footer"
    }
</script>

<style scoped>
    .level{
        justify-content: space-between;
        align-items: baseline;
    }
    .footer{
        text-align: left;
    }
    .info-box{
        width: 25%;
    }
    .ean-list{
        list-style: none;
        margin: 0;
    }
</style>