# 🏠 Flats_Regression_R

Regression analysis and modeling of apartment rental prices in **R**.  
Регрессионный анализ и моделирование стоимости аренды квартир в **R**.

---

## 📌 About / О проекте

🎓 Developed as part of a course on post-statistical methods of machine learning. 
💡 Imports apartment data, explores distributions and correlations, builds regression models (simple and multiple), checks residuals, corrects heteroskedasticity, and makes predictions.  
📦 Covers **data visualization**, **pairwise regression**, **multiple regression**, **residual analysis**, and **forecasting**.

🎓 Разработано в рамках курса по статистическим методам машинного обучения.  
💡 Импорт данных по квартирам, исследование распределений и взаимосвязей, построение регрессионных моделей (парных и множественных), проверка остатков, устранение гетероскедастичности, прогнозирование.  
📦 Включает **визуализацию данных**, **парную регрессию**, **множественную регрессию**, **анализ остатков** и **прогнозирование**.

---

## 🔧 Features / Возможности

- 📊 Data import and preprocessing / Импорт и предобработка данных
- 📈 Histograms, scatterplots, boxplots / Гистограммы, диаграммы рассеяния, диаграммы размаха
- 🔎 Correlation analysis / Анализ корреляций
- 🧮 Simple linear regression / Парная линейная регрессия
- 📉 Residual diagnostics: normality, heteroskedasticity / Диагностика остатков: нормальность, гетероскедастичность
- 🔧 Heteroskedasticity correction: scaling & log-transformation / Устранение гетероскедастичности: деление на фактор и логарифмирование
- 🏗 Multiple regression and factor selection / Множественная регрессия и отбор факторов
- 📐 Prediction for new apartment / Прогноз стоимости аренды для новой квартиры

---

## 📁 Structure / Структура

- **1 — Data Import & Cleaning / Импорт и предобработка**
  - Load `flats.csv`, rename columns to Latin, convert numeric fields
  - Check duplicates, missing values, distributions

- **2 — Visualization / Визуализация**
  - Histograms and boxplots for numerical features
  - Scatterplots and correlation matrix (`corrplot`)
  - Relationships between `Rental_Value` and predictors (`Area`, `Floor`, `Total_Floors`)

- **3 — Simple Regression / Парная регрессия**
  - Model `Rental_Value ~ Area`
  - Regression line, confidence intervals, residuals analysis
  - Test normality (Shapiro-Wilk), heteroskedasticity (BP and GQ tests)

- **4 — Heteroskedasticity Correction / Устранение гетероскедастичности**
  - Scaling: `Rental_Value / Area ~ 1 / Area`
  - Log-transformation: `log(Rental_Value) ~ log(Area)`
  - Check residuals for normality and heteroskedasticity

- **5 — Multiple Regression / Множественная регрессия**
  - Initial model: `Rental_Value ~ Type + Floor + Total_Floors + Area + Furniture`
  - Stepwise removal of insignificant predictors
  - Build final model with significant factors

- **6 — Prediction / Прогноз**
  - Predict rental price for a new apartment based on final model
  - Analyze residuals, correct heteroskedasticity if needed
  - Predict log-transformed model and back-transform

- **7 — Diagnostics / Диагностика**
  - Residual plots, histograms, Q-Q plots
  - Tests: Shapiro-Wilk, Breusch-Pagan, Goldfeld-Quandt

---

## 📦 Libraries / Библиотеки

- `ggplot2` — visualization / визуализация  
- `corrplot` — correlation matrix / корреляционная матрица  
- `lmtest` — heteroskedasticity tests / тесты на гетероскедастичность  
- `stats` — linear models, Shapiro-Wilk / линейные модели, тест Шапиро-Уилка

---

## 🔑 Key Insights / Основные выводы

- Area (`Площадь`) is the most significant factor affecting rental price.  
- Simple and multiple regression models provide reliable predictions.  
- Residual diagnostics are essential to identify and correct heteroskedasticity.  
- Log-transformation stabilizes variance and improves model quality.  

Площадь является ключевым фактором, влияющим на стоимость аренды.  
Парные и множественные модели позволяют делать точные прогнозы.  
Анализ остатков помогает выявлять и устранять гетероскедастичность.  
Логарифмирование зависимой переменной стабилизирует дисперсию и улучшает модель.
