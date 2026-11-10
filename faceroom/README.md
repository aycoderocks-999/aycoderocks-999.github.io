# FaceRoom AI (browser demo)

Upload event photos, group them by person, and find every photo of you from a selfie.
Everything runs in the browser with face-api.js (MIT): detection (SSD MobileNet v1),
68-point landmarks, and 128-d face embeddings compared by Euclidean distance.
Photos are stored only in the visitor's own browser (IndexedDB), never uploaded.

Matching thresholds (in `index.html`): `CLUSTER_DIST = 0.5` for grouping people and
`SEARCH_DIST = 0.55` for selfie search. Lower is stricter.

Host on any static host (GitHub Pages works). Serve over http(s); it will not load models from `file://`.
