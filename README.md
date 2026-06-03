# Catálogo Trigueña — Visualita

## Cómo subir a GitHub Pages

1. Descomprima este ZIP.
2. Verá `index.html` y la carpeta `assets/` en la raíz.
3. Copie **ambos** (`index.html` + carpeta `assets/`) dentro del repositorio local `Visualita`, en su Escritorio.
   - Reemplace el `index.html` que ya tenía.
   - Reemplace o fusione la carpeta `assets/` si ya existía.
4. Haga commit y push como siempre.
5. En unos minutos el sitio refrescará en:
   https://erodriguez-88.github.io/Visualita/

## Estructura del proyecto

```
index.html                      → archivo principal (60 KB)
assets/
  ├── sistema/                  → logo, tabla de medidas
  ├── gala/                     → 150 fotos · 38 prendas
  ├── sf/                       → 30 fotos · 10 prendas
  ├── boho/                     → 96 fotos · 27 prendas
  └── telas/
      ├── manta/                → 2 fotos
      ├── plizada/              → 6 fotos
      ├── lino/                 → 5 fotos
      ├── manta-india/          → 6 fotos
      └── (manta-colombiana)    → pendiente, muestra placeholder
```

## Lo nuevo en esta versión

- Sección **Telas** rehecha con galería interactiva: el visitante toca un thumbnail y la foto principal cambia para mostrar otro tono.
- 7 cards de tela: Manta sedada · Plizada · Lino · Manta india · Manta colombiana · Manta · Licra colombiana.
- Recorte automático de la UI de iOS en los screenshots de Instagram (X, íconos, "Tu historia", etc.).
- Imágenes separadas en `assets/` para que carguen rápido y se puedan cachear.

## Pendiente

- **Manta colombiana** muestra el placeholder "Foto pendiente" porque la carpeta venía vacía en el ZIP de telas. Cuando tenga la foto, agréguela como `assets/telas/manta-colombiana/hero.jpg` y reemplace en `index.html` el bloque:

  ```html
  <div class="tci empty">Foto pendiente</div>
  ```

  Por:

  ```html
  <div class="tci"><img src="assets/telas/manta-colombiana/hero.jpg" loading="lazy" alt="Manta colombiana"/></div>
  ```
