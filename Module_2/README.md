# Optional vedios
1. https://www.youtube.com/watch?v=HQKwgk6XkIA&t=17s  
2. https://www.db-book.com/university-lab-dir/sqljs.html  
3. https://www.w3resource.com/sqlite-exercises/  
4. https://www.w3resource.com/sql-exercises/  


# Debugging in SQLite CLI

### Understanding the `...>` Prompt
Whenever you see the `...>` prompt in SQLite CLI, it means SQLite is waiting for more input to complete a multi-line SQL command or statement. This happens when:
- A semicolon `;` is missing at the end of the statement.
- The command structure is incomplete (e.g., missing parentheses or quotes).

### How to Exit the `...>` Prompt

1. **Use a Semicolon (`;`) to End the Statement**:
   - Simply type `;` and press Enter to terminate the current input and return to the `sqlite>` prompt. Example:
     ```sql
     sqlite> open fardin_db_1.db
        ...> ;
     Parse error: near "open": syntax error
     sqlite>
     ```
   - This approach avoids exiting the SQLite CLI and allows you to continue working.

2. **Use `Ctrl+C` (Not Recommended)**:
   - Pressing `Ctrl+C` will cancel the ongoing command but also exit SQLite completely, returning you to the system shell (e.g., PowerShell or Terminal).
   - Use this only if you want to exit SQLite altogether.
---

## Comparison Table: Windows vs SQLite Commands

| Task                | Windows PowerShell Command | SQLite CLI Command |
|---------------------|----------------------------|--------------------|
| List directory      | `dir`                     | `.shell dir`       |
| Change directory    | `cd <directory>`          | `.cd <directory>`  |
| Go back one level   | `cd ..`                   | `.cd ..`           |
| Show current path(where you at now)   | `cd`                      | `.shell cd`        |

---
## Steps and Commands

### 1. Navigating Directories in PowerShell

```powershell
PS C:\Users\User> D:
PS D:\> cd '.\Winter 25\'
PS D:\Winter 25> ls

    Directory: D:\Winter 25

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----          1/7/2025  11:13 AM                BizzBuzz-e-commerce
d-----         1/11/2025  12:26 PM                CMPT_354
d-----          1/9/2025   1:35 PM                STAT 302

PS D:\Winter 25> cd .\CMPT_354\
PS D:\Winter 25\CMPT_354> ls

    Directory: D:\Winter 25\CMPT_354

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----          1/8/2025   7:16 PM                Module_1
d-----         1/11/2025  12:27 PM                Module_2
```

### 2. Starting SQLite

```powershell
PS D:\Winter 25\CMPT_354> sqlite3
SQLite version 3.42.0 2023-05-16 12:36:15
Enter ".help" for usage hints.
Connected to a transient in-memory database.
Use ".open FILENAME" to reopen on a persistent database.
```

### 3. Exploring SQLite Commands

```sql
sqlite> .help
# Displays a list of available SQLite commands
```
### 4. Create or Open a Database
From the SQLite prompt (`sqlite>`), use the `.open` command followed by your desired database filename:

```sql
.open fardin_database.db
```

- **Creating a New Database**: If the file `fardin_database.db` does not exist, SQLite will create it in the current directory.
- **Opening an Existing Database**: If the file already exists, SQLite will open the file for interaction.

### 4. Verify the Database
To ensure the database is open or to list all attached databases, use:

```sql
.databases
```

### Example Output
```sql
sqlite> .databases
seq  name             file
---  ---------------  --------------------------
0    main             D:/Winter 25/CMPT_354/fardin_database.db
```

---

