---
tags:
  - BenhHoc
TrieuChung:
---
## Chẩn đoán phân biệt
```dataview
TABLE rows.ss AS "TrieuChung"
FROM #BenhHoc
WHERE TrieuChung
FLATTEN TrieuChung as ss
WHERE contains(this.TrieuChung, ss) AND file.name != this.file.name
GROUP BY file.link
```
