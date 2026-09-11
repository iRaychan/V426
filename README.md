# KeySuite V4.26.01 FULL CLEAN

Built from **V4.25.14 Full Clean**.

## V4.26.01 changes

- Motor **IE4 + IE5** catalog rebuilt from `004 - Motor 260811 - V1.2.xlsx`.
  - IE4 2 Pole: **31** models (0.5–500 HP)
  - IE4 4 Pole: **31** models (0.5–500 HP)
  - IE5 2 Pole: **26** models (1–420 HP)
  - IE5 4 Pole: **27** models (0.75–420 HP)
- The Supabase refresh now targets **`public.ks_products_motor` directly**. It no longer guesses Motor table/key columns.
- Canonical database key: **`efficiency_class + hp + pole`**; `model` remains independently unique.
- Existing motor `id`, `source_row`, source prices and rarity are preserved on existing business-key rows.
- Conflicting legacy model-name rows are retained but renamed and made inactive; they are not deleted.
- Missing IE4/IE5 business-key rows are inserted with source prices starting at 0.
- Full-screen desktop layout remains the normal KeySuite layout.
- At split/half-screen widths (621–1000 px), KeySuite uses the compact vertical sidebar and compact Flow / Head controls.
- Phone layout remains stacked below 620 px.

## Supabase

Migration included:
`supabase/migrations/20260911172200_v42601_motor_ie4_ie5_refresh.sql`

The same SQL is also included at the package root as:
`V42601_MOTOR_IE4_IE5_SQL_EDITOR.sql`

Run `VERIFY_MOTOR_IE4_IE5.sql` after the migration.

Expected exact active coverage: **IE4 2P=31, IE4 4P=31, IE5 2P=26, IE5 4P=27**.

No Edge Function deployment is required for this release.
