# Баллистический симулятор (?)
Эта страница из себя представляет пока только что-то типо QnA?, ЧаВо?, __диздока__?

# Что хочется в итоге получить?
- Программку с более-менее вменяемым интерфейсом и простейшей 3D графикой, способную по введенным данным отрисовать процесс движения снаряда, построить траекторию и рассчитать какие-то базовые данные вроде времени полета, его дальности и т.п.. Насчет практической пользы проекта пока ничего не могу сказать, зависит от того, какой функционал мы сможем реализовать. С базовым функционалом (о нем позже) программа будет представлять из себя обычный баллистический калькулятор, но с графикой.
  Ведь если в прошлом семестре первое место занял обычный калькулятор, то обычный калькулятор с 3D графикой будет круче него, и мы сможем занять хоть какое-то место, верно?

#Вид программы
  Программа будет содержать в себе несколько элементов 
  
  
  
  
  
  
  
  
# Средства разработки
* Варианты для GUI: PyQT и QTDesigner к нему, tkinter (хотя в таком случае даже Lazarus удобнее будет), DearPyGUI - очень, как по мне, неплохо выглядит, поддерживает мультиоконные приложения, может отображать 3D в окнах, вроде как даже имеет свой 3D движок.
* Варианты для 3D: DearPy3D, OpenGL, ModernGL, Ursina, Ogre. Или VPython для псевдо-3D. Лучше ModernGL или DearPy3D.
