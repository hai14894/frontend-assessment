# exercise2

Explain why the result of `('b' + 'a' + + 'a' + 'a').toLowerCase()` is banana.

In Javascript , the operation goes from left to right

So first we have `'b' + 'a'`, which resulted to `'ba'` , since the `+` operation performs string concatenation.

Therefore we have  `'ba' + + 'a'`. Javascript will perform string concatenation in the fist `+` operation for whatever comes after it. The second `+` operator which stand in front of `'a'` will attempt to convert `'a'` into a number, which is not possible, and it will be converted to `NaN` (not a number).

So we have `'ba' + NaN`, and this + operator will again do a string concatenation to `NaN`, therefore the result is `'baNaN'`.

And finally, `'baNaN' + 'a'`, as explained above, is `'baNaNa'`, then we add method `.toLowerCase()` to it, then it becomes the string `'banana'`. 