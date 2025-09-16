<h1>Projet : Prévision de consommation d'énergie</h1>

<h2>Objectif du projet</h2>
<p>Prévoir la <strong>consommation d’électricité en France</strong>, de manière <strong>mensuelle ou quotidienne</strong> selon la granularité des données disponibles, en prenant en compte plusieurs facteurs tels que la <strong>saisonnalité</strong> et la <strong>température</strong>.</p>
<p>Pour cela, nous utilisons des méthodes avancées de séries temporelles :</p>
<ul>
  <li><strong>Holt-Winters</strong> (lissage exponentiel)</li>
  <li><strong>SARIMA</strong> (Seasonal ARIMA)</li>
  <li><strong>SARIMAX</strong> (SARIMA avec variables exogènes, par exemple la température)</li>
</ul>

<h2>Outils utilisés</h2>
<ul>
  <li><strong>VS Code</strong> avec l’extension <strong>Jupyter</strong> pour travailler avec des notebooks Python interactifs</li>
  <li>Bibliothèques Python : 
    <ul>
      <li><code>pandas</code>, <code>numpy</code> → manipulation et traitement des données</li>
      <li><code>matplotlib</code>, <code>seaborn</code> → visualisation des séries temporelles</li>
      <li><code>statsmodels</code> → implémentation des modèles Holt-Winters, SARIMA et SARIMAX</li>
      <li><code>scikit-learn</code> → métriques et prétraitement</li>
    </ul>
  </li>
</ul>

<h2>Compétences développées</h2>
<ul>
  <li>Maîtriser les <strong>méthodes de lissage</strong> et la méthode <strong>Holt-Winters</strong></li>
  <li>Comprendre les <strong>composantes d’une série temporelle</strong> et les <strong>modèles de décomposition</strong></li>
  <li>Maîtriser les <strong>modèles SARIMA et SARIMAX</strong> pour les prévisions saisonnières</li>
  <li>Savoir <strong>représenter graphiquement</strong> une série temporelle et analyser ses tendances et saisonnalités</li>
</ul>



<p>Le projet est inspiré de :<br>
<a href="https://github.com/nalron/project_electricity_forecasting/tree/french_version" target="_blank">https://github.com/nalron/project_electricity_forecasting/tree/french_version</a>
</p>

<h2>Étapes du projet</h2>
<ol>
  <li><strong>Visualisation des données</strong> : explorer les séries temporelles, identifier les tendances, saisonnalités et anomalies.</li>
  <li><strong>Nettoyage des données</strong> : traiter les valeurs manquantes et les anomalies.</li>
  <li><strong>Correction de la consommation</strong> : ajuster les valeurs en fonction des variations climatiques et des degrés-jours de chauffage (DJU). Pour plus de détails, consulter le lien : 
    <a href="https://www.enoptea.fr/articles/comment-corriger-mes-consommations-denergie-en-fonction-des-variations-climatiques-dju/" target="_blank">
    https://www.enoptea.fr/articles/comment-corriger-mes-consommations-denergie-en-fonction-des-variations-climatiques-dju/
    </a>
  </li>
  <li><strong>Application des modèles de prévision</strong> : OLS, Holt-Winters, SARIMA, SARIMAX.</li>
  <li><strong>Évaluation des performances</strong> : comparer les prévisions avec les valeurs réelles et calculer les métriques d’erreur (MAE, RMSE, etc.).</li>
</ol>



<div style="margin-top: 20px;"></div>

<p>Pour comprendre les modèles en détail :<br>
<a href="https://perso.univ-rennes1.fr/valerie.monbet/ST_M1/CoursST2017_1.pdf" target="_blank">https://perso.univ-rennes1.fr/valerie.monbet/ST_M1/CoursST2017_1.pdf</a>
</p>

<h2>les bibléothéques utilisées:</h2>
<pre>
import pandas as pd                   # Pour manipuler et analyser des données tabulaires (CSV, DataFrame)
import matplotlib.pyplot as plt       # Pour tracer des graphiques simples (courbes, histogrammes, scatter plots)
import seaborn as sns                 # Pour créer des visualisations statistiques et esthétiques (heatmaps, boxplots)
from sklearn.linear_model import LinearRegression  # Pour construire des modèles de régression linéaire
import numpy as np                    # Pour effectuer des calculs numériques et manipuler des tableaux/matrices
import statsmodels.api as sm          # Pour réaliser des modèles statistiques avancés et des tests
from statsmodels.graphics.gofplots import ProbPlot  # Pour tracer des Q-Q plots et vérifier la normalité des résidus
from statsmodels.tsa.seasonal import seasonal_decompose  # Pour décomposer une série temporelle en tendance, saisonnalité et résidu
from statsmodels.tsa.holtwinters import ExponentialSmoothing  # Pour appliquer le modèle Holt-Winters (saison + tendance)
from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score  # Pour évaluer les performances des modèles
from statsmodels.graphics.tsaplots import plot_acf, plot_pacf  # Pour visualiser l’autocorrélation et la partial autocorrélation
from statsmodels.tsa.statespace.sarimax import SARIMAX  # Pour construire des modèles SARIMAX avec ARIMA + saisonnalité + variables exogènes
import itertools                       # Pour générer automatiquement des combinaisons et permutations de paramètres
</pre>

