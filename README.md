# Big Mountain Studio

SwiftUI Animation Mastery
- Started
    - Каждая анимация включает в себя некоторые изменения.
    - У каждой анимации есть начало, изменение и остановка.
    - Вы определяете состояния запуска и остановки и позволяете SwiftUI обрабатывать анимацию между этими состояниями.
    - Для запуска анимации необходим некий триггер!
    - Триггером может быть:нажатие кнопки, реакция на изменение переменной (вызванное каким-либо другим действием), событие, например, появление экрана.
    - Вы можете добавить модификатор анимации к объекту, который хотите анимировать.
    - Кривые анимации определяют скорость анимации.
    - В SwiftUI есть 4 предустановленные анимации:
        - easeInOut - начинается медленно, ускоряется, замедляется при завершении
        - endeaseIn - начинается медленно, ускоряется
        - easeOut - замедляется при завершении
        - linear - одинаковая скорость на протяжении всей анимации
    - Большинство из того, что можно анимировать, - это свойства представлений, которые имеют какое-то числовое значение."

- Basic
    - Можно анимировать между двумя разными цветами
    - Как анимировать перемещение видов с помощью модификатора смещения
    - Как затухать и исчезать видам с помощью модификатора непрозрачности
    - Что анимирование размера кадра может быть не лучшим способом сделать что-то больше или меньше, потому, что это сместит все остальное в представлении
    - Как делать вещи больше и меньше с помощью модификатора scaleEffect и как этот модификатор сохраняет расположение других видов вокруг него
    - Можете анимировать радиус угла RoundedRectangle, но не значение .infinyty
    - Анимировать размер текста с помощью модификатора .font, возможно, не самая лучшая идея. Вместо этого анимируйте масштаб представления текста, но обязательно начинайте с большего размера, чтобы текст не расплывался.
    - Как анимировать обрезку круга, чтобы было видно, как он продвигается. Примечание: Вы также можете обрезать другие фигуры, такие как эллипс, квадрат и закругленные прямоугольники

- Triggers
    - Есть много способов вызвать анимацию, будь то элемент управления, событие или жест.
    - Главное, что нужно усвоить, это то, что любое событие, которое может изменить данные, может вызвать анимацию.
    - Родитель анимирует добавление и удаление дочерних представлений.
    - Вы можете вызвать анимацию, когда представление появляется или исчезает.
    - Жесты могут вызвать движение, например, вращение, увеличение или перетаскивание, но добавив анимацию, вы можете сделать движения более плавными.

Working with Data in SwiftUI
- @State
- Вы используете @ State, когда:
    - Вы хотите обновить свойство в вашем представлении (сделать его изменяемым)
    - У вас есть значения, которые нужно сохранить после обновления экрана.
    - Вы хотите обеспечить двустороннее связывание между типом значения (не классом) и представлением.
    
- Типы значений, которые можно использовать с @ State, включают (но не ограничиваются ими):
    -  String - Int - Bool - struct - array - tuple - Dictionary
    
- Значения состояний - это локальные значения, которые помогают пользовательскому интерфейсу функционировать определенным образом, например, отслеживать, как что-то меняется в пользовательском интерфейсе.
- Это может быть анимация, открытие и закрытие группы раскрытия, текущий выбор в пикере и т.д.

- Краткое описание привязки
  - Одностороннее связывание
  - Это когда данные идут только в одном направлении - от источника к месту назначения
        @ State private var selectedName = “Scott"
        …
        Text("Selected: \(selectedName)")

 - Двустороннее связывание
    - Это когда данные могут идти в двух направлениях - от источника к месту назначения и от места назначения обратно к источнику.
        @ State private var message = “Hello, World!”
        ...
        TextField("Enter name", text: $message)
        Вам понадобится $, чтобы включить отправку данных обратно в источник.
        11
