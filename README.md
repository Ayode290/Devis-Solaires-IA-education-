# Agent-SolarQuote : Devis Solaires IA Éducation

Agent IA qui génère un devis photovoltaïque complet en moins de 2 min pour le Bénin.

## 1. Le Problème
Au Bénin, faire un devis solaire prend 3 à 7 jours. Il faut un technicien sur site, des calculs manuels, et le coût est élevé. Résultat : 90% des ménages et PME n'accèdent pas au solaire.

## 2. Notre Solution : Comment ça fonctionne
`Agent-SolarQuote` est un agent IA multi-étapes. L'utilisateur n'a qu'à remplir 1 formulaire.

**Étape 1 : Input Utilisateur**
L'utilisateur entre : Ville au Bénin, Budget, Surface toit, Consommation kWh/mois, Type de toiture.

**Étape 2 : Agent IA Analyse**
1.  `Agent Météo` : Récupère l'irradiation solaire de la ville via l'API Splunk/Weather.
2.  `Agent Calcul` : Calcule la puissance kWc nécessaire, le nombre de panneaux, la batterie, l'onduleur.
3.  `Agent Coût` : Applique les prix locaux Bénin : panneau, installation, main d'oeuvre, taxes.
4.  `Agent Gemini` : Rédige un devis PDF pro + une note explicative simple pour le client.

**Étape 3 : Output**
En 2 min, l'utilisateur reçoit :
1.  Devis PDF téléchargeable
2.  ROI : Temps de retour sur investissement
3.  Économies sur 25 ans
4.  Schéma de l'installation recommandée

## 3. Stack Technique
-   **Frontend** : Streamlit
-   **IA / LLM** : Google Gemini API
-   **Backend/Calcul** : Python, Pandas, NumPy
-   **Data Météo** : API Splunk
-   **Déploiement** : Streamlit Community Cloud

## 4. Lancer le projet en local
```bash
