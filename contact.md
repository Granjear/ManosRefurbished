---
layout: page
title: Contacto
keywords: ""
description: "Contacta con la Asociación Civil Manos a la Tierra."
---

<div style="text-align: center; margin-bottom: var(--space-lg);">
    <h2 style="color: var(--primary-dark); margin-bottom: var(--space-sm);">Asociación Civil Manos a la Tierra</h2>
    <p><a href="http://www.manosalatierra.org.ar" target="_blank" style="font-weight: 600; font-size: 1.2em;">www.manosalatierra.org.ar</a></p>
</div>

<div class="card" style="max-width: 600px; margin: 0 auto; padding: var(--space-lg);">
    <h3 style="color: var(--primary); margin-bottom: var(--space-md); text-align: center;">Envíanos un mensaje</h3>
    <form action="https://api.web3forms.com/submit" method="POST">
        <input type="hidden" name="access_key" value="4fe3f562-a839-4f28-a4ac-d4cc0eefc4ab">
        
        <div style="margin-bottom: var(--space-sm);">
            <label for="name" style="display: block; margin-bottom: 5px; font-weight: 600;">Nombre:</label>
            <input type="text" id="name" name="name" required style="width: 100%; padding: 12px; border: 1px solid var(--border); border-radius: var(--radius-sm); font-family: var(--font-family);">
        </div>
        
        <div style="margin-bottom: var(--space-sm);">
            <label for="email" style="display: block; margin-bottom: 5px; font-weight: 600;">Email:</label>
            <input type="email" id="email" name="email" required style="width: 100%; padding: 12px; border: 1px solid var(--border); border-radius: var(--radius-sm); font-family: var(--font-family);">
        </div>
        
        <div style="margin-bottom: var(--space-md);">
            <label for="message" style="display: block; margin-bottom: 5px; font-weight: 600;">Mensaje:</label>
            <textarea id="message" name="message" rows="5" required style="width: 100%; padding: 12px; border: 1px solid var(--border); border-radius: var(--radius-sm); font-family: var(--font-family); resize: vertical;"></textarea>
        </div>
        
        <!-- Optional: Custom redirect after submission -->
        <input type="hidden" name="redirect" value="http://127.0.0.1:4000/contact.html?success=true">
        
        <!-- Optional: Spam Protection (Honeypot) -->
        <input type="checkbox" name="botcheck" class="hidden" style="display: none;">

        <div style="text-align: center;">
            <button type="submit" class="btn btn-secondary" style="width: 100%; border: none; font-size: 1.1em; cursor: pointer;">Enviar Mensaje</button>
        </div>
    </form>
    
    <script>
        const urlParams = new URLSearchParams(window.location.search);
        if (urlParams.get('success') === 'true') {
            const successMsg = document.createElement('div');
            successMsg.style.backgroundColor = '#d4edda';
            successMsg.style.color = '#155724';
            successMsg.style.padding = '15px';
            successMsg.style.marginBottom = '20px';
            successMsg.style.borderRadius = '8px';
            successMsg.style.border = '1px solid #c3e6cb';
            successMsg.style.textAlign = 'center';
            successMsg.style.fontWeight = 'bold';
            successMsg.innerText = '¡Gracias! Tu mensaje ha sido enviado correctamente.';
            document.querySelector('form').prepend(successMsg);
        }
    </script>
</div>
