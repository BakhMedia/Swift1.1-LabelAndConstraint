# Label - Вывод и Центровка.
### Урок 1.

![Image1](https://raw.githubusercontent.com/BakhMedia/Swift1.1-LabelAndConstraint/master/images/1.png "Image1")

1. Запускаем приложение Xcode.
2. Видим 3 категории, выбираем вторую категорию: «**Create a new Xcode project**». Сейчас только она нас интересует.

![Image2](https://raw.githubusercontent.com/BakhMedia/Swift1.1-LabelAndConstraint/master/images/2.png "Image2")

3. Переходим к выбору шаблона. В самом вверху мы видим:

«iOS» «watchOS» «tvOS» «macOS» «Cross-platform»* 
Здесь я считаю ничего не нужно объяснять и так все очевидно.
Нас интересует раздел «iOS», подраздел «Application», категория «Single View App»*.

> \* Все остальные разделы и категории мы будем рассматривать по мере необходимости.

![Image3](https://raw.githubusercontent.com/BakhMedia/Swift1.1-LabelAndConstraint/master/images/3.png "Image3")

4. Далее мы попадаем в настройки так называемых опций, давайте рассмотрим:
- «**Product Name**» - сюда вписываем название проекта (Произвольно; пример: bakh1).
- «**Organization Name**» - Имя Организатора (Имя Фамилия; пример: Игорь Вошин)
- «**Oraganization  Identifier**» - Имя Компании (Произвольно; пример: compX)
- «**Language**» (Swift/Objective - C) - Выбираем Swift.

«**Team**», «**Use Core Data**», «**Include Unit Tests**», «**Include UI Tests**» - на это не обращаем внимания, делаем как показано, ознакомимся как придет время.

![Image4](https://raw.githubusercontent.com/BakhMedia/Swift1.1-LabelAndConstraint/master/images/4.png "Image4")

5. Сейчас вам предлагается выбрать директорию, куда сохранить ваш проект. Не важно куда вы сохраните, перед сохранением уберите галочку с «**Create Git repository on my Mac**» - это простыми словами многопользовательское редактирование. Когда ваши контакты могут участвовать в проектировании. Может рассмотрим эту функцию если будет интересно.

![Image5](https://raw.githubusercontent.com/BakhMedia/Swift1.1-LabelAndConstraint/master/images/5.png "Image5")

6. Вот мы и создали проект. Видим кучу настроек, вкладок и разделов, не будем отвлекать на изучения их так как эта информация сейчас не несет никакой роли. Хочу заверить, что все проще, чем кажется на первый взгляд. 
Приступаем к созданию приложения. Обращаем свое внимание на левую колонку (**Navigation**), а в ней кликаем на «**Main.storyboard**». 

«**Main.storyboard**» - это визуальный редактор. Компания Apple очень постаралась на благо разработчиков приложений и облегчила тем самым жизнь…

![Image6](https://raw.githubusercontent.com/BakhMedia/Swift1.1-LabelAndConstraint/master/images/6.gif "Image6")

7. Вот мы попали в **storyboard** этого проекта. Далее нас интересует правый нижний угол (Объекты библиотеки). Прокручиваем ниже и находим объект «**Label**», зажав его перетаскиваем в **storyboard**.

![Image7](https://raw.githubusercontent.com/BakhMedia/Swift1.1-LabelAndConstraint/master/images/7.gif "Image7")
8. Пол работы уже сделали и даже не вспотели. Давайте рассмотрим нужные сейчас настройки.
* Для начала  впишем текст: «**Приложуха от Bakh**». Нажимаем Enter.
* Color оставлю без изменений (**черный|Default**), можете поменять если есть желание.
* Font и размер укажите на свой вкус, я оставлю **System**, а вот шрифт увеличу до 26.0.
* **Dynamic Type** - оставьте без изменений, к нему еще обратимся в следующих уроках.
* Укажите центровку текста по центру.
И растяните **Label** так что бы весь текст был виден.


9. Вот что должно получиться! Что бы было все по красоте давайте научимся приему который позволит разместить по центру экрана объект. Сразу хочу сказать, что на первый взгляд это будет мудрено выглядеть, но со временем вы поймете, этот принцип так как надо :)

![Image8](https://raw.githubusercontent.com/BakhMedia/Swift1.1-LabelAndConstraint/master/images/8.png "Image8")

![Image9](https://raw.githubusercontent.com/BakhMedia/Swift1.1-LabelAndConstraint/master/images/9.png "Image9")

10. Настроим **Constraints** (констрэйты).
Это внешний отступ от объекта. Для этого нажимаем на **Label** в **storyboard**. 
И нажимаем на указанную кнопку.
- **Верхний отступ** укажем 100 единиц. 
- **Левый и правый** 0 единиц.
- **Низ** оставляем без изменений.
Поставим галочку напротив **Height**. Что бы учитывалась высота блока для отступа. И после нажимаем «**Add 4 Constraints**».

![Image10](https://raw.githubusercontent.com/BakhMedia/Swift1.1-LabelAndConstraint/master/images/10.png "Image10")

11. Результат на лицо. Осталось чуть чуть до победы. Видите какая вещь получилось тот отступ который мы указали сверху в 100 единиц виден визуально в виде отрезка. По умолчанию он отступает от верхнего края экрана, а нам нужно разместить по центру. Для этого нажимаем на этот отрезок что бы настроить его параметры.

![Image11](https://raw.githubusercontent.com/BakhMedia/Swift1.1-LabelAndConstraint/master/images/11.png "Image11")

12. Обращаем внимание на верхний правый угол.

- **First item**  - открываем выпадающий список и устанавливаем Center Y.
- **Relation** -  оставляем без изменений.
- **Second item** - открываем выпадающий список и устанавливаем Center Y.

Там где у нас пункт **Constant** мы видим параметр, установлен в 100 единиц. Объясню так, когда мы настраивали внешний верхний отступ (констрейты) указав 100 единиц. Помним, да? Этот параметр «продублировался» сюда и нам следует установить вместо 100 единиц, **0** и нажимаем Enter. Если вы сейчас не поняли этого не волнуйтесь со следующими уроками к вам придет это понимание.


![Image12](https://raw.githubusercontent.com/BakhMedia/Swift1.1-LabelAndConstraint/master/images/12.png "Image12")

13. Вот у нас и все готово. Теперь я уверен что вам не терпится посмотреть на результат этой работы!


![Image13](https://raw.githubusercontent.com/BakhMedia/Swift1.1-LabelAndConstraint/master/images/13.png "Image13")

14. В верхнем левом углу видим вот такую комбинацию. Вместо iPhone 8 Plus можете выбрать любое устройство импонирующее вам что бы на нем лицезреть результат вашей работы. И нажимаем Play.

![Image14](https://raw.githubusercontent.com/BakhMedia/Swift1.1-LabelAndConstraint/master/images/14.png "Image14")

Я запустил в эмуляторе на iPhone X, любопытные могут запустить не только на этом устройстве, но еще на iPad, закрыть приложение в эмуляторе и запустить заново. На этом все. 



**Сейчас попробуйте по памяти все повторить, желательно 2/3 раза.**
