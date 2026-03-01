def total_salary(path):
    total = 0
    count = 0

    try:
        with open(path, "r", encoding="utf-8") as file:
            for line in file:
                line = line.strip()
                if not line:
                    continue  # пропускаємо порожні рядки

                try:
                    name, salary = line.split(",")
                    total += float(salary)
                    count += 1
                except ValueError:
                    print(f"Некоректний рядок у файлі: {line}")
                    continue

        if count == 0:
            return (0, 0)

        average = total / count
        return (total, average)

    except FileNotFoundError:
        print("Файл не знайдено.")
        return (0, 0)
    except Exception as e:
        print(f"Сталася помилка: {e}")
        return (0, 0)
