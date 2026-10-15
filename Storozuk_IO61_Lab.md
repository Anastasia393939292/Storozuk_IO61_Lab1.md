Міністерство освіти і науки України

Національний технічний університет України

«Київський політехнічний інститут імені Ігоря Сікорського»

 Факультет інформатики та обчислювальної техніки

 Кафедра обчислювальної техніки

# Лабораторна робота №1
## З дисципліни «Структури даних і алгоритми»

 Виконав
Студент групи: ІО-61

Сторожук Анастасія Василівна

номер у списку групи: 25

Перевірив

Русінов Володимир Володимирович

**Київ 2026**

# Завдання 1 
Задано дійсне число x. Визначити значення заданої за варіантом кусково-неперервної функції y(x), якщо воно існує, або вивести на екран повідомлення про неіснування функції для заданого x.

1) Розв'язати задачу двома способами (написати дві програми):
У програмі дозволяється використовувати тільки одиничні операції порівняння (=, <>, <, <=, >, >=) і не дозволяється використовувати булеві (логічні) операції (not, and, or тощо);
2) У програмі необхідно обов'язково використати булеві (логічні) операції (not, and, or тощо); використання булевих операцій не повинно бути надлишковим.

**Умови до варіанту 25:**

         f1(x) ,  x ∈ D1
y(x) =
         f2(x) ,  x ∈ D2

 <img width="1556" height="81" alt="image" src="https://github.com/user-attachments/assets/51af0bf2-88ee-4c35-b624-d1370e956db0" />

 # Блок схеми #
 <img width="583" height="796" alt="image" src="https://github.com/user-attachments/assets/c722d11c-df0f-4882-b868-056f334e5c87" />
 
 <img width="588" height="786" alt="image" src="https://github.com/user-attachments/assets/b263f731-eda3-40cd-9ac0-25921551e354" />
 
# Програмний код програм #
 ```c
 #include <stdio.h>

int main(int argc, char *argv[]) {
    double x;
    double y;

    scanf("%lf", &x);

    if (x <= -10.0) {
        printf("function is undefined for this value\n");
    } else if (x <= -5.0) {
        y = x * x * x - 6;
        printf("%lf\n", y);
    } else if (x <= 5.0) {
        printf("function is undefined for this value\n");
    } else if (x <= 15.0) {
        y = x * x * x - 6;
        printf("%lf\n", y);
    } else if (x < 25.0) {
        printf("function is undefined for this value\n");
    } else {
        y = 2 * x * x * x - 3 * x + 2;
        printf("%lf\n", y);
    }

    return 0;
}
```

 # Другий розв'язок (task2.c) 
 
 ```c
#include <stdio.h>

int main(int argc, char *argv[]) {
    double x;
    double y;

    scanf("%lf", &x);

    if ((x > -10.0 && x <= -5.0) || (x > 5.0 && x <= 15.0)) {
        y = x * x * x - 6;
        printf("%lf\n", y);
    } else if (x >= 25.0) {
        y = 2 * x * x * x - 3 * x + 2;
        printf("%lf\n", y);
    } else {
        printf("function is undefined for this value\n");
    }

    return 0;
```


### Тести кожної програми

| № тесту | Вхідне значення (X) | Очікуваний результат (Y) | Фактичний результат | Статус |
| :---:   | :---:               | :---                     | :---                | :---:  |
| 1       | -12.0               | Функція не визначена     | Функція не визначена | Пройдено |
| 2       | -7.0                | y = (-7)³ - 6 = -349     | -349.000000         | Пройдено |
| 3       | 0.0                 | Функція не визначена     | Функція не визначена | Пройдено |
| 4       | 10.0                | y = 10³ - 6 = 994        | 994.000000          | Пройдено |

## Перший розвязок

<img width="1130" height="180" alt="image" src="https://github.com/user-attachments/assets/4bea8e50-ea6c-48a0-8713-5cb6c1e69f7c" />
<img width="1415" height="89" alt="image" src="https://github.com/user-attachments/assets/7cd0a83a-4165-4f49-9d24-08f452179cd8" />
<img width="1583" height="114" alt="image" src="https://github.com/user-attachments/assets/2823c6d3-1553-4545-ba36-61623d2d57d7" />
<img width="1571" height="191" alt="image" src="https://github.com/user-attachments/assets/ee808d4a-3f7f-4d6d-814a-756409e400d2" />

## другий розвязок

<img width="1571" height="191" alt="image" src="https://github.com/user-attachments/assets/e34f176d-74b5-42f1-9af5-8a63f783cec9" />




