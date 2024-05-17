---
## Front matter
lang: ru-RU
title: Система управления пакетами dpkg
author:
  - Гомазкова А.
institute:
  - Российский университет дружбы народов, Москва, Россия

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
---

# Информация

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Гомазкова Алина
  * студентка из группы НКАбд-02-23
  * Факультет физико-математических и естественных наук
  * Российский университет дружбы народов
  * [1032235008@rudn.ru](mailto:1032235008@rudn.ru)
  * <https://alinagomazkova.github.io>
  
:::
::::::::::::::

# Вводная часть

Linux — одна из наиболее широко используемых операционных систем в мире благодаря своей стабильности, безопасности и гибкости. Одним из ключевых компонентов операционной системы Linux является система управления пакетами. Существуют различные системы управления пакетами, но одной из самых популярных является система dpkg.


## Цель работы

Цель данной работы - рассмотреть команду dpkg в Linux, что она делает и как ее эффективно использовать.Также изучим несколько примеров использования команды dpkg.

# Команда dpkg в Linux 

## Что такое команда dpkg?

dpkg (Debian Package)— это система управления пакетами для дистрибутивов Linux на базе Debian. Он используется для установки, удаления и управления пакетами программного обеспечения в системе. Команда dpkg отвечает за обработку низкоуровневых деталей управления пакетами, таких как распаковка и установка пакетов, настройка пакетов и ведение базы данных установленных пакетов.
Команда dpkg обычно используется в сочетании с другими инструментами управления пакетами, такими как apt или apt-get, которые обеспечивают интерфейс более высокого уровня для системы dpkg.


## Основной синтаксис команды dpkg

Основной синтаксис команды dpkg:

![](image/1.png)

Где —
Параметры– необязательные аргументы для изменения поведения команды dpkg.

Действие– действие,которое необходимо выполнить, например установка,удаление или настройка пакета.

Имя_пакета— имя пакета,который необходимо установить, удалить или настроить.

Теперь давайте рассмотрим некоторые распространенные параметры и действия команды dpkg на примерах.

## Общие параметры команды dpkg

Вот некоторые распространенные параметры, которые вы можете использовать с командой dpkg:

    -i — установить пакет.
    -r — удалить пакет.
    -P — Очистить пакет (удалить пакет и файлы конфигурации).
    -l — список всех установленных пакетов.
    -s — показать информацию о пакете.
    -S — поиск пакета по имени файла.
    -L — список файлов, установленных пакетом.

Теперь давайте рассмотрим несколько примеров использования этих параметров с командой dpkg.

# Примеры использования команды dpkg

Давайте разберемся с несколькими вариантами использования команды dpkg в Linux

## Установка пакета

Чтобы установить пакет с помощью dpkg, используйте параметр -i, за которым следует имя пакета. Например, чтобы установить пакет «firefox.deb», вы должны использовать следующую команду:

sudo dpkg -i firefox.deb

## Удаление пакета

Чтобы удалить пакет с помощью dpkg, используйте параметр -r, за которым следует имя пакета. Например, чтобы удалить пакет «Firefox», вы должны использовать следующую команду:

sudo dpkg -r firefox

## Очистка пакета

Чтобы удалить пакет и его файлы конфигурации с помощью dpkg, используйте параметр -P, за которым следует имя пакета. Например, чтобы очистить пакет «Firefox», вы должны использовать следующую команду:

sudo dpkg -P firefox

## Список установленных пакетов

Чтобы просмотреть все установленные пакеты с помощью dpkg, используйте опцию -l. Например, чтобы вывести список всех установленных пакетов, вы должны использовать следующую команду:

dpkg -l

## Показ информации о посылке

Чтобы отобразить информацию о пакете с помощью dpkg, используйте параметр -s, за которым следует имя пакета. Например, чтобы отобразить информацию о пакете Firefox, вы должны использовать следующую команду:

dpkg -s firefox

## Поиск пакета по имени файла

Чтобы найти пакет по имени файла с помощью dpkg, используйте опцию -S, за которой следует имя файла. Например, чтобы найти пакет, содержащий файл «/usr/bin/firefox», вы можете запустить следующую команду:

dpkg -S /usr/bin/firefox

Это выведет имя и версию пакета, который предоставляет файл. Если файл не предоставлен ни одним установленным пакетом, команда не вернет никаких результатов.

## Проверка целостности упаковки

Чтобы проверить целостность пакета с помощью dpkg, используйте параметр -V, за которым следует имя пакета. Например, чтобы проверить целостность пакета «Firefox», вы можете запустить следующую команду:

sudo dpkg -V firefox

При этом файлы, установленные пакетом, сравниваются с файлами, перечисленными в контрольном файле пакета, и сообщается о любых расхождениях.

## Переконфигурирование пакета

Если вам нужно перенастроить пакет после его установки, вы можете использовать параметр --configure, за которым следует имя пакета. Например, чтобы перенастроить пакет «Firefox», вы можете запустить следующую команду:

sudo dpkg --configure firefox

При этом запустится сценарий конфигурации пакета, что позволит вам обновить его конфигурацию по мере необходимости.

## Заключение

Мы рассмотрели команду dpkg в Linux, включая ее различные параметры и примеры их использования. Команда dpkg — это мощный инструмент для управления пакетами в системе Linux, позволяющий легко устанавливать, удалять и настраивать программное обеспечение. Понимая различные параметры и команды, доступные в dpkg, мы сможем более эффективно управлять своей системой и обеспечивать актуальность и бесперебойную работу нашего программного обеспечения.