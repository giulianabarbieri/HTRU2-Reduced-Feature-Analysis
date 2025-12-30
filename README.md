# HTRU2-Reduced-Feature-Analysis

Language / Idioma:
* [English version](#english)
* [Versión en Español](#español)

<a name="english"></a>
## English Version

# Pulsar Star Classification using Machine Learning 🌌🛰️

This project develops a binary classification system to identify **pulsars** (highly dense, rapidly rotating neutron stars) based on data collected by radio telescopes. The primary goal is to automate the distinction between legitimate pulsar signals and radio frequency interference (RFI) or background noise.

Developed as a Final Project by: **Giuliana Barbieri** and **Almendra Gandini**.

## 📌 Problem Description
Pulsars emit beams of electromagnetic radiation. Due to their rotation, these signals are perceived as periodic pulses. However, in practice, these signals are weak and heavily mixed with terrestrial noise. This project leverages Machine Learning techniques to classify these signals efficiently.

## 📊 Dataset
The **HTRU2** dataset from the UCI Machine Learning Repository is used.
* **Total Samples:** 17,898 signals.
* **Classes:**
    * `0`: Spurious signals (noise/interference).
    * `1`: Confirmed real pulsars.

## 🛠️ Methodology and Technologies
The workflow implemented in the notebook includes:
1. **Exploratory Data Analysis (EDA):** Visualization of distributions and histograms.
2. **Correlation Analysis:** Identification of the most impactful variables.
3. **Modeling:** Implementation of the **XGBoost** (Extreme Gradient Boosting) algorithm.
4. **Evaluation:** Feature Importance analysis.

### Model Features
The model analyzes 8 statistical variables derived from two sources:
* **Integrated Profile (IP Profile):** Mean, standard deviation, excess kurtosis, and skewness.
* **DM-SNR Curve:** Mean, standard deviation, excess kurtosis, and skewness of the dispersion measure.

## 📈 Results and Conclusions
After training with **XGBoost**, the following observations were made:
* **Profile Dominance:** Features associated with the *Integrated Profile* (especially kurtosis and mean) demonstrated significantly higher predictive power than the DM-SNR curve variables.
* **Effectiveness:** The model achieves high precision in separating real signals from noise, streamlining the process of astronomical identification.

<a name="español"></a>
## Versión en Español

# Clasificación de Púlsares mediante Machine Learning 🌌🛰️

Este proyecto desarrolla un sistema de clasificación binaria para identificar **púlsares** (estrellas de neutrones de alta densidad y rotación rápida) a partir de datos recopilados por radiotelescopios. El objetivo principal es automatizar la distinción entre señales legítimas de púlsares y la interferencia por radiofrecuencia (RFI) o ruido de fondo.

Realizado como Trabajo Final por: **Giuliana Barbieri** y **Almendra Gandini**.

## 📌 Descripción del Problema
Los púlsares emiten haces de radiación electromagnética. Debido a su rotación, estas señales se perciben como pulsos periódicos. Sin embargo, en la práctica, estas señales son débiles y se mezclan con ruido terrestre. Este proyecto utiliza técnicas de Machine Learning para clasificar estas señales de manera eficiente.

## 📊 Dataset
Se utiliza el dataset **HTRU2** proveniente del repositorio UCI Machine Learning.
* **Muestras totales:** 17,898 señales.
* **Clases:**
    * `0`: Señales espurias (ruido/interferencia).
    * `1`: Púlsares reales confirmados.

## 🛠️ Metodología y Tecnologías
El flujo de trabajo implementado en el notebook incluye:
1.  **Exploración de Datos (EDA):** Visualización de distribuciones e histogramas.
2.  **Análisis de Correlación:** Identificación de las variables con mayor impacto.
3.  **Modelado:** Implementación del algoritmo **XGBoost** (Extreme Gradient Boosting).
4.  **Evaluación:** Análisis de importancia de variables (*Feature Importance*).

### Variables del Modelo
El modelo analiza 8 variables estadísticas derivadas de dos fuentes:
* **Perfil del Pulso (IP Profile):** Media, desviación estándar, exceso de curtosis y asimetría (skewness).
* **Curva DM-SNR:** Media, desviación estándar, exceso de curtosis y asimetría de la medida de dispersión.

## 📈 Resultados y Conclusiones
Tras el entrenamiento con **XGBoost**, se obtuvieron las siguientes observaciones:
* **Predominancia del Perfil:** Las variables asociadas al *Perfil del Pulso* (especialmente la curtosis y la media) demostraron tener un peso predictivo significativamente mayor que las variables de la curva DM-SNR.
* **Efectividad:** El modelo logra separar con alta precisión las señales reales del ruido, facilitando la labor de identificación astronómica.

