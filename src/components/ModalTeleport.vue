<template>
  <button @click="open = true" class="btn btn-primary">
    Confirmer l'achat
  </button>
  <Teleport to="body">
    <div v-if="open" @click="open = false" class="calc">
      <div @click.stop class="modal-container">
        <h3>Confirmation de votre commande</h3>
        <ul>
          <li>Du contenu</li>
          <li>Du contenu</li>
          <li>Du contenu</li>
        </ul>
        <button @click.stop="open = false" class="btn btn-danger">
          Confirmer la commande
        </button>
      </div>
    </div>
  </Teleport>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const open = ref(false)
</script>

<style scoped lang="scss">
.calc {
  position: fixed;
  inset: 0;
  background-color: rgba(0, 0, 0, 0.5);
  backdrop-filter: blur(5px);
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
}

.modal-container {
  background-color: rgb(1, 9, 26);
  border-radius: 5px;
  padding: 30px;
  display: flex;
  flex-direction: column;
  gap: 20px;
}


</style>
