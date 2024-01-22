# GoIt_Group_Project

<h1 align="center">PawPrints</h1> 
<img src="https://github.com/filinmbg/PawPrints/blob/main/image/pawprints.png" width="220" height="200" />
<h2>Опис проєкту</h2>
<a>PawPrints - це REST API для обміну та управління фотографіями. Застосунок, реалізований на FastAPI, дозволяє користувачам завантажувати фотографії, коментувати їх, додавати теги та дійснювати пошук світлин за ключовим словом або тегом.</a> 

<h2>Основний функціонал</h2>

<h3>Робота с світлинами</h3>
<ul>
  <li>Користувачі можуть завантажувати світлини з описом (POST).</li>
  <li>Користувачі можуть видаляти світлини (DELETE).</li>
  <li>Користувачі можуть редагувати опис світлини (PUT).</li>
  <li>Користувачі можуть отримувати світлину за унікальним посиланням (GET).</li>
  <li>Можливість додавати до 5 тегів під світлину. Додавання тегу не обов'язкове при завантаженні світлини.</li>
  <li>Теги унікальні для всього застосунку. Тег передається на сервер по імені. Якщо такого тега не існує, то він створюється, якщо існує, то для світлини береться існуючий тег з такою назвою.</li>
  <li>Користувачі можуть виконувати базові операції над світлинами, які дозволяє сервіс Cloudinary (https://cloudinary.com/documentation/image_transformations).</li>
  <li>Користувачі можуть створювати посилання на трансформоване зображення для перегляду світлини в вигляді URL та QR-code (https://pypi.org/project/qrcode/). Операція POST, оскільки створюється окреме посилання на трансформоване зображення, яке зберігається в базі даних.</li>
  <li>Створені посилання зберігаються на сервері і через мобільний телефон можна відсканувати QR-code та побачити зображення.</li>
  <li>Адміністратори можуть робить всі CRUD операції зі світлинами користувачів.</li>
</ul>

<h3>Коментування</h3>

<ul>
  <li>Під кожною світлиною, є блок з коментарями. Користувачі можуть коментувати світлину один одного.</li>
  <li>Користувач може редагувати свій коментар, але не видаляти.</li>
  <li>Адміністратори та модератори можуть видаляти коментарі.</li>
  <li>Для коментарів обов'язково зберігати час створення та час редагування коментаря в базі даних. Для реалізації функціональності коментарів, ми можемо використовувати відношення "один до багатьох" між світлинами і коментарями в базі даних. Для тимчасового маркування коментарів, використовувати стовпці "created_at" і "updated_at" у таблиці коментарів.</li>
</ul>

<h3>Додатковий функціонал</h3>

<ul>
  <li>За унікальним юзернеймом повертатися вся інформація про користувача.</li>
  <li>Користувач може редагувати інформацію про себе, та бачити інформацію про себе.</li> 
  <li>Адміністратор може робити користувачів неактивними (банити).</li> 
  <li>Неактивні користувачі не можуть заходити в застосунок.</li>
</ul>

<h3>Пошук та фільтрація</h3>

<ul>
 <li>Користувач може здійснювати пошук світлин за ключовим словом або тегом.</li>
 <li>Модератори та адміністратори можуть виконувати пошук та фільтрацію за користувачами, які додали світлини.</li>
</ul>

<h2>Технології</h2>
<p>Фреймворк: FastAPI.</p>
<p>База даних: PostgreSQL з використанням SQLAlchemy ORM.</p>
<p>Аутентифікація: JWT токени.</p>
<p>Зберігання фотографій: Cloudinary.</p>
<p>Генерація QR-code: бібліотека qrcode.</p>
<p>Документація: Swagger. Повна документація API доступна за посиланням /docs після запуску застосунку.</p>

<p>Застосунок покритий модульними тестами.</p>
<p>Деплой застосунку виконано за допомогою Koyeb.</p>

<h2>Інструкція з встановлення та використання</h2>
<p>Клонувати репозиторій: git clone https://github.com/filinmbg/PawPrints.git</p>
<p>Зайти в папку проекту: cd pawprints</p>
<p>Встановити залежності: poetry install</p>
<p>Перейти у выртуальне середовище: poetry shell</p>
<p>Запустити застосунок: uvicorn main:app --reload</p>

<h2>Розробники</h2
<p>Team Lead: Олександр Юха</p>
<p>Scrum master: Святослав Артеменко</p>
<p>Python Developer: Олександр Куспис</p>
<p>Python Developer: Михайло Питомець</p>


