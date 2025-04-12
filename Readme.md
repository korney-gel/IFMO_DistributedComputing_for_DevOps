# 🧪 Лабораторная работа №2

## 📌 Цель работы

Развёртывание кластера баз данных (MySQL Master–Slave) и WordPress с помощью Ansible и Docker.
---

## 📁 Структура проекта

```bash
ansible-wordpress/
├── inventory.ini              # Inventory-файл с описанием хостов
├── playbook.yml              # Основной playbook
├── files/
│   └── docker-compose.yml    # Docker Compose файл для запуска WordPress и MySQL
├── ansible.cfg               # Конфигурация Ansible
├── .gitignore                # Исключения для Git
└── README.md                 # Описание проекта (вы читаете его!)

🔧 Что делает playbook
	•	Устанавливает Docker и Docker Compose на удалённую машину
	•	Разворачивает сервисы:
	•	db-master (MySQL, принимает записи)
	•	db-slave (MySQL, реплика, только чтение)
	•	wordpress (веб-интерфейс)
	•	Настраивает:
	•	репликацию между мастером и слейвом
	•	базу данных mydb
	•	пользователя user с паролем password и правами на mydb
	•	Гарантирует, что WordPress успешно подключается к БД