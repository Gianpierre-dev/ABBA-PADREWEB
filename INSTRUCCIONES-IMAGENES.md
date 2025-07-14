# 📸 **Guía para Agregar Imágenes de Productos**

## 🎯 **Paso 1: Preparar tus Imágenes**

### Especificaciones recomendadas:
- **Formato**: JPG, PNG, WEBP
- **Tamaño**: 300x400 píxeles mínimo
- **Peso**: Máximo 500KB por imagen
- **Nombres**: Usar guiones en lugar de espacios

### Ejemplo de nombres correctos:
```
dress-casual-1.jpg
dress-elegant-1.jpg
dress-vintage-1.jpg
dress-mini-1.jpg
dress-midi-1.jpg
dress-maxi-1.jpg
```

## 📁 **Paso 2: Subir Imágenes a la Carpeta**

### Ubicación correcta:
```
ABBA-PADREWEB/
├── public/
│   ├── products/          ← AQUÍ VAN TUS IMÁGENES
│   │   ├── dress-casual-1.jpg
│   │   ├── dress-elegant-1.jpg
│   │   ├── dress-vintage-1.jpg
│   │   └── ...
│   ├── logoAB.png
│   └── favicon.svg
```

### Cómo subir:
1. **Arrastra y suelta** las imágenes en la carpeta `public/products/`
2. **O copia manualmente** los archivos a esa ubicación
3. **Asegúrate** de que los nombres coincidan con los del archivo `products.json`

## 🛠️ **Paso 3: Verificar en products.json**

### Estructura actual en products.json:
```json
{
  "id": "1",
  "name": "Vestido Coreano Casual Rosa",
  "image": "/products/dress-casual-1.jpg",  ← Esta ruta debe coincidir
  "price": 45.99
}
```

### Lista de imágenes que necesitas:
- `dress-casual-1.jpg`
- `dress-elegant-1.jpg`
- `dress-vintage-1.jpg`
- `dress-mini-1.jpg`
- `dress-midi-1.jpg`
- `dress-maxi-1.jpg`
- `dress-casual-2.jpg`
- `dress-elegant-2.jpg`
- `dress-vintage-2.jpg`
- `dress-mini-2.jpg`
- `dress-midi-2.jpg`
- `dress-maxi-2.jpg`
- `dress-casual-3.jpg`
- `dress-elegant-3.jpg`
- `dress-vintage-3.jpg`
- `dress-mini-3.jpg`
- `dress-midi-3.jpg`
- `dress-maxi-3.jpg`
- `dress-casual-4.jpg`
- `dress-elegant-4.jpg`

## 🔄 **Alternativas Si No Tienes Imágenes**

### Opción 1: Usar URLs temporales
```json
{
  "image": "https://via.placeholder.com/300x400/FFB6C1/FFFFFF?text=Vestido+Rosa"
}
```

### Opción 2: Usar servicios gratuitos
- **Unsplash**: https://unsplash.com/s/photos/korean-dress
- **Pexels**: https://www.pexels.com/search/korean-fashion/
- **Pixabay**: https://pixabay.com/images/search/korean-dress/

### Opción 3: Imagen placeholder mientras consigues las reales
```json
{
  "image": "/products/placeholder-dress.jpg"
}
```

## 🌐 **Usar CDN (Recomendado para Producción)**

### Cloudinary (Gratuito):
1. Regístrate en https://cloudinary.com
2. Sube tus imágenes
3. Copia la URL:
```json
{
  "image": "https://res.cloudinary.com/tu-cuenta/image/upload/v1234567890/dress-1.jpg"
}
```

### Ventajas del CDN:
- ✅ Optimización automática
- ✅ Diferentes tamaños
- ✅ Carga más rápida
- ✅ No ocupa espacio en tu servidor

## 🚀 **Probar tu Sitio**

1. **Guarda** las imágenes en `public/products/`
2. **Reinicia** el servidor: `npm run dev`
3. **Visita** http://localhost:4324
4. **Navega** a la página de productos
5. **Verifica** que las imágenes se muestren correctamente

## 💡 **Consejos Profesionales**

- **Usa nombres descriptivos** para las imágenes
- **Optimiza el peso** de las imágenes antes de subirlas
- **Mantén consistencia** en el tamaño y estilo
- **Considera hacer backup** de tus imágenes
- **Para múltiples imágenes por producto**, usa array:
```json
{
  "images": [
    "/products/dress-1-front.jpg",
    "/products/dress-1-back.jpg",
    "/products/dress-1-detail.jpg"
  ]
}
```

¿Necesitas ayuda específica con algún paso? ¡Pregúntame! 🚀 