Данный скрипт создает canvas c анимированной кривой Безье со стрелкой.

###Принцип работы:

*Создается элемент canvas, на котором рисуется кривая Безье со стрелкой. Canvas абсолютно позиционирован относительно родителя. Выход скрипта  - объект canvas.*


###Создание кривой:

    canvas = new curveBezier(x1, y1, x2, y2, options);
        x1, y1 - координаты начальной точки кривой
        x2, y2 - координаты конечной точки кривой
        options - настройки кривой (+ их значения по умолчанию):
            width: 1,           толщина кривой, [пиксели]
            color: '#000',      цвет кривой
            speed: 800,         скорость отрисовки кривой, [мс]
            dashed: false,      обычная/пунктирная линия
            camber: '-',        '-' выгнутая кривая; '+' вогнутая кривая
            arrow: {
                length: 15,     длина "крыльев" стрелки, [пиксели]
                angle: .8       угол между "крыльями" стрелки, [рад]
            }


###Пример:
    
    var options = {
        color: 'red',
        width: 2,
        camber: '+',
        speed: 1000,
        dashed: true
    }

    canvas = new curveBezier(400, 100, 100, 400, options);

    document.body.appendChild(canvas);


В данном примере создается красная вогнутая пунктирная кривая толщиной 2 пикселя, время анимации которой 1000 мс.

[Демо](http://jsfiddle.net/D4QZA/2/)


Данный скрипт распространяется по лицензии [Creative Commons license](http://creativecommons.org/licenses/by-sa/3.0/).

Автор: Калиниченко Юрий