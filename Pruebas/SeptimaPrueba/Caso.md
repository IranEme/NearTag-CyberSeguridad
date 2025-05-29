# Prueba de Inyección SQL Básica

## Descripción de la Prueba

Se evaluó la resistencia del sistema ante intentos básicos de inyección SQL. Para ello, se envió un payload como `' OR 1=1--` en un campo de texto (por ejemplo, en el campo de correo electrónico durante el registro, login o actualización de datos).

---

## Evidencia

  *Se envió el payload SQL en un campo de texto. El sistema aceptó el valor como si fuera un dato común, sin rechazarlo ni mostrar errores.*
  
![Captura desde 2025-05-28 19-56-05](https://github.com/user-attachments/assets/14a1845f-8461-40dd-aa18-0db4179d7306)



---

## Impacto

Aceptar cadenas que contienen posibles inyecciones SQL sin validación o sanitización puede representar un riesgo si el sistema no maneja correctamente las consultas a la base de datos. Aunque en esta prueba no se evidenciaron errores ni comportamientos inesperados, el sistema debería prevenir y rechazar este tipo de entradas para reforzar la seguridad.

---

## Recomendación

El sistema debe validar y sanear todos los inputs recibidos, rechazando cualquier cadena que contenga patrones típicos de inyección SQL. Además, nunca debe mostrar mensajes de error internos que puedan revelar detalles de la base de datos o de la consulta ejecutada.

---
