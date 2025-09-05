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
git checkout -b feature
```

2. Добавьте в hello.py простой калькулятор:

```python
def add(a, b):
     return a + b
```

3. Отправьте ветку на GitHub:

```bash
git push -u origin feature
```

#### **Создание Pull Request**

**1. На GitHub:**

- Перейдите в репозиторий → вкладка Pull Requests → New Pull Request
- Выберите feature/calculator для слияния с main
- Напишите описание: «Добавлена функция сложения»
- Создайте PR


#### **Работа с чужим репозиторием**

**Fork и Contribution**

1. Найдите любой open-source проект на GitHub

2. Сделайте Fork репозитория Lesson_One: https://github.com/Daryamals/Lesson_One.

3. Клонируйте свой форк:

```bash
git clone ваша ссылка SSH
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
