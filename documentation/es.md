<!-- ELUCENIA technical documentation · area-valvar-aortica · es · no clinical/professional/rights approval -->

# Área valvular aórtica (ecuación de continuidad)

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/area-valvar-aortica)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### Diámetro del tracto de salida del ventrículo izquierdo

`dvsve`

cm · intervalo: 1,2–3,5

### Integral velocidad-tiempo (VTI) del tracto de salida del ventrículo izquierdo

`vtivsve`

cm · intervalo: 5–50

### Integral velocidad-tiempo de la válvula aórtica (VTI)

`vtiao`

cm · intervalo: 10–250

### Velocidad aórtica máxima (opcional)

`vmax`

m/s · opcional · intervalo: 0,5–8

### Superficie corporal (opcional)

`sc`

m² · opcional · intervalo: 0,8–3

## Edición del método

EACVI/ASE 2017: continuidad por VTI; DVI; Bernoulli simplificado 4 v²

## Fórmula documentada

Área del TSVI = π × (diámetro ÷ 2)²

Área valvular aórtica = área del TSVI × VTI del TSVI ÷ VTI aórtico

Índice adimensional (DVI) = VTI del TSVI ÷ VTI aórtico

Gradiente máximo (Bernoulli simplificado) = 4 × V²

## Límites y población

La evaluación de la estenosis aórtica en las recomendaciones EACVI/ASE 2017 es integrada: deben considerarse conjuntamente el gradiente, el flujo, la fracción de eyección y la calidad de la evaluación del tracto de salida ventricular. Las situaciones de bajo flujo o bajo gradiente requieren la evaluación específica prevista en el documento. Los valores calculados de forma aislada no reproducen este algoritmo completo.

## Referencias

- [Baumgartner H et al. Recommendations on the echocardiographic assessment of aortic valve stenosis (EACVI/ASE). J Am Soc Echocardiogr, 2017.](https://doi.org/10.1016/j.echo.2017.02.009)

- [Otto CM et al. 2020 ACC/AHA Guideline for the Management of Patients With Valvular Heart Disease. Circulation, 2021.](https://doi.org/10.1161/CIR.0000000000000923)

## Reproducir las pruebas técnicas

Ejecute node test.cjs en el directorio raíz de este repositorio para repetir los casos sintéticos registrados. Se conservan las entradas, los resultados esperados y las tolerancias originales. Las pruebas técnicas no constituyen validación clínica.

```sh
node test.cjs
```

tool.json contiene las fuentes, la edición y el alcance de la revisión. examples.json conserva las entradas y los resultados esperados de los casos sintéticos; results.json registra los resultados obtenidos.

[Ficha y referencias](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referencia](../examples.json) · [results.json](../results.json)

## Revisión y condiciones de uso

No se ha realizado una revisión clínica independiente.

Esta interfaz es una traducción de elaboración propia, no una edición oficial o certificada. No se han realizado la revisión clínica independiente, la revisión lingüística profesional ni la autorización de derechos de los instrumentos.

Resultado de la fórmula o clasificación. La interpretación, la conducta y la aplicabilidad dependen de la evaluación profesional y de la fuente seleccionada.

## Licencia y atribución

Apache-2.0 se aplica únicamente al código de ELUCENIA. Los derechos de los instrumentos, publicaciones, traducciones y datos permanecen en manos de sus respectivos titulares. Conserve LICENSE y NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
