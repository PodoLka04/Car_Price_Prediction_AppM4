# 🌐 Language / Язык

[🇬🇧 English](#english) | [🇷🇺 Русский](#russian)

---

## <a name="russian"></a>

# Car Price Prediction App

Проект выполнен в рамках курса **"Приложения и практика анализа данных"** (Майнор НИУ ВШЭ, 4 семестр).

## 📌 О проекте

**Тип проекта:** рекомендательный

**Цель:** построить модель случайного леса для предсказания рыночной стоимости автомобиля на основе его характеристик.

**Целевая аудитория:** автолюбители, продавцы и покупатели автомобилей, автоподборщики.

**Данные:** [Car Price Prediction Challenge (Kaggle)](https://www.kaggle.com/datasets/deepcontractor/car-price-prediction-challenge)

## 🔍 Что было сделано

### Предобработка данных
- Удалены строки с пропущенными значениями и символом "-"
- Преобразованы в числовой тип: Levy, Mileage, Engine.volume, Cylinders
- Исключён столбец ID
- Рассчитаны описательные статистики и матрица корреляций

### Моделирование
- **Модель:** случайный лес (Random Forest)
- **Разделение выборки:** 80% — обучение, 20% — тест
- **Перебор параметров:** тестировались модели с 100, 400 и 350 деревьями
- **Кросс-валидация:** 5 фолдов для оценки стабильности
- **Лучшая модель:** 350 деревьев (оптимальный баланс точности и времени)

### Архитектура приложения
- **Режимы:** упрощённый (для новичков) и расширенный (для опытных пользователей)
- **Ввод:** марка, модель, год выпуска + дополнительные параметры (кож. салон, топливо, пробег, объём, цилиндры, КПП)
- **Вывод:** предсказанная цена + доверительный интервал (задаётся пользователем)
- **Сохранение:** история запросов в localStorage браузера

## 🚀 Ссылка на приложение

🔗 **https://gdt53.shinyapps.io/car_price2/**

## 👥 Команда

| Участник | Роль |
|----------|------|
| Подолин Дмитрий | Создание модели и интерфейса |
| Семенова Мария | Идея, сценарии, создание модели |
| Смульская Ульяна | Идея, выбор методов, оценка моделей |
| Татаев Гурам | Интерфейс, выбор методов, оценка моделей |

## 📁 Содержимое репозитория

| Файл | Описание |
|------|----------|
| `app.Rmd` | Код Shiny-приложения |
| `model.Rda` | Сохранённая модель случайного леса (350 деревьев) |
| `report.html` | HTML-отчёт с описанием проекта |

## 🛠 Инструменты

- R
- Shiny
- randomForest
- caret
- dplyr, ggplot2, corrplot

## 📌 Авторы

Группа 7 + Подолин Дмитрий  
НИУ ВШЭ, курс "Приложения и практика анализа данных"

---

## <a name="english"></a>

# Car Price Prediction App

The project was completed as part of the **"Applications and Practice of Data Analysis"** course (HSE Minor, 4th semester).

## 📌 About the project

**Project type:** recommendation

**Goal:** build a random forest model to predict the market value of a car based on its characteristics.

**Target audience:** car enthusiasts, sellers and buyers of cars, car selection specialists.

**Data:** [Car Price Prediction Challenge (Kaggle)](https://www.kaggle.com/datasets/deepcontractor/car-price-prediction-challenge)

## 🔍 What was done

### Data preprocessing
- Removed rows with missing values and the "-" symbol
- Converted to numeric type: Levy, Mileage, Engine.volume, Cylinders
- Excluded the ID column
- Calculated descriptive statistics and correlation matrix

### Modeling
- **Model:** Random Forest
- **Data split:** 80% training, 20% test
- **Parameter tuning:** tested models with 100, 400, and 350 trees
- **Cross-validation:** 5 folds for stability assessment
- **Best model:** 350 trees (optimal balance of accuracy and time)

### Application architecture
- **Modes:** simplified (for beginners) and extended (for experienced users)
- **Input:** brand, model, year of manufacture + additional parameters (leather interior, fuel type, mileage, engine volume, cylinders, gearbox type)
- **Output:** predicted price + confidence interval (user-defined)
- **Storage:** request history in browser localStorage

## 🚀 Application link

🔗 **https://gdt53.shinyapps.io/car_price2/**

## 👥 Team

| Member | Role |
|----------|------|
| Dmitrii Podolin | Model and interface creation |
| Maria Semenova | Idea, scenarios, model creation |
| Ulyana Smulskaya | Idea, method selection, model evaluation |
| Guram Tataev | Interface, method selection, model evaluation |

## 📁 Repository contents

| File | Description |
|------|-------------|
| `app.Rmd` | Shiny application code |
| `model.Rda` | Saved Random Forest model (350 trees) |
| `report.html` | HTML report describing the project |

## 🛠 Tools

- R
- Shiny
- randomForest
- caret
- dplyr, ggplot2, corrplot

## 📌 Authors

Group 7 + Dmitrii Podolin  
HSE University, "Applications and Practice of Data Analysis" course
