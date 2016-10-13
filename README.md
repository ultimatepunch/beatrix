Beatrix OOSass Framework
========================

Block, Element, Adaptor
-----------------------

Basically BEM, renamed to fit in with the name BEAtrix.
However, Beatrix offers a much cleaner and legible syntax, rather than having double dash, single dashes, double underscores and single underscores all over the place. 

 - Block:
Defines a reusable component that will maintain styling wherever it is placed in the DOM body.
 - Element:
A Block-dependent part of the component which is intrinsically tied to the scope of the block.
 - Adapter:
A subversion of a component or element that varies slightly but maintains most of the original properties of block or element.

Components, which start by defining a...

 **block** class, must follow PascalCase.

    .ComponentName {
    }

**Elements** are defined by a single - (dash), and written in camelCase

    .ComponentName {
	     
        & .ComponentName-elementNameAvatar {
	    }
	    & .ComponentName-elementNameDescription {
	    }
    }

**Adapters** are defined by an underscore, and are also written in camelCase.

    .ComponentName_blueBox {
    }
or, for an Element:

    .ComponentName-elementName_adaptorName {
    }

