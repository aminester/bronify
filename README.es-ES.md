

# Bronify

Bronify es una aplicación de transmisión de música temática basada en canciones parodias de LeBron James. Este repositorio contiene una versión estática de la aplicación optimizada para costos de alojamiento mínimos o nulos, manteniendo toda la funcionalidad de la aplicación original.

## Características

- Sitio web completamente estático sin renderizado del lado del servidor
- Soporte para aplicación web progresiva (PWA) con funcionalidad sin conexión
- Enrutamiento del lado del cliente compatible con alojamiento estático
- Reproducción de medios para contenido de audio y video
- Reproductor de medios personalizado con soporte para listas de reproducción
- Diseño responsivo optimizado para dispositivos móviles

## Requisitos previos

- Node.js (v16 o superior)
- npm o yarn
- Conocimientos básicos de alojamiento web

## Configuración e instalación

1. Clona este repositorio:
```bash
git clone https://github.com/your-username/lebronify.git
cd lebronify
```

2. Instala las dependencias:
```bash
npm install
```

3. Configura los componentes de la interfaz de usuario:
```bash
npm run build
```

## Recursos multimedia

**IMPORTANTE**: Antes de usar esta aplicación, debes agregar tus propios recursos multimedia:

1. Crea un directorio `/assets` en la carpeta `/public` con la siguiente estructura:
```
/public/assets/
  /album-covers/     # Imágenes de carátulas de álbumes
  /audio/            # Archivos MP3 organizados por álbum
  /images/           # Otras imágenes utilizadas en la aplicación
  /thumbnails/       # Miniaturas de video
  /videos/           # Archivos de video
```

2. Actualiza las referencias multimedia en los archivos de datos:
- Los archivos de datos principales se encuentran en `/lib/data.ts` y `/lib/artist-data.ts`
- Todas las URL de medios en estos archivos son marcadores de posición que deben reemplazarse con las rutas reales de tus medios

## Desarrollo

Ejecuta el servidor de desarrollo:

```bash
npm run dev
```

Abre [http://localhost:3000](http://localhost:3000) en tu navegador para ver el resultado.

## Compilación y despliegue

### Compilación del sitio estático

Para compilar el sitio estático:

```bash
npm run build
```

Esto generará un sitio estático en el directorio `out` que puede desplegarse en cualquier servicio de alojamiento estático.

### Opciones de despliegue

#### Opción 1: GitHub Pages

1. Configura un repositorio de GitHub para tu proyecto.
2. Crea un archivo `.github/workflows/deploy.yml` para automatizar el despliegue.
3. Envía tus cambios a GitHub y el sitio estático se desplegará automáticamente.

#### Opción 2: Cloudflare Pages

1. Conecta tu repositorio de GitHub a Cloudflare Pages.
2. Establece el comando de compilación en `npm run build`.
3. Establece el directorio de salida de la compilación en `out`.

#### Opción 3: Alojamiento estático de Vercel

1. Importa tu proyecto en Vercel.
2. Vercel detectará automáticamente el proyecto de Next.js y lo compilará correctamente.

## Personalización

- Modifica `/lib/data.ts` para agregar o actualizar canciones y listas de reproducción
- Modifica `/app/globals.css` para cambiar los estilos
- Agrega tus propios archivos multimedia al directorio `/public/assets`

## Contribuciones

¡Las contribuciones son bienvenidas! No dudes en enviar una Pull Request.

## Licencia

Este proyecto es de código abierto y está disponible bajo la Licencia MIT.
