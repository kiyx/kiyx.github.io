---
title: "Contatti"
permalink: /contact/
layout: single
author_profile: true
---

Hai una proposta o vuoi saperne di più? Scrivimi tramite il form qui sotto (si aprirà il tuo client email).

<form id="contact-form">
  <label>Nome
    <input type="text" id="name" required>
  </label>
  <label>Email
    <input type="email" id="email" required>
  </label>
  <label>Messaggio
    <textarea id="message" rows="5" required></textarea>
  </label>
  <button type="submit" class="btn btn--primary">Invia</button>
</form>

<div id="fallback" class="notice--info" style="display:none;margin-top:1rem;">
  Se non si è aperta l’app di posta, copia l’indirizzo e invia manualmente:
  <code id="mail">espositogiuseppe2003@outlook.it</code>
  <button class="btn btn--small" id="copy">Copia</button>
</div>

<script>
  const to = "espositogiuseppe2003@outlook.it";
  const form = document.getElementById("contact-form");
  form.addEventListener("submit", (e) => {
    e.preventDefault();
    const name = document.getElementById("name").value.trim();
    const email = document.getElementById("email").value.trim();
    const msg = document.getElementById("message").value.trim();

    const subject = `Nuovo messaggio dal Portfolio: ${name}`;
    const body = `Nome: ${name}%0D%0AEmail: ${email}%0D%0A%0D%0AMessaggio:%0D%0A${encodeURIComponent(msg)}`;

    // Prova ad aprire il client email
    window.location.href = `mailto:${to}?subject=${encodeURIComponent(subject)}&body=${body}`;

    // Mostra fallback dopo breve attesa
    setTimeout(() => document.getElementById("fallback").style.display = "block", 1200);
  });

  document.getElementById("copy").addEventListener("click", async () => {
    const mail = document.getElementById("mail").textContent;
    try {
      await navigator.clipboard.writeText(mail);
      alert("Indirizzo copiato negli appunti");
    } catch { alert("Copia non riuscita, seleziona e copia manualmente."); }
  });
</script>

<noscript>
  <p>Email: <a href="mailto:espositogiuseppe2003@outlook.it">espositogiuseppe2003@outlook.it</a></p>
</noscript>