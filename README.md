# Traffic Test
## Table
``` sql
CREATE TABLE employees (
    emp_no      INT             NOT NULL,
    birth_date  DATE            NOT NULL,
    first_name  VARCHAR(14)     NOT NULL,
    last_name   VARCHAR(16)     NOT NULL,
    gender      ENUM('M','F')   NOT NULL,
    hire_date   DATE            NOT NULL,
    PRIMARY KEY (emp_no)
);

CREATE INDEX name ON employees (first_name, last_name);
source load_employees.dump
```

## Regex
### emp_no (INT)
^-?\d+$

### birth_date (DATE)
^\d{4}-\d{2}-\d{2}$

### first_name (VARCHAR(14))
^.{1,14}$

### last_name (VARCHAR(16))
^.{1,16}$

### gender (ENUM('M','F'))
^(M|F)$

### hire_date (DATE)
^\d{4}-\d{2}-\d{2}$

### length
^[1-9][0-9]*$