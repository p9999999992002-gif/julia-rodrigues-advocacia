<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const scrolled = ref(false)
const menuOpen = ref(false)

const handleScroll = () => scrolled.value = window.scrollY > 40

onMounted(() => window.addEventListener('scroll', handleScroll))
onUnmounted(() => window.removeEventListener('scroll', handleScroll))
</script>

<template>
  <header :class="['header', { scrolled }]">
    <div class="container">
      <div class="logo">
        <span>Julia Rodrigues</span>
        <span class="subtitle">ADVOCACIA TRABALHISTA • OAB/SP</span>
      </div>

      <nav class="nav">
        <a href="#home">Início</a>
        <a href="#about">Sobre</a>
        <a href="#areas">Atuação</a>
        <a href="#contact">Contato</a>
      </nav>

      <a href="#contact" class="cta-btn">CONSULTA GRATUITA</a>

      <button @click="menuOpen = !menuOpen" class="mobile-menu-btn">
        <span :class="{ active: menuOpen }"></span>
        <span :class="{ active: menuOpen }"></span>
        <span :class="{ active: menuOpen }"></span>
      </button>
    </div>
  </header>
</template>

<style scoped>
.header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
  background: rgba(6, 8, 16, 0.95);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid rgba(200,169,110,0.1);
}

.container {
  max-width: 1280px;
  margin: 0 auto;
  padding: 1.2rem 2rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 2rem;
}

.header.scrolled{
  background: rgba(6,8,16,0.82);
  border-bottom: 1px solid rgba(200,169,110,0.12);
}

.logo {
  display: flex;
  flex-direction: column;
  gap: 0.15rem;
  line-height: 1;
}

.logo span:first-child {
  font-family: 'Cormorant Garamond', serif;
  font-size: 1.9rem;
  font-weight: 600;
  color: white;
}

.subtitle {
  font-size: 0.68rem;
  letter-spacing: 2px;
  color: #c8a96e;
  text-transform: uppercase;
  margin-left: 2px;
}

.nav {
  display: flex;
  gap: 2.5rem;
  font-size: 0.95rem;
}

.nav a {
  color: #d6d6d6;
  text-decoration: none;
  transition: all 0.3s ease;
  position: relative;
}

.nav a::after{
  content:'';
  position:absolute;
  left:0;
  bottom:-6px;
  width:0%;
  height:1px;
  background:#c8a96e;
  transition:0.35s;
}

.nav a:hover::after{
  width:100%;
}

.cta-btn {
  border: 2px solid #c8a96e;
  color: #c8a96e;
  padding: 0.75rem 2rem;
  font-size: 0.85rem;
  font-weight: 600;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  transition: all 0.4s;
  white-space: nowrap;
}

.cta-btn:hover {
  background: #c8a96e;
  color: #060810;
}

.mobile-menu-btn { display: none; }

@media (max-width: 900px) {
  .nav, .cta-btn { display: none; }
  .mobile-menu-btn {
    display: flex;
    flex-direction: column;
    gap: 5px;
    background: none;
    border: none;
  }
  .mobile-menu-btn span {
    width: 28px;
    height: 2.5px;
    background: white;
    transition: 0.4s;
  }
  .mobile-menu-btn .active:nth-child(1) { transform: rotate(45deg) translate(5px, 5px); }
  .mobile-menu-btn .active:nth-child(2) { opacity: 0; }
  .mobile-menu-btn .active:nth-child(3) { transform: rotate(-45deg) translate(6px, -6px); }

  .mobile-menu {
    position: absolute;
    top: 100%;
    left: 0;
    right: 0;
    background: #060810;
    padding: 2rem;
    flex-direction: column;
    gap: 1.5rem;
    display: none;
  }
  .mobile-menu.open { display: flex; }
}
</style>