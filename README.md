# Diablo Huma Dataset — Traje del Diablo Huma / Aya Uma de Pujilí

Conjunto de imágenes originales del traje emblemático del **Diablo Huma (Aya Uma)** de Pujilí (Cotopaxi, Ecuador), recopilado para el entrenamiento de un modelo **LoRA (Low-Rank Adaptation)** orientado a la preservación y difusión digital de este elemento del patrimonio cultural ecuatoriano mediante inteligencia artificial.

Este repositorio contiene **únicamente las imágenes originales** (sin editar). Las versiones recortadas, redimensionadas y etiquetadas usadas en el entrenamiento se derivan de estas.

## Contenido

```
diablo-huma-dataset/
├── images/          # 33 imágenes originales (.jpg)
├── SOURCES.csv      # autor, licencia y URL de cada imagen
└── README.md
```

## Origen de los datos

Las imágenes provienen de tres tipos de fuentes:

1. Repositorios de acceso libre con licencia Creative Commons (**Flickr** y **Wikimedia Commons**).
2. Fuentes institucionales de patrimonio y cultura del Ecuador (Cancillería, Asamblea Nacional, Viceministerio de Cultura, UTPL).
3. Fotografías de autores independientes bajo licencia CC.

El detalle completo (título, autor, licencia y URL de origen) de cada imagen está en [`SOURCES.csv`](SOURCES.csv).

## Licencias y uso

**No existe una licencia única para todo el conjunto.** Cada imagen conserva la licencia asignada por su autor original. El conjunto reúne, entre otras:

- **CC BY-SA 2.0 / 4.0** (atribución + compartir igual)
- **CC BY-NC-SA 2.0 / 4.0** (atribución + no comercial + compartir igual) — imágenes N.º 4, 30, 32 y 33
- **CC0** (dominio público) — imagen N.º 14

Por incluir material **NonCommercial (NC)** y **ShareAlike (SA)**, este conjunto se comparte **exclusivamente con fines académicos y de investigación**, citando en todo momento al autor y la licencia correspondiente (ver `SOURCES.csv`). Cualquier reutilización debe respetar la licencia individual de cada imagen. No se autoriza el uso comercial del conjunto en bloque.

## Uso para entrenamiento de LoRA

Este dataset se empleó para entrenar un adaptador LoRA sobre **FLUX.2 [klein] 9B** con **Ostris AI-Toolkit**.

- **Palabra de activación (trigger):** `d14bl0huma`
- **Etiquetado:** descripciones en lenguaje natural (no tags booru), ya que FLUX interpreta mejor la prosa.
- **Preparación:** recorte y redimensionamiento a 512/768/1024 px; edición/limpieza con Qwen-Image-Edit.

Para reproducir la preparación y el etiquetado se usó la herramienta utilitaria del proyecto:
https://github.com/ErickColumba/UtitiesPython

Ejemplo de prompt de generación:

```
d14bl0huma, full body of the masked dancer standing in a cobblestone street of Pujili, fur chaps, tall pompom headdress, colonial church behind, festival
```

## Cómo citar

> Columba Párraga, E. D. (2025). *Diablo Huma Dataset: imágenes del traje del Diablo Huma de Pujilí para entrenamiento de modelos LoRA.* Repositorio del proyecto de titulación, [Universidad Central del Ecuador]. Imágenes bajo licencias Creative Commons individuales (ver SOURCES.csv).


