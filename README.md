# Codex 1C Standards Plugin

Плагин для Codex, который добавляет skill `1c-development-standards` со стандартами разработки 1C:Enterprise / BSL.

Цель этого репозитория только в том, чтобы предоставить эти стандарты в виде плагина для Codex.

## Источник стандартов

Все стандарты без изменений взяты из проекта `comol/ai_rules_1c`:

```text
https://github.com/comol/ai_rules_1c/tree/main
```

Большая благодарность авторам и участникам проекта `ai_rules_1c` за проделанную работу, структурирование и публикацию стандартов. Этот репозиторий не претендует на авторство стандартов и служит только упаковкой этих материалов в формат Codex-плагина.

Плагин публикуется через GitHub-репозиторий:

- имя marketplace: `1c-standart-rules`
- имя плагина: `1c-standards-rules`
- отображаемое имя в Codex: `1C SSL Standards`

## Установка в Codex

Добавьте этот репозиторий как marketplace плагинов Codex:

```bash
codex plugin marketplace add free-archer/codex-1c-standards-plugin
```

Установите плагин из marketplace:

```bash
codex plugin add 1c-standards-rules@1c-standart-rules
```

После установки перезапустите Codex или начните новый чат, чтобы skill был загружен.

## Проверка установки

Посмотреть доступные плагины из этого marketplace:

```bash
codex plugin list --available --marketplace 1c-standart-rules
```

Также можно открыть браузер плагинов в Codex:

```text
/plugins
```

Найдите `1C SSL Standards` и установите плагин, если он еще не установлен.

## Использование

После установки просите Codex использовать стандарты 1C при работе с BSL, метаданными, формами, СКД, регистрами, правами БСП, транзакциями, расширениями, логированием или отладкой.

Примеры запросов:

```text
Проверь это изменение BSL по стандартам разработки 1C.
```

```text
Реализуй изменение формы 1C и примени только релевантные стандарты.
```

```text
Какие стандарты из плагина применимы к проектированию этого регистра?
```

Skill загружает только релевантные файлы стандартов, а не весь набор правил для каждой задачи.

## Обновление

Обновить marketplace и переустановить плагин:

```bash
codex plugin marketplace upgrade
codex plugin remove 1c-standards-rules
codex plugin add 1c-standards-rules@1c-standart-rules
```
