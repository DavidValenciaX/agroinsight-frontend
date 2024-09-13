# AgroInsight Frontend Application

## Descripción del Proyecto

AgroInsight es una aplicación innovadora diseñada para optimizar el cultivo de maíz en la región del Huila, Colombia. Utiliza una arquitectura cliente-servidor. El frontend está conformado por una aplicación móvil y una aplicación web desarrolladas con **React Native** utilizando **Expo** y **TypeScript**.

### Características Principales

- Análisis de suelos mediante procesamiento de imágenes
- Detección temprana del gusano cogollero utilizando visión artificial
- Integración de datos meteorológicos de OpenWeatherMap
- Generación de reportes y recomendaciones personalizadas basadas en IA
- Funcionalidad offline y sincronización de datos

## Requisitos previos

Antes de comenzar, asegúrate de cumplir con los siguientes requisitos:

- Tener instalado **Node.js** versión 14 o superior.
- Haber instalado **Expo CLI** globalmente ejecutando:
  ```bash
  npm install -g expo-cli
  ```

- Contar con un dispositivo/emulador Android o iOS para ejecutar la app.

## Instalación

1. **Clona el repositorio**:
   ```bash
   git clone <url-del-repositorio>
   cd AgroInsight_Front
   ```

2. **Instala las dependencias**:
   Ejecuta el siguiente comando en el directorio del proyecto para instalar los paquetes necesarios:
   ```bash
   npm install
   ```

## Ejecutando la Aplicación

1. **Inicia el servidor de desarrollo de Expo**:
   ```bash
   expo start
   ```

2. **Corre la app en un emulador Android/iOS**:
   - Presiona `a` para abrir el emulador de Android.
   - Presiona `i` para abrir el simulador de iOS (solo en MacOS).
   
   Alternativamente, puedes escanear el código QR que aparece en Expo Developer Tools usando la app **Expo Go** en tu dispositivo Android o iOS.

3. **Comandos útiles para ejecución rápida**:
   - Para correr la aplicación en Android directamente desde el emulador, puedes usar:
     ```bash
     npm run android
     ```
   - Para ejecutar la versión web del proyecto, utiliza:
     ```bash
     npm run web
     ```

## Estructura del Proyecto
```bash
├── assets
│   ├── adaptive-icon.png
│   ├── agro.png
│   ├── favicon.png
│   ├── header.png
│   ├── icon.png
│   ├── logo.png
│   └── splash.png
├── components
│   ├── ConfirmIdentity.tsx
│   ├── Header.tsx
│   ├── Home.tsx
│   ├── LoginScreen.tsx
│   ├── RegisterScreen.tsx
│   └── Verification.tsx
├── app.json
├── App.tsx
└── tsconfig.json
```

### Archivos Clave
- **App.tsx**: Contiene la navegación principal que maneja el flujo entre pantallas (inicio de sesión, registro, etc.).
- **LoginScreen.tsx**: Gestión del inicio de sesión.
- **RegisterScreen.tsx**: Gestión del registro de usuarios.
- **ConfirmIdentity.tsx** y **Verification.tsx**: Manejan la confirmación de identidad y la autenticación en dos pasos.
- **Home.tsx**: Pantalla principal a la que los usuarios son redirigidos después de un inicio de sesión exitoso.

### API del Backend
Esta aplicación se comunica con un backend alojado en:
```
https://agroinsight-backend-production.up.railway.app
```

La API se utiliza para el registro de usuarios, inicio de sesión y autenticación en dos pasos.

## Desarrollo

Para realizar cambios o extender la aplicación, ten en cuenta:
- Seguir las buenas prácticas de **TypeScript** para tipar componentes y propiedades.
- Utilizar las utilidades incorporadas de **Expo** para gestionar activos y personalización específica de la plataforma.
  
### Comandos Útiles

- **Linting**:
  Ejecuta ESLint para verificar si existen problemas de estilo:
  ```bash
  npm run lint
  ```

- **Construir APK (Android)**:
  Para generar un archivo APK que se pueda distribuir:
  ```bash
  expo build:android
  ```

- **Construir IPA (iOS)**:
  Para generar una aplicación para iOS (requiere MacOS):
  ```bash
  expo build:ios
  ```