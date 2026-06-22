# Task
# eyesliketomove — Stimuli (FR) · Clé de correction

Plan intra-sujet · 12 tâches + 2 échauffements + 1 baseline · texte à gauche.

| ID | Difficulté | Algorithme | Stimulus | Incohérence | Côté | Fichier |
|----|-----------|------------|----------|-------------|------|---------|
| E1 | easy | Somme d'un tableau | Énoncé + Organigramme | Énoncé : la boucle démarre à i = 1 ; organigramme (correct) démarre à i = 0. | énoncé | `e1_easy_flow_somme_d_un_tableau.html` |
| E2 | easy | Factorielle (itérative) | Énoncé + Organigramme | Organigramme : i démarre à 2 ; énoncé (correct) fait varier i de 1 à n. | organigramme | `e2_easy_flow_factorielle_it_rative.html` |
| E3 | easy | Puissance (itérative) | Énoncé + Organigramme | Énoncé : la boucle va de 1 à exp − 1 ; organigramme (correct) va de 1 à exp. | énoncé | `e3_easy_flow_puissance_it_rative.html` |
| E4 | easy | Recherche linéaire | Énoncé + Code | Code : la boucle va jusqu'à n (hors limites) ; énoncé (correct) s'arrête à n − 1. | code | `e4_easy_code_recherche_lin_aire.html` |
| E5 | easy | Maximum d'un tableau | Énoncé + Code | Énoncé : max initialisé avec tab[1] ; code (correct) initialise avec tab[0]. | énoncé | `e5_easy_code_maximum_d_un_tableau.html` |
| E6 | easy | Compter les occurrences | Énoncé + Code | Code : le compteur cpt est initialisé à 1 ; énoncé (correct) l'initialise à 0. | code | `e6_easy_code_compter_les_occurrences.html` |
| H1 | hard | Tri à bulles | Énoncé + Code | Code : échange si tab[j] < tab[j+1] (tri décroissant) ; énoncé (correct) demande >. | code | `h1_hard_code_tri_bulles.html` |
| H2 | hard | Tri par insertion | Énoncé + Code | Énoncé : j initialisé à i ; code (correct) initialise j à i − 1. | énoncé | `h2_hard_code_tri_par_insertion.html` |
| H3 | hard | Tri par sélection | Énoncé + Code | Code : sélectionne le plus grand (tab[j] > min) ; énoncé (correct) cherche le plus petit. | code | `h3_hard_code_tri_par_s_lection.html` |
| H4 | hard | Recherche binaire | Énoncé + Organigramme | Énoncé : si cible < tab[mil] → moitié droite ; organigramme (correct) → moitié gauche. | énoncé | `h4_hard_flow_recherche_binaire.html` |
| H5 | hard | Tri fusion | Énoncé + Organigramme | Organigramme : droite = triFusion(tab[mil+1:]) (perd l'élément central) ; énoncé (correct) : tab[mil:]. | organigramme | `h5_hard_flow_tri_fusion.html` |
| H6 | hard | Tri rapide | Énoncé + Organigramme | Énoncé : cas de base = tableau vide (taille 0) ; organigramme (correct) = len(tab) ≤ 1. | énoncé | `h6_hard_flow_tri_rapide.html` |
| W1 | warmup | Échanger deux variables | Énoncé + Code | Code : a ← temp (au lieu de a ← b), donc l'échange ne marche pas ; énoncé (correct) copie b dans a. | code | `w1_warmup_code_changer_deux_variables.html` |
| W2 | warmup | Afficher 1 à n | Énoncé + Organigramme | Organigramme : i démarre à 0 ; énoncé (correct) démarre à 1. | organigramme | `w2_warmup_flow_afficher_1_n.html` |
| B1 | baseline | Minimum d'un tableau | Énoncé + Code | Aucune (stimulus de référence cohérent). | — | `b1_baseline_code_minimum_d_un_tableau.html` |

## Comparabilité (mesurée)

| ID | Diff | Stim | mots | phrases | lignes code | ratio surface texte/réf |
|----|------|------|------|---------|-------------|-------------------------|
| E1 | easy | flow | 54 | 5 | - | 0.56 |
| E2 | easy | flow | 51 | 7 | - | 0.56 |
| E3 | easy | flow | 53 | 4 | - | 0.56 |
| E4 | easy | code | 54 | 5 | 5 | 1.06 |
| E5 | easy | code | 50 | 5 | 6 | 0.94 |
| E6 | easy | code | 54 | 5 | 6 | 1.0 |
| H1 | hard | code | 56 | 4 | 6 | 1.0 |
| H2 | hard | code | 66 | 4 | 9 | 0.96 |
| H3 | hard | code | 64 | 4 | 8 | 1.01 |
| H4 | hard | flow | 68 | 5 | - | 0.62 |
| H5 | hard | flow | 60 | 5 | - | 0.73 |
| H6 | hard | flow | 65 | 4 | - | 0.82 |
| W1 | warmup | code | 38 | 3 | 5 | 1.01 |
| W2 | warmup | flow | 37 | 2 | - | 0.29 |
| B1 | baseline | code | 50 | 5 | 6 | 0.94 |
