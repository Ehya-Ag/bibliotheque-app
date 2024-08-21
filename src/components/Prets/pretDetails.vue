<!-- PretDetails.vue -->
<template>
    <div v-if="isVisible" class="details-overlay">
      <div class="details-modal">
        <h2>Détails du Prêt</h2>
        <p><strong>Nom du Livre:</strong> {{ getLivreName(pret.nomLivre) }}</p>
        <p><strong>Nom du Membre:</strong> {{ getMembreName(pret.nomMembre) }}</p>
        <p><strong>Date de Prêt:</strong> {{ pret.datePret }}</p>
        <p><strong>Date de Remise:</strong> {{ pret.dateRemise || 'Non encore remis' }}</p>
        <button class="btn btn-sm btn-secondary" @click="close">Fermer</button>
      </div>
    </div>
  </template>
  
  <script setup>
  // Pas besoin d'importer `defineProps` ou `defineEmits` ici
  
  // Définir les props
  const props = defineProps({
    pret: {
      type: Object,
      default: () => ({}),
    },
    isVisible: {
      type: Boolean,
      default: false,
    },
    livres: {
      type: Array,
      default: () => [],
    },
    membres: {
      type: Array,
      default: () => [],
    },
  });
  
  // Définir les événements émis
  const emit = defineEmits(['onClose']);
  
  // Méthode pour obtenir le nom du livre
  const getLivreName = (id) => {
    const livre = props.livres.find(l => l.id === id);
    return livre ? livre.nom : 'Inconnu';
  };
  
  // Méthode pour obtenir le nom du membre
  const getMembreName = (id) => {
    const membre = props.membres.find(m => m.id === id);
    return membre ? membre.nom : 'Inconnu';
  };
  
  // Méthode pour fermer le modal
  const close = () => {
    emit('onClose');
  };
  </script>
  
  <style scoped>
  .details-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .details-modal {
    background: white;
    padding: 20px;
    border-radius: 5px;
    max-width: 500px;
    width: 100%;
  }
  </style>
  