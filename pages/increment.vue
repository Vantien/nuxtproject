<template>
<div>
    <h1>increment</h1>
  <button @click="$store.commit('increment')">{{ $store.state.counter }}</button>
</div>
</template>