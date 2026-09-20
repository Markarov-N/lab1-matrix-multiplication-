# Лабораторная работа №1: Умножение матриц

## Описание
Программа на C++ для умножения двух квадратных матриц с автоматической проверкой с помощью Python/NumPy.

## Сборка и запуск

```bash
# 1. Скомпилировать C++ программу
g++ -O2 -std=c++17 main.cpp -o main

# 2. Сгенерировать тестовые матрицы 100x100
python3 generate.py 100

# 3. Запустить умножение
./main matrix_a.txt matrix_b.txt result_cpp.txt

# 4. Верифицировать результат через NumPy
python3 verify.py matrix_a.txt matrix_b.txt result_cpp.txt

# 5. Бенчмарк на разных размерах (до 500)
./main matrix_a.txt matrix_b.txt result_cpp.txt 500 > bench.csv

# 6. Построить график
python3 make_graph.py
