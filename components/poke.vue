<template>
    <div class="diosito">
        <div class="TarjetaPadre">
            <img src="https://assets.stickpng.com/images/580b57fcd9996e24bc43c325.png" alt="">
            <p>Pikachu</p>
        </div>

        <div class="TarjetaPadre">
            <img src="https://assets.stickpng.com/images/580b57fcd9996e24bc43c325.png" alt="">
            <p>Pikachu</p>
        </div>

        <div class="TarjetaPadre">
            <img src="https://assets.stickpng.com/images/580b57fcd9996e24bc43c325.png" alt="">
            <p>Pikachu</p>
        </div>

        <div class="TarjetaPadre">
            <img src="https://assets.stickpng.com/images/580b57fcd9996e24bc43c325.png" alt="">
            <p>Pikachu</p>
        </div>

        <div class="TarjetaPadre">
            <img src="https://assets.stickpng.com/images/580b57fcd9996e24bc43c325.png" alt="">
            <p>Pikachu</p>
        </div>

        <div class="TarjetaPadre">
            <img src="https://assets.stickpng.com/images/580b57fcd9996e24bc43c325.png" alt="">
            <p>Pikachu</p>
        </div>
    </div>
</template>

<style>

.diosito{
    display: flex;
    flex-wrap: wrap;
    gap: 40px;
}

img{
    height: 300px;
}

.TarjetaPadre{
    padding: 20px;
    background-color: red;
    height: auto;
    color: white;
    border: 3px solid white;
    border-radius: 10px;
}


.TarjetaPadre:before {
    content: "";
    z-index: -1;
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background: linear-gradient(-45deg, #f13c77 0%, #f5e6ad 100% );
    transform: translate3d(0px, 20px, 0) scale(0.95);
    filter: blur(20px);
    opacity: var(0.7);
    transition: opacity 0.3s;
    border-radius: inherit;
}

.TarjetaPadre::after {
    content: "";
    z-index: -1;
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background: inherit;
    border-radius: inherit;
}
        

p{
    font-size: 30px;
    font-weight: 800px;
    text-align: center;
}
</style>