Пример настроек logstash для выгрузки журнала регистрации 1С в Elasticsearch 6.6.
Выгрузка производилась настройкой заданий в планировщике Win:

"c:\Program Files (x86)\1cv8\8.3.13.1513\bin\1cv8.exe" 
      ENTERPRISE 
      /DisableStartupMessages 
      /IBConnectionString"Srvr=""ServName"";Ref=""BaseName""" 
      /RunModeManagedApplication 
      /Execute"\\PathTo\ВыгрузкаЖР2Elastic.epf"

В выложеной обработке закомментирована выгрузка журнала при открытии формы.

В конфигурациях на БСП можно использовать обработку ОбрабткаВыгрузкиЖРсЗапускомПоРасписанию.epf 
добавив ее в дополнительные обработки и назначив расписание выполнения. Эту обработку так же 
можно использовать для ручной выгрузки.

Файл маппинга получен из индекса oncjornallog на его основе сделан шаблон(template) для создания
индексов oncjornalloп* с переопределенным анализатором для некоторых полей, что обеспечивает 
поиск в формате you-search-as-you-type.

Статьи, которые помогли:</br>
https://www.elastic.co/guide/en/elasticsearch/guide/current/_index_time_search_as_you_type.html</br>
https://tyvik.ru/posts/elasticsearch/
