# Learning combinations vs permutations [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://github.com/hchiam/learning-template/blob/main/LICENSE)

Just one of the things I'm learning. https://github.com/hchiam/learning

A reference: https://www.mathsisfun.com/combinatorics/combinations-permutations.html

Combinations are different from permutations. But did you know that there are actually different kinds of combinations and different kinds of permutations?

Number of: (`n` = options, `r` = choose)

1. **permutations** _with repeats_ allowed: `n^r`
2. **permutations** without repeats (if `r == n`): `n!`
3. **permutations** without repeats (if `r != n`): `n! / (n-r)!`
   - intuition: example: `5 pick 2` = `5*4`, not `5*4*3*2*1`
   - intuition: you're picking the first 2, hence `5*4`
   - intuition: `n! / (n-r)!` is just a fancy math way of getting that `5*4`
   - intuition: divide by `(unwanteds)` = `(n-r)!` = `3*2*1` in the example
4. (**combinations** = permutations but order doesn't matter)
5. **combinations** without repeats: `n! / (n-r)! / r!`
   - intuition: `(permutations) / (ways to order r)`
   - intuition: `(permutations)` = `n! / (n-r)!`
   - intuition: `(ways to order r)` = `r!`
6. **combinations** _with repeats_ allowed: `(n-1 + r)! / (n-1)! / r!`

## To-do:

Understand why there's `-1`s in the equation for **combinations** _with repeats_ allowed.

The rest of that last equation makes sense:

- `n` to be combined + `r` _repeats allowed_ = `(n + r)!` permutations
- `/n!r!` to remove the ways to order `n` items and `r` items
- both of the above give you `(n+r)! / n!r!` "combinations"

So why the `-1` on the top and bottom?
