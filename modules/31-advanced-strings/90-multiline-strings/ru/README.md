
Представьте, что нам нужно определить строку, которая состоит из нескольких строчек — то есть внутри есть переводы строки `\n`. Например, она будет выглядеть так:

```python
text = 'Пример текста,\nсостоящего из\nнескольких строк'
```

На печати строка примет совсем другой вид:

```bash
Пример текста,
состоящего из
нескольких строк
```

Для таких ситуаций в Python есть еще один способ создания строк, который называется **multi-line строки**. Чтобы описать такую «многострочную строку», нужно заключить ее в тройные кавычки — `"""` или `'''`. Внутри multi-line строки можно переносить текст и не использовать перевод строки `\n`:

```python
text = '''Пример текста,
состоящего из
нескольких строк
'''
```

```bash
Пример текста,
состоящего из
нескольких строк

```

Обратите внимание, что в конце текста есть пустая строка. Она появилась в тексте потому, что мы поставили закрывающие кавычки `'''` на новой строке. Если не переносить закрывающие кавычки на новую строку, то пустая строка в тексте не появится:

```python
text = '''Пример текста,
состоящего из
нескольких строк'''
```

```bash
Пример текста,
состоящего из
нескольких строк
```

Из-за тройных кавычек multi-line строки позволяют не экранировать кавычки внутри строки:

```bash
Здесь не нужно экранировать 'одинарные' и "двойные" кавычки
```

Еще multi-line строки могут становиться f-строками для интерполяции:

```python
a = 'A'
b = 'B'

# Слева добавился f
text = f'''{a} и {b}
сидели на трубе
'''
```

```bash
А и B
сидели на трубе

```

Для компьютера неважно, какие способы соединения и переноса строк вы будете использовать. Он все равно произведет вычисления и выдаст нужный результат. Интерполяция и multi-line строки используются для удобства разработчиков, чтобы им было проще читать код.