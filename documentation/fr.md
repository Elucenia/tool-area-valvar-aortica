<!-- ELUCENIA technical documentation · area-valvar-aortica · fr · no clinical/professional/rights approval -->

# Surface valvulaire aortique (équation de continuité)

[conditions, sources et autorisations](https://elucenia.org/fr/outils/area-valvar-aortica)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### Diamètre de la chambre de chasse du ventricule gauche

`dvsve`

cm · intervalle: 1,2–3,5

### Intégrale temps-vitesse (ITV) de la chambre de chasse du ventricule gauche

`vtivsve`

cm · intervalle: 5–50

### Intégrale temps-vitesse de la valve aortique (ITV)

`vtiao`

cm · intervalle: 10–250

### Vitesse aortique maximale (facultative)

`vmax`

m/s · facultatif · intervalle: 0,5–8

### Surface corporelle (facultative)

`sc`

m² · facultatif · intervalle: 0,8–3

## Édition de la méthode

EACVI/ASE 2017 : continuité par ITV ; DVI ; Bernoulli simplifié 4 v²

## Formule documentée

Aire de la chambre de chasse VG = π × (diamètre ÷ 2)²

Aire valvulaire aortique = aire de la chambre de chasse VG × ITV de la chambre de chasse VG ÷ ITV aortique

Indice adimensionnel (DVI) = ITV de la chambre de chasse VG ÷ ITV aortique

Gradient maximal (Bernoulli simplifié) = 4 × V²

## Limites et population

L’évaluation de la sténose aortique dans les recommandations EACVI/ASE 2017 est intégrée : gradient, débit, fraction d’éjection et qualité de l’évaluation de la chambre de chasse ventriculaire doivent être considérés ensemble. Les situations de bas débit ou de faible gradient exigent l’évaluation spécifique prévue par le document. Les valeurs calculées isolément ne reproduisent pas cet algorithme complet.

## Références

- [Baumgartner H et al. Recommendations on the echocardiographic assessment of aortic valve stenosis (EACVI/ASE). J Am Soc Echocardiogr, 2017.](https://doi.org/10.1016/j.echo.2017.02.009)

- [Otto CM et al. 2020 ACC/AHA Guideline for the Management of Patients With Valvular Heart Disease. Circulation, 2021.](https://doi.org/10.1161/CIR.0000000000000923)

## Reproduire les tests techniques

Exécutez node test.cjs dans le répertoire racine de ce dépôt pour reproduire les cas synthétiques enregistrés. Les données d’entrée, les résultats attendus et les tolérances d’origine sont conservés. Les tests techniques ne constituent pas une validation clinique.

```sh
node test.cjs
```

tool.json contient les sources, l’édition et le périmètre de la revue. examples.json conserve les données d’entrée et les résultats attendus des cas synthétiques ; results.json consigne les résultats obtenus.

[Fiche et références](../tool.json) · [Code JavaScript](../calculator.js) · [Cas de référence](../examples.json) · [results.json](../results.json)

## Revue et conditions d’utilisation

Aucune révision clinique indépendante n’a été effectuée.

Cette interface est une traduction réalisée par nos soins, et non une édition officielle ou certifiée. La revue clinique indépendante, la révision linguistique professionnelle et l’autorisation des droits sur les instruments n’ont pas été réalisées.

Résultat de la formule ou de la classification. L’interprétation, la conduite et l’applicabilité dépendent de l’évaluation professionnelle et de la source sélectionnée.

## Licence et attribution

Apache-2.0 s’applique uniquement au code d’ELUCENIA. Les droits sur les instruments, publications, traductions et données restent ceux de leurs titulaires respectifs. Conservez LICENSE et NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Résultats documentés

Les informations ci-dessous conservent les sorties de la méthode pour des exemples synthétiques. Elles ne constituent pas une validation clinique indépendante.

### 1

Sténose aortique importante selon la surface

| Détails du résultat | |
| --- | --- |
| Surface du TSVI | 3,14 cm² |
| Indice sans dimension (DVI) | 0,25 |
| Gradient maximal (4V²) | 64 mmHg |


### 2

Sténose aortique modérée selon la surface

| Détails du résultat | |
| --- | --- |
| Surface du TSVI | 3,80 cm² |
| Indice sans dimension (DVI) | 0,37 |

