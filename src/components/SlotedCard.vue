<template>
  <div class="card">
    <slot name="top"></slot>
    <slot name="middle"></slot>
    <slot name="bottom"></slot>
  </div>
</template>

<style>
  .card {
    background-color: white;
    width: 355px;
    height: 385px;
    border-radius: 20px;
    border: solid 4px lightgray;
    filter: drop-shadow(10px 10px 32px rgba(0, 0, 0, 0.25));
    padding:8px;
  }
</style>
