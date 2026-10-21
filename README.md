# MadFlash — мобильный редактор 2D-анимации

Исходный проект: React + Vite + Capacitor. APK собирается в GitHub Actions; готовый APK не хранится в репозитории.

## Сборка APK через GitHub Actions

1. Распакуй архив проекта на телефоне.
2. Открой репозиторий `ammambouy-ux/madflash-apk` и загрузи в корень **содержимое папки `madflash-apk`**, а не ZIP-файл целиком.
3. Проверь, что вместе с файлами загружена папка `.github/workflows` с файлом `build-apk.yml`. Если скрытая папка не отображается в файловом менеджере, включи показ скрытых файлов.
4. Сделай Commit changes. Сборка должна запуститься автоматически. Также её можно запустить из вкладки **Actions** через workflow **Build MadFlash APK** → **Run workflow**.
5. Открой завершённый запуск workflow и скачай артефакт **MadFlash-debug-apk**. Внутри находится `app-debug.apk`.

## Локальная разработка

Требования: Node.js 20+, JDK 17, Android SDK.

```bash
npm install
npm run dev
npm run build
npx cap add android
npx cap sync android
cd android
./gradlew assembleDebug
```

Результат: `android/app/build/outputs/apk/debug/app-debug.apk`.

Примечание: debug APK подходит для установки и тестирования на Android, но не является релизной сборкой для публикации в магазине.
