<script scope></script>

<template>
  <div>
    <section id="welcome">
      <div class="benefits">
        <h2>Complete this program<br />If you want...</h2>
        <div>
          <p>✅ Follow a simple program with proven results.</p>
          <p>✅ Get fit, Healthy, strong and absolutely shredded.</p>
          <p>✅ Learn more about gym, training and technique.</p>
        </div>
      </div>

      <div>
        <h3>The Training Plan</h3>
        <p>This training plan follows a structure know as the <strong>Bro split</strong>.</p>

        <h5><i>Push &rarr; Pull &rarr; Legs &rarr; Repeat</i></h5>

        <div class="card challenge">
          <h3>🔥 Your challenge</h3>
          <p>Complete all the workouts and track your progress along the way!</p>
          <p>Do you accept?</p>

          <button>Begin &rarr;</button>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
  .challenge,
  .benefits {
    display: flex;
    flex-direction: column;
  }

  #welcome {
    gap:  1.5rem;
  }

  .benefits {
    gap: .5rem;
  }

  .challenge {
    gap: .25rem;
  }
</style>
