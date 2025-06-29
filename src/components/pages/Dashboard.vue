<script setup>
  import Grid from "../Grid.vue";
  import { gymHealthFacts } from "../../utils";

  const randomNumber = Math.floor(Math.random() * gymHealthFacts.length);

  const todaysFact = gymHealthFacts[randomNumber];

  const props = defineProps({
    handleSelectWorkout: Function,
    firstIncompleteWorkoutIndex: Number,
    handleResetPlan: Function
  });
</script>

<template>
  <section id="dashboard">
    <div class="card tip-container">
      <h2>Welcome smaldier</h2>
      <div>
        <p class="tip">
          <strong>Daily Tip</strong>
          <br />
          {{ todaysFact }}

          <button @click="() => handleSelectWorkout(firstIncompleteWorkoutIndex < 0 ? 0 : firstIncompleteWorkoutIndex)">Start workout &rarr;</button>
        </p>
      </div>

      <Grid v-bind="props" />
    </div>
  </section>
</template>

<style scoped>
  .tip-container,
  .tip-container div,
  #dashboard {
    display: flex;
    flex-direction: column;
  }

  .tip-container,
  #dashboard {
    gap: 2rem;
  }

  .tip-container {
    gap: 0.5rem;
  }

  @media (min-width: 640px) {
    .tip-container {
      gap: 1rem;
    }
  }
</style>
