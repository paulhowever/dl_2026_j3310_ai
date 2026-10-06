# Глубокое обучение, 2026

Домашние задания курса.

| | Тема | Решение |
|---|---|---|
| ДЗ-1 | Свёртки, обучение глубоких сетей, adversarial robustness | [`hw1/hw1.ipynb`](hw1/hw1.ipynb) |

## Запуск

```bash
uv venv --python 3.13
uv pip install -r hw1/requirements.txt
uv run jupyter execute --inplace hw1/hw1.ipynb
```

CIFAR-10 и FashionMNIST скачиваются в `hw1/data` при первом запуске. Полный прогон на Apple M5 (MPS) занимает около 17 минут; метрики и веса моделей сохраняются в `hw1/artifacts`.
