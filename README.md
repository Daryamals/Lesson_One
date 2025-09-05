# Lesson_One

#### **Регистрация и базовая настройка**
Создайте аккаунт на github.com, если его нет.

**Настройте профиль:**

- Загрузите аватар
- Укажите краткую информацию о себе (например, «Студент курса по Git»)

Сгенерируйте SSH-ключ и добавьте его в настройках профиля:

```bash
ssh-keygen -t ed25519 -C "ваш_email@example.com" cat ~/.ssh/id_ed25519.pub
```

Скопируйте вывод в Settings → SSH and GPG keys.

#### **Работа с репозиторием**

1. На GitHub создайте публичный репозиторий my-git-practice.

2. Клонируйте его на локальную машину:

```bash
git clone git@github.com:ваш-логин/my-git-practice.git cd my-git-practice
```

**Первый коммит**

Создайте файл hello.py с кодом:

```bash
print("Hello GitHub!")
```

Зафиксируйте изменения:

```bash
git add .
git commit -m "Добавлен скрипт-приветствие"
git push -u origin main
```

**Ветвление и Pull Request**

Работа в отдельной ветке

1. Создайте ветку для новой функции:

```bash
git checkout -b feature/calculator
```

2. Добавьте в hello.py простой калькулятор:

```python
def add(a, b):
     return a + b
```

3. Отправьте ветку на GitHub:

```bash
git push -u origin feature/calculator
```

#### **Создание Pull Request**

**1. На GitHub:**

- Перейдите в репозиторий → вкладка Pull Requests → New Pull Request
- Выберите feature/calculator для слияния с main
- Напишите описание: «Добавлена функция сложения»
- Создайте PR

**2. Слейте PR через кнопку Merge Pull Request.**

#### **Конфликты и их решение**

**Имитация конфликта**

1. На GitHub прямо в интерфейсе измените hello.py (добавьте комментарий # Основной файл).

2. Локально в той же строке добавьте другой комментарий (# Версия 2.0) и сделайте commit + push:

```bash
git checkout main # Внесите изменения и...
git commit -am "Обновление комментария"
git push
```

Получите ошибку! [rejected].

3. Исправьте конфликт:

```bash
git pull # Смотрим конфликт в hello.py
# Редактируем файл, оставляя оба комментария
git add .
git commit -m "Исправлен конфликт"
git push
```

#### **Работа с чужим репозиторием**

**Fork и Contribution**

1. Найдите любой open-source проект на GitHub

2. Сделайте Fork репозитория.

3. Клонируйте свой форк:

```bash
git clone git@github.com:ваш-логин/first-contributions.gi
```

4. Создайте ветку, внесите изменение (например, добавьте своё имя в Contributors.md).

5. Создайте PR в оригинальный репозиторий

**Проверка работы**

- На GitHub должны быть:
- Репозиторий my-git-practice с 2+ коммитами
- Завершённый Pull Request
- Пример участия в open-source (ваш PR в другом репозитории)

Локально:

```bash
git log --oneline --graph # Должна быть видна история слияний
```
