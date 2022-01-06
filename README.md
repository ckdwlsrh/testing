# testing


    I/O Path Testin: One should focus on complete i/o path including block allocation, block de-allocation, in memory operations, cache semantics, disk I/Os etc.,
    Metadata I/O path testing: Since metadata plays a very important role for file I/Os, it’s equally important to design test cases based on different meta I/O operations.
    
    Data fragmentation testing: Designing and executing test cases around data fragmentation will provide a good insight as how file system behaves with different workloads when data is heavily or sparingly fragmented.
    
    Meta fragmentation testing: Meta fragmentation often turns out to be I/O bottleneck and this might impede the overall performance of the file system. So, considering different meta fragmentation scenarios along with different data streams and workloads patterns help in evaluating file system behavior.
    
    Data Dedupe testing: If the file system supports de-dedupe (which most of the commercially available file systems do as part of data reductions), it’s highly recommended to consider different scenarios by ingesting different dedupe ratios in the data streams which would closely mimic the customer representative data. Also, due considerations is to be given if the appliance is a generic storage appliance or backup storage appliance.
    
    Data Compression testing: If file system compression logic is enabled, good to verify with many different compression logic that the file system supports and this would help to evaluate which one best suits with the file system offerings.
    
    Data/meta Integrity check: Since maintaining data integrity is the first and foremost objective of any file system, it’s very much essential to design test plans around file system integrity check. All most all file systems has various integrity check mechanisms viz., ZFS uses checksum method internally to maintain integrity of each block allocated. There are many tools available to do the integrity check e.g., fsck is one of them which comes with Linux
    
    RAID type consideration: In case file system offers different RAID levels, test plan should cover different RAID levels with different disk types (e.g., HDD vs SSD) and also need to consider different volume sector sizes and disk sector sizes ( e.g., 512 byes vs 4KB).
    
    Stress and Load testing : File system will work fine and as expected under normal scenarios with usual workloads. However, this is not true in the real world as there are always extreme situations. So, it’s important to put file system under stress and load tests. So, consideration should be on good stress and load test plans and executions. Also, one can consider some of the most suitable tools such as Load Dynamics, iometer, vdbench, jetstress, etc., targeting different data streams and workload patterns and running them over longer period of time. Also, as part of stress testing, one should consider injecting negative test scenarios, e.g., removing one of the disks under heavy I/O and observing the file system and overall system behavior.
    
    Performance testing: Everyone is concerned about performance and no one likes it if system under performs. A solid performance test plan around file system will help in analyzing file system behavior and overall storage system performance, since most of the time a file system’s poor performance is heavily taxed to overall system performance and hence eventually impacts the economics of scale in business. Again, performance testing is a vast area and care must be taken in considering specific and important criteria while evaluating file system performance testing and most importantly the testing efforts should not go haywire.

https://it-serial.tistory.com/51
