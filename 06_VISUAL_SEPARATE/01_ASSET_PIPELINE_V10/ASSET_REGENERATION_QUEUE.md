# ASSET REGENERATION QUEUE — V10

Primary status remains one of PASS / REGENERATE / AMBIGUOUS / MISSING.
REGENERATE is preserved history, not deletion.
FORM_VALIDATION defaults to PENDING until the real silhouette/form is explicitly validated.

| ID | Defect | Required correction |
|---|---|---|
|007|X baked|Keep shell/form; empty close well; SVG/DOM runtime|
|008|Alert pictogram baked|Keep form; remove symbol; runtime icon|
|009|Dynamic progress/state baked|Neutral rail; progress/state runtime|
|010|X + toggles baked|Keep wells; controls runtime|
|012|Bell + status dot baked|Keep wells; icon/state runtime|
|015|Invented blurred media + arrows baked|No invented media; alpha/empty media areas per job; controls runtime|
|016|Progress + Play/Favorite/Bookmark/Arrow baked|Keep alpha apertures/wells; remove states/icons|
|017|Navigation arrows baked|Keep lateral wells; runtime arrows|
|019|Arrows, Play, heart, bookmark, menu, CTA arrow baked|Remove all controls/icons; preserve candidate form|
|020|Play baked in media apertures|Remove Play triangles; runtime control|
|022|Menu chevrons baked|Neutral wells; runtime chevrons|
|023|Filter chevrons baked|Remove control pictograms|
|024|Two chevrons baked|Keep decorative wells only|
|027|Chevrons + slider handle/state baked|Remove controls/state; DOM runtime|
|031|Fake CTZ/CORTEZIA + nav/icons baked|Keep shell/wells; branding/nav/icons runtime|
|032|CORTEZIA + icons/controls baked|Remove branding/pictograms; preserve candidate form|
|033|Fake CTZ + search/close/play/favorite/arrows baked|Alpha apertures + neutral wells; all controls/branding runtime|
|034|Fake CTZ baked|Leave medallion empty; real branding runtime|
|035|Fake CTZ + chevron baked|Leave crest/action empty; runtime|
|036|Wordmark + legal links + copyright baked|Structural footer only; text/branding runtime|
|037|Cookie text + icons + buttons/close baked|Shell/wells only; DOM controls/text|
|038|Fake CTZ + X baked|Empty crest and close well; runtime branding/X|
|039|Branding, text, trash, arrow, buttons, X baked|Neutral shell only; all functional content DOM/SVG|
|040|X + status symbol baked|Neutral STATUS/ACTION wells; runtime|

## Revalidation gate
1. New version received.
2. Exact ID/job correspondence.
3. Original defect actually corrected.
4. Alpha/media apertures technically compliant.
5. No forbidden runtime content baked.
6. Cortezia DA and functional role compliant.
7. Real silhouette/form visually validated.
8. PASS only after 1→7.

If steps 1→6 pass but step 7 is pending: remain REGENERATE with FORM_VALIDATION=PENDING.


## LOT_05 — 041–050
All ten received versions are preserved as form candidates. FORM_VALIDATION=PENDING.

| ID | Defect | Required correction |
|---|---|---|
|041|Lock icon baked|Keep shell/media aperture/wells; remove lock and runtime state pictograms|
|042|Play, timeline/knob, fullscreen, favorite and states baked|Keep silhouette and alpha aperture; make all controls/states neutral runtime wells|
|043|Crown/state emblems baked|Keep medallion wells; remove crowns/state symbols; PPV-owned state runtime|
|044|Play, timeline, menu, lock and fake metadata bars baked|Keep frame/aperture/wells; empty all controls and metadata zones|
|045|Clock/state pictogram baked|Keep silhouette/wells; remove real icon/state|
|046|Dropdown chevrons and control knobs baked|Keep sculpted filter wells; remove chevrons/knobs/state|
|047|Close X, chevrons, toggles, slider, favorite/state controls baked|Keep grid and alpha apertures; neutralize all controls/states|
|048|Fake metadata/copy bars baked in runtime description area|Keep card/cover aperture/wells; leave copy zone clean and empty|
|049|Lock, Play, heart, progress/state and fake metadata baked|Keep episode shell/alpha thumbnail/wells; remove all controls/states/placeholders|
|050|Fake metadata/copy bars baked|Keep silhouette/alpha thumbnail/action wells; leave TITLE/METADATA zones neutral|

Promotion rule remains: technical correction + V10 compliance + real form/silhouette validation before PASS.
