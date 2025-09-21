Races
Critical section: code section that needs locks
Implementing locks: need to make sure its atomicity. Processors usually provide atomic instructions. RISC-V provides `amoswap`.
Deadlock. Lock ordering. Re-entrant locks.
Memory ordering: Compilers and CPU might change the order of instructions.
Memory barrier: Prevent reordering
Pthreads(POSIX threads)


