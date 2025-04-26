# Analysis-of-the-Disk-Structure-using-Sleuth-Kit
## AIM:
To analyze the disk structure of a given disk image using Sleuth Kit tools in Kali Linux.

## DESIGN STEPS:
## Step 1:
Obtain or create a disk image file (e.g., disk.dd) to analyze. Open the terminal in Kali Linux.

## Step 2:
Use Sleuth Kit tools like mmls, fsstat, and fls to examine the partition layout, file system details, and file listing.

## Step 3:
Interpret the output of the tools to understand the disk structure, including partitions, sectors, and files.

## PROGRAM:
Sleuth Kit Disk Analysis Commands

✅ Option 1: Create a Sample Disk Image (for Testing)

Let’s create a 10MB blank disk image and simulate file system activity:

```
cd ~/Downloads

# Step 1: Create an empty disk image
dd if=/dev/zero of=disk.dd bs=1M count=10

# Step 2: Format it with a file system (like FAT32)
mkfs.vfat disk.dd
```

## OUTPUT:

![435890092-48ad4510-e6d3-42cc-a6f7-a5453af7e6a9](https://github.com/user-attachments/assets/38402af4-39db-4a51-9518-573ca310c30a)


## Create Disk

![435590051-486b446a-0c92-4841-a095-3980000c3fc8](https://github.com/user-attachments/assets/8739f746-485b-4f73-a5af-31280b3cffa9)


## mmls

```
mmls disk.dd
```

## fls

```
fls -f fat -o 0 disk.dd
```

![435591750-85967a1e-38ab-4281-aa16-820b2cfa7479](https://github.com/user-attachments/assets/570ead96-1fd9-4834-ac98-42530ac39c43)

![435593232-36499cfc-15f3-4b86-8023-7876a2d5df25](https://github.com/user-attachments/assets/86d2a644-2f80-4428-85ec-2efc03e16702)

![435596459-1972eea0-f2aa-471e-8cc7-83e1279f38eb](https://github.com/user-attachments/assets/5dd5ec7d-f9f8-4475-a018-a4bef8cb4382)

![435593467-2f3834c6-b0da-45d9-a207-c1afc7937b3c](https://github.com/user-attachments/assets/83a87658-c58b-4a01-b492-91f5f57bfa86)


## RESULT:
The analysis was performed successfully using Sleuth Kit, and the disk structure was understood in detail.
