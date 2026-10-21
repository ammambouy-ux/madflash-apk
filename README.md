# MadFlash — мобильный редактор 2D-анимации

APK собирается через GitHub Actions. Архив проекта должен называться `madflash-apk-cloud-build.zip`.

## Как запустить сборку с телефона

1. Сохрани ZIP-архив проекта на телефон.
2. Открой [репозиторий madflash-apk](https://github.com/ammambouy-ux/madflash-apk).
3. Нажми **Add file → Upload files**, выбери `madflash-apk-cloud-build.zip` и загрузи его **в корень репозитория**. Не распаковывай архив.
4. Нажми **Commit changes**. Workflow **Build MadFlash APK from ZIP** должен запуститься автоматически.
5. Открой вкладку **Actions**, выбери завершённый запуск и скачай артефакт **MadFlash-debug-apk**. Внутри будет `app-debug.apk`.

Если запуск не стартовал автоматически: **Actions → Build MadFlash APK from ZIP → Run workflow**.

Сборка создаёт debug APK для установки и тестирования на Android; это не релизный пакет для публикации в магазине.
