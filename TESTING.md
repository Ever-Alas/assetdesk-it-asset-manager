# AssetDesk — Manual QA Checklist

Test on the StackBlitz preview, then repeat in Chrome with VS Code Live Server.

| Test | Steps | Expected result |
|---|---|---|
| Create | Add a laptop named Test Laptop with tag IT-100 | A row appears |
| Required fields | Try saving an empty name or tag | Form rejects the entry |
| Duplicate tags | Add another item with tag IT-100 | Duplicate is rejected |
| Case-insensitive duplicate | Try it-100 | Duplicate is rejected |
| Edit | Change IT-100 owner and status | Edited values appear |
| Search | Search for IT-100 | Correct row remains |
| Filters | Filter status and type | Only matching rows show |
| Persistence | Reload in the same browser and origin | Saved rows remain |
| CSV | Export CSV and inspect in a spreadsheet | Headers and content are correct |
| JSON backup | Download a backup | Valid JSON array is saved |
| JSON restore | Import saved backup and confirm | Inventory is restored |
| Invalid import | Import malformed JSON | No current records are overwritten |
| Delete | Delete an item and confirm | Item disappears |

## Follow-up enhancements
- Accessible form feedback and keyboard testing
- Sortable table, pagination and summary views
- Explicit 'demo data' reset
- Unit tests for inventory validations
- Clear import/export warnings

## Important limitation
The inventory is stored in browser localStorage, *not GitHub*. Saving code changes to GitHub does not sync inventory records across office/home computers. Export/import JSON to move test data between browsers, without sensitive company data.
