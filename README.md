# Детекция зданий и резервуаров на снимках ортофотопланов

Проект по детекции зданий и резервуаров на спутниковых снимках с использованием модели **Faster R-CNN**.

## Демонстрация

### Пример работы модели

<img width="1144" height="948" alt="image" src="https://github.com/user-attachments/assets/83fcce1b-d0f1-4b8a-bcbf-dc0593e6a015" />
<img width="1078" height="1015" alt="image" src="https://github.com/user-attachments/assets/5e8bd006-1c36-47b3-8ea9-838f309a9d16" />

## Возможности

- **Детекция двух классов объектов**: здания и нефтяные резервуары
- **Визуализация** результатов с bounding boxes и уверенностью

## Структура проекта

```
satellite-building-tank-detection/
│
├── notebooks/ # Jupyter ноутбуки
│ ├── resnet50-model.ipynb # Исследование датасетов и объединение, обучение модели
│ └── use-model.ipynb # Загрузка модели и тестирование

├── models/ # Папка для весов модели
│ └── best_model.pth # Скачать отдельно
│
├── data/ # Папка для датасетов (скачать отдельно)
│ ├── building_dataset/ # Датасет со зданиями
│ └── tanks_dataset/ # Датасет с резервуарами
│
├── requirements.txt # Зависимости
├── .gitignore # Игнорируемые файлы
└── README.md # Описание проекта
```

## Установка и запуск

### 1. Клонирование репозитория

```bash
git clone https://github.com/axizzy19/satellite-building-tank-detection.git
cd satellite-building-tank-detection
```

### 2. Создание виртуального окружения (Windows)

```bash
python -m venv venv_satellite
venv_satellite\Scripts\activate
```
### 3. Установка зависимостей

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

## Скачивание данных и модели

[Датасет](https://drive.google.com/drive/folders/15LuHXf_1oOW3jLe3x-td9tv5DT_xKW_-?usp=sharing) \
[Веса модели](https://drive.google.com/drive/folders/1r6S1zXm27pXhLULYleVDoE41W7VfYymj?usp=sharing) 

Источники: \
https://zenodo.org/records/18094235?preview_file=Training+Dataset.zip \
https://zenodo.org/records/18094235?preview_file=Training+Dataset.zip 


Папки необходимо добавить в структуру проекта в соответствии с описанием выше.

Если вы хотите обучить модель самостоятельно - запустите ноутбук ```resnet50-model.ipynb```. \
Если вы хотите протестировать готовую модель - запустите ноутбук ```use-model.ipynb```.



