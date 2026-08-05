# GEO: FAQPage schema + gaps de contenido — Villa Vadori Suites

## 1. Insertar este JSON-LD en el `<head>` (o antes de `</body>`) de la home

Contenido tomado 1:1 de lo ya publicado en la web — no duplica texto visible, es una capa de datos estructurados para que los motores de IA (ChatGPT, Gemini, Perplexity) lean directamente preguntas y respuestas.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "¿Villa Vadori Suites es solo para adultos?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Sí, Villa Vadori Suites es un complejo exclusivo para adultos, admitiendo huéspedes mayores de 15 años. La capacidad máxima es de 16 huéspedes distribuidos en 8 unidades."
      }
    },
    {
      "@type": "Question",
      "name": "¿Dónde está ubicado Villa Vadori Suites?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Villa Vadori Suites está en Falda del Carmen, Sierras de Córdoba, Argentina, a 30 minutos de Córdoba Capital, 20 minutos de Villa Carlos Paz y 40 minutos de Villa General Belgrano."
      }
    },
    {
      "@type": "Question",
      "name": "¿Qué tipos de unidades tiene Villa Vadori Suites?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Hay 4 cuartos en suite de 20 m² con terraza privada y vista al arroyo, y 4 suites independientes de 24 m² con mayor privacidad y autonomía. Todas cuentan con aire acondicionado frío/calor, WiFi, TV Smart 42\" y limpieza diaria."
      }
    },
    {
      "@type": "Question",
      "name": "¿A qué hora es el check-in y el check-out?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "El check-in es a partir de las 14:30 hs y el check-out hasta las 10:30 hs. Los domingos, dentro de los packs de fin de semana, hay salida tardía disponible."
      }
    },
    {
      "@type": "Question",
      "name": "¿El desayuno está incluido?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Sí. De jueves a domingos y feriados el desayuno se sirve en Gran Vadori de 9 a 11 hs, e incluye café expreso, té, tostadas de pan casero, mermelada artesanal, huevo revuelto, queso crema y jamón asado. El resto de los días se entrega un desayuno seco en la suite."
      }
    },
    {
      "@type": "Question",
      "name": "¿Cuánto cuesta una noche en Villa Vadori Suites?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Valores de referencia en temporada baja, para 2 adultos: una noche con desayuno, desde $140.000 en cuartos en suite y $180.000 en suites independientes. Una noche con desayuno y un almuerzo o cena en Gran Vadori, desde $220.000 en cuartos en suite y $260.000 en suites independientes. Dos noches con desayuno y dos almuerzos o cenas, desde $360.000 en cuartos en suite y $430.000 en suites independientes. Las tarifas varían según temporada y promociones vigentes; consultá disponibilidad actualizada por WhatsApp."
      }
    },
    {
      "@type": "Question",
      "name": "¿Se puede comer en el restaurante Gran Vadori durante la estadía?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Sí. Gran Vadori, a 80 metros de las unidades, es un restaurante de cocina criolla gourmet con 15 años de trayectoria premiada, abierto de jueves a domingo para el almuerzo y los sábados también para la cena."
      }
    },
    {
      "@type": "Question",
      "name": "¿Cómo se hacen las reservas en Villa Vadori Suites?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Las reservas se gestionan exclusivamente por WhatsApp al +54 9 351 642-7600."
      }
    },
    {
      "@type": "Question",
      "name": "¿Se admiten mascotas?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No, Villa Vadori Suites no admite mascotas."
      }
    },
    {
      "@type": "Question",
      "name": "¿Cómo es el servicio de limpieza durante la estadía?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Se realiza limpieza diaria en todas las unidades. Las sábanas se cambian en la cuarta noche de estadía, salvo que se solicite un cambio extra."
      }
    },
    {
      "@type": "Question",
      "name": "¿Qué actividades hay para hacer cerca de Villa Vadori Suites?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "El complejo está al inicio del camino al Observatorio Astronómico, ideal para ciclismo y senderismo, y a 8 km del Autódromo Cabalén, lo que lo convierte en base de grupos de automovilismo, motos y autos clásicos. También recibe grupos de capacitaciones y talleres corporativos."
      }
    }
  ]
}
</script>
```

## 2. Gaps reales de contenido (no cubiertos en ninguna parte de la web)

Agregar como texto visible corto donde corresponda (no requieren sección nueva):

- **Restaurantes cercanos alternativos.** En "Cómo llegar" o "Gastronomía", sumar una línea: *"En la zona también podés encontrar El Quito y Zorra Negra."* — hoy solo está en la Guía del huésped, no en la web pública, y es una consulta típica ("qué otros restaurantes hay cerca").
- **Retiros de yoga/bienestar.** En "Experiencias y actividades grupales" falta el segmento de retiros de yoga/holísticos (sí están ciclismo, motor, capacitaciones). Agregar un bloque corto tipo *"Retiros de yoga y bienestar: el entorno serrano y la privacidad de las unidades independientes son ideales para grupos de retiro."*

## 3. Sobre la tabla de Tarifas (Airtable)

La tabla de precios se carga dinámicamente desde Airtable para mantener unificados los valores entre varias aplicaciones — es intencional, no un bug. Como esos valores no quedan en el HTML estático, los crawlers de IA no los ven. La solución no es cambiar esa tabla, sino sumar un **precio de referencia fijo como texto plano** en la sección FAQ (ver pregunta "¿Cuánto cuesta una noche...?" arriba), aclarando que son valores de temporada baja y que las tarifas actualizadas se consultan por WhatsApp. Esto sí queda indexado, sin tocar la lógica de Airtable.

**Texto visible sugerido para la sección FAQ (además del JSON-LD):**

> **¿Cuánto cuesta una noche en Villa Vadori Suites?**
> Valores de referencia en temporada baja, para 2 adultos:
> - 1 noche con desayuno: desde $140.000 (cuartos en suite) / $180.000 (suites independientes)
> - 1 noche con desayuno + almuerzo o cena en Gran Vadori: desde $220.000 / $260.000
> - 2 noches con desayuno + 2 almuerzos o cenas: desde $360.000 / $430.000
>
> Las tarifas varían según temporada y promociones vigentes. Consultá disponibilidad actualizada por WhatsApp.
