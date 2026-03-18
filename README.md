# claude-ru-gaming

Русские игровые фразы для спиннера Claude Code. Вместо стандартных сообщений при работе Claude показывает культовые реплики из игр — Warcraft, StarCraft, Dark Souls, Factorio, S.T.A.L.K.E.R., Skyrim и других.

![Demo](demo.gif)

## Установка

### Вариант 1: Однострочник (рекомендуется)

```bash
cat ~/.claude/settings.json | jq -s '.[0] * .[1]' - <(curl -s https://raw.githubusercontent.com/max-prtsr/claude-ru-gaming/master/settings.json) > /tmp/merged.json && mv /tmp/merged.json ~/.claude/settings.json
```

### Вариант 2: Вручную

1. Откройте настройки Claude Code:

```bash
# Глобальные (для всех проектов)
~/.claude/settings.json

# Или только для проекта
.claude/settings.json
```

2. Добавьте блок `spinnerVerbs`:

```json
{
  "spinnerVerbs": {
    "mode": "replace",
    "verbs": [
      "Нужно больше золота",
      "Зуг-зуг",
      "Требуются дополнительные пилоны",
      "..."
    ]
  }
}
```

Полный список фраз — в [settings.json](settings.json).

> `"mode": "replace"` — заменяет стандартные фразы. Если хотите добавить к стандартным — используйте `"mode": "append"`.

## Пример

Во время работы Claude Code показывает:

- *Нужно больше золота*
- *Требуются дополнительные пилоны*
- *Зуг-зуг*
- *Praise the Sun!*
- *Чики-брики, и в дамки*
- *Ну, здорово, бродяга*

## Игры

Warcraft II/III · StarCraft · Dark Souls · Factorio · Skyrim · Civilization · S.T.A.L.K.E.R. · Cities: Skylines · Fallout · Anno
