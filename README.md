## [REST API](http://localhost:8080/doc)

## Концепция:
- Spring Modulith
  - [Spring Modulith: достигли ли мы зрелости модульности](https://habr.com/ru/post/701984/)
  - [Introducing Spring Modulith](https://spring.io/blog/2022/10/21/introducing-spring-modulith)
  - [Spring Modulith - Reference documentation](https://docs.spring.io/spring-modulith/docs/current-SNAPSHOT/reference/html/)

```
  url: jdbc:postgresql://localhost:5432/jira
  username: jira
  password: JiraRush
```
- Есть 2 общие таблицы, на которых не fk
  - _Reference_ - справочник. Связь делаем по _code_ (по id нельзя, тк id привязано к окружению-конкретной базе)
  - _UserBelong_ - привязка юзеров с типом (owner, lead, ...) к объекту (таска, проект, спринт, ...). FK вручную будем проверять

## Аналоги
- https://java-source.net/open-source/issue-trackers

## Тестирование
- https://habr.com/ru/articles/259055/

Список выполненных задач:
- [X] Onboarding
- [X] Delete Social networks
- [X] Take out sensitive information
- [X] Configure the H2 in memory test database
- [ ] Write tests for all public methods of the Profile Test Controller controller.
- [ ] Add adding tags to a task
- [ ] Add the ability to subscribe to tasks that are not assigned to the current user
- [ ] Add automatic time counting for how long the task was in operation, testing, etc.
- [ ] Write a Dockerfile for the main server
- [ ] Write a docker-compose file to run the server container together with the database and nginx
- [ ] Add localization in at least two languages for email templates and the home page index.html .
- [ ] Implement a backlog – a complete list of tasks (with paging) that must be completed and do not yet relate to any sprint. (back + front)
- [ ] Redo the "friend-for" recognition mechanism between the front and back from JSESSIONID to JWT