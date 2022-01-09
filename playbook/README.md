# Самоконтроль выполненения задания

1. Где расположен файл с `some_fact` из второго пункта задания?
```group_vars/all/examp.yml```
2. Какая команда нужна для запуска вашего `playbook` на окружении `test.yml`?
```ansible-playbook site.yml -i inventory/test.yml```
3. Какой командой можно зашифровать файл?
```ansible-vault encrypt```
4. Какой командой можно расшифровать файл?
```ansible-vault dencrypt```
5. Можно ли посмотреть содержимое зашифрованного файла без команды расшифровки файла? Если можно, то как?
```Можно, но прочитать ничего не получится :)```
```ansible-vault view имяфайла```
6. Как выглядит команда запуска `playbook`, если переменные зашифрованы?
```ansible-playbook -i inventory/prod.yml site.yml --ask-vault-pass```
7. Как называется модуль подключения к host на windows?
```winrm - Run tasks over Microsoft's WinRM```
```ansible.builtin.winrm```
8. Приведите полный текст команды для поиска информации в документации ansible для модуля подключений ssh
```ansible-doc -t connection -l```
```ansible-doc -t connection ssh ```
9. Какой параметр из модуля подключения `ssh` необходим для того, чтобы определить пользователя, под которым необходимо совершать подключение?
```
remote_user
        Authentication password for the `remote_user'. Can be supplied as CLI option.
        [Default: (null)]
        set_via:
          vars:
          - name: ansible_password
          - name: ansible_ssh_pass
          - name: ansible_ssh_password
```