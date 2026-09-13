# KeySuite V4.26.07 FULL CLEAN

Baseline: V4.26.05.

Changes:
- Fixes KeyBot selling-series routing so `CHC` searches assigned B.G.Reich CHC C4/G1 and C6/G2 products only; TESK SVM and OEM VMS no longer leak into CHC results.
- Accepts `CHC G1` as `CHC C4` and `CHC G2` as `CHC C6`, with each alias hard-scoped to its matching hydraulic generation.
- Routes `SVM` to assigned SVM series, `VMS` to assigned VMS series, and an assigned Brand plus duty to all eligible series under that Brand.
- Keeps candidate ranking by the smallest suitable motor kW, followed by efficiency and selector rank.
- Displays Speed as Hz first, then rpm. Enhanced output uses `Max 60 Hz · 3480 rpm` in KeySelector and KeyBot PDFs.
- Retains all V4.26.05 optimized KeyBot PDF assets and deployment-size fixes.

No new Supabase database migration is required.

Deployment order:
1. Upload/deploy the V4.26.07 web files.
2. Redeploy the `telegram-webhook` Edge Function.
