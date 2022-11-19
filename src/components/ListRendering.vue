<template>
    <div class="container">
        <h3>List Rendering</h3>
        <div class="box">
            <div class="player-list">
                <h4>Pemain</h4>
                <p v-for="(pemain, p) in playerList" :key="p">{{ pemain }}</p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'ListRendering',
        data() {
            return {
                playerList: [ 'Anthony Ginting', 'Kevin Sanjaya', 'a', 'b' ]
            }
        },
    }
</script>

<style scoped>
    .container {
        display: flex;
        justify-content: center;
        flex-direction: column;
        align-items: center;
    }
    .box {
        width: 20%;
        border: 2px solid rgb(46, 46, 46);
        border-radius: 4px;
        text-align: left;
        padding: 8px;
    }
    .player-list h4 {
        margin: 6px 0;
        font-size: 18px;
    }
    .player-list p {
        margin: 4px 0;
    }
</style>