# 🛠️ Структура курса DevOps с краткими описаниями

## 1. Введение в DevOps (2 недели)
**Ключевые темы:**  
- Философия DevOps: принципы «три пути», культура collaboration  
- Жизненный цикл CI/CD: от кода до production  
- Обзор инструментария: Git, Jenkins, Docker, Kubernetes, Terraform  
*Пример:* История трансформации Netflix через DevOps практики.

---

## 2. Системы контроля версий (Git Advanced) (1.5 недели)
**Что изучаем:**  
- Ветвление стратегий (Git Flow vs Trunk-Based)  
- Интерактивный rebase, cherry-pick, подмодули  
- Git Hooks для автоматизации Code Review  
*Практика:* Создание pre-commit hook для проверки синтаксиса Python.

---

## 3. Непрерывная интеграция и доставка (CI/CD) (3 недели)
**Инструменты:** Jenkins, GitLab CI, GitHub Actions  
**Кейсы:**  
- Настройка pipeline с параллельными job  
- Артефакты сборки и их хранение  
- Blue-Green Deployment на примере AWS  
*Пример конфига:*
```yaml
# GitHub Actions для Node.js
name: Node.js CI
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v3
    - name: Install dependencies
      run: npm ci
    - name: Run tests
      run: npm test
