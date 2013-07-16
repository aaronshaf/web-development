An overview of what you can find at the [spec](http://www.w3.org/TR/wai-aria/).

## Roles

### Widgets

* alert
* alertdialog
* button
* checkbox
* dialog
* gridcell
* link
* log
* marquee
* menuitem
* menuitemcheckbox
* menuitemradio
* option
* progressbar
* radio
* scrollbar
* slider
* spinbutton
* status
* tab
* tabpanel
* textbox
* timer
* tooltip
* treeitem

### Composite widgets

* combobox
* grid
* listbox
* menu
* menubar
* radiogroup
* tablist
* tree
* treegrid

### Document structure

* article
* columnheader
* definition
* directory
* document
* group
* heading
* img
* list
* listitem
* math
* note
* presentation
* region
* row
* rowheader
* separator
* toolbar

### Landmarks

* application - "hint to certain assistive technologies to switch from normal browsing mode into a mode more appropriate for interacting with a web application" (spec)
* banner - masthead
* complementary
* contentinfo
* form
* main
* navigation
* search

## States and properties

### Widget attributes

A widget "receive[s] user input and process[es] user actions."

* aria-autocomplete - "whether user input completion suggestions are provided"
* aria-checked (state)
* aria-disabled (state)
* aria-expanded (state)
* aria-haspopup - "has a popup context menu or sub-level menu"
* aria-hidden (state)
* aria-invalid (state)
* aria-label
* aria-level - integer that "defines the hierarchical level"... "applied inside trees to tree items, to headings inside a document, to nested grids, nested tablists", etc.
* aria-multiline - "text box accepts multiple lines"
* aria-multiselectable - "user may select more than one item from the current selectable descendants"
* aria-orientation
* aria-pressed (state)
* aria-readonly
* aria-required
* aria-selected (state)
* aria-sort
 * Apply to only one header at a time
* "ascending", "descending", "none", or "other"
* For range widget
 * aria-valuemax
 * aria-valuemin
 * aria-valuenow
 * aria-valuetext

### Live region attributes


* aria-busy (state) - "currently being updated"
* aria-live
 * off - Updates will not be presented unless currently focused on region
 * polite - Updates should be announced "at next graceful oppportunity"
 * assertive - User should be notified immediately
* aria-relevant
 * aria-atomic - "will present all, or only parts of, the changed region"

## Drop-and-drop attributes

* aria-dropeffect
* aria-grabbed (state)

## Relationship attributes

* aria-activedescendant
* aria-controls - "element(s) whose contents or presence are controlled by the current element"
* aria-describedby
* aria-flowto - "override the general default of reading in document source order"
* aria-labelledby
* aria-owns - indentifies parent/child not already represented in the DOM
* aria-posinset - "number or position in the current set of listitems or treeitems"; only use if not all item elements are in DOM
* aria-setsize - "number of items in the current set of listitems or treeitems"; only use if not all item elements are in DOM

## Examples

### Table with sortable columns

```html
<table>
  <thead>
    <tr role="row">
      <th role="columnheader" aria-sort="ascending">
        <a href="#"></a>
      </th>
      <th role="columnheader">
        Date
      </th>
    </tr>
  </thead>
  <tbody>
    <tr role="row">
      <td role="gridcell"></td>
      <td role="gridcell"></td>
    </tr>
  </tbody>
</table>
```

## Tips

* Get to know: Roles, states, and properties.
* Roles should not be changed after creation.
* "User agents MUST provide a way for assistive technologies to be notified when states change, either through DOM attribute change events or platform accessibility API events."

## Readers

* [JAWS](http://www.freedomscientific.com/products/fs/jaws-product-page.asp)
* [NVDA](http://www.nvaccess.org/)
* [Voiceover](http://www.apple.com/accessibility/osx/voiceover/)

## Questions

* Difference between title, label, and description?
* Difference between describedby and labelledby?
* Aria-specific differences between
 * disabled and hidden?
 * pressed, selected, checked?
 * grid and table?

## See also

* http://www.w3.org/TR/wai-aria/roles
* http://www.w3.org/TR/wai-aria-primer/
* http://rawgithub.com/w3c/aria-in-html/master/index.html
* http://alistapart.com/article/waiaria
* http://www.w3.org/WAI/intro/aria.php
* http://dev.opera.com/articles/view/introduction-to-wai-aria/
* http://www.webmonkey.com/tag/wai-aria/
* http://alistapart.com/article/the-accessibility-of-wai-aria
* http://alistapart.com/article/aria-and-progressive-enhancement
* http://www.accessibleculture.org/articles/2010/11/html5-plus-aria-sanity-check/
* http://www.marcozehe.de/2013/04/24/easy-aria-tip-6-making-clickables-accessible/
* http://john.foliot.ca/aria-hidden/