#🐧 100 Days of Linux — Day 14

🎯 Topic: Mastering the `uniq` Command

Today, I learned how to handle duplicate data using the `uniq` command. It is one of the most powerful tools for text processing, but it has a specific logic that every Linux user must master.



🔍 How `uniq` Works
The `uniq` command filters out repeated lines from a file. However, it **only detects adjacent duplicate lines**. 

> **Important:** If your duplicates are scattered throughout the file, `uniq` won't see them. To fix this, you must always **sort** your data first.

The "Golden Pipeline":
bash
sort file.txt | uniq



---

### 🛠️ Common Flags & Options

| Option | Command | Description |
| --- | --- | --- |
| **Count** | `uniq -c` | Prefixes each line with the number of times it occurred. |
| **Duplicates** | `uniq -d` | Only prints the lines that are repeated. |
| **Unique** | `uniq -u` | Only prints lines that appear exactly once. |
| **Ignore Case** | `uniq -i` | Ignores capitalization (e.g., treats "Linux" and "linux" as the same). |

---

### 🚀 Real-World Application: Log Analysis

I used `uniq` to analyze a web server log to find the most active IP addresses.

**The Pipeline:**

```bash
cat access.log | cut -d ' ' -f 1 | sort | uniq -c | sort -rn

```

**Step-by-step breakdown:**

1. `cat access.log`: Reads the file.
2. `cut -d ' ' -f 1`: Extracts only the first column (IP addresses).
3. `sort`: Groups identical IPs together (essential for `uniq`).
4. `uniq -c`: Counts how many times each IP appears.
5. `sort -rn`: Sorts the counts numerically in reverse (highest hits at the top).
