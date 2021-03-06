"Акт розбіжностей" на підставі "Акта приймання-передавання" (створення, підписання, відправлення та відхилення)
####################################################################################################################################

.. role:: red

.. role:: green

.. role:: underline

.. сюда закину немного картинок для текста

.. |фільтр| image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_01.png

.. :underline:`"Чернетки" для ролі "Організатор"`

.. contents:: Зміст:
   :depth: 6

---------

При формуванні "Акта розбіжностей" ініціатором документа виступає **"Вантажоотримувач"** (в сервісі ETTN передбачені 3 основні ролі учасників документообігу: **"Вантажовідправник"**, **"Перевізник"**, **"Вантажоотримувач"**). Обмін "Актом розбіжностей" здійснюється аналогічно до обміну "ЕТТН" тільки в зворотньому порядку.

.. attention::
    "Акт розбіжностей" створюється на основі підписаного документу "Акт приймання-передавання", що має статус "В процесі". Функціонал створення "Акта розбіжностей" стає доступним лише після підписання **"Перевізником"** пов'язаного документа еТТН (створений на основі вказаного раніше "Акта приймання-передавання"). Документ "еТТН" повинен бути в статусі "Підписаний перевізником".

.. note::
    В одному документі одна і та ж компанія не може виступати в якості "Перевізника", "Вантажовідправника" та "Вантажоотримувача"!!!  

Отже, схема документообігу "Акта розбіжностей" між компаніями має наступний вигляд:

:green:`"Вантажоотримувач" -> "Перевізник" -> "Вантажовідправник"`

.. important::
    Функціонал створення актів доступний для компанії з роллю **"Вантажоотримувача"**

**1 Створення "Акта розбіжностей" на підставі "Акта приймання-передавання" ("Вантажоотримувач")**
========================================================================================================

Для того аби створити "Акт розбіжностей" потрібно перейти до каталогу **"Вхідні"** та обрати підписаний **"Вантажовідправником"** документ "Акт приймання-передавання" (зі статусом "У процесі"):

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_02.png
   :align: center

У вибраному документі "Акт приймання-передавання" потрібно натиснути на кнопку **"+Створити акт розбіжностей"**: 

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_03.png
   :align: center

При створенні документа "Акт розбіжностей" його форма частково автоматично заповнюється даними з "Акта приймання-передавання" та "еТТН": 

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_04.png
   :align: center

В створеній формі потрібно заповнити порожні поля та **"Змінити"** дані в табличній частині (їх також можливо "Додати"):

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_05.png
   :align: center

В модальному вікні "Відомостей про вантаж" можливо змінити всі дані і всі вони є обов'язковими до заповнення окрім "Додаткової інформації". Числові значення не можуть бути менші нуля.

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_06.png
   :align: center

Після того, як форма заповнена документ можливо **"Зберегти"** (документ зберігається, як чернетка):

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_07.png
   :align: center

Після збереження документу "Акт розбіжностей" відображаються посилання на "еТТН" та "Акт приймання-передавання", з'являється можливість додати супровідні метеріали через кнопку **"Додати файл"** (назва файлу повинна бути унікальною). Для того щоб видалити доданий файл необхідно натиснути на іконку корзини.

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_08.png
   :align: center

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_09.png
   :align: center

Після усіх проведених змін документ необхідно **"Зберегти"** (1) та **"Підписати"** (2).

.. _sign:

**1.1 Підписання та відправка "Акта розбіжностей" "Вантажоотримувачем"**
================================================================================================

Після ініціалізації бібліотеки підписання, система надасть можливість додати ключ для підписання. При :underline:`першому` підписанні необхідно додати файловий ключ. Для цього у модальному вікні потрібно обрати файл (2) і ввести пароль (1):

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_10.png
   :align: center

Після чого натиснути кнопку **"Додати"**:

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_11.png
   :align: center

При успішному додаванні ключа автоматично відобразиться вибрана особа, від імені якої буде здійснено підписання (кнопка **"Підписати"**):

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_12.png
   :align: center

При подальшій роботі з раніше доданим ключем/-ами потрібно вводити лише пароль для обраного ключа:

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_13.png
   :align: center

Після підписання "Акту розбіжностей" інформація щодо підписанта відображається в блоці "Підписанти", а документ можливо **"Надіслати"**:

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_14.png
   :align: center

Після відправки документа контрагенту він відображається в журналі вихідних документів. Для відправленого **"Вантажоотримувачем"** "Акта розбіжностей" присвоюється статус "У процесі", а прив'язані документи змінюють свої статуси:

* **"еТТН"** "Підписано перевізником" -> "Підписано перевізником з актом"
* **"Акт приймання-передавання"** "У процесі" -> "У процесі з актом"

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_15.png
   :align: center

Відправлений "Акт розбіжностей" має наступний вигляд:

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_16.png
   :align: center

На формі "Акта про розбіжностей" у лівій верхній частині відображаються QR-код та унікальний ідентифікатор документа.

Користувач може скористатись функціоналом для "Друку", "Завантаження" чи "Клонування"; також у разі виявлення помилки в документі є можливість відхилити відправлений "Акт розбіжностей" **до підтвердження/підписання Перевізником**. Для цього потрібно натиснути на кнопку "Відхилити".

**1.2 Відхилення "Акта розбіжностей" "Вантажоотримувачем"**
==============================================================================

Для того, щоб відхилити документ **"Вантажоотримувачу"** потрібно натиснути **"Відхилити"**. 

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_17.png
   :align: center

Після чого в модульному вікні обов'язково потрібно заповнити причину відміни документа:

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_18.png
   :align: center

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_19.png
   :align: center

На платформі відображається повідомлення та змінюється статус документа в ланцюжку ("Відхилено"). Документообіг завершено.

**2 Отримання "Акта розбіжностей" "Перевізником"**
=================================================================================================================

Відправлений з боку **"Вантажоотримувача"** "Акт розбіжностей" відображається в папці "Вхідні".

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_20.png
   :align: center

Вхідний підписаний документ можливо "Підтвердити" та "Підписати" чи "Відхилити".

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_21.png
   :align: center

**2.1 Підтвердження / Підписання "Акта розбіжностей" "Перевізником"**
===================================================================================================================

.. important::
    В залежності від внутрішньої схеми **"Перевізника"** документ перед "Підписанням" може бути "Підтверджений" водієм, (кнопка **"Підтвердити"**) і відповідно цей документ у вхідних змінить свій статус на "Підтверджений водієм або перевізником":

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_22.png
   :align: center

Окрім зміни статусу, з'являється підказка в верхній частині вікна, а також відображається запис в **"Історії змін статусів"**:

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_23.png
   :align: center

Для підписання документу потрібно натиснути на кнопку **"Підписати"**:

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_24.png
   :align: center

.. hint::
    Процес підписання не відрізняється від підписання **"Вантажоотримувачем"** та описаний в `розділі вище <https://wiki.edi-n.com/uk/latest/ETTN_2_0/Create_discrepancy_act_new.html#sign>`__ .

Після підписання документ змінює свій статус на "Підписано перевізником", а в інформації про підписантів відобразиться інформація про підписання:

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_25.png
   :align: center

Після підписання документу "Відхилити" його неможливо.

**2.2 Відхилення "Акта розбіжностей" "Перевізником"**
==============================================================================

Для того, щоб відхилити документ потрібно натиснути **"Відхилити"**. 

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_26.png
   :align: center

Після чого в модульному вікні обов'язково потрібно заповнити причину відміни документа:

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_18.png
   :align: center

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_27.png
   :align: center

На платформі з'являється підказка про зміну статусу документа в ланцюжку на "Відхилено". В **"Інформації про підписантів"** та **"Історії змін статусів"** червоним кольором також відображається помітка про відмову зі сторони **"Перевізника"**. Документообіг завершено.

**3 Отримання "Акта розбіжностей" "Вантажовідправником"**
=================================================================================================================

Відправлений та підписаний "Акт розбіжностей" у **"Вантажовідправника"** відображається в папці "Надіслані".

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_28.png
   :align: center

Вхідний підписаний документ можливо "Підтвердити" та "Підписати" чи "Відхилити".

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_29.png
   :align: center

**3.1 Підтвердження / Підписання "Акта розбіжностей" "Вантажовідправником"**
===================================================================================================================

.. important::
    В залежності від внутрішньої схеми **"Вантажовідправника"** документ перед "Підписанням" може бути "Підтверджений" вантажовідправником, (кнопка **"Підтвердити"**) і відповідно цей документ у вхідних змінить свій статус на "Підтверджено вантажовідправником":

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_30.png
   :align: center

Окрім зміни статусу, з'являється підказка в верхній частині вікна, а також відображається запис в **"Історії змін статусів"**:

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_31.png
   :align: center

Для підписання документу потрібно натиснути на кнопку **"Підписати"**:

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_32.png
   :align: center

.. hint::
    Процес підписання не відрізняється від описаного раніше в `розділі вище <https://wiki.edi-n.com/uk/latest/ETTN_2_0/Create_discrepancy_act_new.html#sign>`__ .

Після підписання документ змінить свій статус на "Підписано вантажовідправником", а в інформації про підписантів відобразиться інформація про підписання:

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_33.png
   :align: center

Відображається інформативна підказка про те, що документообіг завершено. При перегляді документу/-ів, на основі яких було створено "Акт розбіжностей" відображається посилання про прив'язаний акт.

**3.2 Відхилення "Акта розбіжностей" "Перевізником"**
=======================================================================================

Для того, щоб відхилити документ потрібно натиснути **"Відхилити"**.

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_34.png
   :align: center

Після чого в модульному вікні обов'язково потрібно заповнити причину відміни документа:

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_18.png
   :align: center

.. image:: pics_Create_discrepancy_act_new/Create_discrepancy_act_new_35.png
   :align: center

На платформі з'являється підказка про зміну статусу документа в ланцюжку на "Відхилено". В **"Інформації про підписантів"** та **"Історії змін статусів"** червоним кольором також відображається помітка про відмову зі сторони **"Вантажовідправника"**. Документообіг завершено.

.. include:: kontakti.rst
