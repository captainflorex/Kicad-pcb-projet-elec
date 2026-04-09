# Kicad-pcb-projet-elec - Instrument de musique NE555

## Description
Instrument de musique simple composé de 8 boutons poussoirs et d'un NE555 monté 
en astable. Chaque bouton correspond à une note de la gamme DO RÉ MI FA SOL LA SI DO⁺ 
(octave 4). La fréquence est déterminée par une chaîne de résistances en série, 
calculées et combinées avec des résistances standard (220Ω, 1kΩ, 10kΩ, 20kΩ, 100kΩ).

## Composants
- NE555
- Arduino Nano
- 8 boutons poussoirs
- Résistances (36 au total) :
  - 10× 220Ω
  - 18× 1kΩ
  - 1× 10kΩ
  - 4× 20kΩ
  - 3× 100kΩ
- Condensateur 100nF
- MOSFET 2N7000 (amplification du signal)
- 2× Diodes (protection)
- Potentiomètre 1kΩ (contrôle du volume)
- Haut-parleur
  
## Fichiers
- `projetelec.kicad_sch` — Schéma électronique KiCad
- `projetelec.kicad_pcb` — PCB KiCad
- `projetelec.kicad_pro` — Fichier projet KiCad
- `projetelec.kicad_prl` — Préférences locales KiCad
- `projetelec.wrl` — Modèle 3D du PCB
- `projetelec.round-tracks-config` — Configuration des pistes arrondies
- `freerouting.rules` — Règles de routage automatique

## Résultats obtenus
Toutes les notes dans une tolérance de ±5% sans composants de précision.
