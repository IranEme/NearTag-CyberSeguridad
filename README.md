# NearTag-CyberSeguridad - Evidencias de Pruebas de Seguridad

Este repositorio contiene evidencias y reportes de pruebas de seguridad realizadas sobre el sistema. Cada prueba se encuentra documentada en la carpeta `Pruebas`, organizada por tipo y número de prueba.

---

## Estructura de Carpetas

```
Pruebas/
├── primera/       # 1. Enumeración de Correos Electrónicos
├── segunda/       # 2. Acceso a Endpoint Protegido Sin Autenticación
├── tercera/       # 3. Acceso con Token Inválido
├── cuarta/        # 4. Registro con Correo Ya Existente
├── quinta/        # 5. Fuzzing de Campos de Texto
├── sexta/         # 6. XSS Sencillo
├── septima/       # 7. Inyección SQL Básica
├── octava/        # 8. Fuerza Bruta en Login
├── novena/        # 9. Registro con Email Inválido
└── decima/        # 10. Solicitud a Endpoint Inexistente
```

Cada subcarpeta contiene el reporte en formato markdown, junto con las imágenes de evidencia correspondientes.

---

## Lista de Pruebas Realizadas

1. **Enumeración de Correos Electrónicos**  
   Evaluación de mensajes diferenciados al intentar login con correos registrados y no registrados.

2. **Acceso a Endpoint Protegido Sin Autenticación**  
   Verificación de protección de endpoints ante peticiones sin autenticación.

3. **Acceso con Token Inválido**  
   Prueba del rechazo de tokens JWT inválidos o manipulados.

4. **Registro con Correo Ya Existente**  
   Prueba para evitar el registro de cuentas duplicadas con el mismo correo.

5. **Fuzzing de Campos de Texto**  
   Prueba de validación ante datos excesivos o caracteres especiales en campos de entrada.

6. **XSS Sencillo**  
   Evaluación de resistencia a scripts en campos visibles.

7. **Inyección SQL Básica**  
   Prueba de protección ante intentos de inyección SQL en campos de texto.

8. **Fuerza Bruta en Login**  
   Verificación de controles ante múltiples intentos fallidos de autenticación.

9. **Registro con Email Inválido**  
   Prueba de validación de correos electrónicos absurdos o no legítimos.

10. **Solicitud a Endpoint Inexistente**  
    Evaluación de la respuesta del sistema ante rutas no definidas.

---

## Evidencias

Cada reporte incluye capturas de pantalla del resultado de cada prueba, como la siguiente:

![Captura desde 2025-05-28 19-58-52](https://github.com/user-attachments/assets/759daf52-5164-4a13-903c-8eabe590d6ac)




---
