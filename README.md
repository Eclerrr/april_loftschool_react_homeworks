
# 7 домашнее задание
[Пример](http://5a78bddda6188f169349f1e8.confident-dubinsky-462dd0.netlify.com)

Используя api сервиса tvmaze.com необходимо построить систему поиска сериалов по названию и описанию. Также требуется сделать роутинг и переходы на страницы найденных сериалов. На страницах сериалов нужно обязательно отразить актеров, которые участвовали.


Требования к домашнему заданию:

1. Для работы с api в репозитории будет находится фаил `src/api.js` с готовыми функциями для поиска и получения сериала по id.

2. Сетевые запросы должны совершаться из middleware.

3. Для работы с асинхронными запросами нужно воспользоваться 3 экшенами `_REQUEST`, `_SUCCESS`, `_FAILURE`.

4. Для создания всех экшенов использовать метод `createActions` из библиотеки `redux-actions`.

5. Для описания редьюсеров _желательно_ использовать метод `handleActions` из библиотеки `redux-actions`.

6. Для каждого сериала url страницы должен выглядеть как **/shows/:id** где `id` — id сериала с сайта `tvmaze.com`.

7. При переходе на страницу сериала из поиска должен совершать сетевой запрос за информацие о сериале, и в это время нужно отражать надпись, сообщающую о том, что происходит загрузка.

8. При поиске на странице поиска так же должна выводиться надпись о том, что происходит загрузка, пока происходит себевой запрос.

9. Выдача результатов поиска должна содержать картинки, краткое содержание и ссылку на страницу сериала.


## Подсказки

Поле `summary` в ответах на запросы `api.tvmaze.com` содержит описание вместе с html тегами. Чтобы вывести html в реакте, воспользуйтесь методом **dangerouslySetInnerHTML**:

```
<div dangerouslySetInnerHTML={{__html: summary}} />
```



