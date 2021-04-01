here's how to use the query logger in MySQL

-- enable query logging
SET global `general_log` = 1;
SET global `log_output` = 'table';

-- run your test

-- see what's in there
SELECT * 
FROM `mysql`.`general_log` 
WHERE `command_type` = 'Execute' 
ORDER BY event_time DESC;

-- delete entries so you can run test again
TRUNCATE `mysql`.`general_log`;

