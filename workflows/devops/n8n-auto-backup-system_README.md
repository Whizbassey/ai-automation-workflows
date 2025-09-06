This makes it easy to see when each backup was created.

### File Organization
Each backup folder contains:  
- One **JSON file per workflow**  
- Files named exactly like your workflows  
- Properly formatted JSON that can be imported back to n8n  

---

## Important Notes
- Backups run every **4 hours** by default (you can change this)  
- Old backup folders are automatically deleted to save space  
- Each workflow is saved as a separate JSON file  
- The backup includes all workflow settings, nodes, and connections  
- **Credentials are NOT backed up** (for security reasons)  

---

## Customization Options

### Change Backup Frequency
1. Open the **"Schedule Trigger"** node  
2. Change from **4 hours** to your preferred interval  
   - Options: every hour, twice daily, daily, etc.  

### Keep More/Fewer Backups
By default, the workflow keeps only the **latest backup**.  
- Modify the **cleanup logic** in the filter and delete nodes  
- Add conditions to keep the last **X backups** instead of just the latest  

### Change Backup Location
- Update the folder ID in both Google Drive nodes  
- Point to any folder in your Google Drive  
- You can even back up to a **shared team drive**  

---

## Troubleshooting
- **No backups created:** Check Google Drive API credentials and permissions  
- **Missing workflows:** Verify n8n API access and workflow permissions  
- **Folders not cleaning up:** Check the filter logic and folder ID settings  
- **Upload errors:** Ensure Google Drive has enough space  
- **Schedule not working:** Verify the workflow is set to **Active**  

---

## Security Notes
- Workflow **credentials are NOT included** in backups (this is intentional)  
- Only workflow structure and logic are backed up  
- You’ll need to **reconnect credentials** when restoring workflows  
- Keep your Google Drive secure since it contains your automation logic  

---

## Restore Process
To restore workflows from backup:  
1. Download the **JSON file** from Google Drive  
2. Go to **n8n > Import Workflow**  
3. Upload the JSON file  
4. Reconnect any credentials the workflow needs  
5. Test the restored workflow before activating  
