## Definition
Hard Disk Drive (HDD) is a magnetic storage that uses rotating platters, an actuator arm, and a magnetic head (similar to a record player)

HDD is very goof at writing a continuous amount of data
HDD is not great for writing many small reads and write (think of the arm of the record player having to lift up and down and move around)

- Better for Throughput
- Has physical moving part

RPMs (revolutions per minute)
- The speed at which the drive's platters spin 
- Faster RPMs means faster access times
- Slower RPMs means better cost-savings 


1. 7200 RPM Drives:
These are standard for desktop and high-performance external drives, offering a good balance of performance, cost, and power consumption

2. 5400 RPM Drives:
Often used in laptops, external hard drives, and applications where lower power consumption and heat are priorities over top performance

3. 10000 RPM Drives:
Mostly found in enterprise environments or high-end workstations where performance is critical, through these are less common today due to the rise of solid-state drives (SSDs)

### RAID
Redundant array of independent disks (RAID) is a data storage virtual technology for magnetic disks (not magnetic tape) to improve fault tolerance

RAID combines multiple physical volumes into one logical group, storing redundant data across disks

Since HDD has physical moving parts they are more prone to wear compared to SSD. 

- RAID 0 (Striping)
    - No redundancy; data is split across disks for high performance
    - Increases speed and capacity but offers no fault tolerance
    - Minimum of 2 disks required

- RAID 1 (Mirroring)
    - Data is duplicated on two or more disks, offering high redundancy
    - If one disk fails, data is still accessible from another
    - Requires at least 2 disks

- RAID 5 (Striping with Parity)
    - Combines striping and parity for both speed and data protection
    - Can withstand the failure of one drive without data loss
    - Requires at least 3 disks

- RAID 6 (Striping with Double Parity)
    - Similar to RAID 5 but with double parity, allowing it to survive the failure of two disks
    - Requires at least 4 disks

- RAID 10 (1 + 0)
    - A combination of RAID 1 and RAID 0, offering redundancy and increase performance
    - Requires a minimum of 4 disks 