---
tags:
  - BenhHoc
TrieuChung:
  - "[[Đau bụng]]"
  - "[[Nôn ói]]"
---
## Chẩn đoán phân biệt
```dataview
TABLE
	TrieuChung
FROM #BenhHoc
WHERE TrieuChung
FLATTEN TrieuChung as ss
WHERE contains(this.TrieuChung, ss) AND file.name != this.file.name
```
