# urban_green_space_network

### Тема 
Методы оптимального планирования зеленого каркаса

Суть метода состоит в том, чтобы объединять зеленые пространства (скверы, парки, сады) зеленым коридором.
Коридором выступает УДС. 
### Предложенный метод
![image](https://user-images.githubusercontent.com/113199314/199528977-e699e223-bb5e-4978-9169-c51edf6576a8.png)
![image](https://user-images.githubusercontent.com/113199314/200620563-2d017a39-0b65-4392-97f1-aaf1a9a63b7b.png)
![image](https://user-images.githubusercontent.com/113199314/200621076-0114110d-e31b-48cf-8f4a-a4f9dbe21542.png)

### Проблема метода
С точки зрения краткости связи двух точек столкнулся с этим: зеленый коридор пролегает через граф УДС, где нельзя озеленить, сажать деревья ввиду того корни прорастаю глубоко и могут сконфликтовать с сетями инженерной инфраструктур (трубопровода, ЛЭП, канализация и т.д.).
### Вопрос относительно определение маршрута коридоров:
Нужно сделать так, чтобы коридор между двумя точками/участкой дороги в УДС образовались там, где можно озеленить улицу, т.е. имеется  физическое пространство вдоль и по ширине, есть возможность сажать кусты, деревья и т.д. 
![Диаграмма без названия drawio](https://user-images.githubusercontent.com/113199314/199532156-2e81d798-e883-4f87-a114-e6cc59b4314e.png)

## Схема данных и примитивный алогоритм 
### Cхема данных
https://docs.google.com/document/d/1l9KtydzJfLBQTftYc-mhnDh1vBlkXG9Ewv8GeY6xWVw/edit?usp=sharing
####

### Метод
![scheme](https://user-images.githubusercontent.com/113199314/208105995-97875f3a-bf40-4415-9c06-accc58871902.jpg)
### Cхема данных
#### Пользователь дает дороги и зеленые пространства
![image](https://user-images.githubusercontent.com/113199314/208108745-44e22dd7-0602-4c0c-82f1-ea4ee4bd7ee6.png)
![image](https://user-images.githubusercontent.com/113199314/208109043-c31357e4-9377-4a27-a633-5c81026ccbdb.png)

#### Что внутри происходить?
1. В соответствие указанных видов дорог, по их сетке, алгоритм с помощью Selenium будет собирать панорамы улиц с привязкой геопозиции (может координатами называть имя файлов?). 
2. Далее собранные фотография визуально будут анализированы на оценку озелененности улиц. 
3. На выходе получим 2 результата:
а) Результатом может быть озелененная улица, то есть с уже имеющейся зеленой инфраструрой. Это уже потенциальный зеленый коридор каркаса, нужно лишь доозеленить до необходимого уровня.
б) Улица лишенная зелеными насаждениями. Эти улицы рекомендуется озеленять
