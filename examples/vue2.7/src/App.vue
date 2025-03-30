<template>
  <ModalProvider>
    <Example />
  </ModalProvider>
</template>

<script setup>
import { ModalProvider, useModal } from "vue-modal-provider";
import Example from "./Example.vue";

const modal = useModal(Example);
</script>
