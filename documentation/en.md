<!-- ELUCENIA technical documentation · area-valvar-aortica · en · no clinical/professional/rights approval -->

# Aortic valve area (continuity equation)

[conditions, sources and permissions](https://elucenia.org/en/tools/area-valvar-aortica)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### Left ventricular outflow tract diameter

`dvsve`

cm · range: 1.2–3.5

### Left ventricular outflow tract velocity–time integral (VTI)

`vtivsve`

cm · range: 5–50

### Aortic valve velocity–time integral (VTI)

`vtiao`

cm · range: 10–250

### Peak aortic velocity (optional)

`vmax`

m/s · optional · range: 0.5–8

### Body surface area (optional)

`sc`

m² · optional · range: 0.8–3

## Method edition

EACVI/ASE 2017: VTI continuity equation; DVI; simplified Bernoulli 4 v²

## Documented formula

LVOT area = π × (diameter ÷ 2)²

Aortic valve area = LVOT area × LVOT VTI ÷ aortic VTI

Dimensionless index (DVI) = LVOT VTI ÷ aortic VTI

Peak gradient (simplified Bernoulli) = 4 × V²

## Limits and population

Assessment of aortic stenosis in the EACVI/ASE 2017 recommendations is integrated: gradient, flow, ejection fraction and the quality of ventricular outflow tract assessment must be considered together. Low-flow or low-gradient situations require the specific assessment set out in the document. Calculated values alone do not reproduce this complete algorithm.

## References

- [Baumgartner H et al. Recommendations on the echocardiographic assessment of aortic valve stenosis (EACVI/ASE). J Am Soc Echocardiogr, 2017.](https://doi.org/10.1016/j.echo.2017.02.009)

- [Otto CM et al. 2020 ACC/AHA Guideline for the Management of Patients With Valvular Heart Disease. Circulation, 2021.](https://doi.org/10.1161/CIR.0000000000000923)

## Reproduce the technical tests

Run node test.cjs in the root directory of this repository to repeat the recorded synthetic cases. Original inputs, expectations and tolerances are preserved. Technical tests do not constitute clinical validation.

```sh
node test.cjs
```

tool.json contains sources, edition and review scope. examples.json retains synthetic inputs and expectations; results.json records the obtained results.

[Record and references](../tool.json) · [JavaScript code](../calculator.js) · [Reference cases](../examples.json) · [results.json](../results.json)

## Review and conditions of use

Independent clinical review has not been performed.

This interface is an authorial translation, not an official or certified edition. Independent clinical review, professional language review and instrument rights clearance have not been performed.

Formula or classification result. Interpretation, care and applicability depend on professional assessment and the selected source.

## License and attribution

Apache-2.0 applies only to ELUCENIA code. Rights to instruments, publications, translations and data remain with their respective holders. Preserve LICENSE and NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
