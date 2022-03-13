# Баллистический симулятор (?)
Эта страница из себя представляет пока только что-то типо QnA?, ЧаВо?, __диздока__?

## Что хочется в итоге получить?
- Программку с более-менее вменяемым интерфейсом и простейшей 3D графикой, способную по введенным данным отрисовать процесс движения снаряда, построить траекторию и рассчитать какие-то базовые данные вроде времени полета, его дальности и т.п.. Насчет практической пользы проекта пока ничего не могу сказать, зависит от того, какой функционал мы сможем реализовать. С базовым функционалом (о нем позже) программа будет представлять из себя обычный баллистический калькулятор, но с графикой.
  Ведь если в прошлом семестре первое место занял обычный калькулятор, то обычный калькулятор с 3D графикой будет круче него, и мы сможем занять хоть какое-то место, верно?

## Вид программы
  Программа будет содержать в себе несколько элементов:
1. Окно иерархии объектов на сцене, под ним окно атрибутов объекта (UE4):

![hierarchy](https://github.com/Heldmaster/ballisticsim/blob/main/hierarchy.png)

2. Вьюпорт (UE4/Blender):

![viewport](https://github.com/Heldmaster/ballisticsim/blob/main/viewport.png)

3. Консоль (VS19):

![hierarchy](https://github.com/Heldmaster/ballisticsim/blob/main/console.png)

4. Таймлайн или доупшит с графиками в настраиваемых координатах (Blender):

![timeline](https://github.com/Heldmaster/ballisticsim/blob/main/timeline.png) 
  
В итоге получим некую смесь из виджетов, позаимствованных у разных программ.
  
  
  
  
  
## Средства разработки
* Варианты для GUI: PyQT и QTDesigner к нему, tkinter (хотя в таком случае даже Lazarus удобнее будет), DearPyGUI - очень, как по мне, неплохо выглядит, поддерживает мультиоконные приложения, может отображать 3D в окнах, вроде как даже имеет свой 3D движок.
* Варианты для 3D: DearPy3D, OpenGL, ModernGL, Ursina, Ogre. Или VPython для псевдо-3D. Лучше ModernGL или DearPy3D.
* Билдинг через pyinstaller или AutoPyExe, возможно сх-фриз, но у него уже беды с производительностью.

~~* Работа с cython. Хоть dearpygui и написан на C/C++, у нас не получится преобразовать весь код в Си через cython, ибо в библиотеке есть еще и примеси Pawn и питона. Однако нам достаточно просто прописать все чистые питоновские функции в cython и мы получим файлы заголовков C и решение. В таком случае, билдим в VS или cmake и мы получим программу, __гораздо__ более производительную, чем на питоне.~~



##Базовый функционал
  - [ ] Создается окно, есть некоторые вкладки
  - [ ] Возможность изменения атрибутов лаунчера (хз как еще назвать. Ствола? Спавнера проджектайлов, т.е. снарядов? Ну думаю понятно, о чем идет речь)
  - [ ] Вьюпорт
  - [ ] Отрисовка 3D среды
  - [ ] Возможность изменения координат объектов через вкладку атрибутов или с помощью гизмо
