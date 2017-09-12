---
layout: post
title: 7. ORA-00911 invalid character
---


An ORA-00911 error message is an error that occurs when an SQL statement is misspelled.


if you faces this error, check this 4 cases.

1. missed or wrong put the '(single quotation)
2. missed or wrong put the ;(semicolon)
3. checked ?(question mark)
4. checked alias


Ex1) 
```
StringBuffer sql = new StringBuffer();
sql.append(" insert into dept (dept_id,name)  values(?,?) ; ");
```

-> delete ; where end of "

```
StringBuffer sql = new StringBuffer();
sql.append(" insert into dept (dept_id,name)  values(?,?) ");
```
