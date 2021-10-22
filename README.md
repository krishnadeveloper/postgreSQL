# postgreSQL
PostgreSQL hints
#### Last day (date) of next month
``select (date_trunc('month', now()) + interval '2 month' - interval '1 day')::date as last_day_of_next_month;``

#### First day (date) of next month
``select (date_trunc('month', now()) + interval '1 month')::date as first_day_of_next_month;``

#### First day (date) of current month
``select to_char(now(), 'YYYY-MM-01') as first_day_of_month;``

#### Last day (date) of current month
``select (date_trunc('month', now()) + interval '1 month' - interval '1 day')::date as last_day_of_next_month;``
