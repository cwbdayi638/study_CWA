# 🌐📦 **手動上傳指引** - Manual Upload Guide

## ✅ File List Ready for Upload:

### 📁 24 PDF Research Papers (Earthworm EEW)
```
total files: ~24
estimated size: ~10-12MB
source directory: /root/.openclaw/workspace/Earthworm/data/papers/
```

### 📝 ~7 Markdown Reports:
```
total files: ~7
estimated size: ~35KB combined
source directory: /root/.openclaw/workspace/Earthworm/data/
- download-complete-report.md
- heartbeat-report-20260322.md
- weather-report-20260322.md
- code-claude-doc-compiled.md
- upload-preparation-guide.md
- google-drive-tools-install-report.md
- weatherservice-config.md
```

---

## 🎯 Upload Steps (Manual):

### Step 1: Copy Files to Single Folder (Optional)
```bash
cd /root/.openclaw/workspace/Earthworm/data/
tar -czvf earthworm-full-backup.tar.gz papers/*.md *.md research-*.md
# Note: .pdf files in data/papers/* need separate ZIP
```

### Step 2: Google Drive Upload via Manual Browser:
```
Step 1: Open https://drive.google.com/drive/folders/12dR__rBfQ8HsDObyvhqdhtEg3iIzCN7z in browser
Step 2: Copy all PDF files from ~/Earthworm/data/papers/*
        (or use terminal to drag-drop if supported by your OS)
Step 3: Upload all .md reports as well
Step 4: Verify upload completion (should take ~1-5 minutes for ~20MB)
```

### Step 3: Alternative - Use GDrive CLI Tools:
```bash
# If you later install gdrive (when pip3 available):
gcp earthworm-backup.tar.gz "earthworm-reports/" \
```

---

## 📊 Upload Summary:

| Category | Files | Estimated Size |
|--:-|-:|
| *Earthworm PDF papers* | 24 files | ~10-12MB|
| *System reports (MD)* | ~7 files | ~35KB|
| *Configuration files* | ~3 files | ~10KB|
| **Total** | **~34 items** | **~10.5MB+**

---

## 🌐 Next Steps:

1. ✅ Upload all Earthworm research papers to Google Drive folder
2. ✅ Add weather reports and system documentation
3. ⏰ Verify upload completed successfully
4. 🔄 Backup to additional location (Dropbox/OneDrive as alternative)

---

## 📝 System Status:

*All Earthworm analysis reports complete, ready for upload via manual browser or future cloud tools.*

**Next heartbeat will check**: Weather service at ~20:30 UTC (08:30 Taiwan time tomorrow).
