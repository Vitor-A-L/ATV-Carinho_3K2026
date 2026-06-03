<template>
  <section class="hero">
    <div class="hero-content">
      <div class="hero-text">
        <h1>
          Chill With <br>
          Perfectly Brewed <br>
          Iced Coffee
        </h1>

        <p>
          Refresh your day with our expertly crafted iced coffee —
          smooth, bold, and perfectly chilled for every moment.
        </p>

        <div class="buttons">
          <button class="primary">
            Order Iced Coffee
          </button>

          <button class="secondary">
            Explore Menu
          </button>
        </div>

        <div class="stats">
          <div>
            <h3>30+</h3>
            <span>Iced Coffee Variants</span>
          </div>

          <div>
            <h3>5k+</h3>
            <span>Happy Customers</span>
          </div>

          <div>
            <h3>100%</h3>
            <span>Premium Arabica Beans</span>
          </div>
        </div>
      </div>

      <div class="hero-image">
        <img src="/public/iced-coffee.png" alt="Iced Coffee">
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.hero {
  min-height: calc(100vh - 80px);

  background:
    radial-gradient(
      circle at 75% 50%,
      rgba(120, 80, 50, 0.4),
      rgba(40, 20, 10, 0.3),
      rgba(10, 10, 10, 1)
    );

  color: white;

  overflow-x: hidden;

  display: flex;
  align-items: flex-end;

  padding-top: 40px;
}

.hero-content {
  width: 90%;
  max-width: 1300px;

  margin: 0 auto;

  display: flex;
  justify-content: space-between;
  align-items: flex-end;

  min-height: calc(100vh - 120px);
}

.hero-text {
  max-width: 550px;
  padding-bottom: 50px;
}

.hero-text h1 {
  font-size: 4rem;
  line-height: 1.1;
  font-family: "Playfair Display", serif;
}

.hero-text p {
  margin-top: 20px;
  color: #b9b9b9;
  line-height: 1.6;
}

.buttons {
  display: flex;
  gap: 16px;
  margin-top: 30px;
}

.primary {
  background: #c98a4b;
  color: white;
  border: none;
  padding: 14px 28px;
  border-radius: 6px;
  cursor: pointer;
}

.secondary {
  background: transparent;
  color: white;
  border: 1px solid #666;
  padding: 14px 28px;
  border-radius: 6px;
  cursor: pointer;
}

.stats {
  display: flex;
  gap: 50px;
  margin-top: 60px;
}

.stats h3 {
  font-size: 1.8rem;
}

.stats span {
  color: #aaa;
  font-size: .9rem;
}

.hero-image {
  display: flex;
  align-items: flex-end;
  justify-content: flex-end;
  flex: 1;
    margin-right: -70px;

}

.hero-image img {
  width: min(100%, 900px);
  height: auto;
  display: block;
}
</style>