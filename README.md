# ⏰ Scheduling GitHub Actions Using CRON Jobs

This repository demonstrates how to **schedule GitHub Actions workflows using CRON jobs**.  
Instead of triggering workflows only on push or pull requests, this setup allows workflows to **run automatically at fixed time intervals**.

---

## 📌 What You’ll Learn

- ✅ What CRON jobs are
- ✅ How CRON scheduling works in GitHub Actions
- ✅ How to schedule workflows using `cron`
- ✅ How scheduled workflows differ from event-based workflows
- ✅ Real-world use cases of scheduled GitHub Actions

---

## 🧠 What Is a CRON Job?

A **CRON job** is a time-based task scheduler commonly used in Linux systems.  
It allows tasks to run automatically at specific times or intervals.

GitHub Actions supports CRON scheduling using the same syntax, making it useful for:
- Nightly builds
- Automated checks
- Data sync jobs
- Cleanup tasks
- Health monitoring

---

## ⚙️ Workflow Trigger Using CRON

Scheduled workflows are defined using the `schedule` event inside the workflow file.

### 🔹 Example Trigger

```yaml
on:
  schedule:
    - cron: '0 0 * * *'
