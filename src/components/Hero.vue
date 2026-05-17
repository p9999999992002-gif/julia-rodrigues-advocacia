<script setup>
const stats = [
  { num: "8+", label: "Anos de experiência" },
  { num: "450+", label: "Casos resolvidos" },
  { num: "97%", label: "Clientes satisfeitos" }
]
</script>

<template>
  <section id="home" class="hero">
    <div class="content">
      <div class="text-side">
        <span class="badge">DIREITO TRABALHISTA</span>

        <h1>
          Seus direitos<br>
          <em>defendidos</em><br>
          com precisão.
        </h1>

        <p class="description">
          Advocacia trabalhista estratégica e humana.
          Defendo seus direitos com dedicação,
          transparência e foco em resultados reais.
        </p>

        <div class="actions">
          <a href="#contact" class="main-cta">
            Agendar Consulta Gratuita
          </a>

          <a href="#areas" class="secondary-link">
            Ver Áreas de Atuação →
          </a>
        </div>

        <div class="stats">
          <div
            v-for="(stat, i) in stats"
            :key="i"
            class="stat-item"
          >
            <strong>{{ stat.num }}</strong>
            <span>{{ stat.label }}</span>
          </div>
        </div>
      </div>

      <div class="image-side">
        <div class="image-wrapper">
          <img src="/julia.jpg" alt="Julia Rodrigues" />

          <div class="info-overlay">
            <p class="name">JULIA RODRIGUES</p>
            <p class="title">Advogada Trabalhista</p>
            <p class="location">São Paulo • OAB/SP</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  min-height: 100vh;
  background: #060810;
  display: flex;
  align-items: center;
  padding-top: 110px;
  padding-bottom: 4rem;
  position: relative;
  overflow: hidden;
}

.hero::before {
  content: '';
  position: absolute;
  width: 700px;
  height: 700px;
  background: radial-gradient(circle, rgba(200,169,110,0.08), transparent 70%);
  top: -220px;
  right: -180px;
  pointer-events: none;
}

.content {
  max-width: 1280px;
  margin: 0 auto;
  padding: 0 2rem;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 5rem;
  align-items: center;
  width: 100%;
  position: relative;
  z-index: 2;
}

.badge {
  color: #c8a96e;
  font-size: 0.85rem;
  letter-spacing: 4px;
  text-transform: uppercase;
}

h1 {
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(3rem, 6vw, 5rem);
  line-height: 1;
  color: white;
  margin: 1.3rem 0;
  font-weight: 600;
}

h1 em {
  color: #c8a96e;
  font-style: italic;
  font-weight: 300;
}

.description {
  font-size: 1.08rem;
  color: rgba(255,255,255,0.78);
  max-width: 540px;
  line-height: 1.9;
  margin-bottom: 2.5rem;
}

.actions {
  display: flex;
  align-items: center;
  gap: 1.8rem;
  flex-wrap: wrap;
}

.main-cta {
  background: #c8a96e;
  color: #060810;
  padding: 1.15rem 2.7rem;
  font-weight: 700;
  letter-spacing: 1px;
  text-transform: uppercase;
  text-decoration: none;
  transition: all 0.35s ease;
  border: 1px solid #c8a96e;
}

.main-cta:hover {
  transform: translateY(-3px);
  background: transparent;
  color: #c8a96e;
}

.secondary-link {
  color: #c8a96e;
  text-decoration: none;
  font-size: 1rem;
  display: flex;
  align-items: center;
  transition: all 0.3s ease;
}

.secondary-link:hover {
  transform: translateX(4px);
  opacity: 0.85;
}

.stats {
  margin-top: 4rem;
  display: flex;
  gap: 3rem;
  flex-wrap: wrap;
}

.stat-item {
  display: flex;
  flex-direction: column;
  gap: 0.4rem;
}

.stat-item strong {
  font-size: 2.3rem;
  color: #c8a96e;
  line-height: 1;
}

.stat-item span {
  color: rgba(255,255,255,0.82);
  font-size: 1rem;
}

.image-wrapper {
  position: relative;
  border: 1px solid rgba(200, 169, 110, 0.16);
  padding: 10px;
  background: #0f1626;
  box-shadow: 0 20px 60px rgba(0,0,0,0.45);
  overflow: hidden;
}

img {
  width: 100%;
  aspect-ratio: 3 / 4;
  object-fit: cover;
  display: block;
}

.info-overlay {
  position: absolute;
  left: 30px;
  right: 30px;
  bottom: 30px;
  background: rgba(6, 8, 16, 0.88);
  padding: 1.2rem 1.5rem;
  border: 1px solid rgba(200,169,110,0.25);
}

.name {
  color: #c8a96e;
  font-weight: 700;
  letter-spacing: 1px;
  font-size: 0.9rem;
}

.title {
  font-size: 1.45rem;
  color: white;
  margin: 8px 0;
  font-family: 'Cormorant Garamond', serif;
}

.location {
  color: rgba(255,255,255,0.65);
  font-size: 0.92rem;
}

@media (max-width: 980px) {
  .content {
    grid-template-columns: 1fr;
    gap: 4rem;
  }

  .text-side {
    text-align: center;
  }

  .description {
    margin-left: auto;
    margin-right: auto;
  }

  .actions {
    justify-content: center;
  }

  .stats {
    justify-content: center;
  }
}

@media (max-width: 768px) {
  .hero {
    padding-top: 130px;
    padding-bottom: 5rem;
  }

  .content {
    gap: 3rem;
    padding: 0 1rem;
  }

  h1 {
    font-size: 3rem;
    line-height: 1.05;
  }

  .description {
    font-size: 1rem;
    line-height: 1.7;
  }

  .actions {
    flex-direction: column;
    gap: 1rem;
  }

  .main-cta {
    width: 100%;
    text-align: center;
  }

  .image-wrapper {
    padding: 8px;
  }

  img {
    aspect-ratio: 4 / 5;
  }

  .info-overlay {
    left: 12px;
    right: 12px;
    bottom: 12px;
    padding: 0.8rem 1rem;
  }

  .title {
    font-size: 1.2rem;
  }

  .stats {
    gap: 1.5rem;
  }

  .stat-item strong {
    font-size: 1.8rem;
  }
}
</style>