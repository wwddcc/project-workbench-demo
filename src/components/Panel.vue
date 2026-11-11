<script setup>
defineProps({ title: String, more: String });
const emit = defineEmits(['more']);
</script>
<template><section class="panel"><header class="panel-head"><h2>{{ title }}</h2><div class="panel-actions"><slot name="actions"><button v-if="more" class="text-button" @click="emit('more')">{{ more }} ›</button></slot></div></header><slot /></section></template>
