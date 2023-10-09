![image](https://github.com/Ali-Elbana/filesystems/assets/97269796/da1d0d03-b603-41c0-82af-3b8028d7a833)# filesystems

## Hardware needed
1. SDCARD or USB Flash

![Screenshot 2023-09-27 at 8 24 00 AM](https://github.com/embeddedlinuxworkshop/filesystems/assets/139722851/521b5456-4243-485e-94ba-d55dd6e69f2d)

## Software Needed.
1. gparted.

-------------------------------------------------------

## Requirements.

1. Make at least two partitions on your SD-CARD using *gparted*.
2. Create for each partitions filesystem ( first one *ext4* & second one *ext2* ).
3. Mount two partitions on your root filesystem.
4. Add some files inside each one.
5. reboot your machine.
6. check if mounting points still exists, *it should not*.
7. Make the *ext4* persistance by adding /etc/fstab file ----> (search how you can do that).
8. reboot your system.
9. Check if the *ext4* is mounted.
---------------------------------------------------------
## Solution.

**Enviroment**: I use flash drive with size of 8 Gigabytes:

  ![image](https://github.com/Ali-Elbana/filesystems/assets/97269796/6612c0f2-4be2-4079-9622-ef27a01a490d)

**Firstly**, I want to unmount the mounted partition:

  ![image](https://github.com/Ali-Elbana/filesystems/assets/97269796/3caefacc-8736-4973-92fa-deddf15bd772)
  
  ![image](https://github.com/Ali-Elbana/filesystems/assets/97269796/cc5d8957-ffe5-4be3-a4b9-dc776d541f56)

#### 1-Make at least two partitions on your Flash using gparted:
#### 2-Create for each partitions filesystem ( first one ext4 & second one ext2 ):

  ![image](https://github.com/Ali-Elbana/filesystems/assets/97269796/fd23a03f-d116-4c29-97fe-bbadefc3e62d)
  
  ![image](https://github.com/Ali-Elbana/filesystems/assets/97269796/d619f64f-8ff5-43b6-b837-fd28b2d9c41e)


#### 3-Mount two partitions on your root filesystem:

- First, I want to create two directories for each partition int the root:

    ![image](https://github.com/Ali-Elbana/filesystems/assets/97269796/f081b7e5-9b12-49c9-8f0c-d755bc10aeb4)

- Then, I want to mount each partition to these folders:

  ```BASH
  sudo mount -t ext4 /dev/sdc1 /flash-p1
  sudo mount -t ext2 /dev/sdc2 /flash-p2
  df -h
  ```
    ![image](https://github.com/Ali-Elbana/filesystems/assets/97269796/ba49d34c-653e-4024-86f0-7fe9bcc0ddac)

#### 4-Add some files inside each one:

  ![image](https://github.com/Ali-Elbana/filesystems/assets/97269796/0e664ec9-a101-4964-86de-41bf682b2b48)

#### 5-reboot your machine and check if mounting points still exists, it should not:

  ![image](https://github.com/Ali-Elbana/filesystems/assets/97269796/853be18b-3bbe-41c8-8d7c-b03977698c40)

![image](https://github.com/Ali-Elbana/filesystems/assets/97269796/702a8351-c556-4c1a-8c7b-f45c708430ec)

#### 6-Make the ext4 persistance by adding /etc/fstab file:

![image](https://github.com/Ali-Elbana/filesystems/assets/97269796/9c97119b-b75e-446c-8726-7502b31491f5)

#### 7-reboot your system and Check if the ext4 is mounted:



















