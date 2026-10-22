# Безопасность / Security

## Как сообщить об уязвимости

Не создавайте для этого публичный issue. Откройте закрытое сообщение: [**Сообщить об уязвимости**](https://github.com/whoami-ru/EasyGRC-Free-Releases/security/advisories/new). Его видим только мы.

Заполните два поля, остальные можно оставить пустыми:

- **Title:** одна строка, что за уязвимость.
- **Description:** скопируйте и допишите три строки.

```
Где: (страница или адрес, например /settings/users/)
В чём: (что именно не так, например «можно прочитать чужой файл»)
Какая: (тип, например XSS, обход прав, SQL-инъекция; версия из файла VERSION)
```

Ответим, как только сможем, и сообщим, когда выйдет исправление.

## Что важно знать

- Free не обновляется сам. Исправления выходят в новых версиях на странице [Releases](../../releases). Подпишитесь на них: **Watch → Custom → Releases**.
- Перед установкой проверяйте контрольную сумму архива: `sha256sum -c easygrc-<версия>-free.tar.gz.sha256`. Берите архивы только из этого репозитория.
- Не публикуйте в issue файл `.env`, пароли, ключи и содержимое `deploy/tls/`. Если случайно опубликовали, считайте их скомпрометированными и замените.

---

## How to report a vulnerability

Please do not open a public issue. Use a private report instead: [**Report a vulnerability**](https://github.com/whoami-ru/EasyGRC-Free-Releases/security/advisories/new). Only we can see it.

Fill in two fields, the rest can stay empty:

- **Title:** one line, what the vulnerability is.
- **Description:** copy and complete three lines.

```
Where: (page or address, for example /settings/users/)
What: (what exactly is wrong, for example "another user's file can be read")
Kind: (type, for example XSS, permission bypass, SQL injection; version from the VERSION file)
```

## Good to know

- Free does not update itself. Fixes ship as new versions on the [Releases](../../releases) page. Follow them: **Watch → Custom → Releases**.
- Check the archive checksum before installing: `sha256sum -c easygrc-<version>-free.tar.gz.sha256`. Download archives only from this repository.
- Never post `.env`, passwords, keys or the contents of `deploy/tls/` in an issue. If you did by mistake, treat them as compromised and replace them.
