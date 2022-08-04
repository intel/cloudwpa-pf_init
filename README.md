DISCONTINUATION OF PROJECT.

This project will no longer be maintained by Intel.

Intel has ceased development and contributions including, but not limited to, maintenance, bug fixes, new releases, or updates, to this project. 

Intel no longer accepts patches to this project.

If you have an ongoing need to use this project, are interested in independently developing it, or would like to maintain patches for the open source software community, please create your own fork of this project. 
========================================================================
README for Intel(R) pf_init Package

February 2018
========================================================================


Contents
========

Contains C source code module for Intel X710 NIC initialization/configuration daemon.

Overview
========

This application configure the NIC and all VF's on NIC.
VF's configured in this application will used in VNF-D and VNF-C like NIC.
This need for circumvent kernel network stack and improve speed packet transmitted


How to build
============

For build your must define environment variable RTE_SDK - path to your DPDK
run make

How to run
==========

./build/pf_init -l 2 -w phy1 --socket-mem 256,256 -- -p 0x1 -m 00:00:00:00:00:05

before options  '--' standart dpdk options (see dpdk.org documentation for details).
after
-p enable port mask. Mask of phy to configure
-m mac address of first device/VF


Legal Disclaimer
================

THIS SOFTWARE IS PROVIDED BY INTEL"AS IS". NO LICENSE, EXPRESS OR
IMPLIED, BY ESTOPPEL OR OTHERWISE, TO ANY INTELLECTUAL PROPERTY RIGHTS
ARE GRANTED THROUGH USE. EXCEPT AS PROVIDED IN INTEL'S TERMS AND
CONDITIONS OF SALE, INTEL ASSUMES NO LIABILITY WHATSOEVER AND INTEL
DISCLAIMS ANY EXPRESS OR IMPLIED WARRANTY, RELATING TO SALE AND/OR
USE OF INTEL PRODUCTS INCLUDING LIABILITY OR WARRANTIES RELATING TO
FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR INFRINGEMENT
OF ANY PATENT, COPYRIGHT OR OTHER INTELLECTUAL PROPERTY RIGHT.
