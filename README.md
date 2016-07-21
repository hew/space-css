# Space

> Atomic classes for space.


``npm i --save space-css``



# About Space

I am a big fan of [Basscss](http://basscss.com) but recently working on a large project I decided that I needed more tools
to work with height and width directly. Enter ``Space`` &mdash; a set of atomic classes for working with height and width.


## How Space Works

### Basics 

``Space`` operates on the x, y axes. 

```css

/* 
  width = x-axis 
  height = y-axis 
*/

```

### Fills

Use ``xf`` or ``yf`` to fill the element's width or height (respectively)

```css
/* f = fill */

.xf    { width: 100%               }
.yf    { height: 100%              }
.xyf   { width: 100%; height: 100% }
.zf    { width: 100vh; 100vw;      }

```
You can use either the shorthand, ``xf``, or the full classname, ``fill-x``. 

There is a helper class for setting full screen that operates using the z-index. 


### Static Declarations

Like Basscss, Space asks you to embrace a philosophy where you declare spacing variables ahead of time and work within them.
You can use whatever spacing strategy you want.  

``Space`` comes with eight increments. You can see the defaults [here](https://github.com/hew/space-css/blob/master/index.css#L10). Note 
that they are different from the Basscss white space defaults.

```css
.x1 { width: var(--space-one)  }
.y1 { height: var(--space-one) }
.x2 { width: var(--space-two)  }
.y2 { height: var(--space-two) }a

@media(--breakpoint-sm) {
  .x1 { width: var(--space-one)  }
  .y1 { height: var(--space-one) }
  .x2 { width: var(--space-two)  }
  .y2 { height: var(--space-two) }
}
etc...
```


### Breakpoints

``Space`` uses the same (three) default breakpoints as Basscss. You can see them [here](https://github.com/hew/space-css/blob/master/index.css#L6)

```
@custom-media --breakpoint-sm (min-width: 40em);
@custom-media --breakpoint-md (min-width: 52em);
@custom-media --breakpoint-lg (min-width: 64em);
```



## Do I Need This?

Basscss' white space API is pretty good (that's basically what this is), so if you are building a basic responsive site or page,
you might be able to get away with Basscss and efficient use of padding/margin. ``Space`` is for designs that insist on
actually declaring specific widths/heights.


##License
MIT [Matthew Jones](http://hew.tools)
