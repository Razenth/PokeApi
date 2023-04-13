<template>
<div class="all">
        <img src="https://i.pinimg.com/originals/32/a6/88/32a6883c4d90ce18f01fb552f8418965.gif" alt="" class="gif">
        <div class="load">
        <h1>CARGANDO</h1>
        <div class="lds-ellipsis"><div></div><div></div><div></div><div></div></div>
        </div>

</div>
</template>


<style>

.all{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: rgb(136, 29, 29);
    height: 100vh;
}

.img{
    display: flex;
}

.gif{
    width: 20%;
    height: auto;
}

.load h1{
    width: auto;
    color: black;
    background-color: transparent;
}
.load{
    display: flex;
    align-items: center;
}


.lds-ellipsis {
  display: inline-block;
  position: relative;
  width: 80px;
  height: 80px;
}
.lds-ellipsis div {
  position: absolute;
  top: 33px;
  width: 13px;
  height: 13px;
  border-radius: 50%;
  background: black;
  animation-timing-function: cubic-bezier(0, 1, 1, 0);
}
.lds-ellipsis div:nth-child(1) {
  left: 8px;
  animation: lds-ellipsis1 0.6s infinite;
}
.lds-ellipsis div:nth-child(2) {
  left: 8px;
  animation: lds-ellipsis2 0.6s infinite;
}
.lds-ellipsis div:nth-child(3) {
  left: 32px;
  animation: lds-ellipsis2 0.6s infinite;
}
.lds-ellipsis div:nth-child(4) {
  left: 56px;
  animation: lds-ellipsis3 0.6s infinite;
}
@keyframes lds-ellipsis1 {
  0% {
    transform: scale(0);
  }
  100% {
    transform: scale(1);
  }
}
@keyframes lds-ellipsis3 {
  0% {
    transform: scale(1);
  }
  100% {
    transform: scale(0);
  }
}
@keyframes lds-ellipsis2 {
  0% {
    transform: translate(0, 0);
  }
  100% {
    transform: translate(24px, 0);
  }
}
</style>