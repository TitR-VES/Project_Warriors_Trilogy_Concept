# World-events geography map artifact

The corrected KMZ is preserved here as six Base64 text parts because the connected GitHub write path used for this landing cannot safely transmit the 63,614-byte binary in one write.

Canonical reconstructed filename:
`PW_Post_PANDORA_WW3_World_Events_Geography_Reference_2026-08-14_rev1.kmz`

Expected SHA-256:
`18acfae12d78923615cc750574df1e5c87cf3a97245b57ac750cc7b8b91ca029`

Reconstruction (repository root, Python 3):

```python
from pathlib import Path
import base64, hashlib

parts_dir = Path('dev_src_docs/worldbuilding/geography/PW_Post_PANDORA_WW3_World_Events_Geography_Reference_2026-08-14_rev1_kmz_parts')
encoded = ''.join((parts_dir / f'part{i:02}.b64').read_text().strip() for i in range(1, 7))
data = base64.b64decode(encoded)
out = parts_dir.parent / 'PW_Post_PANDORA_WW3_World_Events_Geography_Reference_2026-08-14_rev1.kmz'
out.write_bytes(data)
assert hashlib.sha256(data).hexdigest() == '18acfae12d78923615cc750574df1e5c87cf3a97245b57ac750cc7b8b91ca029'
```

The KMZ contains the corrected KML 2.2 source map. The normalized placemark inventory and `PW-GEO-*` ontology registry can be used without reconstructing the binary.
