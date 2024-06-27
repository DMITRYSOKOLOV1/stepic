stepik курс - Java (Джава) для начинающих: с нуля до сертификата Oracle


Класс String в Java является одним из наиболее часто используемых классов. Он предоставляет множество методов для работы с строками. Вот обзор его конструкторов и основных методов.
Конструкторы класса String
1 Пустой конструктор:
  String str = new String(); - Создает пустую строку.
2 Конструктор с массивом символов:
char[] data = {'H', 'e', 'l', 'l', 'o'};
String str = new String(data); - Создает строку из массива символов.
3 Конструктор с массивом байтов:
byte[] ascii = {65, 66, 67, 68, 69};
String str = new String(ascii);
Конструктор с массивом символов и диапазоном:
char[] data = {'H', 'e', 'l', 'l', 'o'};
String str = new String(data, 1, 3);  // "ell" - Создает строку из части массива символов.
Конструктор с другим объектом String:
String str1 = "Hello";
String str2 = new String(str1); Создает строку, копируя значение другой строки.

Методы класса String
length(): Возвращает длину строки.
charAt(int index): Возвращает символ в указанной позиции.
substring(int beginIndex, int endIndex): Возвращает подстроку.
concat(String str): Объединяет две строки.
indexOf(String str): Возвращает индекс первого вхождения подстроки.
lastIndexOf(String str): Возвращает индекс последнего вхождения подстроки.
toUpperCase(): Преобразует строку в верхний регистр.
toLowerCase(): Преобразует строку в нижний регистр.
trim(): Удаляет начальные и конечные пробелы.
replace(char oldChar, char newChar): Заменяет все вхождения одного символа другим.
split(String regex): Разделяет строку на массив строк по заданному регулярному выражению.
equals(Object anObject): Сравнивает строку с другим объектом.
equalsIgnoreCase(String anotherString): Сравнивает строки без учета регистра.
compareTo(String anotherString): Сравнивает строки лексикографически.
isEmpty(): Проверяет, пуста ли строка.


Класс StringBuilder в Java
StringBuilder — это класс в Java, который используется для создания и манипуляции изменяемыми строками. Он отличается от String тем, что объекты String неизменяемы (immutable), а объекты StringBuilder изменяемы (mutable). Это означает, что при изменении строки с использованием StringBuilder создается один и тот же объект, что делает его более эффективным с точки зрения производительности при множественных изменениях строки.

Основные отличия между String и StringBuilder
1. Изменяемость:
String: Неизменяемый. Любое изменение строки создает новый объект.
StringBuilder: Изменяемый. Все изменения происходят в том же объекте.
2. Производительность:
String: Менее эффективен при множественных изменениях, так как каждое изменение создает новый объект.
StringBuilder: Более эффективен для множественных изменений, так как изменения происходят в том же объекте.
3.Потокобезопасность:
String: Потокобезопасен.
StringBuilder: Не потокобезопасен. Для потокобезопасности используйте StringBuffer.

Конструкторы класса StringBuilder
1.Пустой конструктор: 
StringBuilder sb = new StringBuilder(); - Создает пустой StringBuilder с начальной емкостью 16 символов.
2.Конструктор с начальной емкостью:
StringBuilder sb = new StringBuilder(50); // Создает StringBuilder с начальной емкостью 50 символов.
3.Конструктор с начальной строкой:
StringBuilder sb = new StringBuilder("Hello"); // Создает StringBuilder, содержащий начальную строку "Hello".

Методы класса StringBuilder
1. append(...): Добавляет строковое представление аргумента к этой последовательности. // sb.append(" World");
2. insert(int offset, ...): Вставляет строковое представление аргумента в эту последовательность в указанной позиции. sb.insert(5, " Java");
3. replace(int start, int end, String str): Заменяет часть строки между указанными индексами на новую строку. sb.replace(6, 11, "Builder");
4. delete(int start, int end): Удаляет символы между указанными индексами. sb.delete(5, 11);
5. deleteCharAt(int index): Удаляет символ в указанной позиции. sb.deleteCharAt(0);
6. reverse(): Переворачивает последовательность символов.
7. substring(int start, int end): Возвращает подстроку между указанными индексами.
8.toString(): Преобразует StringBuilder в строку.

Заключение
Использование StringBuilder вместо String рекомендуется в случаях, когда необходимо часто изменять строку. Это позволяет избежать создания большого количества промежуточных объектов и улучшить производительность приложения. Класс StringBuilder предоставляет широкий набор методов для удобной и эффективной работы с изменяемыми строками.

Классы StringBuilder и StringBuffer в Java имеют много общего, но также имеют ключевые различия. Вот подробный обзор их сходств и различий.
Общее между StringBuilder и StringBuffer
1. Иммутабельность:
Оба класса предоставляют изменяемые строки, в отличие от класса String.
2.Конструкторы:
Оба класса имеют схожие конструкторы, позволяющие создавать пустые объекты, объекты с начальной строкой, и объекты с указанной начальной емкостью.
3. Методы:
Оба класса предоставляют аналогичные методы для изменения строк, такие как append(), insert(), replace(), delete(), reverse(), и другие.

Различия между StringBuilder и StringBuffer
1.Потокобезопасность
StringBuffer: Потокобезопасен. Все методы синхронизированы, что делает его безопасным для использования в многопоточных средах.
StringBuilder: Не является потокобезопасным. Методы не синхронизированы, поэтому он быстрее в однопоточных средах.
2.Производительность
StringBuffer: Из-за синхронизации методов может быть медленнее, особенно в однопоточных приложениях.
StringBuilder: Быстрее, поскольку методы не синхронизированы, и это предпочтительный выбор для однопоточных приложений.
3.Использование
StringBuffer: Используется, когда требуется потокобезопасность, например, при работе с изменяемыми строками в многопоточной среде.
StringBuilder: Используется, когда потокобезопасность не требуется, и предпочтителен для однопоточных операций.

Заключение
Когда использовать StringBuffer: Если ваше приложение многопоточное и требует безопасного изменения строк, используйте StringBuffer.
Когда использовать StringBuilder: Если ваше приложение однопоточное или потокобезопасность не является проблемой, используйте StringBuilder для лучшей производительности.
Таким образом, выбор между StringBuilder и StringBuffer зависит от потребностей вашего приложения в потокобезопасности и производительности.
