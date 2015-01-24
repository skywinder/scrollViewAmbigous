ScrollViewAmbigous Example
==================
Example for my question on SO:
[UIScrollView + Centered View + Ambigous Scrollable Content Size + many iPhone sizes](http://stackoverflow.com/questions/26261659/uiscrollview-centered-view-ambigous-scrollable-content-size-many-iphone-si)

The initial state, with existing problems: 0a8bf35

And resolved `Has ambiguous scrollable content width` and `Has ambiguous scrollable content height` **annoying warnings** : 3b3e874


So, here is the initial state for simplest case:
==================

1. scrollView with 0 constraints to all edges
2. Button centered Horizontal and Vertical with fixed Width and Height
3. And, of course `Has ambiguous scrollable content width` and `Has ambiguous scrollable content height` **annoying warnings**.

![1](http://i.imgur.com/d5Fgmzg.png)

All, that we have to do is:
==================

- Add 2 additional constraints, for example "0" for trailing and/or bottom space for our view (in my case - UIButton)

**Important:** you have to add **trailing and/or bottom** constraints. Not "leading and top" - it's not works!

![2](http://i.imgur.com/7yEMQ7J.png)


You can check it in my example project, that demonstrating how to fix this issue: [**ScrollViewAmbigous**](https://github.com/skywinder/scrollViewAmbigous)

**P.S.**

I don't know why it works and how Xcode detect which constraint is more prioritised (because I'm not set priority for these constraints explicity), but I'll be thankful if someone explain, why it works.

Aligning multiple elements?
==================
When you want to align multiple elements, say three button in one vertical line, you'll have to set the above said additional constraints to the ***bottom most*** element. (example included)