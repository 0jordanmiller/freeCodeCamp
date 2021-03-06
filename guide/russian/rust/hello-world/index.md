---
title: Hello World
localeTitle: Привет мир
---
## Привет, Ржавчина

Написание первой программы Rust так же просто, как и ее установка. В каталоге проекта по вашему выбору создайте новый исходный файл `main.rs` Важно отметить, что файлы Rust всегда заканчиваются расширением `.rs` а имена файлов с более чем одним словом разделяются символами подчеркивания. Например, `helloworld.rs` станет `hello_world.rs` .

После создания `main.rs` добавьте следующий код внутри:

```rust
fn main() { 
    println!("Hello, world!"); 
 } 
```

Вау! Это было легко, не так ли? Внутри нового файла `main.rs` выполняется следующее:

*   Первая строка `fn main()` обозначает _функцию_ в Rust. `main` функция особенная, это первая вещь, которую вызывают для каждой исполняемой программы Rust.
*   Вторая строка `println!("Hello, world!")` Вызывает _макрос_ Rust, передавая _строку_ как первый аргумент. Эта строка печатает строку «Привет, мир!». к терминалу. Вы можете сказать, вызываете ли вы _макрос_ или _функцию_ Rust через наблюдение `!` ,

Чтобы выполнить программу, вы должны сначала ее скомпилировать:

```bash
$ rustc main.rs 
```

Этот процесс создаст исполняемый файл в том же каталоге, который вы затем можете запустить:

```bash
$ ./main 
 Hello, world! 
```

Поздравляем! Вы только что написали свою собственную программу Rust!

## Hello Cargo

Cargo - это инструмент сборки, который поставляется вместе с Rust при его установке и может использоваться для многих вещей. Здесь мы увидим альтернативный подход к использованию груза.

Сначала перейдите в родительский каталог вашего проекта и `cargo new hello_world` . Это создаст наш каталог проекта из `hello_world` с некоторыми файлами внутри него, те , будучи `Cargo.toml` повествующего `cargo` , как построить свой проект, а также `src/main.rs` который является нашим источник Rust файла. Если вы откроете этот файл, вы увидите, что какой-то код уже создан для того, чтобы мы запускали мир привет! Итак, давайте сделаем это.

Чтобы запустить вашу программу с грузом, это так же просто, как запуск `cargo run` в каталог вашего проекта, и он должен выглядеть примерно так:

```bash
cargo run 
   Compiling hello_world v0.1.0 
    Finished dev [unoptimized + debuginfo] target(s) in 1.31s 
     Running `target/debug/hello_world` 
 Hello, world! 
```

Большая работа у вас теперь есть еще больше инструментов в вашем распоряжении!