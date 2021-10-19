# Reed a command line tool for protecting files from spontaneous data corruption
___

## Motivation

When you copy valuable files to a cold storage like a USB drive or en external HDD, for archiving,
how do you know that the files you are going to copy back when needed are exactly the same. And more
importantly, what you are going to do if some files were changed.

Studies have shown that HDD and SSD types of storage are prone to spontaneous data corruptions. These
corruptions are very rare, but when they happen there is a chance you can lose important data. Cloud
storage systems, like S3, solve this problem by keeping at least 3 copies of data, generating checksums
of blocks of data and regularly verifying these checksums.

This tool provides yet another way. It allows creating a recovery file for your files. The bigger the
file, the more you can recover when a data corruption happens. The recovery file contains checksums
and redundancy information that allows future recovering. The principle is based on Reed-Solomon error
correction codes, specifically adjusted to handle corruption of contiguous data blocks.

## Usage


