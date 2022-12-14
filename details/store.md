# Хранилища

### База данных

Для решения большинства задач вам будет необходима реляционная база данных. 
В качестве реляционной базы данных используем ТОЛЬКО `PostgreSQL`. 

Для InMemory баз данных можно использовать `Redis v6.2` или выше. Данное хранилище должно быть использовано для таких задач как: хранения сессий, хранения кеша. Данное хранилище не должно быть использовано для хранения важных данных, так как оно является не персистентным.

### Ведение баз данных (рекомендации):
#### БД должна иметь минимум логики. 
Клиентов много, и нужно оставить логику им, а в БД должны быть простые и быстрые запросы в рамках минимально возможных коротких транзакций.
Не следует использовать триггеры и процедуры в БД. 

Размазывание логики между разными слоями системы делает код не очевидным и приводит к усложнению поддержки системы. Вся бизнес-логика реализуется в приложении.

#### Не используем foreign key
`Foreign key` увеличивает накладные расходы на вставку и обновление записей. Предпочтительно контролировать все связи на стороне приложения, а FK использовать в случаях, где связность важнее производительности.

Можно игнорировать это правило в системах, где производительность не является ключевым аспектом

#### Не используем в запросах "select * ". 
При удалении колонки порядок полей в запросе может измениться и логика чтения результата будет сломана.

#### Вставка
Для оптимизации вставки большого количества записей используйте bulk insert. Каждую пачку записей нужно добавлять в рамках отдельной транзакции.

#### Миграции данных БД.
Миграции производятся с помощью инструмента goose.