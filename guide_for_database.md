
Как подключить базу данных

# 1 - как создать базу

## 1.1 - создание проекта

Идем в supabase

https://supabase.com 

Выбираем New project

<img width="1654" height="506" alt="image" src="https://github.com/user-attachments/assets/04cc7ca2-30d3-4737-b545-bc15cc082637" />

ставим пароль например

new_base_test_password

получаем базу

<img width="1748" height="662" alt="image" src="https://github.com/user-attachments/assets/61f24268-45d1-4334-b0ac-5c8ff985cfd0" />

## 1.2 - создание таблицы

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





# 2 - Как подключиться к базе?

## 2.1 - через dbeaver

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


## 2.2 - как присоединиться к питону (через vscode)

Активируем венв с библиотеками

source /Users/ekaterina/venvs/simple_api_env/bin/activate


Надо добавить ключи. Какие ключи и где их взять?

1 - секретный \ публичный ключ

Слева - Project settings - 

<img width="437" height="625" alt="image" src="https://github.com/user-attachments/assets/633ea188-3c3b-4d18-b118-a146b360798e" />

API keys

<img width="1613" height="791" alt="image" src="https://github.com/user-attachments/assets/dd8f1838-9c7b-44ee-96db-2384289b2edd" />

Там лежат и публичный, и секретный клююч

(берем публичный - пока этого достаточно, чтобы и писать, и читать)

где взять URL? - 

снова Connect

<img width="764" height="62" alt="image" src="https://github.com/user-attachments/assets/69f59fd7-d51c-401a-a358-5468fa7d0dce" />

Framework

<img width="917" height="275" alt="image" src="https://github.com/user-attachments/assets/e8f5ecf3-2abb-4b60-a0e1-ec0a8cd2251e" />

Env files

<img width="878" height="381" alt="image" src="https://github.com/user-attachments/assets/65ddf199-1657-40bd-8fb9-17cd569422d6" />

Мб, можно url найти в другом месте, но я пока не нашел

Кладем все это в .env:


<img width="738" height="466" alt="image" src="https://github.com/user-attachments/assets/05ba32be-2f5a-422b-890e-474ac5985130" />


Плюс делаем гитигнор, чтобы енв не утек:

<img width="198" height="96" alt="image" src="https://github.com/user-attachments/assets/aef614a7-695c-47d6-8638-a5e521f90954" />


чтобы переменные из env читались - добавляем:

<img width="862" height="496" alt="image" src="https://github.com/user-attachments/assets/74b203d9-b39a-4a4d-b2ad-ea56bfe137af" />



(Пеерчислить возможные ошибки - неверный ключ, неверное название таблицы и пр)

Добавим:

<img width="574" height="237" alt="image" src="https://github.com/user-attachments/assets/97f6fafb-6c24-4028-9e9d-14c9298c9dce" />



Теперь все долждно быть ок - но у нас нет прав 

Чтобы их создать - заходим в Policies - Create policy:



<img width="1766" height="652" alt="image" src="https://github.com/user-attachments/assets/b2aab0d8-f898-4d23-9c39-0942338f53be" />

и добавим пока для select \ insert == TRUE (для всех, без проверки - для демо версии)



<img width="601" height="709" alt="image" src="https://github.com/user-attachments/assets/03668f32-00fb-4123-ab09-0b7a3ca6d6bb" />

Она появилась в списке политик:



<img width="1457" height="428" alt="image" src="https://github.com/user-attachments/assets/e11345bf-90c5-40f3-962b-fe80b3672889" />



Итого, у нас две политики:



<img width="1389" height="485" alt="image" src="https://github.com/user-attachments/assets/1806cf8d-9e2b-419c-9ec0-23b4f2e4b733" />




Потом можем выполнять чтение и вставку из питона:

<img width="630" height="207" alt="image" src="https://github.com/user-attachments/assets/f9e68d31-b20c-4265-a2c2-2b15fd5cf8d6" />

Проверим через dbeaver - новые записи появляются


<img width="705" height="514" alt="image" src="https://github.com/user-attachments/assets/0d3de96b-3c1c-4fbc-a914-ced353c60adc" />



**

Чтобы указать эту базу при запуске через Render, указываем переменные env при создании проекта (рассмотрим позже)














