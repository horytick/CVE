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

![image-20250702150306018](./images/image-20250702150306018.png)