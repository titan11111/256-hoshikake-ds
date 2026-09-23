# LEARNINGS

## 2026-09-23 公開前

- 入口を `index.html` にし、旧名 `hoshikake-ds.html` は転送だけ残した
- three.js r128 は CDN をやめ、同梱の `three.min.js` を読むようにした
- ベストタイムのキー `hoshikake-best` は改名していない
- viewport のピンチズーム抑止と、ダブルタップ・長押しメニューの抑止を入れた
- harness: PASS（Canvas 256×192、61 RAF/秒、通信量 0.60MB）。証跡 `docs/harness-reports/256-hoshikake-ds-2026-09-23T06-31-31-199Z.md`
