# Explorateur des cristaux 2D

**Du graphène au MoS₂ : explorateur interactif des cristaux bidimensionnels.**

Le graphène et une monocouche de MoS₂ ont le même réseau en nid d'abeilles. Pourtant, le premier est un semi-métal qui fait un mauvais transistor, et le second un semi-conducteur qui en fait un bon. Cette application de bureau relie la structure du cristal à ses propriétés électroniques, avec des animations et des curseurs.

Projet de l'option PICSEL (Centrale Méditerranée), 2026-2027.

## Versions

L'application est construite par versions successives ; chaque version ajoute un panneau qui réutilise les résultats de la précédente.

| Version | Contenu | État |
|---|---|---|
| v1 Cristal | réseau, réseau réciproque, zone de Brillouin, diffraction | en cours |
| v2 Phonons | dispersion, animation des modes, chaleur spécifique | à faire |
| v3 Bandes | liaisons fortes (graphène, MoS₂), densité d'états | à faire |
| v4 Porteurs | niveau de Fermi, température, dopage, grille | à faire |
| v5 Transport | conductivité (Drude), effet Hall | à faire |
| v6 Transistor | caractéristique courant–tension de grille | à faire |

## Installation

Python 3.12 ou plus récent :

```
pip install -r requirements.txt
```

## Tests

Chaque modèle physique est vérifié par des tests automatiques sur des valeurs de référence publiées :

```
python -m pytest
```

## Organisation du code

```
core/    calcul physique pur, sans interface (un module par version)
ui/      interface PyQt6 (un panneau par version)
tests/   tests des critères de validation
docs/    équations, hypothèses et validations de chaque modèle
```
