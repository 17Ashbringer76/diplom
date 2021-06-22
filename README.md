## Дипломный проект профессии «Тестировщик»
### Документация
* <a href="https://github.com/17Ashbringer76/diplom/blob/main/Documents/Plan.md">План автоматизации тестирования;</a>
* <a href="https://github.com/17Ashbringer76/diplom/blob/main/Documents/Report.md">Отчёт по итогам автоматизированного тестирования;</a>
* <a href="https://github.com/17Ashbringer76/diplom/blob/main/Documents/Summary.md">Отчёт по итогам автоматизации;</a>

### Инструкция по запуску
1. Склонировать проект из репозитория
   * Открыть Git Bash и выполнить команду https://github.com/17Ashbringer76/diplom.git
2. Открыть проект в IDEA
   * Открыть проект с помощью IntelliJ IDEA Ultimate
3. Запустить контейнер с СУБД и симулятором сервисов Банка
   * Внутри IntelliJ IDEA запустить терминал и выполнить команду docker-compose up
4. Запустить приложение
   * Запуск с подключением к MySQL. Открыть новое окно терминала и выполнить команду java -Dspring.datasource.url=jdbc:mysql://localhost:3306/app -Dspring.datasource.username=app -Dspring.datasource.password=pass -jar aqa-shop.jar
   * Запуск с подключением к PostgreSQL. Открыть новое окно терминала и выполнить команду java -Dspring.datasource.url=jdbc:postgresql://localhost:5432/app -Dspring.datasource.username=app -Dspring.datasource.password=pass -jar aqa-shop.jar
5. Запустить тесты
   * Запуск с подключением к MySQL. Открыть новое окно терминала и выполнить команду gradlew clean test -Ddb.url=jdbc:mysql://localhost:3306/app -Ddb.user=app -Ddb.password=pass
   * Запуск с подключением к PostgreSQL. Открыть новое окно терминала и выполнить команду gradlew clean test -Ddb.url=jdbc:postgresql://localhost:5432/app -Ddb.user=app -Ddb.password=pass
6. Сформировать отчёт
   * Выполнить в терминале команду gradlew allureReport, затем команду gradlewServe
