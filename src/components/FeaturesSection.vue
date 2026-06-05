<template>
  <section class="features">
    <div class="container">

      <h2>Brewed to Refresh</h2>

      <p class="subtitle">
        Cold-brewed for smooth flavor and a perfectly chilled finish.
      </p>

      <div class="features-grid">

        <div class="feature">
          <span><Leaf :size="28" /></span>
          <h3>18-Hour Cold Brew</h3>
          <p>
            Slow-brewed to unlock deep flavor and smoothness.
          </p>
        </div>

        <div class="feature">
          <span><Waves :size="28" />
</span>
          <h3>Smooth, Bold & Refreshing</h3>
          <p>
            Rich coffee taste with a clean, chilled finish.
          </p>
        </div>

        <div class="feature">
          <span><Leaf :size="28" />
</span>
          <h3>No Artificial Flavors</h3>
          <p>
            Only real ingredients, nothing unnecessary.
          </p>
        </div>

        <div class="feature">
          <span><Snowflake :size="28" /></span>
          <h3>Served Ice-Cold</h3>
          <p>
            Perfectly chilled for instant refreshment.
          </p>
        </div>

      </div>

    </div>
  </section>
</template>

<script setup>
import {
  Snowflake,
  Waves,
  Leaf,
 GlassWater
} from 'lucide-vue-next'
</script>

<style scoped>
.features {
  background: #e7ddd0;
  padding: 80px 0;
}

.container {
  width: 90%;
  max-width: 1200px;
  margin: 0 auto;
}

h2 {
  text-align: center;
  font-size: 3rem;
  font-family: "Playfair Display", serif;
  color: #1d1d1d;
}

.subtitle {
  text-align: center;
  margin-top: 10px;
  color: #555;
}

.features-grid {
  margin-top: 60px;

  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 40px;
}

.feature {
  text-align: center;
}

.feature span {
  font-size: 1.8rem;
}

.feature h3 {
  margin-top: 15px;
  font-size: 1.1rem;
  color: #111;
}

.feature p {
  margin-top: 8px;
  color: #555;
  line-height: 1.6;
}

@media (max-width: 900px) {
  .features-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 600px) {
  .features-grid {
    grid-template-columns: 1fr;
  }

  h2 {
    font-size: 2.3rem;
  }
}
.feature svg {
  width: 28px;
  height: 28px;
  color: #6b4a36;
  margin-bottom: 1rem;
}
</style>
