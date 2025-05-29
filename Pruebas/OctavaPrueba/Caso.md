# Prueba de Fuerza Bruta en Login

## Descripción de la Prueba

Se verificó si el sistema implementa mecanismos de rate limiting o bloqueo temporal ante múltiples intentos fallidos de login para un mismo usuario. El objetivo fue evaluar la resistencia del sistema frente a ataques de fuerza bruta.

---

## Evidencia

  *Se realizaron múltiples intentos de login con un usuario válido y contraseñas incorrectas en un corto periodo de tiempo. El sistema permitió todos los intentos sin bloquear ni limitar el acceso.*
  
![Captura desde 2025-05-28 19-59-36](https://github.com/user-attachments/assets/c8016559-662e-4f0d-ad84-767bd1ca9ec4)

---

## Impacto

La ausencia de mecanismos de protección ante ataques de fuerza bruta expone a los usuarios a un mayor riesgo de que sus contraseñas sean adivinadas mediante intentos automatizados. Esto compromete la seguridad de las cuentas y del sistema en general.

---

## Recomendación

El sistema debe implementar controles como rate limiting, bloqueos temporales o aumento progresivo del tiempo de espera tras varios intentos fallidos de autenticación. Esto dificulta los ataques automatizados y protege las cuentas de los usuarios.

---

