<script setup lang="ts">

const nav = [
  { name: 'Home', path: '/' },
  { name: 'About', path: '/about' },
  { name: 'Contact', path: '/contact' },
]

</script>

<template>
  <div class="header-container">
    <div class="header-cnt">
      <div class="header-logo">
        <NuxtImg src="/logo.svg" width="120" alt="Logo" />
      </div>
    </div>

    <nav class="header-items-nav">
      <NuxtLink
        v-for="item in nav"
        :key="item.name"
        :to="item.path"
        class="header-item-nav"
      >
        {{ item.name }}
      </NuxtLink>
    </nav>

    <div class="header-actions">
      <button class="btn-login">
        Login
      </button>
      <button class="btn-cart">
        Go to cart
      </button>
    </div>
  </div>
</template>

<style scoped>
.header-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 16px 32px;
  background-color: #ffffff;
  border-bottom: 1px solid #eee;
}

/* nav container */
.header-items-nav {
  display: flex;
  gap: 1.5rem;
}

/* link padrão */
.header-item-nav {
  position: relative;
  font-size: 0.95rem;
  font-weight: 500;
  color: #555;
  text-decoration: none;
  padding: 4px 0;
  transition: color 0.2s ease;
}

/* linha embaixo no hover */
.header-item-nav::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -4px;
  width: 0;
  height: 2px;
  background-color: #0070f3;
  transition: width 0.2s ease;
}

.header-item-nav:hover {
  color: #111;
}

.header-item-nav:hover::after {
  width: 100%;
}

/* estado ativo (Nuxt adiciona .router-link-active/.router-link-exact-active) */
.header-item-nav.router-link-exact-active {
  color: #0070f3;
}

.header-item-nav.router-link-exact-active::after {
  width: 100%;
}

/* ações à direita */
.header-actions {
  display: flex;
  gap: 0.75rem;
}

.btn-login,
.btn-cart {
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
  padding: 0.45rem 0.9rem;
  border-radius: 999px;
  font-size: 0.9rem;
  border: 1px solid transparent;
  cursor: pointer;
  background: transparent;
}

/* login = outline */
.btn-login {
  border-color: #ddd;
}

/* cart = filled */
.btn-cart {
  background-color: #0070f3;
  color: #fff;
}

.btn-cart:hover {
  opacity: 0.9;
}
</style>
