# Гра 15

Класична головоломка «П'ятнашки» у вигляді одного HTML-файлу без залежностей.

## Особливості

- Один файл `index.html` — без фреймворків, без залежностей
- PWA: додається на екран iPhone/Android через «Поділитись → На екран»
- Адаптивний розмір поля (`80vmin`) — працює на будь-якому екрані
- Підтримка safe-area на iPhone з Dynamic Island / notch
- Гарантована розв'язність кожної нової гри
- Мінімальне навантаження на процесор і батарею: DOM оновлюється лише для двох змінених плиток за хід

## Як запустити

Відкрити `index.html` у браузері — більше нічого не потрібно.

## Технічні рішення

- Іконка (favicon, apple-touch-icon, маніфест) генерується через Canvas — без зовнішніх файлів
- Маніфест реєструється через `data:` URI
- Позиція порожньої клітини зберігається у змінній — без `indexOf` при кожному ході
- Делегування подій: один `addEventListener` на всю сітку

--- функція isSolvable правильно враховує умову розв’язності для гри 15

# 15 Puzzle

A classic sliding puzzle implemented as a single, dependency-free HTML file.

## Features

- Single `index.html` — no frameworks, no dependencies
- PWA: installable on iPhone/Android via Share → Add to Home Screen
- Responsive board size (`80vmin`) — works on any screen
- Safe-area support for iPhone with Dynamic Island / notch
- Every new game is guaranteed to be solvable
- Minimal CPU and battery usage: only the two affected tiles are updated per move

## How to run

Open `index.html` in any browser — nothing else required.

## Technical notes

- Icon (favicon, apple-touch-icon, manifest) is generated via Canvas — no external files
- Manifest is registered via `data:` URI — no Blob, no `URL.createObjectURL`
- Empty tile position is tracked in a variable — no `indexOf` on every move
- Event delegation: single `addEventListener` on the entire grid
