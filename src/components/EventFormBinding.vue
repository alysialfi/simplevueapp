<template>
    <div class="container">
        <h3>Event Handling & Form Bindings</h3>
        <div class="box">
            <form @submit.prevent>
                <input type="text" name="player" id="player" v-model="player" @keyup.enter="addPlayer()" placeholder="Masukkan nama pemain">
                <button type="button" @click="addPlayer()">Tambah</button>
            </form>
            <div class="player-list">
                <h4>Pemain</h4>
                <p v-for="(player, p) in playerList" :key="p">{{ player }}</p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'EventFormBinding',
        data() {
            return {
                player: '',
                playerList: [ 'Anthony Ginting', 'Kevin Sanjaya', 'Greysia Poli' ]
            }
        },
        methods: {
            addPlayer() {
                this.playerList.push(this.player);
                this.player = '';
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
        padding: 16px 8px;
    }
    form {
        margin: auto;
    }
    form input {
        width: 65%;
        height: 28px;
        border-radius: 4px 0 0 4px;
        border: 2px solid gray;
        padding: 0 8px;
    }
    form input:focus {
        outline: none;
    }
    form button {
        width: 28%;
        height: 32px;
        border-radius: 0px 4px 4px 0;
        outline: none;
        border-top: 2px solid gray;
        border-right: 2px solid gray;
        border-bottom: 2px solid gray;
        border-left: none;
    }
    form span {
        margin-top: 8px;
    }
    .player-list h4 {
        margin: 24px 0 6px 0;
        font-size: 18px;
    }
    .player-list p {
        margin: 4px 0;
    }
</style>