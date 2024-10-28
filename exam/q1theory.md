### System Programming. Rust. I semester

1. Примітивні типи: Опишіть відмінності між типами u32 та i32 у контексті розміру в байтах і обробки цілих чисел. У яких
   випадках слід використовувати беззнаковий тип, а коли — зі знаком?
2. Примітивні типи: Як відбувається кодування чисел з плаваючою точкою у форматі float? Яке максимальне значення можна
   представити без втрати точності, і як це впливає на обчислення?
3. Примітивні типи: Як кодуються символи в типі char, і які особливості мають типи isize та usize? Опишіть, як кодуються
   від'ємні числа і де можуть бути використані ці типи.
4. Масиви: Як оголошуються та використовуються масиви в Rust? Які переваги та недоліки мають масиви в порівнянні з
   іншими структурами даних?
5. Масиви: Чи може масив містити елементи різних типів? Які обмеження накладає Rust на типи даних, що зберігаються в
   масивах?
6. Масиви: Що таке зрізи (slices), і як вони працюють у Rust? У чому переваги використання зрізів замість масивів у
   певних ситуаціях?
7. String. Char. Encodings: Скільки байтів займає символ у рядку типу String, і чому це залежить від кодування UTF-8? Як
   відрізняється ASCII від UTF-8 у цьому контексті?
8. String. Char. Encodings: Чи є можливість модифікувати рядки в Rust, і як це залежить від того, чи рядок є змінним або
   незмінним? Наведіть приклади використання mutable і immutable рядків.
9. String. Char. Encodings: Як визначити, чи можна розділити рядок у певній позиції, і чому це важливо для коректного
   оброблення символів у UTF-8?
10. Композитні типи: Яку роль відіграють кортежі (tuple) та тип Unit у Rust? Як використовуються ці типи, і які значення
    може приймати тип Unit?
11. Композитні типи: Що таке іменовані кортежі (named tuple або tuple struct) і тип Unit? Наведіть приклади їх
    застосування у структурі програм на Rust.
12. Композитні типи: Як оголошуються структури (struct) у Rust? Яку роль відіграє тип Unit у контексті структур?
13. Композитні типи: Яка основна мета типу enum у Rust? Які переваги й недоліки використання цього типу в порівнянні з
    іншими композитними типами?
14. Композитні типи: Наведіть практичні приклади використання типу enum у програмах на Rust. Як цей тип допомагає
    моделювати складні структури даних?
15. Композитні типи: Що таке перевірка повноти (exhaustiveness check) для enum у Rust, і чому це важливо? Як це
    допомагає уникнути помилок у коді?
16. Патерн матчінг: Для чого використовується патерн матчинг у Rust, і як виглядає вираз else у ньому? Чим відрізняється
    від класичних умовних операторів?
17. Патерн матчінг: Які обмеження існують для патерн матчингу у Rust? Як це впливає на можливості використання цього
    інструменту?
18. Патерн матчінг: Наведіть практичні приклади використання патерн матчингу у Rust, враховуючи перевірку повноти (
    exhaustiveness check). Як це полегшує роботу з різними варіантами даних?
19. Управління виконанням: Як працюють конструкції if, else та match у Rust? У чому полягають їхні особливості та
    переваги в порівнянні з іншими мовами програмування?
20. Управління виконанням: Що таке булева алгебра, і як реалізовані операції NOT, AND, OR, XOR, та => в Rust? Які
    завдання можна вирішувати за допомогою цих операцій?
21. Управління виконанням: Як працюють цикли loop, while, та for у Rust? Які особливості мають команди break та
    continue, і в яких випадках вони використовуються?
22. Функції та замикання: Чим відрізняються функції від замикань у Rust? Які переваги та обмеження кожного з цих
    підходів?
23. Функції та замикання: Що таке тип Unit у Rust, і як виглядає неявний та явний Unit у функціях? Які значення може
    приймати цей тип?
24. Функції та замикання: Які основні властивості замикань у Rust? Як відрізняється поведінка замикань від класичних
    функцій?
25. Impl блок: Як працюють impl блоки у Rust? Яка різниця між функціями і асоційованими функціями, і що таке self,
    &self, і Self?
26. Traits: Яка мета використання traits у Rust? Як вони допомагають у реалізації поліморфізму та абстракцій?
27. Traits: Як за допомогою traits можна створювати власний синтаксис у Rust? Наведіть приклади кастомізації поведінки
    через traits.
28. Ітератори: Що таке ітератори у Rust, і які основні методи вони мають? Чи можна використовувати ітератор більше ніж
    один раз?
29. Ітератори: Які методи ітераторів у Rust допомагають працювати з даними, такі як map, filter, flat_map, zip? Як вони
    спрощують обробку колекцій?
30. Ітератори: Які методи ітераторів дозволяють завершити ітерацію, такі як for_each, collect, all, any, count, sum? Як
    ці методи використовуються для ефективного управління даними?
31. Використання _ у мові Rust: Які ситуації потребують використання символу _ у Rust? Наведіть приклади його
    застосування для ігнорування значень або параметрів.

### detailed

- Примітивні типи:

- Який розмір типу u32 в байтах?
- Чи зберігає i32 від'ємні значення?
- Яка різниця між беззнаковими (unsigned) і знаковими (signed) типами?
  Примітивні типи:
- Який тип використовують для чисел з плаваючою точкою в Rust?
- Що таке точність числа з плаваючою точкою?
- Чи завжди можна зберегти число з плаваючою точкою без втрати точності?
  Примітивні типи:
- Скільки байтів займає символ типу char?
- Що означає isize та usize в контексті архітектури?
- Як у Rust кодуються від'ємні числа?
  Масиви:
- Як оголошується масив у Rust?
- Чи можуть масиви змінювати свій розмір після створення?
- Які елементи може містити масив одного типу?
  Масиви:
- Чи можна змішувати різні типи даних у масиві?
- Як можна зберігати різні типи даних у структурі, схожій на масив?
- Що станеться, якщо спробувати додати різні типи до одного масиву?
  Масиви:
- Що таке зріз (slice)?
- Чим відрізняється зріз від масиву?
- Чи можна змінювати довжину зрізу після створення?
  String. Char. Encodings:
- Скільки байтів займає один символ у кодуванні ASCII?
- Яка різниця між кодуваннями ASCII та UTF-8?
- Як визначити, скільки байтів займає рядок у Rust?
  String. Char. Encodings:
- Чи можна змінювати вміст рядка String у Rust?
- Чим відрізняються String та &str у Rust?
- Які методи використовуються для роботи з незмінними рядками?
  String. Char. Encodings:
- Чому важливо перевіряти позицію різання рядка в кодуванні UTF-8?
- Що станеться, якщо неправильно "розрізати" рядок у UTF-8?
- Як дізнатися, скільки байтів займає певний символ у рядку?
  Композитні типи:
- Що таке кортеж (tuple)?
- Скільки елементів може містити кортеж?
- Яке значення має тип Unit?
  Композитні типи:
- Що таке іменований кортеж (tuple struct)?
- Як створити іменований кортеж у Rust?
- Яку користь дає використання типу Unit?
  Композитні типи:
- Як створюється структура (struct) у Rust?
- Чим структура відрізняється від кортежу?
- Чи може структура містити поля з різними типами?
  Композитні типи:
- Що таке enum у Rust?
- Які можливі значення може мати enum?
- Які переваги має використання enum?
  Композитні типи:
- Наведіть приклад простого enum у Rust.
- Як оголошується enum у Rust?
- Як звертатися до конкретного варіанта enum?
  Композитні типи:
- Що таке перевірка повноти (exhaustiveness check) у Rust?
- Чому важливо перевіряти всі можливі варіанти в enum?
- Що станеться, якщо пропустити варіант при перевірці enum?
  Патерн матчінг:
- Що таке патерн матчинг у Rust?
- Який вигляд має вираз else у патерн матчінгу?
- У чому відмінність між if та match?
  Патерн матчінг:
- Чи можна використовувати патерн матчинг для всіх типів?
- Які обмеження існують для патерн матчингу у Rust?
- Чи можна використовувати match для порівняння тільки одного варіанта?
  Патерн матчінг:
- Як виглядає базовий приклад патерн матчингу?
- Що таке перевірка повноти у патерн матчінгу?
- Чому патерн матчинг краще підходить для роботи з enum?
  Управління виконанням:
- Як працює оператор if у Rust?
- У чому різниця між if та match?
- Як записати кілька умов у if-else?
  Управління виконанням:
- Що таке булева операція NOT?
- Як працює логічна операція AND?
- Що означає логічна операція OR?
  Управління виконанням:
- Як працює цикл loop у Rust?
- У чому різниця між while та for циклами?
- Як використовуються break та continue?
  Функції та замикання:
- Як визначається функція в Rust?
- Що таке замикання в Rust?
- Які обмеження мають замикання в порівнянні з функціями?
  Функції та замикання:
- Що таке тип Unit у функціях?
- Як виглядає явний Unit у функції?
- Яка різниця між неявним та явним Unit?
  Функції та замикання:
- Чи можна передавати функції як параметри у Rust?
- Які ключові особливості замикань?
- Чи можуть замикання зберігати змінні з навколишнього контексту?
  Impl блок:
- Що таке impl блок у Rust?
- Як визначити асоційовану функцію у impl блоці?
- У чому різниця між self, &self, та Self?
  Traits:
- Що таке trait у Rust?
- Як можна реалізувати trait для структури?
- Чим trait відрізняється від класу у інших мовах?
  Traits:
- Як за допомогою trait можна створити новий синтаксис?
- Що таке синтаксичне розширення (syntactic sugar) у Rust?
- Як можна використовувати trait для перевантаження операторів?
  Ітератори:
- Що таке ітератор у Rust?
- Які основні методи має ітератор?
- Чи можна використовувати ітератор більше одного разу?
  Ітератори:
- Як працює метод map для ітераторів?
- Що робить метод filter у ітераторах?
- Яка різниця між map та flat_map?
  Ітератори:
- Який метод ітератора дозволяє завершити ітерацію?
- Як працює метод collect?
- Що робить метод for_each?
  Використання _:
- Для чого використовується символ _ у Rust?
- Як _ допомагає ігнорувати значення або параметри?
- У яких випадках використовують _ замість конкретного імені змінної?