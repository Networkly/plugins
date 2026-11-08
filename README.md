# Networkly

Плагин для Codex и Claude Code подключает сервер Networkly MCP. Через него можно работать с событиями, программой, регистрацией и интеграциями в пределах прав своего аккаунта.

## Установка

Репозиторий плагина на GitHub — [Networkly/plugins](https://github.com/Networkly/plugins).

### Codex

```bash
codex plugin marketplace add Networkly/plugins
codex plugin add networkly@networkly-plugins
```

В Codex Desktop выберите Networkly в каталоге плагинов и подключите аккаунт Networkly. В Codex CLI используйте `/mcp` для проверки подключения. Если клиент просит авторизоваться, следуйте ссылке входа и подтвердите доступ в Networkly.

### Claude Code

```bash
claude plugin marketplace add Networkly/plugins
claude plugin install networkly@networkly-plugins
```

Откройте новую сессию Claude Code, выполните `/mcp` и авторизуйте Networkly. Для черновика можно использовать `/networkly:create-event-draft`.

## Примеры

- «Создай черновик события по этому анонсу и добавь программу».
- «Покажи варианты регистрации для моего события и увеличь лимит очного варианта до 50».

Права для OAuth берутся из метаданных сервера. Доступ к событиям и сообществам проверяет Networkly. Набор доступных операций можно посмотреть в ресурсе `networkly://capabilities/organizer`.

[Документация Networkly MCP](https://networkly.app/docs/integrations/mcp.md)
