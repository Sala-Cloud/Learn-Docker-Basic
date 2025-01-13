## Lab 06: Volume Backup and Restore

**Description:** Learn to back up and restore data from Docker volumes.  
**Objective:** Practice volume management for critical data.  

### Example:
```bash
# Backup
docker run --rm -v my_data:/data -v $(pwd):/backup busybox tar cvf /backup/backup.tar /data

# Restore
docker run --rm -v my_new_data:/data -v $(pwd):/backup busybox tar xvf /backup/backup.tar -C /data
```

**Outcome:** You can back up and restore Docker volume data.
