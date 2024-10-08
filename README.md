# Домашнее задание к занятию 2 «Использование Ansible» - Сергей Михалёв



## Основная часть

1. Допишите playbook: нужно сделать ещё один play, который устанавливает и настраивает LightHouse.
2. При создании tasks рекомендую использовать модули: `get_url`, `template`, `yum`, `apt`.
3. Tasks должны: скачать статику LightHouse, установить Nginx или любой другой веб-сервер, настроить его конфиг для открытия LightHouse, запустить веб-сервер.
4. Подготовьте свой inventory-файл `prod.yml`.
5. Запустите `ansible-lint site.yml` и исправьте ошибки, если они есть.
6. Попробуйте запустить playbook на этом окружении с флагом `--check`.
7. Запустите playbook на `prod.yml` окружении с флагом `--diff`. Убедитесь, что изменения на системе произведены.
8. Повторно запустите playbook с флагом `--diff` и убедитесь, что playbook идемпотентен.
9. Подготовьте README.md-файл по своему playbook. В нём должно быть описано: что делает playbook, какие у него есть параметры и теги.
10. Готовый playbook выложите в свой репозиторий, поставьте тег `08-ansible-03-yandex` на фиксирующий коммит, в ответ предоставьте ссылку на него.

---

### Решение

1. Резальтат поиска ошибо к при помощи `ansible-lint site.yml`
     <img src="images/Task_lint.png" alt="Task_lint.png" width="700" height="auto">
2. Результат запуска `ansible-playbook site.yml -i inventory/prod.yml --check`
   <img src="images/Task_check_1.png" alt="Task_check_1.png" width="700" height="auto">
3. Результат запуска `ansible-playbook site.yml -i inventory/prod.yml --diff`
   <img src="images/Task_diff.png" alt="Task_diff.png" width="700" height="auto">
4. Результат повторного запуска `ansible-playbook site.yml -i inventory/prod.yml --diff`
   <img src="images/Task_check_2.png" alt="Task_check_2.png" width="700" height="auto">
4. Ссылка на обновлённый [README.md](https://github.com/sergeMMikh/hw_ansible_02/blob/main/playbook/README.md) playbook.
5. Ссылка на [tag `08-ansible-03-yandex`](https://github.com/sergeMMikh/hw_ansible_02/releases/tag/08-ansible-03-yandex)

---
