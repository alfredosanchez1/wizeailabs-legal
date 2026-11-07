# WiseAI Labs - Legal Documents

Repositorio centralizado de documentos legales para todos los productos de WiseAI Labs.

## 📋 Contenido

Este repositorio contiene las políticas de privacidad y términos de servicio para:

- **RecipeTuner** - App de escaneo y gestión de recetas con IA
- **CaloriSnap** - App de seguimiento nutricional
- Futuros productos de WiseAI Labs

## 🌐 URLs de Producción

Una vez desplegado en Vercel con dominio personalizado:

### RecipeTuner
- **Privacy Policy:** `https://legal.wiseailabs.com/recipetuner/privacy-policy`
- **Terms of Service:** `https://legal.wiseailabs.com/recipetuner/terms-of-service`

### CaloriSnap
- **Privacy Policy:** `https://legal.wiseailabs.com/calorisnap/privacy-policy`

## 📁 Estructura del Proyecto

```
wizeailabs-legal/
├── index.html                          # Landing page principal
├── recipetuner/
│   ├── privacy-policy.html            # Política de Privacidad (ES/EN)
│   └── terms-of-service.html          # Términos de Servicio (ES/EN)
├── styles/
│   └── main.css                       # Estilos compartidos
├── vercel.json                        # Configuración de Vercel
├── .gitignore
└── README.md
```

## 🚀 Despliegue en Vercel

### Prerrequisitos
- Cuenta en [Vercel](https://vercel.com) (gratis)
- Cuenta en [GitHub](https://github.com)
- Dominio `wiseailabs.com` registrado en GoDaddy

### Paso 1: Crear Repositorio en GitHub

```bash
# Navegar al directorio del proyecto
cd /Users/tuusuario/Desktop/wizeailabs-legal

# Inicializar Git
git init

# Agregar todos los archivos
git add .

# Primer commit
git commit -m "Initial commit: Legal documents for WiseAI Labs products"

# Crear repo en GitHub (https://github.com/new)
# Nombrar: wizeailabs-legal

# Conectar con GitHub
git remote add origin https://github.com/[tu-usuario]/wizeailabs-legal.git
git branch -M main
git push -u origin main
```

### Paso 2: Desplegar en Vercel

1. **Ir a Vercel:** https://vercel.com/signup
2. **Sign up con GitHub** (1 click)
3. **Import Project:**
   - Click "Add New Project"
   - Seleccionar repositorio `wizeailabs-legal`
   - Click "Import"
4. **Deploy:**
   - Framework Preset: Other
   - Root Directory: ./
   - Click "Deploy"
5. **Esperar 30-60 segundos** mientras Vercel construye el sitio

### Paso 3: Configurar Dominio Personalizado en Vercel

1. En Vercel, ir a: **Settings → Domains**
2. Agregar dominio: `legal.wiseailabs.com`
3. Vercel te dará instrucciones de DNS

### Paso 4: Configurar DNS en GoDaddy

1. **Ir a GoDaddy:** https://dcc.godaddy.com/
2. **Mis Productos → Dominios → wiseailabs.com → DNS**
3. **Agregar registro CNAME:**
   ```
   Tipo: CNAME
   Nombre: legal
   Valor: cname.vercel-dns.com
   TTL: 600 (o 10 minutos)
   ```
4. **Guardar cambios**
5. **Esperar propagación DNS** (5-60 minutos, usualmente 10-15 min)

### Paso 5: Verificar Dominio en Vercel

1. Volver a Vercel → Settings → Domains
2. Click "Refresh" hasta que aparezca "Valid Configuration" ✅
3. Vercel configurará automáticamente SSL (HTTPS)

## ✅ Verificación

Una vez completado el setup, verifica que funcionen estas URLs:

- ✅ `https://legal.wiseailabs.com`
- ✅ `https://legal.wiseailabs.com/recipetuner/privacy-policy`
- ✅ `https://legal.wiseailabs.com/recipetuner/terms-of-service`

## 🔄 Actualizar Contenido

Para hacer cambios a los documentos legales:

```bash
# 1. Editar archivos localmente
# 2. Commit cambios
git add .
git commit -m "Update: [descripción del cambio]"
git push

# Vercel automáticamente despliega los cambios en ~30 segundos
```

## 📱 Integración con App Store Connect

### Para RecipeTuner

En **App Store Connect → App Information:**

**Privacy Policy URL:**
```
https://legal.wiseailabs.com/recipetuner/privacy-policy
```

**Terms of Service URL (EULA):**
```
https://legal.wiseailabs.com/recipetuner/terms-of-service
```

### Dentro de la App RecipeTuner

En la pantalla de Settings, agregar links:

```javascript
// Ejemplo en React Native
const openPrivacyPolicy = () => {
  Linking.openURL('https://legal.wiseailabs.com/recipetuner/privacy-policy');
};

const openTermsOfService = () => {
  Linking.openURL('https://legal.wiseailabs.com/recipetuner/terms-of-service');
};
```

## 🌍 Soporte Multiidioma

Todos los documentos de RecipeTuner incluyen soporte para:
- **Español** (idioma por defecto)
- **English** (toggle en parte superior derecha)

El idioma se detecta automáticamente basado en el navegador del usuario.

## 🔒 Seguridad

Los archivos incluyen headers de seguridad configurados en `vercel.json`:
- `X-Content-Type-Options: nosniff`
- `X-Frame-Options: DENY`
- `X-XSS-Protection: 1; mode=block`
- `Referrer-Policy: strict-origin-when-cross-origin`

## 📧 Contacto

- **Soporte:** support@wiseailabs.com
- **Legal:** legal@wiseailabs.com
- **Privacy:** privacy@wiseailabs.com

## 📄 Licencia

© 2026 WiseAI Labs. Todos los derechos reservados.

Este repositorio contiene documentos legales propietarios de WiseAI Labs. El contenido no puede ser copiado, modificado o redistribuido sin autorización expresa.

---

## 🛠️ Mantenimiento

### Actualizar Privacy Policy

1. Editar: `recipetuner/privacy-policy.html`
2. Actualizar fecha: "Última actualización"
3. Commit y push a GitHub
4. Vercel despliega automáticamente

### Actualizar Terms of Service

1. Editar: `recipetuner/terms-of-service.html`
2. Actualizar fecha: "Última actualización"
3. Commit y push a GitHub
4. Vercel despliega automáticamente

### Agregar Nuevo Producto

1. Crear carpeta: `nuevo-producto/`
2. Copiar y adaptar archivos de `recipetuner/`
3. Actualizar `index.html` con nuevo producto
4. Actualizar `vercel.json` con nuevas rutas

---

**Desarrollado con ❤️ por WiseAI Labs**
