# postgreSQL
PostgreSQL hints
#### Last day (date) of next month
``select (date_trunc('month', now()) + interval '2 month' - interval '1 day')::date as last_day_of_next_month;``

#### First day (date) of next month
``select (date_trunc('month', now()) + interval '1 month')::date as first_day_of_next_month;``

#### First day (date) of current month
``select to_char(now(), 'YYYY-MM-01') as first_day_of_month;``

#### Last day (date) of current month
``select (date_trunc('month', now()) + interval '1 month' - interval '1 day')::date as last_day_of_current_month;``

#### Concatination String
``Ex1 : 'hello' || '_world' => hello_world``
``Ex2 : 'John's' || ' is pro.' => John's is pro.``
``Ex3 : ''' || 'Jack' || ''' => 'Jack'.``

#### compare two rows from two table / Detect change between two rows
``SELECT COALESCE(ta.* != tb.*, false) AS changeDetect, ta.* FROM tableA AS ta RIGHT JOIN tableB AS tb USING (id) where COALESCE(ta.* != tb.*, false) is TRUE; ``
