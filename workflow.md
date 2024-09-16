<div id="top"></div>
<br />
<div align="center">
<h1 align="center">Рабочий процесс спринта</h1>  
</div>


Все рабочие процессы проходят через GitHub, где создается проект с несколькими досками задач для управления процессом. Это помогает организовать работу команды, включая разработчиков, дизайнеров и тестировщиков.

Основные колонки:
- **TODO**- общий список задач.
- **Sprint** - задачи, запланированные на текущий спринт.
- **In progress** - задачи, которые сейчас выполняются.
- **In check** - задачи на проверке.
- **Done** - завершенные задачи.
- **Blocked** - задачи, заблокированные из-за зависимостей от других задач.

Параметры задачи:
- **Team** - команда или тип задачи (UI/UX, Design, Programming, Testing).
- **Priority** - приоритет (High, Medium, Low).
- **Size** - размер задачи (XS, S, M, L, XL).
- **Estimate** - примерное время выполнения.
- **Sprint** - назначенный спринт.
- **Start date** - дата начала
- **End date** - дата окончания



<h2 align="center">Подготовка к спринту</h2>
Новые задачи добавляются в колонку TODO.
Если задача слишком большая, её нужно разбить на несколько меньших задач, каждая из которых должна быть выполнена за неделю или меньше.
Задачи для спринта переносятся в колонку Sprint, распределяя их между участниками команды.
<br>
<h4 align="center">Составление задачи</h4>

Создание задачи:

- **Title** - краткое описание, начинающееся с тега, например, `[Design]-`, `[UI/UX]-`, `[Feature]-` или `[Testing]-`. 
- **Task description** - подробное описание задачи.
- **Evaluation criteria** - измеримые результаты, по которым можно оценить выполненность задачи.

Дополнительные атрибуты:

- Примеры и ссылки на код или решения.
- Ссылки на макеты.
- Дополнительная информация, скриншоты и шаги для воспроизведения ошибки (если это баг).

<br>
<h2 align="center">Работа разработчика (Developer)</h2>

1. Начало работы:

- Проверьте назначенные вам **Pull Request** или задачи — они в приоритете.
- Выберите задачу из колонки **Sprint**.
- Убедитесь, что задача чётко описана и вам понятна.
- Переместите её в **In progress**.

2. Работа с задачей:

- Опишите план выполнения задачи в виде пунктов **General solution** и **Implementation steps**, затем подтвердите их с менеджером.
- Создайте новую ветку от текущей рабочей ветви (обычно **develop**).
- Коммитьте небольшие изменения с понятными сообщениями.
- Создайте **Pull Request (PR)**, связанный с задачей.

3. Ревью и завершение:
- При создании **PR** необходимо коротко описать проделанную работу в **Description**
- При создании **PR** карточка автоматически перемещается в **In check**
- Проведите ручную проверку кода, чтобы убедиться, что нет простых ошибок, таких как оставшиеся комментарии и console.log()
- Назначьте как минимум двух ревьюеров на ваш **PR** и уведомите их.
- Когда получите два одобрения, выполните merge ветки в **develop**.
- Удалите рабочую ветку после слияния.
- По окончании спринта делать release в ветку **master**.
<br>
<h4 align="center">Блоки и конфликтные ситуации</h4>
- Если вы столкнулись с проблемой или зависимостью, пересмотрите план задачи и обратитесь к документации или другим источникам.
- Если задача блокируется другой задачей, свяжитесь с исполнителем блокирующей задачи и отметьте её номер в описании вашей задачи. Переместите вашу задачу в Blocked.
- Если есть незаблокированные задачи, продолжайте работу над ними или запросите новые задачи у менеджера.
<br>
<h4 align="center">Правильное именование веток</h4>
<br>

  `{type}-{name}-{number}`
<br>
где **type** - тип ветви (feature, fix)
    **name** - псевдоним разработчика, работающего над ветвью 
    **number** - номер прикрепленного issue GitHub

Пример: `feature-john-34`.

Если над веткой работает несколько разработчиков, псевдоним не указывается (например, `feature-34`).
<br>

<h2 align="center">Как исправлять ошибки</h2>

- Убедитесь, что шаги воспроизведения ошибки ясны.
- Для критичных ошибок создавайте ветку **hotfix** от **master**, а затем мерджите изменения в master и develop.
- Для некритичных ошибок работайте по обычной схеме.

<h2 align="center">Проверка Pull Request (PR)</h2>

- Убедитесь, что в коде нет лишних комментариев или console.log().
- Обновите Changelog и версию в package.json.
- Придерживайтесь стандарта оформления кода (см. раздел Codestyle).
- Если внесены изменения в UI/UX, обновите документацию и скриншоты.
<h2 id="sermver" align="center">Семантическое версионирование (SemVer)</h2>
Версии состоят из трёх частей: {major}.{minor}.{patch}:

- major — изменения, несовместимые с предыдущими версиями.
- minor — добавление новой функциональности, не нарушающей совместимость.
- patch — исправления багов без изменения функционала.
Подробнее можно прочитать на semver.org.
<br>
<h2 id="changelog" align="center">Журнализация изменений проекта (Changelog)</h2>
<br>

Все заметные изменения необходимо задокументировать в этом файле

#### Changelog

##### [0.1.0] - 2024-08-15

##### Added (for new features)
  - заголовок изменения
##### Changed (for changes in existing functionality)
  - заголовок изменения
##### Fixed (for any bug fixes)
  - заголовок изменения
##### Remove 
  - заголовок изменения
##### Deprecated (for soon-to-be removed features)
  - заголовок изменения
##### Security (in case of vulnerabilities)
  - заголовок изменения

<br>
<h2 id="codestyle" align="center">Правила организации кода проекта (codestyle)</h2>
<h4 align="center">Поддержка читаемости кода</h4>
<br>

- В коде должны быть понятные имена для переменных
- Выносить дублируемые куски кода в файл helper.js, который находится в корне проекта
- Стараться создавать файлы, код которых не превышает 100 строк
- Искать возможность вынести код в отдельную библиотеку, или расширить существующую библиотеку
- Не делать слишком перегруженный код с множеством **if/else**
- После себя оставлять код чуточку чище и лучше
- Если кусок кода сложен для понимания - надо добавить комментарии в формате <a href="#jsdoc">jsdocs</a>

<h4 align="center">Форматирование кода</h4>
<br>

Для форматирования кода в проекте настроен eslint и prettier.

<h2 align="center">Деплой</h2>
Деплой выполняется через Netlify. Убедитесь, что все тесты проходят и проект готов к развертыванию.

<br>
<h4 align="center">Порядок импорта</h4>
<br>

Импорт стараемся группировать.
 - React
 - Next
 - сторонние контексты/компоненты/хуки
 - наши контексты/компоненты/хуки
 - наши константы/конфиги/хэлперы
 - картинки/иконки

 Например

```javascript
import { useState, useEffect, useRef } from 'react'

import Head from 'next/head'

import { useRouter } from 'next/router'

import Layout from '../components/Layout'

import VcanaLogo from '../public/vcana-logo.svg'
```

<br>
<h4 align="center">Порядок написания классов в Tailwind CSS</h4>
<br>

 - Макет
 - Флексбокс и Сетка
 - Интервал
 - Размеры
 - Типография
 - Фоны
 - Границы
 - Эффекты
 - Фильтры
 - Переходы и анимация

 Например

```javascript
className="custom-class group absolute flex justify-center pt-0 w-1/4 sm:w-1/3 md:w-1/2 text-xl text-slate-100 bg-orange-500 border-r-2 border-stone-800 shadow-md cursor-pointer hover:text-gray-100 hover:bg-blue-500"
```

User Story Example:
Title: As a translator, I want to be able to upload translation files in multiple formats so that I can work on projects efficiently regardless of the file type.

Acceptance Criteria:

The system should allow users to upload files in .docx, .xlsx, .pdf, and .txt formats.
The system should display a success message once the file is uploaded.
The system should notify the user if the file format is unsupported.
Files should be securely stored and accessible only to authorized users.
Explanation:
A user story is a brief, simple description of a feature from the perspective of an end user. It’s a tool in Agile development to communicate user needs to the development team. The story is usually framed as: "As a [user type], I want [an action] so that [benefit/goal]."

User Role: In the example, the user is a "translator."
Need: The translator needs to upload files in multiple formats.
Goal/Benefit: The goal is to work efficiently regardless of file type.
The acceptance criteria define the conditions that must be met for the story to be considered complete. These ensure that the development team knows exactly what to deliver.

This approach ensures focus on user needs, making it easier to prioritize tasks and deliver value to the end users.
