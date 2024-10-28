# Install/Build
```
./gradlew bundle
```
This will build gatk (note that you might need to install JDK 17, git lfs, etc.)

# Quick start
```
Build the GATK: ./gradlew bundle (creates gatk-VERSION.zip in build/)
Get help on running the GATK: ./gatk --help
Get a list of available tools: ./gatk --list
Run a tool: ./gatk PrintReads -I src/test/resources/NA12878.chr17_69k_70k.dictFix.bam -O output.bam
Get help on a particular tool: ./gatk PrintReads --help
```

# Run test
```
- cd /home/lhvu/bio/gatk
- ./gatk PrintReads -I src/test/resources/NA12878.chr17_69k_70k.dictFix.bam -O output.bam
```

# Output:
```
(base) lhvu@realtimeaidoe:~/bio/gatk$ ./gatk PrintReads -I src/test/resources/NA12878.chr17_69k_70k.dictFix.bam -O output.bam
Using GATK jar /home/lhvu/bio/gatk/build/libs/gatk-package-02c87bf-SNAPSHOT-local.jar
Running:
    java -Dsamjdk.use_async_io_read_samtools=false -Dsamjdk.use_async_io_write_samtools=true -Dsamjdk.use_async_io_write_tribble=false -Dsamjdk.compression_level=2 -jar /home/lhvu/bio/gatk/build/libs/gatk-package-02c87bf-SNAPSHOT-local.jar PrintReads -I src/test/resources/NA12878.chr17_69k_70k.dictFix.bam -O output.bam
16:06:44.968 INFO  NativeLibraryLoader - Loading libgkl_compression.so from jar:file:/home/lhvu/bio/gatk/build/libs/gatk-package-02c87bf-SNAPSHOT-local.jar!/com/intel/gkl/native/libgkl_compression.so
SLF4J(W): Class path contains multiple SLF4J providers.
SLF4J(W): Found provider [org.apache.logging.slf4j.SLF4JServiceProvider@530ee28b]
SLF4J(W): Found provider [ch.qos.logback.classic.spi.LogbackServiceProvider@3a3f96ab]
SLF4J(W): See https://www.slf4j.org/codes.html#multiple_bindings for an explanation.
SLF4J(I): Actual provider is of type [org.apache.logging.slf4j.SLF4JServiceProvider@530ee28b]
16:06:45.297 INFO  PrintReads - ------------------------------------------------------------
16:06:45.302 INFO  PrintReads - The Genome Analysis Toolkit (GATK) v02c87bf-SNAPSHOT
16:06:45.302 INFO  PrintReads - For support and documentation go to https://software.broadinstitute.org/gatk/
16:06:45.302 INFO  PrintReads - Executing as lhvu@realtimeaidoe on Linux v5.15.0-119-generic amd64
16:06:45.302 INFO  PrintReads - Java runtime: OpenJDK 64-Bit Server VM v17.0.12+7-Ubuntu-1ubuntu222.04
16:06:45.303 INFO  PrintReads - Start Date/Time: October 28, 2024 at 4:06:44 PM CDT
16:06:45.303 INFO  PrintReads - ------------------------------------------------------------
16:06:45.303 INFO  PrintReads - ------------------------------------------------------------
16:06:45.304 INFO  PrintReads - HTSJDK Version: 4.1.3
16:06:45.305 INFO  PrintReads - Picard Version: 3.3.0
16:06:45.305 INFO  PrintReads - Built for Spark Version: 3.5.0
16:06:45.308 INFO  PrintReads - HTSJDK Defaults.COMPRESSION_LEVEL : 2
16:06:45.309 INFO  PrintReads - HTSJDK Defaults.USE_ASYNC_IO_READ_FOR_SAMTOOLS : false
16:06:45.309 INFO  PrintReads - HTSJDK Defaults.USE_ASYNC_IO_WRITE_FOR_SAMTOOLS : true
16:06:45.310 INFO  PrintReads - HTSJDK Defaults.USE_ASYNC_IO_WRITE_FOR_TRIBBLE : false
16:06:45.310 INFO  PrintReads - Deflater: IntelDeflater
16:06:45.310 INFO  PrintReads - Inflater: IntelInflater
16:06:45.311 INFO  PrintReads - GCS max retries/reopens: 20
16:06:45.311 INFO  PrintReads - Requester pays: disabled
16:06:45.312 INFO  PrintReads - Initializing engine
16:06:45.505 INFO  PrintReads - Done initializing engine
16:06:45.535 INFO  ProgressMeter - Starting traversal
16:06:45.536 INFO  ProgressMeter -        Current Locus  Elapsed Minutes       Reads Processed     Reads/Minute
16:06:45.623 INFO  PrintReads - 0 read(s) filtered by: WellformedReadFilter

16:06:45.624 INFO  ProgressMeter -             unmapped              0.0                   493         340000.0
16:06:45.625 INFO  ProgressMeter - Traversal complete. Processed 493 total reads in 0.0 minutes.
16:06:45.675 INFO  PrintReads - Shutting down engine
[October 28, 2024 at 4:06:45 PM CDT] org.broadinstitute.hellbender.tools.PrintReads done. Elapsed time: 0.01 minutes.
Runtime.totalMemory()=285212672
```
