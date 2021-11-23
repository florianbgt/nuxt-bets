<template>
  <div>
    <h1>Current Bets</h1>
    <b-row>
      <b-col v-for="bet in bets" :key="bet.id" sm="6" md="4" lg="3" class="mb-4">
        <b-card :title="bet.title" class="h-100">
          <template #header>
            <h6 class="mb-0">{{ bet.user }}</h6>
          </template>
          <b-card-text>tetetetette</b-card-text>
        </b-card>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  computed: {
    bets() {
      return [
          { id: 1, title: 'Paris - OM', user: 'userX' },
          { id: 1, title: 'Rennes - OL', user: 'userY' },
          { id: 1, title: 'Bordeaux - Amiens', user: 'userX' },
          { id: 1, title: 'Nantes - Brest', user: 'userZ' }
        ]
    },
  },
}
</script>
