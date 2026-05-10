# ConsistencyWithinCodebase [principle] v0.1.0
Within one codebase, the same problem should be solved the same way. When two reasonable conventions exist, pick one and apply it everywhere. The cost of mixing is real: the reader cannot tell when a different choice carries information versus when it is just whoever-typed-it-first preference, so they have to slow down on every line.
> Local consistency outranks personal preference. If the existing code uses arrow functions everywhere, the new arrow function is correct even if you would have written `function`. If the codebase imports from `./lib`, do not introduce `./lib/index` for the same target. Match what is there. Change conventions deliberately and across the whole codebase, not file-by-file.
domain: web-style
