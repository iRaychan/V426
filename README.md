# KeySuite V4.26.02 UPGRADE

Upgrade baseline: V4.26.01.

Copy the contents of this folder over the existing V4.26.01 deployment, preserving the same relative paths.

## Changes
- Global Page 2 Motor V1.2 lookup for CHC C4/C6, VMS/SVM, BFI/HMS and ES.
- IE1 lookup corrected.
- IE4 and IE5 technical values now come from the shared Motor V1.2 master.
- ES now offers IE5 and supports the same shared lookup for 2P/4P.
- Half-screen / split-view behavior from V4.26.01 is unchanged.

No new Supabase migration or edge-function deployment is required.
