# Upload Test Repository

Test repository for uploading customizable nested folder/file structures to GitHub.

## Quick Start

### 1. Generate Test Data

```bash
python generate_test_data.py
```

You'll be prompted to enter:
- **Depth**: How many folder levels deep (default: 3)
- **Folders per level**: Number of folders at each level (default: 3)
- **Files per folder**: Number of files in each folder (default: 5)
- **File size**: Size of each file in MB (default: 0.5)

**Examples:**

```
# Conservative (safe, quick)
Depth: 3
Folders: 3
Files: 5
Size: 0.5 MB
→ ~135 files, ~67 MB total

# Medium (good test)
Depth: 5
Folders: 3
Files: 10
Size: 1 MB
→ ~2,430 files, ~2.4 GB total

# Large (use with caution!)
Depth: 7
Folders: 5
Files: 10
Size: 2 MB
→ ~156,250 files, ~300 GB total ⚠️
```

### 2. Upload to GitHub

```bash
bash upload_to_github.sh
```

Or manually:

```bash
git add test_data/
git commit -m "Add test data"
git push origin main
```

## Repository Links

- **GitHub Repo**: https://github.com/eliasvestman-dotcom/Upload-test
- **GitHub Pages**: https://eliasvestman-dotcom.github.io/Upload-test/

## GitHub TOS Compliance

This generator respects GitHub's limits:

| Limit | Value | Status |
|-------|-------|--------|
| Single file size | 100 MB | We stay under 50 MB |
| Repository size | 10 GB max | We target < 3 GB |
| Directory depth | 50 levels max | We use < 10 levels |
| Directory width | 3,000 files max | We stay under 50 per folder |

## Features

✅ Customizable folder depth  
✅ Customizable files per folder  
✅ Customizable folder count per level  
✅ Customizable file sizes  
✅ Safety checks for GitHub TOS limits  
✅ Progress indicators  
✅ Size calculations before generation  

## Tips

- Start small (depth: 3, folders: 3, files: 5) to test
- Increase parameters gradually
- Monitor file size — larger files upload slower
- For very large datasets (> 1 GB), consider splitting across multiple repos

## Requirements

- Python 3.6+
- Git
- GitHub repository access

---

**Generated for**: eliasvestman-dotcom/Upload-test
