<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <!-- <transition name="router-animated" > -->
  <!-- <Transition
    name="custom-classes"
    enter-active-class="animate__animated animate__tada"
    leave-active-class="animate__animated animate__bounceOutRight"
  > -->
  <!-- <Transition name="bounce"> -->
  <router-view v-slot="{ Component }">
    <transition name="route" mode="out-in">
      <component :is="Component"></component>
    </transition>
  </router-view>
  <!-- </Transition> -->
</template>

<script>
export default {};
</script>
<style>
@import "https://cdn.jsdelivr.net/npm/animate.css@3.5.1";
/* @import "https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"; */
body {
  background: rgb(233, 233, 233);
  font-family: Arial, Helvetica, sans-serif;
}
html,
body {
  height: calc(100%-50px);
}

#app {
  background: #fff;
  width: 50%;
  padding: 30px;
  border-radius: 10px;
  margin: 50px auto 0 auto;
  height: calc(60% - 50px);
}

.page {
  position: fixed;
  width: inherit;
}

/* ex1 */
/* .route-enter-from{
  opacity: 0;
  transform: translateX(100px);
}

.route-enter-active{
  transition: all 0.3s ease-out;
}

.route-leave-to{
  opacity: 0;
  transform: translateX(-100px);
}

.route-leave-active{
  transition: all 0.3s ease-in;
}  */

/* same:ex1 */
/* .route-enter-active {
  animation: coming .3s ;
}
.route-leave-active {
  animation:going .3s ;
}
@keyframes going {
  from {
    transform: translateX(0px);
    opacity: 1;
  }
  to {
    transform: translateX(-100px);
    opacity:0;
  }
}
@keyframes coming {
  from {
    transform: translateX(100px);
    opacity: 0;
  }
  to {
    transform: translateX(0px);
    opacity: 1;
  }
} */

/* ex2 */
/* .route-enter-active {
  animation: coming 1s; 
}
.route-leave-active {
  animation: going 1s;
}
@keyframes going {
  from {
    transform: translateX(0);
    opacity: 1;
  }
  to {
    transform: translateX(-50px);
    opacity: 0;
  }
}
@keyframes coming {
  from {
    transform: translateX(-50px);
    opacity: 0;
  }
  to {
    transform: translateX(0);
    opacity: 1;
  }
} */
/* same:ex2 */
.route-enter-from{
  opacity: 0;
  transform: translateX(-50px);
}
.route-enter-active{
  transition: all 0.3s ease-out;
}
.route-leave-to{
  opacity: 0;
  transform: translateX(-50px);
}
.route-leave-active{
  transition: all 0.3s ease-out;
}
/* enter-active-class="animated fadeInDown" leave-active-class="animated fadeInDown" */
/* .router-animated-enter-active {
  animation: bounce-in 0.5s;
}
.bounce-enter-active {
  animation: bounce-in 0.5s;
}
.bounce-leave-active {
  animation: bounce-in 0.5s reverse;
}
@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.25);
  }
  100% {
    transform: scale(1);
  }
} */
/* enter-active-class="animated tada"
    leave-active-class="animated bounceOutRight" */
</style>
