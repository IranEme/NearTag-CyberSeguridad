# Prueba de XSS Sencillo

## Descripción de la Prueba

Se evaluó la resistencia del sistema ante ataques de Cross-Site Scripting (XSS) al enviar como valor del campo `username` el siguiente texto: `<script>alert(1)</script>`. El objetivo fue comprobar si el sistema sanea, rechaza o filtra adecuadamente contenido potencialmente malicioso.

---

## Evidencia

  
  *Se realizó el registro/modificación con el payload XSS en el campo `username`. El sistema aceptó el contenido, pero al visualizarlo no se ejecutó ningún código.*
  
![Captura desde 2025-05-28 19-51-07](https://github.com/user-attachments/assets/2756af88-71b2-446d-94e9-b2cc2892e3e6)

![Captura desde 2025-05-28 19-51-37](https://github.com/user-attachments/assets/8e02c634-abf3-4c1b-a488-16f5dddd7f71)

---

## Impacto

Aceptar y almacenar contenido con scripts sin sanear puede exponer el sistema a ataques XSS si en algún momento ese dato se muestra en la interfaz sin el debido filtrado. Aunque en la prueba no se ejecutó el código, la presencia de estos datos en la base puede representar un riesgo futuro si cambia la forma en que se presentan.

---

## Recomendación

El sistema debe validar y sanear todos los campos de entrada que puedan mostrarse en la interfaz, rechazando o limpiando cualquier intento de inyectar código. Es recomendable aplicar filtros que eliminen etiquetas `<script>` y otros vectores XSS antes de almacenar o mostrar los datos al usuario.

---

