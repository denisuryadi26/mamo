# Heartbeat Tasks

## Auto-Backup Memory (2-3x per hari)

Check if memory files have changed since last backup, then commit & push to GitHub.

**Commands:**
```bash
cd /home/aingmaung/.openclaw/workspace
git add -A
git diff --cached --quiet || (git commit -m "Auto-backup: $(date '+%Y-%m-%d %H:%M')" && git push origin main)
```

**Frequency:** Every 4-6 hours during active hours (08:00-23:00)

**Track state in:** `memory/backup-state.json`
