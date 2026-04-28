# 🛡️ Linux for Cloud Security: Day 09
## Topic: Advanced Process Management & Signal Control

Welcome to Day 09 of my Linux journey. Today's focus was on **Process Management**—a critical skill for any Cloud Security professional. In a cloud environment, identifying rogue processes, monitoring resource anomalies, and terminating threats gracefully is fundamental to incident response.

---

## 📋 Learning Objectives
- [x] Identify system-wide processes using `ps` snapshots.
- [x] Monitor real-time resource consumption with `htop`.
- [x] Understand the Linux Signal Hierarchy (`SIGTERM` vs `SIGKILL`).
- [x] Manage background/foreground jobs for security scanning.

---

## 🔍 1. Process Discovery
In security, visibility is everything. I practiced using tools to audit running services.

| Command | Description | Security Use Case |
| :--- | :--- | :--- |
| `ps aux` | Standard snapshot of all processes | Identifying unknown users running tasks. |
| `ps auxf` | Tree-view of processes | Detecting if a web server spawned a shell. |
| `pgrep <name>` | Find PID by process name | Fast lookup for automated scripts. |

**Key Takeaway:** Always check the **PPID** (Parent PID). If the parent process looks suspicious, the child is likely malicious.

---

## 📊 2. Live Monitoring
Real-time monitoring helps detect **Cryptojacking** or **DoS** attacks before they crash the server.

- **Tool used:** `htop`
- **Key Features:**
  - Interactive filtering (`F4`) to isolate specific services.
  - Sorting by `%CPU` or `%MEM` to find resource hogs.
  - Visualizing core usage to check for unusual system load.

---

## 🗡️ 3. The Art of the Kill (Signals)
Termination isn't just about stopping a program; it's about communication.

```bash
# Graceful shutdown (Standard for most scenarios)
kill <PID> 

# Forceful shutdown (For non-responsive malware)
kill -9 <PID>

# Reload configuration without stopping service
kill -1 <PID>
