## Ruby: сервис статистики видеопросмотров 

Напишите на Ruby сервис, реализующий REST API со следующими функциями:

- Принимает от клиентов уведомления о том, что клиент смотрит видео. 

    Параметры: `customer_id` — идентификатор пользователя, `video_id` — идентификатор видео, которое смотрит пользователь.

- Отвечает на запрос, сколько видео потоков смотрит пользователь в данный момент. 

    Параметры: `customer_id` - идентификатор пользователя. 

- Отвечает на вопрос, сколько пользователей смотрят данное видео.

    Параметры: `video_id` — идентификатор видео.

**Дополнительные сведения:**

- Клиенты посылают уведомления о просмотре видео каждые 5 секунд, пока работает плеер. Если в течение 6 и более секунд уведомление от пользователя не пришло, то считается, что просмотр этого видео завершен. 

- Клиентов много и их не интересует ответ на уведомление о просмотре.

- Запросы 2 и 3 приходят существенно реже, нежели запрос 1. 

- Ответ на запрос 2 должен быть максимально актуальным.

- Ответ на запрос 3 может отставать и отражать ситуацию не на текущий момент, а, например, на минуту назад.

Использовать можно любой фреймворк, можно не использовать. Для хранилища можно использовать: память внутри самого ruby-приложения, postgresql, redis.

По желанию: реализовать адаптеры для разных хранилищ.