# Prueba de Registro con Email Inválido

## Descripción de la Prueba

Se verificó si el sistema valida correctamente el formato y la legitimidad del correo electrónico al registrar un usuario. Para ello, se intentó registrar un usuario utilizando un email aparentemente válido en formato pero absurdo en la práctica, como `google@google.com`.

---

## Evidencia

*Se realizó el registro de un usuario con el email `google@google.com` y el sistema permitió el registro sin validar la legitimidad del correo.*

![Captura desde 2025-05-28 20-04-28](https://github.com/user-attachments/assets/4b7430d8-4f22-4f8e-ab6e-e28cb3db7029)

---

## Impacto

Permitir el registro con emails inválidos o absurdos puede derivar en cuentas falsas, problemas de comunicación, spam y dificultades en la gestión y recuperación de cuentas.

---

## Recomendación

El sistema debe validar no solo el formato correcto del email, sino también su legitimidad (por ejemplo, evitando dominios genéricos o reservados, direcciones notoriamente falsas, etc.). Al recibir un email inválido, el registro debe ser rechazado con un mensaje apropiado que indique el error.

---
