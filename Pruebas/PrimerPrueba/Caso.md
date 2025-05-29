

# Prueba de Enumeración de Correos Electrónicos

## Descripción de la Prueba

Se verificó el comportamiento del sistema al intentar iniciar sesión con correos electrónicos registrados y no registrados. El objetivo fue identificar si el sistema revela información sobre la existencia de cuentas de usuario a través de los mensajes de error en el endpoint de autenticación.

---

## Evidencia

  *Intento de login con correo NO registrado: el sistema indica explícitamente que el usuario no existe.*
  ![Captura desde 2025-05-28 17-16-54](https://github.com/user-attachments/assets/f1da4b3b-6ce8-4fe5-8806-f143c05d31d3) 
  


  *Intento de login con correo registrado y contraseña incorrecta: el sistema indica explícitamente que la contraseña es incorrecta.*
![Captura desde 2025-05-28 17-20-52](https://github.com/user-attachments/assets/de2bc1db-98ec-4b6e-a18a-c0830417e676)

---

## Impacto

Este comportamiento permite a un atacante comprobar la existencia de direcciones de correo electrónico registradas en el sistema, simplemente observando los mensajes de error. Esta vulnerabilidad es conocida como **enumeración de usuarios** y puede ser utilizada para:

- Recolectar emails válidos y lanzar ataques dirigidos (phishing, fuerza bruta, etc).
- Comprometer la privacidad de los usuarios.

---

## Recomendación

El sistema **NO debe revelar si un email está registrado**. Se recomienda mostrar siempre un mensaje de error genérico, por ejemplo:

> `"Usuario y/o contraseña incorrectos"`

Esto previene que un atacante pueda distinguir entre un usuario no registrado y una contraseña incorrecta.

---
