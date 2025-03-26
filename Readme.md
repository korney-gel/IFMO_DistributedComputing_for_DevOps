# 🧪 Лабораторная работа №1: Развёртывание WordPress через Ansible

## 📌 Цель работы

Автоматизировать установку Docker и запуск приложения WordPress с базой данных MySQL в отдельных контейнерах на удалённой виртуальной машине с использованием Ansible.

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