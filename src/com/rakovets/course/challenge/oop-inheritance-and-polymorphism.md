# OOP (inheritance and polymorphism)


## Project: `Cat's home`
### Specification of task 1
Создать класс `Cat`.

Поля:
- `name` – кличка кота

Конструкторы:
- `Cat(name)` – принимает кличку кота

Методы:
- `mew()` – кот мяукает
- `purr()` – кот мурлычет
- `getName()` – получить кличку кота
- `setName(name)` – задать кличку кота


### Specification of task 2 
Создать классы `Siamese`, `Persian`, `Sphynx`.

Переопределить в них метод:
- `purr()` – кот мурлычет (каждый по разному)
- `mew()` – кот мяукает (каждый по разному)


### Specification of task 3 
Создать класс `Person`.

Поля:
- `happiness` количество счастья у человека (в процентах)

Конструкторы:
- `Person(happiness)` принимает количество счастья

Методы:
- `takeHappiness(happiness)` получение/возвращение счастья (зависит от того какое число: полож./отриц.)
- `getHappiness()` получить количество счастья
- `setHappiness(happiness)` задать количество счастья


### Specification of task 4
Перезагрузить в классе `Cat` методы.
- `mew(Person)` кот мяукает для `Person`, вызывает у него метод `takeHappiness(happiness)`, где `happiness` 
отрицательное число.
- `purr(Person)` кот мурлычет для `Person`, вызывает у него метод `takeHappiness(happiness)`, где `happiness` 
положительное число.


### Specification of task 5
Переопределить в классах `Siamese`, `Persian`, `Sphynx` методы:
- `mew(Person)` каждый кот по разному воздействует на счастье человека мяуканьем
- `purr(Person)` каждый кот по разному воздействует на счастье человека мяуканьем


### Specification of task 6
Создать класс `Home`.

Методы:
- `main()` в котором демонстрируется воздействие кота на счастье человека.


### Specification of task 7
Продемонстрировать ситуацию, когда дома несколько котов.


### Specification of task 8
Продемонстрировать ситуацию:
- когда у человек начнется депрессия
- когда он познает Дзэн


## Project: `Battle Ground`
### Specification of task 1
- Создать класс `Hero`, представляющий собой героя и содержащий поле `name`.
- Добавить конструктор, принимающий имя героя и геттер для имени (сеттер не нужен).
- Добавить метод `attackEnemy()`, выводящий в консоль сообщение о том, что герой атакует врага.
- Создать класс `TrainingGround`, содержащий метод `main`, где тестируется создание героя и его атака.


### Specification of task 2
- Создать классы `Warrior`, `Mag` и `Archer`, представляющие собой наследников класса `Hero`
- Переопределить в них метод `attackEnemy()` для вывода специализированного для этого класса сообщения об атаке.
- Протестировать создание героев различных классов и их атаки в классе `TrainingGround`.


### Specification of task 3
- Создать класс `Enemy`, представляющий собой врага и содержащий поле `health` (количество здоровья).
- Добавить конструктор, принимающий количество здоровья, а также сеттер и геттер.
- Добавить метод `takeDamage(int damage)`, который уменьшает количество здоровья в соответствии с полученным уроном.
- Переписать метод `attackEnemy()` класса `Hero`, добавив ему параметр типа `Enemy`.
- Метод должен вызывать у врага метод `takeDamage()` и передавать в него определённое количество урона.
- Переопределить метод в подклассах `Warrior`, `Mag` и `Archer` так, чтобы наносимый урон был разный.


### Specification of task 4
- Сделать класс `Hero` и его метод `attackEnemy()` абстрактными.


### Specification of task 5
- Создать интерфейс `Mortal`, содержащий метод `isAlive()`.
- Сделать так, чтобы класс `Enemy` реализовывал интерфейс `Mortal`. 
- Определить метод `isAlive()` в классе `Enemy`, чтобы тот возвращал `true`, если количество здоровья врага больше `0`.


### Specification of task 6
- Создать класс `BattleGround` с методом `main()`, в котором создать симуляцию героя, атакующего врага.


### Specification of task 7
- Добавить герою показатель здоровья и возможность погибнуть.
- Добавить возможность врагу атаковать героя в ответ.
- Создать несколько видов врагов (наследников класса `Enemy`) с разными способностями. Например, `Zombie` имеет шанс
воскреснуть при гибели.
- Дать героям уникальные способности.
- Продемонстрировать сражение героя с несколькими соперниками.


## Project: `Geometry`
Создать иерархию классов, описывающих геометрические фигуры на плоскости.

### Specification of task
- В иерархии должно быть не менее 10 классов/интерфейсов и хотя бы 2 уровня вложенности.
- При переопределении методов обязательно использовать аннотацию `@Override`
- Продемонстрировать переопределение методов в иерархии.
- Продемонстрировать добавление собственных методов в классах-наследниках (можно с помощью интерфейсов). Например,
рассчёт диагонали в прямоугольнике, рассчёт высоты в треугольнике.
- Не создавать лишних классов в системе (полностью дублирующих или не содержащих назначения)
- Каждый класс должен выполнять своё назначение.
- Создать общие методы:
    - Рассчитывающий площадь фигуры.
    - Принимающий в качестве параметра фигуру и определяющий, равны ли площади текущей и полученной фигуры.
- Создать класс `ShapeUtils` со статическими методами:
    - Определяющим, является ли фигура прямоугольником.
    - Определяющим, является ли фигура треугольником.
- Для каждого неабстрактного класса переопределить метод `toString()` класса для представления информации о классах в
строковой форме.


### Recommendations
- При разработке иерархии держать в уме принцип инкапсуляции, выбирать корректные имена классов и методов,
пользоваться преимуществами полиморфизма.
- Отдавайте предпочтение интерфейсам, а не абстрактным классам.