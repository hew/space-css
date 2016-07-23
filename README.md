# Space

> Atomic classes for space.


``npm i --save space-css``



# About Space

I am a big fan of [Basscss](http://basscss.com) but recently working on a large project I decided that I needed more tools
to work with height and width.

Enter ``Space`` &mdash; a mobile-first set of atomic classes for working with height and width. It was designed to work with
Basscss, and follows the same coordinate-based mental model. 


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
You can use either the shorthand, ``xf``, or the full classname, ``x-fill``. 

There is a singler helper class for setting full screen that operates using the z-axis.


### Static Declarations

Like Basscss, ``Space`` asks you to embrace a philosophy where you declare spacing variables ahead of time and work within them.
You can use whatever spacing strategy you want.  

``Space`` comes with eight increments. You can see the defaults [here](https://github.com/hew/space-css/blob/master/index.css#L10). (Note 
that they are different from the Basscss white space defaults.)

```css
.x1 { width: var(--space-one)  }
.x2 { width: var(--space-two)  }

.y1 { height: var(--space-one) }
.y2 { height: var(--space-two) }

@media(--breakpoint-sm) {

  .sm-x1 { width: var(--space-one)  }
  .sm-x2 { width: var(--space-two)  }

  .sm-y1 { height: var(--space-one) }
  .sm-y2 { height: var(--space-two) }

}
```
etc...

### Breakpoints

``Space`` uses the same (three) default breakpoints as Basscss. 

```
@custom-media --breakpoint-sm (min-width: 40em);
@custom-media --breakpoint-md (min-width: 52em);
@custom-media --breakpoint-lg (min-width: 64em);
```


##License
MIT [Matthew Jones](http://hew.tools)
