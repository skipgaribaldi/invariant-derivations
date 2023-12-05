# invariant-derivations
Code to support the paper "Invariant derivations and trace bounds"

This collection of Magma scripts contains the computations that support the paper "Invariant derivations and trace bounds" by Garibaldi, Guralnick, and Rains.

The purpose of this README is to explain the contents of the magma scripts.

   * trace_base = general routines used in several of the scripts, not particularly mathematical

## Files with "inv" or "-M" in the name

The files with "inv" in the name refer to the method of invariant derivations described in the paper.

   * inv = the main routines for calculating with the method of invariant derivations
   * inv-exgroups = compute the critical values of the trace on the adjoint representations of the compact exceptional groups except for E8, relies on inv
   * inv-E8 = compute the critical values of the trace on various fundamental representations of the compact E8, relies on inv.  Has some custom code to handle the harder E8 computations
   * E8-M = contains some data for E8.  This can be recomputed using routines from inv, but it takes a little over 6 minutes on my laptop
   * xx-M = same but for the compact group of type xx

## Files with "break" in the name

   * break-base = the main routines for calculating via symmetry breaking
   * break-exgroups = compute the minimum of the trace and the highest short root representations for the compact exceptional groups other than E6
   * break-e6 = compute the minimum of the trace for the compact E6
