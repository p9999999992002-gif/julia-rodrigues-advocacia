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
.areas{background:#060810;color:#fff;padding:8rem 0}.container{max-width:1280px;margin:0 auto;padding:0 1rem}.section-header{text-align:center;margin-bottom:5rem}.badge{color:#c8a96e;letter-spacing:4px;font-size:.82rem;text-transform:uppercase}.section-header h2{font-family:'Cormorant Garamond',serif;font-size:clamp(2.6rem,5vw,3.5rem);margin-top:1rem}.grid{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:1.5rem;max-width:1180px;margin:0 auto}.card{background:linear-gradient(180deg,rgba(255,255,255,.03),rgba(255,255,255,.015));border:1px solid rgba(200,169,110,.12);padding:2.2rem 1.8rem;transition:all .4s ease;height:100%;backdrop-filter:blur(10px);text-align:center}.card:hover{border-color:#c8a96e;transform:translateY(-10px);background:rgba(200,169,110,.06)}.card h3{color:#c8a96e;font-size:1.25rem;margin-bottom:1rem}.card p{color:rgba(255,255,255,.75);line-height:1.75}@media (max-width:1100px){.grid{grid-template-columns:repeat(2,minmax(0,1fr))}}@media (max-width:768px){.areas{padding:6rem 0}.grid{grid-template-columns:1fr;gap:1rem}.card{padding:2rem 1.4rem}.section-header{margin-bottom:3.5rem}}
</style>