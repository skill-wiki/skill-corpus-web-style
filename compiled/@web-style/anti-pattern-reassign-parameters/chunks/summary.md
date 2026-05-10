# ReassignParameters [anti-pattern] v0.1.0
Treating a parameter as a mutable local — assigning to it, mutating its properties when the caller did not opt in, or using it as scratch space. The parameter binding is part of the function's contract with its callers; rewriting it in the body breaks the obvious mapping between the call site and what runs.
domain: web-style
