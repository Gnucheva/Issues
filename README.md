Домашнее задание к занятию «Collections Framework. CRUD и тестирование систем, управляющих набором объектов»

Какие функции должны быть реализованы:
1. Добавление Issue (набор полей и типы данных для Issue определяете сами, но можете подсмотреть подсказку)
1. Отображение списка открытых и закрытых Issue (два отдельных метода)
1. Фильтрация* (3 отдельных метода):
    1. По имени автора (кто создал)
    1. По Label'у (вам нужно проанализировать механику и подобрать нужный метод самостоятельно, но можете посмотреть подсказку)
    1. По Assignee (на кого назначено)
1. Сортировка (самостоятельно проанализируйте, как выполняется сортировка)
1. Закрытие/открытие Issue по id (фактически, это и есть update)

Фильтрация - это операция возврата только тех объектов, которые удовлетворяют заданному условию. В рамках стандартной библиотеки Java для этого существует специальный интерфейс `Predicate`. Попробуйте по аналогии с `Comparator` реализовать метод `filterBy` в менеджере и передавать в него объект, удовлетворяющий интерфейсу `Predicate`.

Внутри репозитория (конечно же нужно всё разделить на manager и repository) все issue должны храниться в виде `List` (реализацию - `ArrayList` или `LinkedList` - выберите сами).

На основании раздела CRUD спроектируйте наборы тестов и протестируйте разные состояния системы (можете использовать Mockito для того, чтобы отдельно тестировать логику в менеджере).
