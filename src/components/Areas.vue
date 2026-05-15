<script setup>
const areas = [
  { title: "Rescisão Contratual", desc: "Negociação e cobrança de todas as verbas rescisórias" },
  { title: "Horas Extras e Adicionais", desc: "Pagamento correto de horas extras, noturno, insalubridade e periculosidade" },
  { title: "Acidente de Trabalho", desc: "Estabilidade, auxílio-acidente e indenizações por dano moral/material" },
  { title: "Assédio Moral e Sexual", desc: "Proteção da dignidade do trabalhador" },
  { title: "FGTS e Contribuições", desc: "Correção monetária, saques e ações contra abusividades" },
  { title: "Justa Causa e Reintegração", desc: "Contestação de demissões injustas e estabilidades" }
]
</script>

<template>
  <section id="areas" class="areas">
    <div class="container">
      <div class="section-header">
        <span class="badge">ESPECIALIDADES</span>
        <h2>Áreas de Atuação</h2>
      </div>

      <div class="grid">
        <div v-for="(area, i) in areas" :key="i" class="card">
          <h3>{{ area.title }}</h3>
          <p>{{ area.desc }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.areas {
  background: #060810;
  color: white;
  padding: 8rem 0;
}

.section-header {
  text-align: center;
  margin-bottom: 5rem;
}

.badge { color: #c8a96e; letter-spacing: 4px; font-size: 0.82rem; }

.section-header h2 {
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(2.6rem, 5vw, 3.5rem);
  margin-top: 1rem;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
  gap: 2.2rem;
  max-width: 1280px;
  margin: 0 auto;
  padding: 0 2rem;
}

.card {
  background: linear-gradient(
    180deg,
    rgba(255,255,255,0.03),
    rgba(255,255,255,0.015)
  );

  border: 1px solid rgba(200,169,110,0.12);
  padding: 2.8rem 2.3rem;
  transition: all 0.4s ease;
  height: 100%;
  backdrop-filter: blur(10px);
}

.card:hover {
  border-color: #c8a96e;
  transform: translateY(-10px);
  background: rgba(200,169,110,0.06);
}

.card h3 {
  color: #c8a96e;
  font-size: 1.35rem;
  margin-bottom: 1rem;
}

.card p {
  color: rgba(255,255,255,0.75);
  line-height: 1.75;
}
</style>