# DefaultParametersNotMutateArgs [rule] v0.1.0
Express defaults in the parameter list with `=`. Do not patch missing values inside the body with reassignment, `||`, or by writing into `arguments`. Default-parameter syntax keeps the function signature self-documenting and makes the default value visible at the call boundary.
domain: web-style
