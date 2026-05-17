<template>
  <section id="contact" class="contact">
    <div class="container">
      <div class="section-header">
        <span class="badge">CONTATO</span>
        <h2>Agende sua consulta gratuita</h2>
      </div>

      <div class="form-wrapper">
        <form class="form">
          <input type="text" placeholder="Nome completo" required />
          <input type="email" placeholder="Seu melhor e-mail" required />
          <input type="tel" placeholder="WhatsApp com DDD" required />
          <textarea placeholder="Conte brevemente sobre seu caso..." rows="6" required></textarea>
          <button type="submit">ENVIAR MENSAGEM</button>
        </form>

        <div class="contact-info">
          <h3>Informações</h3>
          <div class="info-item">
            <strong>Endereço</strong>
            <p>Rua Monteiro de Melo, 56 — Lapa<br>São Paulo — SP</p>
          </div>
          <div class="info-item">
            <strong>WhatsApp</strong>
            <p>(11) 99999-9999</p>
          </div>
          <div class="info-item">
            <strong>E-mail</strong>
            <p>contato@juliarodrigues.adv.br</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.contact{background:#0a0e1a;color:#fff;padding:8rem 0}.container{max-width:1280px;margin:0 auto;padding:0 1rem}.section-header{text-align:center;margin-bottom:5rem}.section-header h2{font-family:'Cormorant Garamond',serif;font-size:clamp(2.4rem,5vw,3.2rem)}.badge{color:#c8a96e;font-size:.82rem;letter-spacing:4px;text-transform:uppercase}.form-wrapper{max-width:1100px;margin:0 auto;display:grid;grid-template-columns:1fr 1fr;gap:4rem;padding:0 1rem}.form input,.form textarea{width:100%;background:rgba(255,255,255,.05);border:1px solid rgba(200,169,110,.25);padding:1.1rem 1.3rem;color:#fff;margin-bottom:1rem;font-size:1rem;border-radius:4px}.form button{background:#c8a96e;color:#060810;padding:1.2rem;width:100%;font-weight:600;letter-spacing:2px;text-transform:uppercase;cursor:pointer;transition:all .4s;font-size:.95rem;border:none}.form button:hover{background:#fff;transform:translateY(-4px)}.form input:focus,.form textarea:focus{outline:none;border-color:#c8a96e;box-shadow:0 0 0 4px rgba(200,169,110,.08)}.contact-info h3{color:#c8a96e;margin-bottom:2rem;font-size:1.5rem}.info-item{margin-bottom:2rem}.info-item strong{color:#c8a96e;display:block;margin-bottom:.5rem}.info-item p{color:rgba(255,255,255,.8);line-height:1.7}@media (max-width:900px){.form-wrapper{grid-template-columns:1fr;gap:3rem}}@media (max-width:768px){.contact{padding:6rem 0}.form-wrapper{padding:0}.section-header{margin-bottom:3.5rem}}
</style>