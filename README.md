# Глубокое обучение, 2026

Домашние задания курса.

| | Тема | Решение |
|---|---|---|
| ДЗ-1 | Свёртки, обучение глубоких сетей, adversarial robustness | [`hw1/hw1.ipynb`](hw1/hw1.ipynb) |
| ДЗ-2 | Распознавание именованных сущностей (NER) на русском, вариант NLP | [`hw2/hw2_nlp.ipynb`](hw2/hw2_nlp.ipynb) |

## Запуск ДЗ-1

```bash
uv venv --python 3.13
uv pip install -r hw1/requirements.txt
uv run jupyter execute --inplace hw1/hw1.ipynb
```

CIFAR-10 и FashionMNIST скачиваются в `hw1/data` при первом запуске. Полный прогон на Apple M5 (MPS) занимает около 17 минут; метрики и веса моделей сохраняются в `hw1/artifacts`.

## Запуск ДЗ-2

```bash
uv venv --python 3.13
uv pip install -r hw2/requirements.txt nbclient ipykernel
cd hw2 && uv run jupyter execute --inplace hw2_nlp.ipynb
```

Ноутбук запускается из каталога `hw2` (пути к `annotations`, `artifacts`, `data`, `runs` относительные). Модели `DeepPavlov/rubert-base-cased` и `cointegrated/rubert-tiny2` и датасет `RCC-MSU/collection3` скачиваются сами в кэш Hugging Face при первом запуске; токен не нужен. Пакеты `onnx`, `onnxruntime` и `onnxscript` из `hw2/requirements.txt` нужны только для бонуса 6.4. Полный прогон с `FAST_MODE = False` и всеми бонусами на Apple M5 (MPS, 16 ГБ) занимает около 71 минуты; метрики сохраняются в `hw2/artifacts/metrics.json`, промежуточные файлы и ONNX-модели — в `hw2/data` и `hw2/runs` (не коммитятся).
