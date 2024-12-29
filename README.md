# Code to support the paper "Invariant derivations and trace bounds" arXiv:2312.03101

This collection of Magma scripts contains the computations that support the paper "Invariant derivations and trace bounds" by Garibaldi, Guralnick, and Rains.

The purpose of this README is to explain the contents of the magma scripts.

## Description of some files

   * trace_base = general routines used in several of the scripts, not particularly mathematical
   * weyl-D4-E6 = Computations regarding specific elements in the normalizer of a maximal torus for types D4 and E6 used in the proof of Lemma 15.4 
   * bad-char = Check whether the module of invariant derivations for type A is free at the identity, over a field of prime characteristic, see Remark 5.13 in the paper

## Files with "inv" or "-M" in the name

The files with "inv" in the name refer to the method of invariant derivations described in Part I of the paper.

   * inv.magma = the main routines for calculating with the method of invariant derivations
   * inv-exgroups.magma = compute the critical values of the trace on the adjoint representations of the compact exceptional groups except for E8, relies on inv
   * inv-fund-reps.magma = compute the minimum value of the trace (somewhat easier than all critical values) for a fundamental representation, assumed to be of G2, F4, or E8, may fail for other groups
      * inv-F4.magma = use the above to compute the minimum of the trace on all fundamental representations of F4
      * inv-F4.out = output of the above
      * inv-E8.magma = substitute E8 in for F4 in inv-F4.magma to compute fundamental reps of E8
   * E8-M.magma = contains some data for E8.  This can be recomputed using routines from inv, but it takes a little over 6 minutes on my laptop
   * xx-M.magma = same but for the compact group of type xx

## Files with "break" in the name

The files with "break" in the name refer to the method of symmetry breaking as in Part II of the paper.

   * break-base.magma = the main routines for calculating via symmetry breaking
   * break-exgroups.magma = compute the minimum of the trace and the highest short root representations for the compact exceptional groups other than E6
   * break-e6.magma = compute the minimum of the trace for the compact E6
