- New feature: Userfields
  - Attach any custom field to any entity (Products, Locations, Euqipment, etc.)
  - Userfields can have types (Text, Number, Date, etc.)
  - Will be shown / can be filled on the edit page of the corresponding entity and will also optionally show in the corresponding tables (inclcudes overview pages)
  - => Can be configured under Master data / Userfields
- General improvements
  - The "expires soon" or "due soon" days (yelllow bar at the top of each overview page) can now be configured
    - => New settings page for each area under the settings icon at the top right
- Stock improvements
  - It's now possible to have multiple / named shopping lists
    - Automations still use the default shopping list and also the default shopping list cannot be deleted
  - More information on the product card like "Spoil rate" or "Average shelf life"
  - It's now possible to set a price for added products during inventory
  - It's now possible to customize the default amount for purchase/consume (see stock settings under the settings icon on the top right)
- Chores improvements
  - New recurrence patterns - chores can now also be "scheduled" to repat daily/weekly/monthly
- New translations: (thanks all the translators)
  - Swedish (demo available at https://demo-sv.grocy.info)
  - Polish (demo available at https://demo-pl.grocy.info)
- Internal improvement: Localizations are now handled via gettext, both on server and client side
  - Mainly to properly handle languages with more than 2 plural forms
  - This involved some string changes which results in a needed (re)translation of about 20 strings (excluding demo data)
  - Also applies to quantity units, n-plural forms can be entered on the quantity unit edit page
  - It's not required to install the PHP gettext extension, on both, server and client, managed implementations of gettext are used ([oscarotero/Gettext](https://github.com/oscarotero/Gettext) & [oscarotero/gettext-translator](https://github.com/oscarotero/gettext-translator))
- Some other small fixes and improvements
  - The "Add as barcode to existing product" productpicker workflow failed to add the barcode to the given product
  - Recipes can now be filter by stock availability
  - Added a feature flag (`config.php` setting) to also be able to hide all stock related UI elements and routes