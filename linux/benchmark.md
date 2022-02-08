opensuse:
zypper in sysbench

fedora:
dnf install sysbench

cpu benchmark:
sysbench --test=cpu run

memory benchmark:
sysbench --test=memory run

I/O Benchmark:
sysbench --test=fileio --file-test-mode=seqwr run
