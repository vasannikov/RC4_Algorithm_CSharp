# Кодовая реализация потокового шифрования/расшифрования текстовой строки с помощью шифра RC4

## Описание
Этот код представляет пример простой реализации шифрования и расшифрования текстовой строки с использованием потокового шифра RC4. Пользователь может выбрать режим работы (шифрование или расшифрование), ввести приватный ключ и строку, которую нужно зашифровать или расшифровать. Программа использует шифр RC4 для обработки данных и предоставляет результат в консоли.

## Структура кода
- RC4 класс реализует алгоритм шифра RC4, включая генерацию ключевого потока и преобразование данных.
- Encrypt метод принимает строку для шифрования и приватный ключ, возвращает зашифрованную строку в формате base64.
- Decrypt метод принимает зашифрованную строку и приватный ключ, возвращает расшифрованную строку.
- Program класс является точкой входа программы, где пользователь выбирает режим и вводит данные для шифрования или расшифрования.

## Шифр RC4
RC4 (Rivest Cipher 4) – это алгоритм потокового шифрования, разработанный Роном Ривестом. Он подходит для быстрого шифрования больших объемов данных.
1. Использование ключа: RC4 использует ключ переменной длины (обычно от 40 до 2048 бит). В данной реализации мы принимаем ключ в виде массива байтов.
2. Генерация ключевого потока: Для каждого байта шифротекста RC4 генерирует псевдослучайный ключевой байт.
3. Шифрование и расшифрование: Каждый байт открытого текста XOR'ится с соответствующим ключевым байтом для шифрования и расшифрования.

## Примеры использования
1. Шифрование:
    - Пользователь выбирает режим шифрования.
    - Вводит приватный ключ.
    - Вводит строку для шифрования.
    - Программа возвращает зашифрованную строку в формате base64.
    
2. Расшифрование:
    - Пользователь выбирает режим расшифрования.
    - Вводит приватный ключ.
    - Вводит зашифрованную строку.
    - Программа выводит расшифрованную строку.

## Формат обработки данных
- Ключ: Пользователь вводит ключ в виде произвольной строки, которая затем преобразуется в массив байтов для использования в шифровании.
- Строка для шифрования: Текстовая строка, которую пользователь вводит, кодируется в байты UTF-8 и шифруется с помощью RC4.
- Зашифрованная строка: Результат шифрования представлен в формате base64 для удобства отображения и передачи.
