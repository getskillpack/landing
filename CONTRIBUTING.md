# Участие в разработке `getskillpack/landing`

Публичный статический лендинг для org **[getskillpack](https://github.com/getskillpack)** и CLI **skillget**. Здесь — как править сайт локально, проверять результат и оформлять PR; подробности экосистемы — по ссылкам, без дублирования длинных гайдов.

## Где лежит сайт

- **Источник в этом репозитории:** каталог [`docs/`](docs/) (не корень репо).
- **Публикация:** [GitHub Pages](https://pages.github.com/) с ветки **`main`**, папка **`/docs`** (настройка org). **Живой URL:** https://getskillpack.github.io/landing/
- **Каноническая копия контента:** в репозитории [`getskillpack/cli`](https://github.com/getskillpack/cli) в каталоге `docs/landing/`. Когда меняется маркетинговый текст там, изменения нужно **отзеркалить** в `docs/` здесь; либо открыть PR **напрямую в этот репозиторий**, если правки касаются только зеркала/вёрстки на Pages.

## Что почитать в первую очередь

- **Обзор репозитория и таблица смежных репо:** [README.md](README.md)
- **Матрица совместимости** (CLI ↔ skillget-manager ↔ registry): [`COMPATIBILITY_MATRIX_RU.md`](https://github.com/getskillpack/cli/blob/main/docs/COMPATIBILITY_MATRIX_RU.md) (канон в репо CLI)
- **Контрибьютинг в смежных проектах:**
  - CLI: [`CONTRIBUTING.md`](https://github.com/getskillpack/cli/blob/main/CONTRIBUTING.md)
  - Registry: [`CONTRIBUTING.md`](https://github.com/getskillpack/registry/blob/main/CONTRIBUTING.md)
  - skillget-manager: [`CONTRIBUTING.md`](https://github.com/getskillpack/skillget-manager/blob/main/CONTRIBUTING.md)

## Локальный просмотр и самопроверка

Из корня репозитория поднимите статический сервер на каталоге `docs/`:

```bash
cd docs
python3 -m http.server 8080
# откройте http://127.0.0.1:8080/ в браузере
```

Любой другой статический сервер (например `npx --yes serve .` из `docs/`) подойдёт.

**Перед PR:** проверьте главную и затронутые страницы вручную (разметка, ссылки, изображения). Отдельного сборочного шага для этого репозитория нет.

## Issues и pull requests

1. **Issue** — опишите, какую страницу/блок меняете, ожидаемый результат и скрин или ссылку на канон в `cli`, если правка оттуда.
2. **PR** — нацеливайте на ветку **`main`**, одна логическая тема на PR; для заметных пользователю правок текста согласуйте с каноном в [`getskillpack/cli`](https://github.com/getskillpack/cli) (`docs/landing/`), чтобы не разъехались копии.
3. Автоматизации и агентам в org **getskillpack:** не коммитьте секреты; гигиена PAT, веток и push — [AGENT_GITHUB_REPO_WORKFLOW_RU.md](https://github.com/getskillpack/cli/blob/main/docs/AGENT_GITHUB_REPO_WORKFLOW_RU.md) в репозитории CLI.

## Безопасность

Сообщения об уязвимостях продукта и CLI — по [SECURITY.md](https://github.com/getskillpack/cli/blob/main/SECURITY.md) в репозитории CLI (в этом репозитории отдельного `SECURITY.md` может не быть).
