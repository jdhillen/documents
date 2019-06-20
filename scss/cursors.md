[Cursor](https://css-tricks.com/almanac/properties/c/cursor/)
===

```scss
.cursor {
    // - All Cursor Styles -------------------------------------------------------------------------
    &--auto            { cursor: auto; }
    &--default         { cursor: default; }
    &--none            { cursor: none; }
    &--context-menu    { cursor: context-menu; }
    &--help            { cursor: help; }
    &--pointer         { cursor: pointer; }
    &--progress        { cursor: progress; }
    &--wait            { cursor: wait; }
    &--cell            { cursor: cell; }
    &--crosshair       { cursor: crosshair; }
    &--text            { cursor: text; }
    &--vertical-text   { cursor: vertical-text; }
    &--alias           { cursor: alias; }
    &--copy            { cursor: copy; }
    &--move            { cursor: move; }
    &--no-drop         { cursor: no-drop; }
    &--not-allowed     { cursor: not-allowed; }
    &--all-scroll      { cursor: all-scroll; }
    &--col-resize      { cursor: col-resize; }
    &--row-resize      { cursor: row-resize; }
    &--n-resize        { cursor: n-resize; }
    &--e-resize        { cursor: e-resize; }
    &--s-resize        { cursor: s-resize; }
    &--w-resize        { cursor: w-resize; }
    &--ns-resize       { cursor: ns-resize; }
    &--ew-resize       { cursor: ew-resize; }
    &--ne-resize       { cursor: ne-resize; }
    &--nw-resize       { cursor: nw-resize; }
    &--se-resize       { cursor: se-resize; }
    &--sw-resize       { cursor: sw-resize; }
    &--nesw-resize     { cursor: nesw-resize; }
    &--nwse-resize     { cursor: nwse-resize; }

    // - Webkit Only Cursors -----------------------------------------------------------------------
    &--wk-zoom-in       { cursor: -webkit-zoom-in; }
    &--wk-zoom-out      { cursor: -webkit-zoom-out; }
    &--wk-zoom-grab     { cursor: -webkit-zoom-grab; }
    &--wk-zoom-grabbing { cursor: -webkit-zoom-grabbing; }

    //- Custom Cursors -----------------------------------------------------------------------------
    &--custom {
        cursor: url('path/to/my/cursor.png'), auto;
    }
}
```
