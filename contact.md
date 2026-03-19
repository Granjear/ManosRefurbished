---
layout: page
title: Manos a la Tierra - Contacto
keywords: ""
description: ""
---

<div style="text-align: center; font-weight: bold; font-size: 1.2em;">CONTACTO</div>

<div style="text-align: center; font-weight: bold; font-size: 1.2em; margin-top: 1em;">Asociación Civil Manos a la Tierra</div>

<div style="text-align: center; margin-top: 1em;">
    <a href="http://www.manosalatierra.org.ar" target="_blank">www.manosalatierra.org.ar</a>
</div>

<div class="zpelement-wrapper form" name="form" style="margin-top: 20px; padding: 20px; background: rgba(255,255,255,0.8); border-radius: 8px;">
    <h2 style="color: #4a7c24; margin-bottom: 15px;">Envíanos un mensaje</h2>
    <form action="https://api.web3forms.com/submit" method="POST">
        <input type="hidden" name="access_key" value="4fe3f562-a839-4f28-a4ac-d4cc0eefc4ab">
        
        <div style="margin-bottom: 15px;">
            <label for="name" style="display: block; margin-bottom: 5px; color: #333; font-weight: bold;">Nombre:</label>
            <input type="text" id="name" name="name" required style="width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 4px; box-sizing: border-box;">
        </div>
        
        <div style="margin-bottom: 15px;">
            <label for="email" style="display: block; margin-bottom: 5px; color: #333; font-weight: bold;">Email:</label>
            <input type="email" id="email" name="email" required style="width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 4px; box-sizing: border-box;">
        </div>
        
        <div style="margin-bottom: 15px;">
            <label for="message" style="display: block; margin-bottom: 5px; color: #333; font-weight: bold;">Mensaje:</label>
            <textarea id="message" name="message" rows="5" required style="width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 4px; box-sizing: border-box; resize: vertical;"></textarea>
        </div>
        
        <!-- Optional: Custom redirect after submission -->
        <input type="hidden" name="redirect" value="http://127.0.0.1:4000/contact.html?success=true">
        
        <!-- Optional: Spam Protection (Honeypot) -->
        <input type="checkbox" name="botcheck" class="hidden" style="display: none;">

        <button type="submit" style="background-color: #fca311; color: white; border: none; padding: 12px 20px; font-size: 16px; font-weight: bold; border-radius: 4px; cursor: pointer; transition: background-color 0.3s;">Enviar Mensaje</button>
    </form>
    
    <script>
        // Simple script to show success message if redirected with ?success=true
        const urlParams = new URLSearchParams(window.location.search);
        if (urlParams.get('success') === 'true') {
            const successMsg = document.createElement('div');
            successMsg.style.backgroundColor = '#d4edda';
            successMsg.style.color = '#155724';
            successMsg.style.padding = '10px';
            successMsg.style.marginBottom = '15px';
            successMsg.style.borderRadius = '4px';
            successMsg.style.border = '1px solid #c3e6cb';
            successMsg.innerText = '¡Gracias! Tu mensaje ha sido enviado correctamente.';
            document.querySelector('form').prepend(successMsg);
        }
    </script>
</div>
