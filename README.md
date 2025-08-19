# 🔍 Pokédex Simple - PokeAPI

Una aplicación web completa que consume la PokeAPI para explorar, buscar y filtrar Pokémon con interfaz moderna y responsive.

## 📁 Archivos

- `index.html` - Estructura HTML de la Pokédex
- `styles.css` - Estilos CSS con diseño responsive y colores de tipos
- `config.js` - Configuración de la PokeAPI
- `state.js` - Estado global de la aplicación
- `api.js` - Funciones de API y fetch
- `ui.js` - Funciones de interfaz y renderizado
- `app.js` - Lógica principal y event listeners
- `README.md` - Este archivo

## 🚀 Cómo usar

1. **Abrir** el archivo `index.html` en tu navegador
2. **Buscar por nombre**: Escribe el nombre exacto (ej: pikachu, charizard)
3. **Filtrar por tipo**: Selecciona un tipo para ver Pokémon de ese elemento
4. **Navegar**: Usa los botones de paginación para explorar más Pokémon
5. **Ver detalles**: Haz clic en cualquier tarjeta para abrir el modal de detalles

## ✨ Características

- ✅ **Búsqueda por nombre** exacto con manejo de errores 404
- ✅ **Filtro por tipo** con 18 tipos Pokémon estándar
- ✅ **Paginación** con límites configurables (12, 20, 50 por página)
- ✅ **Modal de detalles** con sprites, stats, habilidades y características
- ✅ **Diseño responsive** con grid fluido (1-4 columnas según ancho)
- ✅ **Colores de tipos** auténticos para cada elemento Pokémon
- ✅ **Debounce** de 300ms para búsquedas en tiempo real
- ✅ **Manejo de errores** robusto con mensajes claros
- ✅ **Arquitectura modular** JavaScript para mejor mantenibilidad

## 🔧 Tecnologías

- HTML5 semántico
- CSS3 Grid y Flexbox (responsive)
- JavaScript ES6+ (async/await, fetch, Promise.all)
- PokeAPI v2 (sin claves requeridas)

## 🏗️ Arquitectura Modular

La aplicación está dividida en módulos JavaScript para mejor organización:

- **`config.js`**: Configuración de endpoints de la API
- **`state.js`**: Estado global y variables de la aplicación
- **`api.js`**: Todas las funciones de fetch y consumo de API
- **`ui.js`**: Funciones de renderizado y manejo de interfaz
- **`app.js`**: Lógica principal, event listeners y funciones utilitarias

## 📱 API - PokeAPI

- **Base URL**: `https://pokeapi.co/api/v2/`
- **Endpoints utilizados**:
  - `GET /pokemon?limit={n}&offset={m}` → Listado paginado
  - `GET /pokemon/{name|id}` → Detalle completo del Pokémon
  - `GET /type` → Lista de tipos disponibles
  - `GET /type/{name}` → Pokémon de un tipo específico

## 🎯 Casos de Prueba

### 1. Búsqueda por nombre exitosa
- Buscar "pikachu" → Muestra tarjeta y permite abrir detalle
- **Resultado esperado**: Tarjeta con sprite, nombre, ID y tipos

### 2. Filtro por tipo
- Seleccionar tipo "fire" → Lista Pokémon de fuego
- Abrir detalle de "charmander" → Modal con stats y habilidades
- **Resultado esperado**: Lista filtrada y modal funcional

### 3. Búsqueda inexistente
- Buscar "nombreinexistente" → Mensaje de error 404
- **Resultado esperado**: "No se encontró el Pokémon 'nombreinexistente'"

## 🎨 Características de UI/UX

- **Grid responsive**: Se adapta de 1 a 4 columnas según el ancho de pantalla
- **Badges de tipos**: Colores oficiales para cada tipo Pokémon
- **Modal centrado**: Overlay con información detallada
- **Estados visuales**: Loading, error, sin resultados
- **Accesibilidad**: ARIA labels, lectores de pantalla, navegación por teclado

## 🔍 Funcionalidades de Búsqueda

- **Búsqueda simple**: Solo por nombre
- **Filtro simple**: Solo por tipo
- **Búsqueda combinada**: Nombre + tipo (intersección)
- **Paginación**: Navegación por páginas con límites configurables
- **Límites**: 12, 20 o 50 Pokémon por página

## 📊 Datos del Pokémon

- **Información básica**: Nombre, ID, sprite frontal
- **Tipos**: Badges con colores oficiales
- **Características**: Altura y peso en unidades métricas
- **Estadísticas**: HP, Attack, Defense, Special Attack, Special Defense, Speed
- **Habilidades**: Lista de habilidades del Pokémon
- **Sprites**: Imagen frontal y artwork oficial (si está disponible)

---
*Desarrollado para ejercicios de APIs - Clase 03*
*Migrado de Cat Facts a PokeAPI para demostrar consumo de APIs complejas*
*Arquitectura modular para mejor mantenibilidad y organización del código*
