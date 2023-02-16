# SFQ-Ranking

Superconductor electronics offer the potential to perform computation at tremendous speeds and energy savings but suffer from high buffering and splitting hardware overhead. Replicating SFQ pulses requires active hardware, which increases energy consumption, JJ count, and signal skew. Moreover, the hardware used for buffering and splitting purposes serves the same purpose---to maintain signal fidelity.

Our goal in this work is to reduce these overheads by using JJs at the cell boundaries to increase the number of outputs that a single logic cell can drive. We do so by assigning number labels that we call *rank* to discrete critical currents in a chosen range, and establish rules for multiple-output connections between cells with these critical current baselines. We show that:
* superconductor cells can directly drive multiple outputs without observed bias margin reduction compared to cases that use conventional splitters, with careful critical current tuning,
* connections between cells can be easily defined in a way that allows for potential circuit optimizations,
* the resulting design methodology can allow 10-20% savings in the total JJ count.

To verify and evaluate our idea we built and simulated RSFQ circuits for various test cases and example 2-bit KSA designs.

For more information and a detailed description of this work please read our paper.

### Package Contents
* *RankingR3_SecIV_Netlists/* RSFQ Spectre netlists for test cases in Section IV-A of the corresponding paper. 
* *adder-designs/* RSFQ Spectre netlists for example 2-bit KSA adder designs in Section IV-B of the corresponding paper.

This work is currently under review for a regular issue of the IEEE Transactions of Applied Superconductivity journal. Cadence Virtuoso (maestro) was used for simulation with Virtuoso version 6.1.8-64b (ip-172-18-22-57), Sub version: IC6.1.8-64b.83.

Netlists were designed using the MIT-LL 2020 PDK for the SFQ5ee 10 kA/cm2 process. The corresponding model files are not included; however, it is easy to replace these model references with custom ones for SPICE simulation, provided that the rest of the file is also modified to meet the required SPICE format. To do make this substitution, replace the line [include "<path/to/model/files>"] with one that references the desired model/model files.

In most cases, the original DC to SFQ converter used to acquire the results shown in the paper is one that is proprietary. For the purposes of publishing these designs, this converter has been swapped for the publicly-available version from Stonybrook (http://www.physics.sunysb.edu/Physics/RSFQ/Lib/AR/dcsfq.html). It is not expected that this change will result in major changes to performance or simulated bias margins; however, exact simulation results may vary.

There are no restrictions on these designs; however, it is requested that design reuse be properly attributed to the corresponding designer/author.

###References:

[1] Volk, J., Tzimpragos, G., Wynn, A., Golden, E. and Sherwood, T., 2022. Low-Cost Superconducting Fan-Out with Repurposed Josephson Junctions. arXiv preprint arXiv:2206.07817.

###Others:

Link to the SFQ Ranking Github: https://github.com/UCSBarchlab/SFQ-Ranking

###Contact:

For general questions feel free to reach out to Archlab @ UCSB.

For immediate help with SFQ0-Ranking, please correspond with Jennifer Volk (jevolk@ucsb.edu). Happy designing!
