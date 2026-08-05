# GEO: Schema LodgingBusiness + consistencia NAP — Villa Vadori Suites

## 1. JSON-LD `LodgingBusiness` para el `<head>` de la home

Va junto al `FAQPage` que ya armamos (podés tener varios bloques `<script type="application/ld+json">` en la misma página, o combinarlos en un array `@graph`).

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LodgingBusiness",
  "name": "Villa Vadori Suites",
  "image": "https://www.villavadorisuites.ar/[RUTA_A_FOTO_PRINCIPAL]",
  "url": "https://www.villavadorisuites.ar",
  "telephone": "+5493516427600",
  "priceRange": "$$",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "Ruta C45, km 15,2",
    "addressLocality": "Falda del Carmen",
    "addressRegion": "Córdoba",
    "postalCode": "X5187AC",
    "addressCountry": "AR"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": "-31.586603326232545",
    "longitude": "-64.45868938702175"
  },
  "amenityFeature": [
    { "@type": "LocationFeatureSpecification", "name": "Pileta", "value": true },
    { "@type": "LocationFeatureSpecification", "name": "WiFi", "value": true },
    { "@type": "LocationFeatureSpecification", "name": "Aire acondicionado frío/calor", "value": true },
    { "@type": "LocationFeatureSpecification", "name": "Fogón social", "value": true },
    { "@type": "LocationFeatureSpecification", "name": "Asadores", "value": true },
    { "@type": "LocationFeatureSpecification", "name": "Solo adultos (+15 años)", "value": true },
    { "@type": "LocationFeatureSpecification", "name": "Apto mascotas", "value": false }
  ],
  "checkinTime": "14:30",
  "checkoutTime": "10:30",
  "petsAllowed": false,
  "smokingAllowed": false,
  "sameAs": [
    "https://www.instagram.com/villavadori.suites",
    "https://www.google.com/maps/place/Villa+Vadori+suites/@-31.5866415,-64.4606271,17z/data=!3m1!4b1!4m9!3m8!1s0x942d5b0484fd137f:0x9f3f4a696f0f8f2f!5m2!4m1!1i2!8m2!3d-31.5866447!4d-64.4588397!16s%2Fg%2F11gnp701gm",
    "https://www.booking.com/hotel/ar/villa-vadori-suites.html"
  ]
}
</script>
```

✅ Dirección y código postal ya confirmados y corregidos en Google Business Profile: Ruta C45, km 15,2, X5187AC, Falda del Carmen, Córdoba.
✅ Coordenadas confirmadas: -31.586603326232545, -64.45868938702175.

Falta 1 solo dato para cerrar esto:
1. Link directo al perfil de Booking.com de VVS (la URL completa de la propiedad, no solo el nombre) — para sumarlo al `sameAs`.

## 2. Consistencia NAP (Nombre, Dirección, Teléfono)

Esto es lo que las IA y Google cruzan para confirmar que sos una entidad real. Cualquier diferencia (aunque sea "Av." vs "Avenida", o un teléfono viejo dando vueltas) baja la confianza de la señal.

**Checklist — completá con lo que tengas en cada plataforma:**

| Plataforma | Nombre usado | Dirección | Teléfono |
|---|---|---|---|
| Web (villavadorisuites.ar) | Villa Vadori Suites | ? (chequear que diga Ruta C45, km 15,2, X5187AC) | +54 9 351 642-7600 |
| Google Business Profile | Villa Vadori suites | Ruta C45, km 15,2, X5187AC ✅ (ya corregida) | ? |
| Booking.com | Villa Vadori suites ✅ (ya corregido) | ? | ? |
| Instagram (@villavadori.suites) | ? | ? | ? |

Pasame la dirección y teléfono tal como figuran en Booking.com y en Instagram (si están publicados) para terminar de completar la tabla — no bloquea el schema, es un chequeo aparte.

## 3. Nota

El `LodgingBusiness` en VVS y el `LocalBusiness`/gastronómico de Gran Vadori pueden convivir más adelante en la web de Gran Vadori — cuando quieras encaramos ese en un archivo aparte.
