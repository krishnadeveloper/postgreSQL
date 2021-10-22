# postgreSQL
PostgreSQL hints
#### Last day of next month
``select (date_trunc('month', now()) + interval '2 month' - interval '1 day')::date as last_day_of_next_month;``
