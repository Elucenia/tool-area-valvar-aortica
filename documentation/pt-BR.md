<!-- ELUCENIA technical documentation · area-valvar-aortica · pt-BR · no clinical/professional/rights approval -->

# Área valvar aórtica (equação de continuidade)

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/area-valvar-aortica)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### Diâmetro da via de saída do VE

`dvsve`

cm · intervalo: 1,2–3,5

### VTI da via de saída do VE

`vtivsve`

cm · intervalo: 5–50

### VTI da valva aórtica

`vtiao`

cm · intervalo: 10–250

### Velocidade máxima aórtica (opcional)

`vmax`

m/s · opcional · intervalo: 0,5–8

### Superfície corporal (opcional)

`sc`

m² · opcional · intervalo: 0,8–3

## Edição do método

EACVI/ASE 2017:continuidade por VTI; DVI; Bernoulli simplificado 4 v²

## Fórmula documentada

Área da VSVE = π × (diâmetro ÷ 2)²

Área valvar aórtica = área da VSVE × VTI da VSVE ÷ VTI aórtico

Índice adimensional (DVI) = VTI da VSVE ÷ VTI aórtico

Gradiente máximo (Bernoulli simplificado) = 4 × V²

## Limites e população

A avaliação da estenose aórtica nas recomendações EACVI/ASE 2017 é integrada: gradiente, fluxo, fração de ejeção e qualidade da avaliação da via de saída ventricular devem ser considerados juntos. Situações de baixo fluxo ou baixo gradiente exigem a avaliação específica prevista no documento. Os valores calculados isoladamente não reproduzem esse algoritmo completo.

## Referências

- [Baumgartner H et al. Recommendations on the echocardiographic assessment of aortic valve stenosis (EACVI/ASE). J Am Soc Echocardiogr, 2017.](https://doi.org/10.1016/j.echo.2017.02.009)

- [Otto CM et al. 2020 ACC/AHA Guideline for the Management of Patients With Valvular Heart Disease. Circulation, 2021.](https://doi.org/10.1161/CIR.0000000000000923)

## Reproduzir os testes técnicos

Execute node test.cjs na pasta raiz deste repositório para repetir os casos sintéticos registrados. As entradas, expectativas e tolerâncias originais são preservadas. Testes técnicos não constituem validação clínica.

```sh
node test.cjs
```

tool.json contém fontes, edição e escopo de revisão. examples.json conserva as entradas e expectativas sintéticas; results.json registra os resultados obtidos.

[Ficha e referências](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referência](../examples.json) · [results.json](../results.json)

## Revisão e condições de uso

Revisão clínica independente não realizada.

Esta interface é uma tradução autoral, não uma edição oficial ou certificada. Revisão clínica independente, revisão linguística profissional e autorização de direitos de instrumentos não foram realizadas.

Resultado da fórmula ou classificação. Interpretação, conduta e aplicabilidade dependem da avaliação profissional e da fonte selecionada.

## Licença e atribuição

Apache-2.0 aplica-se somente ao código da ELUCENIA. Os instrumentos, publicações, traduções e dados mantêm os direitos dos respectivos titulares. Preserve LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Resultados documentados

As informações abaixo preservam as saídas do método para exemplos sintéticos. Não constituem validação clínica independente.

### 1

Estenose aórtica importante pela área

| Detalhes do resultado | |
| --- | --- |
| Área da VSVE | 3,14 cm² |
| Índice adimensional (DVI) | 0,25 |
| Gradiente máximo (4V²) | 64 mmHg |


### 2

Estenose aórtica moderada pela área

| Detalhes do resultado | |
| --- | --- |
| Área da VSVE | 3,80 cm² |
| Índice adimensional (DVI) | 0,37 |

