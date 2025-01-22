# Regions Updater

Этот проект предназначен для обогащения данных о регионах с помощью сервиса DaData и загрузки этих данных в Elasticsearch.

## Установка

1. Клонируйте репозиторий:
    ```sh
    git clone https://github.com/tsepelev/regions_updater.git
    ```
2. Установите зависимости:
    ```sh
    poetry install
    ```
3. Создайте файл `.env` и добавьте в него следующие переменные:
    ```env
    DADATA_API_KEY=<Ваш API-ключ DaData>
    ELASTICSEARCH_HOST=<Хост Elasticsearch>
    ELASTIC_USERNAME=<Имя пользователя Elasticsearch>
    ELASTIC_PASSWORD=<Пароль Elasticsearch>
    ```

## Использование

1. Обогатите данные о регионах с помощью DaData и сохраните их в формате JSONL:
    ```sh
    python main.py
    ```
2. Загрузите данные в Elasticsearch из файла JSONL:
    ```sh
    python main.py
    ```

## Структура проекта

- `main.py`: основной файл проекта, содержащий функции для обогащения данных, сохранения их в формате JSONL и загрузки в Elasticsearch.
- `pyproject.toml`: файл с зависимостями проекта.

## Функции

- `enrich_regions(regions)`: обогащает данные о регионах с помощью сервиса DaData.
- `save_to_jsonl(data)`: сохраняет обогащенные данные в формате JSONL.
- `save_to_elasticsearch_from_file()`: загружает данные в Elasticsearch из файла JSONL.

## Лицензия

Этот проект лицензирован под лицензией MIT. Подробности см. в файле LICENSE.