# Space

> Atomic classes for space.


``npm i --save space-css`` 

# About Space

Space, the final frontier. 

I am a big fan of Basscss (and the addons) but recently working on a large project I decided that I needed some
more tools when it comes to declaring space. But using atomic classes to handle spacing is tricky. You could make
the argument that any static measurement should probably live in a custom class or inline styles. Maybe. This 
library is going to attempt to say, maybe not. 


## How Space Works


### Fills

Use ``fx`` or ``fy`` to fill the element's width or height (respectively)

``width`` = ``x-axis``i = ``x``
``height`` = ``y-axis`` = ``y``

``width: 100%`` = ``fill x-axis`` = ``.fx`` 
``height: 100%`` = ``fill y-axis`` = ``.fy`` 

You can use either the shorthand, (``fx``) or the full classname, ``fill-x``

But in some ways, this isn't anything new. You can use ``col-10`` to achieve ``width: 100%`` with Basscss. The reason
the fill classes exist are for non-column elements. Either class results in ``width: 100%``, but an important part of 
working with atomic classes is establishing a clear mental modal for what each class is doing, and why.


### Static Declarations

Like Basscss, Space asks you to embrace a philosophy where you declare spacing variables ahead of time and work within them.
You can use whatever spacing strategy you want.  

``Space`` comes with eight increments.

``.x1`` = ``width: var(--space-one)``
``.x1`` = ``width: var(--space-one)``
``.y2`` = ``height: var(--space-two)``
``.y2`` = ``height: var(--space-two)``
``etc...``


### Breakpoints

``Space`` uses the same default breakpoints as Basscss:

```
@custom-media --breakpoint-sm (min-width: 40em);
@custom-media --breakpoint-md (min-width: 52em);
@custom-media --breakpoint-lg (min-width: 64em);

```

etc..



### Do I Need This?

Basscss' white space API is pretty good (that's basically what this is), so if you are building a basic responsive site or page,
you might be able to get away with Basscss and efficient use of padding/margin. ``Space`` is for more complex designs that insist on
actually declaring specific widths/heights.




##License
MIT [Matthew Jones](http://hew.tools)
