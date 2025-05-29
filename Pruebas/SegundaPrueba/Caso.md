# Prueba de Acceso a Endpoint Protegido Sin Autenticación

## Descripción de la Prueba

Se verificó el comportamiento del sistema al intentar acceder a un endpoint protegido sin estar autenticado (es decir, sin proporcionar un token JWT). El objetivo fue confirmar que el sistema restringe correctamente el acceso a estos recursos.

---

## Evidencia

  *Intento de acceder a un endpoint protegido sin autenticación: el sistema responde negando el acceso como se espera.*
  ![Captura desde 2025-05-28 17-22-59](https://github.com/user-attachments/assets/7a8c1ab6-d89d-4c21-b4ca-e21d195c048e)


---

## Impacto

Si el sistema no restringe adecuadamente el acceso a los endpoints protegidos, un atacante podría acceder a información o funcionalidades sensibles sin autorización. Esto comprometería la confidencialidad e integridad de los datos de los usuarios.

---

## Recomendación

El sistema debe requerir siempre un token de autenticación válido para acceder a cualquier endpoint protegido. Si no se proporciona o es inválido, debe responder con un mensaje genérico de acceso denegado, por ejemplo:

> `"Acceso no autorizado"`

---


