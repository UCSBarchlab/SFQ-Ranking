# SFQ-Ranking

This repository contains all Spectre netlists used for the simulated experiments in the paper "Low-Cost Superconducting Fan-Out with Cell Ic Ranking" (https://arxiv.org/abs/2206.07817). It is currently under review for a regular issue of the IEEE Transactions of Applied Superconductivity journal. Cadence Virtuoso (maestro) was used for simulation with Virtuoso version 6.1.8-64b (ip-172-18-22-57), Sub version: IC6.1.8-64b.83.

Netlists were designed using the MIT-LL 2020 PDK for the SFQ5ee 10 kA/cm2 process. The corresponding model files are not included; however, it is easy to replace these model references with custom ones for SPICE simulation, provided that the rest of the file is also modified to meet the required SPICE format. To do make this substitution, replace the line [include "<path/to/model/files>"] with one that references the desired model/model files.

In most cases, the original DC to SFQ converter used to acquire the results shown in the paper is one that is proprietary. For the purposes of publishing these designs, this converter has been swapped for the publicly-available version from Stonybrook (http://www.physics.sunysb.edu/Physics/RSFQ/Lib/AR/dcsfq.html). It is not expected that this change will result in major changes to performance or simulated bias margins; however, exact simulation results may vary.

There are no restrictions on these designs; however, it is requested that design reuse be properly attributed to the corresponding designer/author.

For questions, comments, etc. please correspond with Jennifer Volk (jevolk@ucsb.edu). Happy designing!
