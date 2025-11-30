<script setup lang="ts">
</script>

<template>
  <div class="bd-container">
    <div class="bd-content">
      <div class="bg-container">
        <!-- Imagem de fundo ocupando tudo -->
        <div class="bg-image">
          <NuxtImg
            src="/bg-image.svg"
            alt="Banner Discovery"
            class="bg-img"
          />
        </div>

        <!-- Overlay centralizado -->
        <div class="bg-overlay">
          <div class="bd-texts">
            <h1 class="bd-title">Discover Amazing Places</h1>
            <p class="bd-subtitle">
              Explore the world with us and find your next adventure.
            </p>
            <button class="bd-button">Get Started</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.bd-container {
  width: 100%;
  display: flex;
  justify-content: center;
}

.bd-content {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.bg-container {
  position: relative;
  width: 100%;
  height: 700px;
  border-radius: 12px;
  overflow: hidden;
}

.bg-image {
  position: absolute;
  inset: 0;
}

.bg-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

.bg-overlay {
  position: absolute;
  inset: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0 2rem;
  text-align: center;
}

.bd-texts {
  max-width: 600px;
  color: #fff;
}

.bd-title {
  font-size: 2.5rem;
  margin-bottom: 0.75rem;
}

.bd-subtitle {
  font-size: 1.05rem;
  margin-bottom: 1.25rem;
}

.bd-button {
  padding: 0.75rem 1.5rem;
  border-radius: 999px;
  border: none;
  cursor: pointer;
  background-color: #56B280;
  color: #fff;
  font-weight: 600;
}
</style>
