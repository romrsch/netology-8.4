## Домашнее задание к занятию "8.4 Работа с Roles"


### Подготовка к выполнению

* Создайте два пустых публичных репозитория в любом своём проекте: `kibana-role` и `filebeat-role`.
* Добавьте публичную часть своего ключа к своему профилю в github.


### Основная часть

Наша основная цель - разбить наш playbook на отдельные roles. Задача: сделать roles для elastic, kibana, filebeat и написать playbook для использования этих ролей. Ожидаемый результат: существуют два ваших репозитория с roles и один репозиторий с playbook.

1. Создать в старой версии playbook файл requirements.yml и заполнить его следующим содержимым:
```
---
  - src: git@github.com:netology-code/mnt-homeworks-ansible.git
    scm: git
    version: "2.0.0"
    name: elastic 
```
2. При помощи `ansible-galaxy` скачать себе эту роль.
3. Создать новый каталог с ролью при помощи `ansible-galaxy role init kibana-role`.
4. На основе tasks из старого playbook заполните новую role. Разнесите переменные между `vars` и `default`.
5. Перенести нужные шаблоны конфигов в `templates`.
6. Создать новый каталог с ролью при помощи `ansible-galaxy role init filebeat-role`.
7. На основе tasks из старого playbook заполните новую role. Разнесите переменные между `vars` и `default`.
8. Перенести нужные шаблоны конфигов в templates.
9. Описать в `README.md` обе роли и их параметры.
10. Выложите все roles в репозитории. Проставьте тэги, используя семантическую нумерацию.
11. Добавьте roles в `requirements.yml` в playbook.
12. Переработайте playbook на использование roles.


Выложите playbook в репозиторий.
В ответ приведите ссылки на оба репозитория с roles и одну ссылку на репозиторий с playbook.

***Ответ:***

Создал два пустых репозитория в github:

* [kibana-role](https://github.com/romrsch/kibana-role)
* [filebeat-role](https://github.com/romrsch/filebeat-role)

Создал файл `requirements.yml` и с помощью команды скачал её себе.

```
romrsch@ubuntu:~/8.4/playbook$ ansible-galaxy install -r requirements.yml --roles-path ./
```
![alt](https://i.ibb.co/Vq6jTGv/Screenshot-2.jpg)


>Создать новый каталог с ролью при помощи ansible-galaxy role init kibana-role.
```
romrsch@ubuntu:~/8.4/playbook$ ansible-galaxy role init kibana-role
```
![alt](https://i.ibb.co/w0bFdXc/Screenshot-12.jpg)

> Создать новый каталог с ролью при помощи ansible-galaxy role init filebeat-role.
> 
```
romrsch@ubuntu:~/8.4/playbook$ ansible-galaxy role init filebeat-role
```
![alt](https://i.ibb.co/HKLnZjv/Screenshot-3.jpg)

ссылки на репозитории

* [kibana-role](https://github.com/romrsch/kibana-role)
* [filebeat-role](https://github.com/romrsch/filebeat-role)


--
