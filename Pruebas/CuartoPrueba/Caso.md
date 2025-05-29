# Prueba de Registro Doble con el Mismo Correo

## Descripción de la Prueba

Se verificó el comportamiento del sistema al intentar registrar dos cuentas utilizando el mismo correo electrónico. El objetivo fue comprobar si el sistema permite la creación de cuentas duplicadas con el mismo correo, lo cual no debería ser posible.

---

## Evidencia

  
  *Primer intento de registro con un correo válido: el sistema permite la creación de la cuenta.*
![Captura desde 2025-05-28 17-49-17](https://github.com/user-attachments/assets/04b5c79e-ec3c-4253-804d-f303f053a17e)


  *Segundo intento de registro con el mismo correo: el sistema rechaza el registro e indica que el correo ya está registrado.*
![Captura desde 2025-05-28 17-52-03](https://github.com/user-attachments/assets/3c99f29e-2b25-4049-8b1b-bfc8c27e7d05)


## Impacto

Permitir el registro de múltiples cuentas con el mismo correo electrónico puede generar confusión, problemas de recuperación de cuentas y potenciales riesgos de seguridad. El sistema debe garantizar la unicidad del correo electrónico para cada cuenta de usuario.

---

## Recomendación

El sistema debe rechazar cualquier intento de registro con un correo electrónico que ya se encuentre registrado. El mensaje de error debe ser genérico para no revelar si el correo ya existe, por ejemplo:

> `"No se pudo completar el registro. Por favor, verifique sus datos."`

De esta forma, se evita la enumeración de usuarios y se mantiene la integridad de la base de datos.

---

