# Домашнее задание к занятию 10 «Jenkins»

## Подготовка к выполнению

1. Создать два VM: для jenkins-master и jenkins-agent.
2. Установить Jenkins при помощи playbook.
3. Запустить и проверить работоспособность.
4. Сделать первоначальную настройку.

## Основная часть

1. Сделать Freestyle Job, который будет запускать `molecule test` из любого вашего репозитория с ролью.  
**Ответ 1**  
[Полный лог задание 1](https://github.com/bag2000/ansible-nginx/blob/main/solutions/1-3-full-log.txt)  
![img1-1](https://github.com/bag2000/ansible-nginx/blob/main/solutions/1-1.png)  
![img1-2](https://github.com/bag2000/ansible-nginx/blob/main/solutions/1-2.png)  
![img1-3](https://github.com/bag2000/ansible-nginx/blob/main/solutions/1-3.png)  
2. Сделать Declarative Pipeline Job, который будет запускать `molecule test` из любого вашего репозитория с ролью.
**Ответ 2**  
[Полный лог задание 2](https://github.com/bag2000/ansible-nginx/blob/main/solutions/2-3-full-log.txt)  
![img2-1](https://github.com/bag2000/ansible-nginx/blob/main/solutions/2-1.png)  
![img2-2](https://github.com/bag2000/ansible-nginx/blob/main/solutions/2-2.png)  
![img2-3](https://github.com/bag2000/ansible-nginx/blob/main/solutions/2-3.png)  
3. Перенести Declarative Pipeline в репозиторий в файл `Jenkinsfile`.  
**Ответ 3**  
[Jenkinsfile](https://github.com/bag2000/ansible-nginx/blob/main/files/Jenkinsfile)  
4. Создать Multibranch Pipeline на запуск `Jenkinsfile` из репозитория.  
**Ответ 4**  
[Полный лог задание 4](https://github.com/bag2000/ansible-nginx/blob/main/solutions/4-2-full-log.txt)  
![img4-1](https://github.com/bag2000/ansible-nginx/blob/main/solutions/4-1.png)  
![img4-2](https://github.com/bag2000/ansible-nginx/blob/main/solutions/4-2.png)  
5. Создать Scripted Pipeline, наполнить его скриптом из [pipeline](./pipeline).
6. Внести необходимые изменения, чтобы Pipeline запускал `ansible-playbook` без флагов `--check --diff`, если не установлен параметр при запуске джобы (prod_run = True). По умолчанию параметр имеет значение False и запускает прогон с флагами `--check --diff`.
7. Проверить работоспособность, исправить ошибки, исправленный Pipeline вложить в репозиторий в файл `ScriptedJenkinsfile`.
**Ответ 7**  
[ScriptedJenkinsfile](https://github.com/bag2000/ansible-nginx/blob/main/files/ScriptedJenkinsfile) 
8. Отправить ссылку на репозиторий с ролью и Declarative Pipeline и Scripted Pipeline.
**Ответ 8**  
[Роль](https://github.com/bag2000/ansible-nginx/tree/main/roles)  
[Declarative Pipeline](https://github.com/bag2000/ansible-nginx/blob/main/files/Jenkinsfile)  
[ScriptedJenkinsfile](https://github.com/bag2000/ansible-nginx/blob/main/files/ScriptedJenkinsfile) 
9. Сопроводите процесс настройки скриншотами для каждого пункта задания!!