Beatrix OOSass Framework
========================

Block, Element, Adaptor
-----------------------

Basically BEM, renamed to fit in with the name BEAtrix.
However, Beatrix offers a much cleaner and legible syntax, rather than having double dash, single dashes, double underscores and single underscores all over the place. It focuses on symantically written class names and logical divisions of code.

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


Property Order
--------------

One thing about CSS is that it can all just look like a long list of properties. This can cause duplication, scoping issues and general clutter. In an effort to avoid this, a structured order should be maintain based upon the kind of properties you are adding to your class. We have broken these down into Property Segments. When writing your class, you should make sure your properties are listed within the correct Property Segment, and that your Property Segments are ordered correctly. Ordering of properties within Property Segments doesn't matter.

Segment 1: Dimensions

 - width
 - height
 - max-width
 - max-height

Segment 2: Additional Dimensions

 - margin
 - padding
 
Segment 3: Positioning

 - float
 - position
 - display
 - z-index

Segment 4: Styling

 - background 
 - border (including border-radius) 
 - opacity

Segment 5: Typography

 - font (including font-family, font-size etc.)
 - color
 - text-decoration

(complete list required)

File Structure
--------------

The file structure is related to the various kinds of classes the Beatrix framework implements.

- components
- config
- layout
- lib
- utils

**base**
As you will read in the notes left in the boilerplate files, the base directory is home for the groundworks of your styles. For example, basic html nodes are to be configured for default behaviour here. 

**components**
The directory to house your components using the BEA methodology. 
Files are to be named according to the name of the component block class name.

**config**
Your global Sass Variables live here, as well as the groundworks of your styles. Base html nodes are to be configured for default behaviour here. 

**layout**
This directory is for elements on your site such as the header and footer, which are (on the whole) none-reusable elements and require specific styles. These elements should still follow the BEA class naming convention and rules.

**lib**
A directory for all your libraries

**utils**
Utility classes & mixins. Utility classes should be prefixed with "u-", and contain the the property and attribute, divided by another "u". (E.g., .u-float-left, .u-bg-white, .u-colour-black, .u-display-block). Shorthand property names are acceptable, but each utility class should only provide one overriding attribute.
