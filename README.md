# Cooking Hub
Save path: C:/MarvelApps/cookinghub/README.md

Live (once pushed): https://smarvel1963-ops.github.io/cookinghub/ - app #11 of the Marvel Corp Hub family (Scott 2026-11-15: his
Recipe Hub boards, "Yes, build it", then "maybe should be clalled cooking hub" - Google Play already has a "Recipe Hub: Easy Recipes
meal"). Boards + notes: C:/MarvelApps/docs/recipehub_design_2026-11-15/ (README.md, RECIPE_SOURCES_AUDIT_2026-11-15.md).

This repo is Cooking Hub's OWN shell: index.html, manifest.json, icons, sw.js and privacy.html. The app itself is the shared Hub
engine in the Day Hub repo, run with window.DH_MODE = "cooking" plus cookbook.js (the built-in recipes), cooking.js and
cookingtiles.css (Cooking Hub's two looks, loaded only here).

- Two looks the cook picks: Magical Kitchen (storybook kitchen, chef fox) and Grandma's Recipe Box (gingham, binder, index tabs).
- Screens: Home, Dinner Finder ("Magic Meal Finder" - a plain match, no AI), recipe page (servings scale the amounts; Ingredients /
  Steps / Chef's Tips; Watch the video for recipes from creators' videos), Cook Along (one step at a time, timers, the phone's own
  voice, screen stays on), My Pantry (use-by), This Week's Table + Grocery List, My Cookbook, Write My Recipe (+ Scan an Old Recipe =
  a photo of the card), Rate a Recipe, The Blue Ribbon Recipes (your own ratings, review-count-weighted), More.
- Own data on the phone (cookinghub.v1, S.ck); photos in IndexedDB (cookinghub.photos), never in the backup, emptied by Erase.
  Private Family Recipes never leave the phone (not in Share, not in Ask).
- Reminders: tonight's planned dinner at 3 PM; a pantry item the day before and the morning it expires.
- Icons: the chef fox, drawn in code (cooking.js ckFox) and rendered by docs/recipehub_design_2026-11-15/make_cookinghub_icons.py.
- Release order: push THIS repo first (and turn on GitHub Pages), then the Day Hub repo.
- Tests: the Day Hub repo (python tests/test_cooking.py; plus tests/run_tests.py for the whole engine).
