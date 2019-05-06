Пример настроек logstash для выгрузки журнала регистрации 1С в Elasticsearch 6.6.
Выгрузка производилась настройкой заданий в планировщике Win:

"c:\Program Files (x86)\1cv8\8.3.13.1513\bin\1cv8.exe" 
      ENTERPRISE 
      /DisableStartupMessages 
      /IBConnectionString"Srvr=""ServName"";Ref=""BaseName""" 
      /RunModeManagedApplication 
      /Execute"\\PathTo\ВыгрузкаЖР2Elastic.epf"

В выложеной обработке закомментирована выгрузка журнала при открытии формы.
