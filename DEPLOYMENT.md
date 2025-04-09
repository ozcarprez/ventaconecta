# Guía de Despliegue para VentaConecta

## Requisitos previos
- Cuenta en Vercel (https://vercel.com)
- Git instalado en tu computadora
- Node.js y npm instalados

## Pasos para desplegar en Vercel

### 1. Preparar el repositorio

Primero, crea un repositorio en GitHub, GitLab o Bitbucket y sube el código:

```bash
# Inicializar git en el proyecto
git init

# Añadir todos los archivos
git add .

# Hacer commit de los cambios
git commit -m "Versión inicial de VentaConecta"

# Conectar con tu repositorio remoto (reemplaza la URL)
git remote add origin https://github.com/tu-usuario/ventaconecta.git

# Subir los cambios
git push -u origin main
```

### 2. Desplegar en Vercel

#### Opción 1: Desde la interfaz web de Vercel

1. Inicia sesión en [Vercel](https://vercel.com)
2. Haz clic en "New Project"
3. Importa tu repositorio de GitHub, GitLab o Bitbucket
4. Configura el proyecto:
   - Framework Preset: Vite
   - Build Command: `npm run build`
   - Output Directory: `dist`
5. Haz clic en "Deploy"

#### Opción 2: Usando Vercel CLI

1. Instala Vercel CLI:
   ```bash
   npm install -g vercel
   ```

2. Inicia sesión en Vercel:
   ```bash
   vercel login
   ```

3. Despliega el proyecto:
   ```bash
   vercel
   ```

4. Sigue las instrucciones en pantalla para completar el despliegue

### 3. Configuración de variables de entorno (si es necesario)

Si necesitas configurar variables de entorno en Vercel:

1. Ve a la configuración del proyecto en Vercel
2. Navega a la sección "Environment Variables"
3. Añade las variables necesarias (por ejemplo, claves de API de Firebase)

## Notas importantes

- La configuración de Firebase debe coincidir entre el entorno de desarrollo y producción
- Asegúrate de que las reglas de seguridad de Firestore estén correctamente configuradas
- Para actualizar la aplicación, simplemente haz push a tu repositorio y Vercel se encargará de redesplegar automáticamente

## Solución de problemas comunes

- Si la aplicación no se carga correctamente, verifica los logs de construcción en Vercel
- Asegúrate de que todas las dependencias estén correctamente listadas en package.json
- Verifica que la configuración de Firebase sea correcta y que todos los servicios necesarios estén habilitados
