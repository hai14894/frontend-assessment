### Exercise 1

* exercise1 -Desktop view
<img width="1293" alt="Screen Shot 2023-02-08 at 1 57 42 pm" src="https://user-images.githubusercontent.com/61439970/217417409-7e22e521-c197-4837-b7bb-28977406c99e.png">

* exercise1- Mobile View

<img width="634" alt="Screen Shot 2023-02-08 at 1 57 52 pm" src="https://user-images.githubusercontent.com/61439970/217417423-dce62d5a-5d05-4a45-a448-bdafb1cb33d6.png">

### Exercise 2
Desktop/ Tab view
<img width="1119" alt="Screen Shot 2023-02-08 at 1 48 30 pm" src="https://user-images.githubusercontent.com/61439970/217416646-4b7c052f-6eff-4f3d-9b02-f800b8c5cb61.png">

Mobile/ Accordion view
<img width="549" alt="Screen Shot 2023-02-08 at 1 48 19 pm" src="https://user-images.githubusercontent.com/61439970/217416517-bc9a5746-0dc3-4da2-aa7f-cd9ba2485147.png">

The breakpoint for mobile view on both project is 1000 px.
###### Bonus points
* Improve the user experience with meaningful animations/transitions,  Design and styling.
  I have styled the view and button (which have the normal and active state). I also added a fade in/ out transition on the Mobile/ Accordion view.
* Explain why the result of `('b' + 'a' + + 'a' + 'a').toLowerCase()` is `banana`.
In Javascript , the operation goes from left to right

So first we have `'b' + 'a'`, which resulted to `'ba'` , since the `+` operation performs string concatenation.

Therefore we have  `'ba' + + 'a'`. Javascript will perform string concatenation in the fist `+` operation for whatever comes after it. The second `+` operator which stand in front of `'a'` will attempt to convert `'a'` into a number, which is not possible, and it will be converted to `NaN` (not a number).

So we have `'ba' + NaN`, and this + operator will again do a string concatenation to `NaN`, therefore the result is `'baNaN'`.

And finally, `'baNaN' + 'a'`, as explained above, is `'baNaNa'`, then we add method `.toLowerCase()` to it, then it becomes the string `'banana'`. 
