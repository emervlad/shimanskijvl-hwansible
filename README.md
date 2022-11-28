# Homework 3: Ansible
## Запуск машин Vagrant

Чтобы запустить три машины, необходимо

- Изменить значения массивов box и box_url, поскольку я скачивал коробки локально (virtualbox: ubuntu/trusty64, centos/7, archlinux/archlinux), также все работают на localhost. Порты оставил по умолчанию. Версия боксов указана в их названии в  Vagrantfile.
- Запустить ``` vagrant up ```

## Запуск ролей Ansible

- Прописать ``` export ANSIBLE_HOST_KEY_CHECKING=False ```
- Прописать ``` ansible-playbook -i hosts play.yml ```

Зайти в VirtualBox и начать проверку по инструкции из репозитория с условиями ДЗ
