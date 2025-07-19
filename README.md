# Ferrovil - Sistema de Gestión de Inventario para Ferreterías

<div align="center">
  <img src="https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Android">
  <img src="https://img.shields.io/badge/API-23%2B-brightgreen?style=for-the-badge" alt="API">
  <img src="https://img.shields.io/badge/Version-1.0.0-orange?style=for-the-badge" alt="Version">
</div>

## 📋 Descripción

**Ferrovil** es una aplicación móvil Android desarrollada para la gestión integral de inventarios en ferreterías. El sistema permite administrar productos, realizar ventas, generar facturas y mantener un control detallado del stock y las transacciones comerciales.

## 🎓 Contexto Académico

Este proyecto fue desarrollado como parte del curso de **MANTENIMIENTO, CONFIGURACIÓN Y EVOLUCIÓN DE SOFTWARE** en la Universidad Nacional de San Agustín de Arequipa (UNSA).

### Objetivos del Proyecto
- Aplicar conceptos de mantenimiento de software
- Implementar buenas prácticas de configuración de proyectos
- Demostrar la evolución y mejora continua del software
- Gestionar versiones y control de cambios

## 🚀 Características Principales

### 📦 Gestión de Inventario
- Registro y edición de productos
- Control de stock en tiempo real
- Categorización de productos
- Búsqueda y filtrado avanzado
- Alertas de stock bajo

### 💰 Sistema de Ventas
- Carrito de compras intuitivo
- Generación automática de facturas
- Historial completo de ventas
- Reportes de ventas por período
- Gestión de tasas de cambio

### 📊 Reportes y Estadísticas
- Gráficos de ventas
- Análisis de productos más vendidos
- Reportes de inventario
- Estadísticas de rentabilidad

### 💾 Base de Datos
- SQLite integrado
- Respaldos automáticos
- Sincronización de datos
- Migración de esquemas

## 🛠️ Tecnologías Utilizadas

### Desarrollo Android
- **Java** - Lenguaje principal
- **Android SDK API 23+** - Compatibilidad amplia
- **Material Design** - Interfaz moderna
- **RecyclerView** - Listas eficientes
- **Fragments** - Arquitectura modular

### Bibliotecas Principales
- **MPAndroidChart v3.1.0** - Gráficos y estadísticas
- **Glide 4.11.0** - Carga y gestión de imágenes
- **SQLDroid 1.0.3** - Manejo avanzado de SQLite
- **CircleImageView 3.1.0** - Imágenes circulares
- **Material Components 1.2.1** - Componentes UI

### Herramientas de Desarrollo
- **Android Studio** - IDE principal
- **Gradle 8.12** - Sistema de construcción
- **Git** - Control de versiones
- **GitHub** - Repositorio remoto

## 📱 Requisitos del Sistema

### Mínimos
- Android 6.0 (API 23) o superior
- 2 GB de RAM
- 100 MB de espacio disponible
- Permisos de almacenamiento

### Recomendados
- Android 10.0 (API 29) o superior
- 4 GB de RAM
- 200 MB de espacio disponible
- Conexión a Internet (opcional)

## 📁 Estructura del Proyecto

```
ferrovil/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/teamihc/inventas/
│   │   │   │   ├── activities/          # Actividades principales
│   │   │   │   ├── fragments/           # Fragmentos de UI
│   │   │   │   ├── adapters/            # Adaptadores RecyclerView
│   │   │   │   ├── backend/
│   │   │   │   │   ├── entidades/       # Modelos de datos
│   │   │   │   │   └── Herramientas.java # Utilidades
│   │   │   │   └── dialogs/             # Diálogos personalizados
│   │   │   ├── res/
│   │   │   │   ├── layout/              # Diseños XML
│   │   │   │   ├── drawable/            # Recursos gráficos
│   │   │   │   ├── values/              # Valores y estilos
│   │   │   │   └── menu/                # Menús de navegación
│   │   │   └── assets/
│   │   │       └── database/            # Base de datos SQLite
│   │   └── androidTest/                 # Tests instrumentales
│   └── build.gradle                     # Configuración del módulo
├── gradle/                              # Wrapper de Gradle
├── build.gradle                         # Configuración del proyecto
├── gradle.properties                    # Propiedades de Gradle
└── README.md                           # Este archivo
```

## 🚀 Instalación y Configuración

### 1. Clonar el Repositorio
```bash
git clone https://github.com/Angelol72/InventarioFerreteria.git
cd InventarioFerreteria
```

### 2. Configurar Android Studio
1. Abrir Android Studio
2. Seleccionar "Open an existing project"
3. Navegar a la carpeta del proyecto
4. Esperar la sincronización de Gradle

### 3. Ejecutar la Aplicación
1. Conectar un dispositivo Android o iniciar un emulador
2. Hacer clic en "Run" o presionar `Shift + F10`
3. La aplicación se instalará automáticamente

## 🔧 Configuración de Desarrollo

### Variables de Entorno
Configurar las siguientes variables en `gradle.properties`:
```properties
android.useAndroidX=true
android.enableJetifier=true
org.gradle.jvmargs=-Xmx2048m -Dfile.encoding=UTF-8
```

### Base de Datos
La aplicación incluye una base de datos SQLite preconfigurada ubicada en:
`app/src/main/assets/database/inventas.sqlite`

## 📚 Funcionalidades Detalladas

### Gestión de Productos
- **Crear Producto**: Formulario completo con imagen, precio, stock
- **Editar Producto**: Modificación de datos existentes
- **Eliminar Producto**: Confirmación de eliminación
- **Buscar Producto**: Filtrado por nombre, código o categoría

### Proceso de Venta
1. Selección de productos desde el inventario
2. Añadir al carrito con cantidad específica
3. Revisión y modificación del carrito
4. Generación de factura con totales
5. Actualización automática del stock

### Reportes y Análisis
- **Ventas Diarias**: Gráfico de barras por día
- **Productos Populares**: Lista ordenada por ventas
- **Inventario Actual**: Estado del stock
- **Historial de Transacciones**: Log completo de operaciones

## 🐛 Solución de Problemas Comunes

### Error de Gradle Sync
```bash
./gradlew clean
./gradlew build --refresh-dependencies
```

### Problemas de Base de Datos
1. Verificar que `inventas.sqlite` esté en `assets/database/`
2. Comprobar permisos de almacenamiento
3. Reiniciar la aplicación

### Errores de Compilación
- Verificar versión de Android Studio (2021.1.1+)
- Actualizar Android SDK y Build Tools
- Limpiar y reconstruir el proyecto

## 🔄 Mantenimiento y Evolución

### Control de Versiones
- **Versionado Semántico**: Mayor.Menor.Parche
- **Branches**: main, develop, feature/*
- **Tags**: Para releases estables

### Buenas Prácticas Implementadas
- Separación de responsabilidades
- Patrón MVC en actividades
- Reutilización de componentes
- Documentación del código
- Testing unitario básico

### Evolución Futura
- [ ] Integración con servicios web
- [ ] Sincronización en la nube
- [ ] Modo offline mejorado
- [ ] Reportes avanzados
- [ ] Multi-idioma
- [ ] Backup automático

## 📖 Documentación Adicional

### Arquitectura del Sistema
El proyecto sigue una arquitectura MVC (Model-View-Controller) adaptada para Android:
- **Model**: Entidades en `backend/entidades/`
- **View**: Activities y Fragments
- **Controller**: Lógica en Activities y Adapters

### Patrones de Diseño Utilizados
- **Adapter Pattern**: Para RecyclerViews
- **Singleton**: Para acceso a base de datos
- **Observer Pattern**: Para actualizaciones de UI
- **Factory Pattern**: Para creación de diálogos

## 📞 Soporte y Contacto

Para reportar bugs, solicitar características o contribuir al proyecto:
- **Issues**: Utilizar el sistema de issues de GitHub
- **Email**: Contactar al administrador del repositorio
- **Documentación**: Wiki del proyecto (próximamente)

---

**Desarrollado para el curso de Mantenimiento, Configuración y Evolución de Software - UNSA 2025**
