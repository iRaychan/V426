# KeySuite V4.26.03 UPGRADE

Apply over V4.26.02.

Fixes:
- Product Curve keeps the selected pump curve/model when Motor IE or Phase changes.
- D1 can be cleared/removed without losing the selected pump curve.
- Clearing either main Flow or Head removes active D1/system-duty markers until both values are entered again.
- D2-D6 remove controls are unchanged.

Applies to CHC C4/C6, VMS/SVM aliases and BFI/HMS. No Supabase db push is required.
