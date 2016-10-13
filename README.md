Beatrix OOSass Framework
========================

**Block, Element, Adaptor**

 - Block:
Defines a reusable component that will maintain styling wherever it is placed in the DOM body.
 - Element:
A Block-dependent part of the component which is intrinsically tied to the scope of the block.
 - Adapter:
A subversion of a component or element that varies slightly but maintains most of the original properties of block or element.

Syntax:
Components, which start by defining a **block** class, must follow PascalCase.

    .ComponentName {
    }

Elements are defined by a single - (dash), and written in camelCase

    .ComponentName {
	     
        & .ComponentName-elementNameAvatar {
	    }
	    & .ComponentName-elementNameDescription {
	    }
    }

Adapters are defined by an underscore, and are also written in camelCase.

    .ComponentName_blueBox {
    }
or, for an Element:

    .ComponentName-elementName_adaptorName {
    }

