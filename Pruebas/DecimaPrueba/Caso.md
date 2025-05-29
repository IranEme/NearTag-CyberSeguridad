# Prueba de Solicitud a Endpoint Inexistente

## Descripción de la Prueba

Se verificó cómo responde la API ante solicitudes realizadas a rutas que no existen. El objetivo fue confirmar que el sistema maneja adecuadamente estas peticiones, devolviendo un error genérico sin revelar detalles internos.

---

## Evidencia

*Se realizó una petición POST a un endpoint inexistente (`/rutaquenoexiste`). El sistema respondió con un mensaje que indica explícitamente la ruta y el método utilizados.*

![Captura desde 2025-05-28 20-06-39](https://github.com/user-attachments/assets/e08cb2e3-a8e0-4335-8c8b-41cbcfc2921d)


---

## Impacto

Proveer mensajes de error que revelan detalles específicos como la ruta solicitada y el método puede dar información innecesaria a un atacante, facilitando el reconocimiento de la estructura interna de la API y posibles vectores de ataque.

---

## Recomendación

El sistema debe devolver un error 404 (Not Found) acompañado de un mensaje genérico, por ejemplo:

> `"Recurso no encontrado"`

No se deben exponer detalles internos como el path o el método en los mensajes de error.

---
