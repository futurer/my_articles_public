
Как подключить базу данных

1 - как ее содзать

Идем в supabase

Выбираем New project

<img width="1654" height="506" alt="image" src="https://github.com/user-attachments/assets/04cc7ca2-30d3-4737-b545-bc15cc082637" />


ставим пароль например

new_base_test_password

получаем базу

<img width="1748" height="662" alt="image" src="https://github.com/user-attachments/assets/61f24268-45d1-4334-b0ac-5c8ff985cfd0" />


Как содзать таблицу?

заходим в Table editor == Vreate table



<img width="1230" height="645" alt="image" src="https://github.com/user-attachments/assets/60420bed-2aa5-4e9e-9ade-71b83c4161ed" />



и указываем:

вверху - название

<img width="772" height="238" alt="image" src="https://github.com/user-attachments/assets/5015b46a-b23b-4714-9ac7-f83f7ccaa1c1" />

внизу - данные


<img width="885" height="735" alt="image" src="https://github.com/user-attachments/assets/de2af10f-76a4-47ed-811d-fac64bb436ca" />


нажимаем Save

вставим демо данные:
для теста - нажимаем Insert - и вводим пару лююых чисел

<img width="1588" height="647" alt="image" src="https://github.com/user-attachments/assets/7b81dbc2-4cb9-4239-a9ca-7707677b537f" />







## 2 == как к ней подключиться?

1 - через dbeaver

(пока просто посмотреть)

идем в dbeaver

New connection - PostgreSQL - 

<img width="690" height="587" alt="image" src="https://github.com/user-attachments/assets/58e6c70f-5828-460b-9126-978425dec1d2" />

и вводим сюда данные - отсюда:

вверху - Connect

<img width="770" height="153" alt="image" src="https://github.com/user-attachments/assets/75d631c9-cf7a-45a4-861f-e7e418aeb2e1" />

берем Direct == Session pooler

<img width="953" height="665" alt="image" src="https://github.com/user-attachments/assets/c591f946-9a55-4cf0-80ec-b05ef6247b77" />


Переносим эти данные в dbeaver


<img width="917" height="687" alt="image" src="https://github.com/user-attachments/assets/94e5da9c-c3e1-402e-8651-69305ff735ad" />




Получаем:

<img width="1252" height="658" alt="image" src="https://github.com/user-attachments/assets/4873fb38-97ed-4f4c-8af7-6916a363e4d6" />

Итого - ок:

Заходим в наш коннект - Schemas - Pub;ic - Database


<img width="397" height="490" alt="image" src="https://github.com/user-attachments/assets/c657a5c2-5dc9-4938-9ab7-fded94e31e66" />

Видим нашу базу (посмотрим на Data - все ок)

<img width="1154" height="528" alt="image" src="https://github.com/user-attachments/assets/98657c39-923f-4db6-9ffa-f284648f3461" />




Проверим - напишем простой sql запрос:



<img width="831" height="513" alt="image" src="https://github.com/user-attachments/assets/6401079c-90a1-49a8-a9c1-2685186f7d1a" />

== Все работает.


## 2 - как присоединиться к питону (через vscode)

Активируем венв с библиотеками

source /Users/ekaterina/venvs/simple_api_env/bin/activate














