Rust Incubator
==============

> Раньше это было не так очевидно, но суть языка программирования Rust заключается в _расширении возможностей_: независимо от того, какой код вы пишете сейчас, Rust позволяет вам выходить на новый уровень, программировать с уверенностью в более широком спектре областей, чем раньше.  
_<div align="right">Предисловие к книге о Rust</div>_

Этот проект представляет собой пошаговый курс изучения [Rust] «трудным путём» — от основ языка до умения разрабатывать веб‑бэкенд.

## Предварительные требования

### Инструментарий

- [rustup] — для установки инструментария [Rust] и его обновления.
- [CLion]/[IntelliJ IDEA] + плагины [IntelliJ Rust] + [Toml][IntelliJ Toml] в качестве среды разработки (или любая другая по вашему выбору).

### Книжная полка

- [Книга о Rust] ([Rust Book]) — обучает основам [Rust] и объясняет их.
- [Rust By Example] — обучает основам [Rust] на редактируемых примерах.
- [Справочник по Rust] ([Rust Reference]) — не является официальной спецификацией, но более детализирован и всеобъемлющ, чем [Книга о Rust].
- [Cheats.rs] и [Шпаргалка по Rust в SVG] ([Rust SVG Cheatsheet]) — для быстрого поиска информации.
- [Руководство по изданиям Rust] ([Rust Edition Guide]) — чтобы ознакомиться с улучшениями в [Rust 2018] и [Rust 2021].
- Документация [стандартной библиотеки Rust] ([Rust std lib]).
- [Книга о Cargo] ([Cargo Book]) — руководство по [Cargo], инструменту сборки и менеджеру зависимостей в [Rust].
- [Книга о rustdoc] ([Rustdoc Book]) — руководство по инструменту документирования `rustdoc`.
- [Кулинарная книга Rust] ([Rust Cookbook]) — сборник простых примеров, демонстрирующих лучшие практики для решения типовых задач программирования с использованием крейтов из экосистемы [Rust].
- [Шаблоны проектирования Rust] ([Rust Design Patterns]) — открытый репозиторий шаблонов и идиом [Rust].
- [Effective Rust] — сборник рекомендаций, выведенных из реального опыта создания программного обеспечения на [Rust].
- [Рекомендации по проектированию API для Rust] ([Rust API Guidelines]) — набор рекомендаций о том, как проектировать и представлять API для [Rust].
- [FAQ по Rust] ([Rust FAQ]) — ответы на распространённые вопросы о [Rust].
- [Площадка Rust] ([Rust Playground]) — позволяет делиться и проверять исполняемые фрагменты кода [Rust] онлайн.
- [Awesome Rust] — тщательно отобранный список кода и ресурсов [Rust].
- [This Week in Rust] — подборка актуальных еженедельных обновлений по [Rust], на которые можно подписаться.
- Блог [Baby Steps] от [Николаса Матсакиса](https://github.com/nikomatsakis) — полезные шаблоны, идеи и решения по проектированию на [Rust].
- [Материалы для изучения идиоматичного Rust] ([Learning Material for Idiomatic Rust]) — подборка ресурсов, которые помогут писать эргономичный и идиоматичный код на [Rust].

## Этапы

### Перед началом

[Создайте][1] новый [репозиторий на GitHub] для себя, используя этот репозиторий [в качестве шаблона][11].

> __ПРИМЕЧАНИЕ:__ __Этот учебный курс постоянно совершенствуется и развивается.__
>
> Чтобы быть в курсе последних изменений в вашей копии репозитория, подключите историю исходного репозитория с помощью следующих команд:
> ```bash
> git remote add upstream https://github.com/instrumentisto/rust-incubator.git
> git fetch upstream main
> git merge upstream/main --allow-unrelated-histories
> ```
> Затем, когда вы захотите получить новые изменения, выполните:
> ```bash
> git fetch upstream main
> git merge upstream/main
> ```
> Кроме того, чтобы быть в курсе новых изменений, вы можете либо [подписаться на этот репозиторий на GitHub][2], либо отслеживать его через [RSS‑подписку].

### График

Каждый этап должен быть выполнен как отдельный [PR (запрос на включение, pull request)][PR] с соответствующим названием и отмечен галочкой здесь, в графике README, после завершения. Каждый этап — это [член рабочей области Cargo][13], поэтому вы можете запускать/тестировать его из корневой директории проекта (например, `cargo run -p step_1_8`). __Рекомендуется использовать [rustfmt] и [Clippy] при написании кода на [Rust].__

- [ ] [0. Ознакомление с основами Rust][Step 0] (3 дня)
- [ ] [1. Концепции][Step 1] (2 дня, после всех подэтапов)
    - [ ] [1.1. Значения по умолчанию, клонирование и копирование][Step 1.1] (1 день)
    - [ ] [1.2. Боксинг и закрепление (boxing и pinning)][Step 1.2] (1 день)
    - [ ] [1.3. Совместное владение и внутренняя изменчивость (shared ownership и interior mutability)][Step 1.3] (1 день)
    - [ ] [1.4. Клонирование при записи (clone‑on‑write)][Step 1.4] (1 день)
    - [ ] [1.5. Преобразования, приведение типов и разыменование (conversions, casting и dereferencing)][Step 1.5] (1 день)
    - [ ] [1.6. Статическая и динамическая диспетчеризация (static и dynamic dispatch)][Step 1.6] (1 день)
    - [ ] [1.7. Типы `Sized` и `?Sized`][Step 1.7] (1 день)
    - [ ] [1.8. Потокобезопасность (thread safety)][Step 1.8] (1 день)
    - [ ] [1.9. Фантомные типы (phantom types)][Step 1.9] (1 день)
- [ ] [2. Идиомы][Step 2] (2 дня, после всех подэтапов)
    - [ ] [2.1. Насыщенные типы обеспечивают корректность (rich types ensure correctness)][Step 2.1] (1 день)
    - [ ] [2.2. Обмен значениями с помощью `mem::replace`][Step 2.2] (1 день)
    - [ ] [2.3. Ограничение поведения, а не данных (bound behavior, not data)][Step 2.3] (1 день)
    - [ ] [2.4. Абстрактный тип на входе, конкретный тип на выходе (abstract type in, concrete type out)][Step 2.4] (1 день)
    - [ ] [2.5. Полнота (exhaustivity)][Step 2.5] (1 день)
    - [ ] [2.6. Сеалинг (sealing)][Step 2.6] (1 день)
- [ ] [3. Распространённая экосистема][Step 3] (2 дня, после всех подэтапов)
    - [ ] [3.1. Тестирование и моки (testing и mocking)][Step 3.1] (1 день)
    - [ ] [3.2. Декларативные и процедурные макросы (declarative и procedural macros)][Step 3.2] (1 день)
    - [ ] [3.3. Дата и время (date и time)][Step 3.3] (1 день)
    - [ ] [3.4. Регулярные выражения и пользовательские парсеры (regular expressions и custom parsers)][Step 3.4] (1 день)
    - [ ] [3.5. Коллекции и итераторы (collections и iterators)][Step 3.5] (1 день)
    - [ ] [3.6. Сериализация и десериализация (serialization и deserialization)][Step 3.6] (1 день)
    - [ ] [3.7. Случайность и криптография (randomness и cryptography)][Step 3.7] (1 день)
    - [ ] [3.8. Логирование и трассировка (logging и tracing)][Step 3.8] (1 день)
    - [ ] [3.9. Аргументы командной строки, переменные окружения и конфигурации (command‑line arguments, environment variables и configs)][Step 3.9] (1 день)
    - [ ] [3.10. Многопоточность и параллелизм (multithreading и parallelism)][Step 3.10] (1 день)
    - [ ] [3.11. Асинхронный ввод‑вывод, фьючерсы и акторы (async I/O, futures и actors)][Step 3.11] (2 дня)
- [ ] [4. Экосистема бэкенда][Step 4] (3 дня, после всех подэтапов)  
    - [ ] [4.1. Базы данных, пулы соединений и ORM][Step 4.1] (1 день)  
    - [ ] [4.2. HTTP‑серверы и клиенты][Step 4.2] (1 день)  
    - [ ] [4.3. API‑серверы, клиенты и инструменты][Step 4.3] (1 день)  

## Дополнительная практика  

- [Rustlings][rustlings] — сборник небольших упражнений, чтобы привыкнуть к чтению и написанию кода на [Rust].  
- [Rust на Exercism][Rust on Exercism] — упражнения по программированию с наставничеством.  
- [Rust Quiz][Rust Quiz] — вопросы по [Rust] средней и высокой сложности с пояснениями.
[Awesome Rust]: https://github.com/rust-unofficial/awesome-rust
[Baby Steps]: http://smallcultfollowing.com/babysteps
[Cargo]: https://github.com/rust-lang/cargo
[Cargo Book]: https://doc.rust-lang.org/cargo
[Cheats.rs]: https://cheats.rs
[CLion]: https://www.jetbrains.com/clion
[Clippy]: https://github.com/rust-lang/rust-clippy
[Effective Rust]: https://www.lurklurk.org/effective-rust
[GitHub repository]: https://help.github.com/articles/github-glossary/#repository
[IntelliJ IDEA]: https://www.jetbrains.com/idea
[IntelliJ Rust]: https://intellij-rust.github.io
[IntelliJ Toml]: https://plugins.jetbrains.com/plugin/8195-toml
[Learning Material for Idiomatic Rust]: https://corrode.dev/blog/idiomatic-rust-resources
[PR]: https://help.github.com/articles/github-glossary/#pull-request
[RSS subscription]: https://github.com/instrumentisto/rust-incubator/commits/main.atom
[Rust]: https://www.rust-lang.org
[Rust 2018]: https://doc.rust-lang.org/edition-guide/rust-2018/index.html
[Rust 2021]: https://doc.rust-lang.org/edition-guide/rust-2021/index.html
[Rust API Guidelines]: https://rust-lang.github.io/api-guidelines
[Rust Book]: https://doc.rust-lang.org/book
[Rust By Example]: https://doc.rust-lang.org/rust-by-example
[Rust Cookbook]: https://rust-lang-nursery.github.io/rust-cookbook
[Rust Design Patterns]: https://rust-unofficial.github.io/patterns
[Rust Edition Guide]: https://doc.rust-lang.org/edition-guide
[Rust FAQ]: https://prev.rust-lang.org/faq.html
[Rust on Exercism]: https://exercism.org/tracks/rust/exercises
[Rust Playground]: https://play.rust-lang.org
[Rust Quiz]: https://github.com/dtolnay/rust-quiz
[Rust Reference]: https://doc.rust-lang.org/reference
[Rust std lib]: https://doc.rust-lang.org/std
[Rust SVG Cheatsheet]: https://web.archive.org/web/20241001012119/https://www.breakdown-notes.com/make/load/rust_cs_canvas/true
[Rustdoc Book]: https://doc.rust-lang.org/rustdoc
[rustfmt]: https://github.com/rust-lang/rustfmt
[rustlings]: https://rustlings.cool
[rustup]: https://rustup.rs
[This Week in Rust]: https://this-week-in-rust.org

[1]: https://github.com/instrumentisto/rust-incubator/generate
[2]: https://github.com/instrumentisto/rust-incubator/subscription
[11]: https://help.github.com/en/articles/creating-a-repository-from-a-template
[13]: https://doc.rust-lang.org/book/ch14-03-cargo-workspaces.html
