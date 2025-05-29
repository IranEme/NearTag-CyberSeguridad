
# Prueba de Acceso a Endpoint Protegido con Token Inválido

## Descripción de la Prueba

Se verificó el comportamiento del sistema al intentar acceder a un endpoint protegido utilizando un token JWT inválido o manipulado. El objetivo fue comprobar que el sistema rechaza correctamente el acceso cuando el token no es válido.

---

## Evidencia


  *Intento de acceder a un endpoint protegido usando un token JWT inválido: el sistema rechaza la petición y no permite el acceso.*
![Captura desde 2025-05-28 17-41-14](https://github.com/user-attachments/assets/c45b54e6-b8fd-499d-b414-64d24db1903a)

---

## Impacto

Si el sistema no valida correctamente los tokens de autenticación, un atacante podría manipular tokens para intentar acceder a información o funcionalidades restringidas. Validar la integridad de los tokens es fundamental para la seguridad de la aplicación y la protección de los datos de los usuarios.

---

## Recomendación

El sistema debe validar siempre la autenticidad y validez de los tokens JWT proporcionados en las peticiones a endpoints protegidos. Si el token es inválido, manipulado o expirado, se debe responder con un mensaje genérico de acceso denegado, por ejemplo:

> `"Acceso no autorizado"`

---

