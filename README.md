# 🔧 Prueba Técnica Full-Stack - Medusa + Next.js

## Descripción del Desafío

Desarrolla una extensión personalizada para un e-commerce utilizando Medusa como backend y Next.js como storefront. El objetivo es demostrar habilidades en extensión de modelos, customización del admin panel y manejo del sistema de eventos.

**Stack tecnológico:** TypeScript, Next.js, Medusa.js, PostgreSQL.

---

## 🎯 Funcionalidades a Implementar

### 1. Extensión del Modelo de Producto

**Objetivo:** Agregar campos personalizados al modelo de producto existente.

**Campos requeridos:**
- `is_custom` (boolean): Indica si el producto es personalizable
- `custom_notes` (string, opcional): Notas adicionales sobre la personalización

**Tareas técnicas:**
- **Opción recomendada:** Extender el modelo siguiendo la [documentación oficial](https://docs.medusajs.com/resources/commerce-modules/product/extend)
- **Opción alternativa:** Si se complica la extensión del modelo, puedes usar directamente la metadata del producto que acepta key-value pairs
- Crear migración si optas por extender el modelo
- Validar que los datos se persisten correctamente en la base de datos
- Asegurar compatibilidad con las APIs existentes

### 2. Widget en Medusa Admin

**Objetivo:** Crear un widget personalizado en la página de detalles de producto del Admin.

**Funcionalidades del widget:**
- Mostrar el estado actual de los campos personalizados
- Permitir edición de los campos `is_custom` y `custom_notes`
- Incluir validación de formulario apropiada
- Manejar estados de loading, éxito y error

**Tareas técnicas:**
- Seguir la documentación oficial para inyectar widgets en el Admin
- Crear una interfaz de usuario intuitiva y funcional
- Implementar manejo de estados con React
- Crear los endpoints necesarios que manejen la lógica para añadir, editar o borrar la información
- Asegurar que los cambios se reflejen inmediatamente en el Admin

### 3. Sistema de Eventos y Subscriber

**Objetivo:** Implementar un sistema de eventos que reaccione a cambios en los campos personalizados.

**Funcionalidades:**
- Emitir evento personalizado `product.custom_changed` cuando se modifiquen los campos
- Crear subscriber que capture y procese el evento
- Implementar lógica de respuesta (logging, notificaciones, etc.)

**Tareas técnicas:**
- Usar el Event Module de Medusa para emitir eventos
- Crear subscriber siguiendo las convenciones de Medusa
- Implementar manejo de errores en el subscriber
- Probar que el flujo completo de eventos funciona correctamente
- Documentar los eventos emitidos y su estructura

### 4. Visualización en Storefront 

**Objetivo:** Mostrar la información de personalización en el frontend para los usuarios.

**Funcionalidades:**
- Mostrar badge/indicador visual cuando un producto sea personalizable
- Integrar la visualización con el diseño existente del storefront
- Asegurar responsive design

**Tareas técnicas:**
- Crear componente reutilizable para mostrar información custom
- Integrar con las páginas de producto existentes
- Aplicar estilos consistentes con el design system
- Manejar casos donde no hay información de personalización

---

## 🚀 Setup del Proyecto

### Prerrequisitos
- Node.js 18+
- Git
- PostgreSQL instalado en tu maquina
- Editor de código (VSCode / Cursor / Windsurf)

### Instalación

1. **Crear el proyecto con el starter oficial:**
   ```bash
   npx create-medusa-app@latest mi-prueba-tecnica --with-nextjs-starter
   ```

2. **Verificar que todo funciona:**
   - Backend Admin: http://localhost:9000/app
   - Storefront: http://localhost:8000

3. **Crear productos de prueba:**
   - Acceder al Admin de Medusa
   - Crear al menos 3 productos con diferentes características
   - Configurar imágenes y precios básicos

4. **Comenzar el desarrollo:**
   - Backend: Trabajar en la carpeta del proyecto Medusa
   - Frontend: Trabajar en la carpeta `{proyecto}-storefront`

---

## 📦 Entrega Esperada

### 1. Código Fuente Completo
- **Backend:** Modelo extendido + subscriber funcionando
- **Admin:** Widget inyectado en product detail page
- **Storefront:** Componente de visualización integrado
- **Estructura:** Código organizado y bien comentado

### 2. Documentación
- **README:** Instrucciones de setup y explicación de decisiones técnicas
- **Comentarios:** No es necesario pero es un plus.
- **API:** Documentación de eventos y endpoints custom (si aplica)

### 3. Demo Funcional
- **Video:** Screencast de 3-5 minutos mostrando el flujo completo:
  - Edición de campos en Admin
  - Evento siendo procesado (logs en consola)
  - Visualización en Storefront
- **Deploy:** Opcional pero valorado positivamente

---

## 🤝 Instrucciones de Entrega

1. **Subir código a repositorio Git** (GitHub/GitLab)
2. **Incluir README detallado** con setup y explicaciones
3. **Subir video demo** (YouTube, Loom, o archivo)
4. **Enviar enlace del repositorio** junto con link del video
5. **Tiempo límite:** Sábado 20/09/2025 a las 23:59

---

## ❓ Preguntas Frecuentes

**¿Puedo usar librerías adicionales?**  
Sí, pero justifica su uso en el README.

**¿Es necesario hacer deploy?**  
No es obligatorio, pero se valorará positivamente.

**¿Qué pasa si no termino todo?**  
Entrega lo que tengas funcional y documenta qué falta por implementar.

---

*¡Buena suerte! Demuestra tus habilidades técnicas y creatividad en esta prueba integral de desarrollo full-stack.*
