<template>
    <div class="father">
        <h1>PokeDex</h1>
        <input type="text" placeholder="Buscar a un Pokemón">

        <div class="cartas">
            <poke/>
        </div>
    </div>
</template>

<script>
export default {
  name: 'PokePage',
}
</script>

<style>
    .father{
        display: flex;
        flex-direction: column;
        align-items: center;
        background-color: rgb(169, 229, 240);
        height: 100vh;
        padding: 15px;
    }

    h1{
        background-color: white;
        color: black;
        width: 100%;
        height: 100px;
        text-align: center;
        font-size: 75px;
        font-weight: 700;
        border-radius: 10px;
        margin-bottom: 20px;
    }

    input{
        align-self: flex-start;
        height: 25px;
    }
</style>