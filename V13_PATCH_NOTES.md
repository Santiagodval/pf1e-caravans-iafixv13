# pf1e-caravans v13 patch notes

This is a best-effort compatibility patch for Foundry VTT v13 / PF1e 11.x.

Changes:
- Updated module compatibility metadata to Foundry v13.
- Fixed manifest custom document type IDs to match the module's registered types:
  - `pf1e-caravans.caravan`
  - `pf1e-caravans.equipment`
  - `pf1e-caravans.wagon`
  - `pf1e-caravans.traveler`
  - `pf1e-caravans.feat`
- Replaced legacy global helpers with `foundry.utils.*` helpers.
- Added guards around libWrapper / PF1e CreateDialog hooks so the module does not hard-crash if APIs differ.
- Added safer traveler actor UUID handling.
- Added null-safe cargo weight/unit calculations.

Known limitations:
- This does not guarantee every caravan sheet workflow is fully compatible with PF1e v13.
- Existing caravan actors/items from old worlds may still need migration or recreation.
- Test in a throwaway world before using in your live campaign.
