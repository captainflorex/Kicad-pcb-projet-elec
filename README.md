# Kicad-pcb-projet-elec — Instrument de musique NE555 (8 touches)

## Présentation
Ce dépôt contient un projet **KiCad** pour réaliser un petit **instrument de musique à 8 boutons** (gamme **Do → Do+**, octave 4) basé sur un **NE555** monté en **astable**.

Chaque bouton sélectionne une valeur de résistance dans une chaîne, ce qui fait varier la fréquence d’oscillation du NE555 et permet de jouer la note correspondante sur un **haut-parleur**.  
Un **Arduino Nano** est utilisé comme **fréquencemètre** afin de mesurer les fréquences en temps réel.

## Fonctionnement (vue d’ensemble)
- NE555 en oscillateur astable
- 8 boutons poussoirs → sélection de résistances → fréquence différente par note
- Étape de sortie (MOSFET) + réglage de volume (potentiomètre)
- Arduino Nano : mesure/affichage de la fréquence (fréquencemètre)

## Composants principaux
- NE555
- Arduino Nano (fréquencemètre)
- 8× boutons poussoirs
- Résistances (36 au total) :
  - 10× 220Ω
  - 18× 1kΩ
  - 1× 10kΩ
  - 4× 20kΩ
  - 3× 100kΩ
- 1× condensateur 100nF
- 1× MOSFET 2N7000 (amplification/commande)
- 2× diodes (protection)
- 1× potentiomètre 1kΩ (volume)
- 1× haut-parleur
- 1× buzzer (métronome)

## Fichiers du projet
Fichiers principaux KiCad :
- `projetelec.kicad_sch` — Schéma électronique
- `projetelec.kicad_pcb` — PCB
- `projetelec.kicad_pro` — Projet KiCad

Fichiers / exports utiles :
- `projetelec.wrl` — Modèle 3D du PCB
- `projetelec.round-tracks-config` — Configuration pistes arrondies
- `freerouting.dsn` / `temp-freerouting.dsn` — Fichiers pour autoroutage (Freerouting)
- `projetelectest.kicad_*` — Variante/PCB de test

## Résultats
Les notes obtenues sont dans une tolérance d’environ **±5%** sans composants de précision.

## Ouvrir le projet
1. Installer **KiCad** (version récente recommandée).
2. Ouvrir `projetelec.kicad_pro`.
3. Consulter le schéma (`.kicad_sch`) puis le PCB (`.kicad_pcb`).

## Notes / améliorations possibles
- Ajouter une BOM (liste de composants) et/ou des références de footprints
- Ajouter des captures (schéma + PCB + rendu 3D) dans le README
- Ajouter un tableau “Note → fréquence mesurée” pour documenter le calibrage