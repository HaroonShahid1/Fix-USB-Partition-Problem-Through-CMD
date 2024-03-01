# USB Drive Partitioning and Cleaning

This guide provides instructions on how to remove two partitions and clean a USB drive using the command line interface (CMD) in Windows.

## Windows (Command Prompt):

1. **Open Command Prompt:**
   - Press `Win + X` and select "Command Prompt" or "Command Prompt (Admin)."
   - Alternatively, press `Win + R`, type `cmd`, and press Enter.

2. **Run Diskpart:**
   - Type `diskpart` and press Enter. 

3. **List Disks:**
   - Type `list disk` and press Enter to display a list of all connected disks.

4. **Select the USB Drive:**
   - Identify your USB drive based on its size. Use the command `select disk X` (replace X with the appropriate disk number for your USB drive).

5. **List Partitions:**
   - Type `list partition` and press Enter to view a list of partitions on the selected disk.

6. **Delete Partitions:**
   - For each partition you want to delete, type `select partition X` (replace X with the partition number), then `delete partition` and press Enter.

7. **Clean the Disk:**
   - After deleting all partitions, type `clean` and press Enter. This removes all partitions and data from the disk.

8. **Create a New Partition:**
   - Type `create partition primary` and press Enter to create a new primary partition.

9. **Format the USB Drive:**
   - Type `format fs=ntfs quick` (or `format fs=fat32 quick` if you prefer FAT32) and press Enter to format the newly created partition.

10. **Assign a Drive Letter:**
    - Type `assign` and press Enter to assign a drive letter to the USB drive.

11. **Exit Diskpart:**
    - Type `exit` and press Enter to exit the Diskpart utility.

After completing these steps, your USB drive should be cleaned, with a single partition formatted and ready for use.

**Note:** Be cautious while using Diskpart, as it performs operations directly on your storage devices and can lead to data loss if not used carefully.
