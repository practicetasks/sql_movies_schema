# sql_movies_schema


### Tables
```sql
create table genres
(
    id   serial8 primary key,
    name varchar(50) not null
);

create table movies_genres(
    genre_id int8 not null,
    movie_id int8 not null,
    foreign key (genre_id) references genres(id),
    foreign key (movie_id) references movies(id)
);

create table movies
(
    id           serial8 primary key,
    title        varchar(100) not null,
    release_year int2         not null,
    rating       float4       not null
);

create table movies_actors(
    movie_id int8 not null,
    actor_id int8 not null,
    foreign key (movie_id) references movies(id),
    foreign key (actor_id) references actors(id)
);

create table actors
(
    id         serial8 primary key,
    name       varchar(50) not null,
    lastname   varchar(50) not null,
    birth_year int2
);
```

### INSERTS
```sql
insert into genres (name) values ('Драма');
insert into genres (name) values ('Комедия');
insert into genres (name) values ('Боевик');
insert into genres (name) values ('Фантастика');
insert into genres (name) values ('Ужасы');
insert into genres (name) values ('Криминал');
insert into genres (name) values ('Анимационный');
insert into genres (name) values ('Триллер');
insert into genres (name) values ('Приключение');
insert into genres (name) values ('Фэнтези');
insert into genres (name) values ('Биография');
insert into genres (name) values ('Биография');
insert into genres (name) values ('История');
insert into genres (name) values ('Романтика');
insert into genres (name) values ('Мистика');
insert into genres (name) values ('Война');


insert into movies (title, release_year, rating) values ('Побег из Шоушенка', 1994, 9.3);
insert into movies (title, release_year, rating) values ('Крестный Отец', 1972, 9.2);
insert into movies (title, release_year, rating) values ('Тёмный Рыцарь', 2008, 9.0);
insert into movies (title, release_year, rating) values ('Крестный Отец 2', 1974, 9.0);
insert into movies (title, release_year, rating) values ('Список Шиндлера', 1993, 9.0);
insert into movies (title, release_year, rating) values ('Властелин Колец: Возвращение Короля', 2003, 9.0);
insert into movies (title, release_year, rating) values ('Криминальное Чтиво', 1994, 9.0);
insert into movies (title, release_year, rating) values ('Властелин Колец: Братство Кольца', 8.8, 2001);
insert into movies (title, release_year, rating) values ('Форрест Гамп', 1994, 8.8);
insert into movies (title, release_year, rating) values ('Бойцовский Клуб', 1999, 8.8);
insert into movies (title, release_year, rating) values ('Властелин Колец: Две Крепости', 2002, 8.8);
insert into movies (title, release_year, rating) values ('Начало', 2010, 8.8);
insert into movies (title, release_year, rating) values ('Звездные Войны V: Империя наносит ответный удар', 1980, 8.7);
insert into movies (title, release_year, rating) values ('Матрица', 1999, 8.7);
insert into movies (title, release_year, rating) values ('Человек-Паук: Паутина Вселенных', 2023, 8.8);
insert into movies (title, release_year, rating) values ('Славные Парни', 1990, 8.7);
insert into movies (title, release_year, rating) values ('Семь', 1995, 8.6);
insert into movies (title, release_year, rating) values ('Эта замечательная жизнь', 1947, 8.6);
insert into movies (title, release_year, rating) values ('Молчание ягнят', 1991, 8.6);
insert into movies (title, release_year, rating) values ('Интерстеллар', 2014, 8.6);
insert into movies (title, release_year, rating) values ('Спасти рядового Райана', 1998, 8.6);
insert into movies (title, release_year, rating) values ('Зеленая Миля', 1999, 8.6);
insert into movies (title, release_year, rating) values ('Звездные Войны IV: Новая надежда', 1977, 8.6);
insert into movies (title, release_year, rating) values ('Теминатор 2: Судный день', 1991, 8.6);
insert into movies (title, release_year, rating) values ('Назад в Будущее', 1985, 8.5);
insert into movies (title, release_year, rating) values ('Унесенные призраками', 2001, 8.6);
insert into movies (title, release_year, rating) values ('Пианист', 2002, 8.5);
insert into movies (title, release_year, rating) values ('Оппенгеймер', 2023, 8.6);
insert into movies (title, release_year, rating) values ('Психопат', 1960, 8.5);
insert into movies (title, release_year, rating) values ('Паразит', 2019, 8.5);
insert into movies (title, release_year, rating) values ('Гладиатор', 2000, 8.5);
insert into movies (title, release_year, rating) values ('Король Лев', 1994, 8.5);
insert into movies (title, release_year, rating) values ('Леон', 1994, 8.5);
insert into movies (title, release_year, rating) values ('Американская история X', 1998, 8.5);
insert into movies (title, release_year, rating) values ('Отпускники', 2006, 8.5);
insert into movies (title, release_year, rating) values ('Одержимость', 2014, 8.5);
insert into movies (title, release_year, rating) values ('Престиж', 2006, 8.5);
insert into movies (title, release_year, rating) values ('1+1', 2011, 8.5);
insert into movies (title, release_year, rating) values ('Ла-Ла Ленд', 2016, 8.0);
insert into movies (title, release_year, rating) values ('Тайна Коко', 2017, 8.4);
insert into movies (title, release_year, rating) values ('Достучаться до небес', 1997, 8.6);
insert into movies (title, release_year, rating) values ('Мстители: Финал', 2019, 8.4);
insert into movies (title, release_year, rating) values ('Заводной апельсин', 1971, 8.3);
insert into movies (title, release_year, rating) values ('Жизнь прекрасна', 1997, 8.6);
insert into movies (title, release_year, rating) values ('Иван Васильевич меняет профессию', 1973, 8.7);
insert into movies (title, release_year, rating) values ('Джокер', 2019, 8.4);
insert into movies (title, release_year, rating) values ('Титаник', 1997, 7.8);
insert into movies (title, release_year, rating) values ('Пираты Карибского моря: Проклятие Чёрной жемчужины', 2003, 8.0);
insert into movies (title, release_year, rating) values ('ВАЛЛ·И', 2008, 8.4);
insert into movies (title, release_year, rating) values ('Поймай меня, если сможешь', 2002, 8.1);
insert into movies (title, release_year, rating) values ('Скайфолл', 2012, 7.7);
insert into movies (title, release_year, rating) values ('Аватар', 2009, 7.8);
insert into movies (title, release_year, rating) values ('Храброе сердце', 1995, 8.4);
insert into movies (title, release_year, rating) values ('История игрушек', 1995, 8.3);
insert into movies (title, release_year, rating) values ('Король Говорит!', 2010, 8.0);
insert into movies (title, release_year, rating) values ('Бриллиантовая рука', 1969, 8.9);
insert into movies (title, release_year, rating) values ('Монстры на каникулах', 2012, 7.1);
insert into movies (title, release_year, rating) values ('Звёздные войны: Пробуждение Силы', 2015, 7.8);
insert into movies (title, release_year, rating) values ('Гарри Поттер и философский камень', 2001, 7.6);
insert into movies (title, release_year, rating) values ('Рататуй', 2007, 8.0);
insert into movies (title, release_year, rating) values ('История игрушек 3', 2010, 8.2);
insert into movies (title, release_year, rating) values ('Безумный Макс: Дорога ярости', 2015, 8.1);
insert into movies (title, release_year, rating) values ('Ходячий замок', 2004, 8.2);
insert into movies (title, release_year, rating) values ('Таинственная река', 1988, 8.1);
insert into movies (title, release_year, rating) values ('Время', 2011, 7.9);
insert into movies (title, release_year, rating) values ('Малавита', 2013, 6.9);
insert into movies (title, release_year, rating) values ('Люди Икс: Дни минувшего будущего', 2014, 8.0);
insert into movies (title, release_year, rating) values ('Амадей', 1984, 8.4);
insert into movies (title, release_year, rating) values ('Мстители', 2012, 8.0);
insert into movies (title, release_year, rating) values ('Зеленая книга', 2018, 8.2);
insert into movies (title, release_year, rating) values ('Прибытие', 2016, 7.9);
insert into movies (title, release_year, rating) values ('Джентльмены', 2019, 7.8);
insert into movies (title, release_year, rating) values ('Алита: Боевой ангел', 2019, 7.3);

-- 1. DRAMA
-- 2. COMEDY
-- 3. ACTION (Боевик)
-- 4. SCI-FI (Фантастика)
-- 5. HORROR (Ужасы)
-- 6. CRIME
-- 7. ANIMATED
-- 8. THRILLER
-- 9. ADVENTURE
-- 10. FANTASY
-- 11. BIOGRAPHY
-- 12. HISTORY
-- 13. ROMANCE
-- 14. MYSTERY
-- 15. WAR

insert into movies_genres (movie_id, genre_id) values (1, 1);
insert into movies_genres (movie_id, genre_id) values (2, 1);
insert into movies_genres (movie_id, genre_id) values (2, 6);
insert into movies_genres (movie_id, genre_id) values (3, 3);
insert into movies_genres (movie_id, genre_id) values (3, 6);
insert into movies_genres (movie_id, genre_id) values (3, 1);
insert into movies_genres (movie_id, genre_id) values (4, 6);
insert into movies_genres (movie_id, genre_id) values (4, 1);
insert into movies_genres (movie_id, genre_id) values (5, 11);
insert into movies_genres (movie_id, genre_id) values (5, 1);
insert into movies_genres (movie_id, genre_id) values (5, 12);
insert into movies_genres (movie_id, genre_id) values (6, 3);
insert into movies_genres (movie_id, genre_id) values (6, 9);
insert into movies_genres (movie_id, genre_id) values (6, 1);
insert into movies_genres (movie_id, genre_id) values (7, 6);
insert into movies_genres (movie_id, genre_id) values (7, 1);
insert into movies_genres (movie_id, genre_id) values (8, 3);
insert into movies_genres (movie_id, genre_id) values (8, 9);
insert into movies_genres (movie_id, genre_id) values (8, 1);
insert into movies_genres (movie_id, genre_id) values (9, 1);
insert into movies_genres (movie_id, genre_id) values (9, 13);
insert into movies_genres (movie_id, genre_id) values (10, 1);
insert into movies_genres (movie_id, genre_id) values (11, 3);
insert into movies_genres (movie_id, genre_id) values (11, 9);
insert into movies_genres (movie_id, genre_id) values (11, 1);
insert into movies_genres (movie_id, genre_id) values (12, 3);
insert into movies_genres (movie_id, genre_id) values (12, 9);
insert into movies_genres (movie_id, genre_id) values (12, 4);
insert into movies_genres (movie_id, genre_id) values (13, 3);
insert into movies_genres (movie_id, genre_id) values (13, 9);
insert into movies_genres (movie_id, genre_id) values (13, 10);
insert into movies_genres (movie_id, genre_id) values (14, 3);
insert into movies_genres (movie_id, genre_id) values (14, 4);
insert into movies_genres (movie_id, genre_id) values (15, 7);
insert into movies_genres (movie_id, genre_id) values (15, 3);
insert into movies_genres (movie_id, genre_id) values (15, 9);
insert into movies_genres (movie_id, genre_id) values (16, 11);
insert into movies_genres (movie_id, genre_id) values (16, 6);
insert into movies_genres (movie_id, genre_id) values (16, 1);
insert into movies_genres (movie_id, genre_id) values (17, 6);
insert into movies_genres (movie_id, genre_id) values (17, 1);
insert into movies_genres (movie_id, genre_id) values (17, 14);
insert into movies_genres (movie_id, genre_id) values (18, 1);
insert into movies_genres (movie_id, genre_id) values (18, 10);
insert into movies_genres (movie_id, genre_id) values (19, 6);
insert into movies_genres (movie_id, genre_id) values (19, 1);
insert into movies_genres (movie_id, genre_id) values (19, 8);
insert into movies_genres (movie_id, genre_id) values (20, 9);
insert into movies_genres (movie_id, genre_id) values (20, 1);
insert into movies_genres (movie_id, genre_id) values (20, 4);
insert into movies_genres (movie_id, genre_id) values (21, 1);
insert into movies_genres (movie_id, genre_id) values (21, 15);
insert into movies_genres (movie_id, genre_id) values (22, 6);
insert into movies_genres (movie_id, genre_id) values (22, 1);
insert into movies_genres (movie_id, genre_id) values (22, 10);
insert into movies_genres (movie_id, genre_id) values (23, 3);
insert into movies_genres (movie_id, genre_id) values (23, 9);
insert into movies_genres (movie_id, genre_id) values (23, 10);
insert into movies_genres (movie_id, genre_id) values (24, 3);
insert into movies_genres (movie_id, genre_id) values (24, 4);
insert into movies_genres (movie_id, genre_id) values (25, 9);
insert into movies_genres (movie_id, genre_id) values (25, 2);
insert into movies_genres (movie_id, genre_id) values (25, 4);
insert into movies_genres (movie_id, genre_id) values (26, 7);
insert into movies_genres (movie_id, genre_id) values (26, 9);
insert into movies_genres (movie_id, genre_id) values (27, 11);
insert into movies_genres (movie_id, genre_id) values (27, 1);
insert into movies_genres (movie_id, genre_id) values (28, 11);
insert into movies_genres (movie_id, genre_id) values (28, 1);
insert into movies_genres (movie_id, genre_id) values (28, 12);
insert into movies_genres (movie_id, genre_id) values (29, 5);
insert into movies_genres (movie_id, genre_id) values (29, 14);
insert into movies_genres (movie_id, genre_id) values (29, 8);
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();
insert into movies_genres (movie_id, genre_id) values ();

```

