<h1 align=center>Test-ML-Samokat</h1>

<h2><details open="open">
  <summary>Содержание</summary>
  <ol>
    <li><a href="#задание">Задание</a></li>
    <li><a href="#структура-проекта">Структура проекта</a></li>
    <li><a href="#результаты">Результаты</a></li>
    <li><a href="#выводы">Выводы</a></li>
  </ol>
</details></h2>

## Задание
Реализовать базовый *Embedding MixUp* метод для аугментации данных для файнтюнинга [bert-base-cased](https://huggingface.co/bert-base-cased) на [датасете](https://huggingface.co/datasets/rotten_tomatoes) rotten_tomatoes

## Структура проекта
Проект включает в себя:
- веса моделей (weights);
- данные для обучения (data);
- файлы метрик из transformers (metrics);
- файл с исключениями для git (.gitignore);
- jupyter notebook с решением задачи (notebook.ipynb)
  

```
Дерево проекта:

├── data
    ├── rotten_tomatoes
    ├── aug_data.pickle
├── metrics
├── weights
    ├── models--bert-base-cased
    ├── my_model_v1
    ├── my_model_v2
├── .gitignore
├── notebook.ipynb
├── README.md
```

## Результаты
1. Данные, полученные с помощью метода MixUP для аугментации данных, доступны по [ссылке](./data/aug_data.pickle)
2. В ходе выполнения задания была обучена сначала базовая версия bert-base-cased модель. Веса модели доступны по [ссылке](https://disk.yandex.ru/d/LIbBvD_GPTJMLg) - my_model_v1
3. С помощью MixUP метода аугментации модель была дообучена на новых наборах данных. Веса модели доступны по [ссылке](https://disk.yandex.ru/d/Wov9fWzNYsJ5Xg) - my_model_v2
4. Ноутбук с полным решением доступен по [ссылке](./notebook.ipynb)

## Выводы
В итоге модель дообученная на данных, полученных с помощью базового метода MixUP имеет точность на 2% хуже, чем точность модели обученной на исходных обучающих данных:
- my_model_v1 Accuracy = 0.85;
- my_model_v2 Accuracy = 0.83