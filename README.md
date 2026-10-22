<div align="center">

# EasyGRC

**Система управления соответствием и рисками.**

[![Последняя версия](https://img.shields.io/github/v/release/whoami-ru/EasyGRC-Free-Releases?label=%D0%B2%D0%B5%D1%80%D1%81%D0%B8%D1%8F&color=2ea043)](https://github.com/whoami-ru/EasyGRC-Free-Releases/releases/latest)
[![Лицензия](https://img.shields.io/badge/%D0%BB%D0%B8%D1%86%D0%B5%D0%BD%D0%B7%D0%B8%D1%8F-PolyForm%20Strict%201.0.0-blue)](#лицензия)
[![Linux x86_64](https://img.shields.io/badge/Linux-x86__64-lightgrey)](#требования)

[**Скачать последнюю версию**](https://github.com/whoami-ru/EasyGRC-Free-Releases/releases/latest) · [English](README.en.md) · [Предложить доработку](https://github.com/whoami-ru/EasyGRC-Free-Releases/issues/new/choose)

</div>

---

## Установка за 3 шага

**1. Скачайте** архив `easygrc-<версия>-free.tar.gz` и файл `.sha256` со страницы [Releases](https://github.com/whoami-ru/EasyGRC-Free-Releases/releases/latest).

**2. Проверьте целостность** (на сервере, оба файла в одной папке):

```bash
sha256sum -c easygrc-<версия>-free.tar.gz.sha256
```

Должно появиться `OK`. Если нет, скачайте файл заново.

**3. Установите:**

```bash
sudo mkdir -p /opt/easygrc
sudo tar -xzf easygrc-<версия>-free.tar.gz -C /opt/easygrc --strip-components=1
cd /opt/easygrc
sudo ./install.sh
```

Скрипт проверит сервер, при необходимости поставит Docker, загрузит образы, спросит язык и доменное имя, создаст настройки и сертификат, запустит систему и предложит создать первого администратора. После этого откройте `https://<адрес сервера>/`.

Подробная инструкция (домен и сертификат, резервные копии, диагностика) лежит в архиве, в файле `INSTALL.md`.

## Требования

- Linux x86_64: Ubuntu 22.04+, Debian 12+, AlmaLinux/Rocky/RHEL 9+ или аналог. Windows и macOS не поддерживаются.
- 2 vCPU, 4 ГБ памяти, 20 ГБ диска. Для пробы хватит 1 ГБ памяти и swap на 2 ГБ.
- Порты 80 и 443. Домен не обязателен: без него система открывается по IP-адресу.
- Не уверены, что сервер подойдёт? Запустите `sudo ./install.sh --check`, он ничего не меняет и покажет, чего не хватает.


## Предложения и вопросы

Нашли ошибку, не хватает функции или что-то непонятно в установке? [Создайте issue](https://github.com/whoami-ru/EasyGRC-Free-Releases/issues/new/choose), там есть шаблоны. Приложите версию из файла `VERSION` и не публикуйте `.env`, пароли и ключи.

Об уязвимостях сообщайте закрыто, а не в issue: [SECURITY.md](SECURITY.md).

## Лицензия

Программа распространяется на условиях [PolyForm Strict 1.0.0](https://polyformproject.org/licenses/strict/1.0.0): можно использовать для некоммерческих целей, нельзя распространять и изменять. Полный текст лежит в файле `LICENSE` внутри архива. Этот репозиторий содержит только описание и релизы, исходного кода здесь нет.

##

Хотите получать сообщения о новых версиях? Нажмите **Watch → Custom → Releases** вверху страницы.
