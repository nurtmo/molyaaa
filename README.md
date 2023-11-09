# molyaaa
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

# Создаем данные о заболеваниях
data = {'Год': [2010, 2011, 2012, 2013, 2014],
        'Грипп': [250, 300, 280, 180, 350],
        'Гепатит': [50, 80, 100, 60, 40],
        'Грибковые инфекции': [120, 150, 180, 200, 160],
        'Аллергии': [80, 100, 120, 150, 110]}

# Создаем фрейм данных
df_diseases = pd.DataFrame(data)

# Выводим общую информацию о данных
print("Информация о заболеваниях:")
print(df_diseases.info())

# Анализируем данные
print("\nОбобщенные данные:")
print(df_diseases.describe())

# Строим график для визуализации
df_diseases.set_index('Год').plot(marker='o', linestyle='-', color='b')
plt.title('Динамика заболеваний по годам')
plt.xlabel('Год')
plt.ylabel('Количество случаев')
plt.legend(title='Заболевания', bbox_to_anchor=(1.05, 1), loc='upper left')
plt.grid(True)
plt.show()
