<p align="center">
  <img src="Logo_Geomark_mini.JPG" alt="Geomark Solutions SIG" width="260"/>
</p>

<h1 align="center">Carte interactive – Carreaux FILOSOFI 2021<br><sub>Le Tampon · La Réunion</sub></h1>

<p align="center">
  <img src="https://img.shields.io/badge/Leaflet-1.9.4-199900?logo=leaflet&logoColor=white"/>
  <img src="https://img.shields.io/badge/Données-INSEE%20FILOSOFI%202021-0055A4"/>
  <img src="https://img.shields.io/badge/Projection-WGS84-gray"/>
  <img src="https://img.shields.io/badge/Licence-MIT-orange"/>
</p>

---

## 📌 Description

Application cartographique interactive développée avec **Leaflet.js** pour visualiser et analyser les données du **Fichier Localisé Social et Fiscal (FILOSOFI) 2021** à l'échelle des **carreaux de 200 mètres** sur la commune du **Tampon (La Réunion)**.

Trois couches géographiques issues du référentiel IGN et de l'INSEE sont superposées :

| Couche | Source | Format |
|--------|--------|--------|
| Carreaux 200 m (FILOSOFI 2021) | INSEE | GeoJSON |
| Bâti (BD TOPO) | IGN | GeoJSON |
| Communes | IGN Admin Express | GeoJSON |

---

## 🗺️ Fonctionnalités

- **4 fonds de plan** : OpenStreetMap, Google Maps, Google Hybrid, Fond blanc
- **Basculement des couches** : Communes, Carreaux 200 m, Bâti (chargé à la demande)
- **Panneau de filtres FILOSOFI** : 17 attributs filtrables par opérateur (≥ / ≤ / =)
- **Popups détaillées** sur chaque entité (attributs complets)
- **Compteur dynamique** des carreaux visibles après filtrage
- Légende intégrée

---

## 📂 Structure du projet

```
/
├── carte_tampon.html      ← Application principale
├── carreaux.geojson       ← Carreaux FILOSOFI 200m (1 651 entités)
├── commune.geojson        ← Périmètre communal (25 entités)
├── bati.geojson           ← Bâtiments BD TOPO (55 658 entités, ~14 Mo)
├── Logo_Geomark_mini.JPG  ← Logo Geomark Solutions SIG
└── README.md
```

---

## 🧮 Attributs FILOSOFI disponibles dans les filtres

| Attribut | Description |
|----------|-------------|
| `ind` | Nombre d'individus (population) |
| `men` | Nombre de ménages |
| `men_pauv` | Ménages sous le seuil de pauvreté |
| `men_1ind` | Ménages d'une seule personne |
| `men_prop` | Ménages propriétaires |
| `men_fmp` | Familles monoparentales |
| `men_coll` | Ménages en logement collectif |
| `men_mais` | Ménages en maison individuelle |
| `log_soc` | Logements sociaux |
| `log_ap90` | Logements construits après 1990 |
| `log_av45` | Logements construits avant 1945 |
| `ind_snv` | Somme des niveaux de vie (€) |
| `ind_0_3` à `ind_80p` | Population par tranche d'âge |

---

## 🚀 Déploiement sur GitHub Pages

1. Créer un dépôt GitHub public
2. Déposer tous les fichiers à la racine
3. Activer **Settings → Pages → Deploy from branch `main`**
4. Accéder à `https://<votre-compte>.github.io/<votre-repo>/carte_tampon.html`

> ⚠️ Le fichier `bati.geojson` fait ~14 Mo. Le chargement du bâti se fait à la demande (case à cocher).

---

## 🛠️ Technologies utilisées

- [Leaflet.js](https://leafletjs.com/) 1.9.4
- Fonds Google Maps via tuiles XYZ non officielles *(usage personnel/démonstration)*
- Données INSEE FILOSOFI 2021 – carreaux 200 m
- Données IGN BD TOPO® & Admin Express®
- Conversion : GDAL / ogr2ogr (EPSG:2975 → EPSG:4326)
- Simplification géométrique : Mapshaper

---

## 📬 Contact

<table>
  <tr>
    <td>
      <img src="Logo_Geomark_mini.JPG" width="120"/>
    </td>
    <td>
      <strong>Robin MAUME</strong><br>
      Chef de projet | Consultant | Formateur SIG<br><br>
      📍 63A rue Paul Cézanne · 97432 La Ravine des Cabris<br>
      📞 (+33) 06.13.18.47.10<br>
      📞 (+262) 06.93.61.69.23<br>
      ✉️ <a href="mailto:maumerobin@yahoo.fr">maumerobin@yahoo.fr</a><br>
      🔗 <a href="http://www.linkedin.com/in/robin-maume/">linkedin.com/in/robin-maume</a>
    </td>
  </tr>
</table>

---

<p align="center">
  <sub>© 2025 Geomark Solutions SIG – Tous droits réservés</sub>
</p>
