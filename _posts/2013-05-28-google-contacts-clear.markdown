---
layout: post
title: Чистим контакты в google
permalink: /2013/05/google-contacts-clear/
---

У меня возникла проблема с крашем адресной книги в android. Совершенно невыносимая проблема, которая не решилась сменой аппарата. Вроде бы все было нормально в адресной книге, пока я не заметил галочку отображать контакты только с номерами телефонов.
Убрав галочку я обнаружил 4800 контактов с js кодом вместо имени и описания. Этот код был эхом импорта контактов из mail.ru. Ничего не имею против mail.ru, но где то произошел косяк, который я не замечал пару лет, пока android фон не начал перезагружаться в адресной книге.
Еще не работал автоподбор контактов htc, но это я повесил на саму htc. 

**Итак проблема:**
4800 ненужных контактов в google contacts, которые своими данными и кол-во портят жизнь моему android телефону.

**Решение:**
Открываю vim(текстовый редактор на выбор)...

<script src="https://gist.github.com/Partysun/5661268.js"></script>

Немного надо знать о пароле. Если у вас двухэтапная аутентификация, то пароль надо создать специально для нашего скрипта.
На <a href="https://www.google.com/settings/security">Security старнице</a> надо зайти в управление доступом и создать новый пароль для приложения, что кстати очень удобно в нашем случае. Мы не передаем настоящий пароль, а просто используем временный специальный пароль, который сразу же после чистки контактов можно удалить.

**Заключение**
После чистки контактов - падение ос android в адресной книге прекратилось и также начал работать автоподбор htc. Интересно как решилась бы эта проблема при обращении в саппорт google.
