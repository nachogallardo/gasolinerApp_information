# 🚗 GasCompare - Comparador de Gasolineras de España

## 📋 Descripción

GasCompare es una aplicación móvil y web para encontrar las gasolineras más baratas de España. Utiliza datos oficiales actualizados en tiempo real del Ministerio de Transición Ecológica y la API de Precioil.es para ayudarte a ahorrar dinero en cada repostaje.

## ✨ Características Principales

### 🗺️ **Visualización de Gasolineras**
- **Mapa Interactivo**: Visualiza todas las gasolineras cercanas en un mapa con Leaflet/OpenStreetMap
- **Vista de Lista**: Alterna entre mapa y lista para ver las gasolineras de forma detallada
- **Marcadores Personalizados**: Cada gasolinera se muestra con un marcador de color según el precio:
  - Verde: Precios más baratos
  - Amarillo: Precios medios
  - Rojo: Precios más caros

### 📍 **Búsqueda por Ubicación**
- **GPS Automático**: Detecta tu ubicación actual con un solo clic
- **Selección Manual en Mapa**: Haz clic en cualquier punto del mapa para buscar gasolineras en esa zona
- **Radio de Búsqueda**: Busca gasolineras en un radio de 7km alrededor de tu ubicación
- **Búsqueda Inteligente**: Sistema robusto de búsqueda paralela con múltiples puntos para encontrar más gasolineras

### ⛽ **Tipos de Combustible**
La aplicación soporta todos los tipos de combustible disponibles en España:
- **Gasolina 95 E5**
- **Gasolina 98 E5**
- **Diésel A**
- **Diésel Premium**
- **Gasolina 95 E5 Premium**
- **Gasolina 98 E5 Premium**

### 🔍 **Filtros Avanzados**

#### **Por Tipo de Combustible**
- Selecciona el tipo de combustible que necesitas
- Los precios se actualizan automáticamente según tu selección
- Comparación instantánea de precios

#### **Por Marca**
- Filtra por tu marca de gasolinera favorita
- Más de 50 marcas disponibles (Repsol, Cepsa, BP, Shell, Galp, etc.)
- Opción "Todas" para ver todas las marcas

#### **Por Precio**
- **Mostrar solo las más baratas**: Filtra automáticamente las gasolineras con mejores precios
- Ordenación automática por precio de menor a mayor
- Visualización clara del ahorro potencial

#### **Por Actualización**
- Opción para ocultar gasolineras con precios desactualizados (más de 7 días)
- Indicador visual del tiempo transcurrido desde la última actualización
- Garantiza información fiable y actualizada

### 🚗 **Planificación de Viajes**

#### **Sistema Inteligente de Rutas**
1. **Selección de Origen y Destino**: Autocompletado con OpenStreetMap Nominatim
2. **Cálculo de Distancia**: Algoritmo propio que calcula la distancia entre puntos
3. **Búsqueda Optimizada**: Encuentra gasolineras en la dirección correcta de tu viaje
4. **Filtrado Inteligente**:
   - Solo gasolineras en los primeros 50km de la ruta
   - Máximo 2.5km de desviación de la ruta
   - Elimina duplicados automáticamente
5. **Selección de la Más Barata**: Algoritmo que encuentra la opción más económica
6. **Integración con Google Maps**: Abre la ruta con waypoint (parada en gasolinera) directamente en Google Maps

#### **Ventajas del Sistema de Viajes**
- 💰 **100% GRATUITO**: No usa APIs de pago
- 🧠 **Inteligente**: Filtra gasolineras en la dirección correcta
- 📍 **Desviación Controlada**: Minimiza desvíos innecesarios
- ⚡ **Rápido**: Una sola búsqueda optimizada
- 🔄 **Robusto**: Funciona sin APIs externas de rutas

### 💾 **Sistema de Caché Inteligente**
- **Caché de 5 minutos**: Los datos se mantienen en memoria para cargas instantáneas
- **Actualización automática**: Cada 10 minutos se refresca automáticamente
- **Indicador de antigüedad**: Muestra cuándo fue la última actualización
- **Búsquedas offline**: Mantiene los últimos resultados disponibles

### 📱 **Detalles de Gasolineras**
Al hacer clic en cualquier gasolinera, verás:
- **Información básica**: Nombre, marca, dirección, código postal
- **Precios de todos los combustibles**: Con indicador visual de precios actualizados/desactualizados
- **Horario de apertura**: Disponibilidad 24h o horarios específicos
- **Distancia**: Desde tu ubicación actual
- **Última actualización**: Fecha y hora de la última actualización de precios
- **Botones de acción**:
  - 🗺️ **Cómo llegar**: Abre Google Maps con direcciones
  - 🧭 **Navegar**: Inicia navegación directa

### 🎨 **Interfaz de Usuario**
- **Diseño Moderno**: Interfaz limpia con Tailwind CSS y shadcn/ui
- **Responsive**: Optimizado para móviles, tablets y escritorio
- **Modo Claro/Oscuro**: (Preparado para implementación futura)
- **Animaciones Fluidas**: Transiciones suaves y feedback visual
- **Sin Publicidad**: Experiencia de usuario sin interrupciones

### 🔄 **Actualización de Datos**
- **Botón de Refresco Manual**: Actualiza los datos cuando quieras
- **Indicador de Carga**: Spinner visual durante las búsquedas
- **Notificaciones Toast**: Feedback claro de operaciones exitosas o errores
- **Gestión de Errores**: Reintentos automáticos y fallbacks

## 🛠️ Tecnologías Utilizadas

### **Frontend**
- **React 18**: Framework principal
- **TypeScript**: Tipado estático
- **Vite**: Build tool ultrarrápido
- **Tailwind CSS**: Estilos utility-first
- **shadcn/ui**: Componentes UI de alta calidad
- **Radix UI**: Componentes accesibles

### **Mapas y Geolocalización**
- **Leaflet**: Librería de mapas interactivos
- **React Leaflet**: Integración de Leaflet con React
- **OpenStreetMap**: Tiles de mapas gratuitos
- **Capacitor Geolocation**: API de geolocalización nativa

### **APIs Externas (100% GRATUITAS)**
- **Precioil.es API**: Datos de gasolineras y precios (API principal)
- **OpenStreetMap Nominatim**: Autocompletado de direcciones
- **Google Maps**: Navegación (sin coste para el usuario final)
- **API MITECO**: Fallback del Ministerio de Transición Ecológica

### **Móvil**
- **Capacitor 7**: Framework para apps nativas
- **Android**: Build nativo para Google Play Store
- **Capacitor Browser**: Apertura de enlaces externos
- **Capacitor App**: Gestión del ciclo de vida de la app

## 📊 Arquitectura de Datos

### **Flujo de Búsqueda de Gasolineras**
1. Usuario solicita búsqueda por ubicación
2. Sistema genera múltiples puntos de búsqueda (estrategia robusta)
3. Búsqueda paralela en 6 puntos simultáneos
4. Agregación y deduplicación de resultados
5. Cálculo de distancias desde ubicación del usuario
6. Ordenación por distancia o precio
7. Aplicación de filtros (marca, combustible, actualización)
8. Renderizado en mapa y/o lista

### **Optimizaciones de Rendimiento**
- **Búsquedas paralelas**: Hasta 6 requests simultáneos
- **Timeout inteligente**: 6 segundos máximo de búsqueda
- **Rate limiting**: Configuración optimizada para evitar bloqueos
- **Retry logic**: Reintentos automáticos con exponential backoff
- **Deduplicación**: Eliminación de gasolineras duplicadas
- **Lazy loading**: Carga progresiva de componentes

## 🚀 Funcionalidades Adicionales

### **Modal de Bienvenida**
- Guía inicial para nuevos usuarios
- Explicación de las características principales
- Se muestra solo la primera vez

### **Gestión de Estado**
- **useState/useEffect**: Manejo de estado local
- **Context API**: (Preparado para estado global)
- **Custom Hooks**: `useAppState`, `useBackButton`, `useMobile`, `useToast`

### **Navegación Móvil**
- **Botón Atrás**: Gestión del botón atrás de Android
- **Deep Links**: Preparado para enlaces profundos
- **App State**: Manejo de estados de la aplicación (background/foreground)

### **Compatibilidad**
- ✅ Android (Google Play Store)
- ✅ Web (Progressive Web App)
- ✅ iOS (Preparado, no desplegado)

## 📈 Ventajas Competitivas

1. **Completamente Gratuito**: Sin costes de API ni subscripciones
2. **Sin Publicidad**: Experiencia limpia sin anuncios
3. **Datos Oficiales**: Información verificada del gobierno
4. **Actualización Constante**: Precios actualizados diariamente
5. **Cobertura Total**: Todas las gasolineras de España
6. **Planificación Inteligente**: Algoritmo único de optimización de rutas
7. **Privacidad**: Solo usa ubicación cuando es necesario
8. **Open Source**: Código abierto y transparente

## 💡 Casos de Uso

### **Para Conductores Diarios**
- Encuentra la gasolinera más barata cerca de casa o trabajo
- Ahorra dinero en cada repostaje
- Compara precios antes de salir

### **Para Viajeros**
- Planifica paradas económicas en viajes largos
- Evita desvíos innecesarios
- Encuentra gasolineras en rutas desconocidas

### **Para Empresas de Transporte**
- Optimiza costes de combustible
- Planifica rutas con paradas estratégicas
- Control de gastos de flota

### **Para Motociclistas**
- Encuentra gasolineras abiertas 24h
- Compara precios de gasolina premium
- Planifica rutas turísticas

## 🔐 Privacidad y Permisos

### **Permisos Utilizados**
- **📍 Ubicación (GPS)**: Solo cuando buscas gasolineras cercanas
- **🌐 Internet**: Necesario para obtener datos actualizados
- **🗺️ Acceso a Mapas**: Para mostrar gasolineras en el mapa

### **Política de Privacidad**
- No se recopilan datos personales
- La ubicación no se almacena ni se comparte
- Sin tracking de terceros
- Sin cookies de publicidad

## 📦 Versión Actual

**Versión**: 1.7.0
**Última Actualización**: Octubre 2025
**Plataformas**: Android, Web

## 🎯 Roadmap Futuro

- [ ] Historial de precios
- [ ] Favoritos y gasolineras guardadas
- [ ] Notificaciones de bajadas de precio
- [ ] Comparativa de ahorro mensual
- [ ] Modo oscuro
- [ ] Soporte para iOS
- [ ] Integración con Waze
- [ ] Reseñas y valoraciones de usuarios
- [ ] Compartir gasolineras con amigos


## 📄 Licencia

Este proyecto está desarrollado como una herramienta de utilidad pública para ayudar a los conductores españoles a ahorrar en combustible.

## 🤝 Contribuciones

¿Tienes ideas para mejorar GasCompare? ¡Las contribuciones son bienvenidas!

---

**GasCompare** - *Ahorra en cada repostaje* 🚗⛽💰
