<script setup>
  import { workoutProgram } from "../../utils";

  const selectedWorkout = 2;
  const { workout, warmup } = workoutProgram[selectedWorkout];
</script>

<template>
  <div id="workout-card">
    <div class="plan-card card">
      <div class="pan-card-header">
        <p>Day {{ selectedWorkout < 9 ? "0" + selectedWorkout : selectedWorkout }}</p>

        <i class="fa-solid fa-dumbbell"></i>
      </div>

      <h2>{{ "Push" }} Workout</h2>
    </div>

    <div class="workout-grid">
      <h4 class="grid-name">Warmup</h4>
      <h6>Sets</h6>
      <h6>Reps</h6>
      <h6 class="grid-weights">Weights</h6>

      <div :key="wIdx" class="workout-grid-row" v-for="(w, wIdx) in warmup">
        <div class="grid-name">
          <p>{{ w.name }}</p>
          <button>
            <i class="fa-regular fa-circle-question"></i>
          </button>
        </div>

        <p>{{ w.sets }}</p>
        <p>{{ w.reps }}</p>

        <input type="text" class="grid-weights" placeholder="14kg" disabled />
      </div>

      <div class="workout-grid-line"></div>

      <h4 class="grid-name">Workout</h4>
      <h6>Sets</h6>
      <h6>Reps</h6>

      <div :key="wIdx" class="workout-grid-row" v-for="(w, wIdx) in workout">
        <div class="grid-name">
          <p>{{ w.name }}</p>
          <button>
            <i class="fa-regular fa-circle-question"></i>
          </button>
        </div>

        <p>{{ w.sets }}</p>
        <p>{{ w.reps }}</p>

        <input type="text" class="grid-weights" placeholder="14kg" />
      </div>
    </div>

    <div class="card">
      <button>Save & Exit <i class="fa-solid fa-save"></i></button>

      <button>Complete <i class="fa-solid fa-check"></i></button>
    </div>
  </div>
</template>

<style scoped></style>
