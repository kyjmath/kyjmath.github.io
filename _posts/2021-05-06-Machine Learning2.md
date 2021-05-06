---
layout: post
comments: true
title : Machine Learning2 [CHI]
categories: [Practice]
---


<html>
<head><meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>2019_Lec10 Trading and machine learning_2</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>




<style type="text/css">
    pre { line-height: 125%; margin: 0; }
td.linenos pre { color: #000000; background-color: #f0f0f0; padding-left: 5px; padding-right: 5px; }
span.linenos { color: #000000; background-color: #f0f0f0; padding-left: 5px; padding-right: 5px; }
td.linenos pre.special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
span.linenos.special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
.highlight .hll { background-color: var(--jp-cell-editor-active-background) }
.highlight { background: var(--jp-cell-editor-background); color: var(--jp-mirror-editor-variable-color) }
.highlight .c { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment */
.highlight .err { color: var(--jp-mirror-editor-error-color) } /* Error */
.highlight .k { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword */
.highlight .o { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator */
.highlight .p { color: var(--jp-mirror-editor-punctuation-color) } /* Punctuation */
.highlight .ch { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Multiline */
.highlight .cp { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Preproc */
.highlight .cpf { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Single */
.highlight .cs { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Special */
.highlight .kc { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Pseudo */
.highlight .kr { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Type */
.highlight .m { color: var(--jp-mirror-editor-number-color) } /* Literal.Number */
.highlight .s { color: var(--jp-mirror-editor-string-color) } /* Literal.String */
.highlight .ow { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator.Word */
.highlight .w { color: var(--jp-mirror-editor-variable-color) } /* Text.Whitespace */
.highlight .mb { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Bin */
.highlight .mf { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Float */
.highlight .mh { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Hex */
.highlight .mi { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer */
.highlight .mo { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Oct */
.highlight .sa { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Affix */
.highlight .sb { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Backtick */
.highlight .sc { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Char */
.highlight .dl { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Delimiter */
.highlight .sd { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Doc */
.highlight .s2 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Double */
.highlight .se { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Escape */
.highlight .sh { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Heredoc */
.highlight .si { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Interpol */
.highlight .sx { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Other */
.highlight .sr { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Regex */
.highlight .s1 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Single */
.highlight .ss { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Symbol */
.highlight .il { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer.Long */
  </style>



<style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
 * Mozilla scrollbar styling
 */

/* use standard opaque scrollbars for most nodes */
[data-jp-theme-scrollbars='true'] {
  scrollbar-color: rgb(var(--jp-scrollbar-thumb-color))
    var(--jp-scrollbar-background-color);
}

/* for code nodes, use a transparent style of scrollbar. These selectors
 * will match lower in the tree, and so will override the above */
[data-jp-theme-scrollbars='true'] .CodeMirror-hscrollbar,
[data-jp-theme-scrollbars='true'] .CodeMirror-vscrollbar {
  scrollbar-color: rgba(var(--jp-scrollbar-thumb-color), 0.5) transparent;
}

/*
 * Webkit scrollbar styling
 */

/* use standard opaque scrollbars for most nodes */

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar,
[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-corner {
  background: var(--jp-scrollbar-background-color);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-thumb {
  background: rgb(var(--jp-scrollbar-thumb-color));
  border: var(--jp-scrollbar-thumb-margin) solid transparent;
  background-clip: content-box;
  border-radius: var(--jp-scrollbar-thumb-radius);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-track:horizontal {
  border-left: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
  border-right: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-track:vertical {
  border-top: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
  border-bottom: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
}

/* for code nodes, use a transparent style of scrollbar */

[data-jp-theme-scrollbars='true'] .CodeMirror-hscrollbar::-webkit-scrollbar,
[data-jp-theme-scrollbars='true'] .CodeMirror-vscrollbar::-webkit-scrollbar,
[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-corner,
[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-corner {
  background-color: transparent;
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-thumb,
[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-thumb {
  background: rgba(var(--jp-scrollbar-thumb-color), 0.5);
  border: var(--jp-scrollbar-thumb-margin) solid transparent;
  background-clip: content-box;
  border-radius: var(--jp-scrollbar-thumb-radius);
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-track:horizontal {
  border-left: var(--jp-scrollbar-endpad) solid transparent;
  border-right: var(--jp-scrollbar-endpad) solid transparent;
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-track:vertical {
  border-top: var(--jp-scrollbar-endpad) solid transparent;
  border-bottom: var(--jp-scrollbar-endpad) solid transparent;
}

/*
 * Phosphor
 */

.lm-ScrollBar[data-orientation='horizontal'] {
  min-height: 16px;
  max-height: 16px;
  min-width: 45px;
  border-top: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] {
  min-width: 16px;
  max-width: 16px;
  min-height: 45px;
  border-left: 1px solid #a0a0a0;
}

.lm-ScrollBar-button {
  background-color: #f0f0f0;
  background-position: center center;
  min-height: 15px;
  max-height: 15px;
  min-width: 15px;
  max-width: 15px;
}

.lm-ScrollBar-button:hover {
  background-color: #dadada;
}

.lm-ScrollBar-button.lm-mod-active {
  background-color: #cdcdcd;
}

.lm-ScrollBar-track {
  background: #f0f0f0;
}

.lm-ScrollBar-thumb {
  background: #cdcdcd;
}

.lm-ScrollBar-thumb:hover {
  background: #bababa;
}

.lm-ScrollBar-thumb.lm-mod-active {
  background: #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal'] .lm-ScrollBar-thumb {
  height: 100%;
  min-width: 15px;
  border-left: 1px solid #a0a0a0;
  border-right: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] .lm-ScrollBar-thumb {
  width: 100%;
  min-height: 15px;
  border-top: 1px solid #a0a0a0;
  border-bottom: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-left);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-right);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-up);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-down);
  background-size: 17px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-Widget, /* </DEPRECATED> */
.lm-Widget {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  cursor: default;
}


/* <DEPRECATED> */ .p-Widget.p-mod-hidden, /* </DEPRECATED> */
.lm-Widget.lm-mod-hidden {
  display: none !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-CommandPalette, /* </DEPRECATED> */
.lm-CommandPalette {
  display: flex;
  flex-direction: column;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-CommandPalette-search, /* </DEPRECATED> */
.lm-CommandPalette-search {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-content, /* </DEPRECATED> */
.lm-CommandPalette-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  min-height: 0;
  overflow: auto;
  list-style-type: none;
}


/* <DEPRECATED> */ .p-CommandPalette-header, /* </DEPRECATED> */
.lm-CommandPalette-header {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}


/* <DEPRECATED> */ .p-CommandPalette-item, /* </DEPRECATED> */
.lm-CommandPalette-item {
  display: flex;
  flex-direction: row;
}


/* <DEPRECATED> */ .p-CommandPalette-itemIcon, /* </DEPRECATED> */
.lm-CommandPalette-itemIcon {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-itemContent, /* </DEPRECATED> */
.lm-CommandPalette-itemContent {
  flex: 1 1 auto;
  overflow: hidden;
}


/* <DEPRECATED> */ .p-CommandPalette-itemShortcut, /* </DEPRECATED> */
.lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-itemLabel, /* </DEPRECATED> */
.lm-CommandPalette-itemLabel {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-DockPanel, /* </DEPRECATED> */
.lm-DockPanel {
  z-index: 0;
}


/* <DEPRECATED> */ .p-DockPanel-widget, /* </DEPRECATED> */
.lm-DockPanel-widget {
  z-index: 0;
}


/* <DEPRECATED> */ .p-DockPanel-tabBar, /* </DEPRECATED> */
.lm-DockPanel-tabBar {
  z-index: 1;
}


/* <DEPRECATED> */ .p-DockPanel-handle, /* </DEPRECATED> */
.lm-DockPanel-handle {
  z-index: 2;
}


/* <DEPRECATED> */ .p-DockPanel-handle.p-mod-hidden, /* </DEPRECATED> */
.lm-DockPanel-handle.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-DockPanel-handle:after, /* </DEPRECATED> */
.lm-DockPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='horizontal'],
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='horizontal'] {
  cursor: ew-resize;
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='vertical'],
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='vertical'] {
  cursor: ns-resize;
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='horizontal']:after,
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='horizontal']:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='vertical']:after,
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='vertical']:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}


/* <DEPRECATED> */ .p-DockPanel-overlay, /* </DEPRECATED> */
.lm-DockPanel-overlay {
  z-index: 3;
  box-sizing: border-box;
  pointer-events: none;
}


/* <DEPRECATED> */ .p-DockPanel-overlay.p-mod-hidden, /* </DEPRECATED> */
.lm-DockPanel-overlay.lm-mod-hidden {
  display: none !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-Menu, /* </DEPRECATED> */
.lm-Menu {
  z-index: 10000;
  position: absolute;
  white-space: nowrap;
  overflow-x: hidden;
  overflow-y: auto;
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-Menu-content, /* </DEPRECATED> */
.lm-Menu-content {
  margin: 0;
  padding: 0;
  display: table;
  list-style-type: none;
}


/* <DEPRECATED> */ .p-Menu-item, /* </DEPRECATED> */
.lm-Menu-item {
  display: table-row;
}


/* <DEPRECATED> */
.p-Menu-item.p-mod-hidden,
.p-Menu-item.p-mod-collapsed,
/* </DEPRECATED> */
.lm-Menu-item.lm-mod-hidden,
.lm-Menu-item.lm-mod-collapsed {
  display: none !important;
}


/* <DEPRECATED> */
.p-Menu-itemIcon,
.p-Menu-itemSubmenuIcon,
/* </DEPRECATED> */
.lm-Menu-itemIcon,
.lm-Menu-itemSubmenuIcon {
  display: table-cell;
  text-align: center;
}


/* <DEPRECATED> */ .p-Menu-itemLabel, /* </DEPRECATED> */
.lm-Menu-itemLabel {
  display: table-cell;
  text-align: left;
}


/* <DEPRECATED> */ .p-Menu-itemShortcut, /* </DEPRECATED> */
.lm-Menu-itemShortcut {
  display: table-cell;
  text-align: right;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-MenuBar, /* </DEPRECATED> */
.lm-MenuBar {
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-MenuBar-content, /* </DEPRECATED> */
.lm-MenuBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: row;
  list-style-type: none;
}


/* <DEPRECATED> */ .p--MenuBar-item, /* </DEPRECATED> */
.lm-MenuBar-item {
  box-sizing: border-box;
}


/* <DEPRECATED> */
.p-MenuBar-itemIcon,
.p-MenuBar-itemLabel,
/* </DEPRECATED> */
.lm-MenuBar-itemIcon,
.lm-MenuBar-itemLabel {
  display: inline-block;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-ScrollBar, /* </DEPRECATED> */
.lm-ScrollBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */
.p-ScrollBar[data-orientation='horizontal'],
/* </DEPRECATED> */
.lm-ScrollBar[data-orientation='horizontal'] {
  flex-direction: row;
}


/* <DEPRECATED> */
.p-ScrollBar[data-orientation='vertical'],
/* </DEPRECATED> */
.lm-ScrollBar[data-orientation='vertical'] {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-ScrollBar-button, /* </DEPRECATED> */
.lm-ScrollBar-button {
  box-sizing: border-box;
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-ScrollBar-track, /* </DEPRECATED> */
.lm-ScrollBar-track {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  flex: 1 1 auto;
}


/* <DEPRECATED> */ .p-ScrollBar-thumb, /* </DEPRECATED> */
.lm-ScrollBar-thumb {
  box-sizing: border-box;
  position: absolute;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-SplitPanel-child, /* </DEPRECATED> */
.lm-SplitPanel-child {
  z-index: 0;
}


/* <DEPRECATED> */ .p-SplitPanel-handle, /* </DEPRECATED> */
.lm-SplitPanel-handle {
  z-index: 1;
}


/* <DEPRECATED> */ .p-SplitPanel-handle.p-mod-hidden, /* </DEPRECATED> */
.lm-SplitPanel-handle.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-SplitPanel-handle:after, /* </DEPRECATED> */
.lm-SplitPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='horizontal'] > .p-SplitPanel-handle,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle {
  cursor: ew-resize;
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='vertical'] > .p-SplitPanel-handle,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle {
  cursor: ns-resize;
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='horizontal'] > .p-SplitPanel-handle:after,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='vertical'] > .p-SplitPanel-handle:after,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-TabBar, /* </DEPRECATED> */
.lm-TabBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-TabBar[data-orientation='horizontal'], /* </DEPRECATED> */
.lm-TabBar[data-orientation='horizontal'] {
  flex-direction: row;
}


/* <DEPRECATED> */ .p-TabBar[data-orientation='vertical'], /* </DEPRECATED> */
.lm-TabBar[data-orientation='vertical'] {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-TabBar-content, /* </DEPRECATED> */
.lm-TabBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex: 1 1 auto;
  list-style-type: none;
}


/* <DEPRECATED> */
.p-TabBar[data-orientation='horizontal'] > .p-TabBar-content,
/* </DEPRECATED> */
.lm-TabBar[data-orientation='horizontal'] > .lm-TabBar-content {
  flex-direction: row;
}


/* <DEPRECATED> */
.p-TabBar[data-orientation='vertical'] > .p-TabBar-content,
/* </DEPRECATED> */
.lm-TabBar[data-orientation='vertical'] > .lm-TabBar-content {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-TabBar-tab, /* </DEPRECATED> */
.lm-TabBar-tab {
  display: flex;
  flex-direction: row;
  box-sizing: border-box;
  overflow: hidden;
}


/* <DEPRECATED> */
.p-TabBar-tabIcon,
.p-TabBar-tabCloseIcon,
/* </DEPRECATED> */
.lm-TabBar-tabIcon,
.lm-TabBar-tabCloseIcon {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-TabBar-tabLabel, /* </DEPRECATED> */
.lm-TabBar-tabLabel {
  flex: 1 1 auto;
  overflow: hidden;
  white-space: nowrap;
}


/* <DEPRECATED> */ .p-TabBar-tab.p-mod-hidden, /* </DEPRECATED> */
.lm-TabBar-tab.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-TabBar.p-mod-dragging .p-TabBar-tab, /* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging .lm-TabBar-tab {
  position: relative;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging[data-orientation='horizontal'] .p-TabBar-tab,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging[data-orientation='horizontal'] .lm-TabBar-tab {
  left: 0;
  transition: left 150ms ease;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging[data-orientation='vertical'] .p-TabBar-tab,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging[data-orientation='vertical'] .lm-TabBar-tab {
  top: 0;
  transition: top 150ms ease;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging .p-TabBar-tab.p-mod-dragging
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging .lm-TabBar-tab.lm-mod-dragging {
  transition: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-TabPanel-tabBar, /* </DEPRECATED> */
.lm-TabPanel-tabBar {
  z-index: 1;
}


/* <DEPRECATED> */ .p-TabPanel-stackedPanel, /* </DEPRECATED> */
.lm-TabPanel-stackedPanel {
  z-index: 0;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

@charset "UTF-8";
/*!

Copyright 2015-present Palantir Technologies, Inc. All rights reserved.
Licensed under the Apache License, Version 2.0.

*/
html{
  -webkit-box-sizing:border-box;
          box-sizing:border-box; }

*,
*::before,
*::after{
  -webkit-box-sizing:inherit;
          box-sizing:inherit; }

body{
  text-transform:none;
  line-height:1.28581;
  letter-spacing:0;
  font-size:14px;
  font-weight:400;
  color:#182026;
  font-family:-apple-system, "BlinkMacSystemFont", "Segoe UI", "Roboto", "Oxygen", "Ubuntu", "Cantarell", "Open Sans", "Helvetica Neue", "Icons16", sans-serif; }

p{
  margin-top:0;
  margin-bottom:10px; }

small{
  font-size:12px; }

strong{
  font-weight:600; }

::-moz-selection{
  background:rgba(125, 188, 255, 0.6); }

::selection{
  background:rgba(125, 188, 255, 0.6); }
.bp3-heading{
  color:#182026;
  font-weight:600;
  margin:0 0 10px;
  padding:0; }
  .bp3-dark .bp3-heading{
    color:#f5f8fa; }

h1.bp3-heading, .bp3-running-text h1{
  line-height:40px;
  font-size:36px; }

h2.bp3-heading, .bp3-running-text h2{
  line-height:32px;
  font-size:28px; }

h3.bp3-heading, .bp3-running-text h3{
  line-height:25px;
  font-size:22px; }

h4.bp3-heading, .bp3-running-text h4{
  line-height:21px;
  font-size:18px; }

h5.bp3-heading, .bp3-running-text h5{
  line-height:19px;
  font-size:16px; }

h6.bp3-heading, .bp3-running-text h6{
  line-height:16px;
  font-size:14px; }
.bp3-ui-text{
  text-transform:none;
  line-height:1.28581;
  letter-spacing:0;
  font-size:14px;
  font-weight:400; }

.bp3-monospace-text{
  text-transform:none;
  font-family:monospace; }

.bp3-text-muted{
  color:#5c7080; }
  .bp3-dark .bp3-text-muted{
    color:#a7b6c2; }

.bp3-text-disabled{
  color:rgba(92, 112, 128, 0.6); }
  .bp3-dark .bp3-text-disabled{
    color:rgba(167, 182, 194, 0.6); }

.bp3-text-overflow-ellipsis{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal; }
.bp3-running-text{
  line-height:1.5;
  font-size:14px; }
  .bp3-running-text h1{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h1{
      color:#f5f8fa; }
  .bp3-running-text h2{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h2{
      color:#f5f8fa; }
  .bp3-running-text h3{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h3{
      color:#f5f8fa; }
  .bp3-running-text h4{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h4{
      color:#f5f8fa; }
  .bp3-running-text h5{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h5{
      color:#f5f8fa; }
  .bp3-running-text h6{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h6{
      color:#f5f8fa; }
  .bp3-running-text hr{
    margin:20px 0;
    border:none;
    border-bottom:1px solid rgba(16, 22, 26, 0.15); }
    .bp3-dark .bp3-running-text hr{
      border-color:rgba(255, 255, 255, 0.15); }
  .bp3-running-text p{
    margin:0 0 10px;
    padding:0; }

.bp3-text-large{
  font-size:16px; }

.bp3-text-small{
  font-size:12px; }
a{
  text-decoration:none;
  color:#106ba3; }
  a:hover{
    cursor:pointer;
    text-decoration:underline;
    color:#106ba3; }
  a .bp3-icon, a .bp3-icon-standard, a .bp3-icon-large{
    color:inherit; }
  a code,
  .bp3-dark a code{
    color:inherit; }
  .bp3-dark a,
  .bp3-dark a:hover{
    color:#48aff0; }
    .bp3-dark a .bp3-icon, .bp3-dark a .bp3-icon-standard, .bp3-dark a .bp3-icon-large,
    .bp3-dark a:hover .bp3-icon,
    .bp3-dark a:hover .bp3-icon-standard,
    .bp3-dark a:hover .bp3-icon-large{
      color:inherit; }
.bp3-running-text code, .bp3-code{
  text-transform:none;
  font-family:monospace;
  border-radius:3px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2);
  background:rgba(255, 255, 255, 0.7);
  padding:2px 5px;
  color:#5c7080;
  font-size:smaller; }
  .bp3-dark .bp3-running-text code, .bp3-running-text .bp3-dark code, .bp3-dark .bp3-code{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
    background:rgba(16, 22, 26, 0.3);
    color:#a7b6c2; }
  .bp3-running-text a > code, a > .bp3-code{
    color:#137cbd; }
    .bp3-dark .bp3-running-text a > code, .bp3-running-text .bp3-dark a > code, .bp3-dark a > .bp3-code{
      color:inherit; }

.bp3-running-text pre, .bp3-code-block{
  text-transform:none;
  font-family:monospace;
  display:block;
  margin:10px 0;
  border-radius:3px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
  background:rgba(255, 255, 255, 0.7);
  padding:13px 15px 12px;
  line-height:1.4;
  color:#182026;
  font-size:13px;
  word-break:break-all;
  word-wrap:break-word; }
  .bp3-dark .bp3-running-text pre, .bp3-running-text .bp3-dark pre, .bp3-dark .bp3-code-block{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
    background:rgba(16, 22, 26, 0.3);
    color:#f5f8fa; }
  .bp3-running-text pre > code, .bp3-code-block > code{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:none;
    padding:0;
    color:inherit;
    font-size:inherit; }

.bp3-running-text kbd, .bp3-key{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  background:#ffffff;
  min-width:24px;
  height:24px;
  padding:3px 6px;
  vertical-align:middle;
  line-height:24px;
  color:#5c7080;
  font-family:inherit;
  font-size:12px; }
  .bp3-running-text kbd .bp3-icon, .bp3-key .bp3-icon, .bp3-running-text kbd .bp3-icon-standard, .bp3-key .bp3-icon-standard, .bp3-running-text kbd .bp3-icon-large, .bp3-key .bp3-icon-large{
    margin-right:5px; }
  .bp3-dark .bp3-running-text kbd, .bp3-running-text .bp3-dark kbd, .bp3-dark .bp3-key{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
    background:#394b59;
    color:#a7b6c2; }
.bp3-running-text blockquote, .bp3-blockquote{
  margin:0 0 10px;
  border-left:solid 4px rgba(167, 182, 194, 0.5);
  padding:0 20px; }
  .bp3-dark .bp3-running-text blockquote, .bp3-running-text .bp3-dark blockquote, .bp3-dark .bp3-blockquote{
    border-color:rgba(115, 134, 148, 0.5); }
.bp3-running-text ul,
.bp3-running-text ol, .bp3-list{
  margin:10px 0;
  padding-left:30px; }
  .bp3-running-text ul li:not(:last-child), .bp3-running-text ol li:not(:last-child), .bp3-list li:not(:last-child){
    margin-bottom:5px; }
  .bp3-running-text ul ol, .bp3-running-text ol ol, .bp3-list ol,
  .bp3-running-text ul ul,
  .bp3-running-text ol ul,
  .bp3-list ul{
    margin-top:5px; }

.bp3-list-unstyled{
  margin:0;
  padding:0;
  list-style:none; }
  .bp3-list-unstyled li{
    padding:0; }
.bp3-rtl{
  text-align:right; }

.bp3-dark{
  color:#f5f8fa; }

:focus{
  outline:rgba(19, 124, 189, 0.6) auto 2px;
  outline-offset:2px;
  -moz-outline-radius:6px; }

.bp3-focus-disabled :focus{
  outline:none !important; }
  .bp3-focus-disabled :focus ~ .bp3-control-indicator{
    outline:none !important; }

.bp3-alert{
  max-width:400px;
  padding:20px; }

.bp3-alert-body{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }
  .bp3-alert-body .bp3-icon{
    margin-top:0;
    margin-right:20px;
    font-size:40px; }

.bp3-alert-footer{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:reverse;
      -ms-flex-direction:row-reverse;
          flex-direction:row-reverse;
  margin-top:10px; }
  .bp3-alert-footer .bp3-button{
    margin-left:10px; }
.bp3-breadcrumbs{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-wrap:wrap;
      flex-wrap:wrap;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  margin:0;
  cursor:default;
  height:30px;
  padding:0;
  list-style:none; }
  .bp3-breadcrumbs > li{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center; }
    .bp3-breadcrumbs > li::after{
      display:block;
      margin:0 5px;
      background:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M10.71 7.29l-4-4a1.003 1.003 0 0 0-1.42 1.42L8.59 8 5.3 11.29c-.19.18-.3.43-.3.71a1.003 1.003 0 0 0 1.71.71l4-4c.18-.18.29-.43.29-.71 0-.28-.11-.53-.29-.71z' fill='%235C7080'/%3e%3c/svg%3e");
      width:16px;
      height:16px;
      content:""; }
    .bp3-breadcrumbs > li:last-of-type::after{
      display:none; }

.bp3-breadcrumb,
.bp3-breadcrumb-current,
.bp3-breadcrumbs-collapsed{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  font-size:16px; }

.bp3-breadcrumb,
.bp3-breadcrumbs-collapsed{
  color:#5c7080; }

.bp3-breadcrumb:hover{
  text-decoration:none; }

.bp3-breadcrumb.bp3-disabled{
  cursor:not-allowed;
  color:rgba(92, 112, 128, 0.6); }

.bp3-breadcrumb .bp3-icon{
  margin-right:5px; }

.bp3-breadcrumb-current{
  color:inherit;
  font-weight:600; }
  .bp3-breadcrumb-current .bp3-input{
    vertical-align:baseline;
    font-size:inherit;
    font-weight:inherit; }

.bp3-breadcrumbs-collapsed{
  margin-right:2px;
  border:none;
  border-radius:3px;
  background:#ced9e0;
  cursor:pointer;
  padding:1px 5px;
  vertical-align:text-bottom; }
  .bp3-breadcrumbs-collapsed::before{
    display:block;
    background:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cg fill='%235C7080'%3e%3ccircle cx='2' cy='8.03' r='2'/%3e%3ccircle cx='14' cy='8.03' r='2'/%3e%3ccircle cx='8' cy='8.03' r='2'/%3e%3c/g%3e%3c/svg%3e") center no-repeat;
    width:16px;
    height:16px;
    content:""; }
  .bp3-breadcrumbs-collapsed:hover{
    background:#bfccd6;
    text-decoration:none;
    color:#182026; }

.bp3-dark .bp3-breadcrumb,
.bp3-dark .bp3-breadcrumbs-collapsed{
  color:#a7b6c2; }

.bp3-dark .bp3-breadcrumbs > li::after{
  color:#a7b6c2; }

.bp3-dark .bp3-breadcrumb.bp3-disabled{
  color:rgba(167, 182, 194, 0.6); }

.bp3-dark .bp3-breadcrumb-current{
  color:#f5f8fa; }

.bp3-dark .bp3-breadcrumbs-collapsed{
  background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-breadcrumbs-collapsed:hover{
    background:rgba(16, 22, 26, 0.6);
    color:#f5f8fa; }
.bp3-button{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  border:none;
  border-radius:3px;
  cursor:pointer;
  padding:5px 10px;
  vertical-align:middle;
  text-align:left;
  font-size:14px;
  min-width:30px;
  min-height:30px; }
  .bp3-button > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-button > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-button::before,
  .bp3-button > *{
    margin-right:7px; }
  .bp3-button:empty::before,
  .bp3-button > :last-child{
    margin-right:0; }
  .bp3-button:empty{
    padding:0 !important; }
  .bp3-button:disabled, .bp3-button.bp3-disabled{
    cursor:not-allowed; }
  .bp3-button.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-button.bp3-align-right,
  .bp3-align-right .bp3-button{
    text-align:right; }
  .bp3-button.bp3-align-left,
  .bp3-align-left .bp3-button{
    text-align:left; }
  .bp3-button:not([class*="bp3-intent-"]){
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    color:#182026; }
    .bp3-button:not([class*="bp3-intent-"]):hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
      background-clip:padding-box;
      background-color:#ebf1f5; }
    .bp3-button:not([class*="bp3-intent-"]):active, .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#d8e1e8;
      background-image:none; }
    .bp3-button:not([class*="bp3-intent-"]):disabled, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled{
      outline:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(206, 217, 224, 0.5);
      background-image:none;
      cursor:not-allowed;
      color:rgba(92, 112, 128, 0.6); }
      .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active, .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active:hover, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active:hover{
        background:rgba(206, 217, 224, 0.7); }
  .bp3-button.bp3-intent-primary{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
    .bp3-button.bp3-intent-primary:hover, .bp3-button.bp3-intent-primary:active, .bp3-button.bp3-intent-primary.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-primary:hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
      background-color:#106ba3; }
    .bp3-button.bp3-intent-primary:active, .bp3-button.bp3-intent-primary.bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#0e5a8a;
      background-image:none; }
    .bp3-button.bp3-intent-primary:disabled, .bp3-button.bp3-intent-primary.bp3-disabled{
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(19, 124, 189, 0.5);
      background-image:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-success{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#0f9960;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
    .bp3-button.bp3-intent-success:hover, .bp3-button.bp3-intent-success:active, .bp3-button.bp3-intent-success.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-success:hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
      background-color:#0d8050; }
    .bp3-button.bp3-intent-success:active, .bp3-button.bp3-intent-success.bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#0a6640;
      background-image:none; }
    .bp3-button.bp3-intent-success:disabled, .bp3-button.bp3-intent-success.bp3-disabled{
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(15, 153, 96, 0.5);
      background-image:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-warning{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#d9822b;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
    .bp3-button.bp3-intent-warning:hover, .bp3-button.bp3-intent-warning:active, .bp3-button.bp3-intent-warning.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-warning:hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
      background-color:#bf7326; }
    .bp3-button.bp3-intent-warning:active, .bp3-button.bp3-intent-warning.bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#a66321;
      background-image:none; }
    .bp3-button.bp3-intent-warning:disabled, .bp3-button.bp3-intent-warning.bp3-disabled{
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(217, 130, 43, 0.5);
      background-image:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-danger{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#db3737;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
    .bp3-button.bp3-intent-danger:hover, .bp3-button.bp3-intent-danger:active, .bp3-button.bp3-intent-danger.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-danger:hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
      background-color:#c23030; }
    .bp3-button.bp3-intent-danger:active, .bp3-button.bp3-intent-danger.bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#a82a2a;
      background-image:none; }
    .bp3-button.bp3-intent-danger:disabled, .bp3-button.bp3-intent-danger.bp3-disabled{
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(219, 55, 55, 0.5);
      background-image:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button[class*="bp3-intent-"] .bp3-button-spinner .bp3-spinner-head{
    stroke:#ffffff; }
  .bp3-button.bp3-large,
  .bp3-large .bp3-button{
    min-width:40px;
    min-height:40px;
    padding:5px 15px;
    font-size:16px; }
    .bp3-button.bp3-large::before,
    .bp3-button.bp3-large > *,
    .bp3-large .bp3-button::before,
    .bp3-large .bp3-button > *{
      margin-right:10px; }
    .bp3-button.bp3-large:empty::before,
    .bp3-button.bp3-large > :last-child,
    .bp3-large .bp3-button:empty::before,
    .bp3-large .bp3-button > :last-child{
      margin-right:0; }
  .bp3-button.bp3-small,
  .bp3-small .bp3-button{
    min-width:24px;
    min-height:24px;
    padding:0 7px; }
  .bp3-button.bp3-loading{
    position:relative; }
    .bp3-button.bp3-loading[class*="bp3-icon-"]::before{
      visibility:hidden; }
    .bp3-button.bp3-loading .bp3-button-spinner{
      position:absolute;
      margin:0; }
    .bp3-button.bp3-loading > :not(.bp3-button-spinner){
      visibility:hidden; }
  .bp3-button[class*="bp3-icon-"]::before{
    line-height:1;
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-weight:400;
    font-style:normal;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    color:#5c7080; }
  .bp3-button .bp3-icon, .bp3-button .bp3-icon-standard, .bp3-button .bp3-icon-large{
    color:#5c7080; }
    .bp3-button .bp3-icon.bp3-align-right, .bp3-button .bp3-icon-standard.bp3-align-right, .bp3-button .bp3-icon-large.bp3-align-right{
      margin-left:7px; }
  .bp3-button .bp3-icon:first-child:last-child,
  .bp3-button .bp3-spinner + .bp3-icon:last-child{
    margin:0 -7px; }
  .bp3-dark .bp3-button:not([class*="bp3-intent-"]){
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background-color:#394b59;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
    color:#f5f8fa; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):hover, .bp3-dark .bp3-button:not([class*="bp3-intent-"]):active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      color:#f5f8fa; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):hover{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      background-color:#30404d; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#202b33;
      background-image:none; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):disabled, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(57, 75, 89, 0.5);
      background-image:none;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active{
        background:rgba(57, 75, 89, 0.7); }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-button-spinner .bp3-spinner-head{
      background:rgba(16, 22, 26, 0.5);
      stroke:#8a9ba8; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"])[class*="bp3-icon-"]::before{
      color:#a7b6c2; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon, .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon-standard, .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon-large{
      color:#a7b6c2; }
  .bp3-dark .bp3-button[class*="bp3-intent-"]{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:hover{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:active, .bp3-dark .bp3-button[class*="bp3-intent-"].bp3-active{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:disabled, .bp3-dark .bp3-button[class*="bp3-intent-"].bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background-image:none;
      color:rgba(255, 255, 255, 0.3); }
    .bp3-dark .bp3-button[class*="bp3-intent-"] .bp3-button-spinner .bp3-spinner-head{
      stroke:#8a9ba8; }
  .bp3-button:disabled::before,
  .bp3-button:disabled .bp3-icon, .bp3-button:disabled .bp3-icon-standard, .bp3-button:disabled .bp3-icon-large, .bp3-button.bp3-disabled::before,
  .bp3-button.bp3-disabled .bp3-icon, .bp3-button.bp3-disabled .bp3-icon-standard, .bp3-button.bp3-disabled .bp3-icon-large, .bp3-button[class*="bp3-intent-"]::before,
  .bp3-button[class*="bp3-intent-"] .bp3-icon, .bp3-button[class*="bp3-intent-"] .bp3-icon-standard, .bp3-button[class*="bp3-intent-"] .bp3-icon-large{
    color:inherit !important; }
  .bp3-button.bp3-minimal{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:none; }
    .bp3-button.bp3-minimal:hover{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(167, 182, 194, 0.3);
      text-decoration:none;
      color:#182026; }
    .bp3-button.bp3-minimal:active, .bp3-button.bp3-minimal.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(115, 134, 148, 0.3);
      color:#182026; }
    .bp3-button.bp3-minimal:disabled, .bp3-button.bp3-minimal:disabled:hover, .bp3-button.bp3-minimal.bp3-disabled, .bp3-button.bp3-minimal.bp3-disabled:hover{
      background:none;
      cursor:not-allowed;
      color:rgba(92, 112, 128, 0.6); }
      .bp3-button.bp3-minimal:disabled.bp3-active, .bp3-button.bp3-minimal:disabled:hover.bp3-active, .bp3-button.bp3-minimal.bp3-disabled.bp3-active, .bp3-button.bp3-minimal.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button.bp3-minimal{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:inherit; }
      .bp3-dark .bp3-button.bp3-minimal:hover, .bp3-dark .bp3-button.bp3-minimal:active, .bp3-dark .bp3-button.bp3-minimal.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none; }
      .bp3-dark .bp3-button.bp3-minimal:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button.bp3-minimal:active, .bp3-dark .bp3-button.bp3-minimal.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button.bp3-minimal:disabled, .bp3-dark .bp3-button.bp3-minimal:disabled:hover, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled:hover{
        background:none;
        cursor:not-allowed;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-button.bp3-minimal:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal:disabled:hover.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:hover, .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:disabled, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-primary:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-success{
      color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:hover, .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:disabled, .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-success:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:hover, .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:disabled, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-warning:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-danger{
      color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:hover, .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:disabled, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-danger:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }

a.bp3-button{
  text-align:center;
  text-decoration:none;
  -webkit-transition:none;
  transition:none; }
  a.bp3-button, a.bp3-button:hover, a.bp3-button:active{
    color:#182026; }
  a.bp3-button.bp3-disabled{
    color:rgba(92, 112, 128, 0.6); }

.bp3-button-text{
  -webkit-box-flex:0;
      -ms-flex:0 1 auto;
          flex:0 1 auto; }

.bp3-button.bp3-align-left .bp3-button-text, .bp3-button.bp3-align-right .bp3-button-text,
.bp3-button-group.bp3-align-left .bp3-button-text,
.bp3-button-group.bp3-align-right .bp3-button-text{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto; }
.bp3-button-group{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex; }
  .bp3-button-group .bp3-button{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    position:relative;
    z-index:4; }
    .bp3-button-group .bp3-button:focus{
      z-index:5; }
    .bp3-button-group .bp3-button:hover{
      z-index:6; }
    .bp3-button-group .bp3-button:active, .bp3-button-group .bp3-button.bp3-active{
      z-index:7; }
    .bp3-button-group .bp3-button:disabled, .bp3-button-group .bp3-button.bp3-disabled{
      z-index:3; }
    .bp3-button-group .bp3-button[class*="bp3-intent-"]{
      z-index:9; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:focus{
        z-index:10; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:hover{
        z-index:11; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:active, .bp3-button-group .bp3-button[class*="bp3-intent-"].bp3-active{
        z-index:12; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:disabled, .bp3-button-group .bp3-button[class*="bp3-intent-"].bp3-disabled{
        z-index:8; }
  .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:first-child) .bp3-button,
  .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:first-child){
    border-top-left-radius:0;
    border-bottom-left-radius:0; }
  .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:last-child){
    margin-right:-1px;
    border-top-right-radius:0;
    border-bottom-right-radius:0; }
  .bp3-button-group.bp3-minimal .bp3-button{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:none; }
    .bp3-button-group.bp3-minimal .bp3-button:hover{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(167, 182, 194, 0.3);
      text-decoration:none;
      color:#182026; }
    .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(115, 134, 148, 0.3);
      color:#182026; }
    .bp3-button-group.bp3-minimal .bp3-button:disabled, .bp3-button-group.bp3-minimal .bp3-button:disabled:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover{
      background:none;
      cursor:not-allowed;
      color:rgba(92, 112, 128, 0.6); }
      .bp3-button-group.bp3-minimal .bp3-button:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button:disabled:hover.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button-group.bp3-minimal .bp3-button{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:inherit; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:hover, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled:hover, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover{
        background:none;
        cursor:not-allowed;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled:hover.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success{
      color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger{
      color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }
  .bp3-button-group .bp3-popover-wrapper,
  .bp3-button-group .bp3-popover-target{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-button-group.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-button-group .bp3-button.bp3-fill,
  .bp3-button-group.bp3-fill .bp3-button:not(.bp3-fixed){
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-button-group.bp3-vertical{
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column;
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch;
    vertical-align:top; }
    .bp3-button-group.bp3-vertical.bp3-fill{
      width:unset;
      height:100%; }
    .bp3-button-group.bp3-vertical .bp3-button{
      margin-right:0 !important;
      width:100%; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:first-child .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:first-child{
      border-radius:3px 3px 0 0; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:last-child .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:last-child{
      border-radius:0 0 3px 3px; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:not(:last-child){
      margin-bottom:-1px; }
  .bp3-button-group.bp3-align-left .bp3-button{
    text-align:left; }
  .bp3-dark .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-dark .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:last-child){
    margin-right:1px; }
  .bp3-dark .bp3-button-group.bp3-vertical > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-dark .bp3-button-group.bp3-vertical > .bp3-button:not(:last-child){
    margin-bottom:1px; }
.bp3-callout{
  line-height:1.5;
  font-size:14px;
  position:relative;
  border-radius:3px;
  background-color:rgba(138, 155, 168, 0.15);
  width:100%;
  padding:10px 12px 9px; }
  .bp3-callout[class*="bp3-icon-"]{
    padding-left:40px; }
    .bp3-callout[class*="bp3-icon-"]::before{
      line-height:1;
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-weight:400;
      font-style:normal;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased;
      position:absolute;
      top:10px;
      left:10px;
      color:#5c7080; }
  .bp3-callout.bp3-callout-icon{
    padding-left:40px; }
    .bp3-callout.bp3-callout-icon > .bp3-icon:first-child{
      position:absolute;
      top:10px;
      left:10px;
      color:#5c7080; }
  .bp3-callout .bp3-heading{
    margin-top:0;
    margin-bottom:5px;
    line-height:20px; }
    .bp3-callout .bp3-heading:last-child{
      margin-bottom:0; }
  .bp3-dark .bp3-callout{
    background-color:rgba(138, 155, 168, 0.2); }
    .bp3-dark .bp3-callout[class*="bp3-icon-"]::before{
      color:#a7b6c2; }
  .bp3-callout.bp3-intent-primary{
    background-color:rgba(19, 124, 189, 0.15); }
    .bp3-callout.bp3-intent-primary[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-primary > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-primary .bp3-heading{
      color:#106ba3; }
    .bp3-dark .bp3-callout.bp3-intent-primary{
      background-color:rgba(19, 124, 189, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-primary[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-primary > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-primary .bp3-heading{
        color:#48aff0; }
  .bp3-callout.bp3-intent-success{
    background-color:rgba(15, 153, 96, 0.15); }
    .bp3-callout.bp3-intent-success[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-success > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-success .bp3-heading{
      color:#0d8050; }
    .bp3-dark .bp3-callout.bp3-intent-success{
      background-color:rgba(15, 153, 96, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-success[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-success > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-success .bp3-heading{
        color:#3dcc91; }
  .bp3-callout.bp3-intent-warning{
    background-color:rgba(217, 130, 43, 0.15); }
    .bp3-callout.bp3-intent-warning[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-warning > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-warning .bp3-heading{
      color:#bf7326; }
    .bp3-dark .bp3-callout.bp3-intent-warning{
      background-color:rgba(217, 130, 43, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-warning[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-warning > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-warning .bp3-heading{
        color:#ffb366; }
  .bp3-callout.bp3-intent-danger{
    background-color:rgba(219, 55, 55, 0.15); }
    .bp3-callout.bp3-intent-danger[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-danger > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-danger .bp3-heading{
      color:#c23030; }
    .bp3-dark .bp3-callout.bp3-intent-danger{
      background-color:rgba(219, 55, 55, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-danger[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-danger > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-danger .bp3-heading{
        color:#ff7373; }
  .bp3-running-text .bp3-callout{
    margin:20px 0; }
.bp3-card{
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
  background-color:#ffffff;
  padding:20px;
  -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-card.bp3-dark,
  .bp3-dark .bp3-card{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
    background-color:#30404d; }

.bp3-elevation-0{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }
  .bp3-elevation-0.bp3-dark,
  .bp3-dark .bp3-elevation-0{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }

.bp3-elevation-1{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-1.bp3-dark,
  .bp3-dark .bp3-elevation-1{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-elevation-2{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 1px 1px rgba(16, 22, 26, 0.2), 0 2px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 1px 1px rgba(16, 22, 26, 0.2), 0 2px 6px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-2.bp3-dark,
  .bp3-dark .bp3-elevation-2{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.4), 0 2px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.4), 0 2px 6px rgba(16, 22, 26, 0.4); }

.bp3-elevation-3{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-3.bp3-dark,
  .bp3-dark .bp3-elevation-3{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }

.bp3-elevation-4{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-4.bp3-dark,
  .bp3-dark .bp3-elevation-4{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4); }

.bp3-card.bp3-interactive:hover{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  cursor:pointer; }
  .bp3-card.bp3-interactive:hover.bp3-dark,
  .bp3-dark .bp3-card.bp3-interactive:hover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }

.bp3-card.bp3-interactive:active{
  opacity:0.9;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  -webkit-transition-duration:0;
          transition-duration:0; }
  .bp3-card.bp3-interactive:active.bp3-dark,
  .bp3-dark .bp3-card.bp3-interactive:active{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-collapse{
  height:0;
  overflow-y:hidden;
  -webkit-transition:height 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:height 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-collapse .bp3-collapse-body{
    -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-collapse .bp3-collapse-body[aria-hidden="true"]{
      display:none; }

.bp3-context-menu .bp3-popover-target{
  display:block; }

.bp3-context-menu-popover-target{
  position:fixed; }

.bp3-divider{
  margin:5px;
  border-right:1px solid rgba(16, 22, 26, 0.15);
  border-bottom:1px solid rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-divider{
    border-color:rgba(16, 22, 26, 0.4); }
.bp3-dialog-container{
  opacity:1;
  -webkit-transform:scale(1);
          transform:scale(1);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  width:100%;
  min-height:100%;
  pointer-events:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-dialog-container.bp3-overlay-enter > .bp3-dialog, .bp3-dialog-container.bp3-overlay-appear > .bp3-dialog{
    opacity:0;
    -webkit-transform:scale(0.5);
            transform:scale(0.5); }
  .bp3-dialog-container.bp3-overlay-enter-active > .bp3-dialog, .bp3-dialog-container.bp3-overlay-appear-active > .bp3-dialog{
    opacity:1;
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-property:opacity, -webkit-transform;
    transition-property:opacity, -webkit-transform;
    transition-property:opacity, transform;
    transition-property:opacity, transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-dialog-container.bp3-overlay-exit > .bp3-dialog{
    opacity:1;
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-dialog-container.bp3-overlay-exit-active > .bp3-dialog{
    opacity:0;
    -webkit-transform:scale(0.5);
            transform:scale(0.5);
    -webkit-transition-property:opacity, -webkit-transform;
    transition-property:opacity, -webkit-transform;
    transition-property:opacity, transform;
    transition-property:opacity, transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }

.bp3-dialog{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:30px 0;
  border-radius:6px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  background:#ebf1f5;
  width:500px;
  padding-bottom:20px;
  pointer-events:all;
  -webkit-user-select:text;
     -moz-user-select:text;
      -ms-user-select:text;
          user-select:text; }
  .bp3-dialog:focus{
    outline:0; }
  .bp3-dialog.bp3-dark,
  .bp3-dark .bp3-dialog{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    background:#293742;
    color:#f5f8fa; }

.bp3-dialog-header{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  border-radius:6px 6px 0 0;
  -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
  background:#ffffff;
  min-height:40px;
  padding-right:5px;
  padding-left:20px; }
  .bp3-dialog-header .bp3-icon-large,
  .bp3-dialog-header .bp3-icon{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    margin-right:10px;
    color:#5c7080; }
  .bp3-dialog-header .bp3-heading{
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    margin:0;
    line-height:inherit; }
    .bp3-dialog-header .bp3-heading:last-child{
      margin-right:20px; }
  .bp3-dark .bp3-dialog-header{
    -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
    background:#30404d; }
    .bp3-dark .bp3-dialog-header .bp3-icon-large,
    .bp3-dark .bp3-dialog-header .bp3-icon{
      color:#a7b6c2; }

.bp3-dialog-body{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  margin:20px;
  line-height:18px; }

.bp3-dialog-footer{
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  margin:0 20px; }

.bp3-dialog-footer-actions{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:end;
      -ms-flex-pack:end;
          justify-content:flex-end; }
  .bp3-dialog-footer-actions .bp3-button{
    margin-left:10px; }
.bp3-drawer{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:0;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  background:#ffffff;
  padding:0; }
  .bp3-drawer:focus{
    outline:0; }
  .bp3-drawer.bp3-position-top{
    top:0;
    right:0;
    left:0;
    height:50%; }
    .bp3-drawer.bp3-position-top.bp3-overlay-enter, .bp3-drawer.bp3-position-top.bp3-overlay-appear{
      -webkit-transform:translateY(-100%);
              transform:translateY(-100%); }
    .bp3-drawer.bp3-position-top.bp3-overlay-enter-active, .bp3-drawer.bp3-position-top.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer.bp3-position-top.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer.bp3-position-top.bp3-overlay-exit-active{
      -webkit-transform:translateY(-100%);
              transform:translateY(-100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer.bp3-position-bottom{
    right:0;
    bottom:0;
    left:0;
    height:50%; }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-enter, .bp3-drawer.bp3-position-bottom.bp3-overlay-appear{
      -webkit-transform:translateY(100%);
              transform:translateY(100%); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-enter-active, .bp3-drawer.bp3-position-bottom.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-exit-active{
      -webkit-transform:translateY(100%);
              transform:translateY(100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer.bp3-position-left{
    top:0;
    bottom:0;
    left:0;
    width:50%; }
    .bp3-drawer.bp3-position-left.bp3-overlay-enter, .bp3-drawer.bp3-position-left.bp3-overlay-appear{
      -webkit-transform:translateX(-100%);
              transform:translateX(-100%); }
    .bp3-drawer.bp3-position-left.bp3-overlay-enter-active, .bp3-drawer.bp3-position-left.bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer.bp3-position-left.bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer.bp3-position-left.bp3-overlay-exit-active{
      -webkit-transform:translateX(-100%);
              transform:translateX(-100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer.bp3-position-right{
    top:0;
    right:0;
    bottom:0;
    width:50%; }
    .bp3-drawer.bp3-position-right.bp3-overlay-enter, .bp3-drawer.bp3-position-right.bp3-overlay-appear{
      -webkit-transform:translateX(100%);
              transform:translateX(100%); }
    .bp3-drawer.bp3-position-right.bp3-overlay-enter-active, .bp3-drawer.bp3-position-right.bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer.bp3-position-right.bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer.bp3-position-right.bp3-overlay-exit-active{
      -webkit-transform:translateX(100%);
              transform:translateX(100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
  .bp3-position-right):not(.bp3-vertical){
    top:0;
    right:0;
    bottom:0;
    width:50%; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-enter, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-appear{
      -webkit-transform:translateX(100%);
              transform:translateX(100%); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-enter-active, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-exit-active{
      -webkit-transform:translateX(100%);
              transform:translateX(100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
  .bp3-position-right).bp3-vertical{
    right:0;
    bottom:0;
    left:0;
    height:50%; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-enter, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-appear{
      -webkit-transform:translateY(100%);
              transform:translateY(100%); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-enter-active, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-exit-active{
      -webkit-transform:translateY(100%);
              transform:translateY(100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer.bp3-dark,
  .bp3-dark .bp3-drawer{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    background:#30404d;
    color:#f5f8fa; }

.bp3-drawer-header{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  position:relative;
  border-radius:0;
  -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
  min-height:40px;
  padding:5px;
  padding-left:20px; }
  .bp3-drawer-header .bp3-icon-large,
  .bp3-drawer-header .bp3-icon{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    margin-right:10px;
    color:#5c7080; }
  .bp3-drawer-header .bp3-heading{
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    margin:0;
    line-height:inherit; }
    .bp3-drawer-header .bp3-heading:last-child{
      margin-right:20px; }
  .bp3-dark .bp3-drawer-header{
    -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:0 1px 0 rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-drawer-header .bp3-icon-large,
    .bp3-dark .bp3-drawer-header .bp3-icon{
      color:#a7b6c2; }

.bp3-drawer-body{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  overflow:auto;
  line-height:18px; }

.bp3-drawer-footer{
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  position:relative;
  -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
  padding:10px 20px; }
  .bp3-dark .bp3-drawer-footer{
    -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.4); }
.bp3-editable-text{
  display:inline-block;
  position:relative;
  cursor:text;
  max-width:100%;
  vertical-align:top;
  white-space:nowrap; }
  .bp3-editable-text::before{
    position:absolute;
    top:-3px;
    right:-3px;
    bottom:-3px;
    left:-3px;
    border-radius:3px;
    content:"";
    -webkit-transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-editable-text:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-editable-text.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
    background-color:#ffffff; }
  .bp3-editable-text.bp3-disabled::before{
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-editable-text.bp3-intent-primary .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-primary .bp3-editable-text-content{
    color:#137cbd; }
  .bp3-editable-text.bp3-intent-primary:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(19, 124, 189, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(19, 124, 189, 0.4); }
  .bp3-editable-text.bp3-intent-primary.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-success .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-success .bp3-editable-text-content{
    color:#0f9960; }
  .bp3-editable-text.bp3-intent-success:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px rgba(15, 153, 96, 0.4);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px rgba(15, 153, 96, 0.4); }
  .bp3-editable-text.bp3-intent-success.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-warning .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-warning .bp3-editable-text-content{
    color:#d9822b; }
  .bp3-editable-text.bp3-intent-warning:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px rgba(217, 130, 43, 0.4);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px rgba(217, 130, 43, 0.4); }
  .bp3-editable-text.bp3-intent-warning.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-danger .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-danger .bp3-editable-text-content{
    color:#db3737; }
  .bp3-editable-text.bp3-intent-danger:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px rgba(219, 55, 55, 0.4);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px rgba(219, 55, 55, 0.4); }
  .bp3-editable-text.bp3-intent-danger.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-editable-text:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(255, 255, 255, 0.15); }
  .bp3-dark .bp3-editable-text.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    background-color:rgba(16, 22, 26, 0.3); }
  .bp3-dark .bp3-editable-text.bp3-disabled::before{
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-dark .bp3-editable-text.bp3-intent-primary .bp3-editable-text-content{
    color:#48aff0; }
  .bp3-dark .bp3-editable-text.bp3-intent-primary:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(72, 175, 240, 0), 0 0 0 0 rgba(72, 175, 240, 0), inset 0 0 0 1px rgba(72, 175, 240, 0.4);
            box-shadow:0 0 0 0 rgba(72, 175, 240, 0), 0 0 0 0 rgba(72, 175, 240, 0), inset 0 0 0 1px rgba(72, 175, 240, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-primary.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #48aff0, 0 0 0 3px rgba(72, 175, 240, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #48aff0, 0 0 0 3px rgba(72, 175, 240, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-success .bp3-editable-text-content{
    color:#3dcc91; }
  .bp3-dark .bp3-editable-text.bp3-intent-success:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(61, 204, 145, 0), 0 0 0 0 rgba(61, 204, 145, 0), inset 0 0 0 1px rgba(61, 204, 145, 0.4);
            box-shadow:0 0 0 0 rgba(61, 204, 145, 0), 0 0 0 0 rgba(61, 204, 145, 0), inset 0 0 0 1px rgba(61, 204, 145, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-success.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #3dcc91, 0 0 0 3px rgba(61, 204, 145, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #3dcc91, 0 0 0 3px rgba(61, 204, 145, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-warning .bp3-editable-text-content{
    color:#ffb366; }
  .bp3-dark .bp3-editable-text.bp3-intent-warning:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(255, 179, 102, 0), 0 0 0 0 rgba(255, 179, 102, 0), inset 0 0 0 1px rgba(255, 179, 102, 0.4);
            box-shadow:0 0 0 0 rgba(255, 179, 102, 0), 0 0 0 0 rgba(255, 179, 102, 0), inset 0 0 0 1px rgba(255, 179, 102, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-warning.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #ffb366, 0 0 0 3px rgba(255, 179, 102, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #ffb366, 0 0 0 3px rgba(255, 179, 102, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-danger .bp3-editable-text-content{
    color:#ff7373; }
  .bp3-dark .bp3-editable-text.bp3-intent-danger:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(255, 115, 115, 0), 0 0 0 0 rgba(255, 115, 115, 0), inset 0 0 0 1px rgba(255, 115, 115, 0.4);
            box-shadow:0 0 0 0 rgba(255, 115, 115, 0), 0 0 0 0 rgba(255, 115, 115, 0), inset 0 0 0 1px rgba(255, 115, 115, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-danger.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #ff7373, 0 0 0 3px rgba(255, 115, 115, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #ff7373, 0 0 0 3px rgba(255, 115, 115, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-editable-text-input,
.bp3-editable-text-content{
  display:inherit;
  position:relative;
  min-width:inherit;
  max-width:inherit;
  vertical-align:top;
  text-transform:inherit;
  letter-spacing:inherit;
  color:inherit;
  font:inherit;
  resize:none; }

.bp3-editable-text-input{
  border:none;
  -webkit-box-shadow:none;
          box-shadow:none;
  background:none;
  width:100%;
  padding:0;
  white-space:pre-wrap; }
  .bp3-editable-text-input::-webkit-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-editable-text-input::-moz-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-editable-text-input:-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-editable-text-input::-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-editable-text-input::placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-editable-text-input:focus{
    outline:none; }
  .bp3-editable-text-input::-ms-clear{
    display:none; }

.bp3-editable-text-content{
  overflow:hidden;
  padding-right:2px;
  text-overflow:ellipsis;
  white-space:pre; }
  .bp3-editable-text-editing > .bp3-editable-text-content{
    position:absolute;
    left:0;
    visibility:hidden; }
  .bp3-editable-text-placeholder > .bp3-editable-text-content{
    color:rgba(92, 112, 128, 0.6); }
    .bp3-dark .bp3-editable-text-placeholder > .bp3-editable-text-content{
      color:rgba(167, 182, 194, 0.6); }

.bp3-editable-text.bp3-multiline{
  display:block; }
  .bp3-editable-text.bp3-multiline .bp3-editable-text-content{
    overflow:auto;
    white-space:pre-wrap;
    word-wrap:break-word; }
.bp3-control-group{
  -webkit-transform:translateZ(0);
          transform:translateZ(0);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:stretch;
      -ms-flex-align:stretch;
          align-items:stretch; }
  .bp3-control-group > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-control-group > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-control-group .bp3-button,
  .bp3-control-group .bp3-html-select,
  .bp3-control-group .bp3-input,
  .bp3-control-group .bp3-select{
    position:relative; }
  .bp3-control-group .bp3-input{
    z-index:2;
    border-radius:inherit; }
    .bp3-control-group .bp3-input:focus{
      z-index:14;
      border-radius:3px; }
    .bp3-control-group .bp3-input[class*="bp3-intent"]{
      z-index:13; }
      .bp3-control-group .bp3-input[class*="bp3-intent"]:focus{
        z-index:15; }
    .bp3-control-group .bp3-input[readonly], .bp3-control-group .bp3-input:disabled, .bp3-control-group .bp3-input.bp3-disabled{
      z-index:1; }
  .bp3-control-group .bp3-input-group[class*="bp3-intent"] .bp3-input{
    z-index:13; }
    .bp3-control-group .bp3-input-group[class*="bp3-intent"] .bp3-input:focus{
      z-index:15; }
  .bp3-control-group .bp3-button,
  .bp3-control-group .bp3-html-select select,
  .bp3-control-group .bp3-select select{
    -webkit-transform:translateZ(0);
            transform:translateZ(0);
    z-index:4;
    border-radius:inherit; }
    .bp3-control-group .bp3-button:focus,
    .bp3-control-group .bp3-html-select select:focus,
    .bp3-control-group .bp3-select select:focus{
      z-index:5; }
    .bp3-control-group .bp3-button:hover,
    .bp3-control-group .bp3-html-select select:hover,
    .bp3-control-group .bp3-select select:hover{
      z-index:6; }
    .bp3-control-group .bp3-button:active,
    .bp3-control-group .bp3-html-select select:active,
    .bp3-control-group .bp3-select select:active{
      z-index:7; }
    .bp3-control-group .bp3-button[readonly], .bp3-control-group .bp3-button:disabled, .bp3-control-group .bp3-button.bp3-disabled,
    .bp3-control-group .bp3-html-select select[readonly],
    .bp3-control-group .bp3-html-select select:disabled,
    .bp3-control-group .bp3-html-select select.bp3-disabled,
    .bp3-control-group .bp3-select select[readonly],
    .bp3-control-group .bp3-select select:disabled,
    .bp3-control-group .bp3-select select.bp3-disabled{
      z-index:3; }
    .bp3-control-group .bp3-button[class*="bp3-intent"],
    .bp3-control-group .bp3-html-select select[class*="bp3-intent"],
    .bp3-control-group .bp3-select select[class*="bp3-intent"]{
      z-index:9; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:focus,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:focus,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:focus{
        z-index:10; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:hover,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:hover,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:hover{
        z-index:11; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:active,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:active,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:active{
        z-index:12; }
      .bp3-control-group .bp3-button[class*="bp3-intent"][readonly], .bp3-control-group .bp3-button[class*="bp3-intent"]:disabled, .bp3-control-group .bp3-button[class*="bp3-intent"].bp3-disabled,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"][readonly],
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:disabled,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"].bp3-disabled,
      .bp3-control-group .bp3-select select[class*="bp3-intent"][readonly],
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:disabled,
      .bp3-control-group .bp3-select select[class*="bp3-intent"].bp3-disabled{
        z-index:8; }
  .bp3-control-group .bp3-input-group > .bp3-icon,
  .bp3-control-group .bp3-input-group > .bp3-button,
  .bp3-control-group .bp3-input-group > .bp3-input-action{
    z-index:16; }
  .bp3-control-group .bp3-select::after,
  .bp3-control-group .bp3-html-select::after,
  .bp3-control-group .bp3-select > .bp3-icon,
  .bp3-control-group .bp3-html-select > .bp3-icon{
    z-index:17; }
  .bp3-control-group:not(.bp3-vertical) > *{
    margin-right:-1px; }
  .bp3-dark .bp3-control-group:not(.bp3-vertical) > *{
    margin-right:0; }
  .bp3-dark .bp3-control-group:not(.bp3-vertical) > .bp3-button + .bp3-button{
    margin-left:1px; }
  .bp3-control-group .bp3-popover-wrapper,
  .bp3-control-group .bp3-popover-target{
    border-radius:inherit; }
  .bp3-control-group > :first-child{
    border-radius:3px 0 0 3px; }
  .bp3-control-group > :last-child{
    margin-right:0;
    border-radius:0 3px 3px 0; }
  .bp3-control-group > :only-child{
    margin-right:0;
    border-radius:3px; }
  .bp3-control-group .bp3-input-group .bp3-button{
    border-radius:3px; }
  .bp3-control-group > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-control-group.bp3-fill > *:not(.bp3-fixed){
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-control-group.bp3-vertical{
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column; }
    .bp3-control-group.bp3-vertical > *{
      margin-top:-1px; }
    .bp3-control-group.bp3-vertical > :first-child{
      margin-top:0;
      border-radius:3px 3px 0 0; }
    .bp3-control-group.bp3-vertical > :last-child{
      border-radius:0 0 3px 3px; }
.bp3-control{
  display:block;
  position:relative;
  margin-bottom:10px;
  cursor:pointer;
  text-transform:none; }
  .bp3-control input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
  .bp3-control:hover input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#106ba3; }
  .bp3-control input:not(:disabled):active:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background:#0e5a8a; }
  .bp3-control input:disabled:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(19, 124, 189, 0.5); }
  .bp3-dark .bp3-control input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control:hover input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background-color:#106ba3; }
  .bp3-dark .bp3-control input:not(:disabled):active:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#0e5a8a; }
  .bp3-dark .bp3-control input:disabled:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(14, 90, 138, 0.5); }
  .bp3-control:not(.bp3-align-right){
    padding-left:26px; }
    .bp3-control:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-26px; }
  .bp3-control.bp3-align-right{
    padding-right:26px; }
    .bp3-control.bp3-align-right .bp3-control-indicator{
      margin-right:-26px; }
  .bp3-control.bp3-disabled{
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-control.bp3-inline{
    display:inline-block;
    margin-right:20px; }
  .bp3-control input{
    position:absolute;
    top:0;
    left:0;
    opacity:0;
    z-index:-1; }
  .bp3-control .bp3-control-indicator{
    display:inline-block;
    position:relative;
    margin-top:-3px;
    margin-right:10px;
    border:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-clip:padding-box;
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    cursor:pointer;
    width:1em;
    height:1em;
    vertical-align:middle;
    font-size:16px;
    -webkit-user-select:none;
       -moz-user-select:none;
        -ms-user-select:none;
            user-select:none; }
    .bp3-control .bp3-control-indicator::before{
      display:block;
      width:1em;
      height:1em;
      content:""; }
  .bp3-control:hover .bp3-control-indicator{
    background-color:#ebf1f5; }
  .bp3-control input:not(:disabled):active ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background:#d8e1e8; }
  .bp3-control input:disabled ~ .bp3-control-indicator{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(206, 217, 224, 0.5);
    cursor:not-allowed; }
  .bp3-control input:focus ~ .bp3-control-indicator{
    outline:rgba(19, 124, 189, 0.6) auto 2px;
    outline-offset:2px;
    -moz-outline-radius:6px; }
  .bp3-control.bp3-align-right .bp3-control-indicator{
    float:right;
    margin-top:1px;
    margin-left:10px; }
  .bp3-control.bp3-large{
    font-size:16px; }
    .bp3-control.bp3-large:not(.bp3-align-right){
      padding-left:30px; }
      .bp3-control.bp3-large:not(.bp3-align-right) .bp3-control-indicator{
        margin-left:-30px; }
    .bp3-control.bp3-large.bp3-align-right{
      padding-right:30px; }
      .bp3-control.bp3-large.bp3-align-right .bp3-control-indicator{
        margin-right:-30px; }
    .bp3-control.bp3-large .bp3-control-indicator{
      font-size:20px; }
    .bp3-control.bp3-large.bp3-align-right .bp3-control-indicator{
      margin-top:0; }
  .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
  .bp3-control.bp3-checkbox:hover input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#106ba3; }
  .bp3-control.bp3-checkbox input:not(:disabled):active:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background:#0e5a8a; }
  .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(19, 124, 189, 0.5); }
  .bp3-dark .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-checkbox:hover input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background-color:#106ba3; }
  .bp3-dark .bp3-control.bp3-checkbox input:not(:disabled):active:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#0e5a8a; }
  .bp3-dark .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(14, 90, 138, 0.5); }
  .bp3-control.bp3-checkbox .bp3-control-indicator{
    border-radius:3px; }
  .bp3-control.bp3-checkbox input:checked ~ .bp3-control-indicator::before{
    background-image:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M12 5c-.28 0-.53.11-.71.29L7 9.59l-2.29-2.3a1.003 1.003 0 0 0-1.42 1.42l3 3c.18.18.43.29.71.29s.53-.11.71-.29l5-5A1.003 1.003 0 0 0 12 5z' fill='white'/%3e%3c/svg%3e"); }
  .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator::before{
    background-image:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M11 7H5c-.55 0-1 .45-1 1s.45 1 1 1h6c.55 0 1-.45 1-1s-.45-1-1-1z' fill='white'/%3e%3c/svg%3e"); }
  .bp3-control.bp3-radio .bp3-control-indicator{
    border-radius:50%; }
  .bp3-control.bp3-radio input:checked ~ .bp3-control-indicator::before{
    background-image:radial-gradient(#ffffff, #ffffff 28%, transparent 32%); }
  .bp3-control.bp3-radio input:checked:disabled ~ .bp3-control-indicator::before{
    opacity:0.5; }
  .bp3-control.bp3-radio input:focus ~ .bp3-control-indicator{
    -moz-outline-radius:16px; }
  .bp3-control.bp3-switch input ~ .bp3-control-indicator{
    background:rgba(167, 182, 194, 0.5); }
  .bp3-control.bp3-switch:hover input ~ .bp3-control-indicator{
    background:rgba(115, 134, 148, 0.5); }
  .bp3-control.bp3-switch input:not(:disabled):active ~ .bp3-control-indicator{
    background:rgba(92, 112, 128, 0.5); }
  .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator{
    background:rgba(206, 217, 224, 0.5); }
    .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator::before{
      background:rgba(255, 255, 255, 0.8); }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator{
    background:#137cbd; }
  .bp3-control.bp3-switch:hover input:checked ~ .bp3-control-indicator{
    background:#106ba3; }
  .bp3-control.bp3-switch input:checked:not(:disabled):active ~ .bp3-control-indicator{
    background:#0e5a8a; }
  .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator{
    background:rgba(19, 124, 189, 0.5); }
    .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator::before{
      background:rgba(255, 255, 255, 0.8); }
  .bp3-control.bp3-switch:not(.bp3-align-right){
    padding-left:38px; }
    .bp3-control.bp3-switch:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-38px; }
  .bp3-control.bp3-switch.bp3-align-right{
    padding-right:38px; }
    .bp3-control.bp3-switch.bp3-align-right .bp3-control-indicator{
      margin-right:-38px; }
  .bp3-control.bp3-switch .bp3-control-indicator{
    border:none;
    border-radius:1.75em;
    -webkit-box-shadow:none !important;
            box-shadow:none !important;
    width:auto;
    min-width:1.75em;
    -webkit-transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-control.bp3-switch .bp3-control-indicator::before{
      position:absolute;
      left:0;
      margin:2px;
      border-radius:50%;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
      background:#ffffff;
      width:calc(1em - 4px);
      height:calc(1em - 4px);
      -webkit-transition:left 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
      transition:left 100ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator::before{
    left:calc(100% - 1em); }
  .bp3-control.bp3-switch.bp3-large:not(.bp3-align-right){
    padding-left:45px; }
    .bp3-control.bp3-switch.bp3-large:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-45px; }
  .bp3-control.bp3-switch.bp3-large.bp3-align-right{
    padding-right:45px; }
    .bp3-control.bp3-switch.bp3-large.bp3-align-right .bp3-control-indicator{
      margin-right:-45px; }
  .bp3-dark .bp3-control.bp3-switch input ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.5); }
  .bp3-dark .bp3-control.bp3-switch:hover input ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.7); }
  .bp3-dark .bp3-control.bp3-switch input:not(:disabled):active ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.9); }
  .bp3-dark .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator{
    background:rgba(57, 75, 89, 0.5); }
    .bp3-dark .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator::before{
      background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator{
    background:#137cbd; }
  .bp3-dark .bp3-control.bp3-switch:hover input:checked ~ .bp3-control-indicator{
    background:#106ba3; }
  .bp3-dark .bp3-control.bp3-switch input:checked:not(:disabled):active ~ .bp3-control-indicator{
    background:#0e5a8a; }
  .bp3-dark .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator{
    background:rgba(14, 90, 138, 0.5); }
    .bp3-dark .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator::before{
      background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch .bp3-control-indicator::before{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background:#394b59; }
  .bp3-dark .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator::before{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-control.bp3-switch .bp3-switch-inner-text{
    text-align:center;
    font-size:0.7em; }
  .bp3-control.bp3-switch .bp3-control-indicator-child:first-child{
    visibility:hidden;
    margin-right:1.2em;
    margin-left:0.5em;
    line-height:0; }
  .bp3-control.bp3-switch .bp3-control-indicator-child:last-child{
    visibility:visible;
    margin-right:0.5em;
    margin-left:1.2em;
    line-height:1em; }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator .bp3-control-indicator-child:first-child{
    visibility:visible;
    line-height:1em; }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator .bp3-control-indicator-child:last-child{
    visibility:hidden;
    line-height:0; }
  .bp3-dark .bp3-control{
    color:#f5f8fa; }
    .bp3-dark .bp3-control.bp3-disabled{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-control .bp3-control-indicator{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      background-color:#394b59;
      background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
      background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0)); }
    .bp3-dark .bp3-control:hover .bp3-control-indicator{
      background-color:#30404d; }
    .bp3-dark .bp3-control input:not(:disabled):active ~ .bp3-control-indicator{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background:#202b33; }
    .bp3-dark .bp3-control input:disabled ~ .bp3-control-indicator{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(57, 75, 89, 0.5);
      cursor:not-allowed; }
    .bp3-dark .bp3-control.bp3-checkbox input:disabled:checked ~ .bp3-control-indicator, .bp3-dark .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
      color:rgba(167, 182, 194, 0.6); }
.bp3-file-input{
  display:inline-block;
  position:relative;
  cursor:pointer;
  height:30px; }
  .bp3-file-input input{
    opacity:0;
    margin:0;
    min-width:200px; }
    .bp3-file-input input:disabled + .bp3-file-upload-input,
    .bp3-file-input input.bp3-disabled + .bp3-file-upload-input{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(206, 217, 224, 0.5);
      cursor:not-allowed;
      color:rgba(92, 112, 128, 0.6);
      resize:none; }
      .bp3-file-input input:disabled + .bp3-file-upload-input::after,
      .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after{
        outline:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        background-color:rgba(206, 217, 224, 0.5);
        background-image:none;
        cursor:not-allowed;
        color:rgba(92, 112, 128, 0.6); }
        .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active, .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active:hover,
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active,
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active:hover{
          background:rgba(206, 217, 224, 0.7); }
      .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input, .bp3-dark
      .bp3-file-input input.bp3-disabled + .bp3-file-upload-input{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:rgba(57, 75, 89, 0.5);
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input::after, .bp3-dark
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after{
          -webkit-box-shadow:none;
                  box-shadow:none;
          background-color:rgba(57, 75, 89, 0.5);
          background-image:none;
          color:rgba(167, 182, 194, 0.6); }
          .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active, .bp3-dark
          .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active{
            background:rgba(57, 75, 89, 0.7); }
  .bp3-file-input.bp3-file-input-has-selection .bp3-file-upload-input{
    color:#182026; }
  .bp3-dark .bp3-file-input.bp3-file-input-has-selection .bp3-file-upload-input{
    color:#f5f8fa; }
  .bp3-file-input.bp3-fill{
    width:100%; }
  .bp3-file-input.bp3-large,
  .bp3-large .bp3-file-input{
    height:40px; }
  .bp3-file-input .bp3-file-upload-input-custom-text::after{
    content:attr(bp3-button-text); }

.bp3-file-upload-input{
  outline:none;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
  background:#ffffff;
  height:30px;
  padding:0 10px;
  vertical-align:middle;
  line-height:30px;
  color:#182026;
  font-size:14px;
  font-weight:400;
  -webkit-transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  -webkit-appearance:none;
     -moz-appearance:none;
          appearance:none;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  position:absolute;
  top:0;
  right:0;
  left:0;
  padding-right:80px;
  color:rgba(92, 112, 128, 0.6);
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-file-upload-input::-webkit-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-file-upload-input::-moz-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-file-upload-input:-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-file-upload-input::-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-file-upload-input::placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-file-upload-input:focus, .bp3-file-upload-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-file-upload-input[type="search"], .bp3-file-upload-input.bp3-round{
    border-radius:30px;
    -webkit-box-sizing:border-box;
            box-sizing:border-box;
    padding-left:10px; }
  .bp3-file-upload-input[readonly]{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-file-upload-input:disabled, .bp3-file-upload-input.bp3-disabled{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(206, 217, 224, 0.5);
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6);
    resize:none; }
  .bp3-file-upload-input::after{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    color:#182026;
    min-width:24px;
    min-height:24px;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    position:absolute;
    top:0;
    right:0;
    margin:3px;
    border-radius:3px;
    width:70px;
    text-align:center;
    line-height:24px;
    content:"Browse"; }
    .bp3-file-upload-input::after:hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
      background-clip:padding-box;
      background-color:#ebf1f5; }
    .bp3-file-upload-input::after:active, .bp3-file-upload-input::after.bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#d8e1e8;
      background-image:none; }
    .bp3-file-upload-input::after:disabled, .bp3-file-upload-input::after.bp3-disabled{
      outline:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(206, 217, 224, 0.5);
      background-image:none;
      cursor:not-allowed;
      color:rgba(92, 112, 128, 0.6); }
      .bp3-file-upload-input::after:disabled.bp3-active, .bp3-file-upload-input::after:disabled.bp3-active:hover, .bp3-file-upload-input::after.bp3-disabled.bp3-active, .bp3-file-upload-input::after.bp3-disabled.bp3-active:hover{
        background:rgba(206, 217, 224, 0.7); }
  .bp3-file-upload-input:hover::after{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-clip:padding-box;
    background-color:#ebf1f5; }
  .bp3-file-upload-input:active::after{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#d8e1e8;
    background-image:none; }
  .bp3-large .bp3-file-upload-input{
    height:40px;
    line-height:40px;
    font-size:16px;
    padding-right:95px; }
    .bp3-large .bp3-file-upload-input[type="search"], .bp3-large .bp3-file-upload-input.bp3-round{
      padding:0 15px; }
    .bp3-large .bp3-file-upload-input::after{
      min-width:30px;
      min-height:30px;
      margin:5px;
      width:85px;
      line-height:30px; }
  .bp3-dark .bp3-file-upload-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    background:rgba(16, 22, 26, 0.3);
    color:#f5f8fa;
    color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input:disabled, .bp3-dark .bp3-file-upload-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(57, 75, 89, 0.5);
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::after{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      background-color:#394b59;
      background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
      background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
      color:#f5f8fa; }
      .bp3-dark .bp3-file-upload-input::after:hover, .bp3-dark .bp3-file-upload-input::after:active, .bp3-dark .bp3-file-upload-input::after.bp3-active{
        color:#f5f8fa; }
      .bp3-dark .bp3-file-upload-input::after:hover{
        -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
        background-color:#30404d; }
      .bp3-dark .bp3-file-upload-input::after:active, .bp3-dark .bp3-file-upload-input::after.bp3-active{
        -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
                box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
        background-color:#202b33;
        background-image:none; }
      .bp3-dark .bp3-file-upload-input::after:disabled, .bp3-dark .bp3-file-upload-input::after.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none;
        background-color:rgba(57, 75, 89, 0.5);
        background-image:none;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-file-upload-input::after:disabled.bp3-active, .bp3-dark .bp3-file-upload-input::after.bp3-disabled.bp3-active{
          background:rgba(57, 75, 89, 0.7); }
      .bp3-dark .bp3-file-upload-input::after .bp3-button-spinner .bp3-spinner-head{
        background:rgba(16, 22, 26, 0.5);
        stroke:#8a9ba8; }
    .bp3-dark .bp3-file-upload-input:hover::after{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      background-color:#30404d; }
    .bp3-dark .bp3-file-upload-input:active::after{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#202b33;
      background-image:none; }

.bp3-file-upload-input::after{
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
.bp3-form-group{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:0 0 15px; }
  .bp3-form-group label.bp3-label{
    margin-bottom:5px; }
  .bp3-form-group .bp3-control{
    margin-top:7px; }
  .bp3-form-group .bp3-form-helper-text{
    margin-top:5px;
    color:#5c7080;
    font-size:12px; }
  .bp3-form-group.bp3-intent-primary .bp3-form-helper-text{
    color:#106ba3; }
  .bp3-form-group.bp3-intent-success .bp3-form-helper-text{
    color:#0d8050; }
  .bp3-form-group.bp3-intent-warning .bp3-form-helper-text{
    color:#bf7326; }
  .bp3-form-group.bp3-intent-danger .bp3-form-helper-text{
    color:#c23030; }
  .bp3-form-group.bp3-inline{
    -webkit-box-orient:horizontal;
    -webkit-box-direction:normal;
        -ms-flex-direction:row;
            flex-direction:row;
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start; }
    .bp3-form-group.bp3-inline.bp3-large label.bp3-label{
      margin:0 10px 0 0;
      line-height:40px; }
    .bp3-form-group.bp3-inline label.bp3-label{
      margin:0 10px 0 0;
      line-height:30px; }
  .bp3-form-group.bp3-disabled .bp3-label,
  .bp3-form-group.bp3-disabled .bp3-text-muted,
  .bp3-form-group.bp3-disabled .bp3-form-helper-text{
    color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-dark .bp3-form-group.bp3-intent-primary .bp3-form-helper-text{
    color:#48aff0; }
  .bp3-dark .bp3-form-group.bp3-intent-success .bp3-form-helper-text{
    color:#3dcc91; }
  .bp3-dark .bp3-form-group.bp3-intent-warning .bp3-form-helper-text{
    color:#ffb366; }
  .bp3-dark .bp3-form-group.bp3-intent-danger .bp3-form-helper-text{
    color:#ff7373; }
  .bp3-dark .bp3-form-group .bp3-form-helper-text{
    color:#a7b6c2; }
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-label,
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-text-muted,
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-form-helper-text{
    color:rgba(167, 182, 194, 0.6) !important; }
.bp3-input-group{
  display:block;
  position:relative; }
  .bp3-input-group .bp3-input{
    position:relative;
    width:100%; }
    .bp3-input-group .bp3-input:not(:first-child){
      padding-left:30px; }
    .bp3-input-group .bp3-input:not(:last-child){
      padding-right:30px; }
  .bp3-input-group .bp3-input-action,
  .bp3-input-group > .bp3-button,
  .bp3-input-group > .bp3-icon{
    position:absolute;
    top:0; }
    .bp3-input-group .bp3-input-action:first-child,
    .bp3-input-group > .bp3-button:first-child,
    .bp3-input-group > .bp3-icon:first-child{
      left:0; }
    .bp3-input-group .bp3-input-action:last-child,
    .bp3-input-group > .bp3-button:last-child,
    .bp3-input-group > .bp3-icon:last-child{
      right:0; }
  .bp3-input-group .bp3-button{
    min-width:24px;
    min-height:24px;
    margin:3px;
    padding:0 7px; }
    .bp3-input-group .bp3-button:empty{
      padding:0; }
  .bp3-input-group > .bp3-icon{
    z-index:1;
    color:#5c7080; }
    .bp3-input-group > .bp3-icon:empty{
      line-height:1;
      font-family:"Icons16", sans-serif;
      font-size:16px;
      font-weight:400;
      font-style:normal;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased; }
  .bp3-input-group > .bp3-icon,
  .bp3-input-group .bp3-input-action > .bp3-spinner{
    margin:7px; }
  .bp3-input-group .bp3-tag{
    margin:5px; }
  .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus),
  .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus){
    color:#5c7080; }
    .bp3-dark .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus), .bp3-dark
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus){
      color:#a7b6c2; }
    .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-standard, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-large,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-standard,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-large{
      color:#5c7080; }
  .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled,
  .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled{
    color:rgba(92, 112, 128, 0.6) !important; }
    .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon-standard, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon-large,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon-standard,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon-large{
      color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-input-group.bp3-disabled{
    cursor:not-allowed; }
    .bp3-input-group.bp3-disabled .bp3-icon{
      color:rgba(92, 112, 128, 0.6); }
  .bp3-input-group.bp3-large .bp3-button{
    min-width:30px;
    min-height:30px;
    margin:5px; }
  .bp3-input-group.bp3-large > .bp3-icon,
  .bp3-input-group.bp3-large .bp3-input-action > .bp3-spinner{
    margin:12px; }
  .bp3-input-group.bp3-large .bp3-input{
    height:40px;
    line-height:40px;
    font-size:16px; }
    .bp3-input-group.bp3-large .bp3-input[type="search"], .bp3-input-group.bp3-large .bp3-input.bp3-round{
      padding:0 15px; }
    .bp3-input-group.bp3-large .bp3-input:not(:first-child){
      padding-left:40px; }
    .bp3-input-group.bp3-large .bp3-input:not(:last-child){
      padding-right:40px; }
  .bp3-input-group.bp3-small .bp3-button{
    min-width:20px;
    min-height:20px;
    margin:2px; }
  .bp3-input-group.bp3-small .bp3-tag{
    min-width:20px;
    min-height:20px;
    margin:2px; }
  .bp3-input-group.bp3-small > .bp3-icon,
  .bp3-input-group.bp3-small .bp3-input-action > .bp3-spinner{
    margin:4px; }
  .bp3-input-group.bp3-small .bp3-input{
    height:24px;
    padding-right:8px;
    padding-left:8px;
    line-height:24px;
    font-size:12px; }
    .bp3-input-group.bp3-small .bp3-input[type="search"], .bp3-input-group.bp3-small .bp3-input.bp3-round{
      padding:0 12px; }
    .bp3-input-group.bp3-small .bp3-input:not(:first-child){
      padding-left:24px; }
    .bp3-input-group.bp3-small .bp3-input:not(:last-child){
      padding-right:24px; }
  .bp3-input-group.bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:100%; }
  .bp3-input-group.bp3-round .bp3-button,
  .bp3-input-group.bp3-round .bp3-input,
  .bp3-input-group.bp3-round .bp3-tag{
    border-radius:30px; }
  .bp3-dark .bp3-input-group .bp3-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-input-group.bp3-disabled .bp3-icon{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-input-group.bp3-intent-primary .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-primary .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-primary .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #137cbd;
              box-shadow:inset 0 0 0 1px #137cbd; }
    .bp3-input-group.bp3-intent-primary .bp3-input:disabled, .bp3-input-group.bp3-intent-primary .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-primary > .bp3-icon{
    color:#106ba3; }
    .bp3-dark .bp3-input-group.bp3-intent-primary > .bp3-icon{
      color:#48aff0; }
  .bp3-input-group.bp3-intent-success .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-success .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-success .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #0f9960;
              box-shadow:inset 0 0 0 1px #0f9960; }
    .bp3-input-group.bp3-intent-success .bp3-input:disabled, .bp3-input-group.bp3-intent-success .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-success > .bp3-icon{
    color:#0d8050; }
    .bp3-dark .bp3-input-group.bp3-intent-success > .bp3-icon{
      color:#3dcc91; }
  .bp3-input-group.bp3-intent-warning .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-warning .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-warning .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #d9822b;
              box-shadow:inset 0 0 0 1px #d9822b; }
    .bp3-input-group.bp3-intent-warning .bp3-input:disabled, .bp3-input-group.bp3-intent-warning .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-warning > .bp3-icon{
    color:#bf7326; }
    .bp3-dark .bp3-input-group.bp3-intent-warning > .bp3-icon{
      color:#ffb366; }
  .bp3-input-group.bp3-intent-danger .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-danger .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-danger .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #db3737;
              box-shadow:inset 0 0 0 1px #db3737; }
    .bp3-input-group.bp3-intent-danger .bp3-input:disabled, .bp3-input-group.bp3-intent-danger .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-danger > .bp3-icon{
    color:#c23030; }
    .bp3-dark .bp3-input-group.bp3-intent-danger > .bp3-icon{
      color:#ff7373; }
.bp3-input{
  outline:none;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
  background:#ffffff;
  height:30px;
  padding:0 10px;
  vertical-align:middle;
  line-height:30px;
  color:#182026;
  font-size:14px;
  font-weight:400;
  -webkit-transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  -webkit-appearance:none;
     -moz-appearance:none;
          appearance:none; }
  .bp3-input::-webkit-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input::-moz-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input:-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input::-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input::placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input:focus, .bp3-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-input[type="search"], .bp3-input.bp3-round{
    border-radius:30px;
    -webkit-box-sizing:border-box;
            box-sizing:border-box;
    padding-left:10px; }
  .bp3-input[readonly]{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-input:disabled, .bp3-input.bp3-disabled{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(206, 217, 224, 0.5);
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6);
    resize:none; }
  .bp3-input.bp3-large{
    height:40px;
    line-height:40px;
    font-size:16px; }
    .bp3-input.bp3-large[type="search"], .bp3-input.bp3-large.bp3-round{
      padding:0 15px; }
  .bp3-input.bp3-small{
    height:24px;
    padding-right:8px;
    padding-left:8px;
    line-height:24px;
    font-size:12px; }
    .bp3-input.bp3-small[type="search"], .bp3-input.bp3-small.bp3-round{
      padding:0 12px; }
  .bp3-input.bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:100%; }
  .bp3-dark .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    background:rgba(16, 22, 26, 0.3);
    color:#f5f8fa; }
    .bp3-dark .bp3-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-input:disabled, .bp3-dark .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(57, 75, 89, 0.5);
      color:rgba(167, 182, 194, 0.6); }
  .bp3-input.bp3-intent-primary{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-primary:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-primary[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #137cbd;
              box-shadow:inset 0 0 0 1px #137cbd; }
    .bp3-input.bp3-intent-primary:disabled, .bp3-input.bp3-intent-primary.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-primary:focus{
        -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-primary[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #137cbd;
                box-shadow:inset 0 0 0 1px #137cbd; }
      .bp3-dark .bp3-input.bp3-intent-primary:disabled, .bp3-dark .bp3-input.bp3-intent-primary.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-success{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-success:focus{
      -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-success[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #0f9960;
              box-shadow:inset 0 0 0 1px #0f9960; }
    .bp3-input.bp3-intent-success:disabled, .bp3-input.bp3-intent-success.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-success{
      -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-success:focus{
        -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #0f9960, 0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-success[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #0f9960;
                box-shadow:inset 0 0 0 1px #0f9960; }
      .bp3-dark .bp3-input.bp3-intent-success:disabled, .bp3-dark .bp3-input.bp3-intent-success.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-warning{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-warning:focus{
      -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-warning[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #d9822b;
              box-shadow:inset 0 0 0 1px #d9822b; }
    .bp3-input.bp3-intent-warning:disabled, .bp3-input.bp3-intent-warning.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-warning:focus{
        -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #d9822b, 0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-warning[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #d9822b;
                box-shadow:inset 0 0 0 1px #d9822b; }
      .bp3-dark .bp3-input.bp3-intent-warning:disabled, .bp3-dark .bp3-input.bp3-intent-warning.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-danger{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-danger:focus{
      -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-danger[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #db3737;
              box-shadow:inset 0 0 0 1px #db3737; }
    .bp3-input.bp3-intent-danger:disabled, .bp3-input.bp3-intent-danger.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-danger:focus{
        -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #db3737, 0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-danger[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #db3737;
                box-shadow:inset 0 0 0 1px #db3737; }
      .bp3-dark .bp3-input.bp3-intent-danger:disabled, .bp3-dark .bp3-input.bp3-intent-danger.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input::-ms-clear{
    display:none; }
textarea.bp3-input{
  max-width:100%;
  padding:10px; }
  textarea.bp3-input, textarea.bp3-input.bp3-large, textarea.bp3-input.bp3-small{
    height:auto;
    line-height:inherit; }
  textarea.bp3-input.bp3-small{
    padding:8px; }
  .bp3-dark textarea.bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    background:rgba(16, 22, 26, 0.3);
    color:#f5f8fa; }
    .bp3-dark textarea.bp3-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark textarea.bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark textarea.bp3-input:disabled, .bp3-dark textarea.bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(57, 75, 89, 0.5);
      color:rgba(167, 182, 194, 0.6); }
label.bp3-label{
  display:block;
  margin-top:0;
  margin-bottom:15px; }
  label.bp3-label .bp3-html-select,
  label.bp3-label .bp3-input,
  label.bp3-label .bp3-select,
  label.bp3-label .bp3-slider,
  label.bp3-label .bp3-popover-wrapper{
    display:block;
    margin-top:5px;
    text-transform:none; }
  label.bp3-label .bp3-button-group{
    margin-top:5px; }
  label.bp3-label .bp3-select select,
  label.bp3-label .bp3-html-select select{
    width:100%;
    vertical-align:top;
    font-weight:400; }
  label.bp3-label.bp3-disabled,
  label.bp3-label.bp3-disabled .bp3-text-muted{
    color:rgba(92, 112, 128, 0.6); }
  label.bp3-label.bp3-inline{
    line-height:30px; }
    label.bp3-label.bp3-inline .bp3-html-select,
    label.bp3-label.bp3-inline .bp3-input,
    label.bp3-label.bp3-inline .bp3-input-group,
    label.bp3-label.bp3-inline .bp3-select,
    label.bp3-label.bp3-inline .bp3-popover-wrapper{
      display:inline-block;
      margin:0 0 0 5px;
      vertical-align:top; }
    label.bp3-label.bp3-inline .bp3-button-group{
      margin:0 0 0 5px; }
    label.bp3-label.bp3-inline .bp3-input-group .bp3-input{
      margin-left:0; }
    label.bp3-label.bp3-inline.bp3-large{
      line-height:40px; }
  label.bp3-label:not(.bp3-inline) .bp3-popover-target{
    display:block; }
  .bp3-dark label.bp3-label{
    color:#f5f8fa; }
    .bp3-dark label.bp3-label.bp3-disabled,
    .bp3-dark label.bp3-label.bp3-disabled .bp3-text-muted{
      color:rgba(167, 182, 194, 0.6); }
.bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button{
  -webkit-box-flex:1;
      -ms-flex:1 1 14px;
          flex:1 1 14px;
  width:30px;
  min-height:0;
  padding:0; }
  .bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button:first-child{
    border-radius:0 3px 0 0; }
  .bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button:last-child{
    border-radius:0 0 3px 0; }

.bp3-numeric-input .bp3-button-group.bp3-vertical:first-child > .bp3-button:first-child{
  border-radius:3px 0 0 0; }

.bp3-numeric-input .bp3-button-group.bp3-vertical:first-child > .bp3-button:last-child{
  border-radius:0 0 0 3px; }

.bp3-numeric-input.bp3-large .bp3-button-group.bp3-vertical > .bp3-button{
  width:40px; }

form{
  display:block; }
.bp3-html-select select,
.bp3-select select{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  border:none;
  border-radius:3px;
  cursor:pointer;
  padding:5px 10px;
  vertical-align:middle;
  text-align:left;
  font-size:14px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
  background-color:#f5f8fa;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
  color:#182026;
  border-radius:3px;
  width:100%;
  height:30px;
  padding:0 25px 0 10px;
  -moz-appearance:none;
  -webkit-appearance:none; }
  .bp3-html-select select > *, .bp3-select select > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-html-select select > .bp3-fill, .bp3-select select > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-html-select select::before,
  .bp3-select select::before, .bp3-html-select select > *, .bp3-select select > *{
    margin-right:7px; }
  .bp3-html-select select:empty::before,
  .bp3-select select:empty::before,
  .bp3-html-select select > :last-child,
  .bp3-select select > :last-child{
    margin-right:0; }
  .bp3-html-select select:hover,
  .bp3-select select:hover{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-clip:padding-box;
    background-color:#ebf1f5; }
  .bp3-html-select select:active,
  .bp3-select select:active, .bp3-html-select select.bp3-active,
  .bp3-select select.bp3-active{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#d8e1e8;
    background-image:none; }
  .bp3-html-select select:disabled,
  .bp3-select select:disabled, .bp3-html-select select.bp3-disabled,
  .bp3-select select.bp3-disabled{
    outline:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    background-color:rgba(206, 217, 224, 0.5);
    background-image:none;
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
    .bp3-html-select select:disabled.bp3-active,
    .bp3-select select:disabled.bp3-active, .bp3-html-select select:disabled.bp3-active:hover,
    .bp3-select select:disabled.bp3-active:hover, .bp3-html-select select.bp3-disabled.bp3-active,
    .bp3-select select.bp3-disabled.bp3-active, .bp3-html-select select.bp3-disabled.bp3-active:hover,
    .bp3-select select.bp3-disabled.bp3-active:hover{
      background:rgba(206, 217, 224, 0.7); }

.bp3-html-select.bp3-minimal select,
.bp3-select.bp3-minimal select{
  -webkit-box-shadow:none;
          box-shadow:none;
  background:none; }
  .bp3-html-select.bp3-minimal select:hover,
  .bp3-select.bp3-minimal select:hover{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(167, 182, 194, 0.3);
    text-decoration:none;
    color:#182026; }
  .bp3-html-select.bp3-minimal select:active,
  .bp3-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal select.bp3-active,
  .bp3-select.bp3-minimal select.bp3-active{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(115, 134, 148, 0.3);
    color:#182026; }
  .bp3-html-select.bp3-minimal select:disabled,
  .bp3-select.bp3-minimal select:disabled, .bp3-html-select.bp3-minimal select:disabled:hover,
  .bp3-select.bp3-minimal select:disabled:hover, .bp3-html-select.bp3-minimal select.bp3-disabled,
  .bp3-select.bp3-minimal select.bp3-disabled, .bp3-html-select.bp3-minimal select.bp3-disabled:hover,
  .bp3-select.bp3-minimal select.bp3-disabled:hover{
    background:none;
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
    .bp3-html-select.bp3-minimal select:disabled.bp3-active,
    .bp3-select.bp3-minimal select:disabled.bp3-active, .bp3-html-select.bp3-minimal select:disabled:hover.bp3-active,
    .bp3-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-html-select.bp3-minimal select.bp3-disabled.bp3-active,
    .bp3-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-disabled:hover.bp3-active,
    .bp3-select.bp3-minimal select.bp3-disabled:hover.bp3-active{
      background:rgba(115, 134, 148, 0.3); }
  .bp3-dark .bp3-html-select.bp3-minimal select, .bp3-html-select.bp3-minimal .bp3-dark select,
  .bp3-dark .bp3-select.bp3-minimal select, .bp3-select.bp3-minimal .bp3-dark select{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:none;
    color:inherit; }
    .bp3-dark .bp3-html-select.bp3-minimal select:hover, .bp3-html-select.bp3-minimal .bp3-dark select:hover,
    .bp3-dark .bp3-select.bp3-minimal select:hover, .bp3-select.bp3-minimal .bp3-dark select:hover, .bp3-dark .bp3-html-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal .bp3-dark select:active,
    .bp3-dark .bp3-select.bp3-minimal select:active, .bp3-select.bp3-minimal .bp3-dark select:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-active,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none; }
    .bp3-dark .bp3-html-select.bp3-minimal select:hover, .bp3-html-select.bp3-minimal .bp3-dark select:hover,
    .bp3-dark .bp3-select.bp3-minimal select:hover, .bp3-select.bp3-minimal .bp3-dark select:hover{
      background:rgba(138, 155, 168, 0.15); }
    .bp3-dark .bp3-html-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal .bp3-dark select:active,
    .bp3-dark .bp3-select.bp3-minimal select:active, .bp3-select.bp3-minimal .bp3-dark select:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-active,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-active{
      background:rgba(138, 155, 168, 0.3);
      color:#f5f8fa; }
    .bp3-dark .bp3-html-select.bp3-minimal select:disabled, .bp3-html-select.bp3-minimal .bp3-dark select:disabled,
    .bp3-dark .bp3-select.bp3-minimal select:disabled, .bp3-select.bp3-minimal .bp3-dark select:disabled, .bp3-dark .bp3-html-select.bp3-minimal select:disabled:hover, .bp3-html-select.bp3-minimal .bp3-dark select:disabled:hover,
    .bp3-dark .bp3-select.bp3-minimal select:disabled:hover, .bp3-select.bp3-minimal .bp3-dark select:disabled:hover, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled:hover,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled:hover{
      background:none;
      cursor:not-allowed;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-html-select.bp3-minimal select:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select:disabled.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select:disabled:hover.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-select.bp3-minimal .bp3-dark select:disabled:hover.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled:hover.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled:hover.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled:hover.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled:hover.bp3-active{
        background:rgba(138, 155, 168, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-primary,
  .bp3-select.bp3-minimal select.bp3-intent-primary{
    color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover,
    .bp3-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-html-select.bp3-minimal select.bp3-intent-primary:active,
    .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover,
    .bp3-select.bp3-minimal select.bp3-intent-primary:hover{
      background:rgba(19, 124, 189, 0.15);
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:active,
    .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active{
      background:rgba(19, 124, 189, 0.3);
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled{
      background:none;
      color:rgba(16, 107, 163, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active{
        background:rgba(19, 124, 189, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
      stroke:#106ba3; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary{
      color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.2);
        color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(72, 175, 240, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-success,
  .bp3-select.bp3-minimal select.bp3-intent-success{
    color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:hover,
    .bp3-select.bp3-minimal select.bp3-intent-success:hover, .bp3-html-select.bp3-minimal select.bp3-intent-success:active,
    .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:hover,
    .bp3-select.bp3-minimal select.bp3-intent-success:hover{
      background:rgba(15, 153, 96, 0.15);
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:active,
    .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active{
      background:rgba(15, 153, 96, 0.3);
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled{
      background:none;
      color:rgba(13, 128, 80, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active{
        background:rgba(15, 153, 96, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-success .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
      stroke:#0d8050; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success{
      color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.2);
        color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(61, 204, 145, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-warning,
  .bp3-select.bp3-minimal select.bp3-intent-warning{
    color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover,
    .bp3-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-html-select.bp3-minimal select.bp3-intent-warning:active,
    .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover,
    .bp3-select.bp3-minimal select.bp3-intent-warning:hover{
      background:rgba(217, 130, 43, 0.15);
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:active,
    .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active{
      background:rgba(217, 130, 43, 0.3);
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled{
      background:none;
      color:rgba(191, 115, 38, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active{
        background:rgba(217, 130, 43, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
      stroke:#bf7326; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning{
      color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.2);
        color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(255, 179, 102, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-danger,
  .bp3-select.bp3-minimal select.bp3-intent-danger{
    color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover,
    .bp3-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-html-select.bp3-minimal select.bp3-intent-danger:active,
    .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover,
    .bp3-select.bp3-minimal select.bp3-intent-danger:hover{
      background:rgba(219, 55, 55, 0.15);
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:active,
    .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active{
      background:rgba(219, 55, 55, 0.3);
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled{
      background:none;
      color:rgba(194, 48, 48, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active{
        background:rgba(219, 55, 55, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
      stroke:#c23030; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger{
      color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.2);
        color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(255, 115, 115, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }

.bp3-html-select.bp3-large select,
.bp3-select.bp3-large select{
  height:40px;
  padding-right:35px;
  font-size:16px; }

.bp3-dark .bp3-html-select select, .bp3-dark .bp3-select select{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
  background-color:#394b59;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
  color:#f5f8fa; }
  .bp3-dark .bp3-html-select select:hover, .bp3-dark .bp3-select select:hover, .bp3-dark .bp3-html-select select:active, .bp3-dark .bp3-select select:active, .bp3-dark .bp3-html-select select.bp3-active, .bp3-dark .bp3-select select.bp3-active{
    color:#f5f8fa; }
  .bp3-dark .bp3-html-select select:hover, .bp3-dark .bp3-select select:hover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background-color:#30404d; }
  .bp3-dark .bp3-html-select select:active, .bp3-dark .bp3-select select:active, .bp3-dark .bp3-html-select select.bp3-active, .bp3-dark .bp3-select select.bp3-active{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#202b33;
    background-image:none; }
  .bp3-dark .bp3-html-select select:disabled, .bp3-dark .bp3-select select:disabled, .bp3-dark .bp3-html-select select.bp3-disabled, .bp3-dark .bp3-select select.bp3-disabled{
    -webkit-box-shadow:none;
            box-shadow:none;
    background-color:rgba(57, 75, 89, 0.5);
    background-image:none;
    color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-html-select select:disabled.bp3-active, .bp3-dark .bp3-select select:disabled.bp3-active, .bp3-dark .bp3-html-select select.bp3-disabled.bp3-active, .bp3-dark .bp3-select select.bp3-disabled.bp3-active{
      background:rgba(57, 75, 89, 0.7); }
  .bp3-dark .bp3-html-select select .bp3-button-spinner .bp3-spinner-head, .bp3-dark .bp3-select select .bp3-button-spinner .bp3-spinner-head{
    background:rgba(16, 22, 26, 0.5);
    stroke:#8a9ba8; }

.bp3-html-select select:disabled,
.bp3-select select:disabled{
  -webkit-box-shadow:none;
          box-shadow:none;
  background-color:rgba(206, 217, 224, 0.5);
  cursor:not-allowed;
  color:rgba(92, 112, 128, 0.6); }

.bp3-html-select .bp3-icon,
.bp3-select .bp3-icon, .bp3-select::after{
  position:absolute;
  top:7px;
  right:7px;
  color:#5c7080;
  pointer-events:none; }
  .bp3-html-select .bp3-disabled.bp3-icon,
  .bp3-select .bp3-disabled.bp3-icon, .bp3-disabled.bp3-select::after{
    color:rgba(92, 112, 128, 0.6); }
.bp3-html-select,
.bp3-select{
  display:inline-block;
  position:relative;
  vertical-align:middle;
  letter-spacing:normal; }
  .bp3-html-select select::-ms-expand,
  .bp3-select select::-ms-expand{
    display:none; }
  .bp3-html-select .bp3-icon,
  .bp3-select .bp3-icon{
    color:#5c7080; }
    .bp3-html-select .bp3-icon:hover,
    .bp3-select .bp3-icon:hover{
      color:#182026; }
    .bp3-dark .bp3-html-select .bp3-icon, .bp3-dark
    .bp3-select .bp3-icon{
      color:#a7b6c2; }
      .bp3-dark .bp3-html-select .bp3-icon:hover, .bp3-dark
      .bp3-select .bp3-icon:hover{
        color:#f5f8fa; }
  .bp3-html-select.bp3-large::after,
  .bp3-html-select.bp3-large .bp3-icon,
  .bp3-select.bp3-large::after,
  .bp3-select.bp3-large .bp3-icon{
    top:12px;
    right:12px; }
  .bp3-html-select.bp3-fill,
  .bp3-html-select.bp3-fill select,
  .bp3-select.bp3-fill,
  .bp3-select.bp3-fill select{
    width:100%; }
  .bp3-dark .bp3-html-select option, .bp3-dark
  .bp3-select option{
    background-color:#30404d;
    color:#f5f8fa; }
  .bp3-dark .bp3-html-select::after, .bp3-dark
  .bp3-select::after{
    color:#a7b6c2; }

.bp3-select::after{
  line-height:1;
  font-family:"Icons16", sans-serif;
  font-size:16px;
  font-weight:400;
  font-style:normal;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  content:""; }
.bp3-running-text table, table.bp3-html-table{
  border-spacing:0;
  font-size:14px; }
  .bp3-running-text table th, table.bp3-html-table th,
  .bp3-running-text table td,
  table.bp3-html-table td{
    padding:11px;
    vertical-align:top;
    text-align:left; }
  .bp3-running-text table th, table.bp3-html-table th{
    color:#182026;
    font-weight:600; }
  
  .bp3-running-text table td,
  table.bp3-html-table td{
    color:#182026; }
  .bp3-running-text table tbody tr:first-child th, table.bp3-html-table tbody tr:first-child th,
  .bp3-running-text table tbody tr:first-child td,
  table.bp3-html-table tbody tr:first-child td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-running-text table th, .bp3-running-text .bp3-dark table th, .bp3-dark table.bp3-html-table th{
    color:#f5f8fa; }
  .bp3-dark .bp3-running-text table td, .bp3-running-text .bp3-dark table td, .bp3-dark table.bp3-html-table td{
    color:#f5f8fa; }
  .bp3-dark .bp3-running-text table tbody tr:first-child th, .bp3-running-text .bp3-dark table tbody tr:first-child th, .bp3-dark table.bp3-html-table tbody tr:first-child th,
  .bp3-dark .bp3-running-text table tbody tr:first-child td,
  .bp3-running-text .bp3-dark table tbody tr:first-child td,
  .bp3-dark table.bp3-html-table tbody tr:first-child td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15); }

table.bp3-html-table.bp3-html-table-condensed th,
table.bp3-html-table.bp3-html-table-condensed td, table.bp3-html-table.bp3-small th,
table.bp3-html-table.bp3-small td{
  padding-top:6px;
  padding-bottom:6px; }

table.bp3-html-table.bp3-html-table-striped tbody tr:nth-child(odd) td{
  background:rgba(191, 204, 214, 0.15); }

table.bp3-html-table.bp3-html-table-bordered th:not(:first-child){
  -webkit-box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-html-table-bordered tbody tr td{
  -webkit-box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15); }
  table.bp3-html-table.bp3-html-table-bordered tbody tr td:not(:first-child){
    -webkit-box-shadow:inset 1px 1px 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 1px 1px 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td{
  -webkit-box-shadow:none;
          box-shadow:none; }
  table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td:not(:first-child){
    -webkit-box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-interactive tbody tr:hover td{
  background-color:rgba(191, 204, 214, 0.3);
  cursor:pointer; }

table.bp3-html-table.bp3-interactive tbody tr:active td{
  background-color:rgba(191, 204, 214, 0.4); }

.bp3-dark table.bp3-html-table.bp3-html-table-striped tbody tr:nth-child(odd) td{
  background:rgba(92, 112, 128, 0.15); }

.bp3-dark table.bp3-html-table.bp3-html-table-bordered th:not(:first-child){
  -webkit-box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15);
          box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15); }

.bp3-dark table.bp3-html-table.bp3-html-table-bordered tbody tr td{
  -webkit-box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15);
          box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered tbody tr td:not(:first-child){
    -webkit-box-shadow:inset 1px 1px 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 1px 1px 0 0 rgba(255, 255, 255, 0.15); }

.bp3-dark table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td{
  -webkit-box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15);
          box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td:first-child{
    -webkit-box-shadow:none;
            box-shadow:none; }

.bp3-dark table.bp3-html-table.bp3-interactive tbody tr:hover td{
  background-color:rgba(92, 112, 128, 0.3);
  cursor:pointer; }

.bp3-dark table.bp3-html-table.bp3-interactive tbody tr:active td{
  background-color:rgba(92, 112, 128, 0.4); }

.bp3-key-combo{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center; }
  .bp3-key-combo > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-key-combo > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-key-combo::before,
  .bp3-key-combo > *{
    margin-right:5px; }
  .bp3-key-combo:empty::before,
  .bp3-key-combo > :last-child{
    margin-right:0; }

.bp3-hotkey-dialog{
  top:40px;
  padding-bottom:0; }
  .bp3-hotkey-dialog .bp3-dialog-body{
    margin:0;
    padding:0; }
  .bp3-hotkey-dialog .bp3-hotkey-label{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1; }

.bp3-hotkey-column{
  margin:auto;
  max-height:80vh;
  overflow-y:auto;
  padding:30px; }
  .bp3-hotkey-column .bp3-heading{
    margin-bottom:20px; }
    .bp3-hotkey-column .bp3-heading:not(:first-child){
      margin-top:40px; }

.bp3-hotkey{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:justify;
      -ms-flex-pack:justify;
          justify-content:space-between;
  margin-right:0;
  margin-left:0; }
  .bp3-hotkey:not(:last-child){
    margin-bottom:10px; }
.bp3-icon{
  display:inline-block;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  vertical-align:text-bottom; }
  .bp3-icon:not(:empty)::before{
    content:"" !important;
    content:unset !important; }
  .bp3-icon > svg{
    display:block; }
    .bp3-icon > svg:not([fill]){
      fill:currentColor; }

.bp3-icon.bp3-intent-primary, .bp3-icon-standard.bp3-intent-primary, .bp3-icon-large.bp3-intent-primary{
  color:#106ba3; }
  .bp3-dark .bp3-icon.bp3-intent-primary, .bp3-dark .bp3-icon-standard.bp3-intent-primary, .bp3-dark .bp3-icon-large.bp3-intent-primary{
    color:#48aff0; }

.bp3-icon.bp3-intent-success, .bp3-icon-standard.bp3-intent-success, .bp3-icon-large.bp3-intent-success{
  color:#0d8050; }
  .bp3-dark .bp3-icon.bp3-intent-success, .bp3-dark .bp3-icon-standard.bp3-intent-success, .bp3-dark .bp3-icon-large.bp3-intent-success{
    color:#3dcc91; }

.bp3-icon.bp3-intent-warning, .bp3-icon-standard.bp3-intent-warning, .bp3-icon-large.bp3-intent-warning{
  color:#bf7326; }
  .bp3-dark .bp3-icon.bp3-intent-warning, .bp3-dark .bp3-icon-standard.bp3-intent-warning, .bp3-dark .bp3-icon-large.bp3-intent-warning{
    color:#ffb366; }

.bp3-icon.bp3-intent-danger, .bp3-icon-standard.bp3-intent-danger, .bp3-icon-large.bp3-intent-danger{
  color:#c23030; }
  .bp3-dark .bp3-icon.bp3-intent-danger, .bp3-dark .bp3-icon-standard.bp3-intent-danger, .bp3-dark .bp3-icon-large.bp3-intent-danger{
    color:#ff7373; }

span.bp3-icon-standard{
  line-height:1;
  font-family:"Icons16", sans-serif;
  font-size:16px;
  font-weight:400;
  font-style:normal;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  display:inline-block; }

span.bp3-icon-large{
  line-height:1;
  font-family:"Icons20", sans-serif;
  font-size:20px;
  font-weight:400;
  font-style:normal;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  display:inline-block; }

span.bp3-icon:empty{
  line-height:1;
  font-family:"Icons20";
  font-size:inherit;
  font-weight:400;
  font-style:normal; }
  span.bp3-icon:empty::before{
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased; }

.bp3-icon-add::before{
  content:""; }

.bp3-icon-add-column-left::before{
  content:""; }

.bp3-icon-add-column-right::before{
  content:""; }

.bp3-icon-add-row-bottom::before{
  content:""; }

.bp3-icon-add-row-top::before{
  content:""; }

.bp3-icon-add-to-artifact::before{
  content:""; }

.bp3-icon-add-to-folder::before{
  content:""; }

.bp3-icon-airplane::before{
  content:""; }

.bp3-icon-align-center::before{
  content:""; }

.bp3-icon-align-justify::before{
  content:""; }

.bp3-icon-align-left::before{
  content:""; }

.bp3-icon-align-right::before{
  content:""; }

.bp3-icon-alignment-bottom::before{
  content:""; }

.bp3-icon-alignment-horizontal-center::before{
  content:""; }

.bp3-icon-alignment-left::before{
  content:""; }

.bp3-icon-alignment-right::before{
  content:""; }

.bp3-icon-alignment-top::before{
  content:""; }

.bp3-icon-alignment-vertical-center::before{
  content:""; }

.bp3-icon-annotation::before{
  content:""; }

.bp3-icon-application::before{
  content:""; }

.bp3-icon-applications::before{
  content:""; }

.bp3-icon-archive::before{
  content:""; }

.bp3-icon-arrow-bottom-left::before{
  content:"↙"; }

.bp3-icon-arrow-bottom-right::before{
  content:"↘"; }

.bp3-icon-arrow-down::before{
  content:"↓"; }

.bp3-icon-arrow-left::before{
  content:"←"; }

.bp3-icon-arrow-right::before{
  content:"→"; }

.bp3-icon-arrow-top-left::before{
  content:"↖"; }

.bp3-icon-arrow-top-right::before{
  content:"↗"; }

.bp3-icon-arrow-up::before{
  content:"↑"; }

.bp3-icon-arrows-horizontal::before{
  content:"↔"; }

.bp3-icon-arrows-vertical::before{
  content:"↕"; }

.bp3-icon-asterisk::before{
  content:"*"; }

.bp3-icon-automatic-updates::before{
  content:""; }

.bp3-icon-badge::before{
  content:""; }

.bp3-icon-ban-circle::before{
  content:""; }

.bp3-icon-bank-account::before{
  content:""; }

.bp3-icon-barcode::before{
  content:""; }

.bp3-icon-blank::before{
  content:""; }

.bp3-icon-blocked-person::before{
  content:""; }

.bp3-icon-bold::before{
  content:""; }

.bp3-icon-book::before{
  content:""; }

.bp3-icon-bookmark::before{
  content:""; }

.bp3-icon-box::before{
  content:""; }

.bp3-icon-briefcase::before{
  content:""; }

.bp3-icon-bring-data::before{
  content:""; }

.bp3-icon-build::before{
  content:""; }

.bp3-icon-calculator::before{
  content:""; }

.bp3-icon-calendar::before{
  content:""; }

.bp3-icon-camera::before{
  content:""; }

.bp3-icon-caret-down::before{
  content:"⌄"; }

.bp3-icon-caret-left::before{
  content:"〈"; }

.bp3-icon-caret-right::before{
  content:"〉"; }

.bp3-icon-caret-up::before{
  content:"⌃"; }

.bp3-icon-cell-tower::before{
  content:""; }

.bp3-icon-changes::before{
  content:""; }

.bp3-icon-chart::before{
  content:""; }

.bp3-icon-chat::before{
  content:""; }

.bp3-icon-chevron-backward::before{
  content:""; }

.bp3-icon-chevron-down::before{
  content:""; }

.bp3-icon-chevron-forward::before{
  content:""; }

.bp3-icon-chevron-left::before{
  content:""; }

.bp3-icon-chevron-right::before{
  content:""; }

.bp3-icon-chevron-up::before{
  content:""; }

.bp3-icon-circle::before{
  content:""; }

.bp3-icon-circle-arrow-down::before{
  content:""; }

.bp3-icon-circle-arrow-left::before{
  content:""; }

.bp3-icon-circle-arrow-right::before{
  content:""; }

.bp3-icon-circle-arrow-up::before{
  content:""; }

.bp3-icon-citation::before{
  content:""; }

.bp3-icon-clean::before{
  content:""; }

.bp3-icon-clipboard::before{
  content:""; }

.bp3-icon-cloud::before{
  content:"☁"; }

.bp3-icon-cloud-download::before{
  content:""; }

.bp3-icon-cloud-upload::before{
  content:""; }

.bp3-icon-code::before{
  content:""; }

.bp3-icon-code-block::before{
  content:""; }

.bp3-icon-cog::before{
  content:""; }

.bp3-icon-collapse-all::before{
  content:""; }

.bp3-icon-column-layout::before{
  content:""; }

.bp3-icon-comment::before{
  content:""; }

.bp3-icon-comparison::before{
  content:""; }

.bp3-icon-compass::before{
  content:""; }

.bp3-icon-compressed::before{
  content:""; }

.bp3-icon-confirm::before{
  content:""; }

.bp3-icon-console::before{
  content:""; }

.bp3-icon-contrast::before{
  content:""; }

.bp3-icon-control::before{
  content:""; }

.bp3-icon-credit-card::before{
  content:""; }

.bp3-icon-cross::before{
  content:"✗"; }

.bp3-icon-crown::before{
  content:""; }

.bp3-icon-cube::before{
  content:""; }

.bp3-icon-cube-add::before{
  content:""; }

.bp3-icon-cube-remove::before{
  content:""; }

.bp3-icon-curved-range-chart::before{
  content:""; }

.bp3-icon-cut::before{
  content:""; }

.bp3-icon-dashboard::before{
  content:""; }

.bp3-icon-data-lineage::before{
  content:""; }

.bp3-icon-database::before{
  content:""; }

.bp3-icon-delete::before{
  content:""; }

.bp3-icon-delta::before{
  content:"Δ"; }

.bp3-icon-derive-column::before{
  content:""; }

.bp3-icon-desktop::before{
  content:""; }

.bp3-icon-diagram-tree::before{
  content:""; }

.bp3-icon-direction-left::before{
  content:""; }

.bp3-icon-direction-right::before{
  content:""; }

.bp3-icon-disable::before{
  content:""; }

.bp3-icon-document::before{
  content:""; }

.bp3-icon-document-open::before{
  content:""; }

.bp3-icon-document-share::before{
  content:""; }

.bp3-icon-dollar::before{
  content:"$"; }

.bp3-icon-dot::before{
  content:"•"; }

.bp3-icon-double-caret-horizontal::before{
  content:""; }

.bp3-icon-double-caret-vertical::before{
  content:""; }

.bp3-icon-double-chevron-down::before{
  content:""; }

.bp3-icon-double-chevron-left::before{
  content:""; }

.bp3-icon-double-chevron-right::before{
  content:""; }

.bp3-icon-double-chevron-up::before{
  content:""; }

.bp3-icon-doughnut-chart::before{
  content:""; }

.bp3-icon-download::before{
  content:""; }

.bp3-icon-drag-handle-horizontal::before{
  content:""; }

.bp3-icon-drag-handle-vertical::before{
  content:""; }

.bp3-icon-draw::before{
  content:""; }

.bp3-icon-drive-time::before{
  content:""; }

.bp3-icon-duplicate::before{
  content:""; }

.bp3-icon-edit::before{
  content:"✎"; }

.bp3-icon-eject::before{
  content:"⏏"; }

.bp3-icon-endorsed::before{
  content:""; }

.bp3-icon-envelope::before{
  content:"✉"; }

.bp3-icon-equals::before{
  content:""; }

.bp3-icon-eraser::before{
  content:""; }

.bp3-icon-error::before{
  content:""; }

.bp3-icon-euro::before{
  content:"€"; }

.bp3-icon-exchange::before{
  content:""; }

.bp3-icon-exclude-row::before{
  content:""; }

.bp3-icon-expand-all::before{
  content:""; }

.bp3-icon-export::before{
  content:""; }

.bp3-icon-eye-off::before{
  content:""; }

.bp3-icon-eye-on::before{
  content:""; }

.bp3-icon-eye-open::before{
  content:""; }

.bp3-icon-fast-backward::before{
  content:""; }

.bp3-icon-fast-forward::before{
  content:""; }

.bp3-icon-feed::before{
  content:""; }

.bp3-icon-feed-subscribed::before{
  content:""; }

.bp3-icon-film::before{
  content:""; }

.bp3-icon-filter::before{
  content:""; }

.bp3-icon-filter-keep::before{
  content:""; }

.bp3-icon-filter-list::before{
  content:""; }

.bp3-icon-filter-open::before{
  content:""; }

.bp3-icon-filter-remove::before{
  content:""; }

.bp3-icon-flag::before{
  content:"⚑"; }

.bp3-icon-flame::before{
  content:""; }

.bp3-icon-flash::before{
  content:""; }

.bp3-icon-floppy-disk::before{
  content:""; }

.bp3-icon-flow-branch::before{
  content:""; }

.bp3-icon-flow-end::before{
  content:""; }

.bp3-icon-flow-linear::before{
  content:""; }

.bp3-icon-flow-review::before{
  content:""; }

.bp3-icon-flow-review-branch::before{
  content:""; }

.bp3-icon-flows::before{
  content:""; }

.bp3-icon-folder-close::before{
  content:""; }

.bp3-icon-folder-new::before{
  content:""; }

.bp3-icon-folder-open::before{
  content:""; }

.bp3-icon-folder-shared::before{
  content:""; }

.bp3-icon-folder-shared-open::before{
  content:""; }

.bp3-icon-follower::before{
  content:""; }

.bp3-icon-following::before{
  content:""; }

.bp3-icon-font::before{
  content:""; }

.bp3-icon-fork::before{
  content:""; }

.bp3-icon-form::before{
  content:""; }

.bp3-icon-full-circle::before{
  content:""; }

.bp3-icon-full-stacked-chart::before{
  content:""; }

.bp3-icon-fullscreen::before{
  content:""; }

.bp3-icon-function::before{
  content:""; }

.bp3-icon-gantt-chart::before{
  content:""; }

.bp3-icon-geolocation::before{
  content:""; }

.bp3-icon-geosearch::before{
  content:""; }

.bp3-icon-git-branch::before{
  content:""; }

.bp3-icon-git-commit::before{
  content:""; }

.bp3-icon-git-merge::before{
  content:""; }

.bp3-icon-git-new-branch::before{
  content:""; }

.bp3-icon-git-pull::before{
  content:""; }

.bp3-icon-git-push::before{
  content:""; }

.bp3-icon-git-repo::before{
  content:""; }

.bp3-icon-glass::before{
  content:""; }

.bp3-icon-globe::before{
  content:""; }

.bp3-icon-globe-network::before{
  content:""; }

.bp3-icon-graph::before{
  content:""; }

.bp3-icon-graph-remove::before{
  content:""; }

.bp3-icon-greater-than::before{
  content:""; }

.bp3-icon-greater-than-or-equal-to::before{
  content:""; }

.bp3-icon-grid::before{
  content:""; }

.bp3-icon-grid-view::before{
  content:""; }

.bp3-icon-group-objects::before{
  content:""; }

.bp3-icon-grouped-bar-chart::before{
  content:""; }

.bp3-icon-hand::before{
  content:""; }

.bp3-icon-hand-down::before{
  content:""; }

.bp3-icon-hand-left::before{
  content:""; }

.bp3-icon-hand-right::before{
  content:""; }

.bp3-icon-hand-up::before{
  content:""; }

.bp3-icon-header::before{
  content:""; }

.bp3-icon-header-one::before{
  content:""; }

.bp3-icon-header-two::before{
  content:""; }

.bp3-icon-headset::before{
  content:""; }

.bp3-icon-heart::before{
  content:"♥"; }

.bp3-icon-heart-broken::before{
  content:""; }

.bp3-icon-heat-grid::before{
  content:""; }

.bp3-icon-heatmap::before{
  content:""; }

.bp3-icon-help::before{
  content:"?"; }

.bp3-icon-helper-management::before{
  content:""; }

.bp3-icon-highlight::before{
  content:""; }

.bp3-icon-history::before{
  content:""; }

.bp3-icon-home::before{
  content:"⌂"; }

.bp3-icon-horizontal-bar-chart::before{
  content:""; }

.bp3-icon-horizontal-bar-chart-asc::before{
  content:""; }

.bp3-icon-horizontal-bar-chart-desc::before{
  content:""; }

.bp3-icon-horizontal-distribution::before{
  content:""; }

.bp3-icon-id-number::before{
  content:""; }

.bp3-icon-image-rotate-left::before{
  content:""; }

.bp3-icon-image-rotate-right::before{
  content:""; }

.bp3-icon-import::before{
  content:""; }

.bp3-icon-inbox::before{
  content:""; }

.bp3-icon-inbox-filtered::before{
  content:""; }

.bp3-icon-inbox-geo::before{
  content:""; }

.bp3-icon-inbox-search::before{
  content:""; }

.bp3-icon-inbox-update::before{
  content:""; }

.bp3-icon-info-sign::before{
  content:"ℹ"; }

.bp3-icon-inheritance::before{
  content:""; }

.bp3-icon-inner-join::before{
  content:""; }

.bp3-icon-insert::before{
  content:""; }

.bp3-icon-intersection::before{
  content:""; }

.bp3-icon-ip-address::before{
  content:""; }

.bp3-icon-issue::before{
  content:""; }

.bp3-icon-issue-closed::before{
  content:""; }

.bp3-icon-issue-new::before{
  content:""; }

.bp3-icon-italic::before{
  content:""; }

.bp3-icon-join-table::before{
  content:""; }

.bp3-icon-key::before{
  content:""; }

.bp3-icon-key-backspace::before{
  content:""; }

.bp3-icon-key-command::before{
  content:""; }

.bp3-icon-key-control::before{
  content:""; }

.bp3-icon-key-delete::before{
  content:""; }

.bp3-icon-key-enter::before{
  content:""; }

.bp3-icon-key-escape::before{
  content:""; }

.bp3-icon-key-option::before{
  content:""; }

.bp3-icon-key-shift::before{
  content:""; }

.bp3-icon-key-tab::before{
  content:""; }

.bp3-icon-known-vehicle::before{
  content:""; }

.bp3-icon-label::before{
  content:""; }

.bp3-icon-layer::before{
  content:""; }

.bp3-icon-layers::before{
  content:""; }

.bp3-icon-layout::before{
  content:""; }

.bp3-icon-layout-auto::before{
  content:""; }

.bp3-icon-layout-balloon::before{
  content:""; }

.bp3-icon-layout-circle::before{
  content:""; }

.bp3-icon-layout-grid::before{
  content:""; }

.bp3-icon-layout-group-by::before{
  content:""; }

.bp3-icon-layout-hierarchy::before{
  content:""; }

.bp3-icon-layout-linear::before{
  content:""; }

.bp3-icon-layout-skew-grid::before{
  content:""; }

.bp3-icon-layout-sorted-clusters::before{
  content:""; }

.bp3-icon-learning::before{
  content:""; }

.bp3-icon-left-join::before{
  content:""; }

.bp3-icon-less-than::before{
  content:""; }

.bp3-icon-less-than-or-equal-to::before{
  content:""; }

.bp3-icon-lifesaver::before{
  content:""; }

.bp3-icon-lightbulb::before{
  content:""; }

.bp3-icon-link::before{
  content:""; }

.bp3-icon-list::before{
  content:"☰"; }

.bp3-icon-list-columns::before{
  content:""; }

.bp3-icon-list-detail-view::before{
  content:""; }

.bp3-icon-locate::before{
  content:""; }

.bp3-icon-lock::before{
  content:""; }

.bp3-icon-log-in::before{
  content:""; }

.bp3-icon-log-out::before{
  content:""; }

.bp3-icon-manual::before{
  content:""; }

.bp3-icon-manually-entered-data::before{
  content:""; }

.bp3-icon-map::before{
  content:""; }

.bp3-icon-map-create::before{
  content:""; }

.bp3-icon-map-marker::before{
  content:""; }

.bp3-icon-maximize::before{
  content:""; }

.bp3-icon-media::before{
  content:""; }

.bp3-icon-menu::before{
  content:""; }

.bp3-icon-menu-closed::before{
  content:""; }

.bp3-icon-menu-open::before{
  content:""; }

.bp3-icon-merge-columns::before{
  content:""; }

.bp3-icon-merge-links::before{
  content:""; }

.bp3-icon-minimize::before{
  content:""; }

.bp3-icon-minus::before{
  content:"−"; }

.bp3-icon-mobile-phone::before{
  content:""; }

.bp3-icon-mobile-video::before{
  content:""; }

.bp3-icon-moon::before{
  content:""; }

.bp3-icon-more::before{
  content:""; }

.bp3-icon-mountain::before{
  content:""; }

.bp3-icon-move::before{
  content:""; }

.bp3-icon-mugshot::before{
  content:""; }

.bp3-icon-multi-select::before{
  content:""; }

.bp3-icon-music::before{
  content:""; }

.bp3-icon-new-drawing::before{
  content:""; }

.bp3-icon-new-grid-item::before{
  content:""; }

.bp3-icon-new-layer::before{
  content:""; }

.bp3-icon-new-layers::before{
  content:""; }

.bp3-icon-new-link::before{
  content:""; }

.bp3-icon-new-object::before{
  content:""; }

.bp3-icon-new-person::before{
  content:""; }

.bp3-icon-new-prescription::before{
  content:""; }

.bp3-icon-new-text-box::before{
  content:""; }

.bp3-icon-ninja::before{
  content:""; }

.bp3-icon-not-equal-to::before{
  content:""; }

.bp3-icon-notifications::before{
  content:""; }

.bp3-icon-notifications-updated::before{
  content:""; }

.bp3-icon-numbered-list::before{
  content:""; }

.bp3-icon-numerical::before{
  content:""; }

.bp3-icon-office::before{
  content:""; }

.bp3-icon-offline::before{
  content:""; }

.bp3-icon-oil-field::before{
  content:""; }

.bp3-icon-one-column::before{
  content:""; }

.bp3-icon-outdated::before{
  content:""; }

.bp3-icon-page-layout::before{
  content:""; }

.bp3-icon-panel-stats::before{
  content:""; }

.bp3-icon-panel-table::before{
  content:""; }

.bp3-icon-paperclip::before{
  content:""; }

.bp3-icon-paragraph::before{
  content:""; }

.bp3-icon-path::before{
  content:""; }

.bp3-icon-path-search::before{
  content:""; }

.bp3-icon-pause::before{
  content:""; }

.bp3-icon-people::before{
  content:""; }

.bp3-icon-percentage::before{
  content:""; }

.bp3-icon-person::before{
  content:""; }

.bp3-icon-phone::before{
  content:"☎"; }

.bp3-icon-pie-chart::before{
  content:""; }

.bp3-icon-pin::before{
  content:""; }

.bp3-icon-pivot::before{
  content:""; }

.bp3-icon-pivot-table::before{
  content:""; }

.bp3-icon-play::before{
  content:""; }

.bp3-icon-plus::before{
  content:"+"; }

.bp3-icon-polygon-filter::before{
  content:""; }

.bp3-icon-power::before{
  content:""; }

.bp3-icon-predictive-analysis::before{
  content:""; }

.bp3-icon-prescription::before{
  content:""; }

.bp3-icon-presentation::before{
  content:""; }

.bp3-icon-print::before{
  content:"⎙"; }

.bp3-icon-projects::before{
  content:""; }

.bp3-icon-properties::before{
  content:""; }

.bp3-icon-property::before{
  content:""; }

.bp3-icon-publish-function::before{
  content:""; }

.bp3-icon-pulse::before{
  content:""; }

.bp3-icon-random::before{
  content:""; }

.bp3-icon-record::before{
  content:""; }

.bp3-icon-redo::before{
  content:""; }

.bp3-icon-refresh::before{
  content:""; }

.bp3-icon-regression-chart::before{
  content:""; }

.bp3-icon-remove::before{
  content:""; }

.bp3-icon-remove-column::before{
  content:""; }

.bp3-icon-remove-column-left::before{
  content:""; }

.bp3-icon-remove-column-right::before{
  content:""; }

.bp3-icon-remove-row-bottom::before{
  content:""; }

.bp3-icon-remove-row-top::before{
  content:""; }

.bp3-icon-repeat::before{
  content:""; }

.bp3-icon-reset::before{
  content:""; }

.bp3-icon-resolve::before{
  content:""; }

.bp3-icon-rig::before{
  content:""; }

.bp3-icon-right-join::before{
  content:""; }

.bp3-icon-ring::before{
  content:""; }

.bp3-icon-rotate-document::before{
  content:""; }

.bp3-icon-rotate-page::before{
  content:""; }

.bp3-icon-satellite::before{
  content:""; }

.bp3-icon-saved::before{
  content:""; }

.bp3-icon-scatter-plot::before{
  content:""; }

.bp3-icon-search::before{
  content:""; }

.bp3-icon-search-around::before{
  content:""; }

.bp3-icon-search-template::before{
  content:""; }

.bp3-icon-search-text::before{
  content:""; }

.bp3-icon-segmented-control::before{
  content:""; }

.bp3-icon-select::before{
  content:""; }

.bp3-icon-selection::before{
  content:"⦿"; }

.bp3-icon-send-to::before{
  content:""; }

.bp3-icon-send-to-graph::before{
  content:""; }

.bp3-icon-send-to-map::before{
  content:""; }

.bp3-icon-series-add::before{
  content:""; }

.bp3-icon-series-configuration::before{
  content:""; }

.bp3-icon-series-derived::before{
  content:""; }

.bp3-icon-series-filtered::before{
  content:""; }

.bp3-icon-series-search::before{
  content:""; }

.bp3-icon-settings::before{
  content:""; }

.bp3-icon-share::before{
  content:""; }

.bp3-icon-shield::before{
  content:""; }

.bp3-icon-shop::before{
  content:""; }

.bp3-icon-shopping-cart::before{
  content:""; }

.bp3-icon-signal-search::before{
  content:""; }

.bp3-icon-sim-card::before{
  content:""; }

.bp3-icon-slash::before{
  content:""; }

.bp3-icon-small-cross::before{
  content:""; }

.bp3-icon-small-minus::before{
  content:""; }

.bp3-icon-small-plus::before{
  content:""; }

.bp3-icon-small-tick::before{
  content:""; }

.bp3-icon-snowflake::before{
  content:""; }

.bp3-icon-social-media::before{
  content:""; }

.bp3-icon-sort::before{
  content:""; }

.bp3-icon-sort-alphabetical::before{
  content:""; }

.bp3-icon-sort-alphabetical-desc::before{
  content:""; }

.bp3-icon-sort-asc::before{
  content:""; }

.bp3-icon-sort-desc::before{
  content:""; }

.bp3-icon-sort-numerical::before{
  content:""; }

.bp3-icon-sort-numerical-desc::before{
  content:""; }

.bp3-icon-split-columns::before{
  content:""; }

.bp3-icon-square::before{
  content:""; }

.bp3-icon-stacked-chart::before{
  content:""; }

.bp3-icon-star::before{
  content:"★"; }

.bp3-icon-star-empty::before{
  content:"☆"; }

.bp3-icon-step-backward::before{
  content:""; }

.bp3-icon-step-chart::before{
  content:""; }

.bp3-icon-step-forward::before{
  content:""; }

.bp3-icon-stop::before{
  content:""; }

.bp3-icon-stopwatch::before{
  content:""; }

.bp3-icon-strikethrough::before{
  content:""; }

.bp3-icon-style::before{
  content:""; }

.bp3-icon-swap-horizontal::before{
  content:""; }

.bp3-icon-swap-vertical::before{
  content:""; }

.bp3-icon-symbol-circle::before{
  content:""; }

.bp3-icon-symbol-cross::before{
  content:""; }

.bp3-icon-symbol-diamond::before{
  content:""; }

.bp3-icon-symbol-square::before{
  content:""; }

.bp3-icon-symbol-triangle-down::before{
  content:""; }

.bp3-icon-symbol-triangle-up::before{
  content:""; }

.bp3-icon-tag::before{
  content:""; }

.bp3-icon-take-action::before{
  content:""; }

.bp3-icon-taxi::before{
  content:""; }

.bp3-icon-text-highlight::before{
  content:""; }

.bp3-icon-th::before{
  content:""; }

.bp3-icon-th-derived::before{
  content:""; }

.bp3-icon-th-disconnect::before{
  content:""; }

.bp3-icon-th-filtered::before{
  content:""; }

.bp3-icon-th-list::before{
  content:""; }

.bp3-icon-thumbs-down::before{
  content:""; }

.bp3-icon-thumbs-up::before{
  content:""; }

.bp3-icon-tick::before{
  content:"✓"; }

.bp3-icon-tick-circle::before{
  content:""; }

.bp3-icon-time::before{
  content:"⏲"; }

.bp3-icon-timeline-area-chart::before{
  content:""; }

.bp3-icon-timeline-bar-chart::before{
  content:""; }

.bp3-icon-timeline-events::before{
  content:""; }

.bp3-icon-timeline-line-chart::before{
  content:""; }

.bp3-icon-tint::before{
  content:""; }

.bp3-icon-torch::before{
  content:""; }

.bp3-icon-tractor::before{
  content:""; }

.bp3-icon-train::before{
  content:""; }

.bp3-icon-translate::before{
  content:""; }

.bp3-icon-trash::before{
  content:""; }

.bp3-icon-tree::before{
  content:""; }

.bp3-icon-trending-down::before{
  content:""; }

.bp3-icon-trending-up::before{
  content:""; }

.bp3-icon-truck::before{
  content:""; }

.bp3-icon-two-columns::before{
  content:""; }

.bp3-icon-unarchive::before{
  content:""; }

.bp3-icon-underline::before{
  content:"⎁"; }

.bp3-icon-undo::before{
  content:"⎌"; }

.bp3-icon-ungroup-objects::before{
  content:""; }

.bp3-icon-unknown-vehicle::before{
  content:""; }

.bp3-icon-unlock::before{
  content:""; }

.bp3-icon-unpin::before{
  content:""; }

.bp3-icon-unresolve::before{
  content:""; }

.bp3-icon-updated::before{
  content:""; }

.bp3-icon-upload::before{
  content:""; }

.bp3-icon-user::before{
  content:""; }

.bp3-icon-variable::before{
  content:""; }

.bp3-icon-vertical-bar-chart-asc::before{
  content:""; }

.bp3-icon-vertical-bar-chart-desc::before{
  content:""; }

.bp3-icon-vertical-distribution::before{
  content:""; }

.bp3-icon-video::before{
  content:""; }

.bp3-icon-volume-down::before{
  content:""; }

.bp3-icon-volume-off::before{
  content:""; }

.bp3-icon-volume-up::before{
  content:""; }

.bp3-icon-walk::before{
  content:""; }

.bp3-icon-warning-sign::before{
  content:""; }

.bp3-icon-waterfall-chart::before{
  content:""; }

.bp3-icon-widget::before{
  content:""; }

.bp3-icon-widget-button::before{
  content:""; }

.bp3-icon-widget-footer::before{
  content:""; }

.bp3-icon-widget-header::before{
  content:""; }

.bp3-icon-wrench::before{
  content:""; }

.bp3-icon-zoom-in::before{
  content:""; }

.bp3-icon-zoom-out::before{
  content:""; }

.bp3-icon-zoom-to-fit::before{
  content:""; }
.bp3-submenu > .bp3-popover-wrapper{
  display:block; }

.bp3-submenu .bp3-popover-target{
  display:block; }

.bp3-submenu.bp3-popover{
  -webkit-box-shadow:none;
          box-shadow:none;
  padding:0 5px; }
  .bp3-submenu.bp3-popover > .bp3-popover-content{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-submenu.bp3-popover, .bp3-submenu.bp3-popover.bp3-dark{
    -webkit-box-shadow:none;
            box-shadow:none; }
    .bp3-dark .bp3-submenu.bp3-popover > .bp3-popover-content, .bp3-submenu.bp3-popover.bp3-dark > .bp3-popover-content{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
.bp3-menu{
  margin:0;
  border-radius:3px;
  background:#ffffff;
  min-width:180px;
  padding:5px;
  list-style:none;
  text-align:left;
  color:#182026; }

.bp3-menu-divider{
  display:block;
  margin:5px;
  border-top:1px solid rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-menu-divider{
    border-top-color:rgba(255, 255, 255, 0.15); }

.bp3-menu-item{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  border-radius:2px;
  padding:5px 7px;
  text-decoration:none;
  line-height:20px;
  color:inherit;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-menu-item > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-menu-item > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-menu-item::before,
  .bp3-menu-item > *{
    margin-right:7px; }
  .bp3-menu-item:empty::before,
  .bp3-menu-item > :last-child{
    margin-right:0; }
  .bp3-menu-item > .bp3-fill{
    word-break:break-word; }
  .bp3-menu-item:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
    background-color:rgba(167, 182, 194, 0.3);
    cursor:pointer;
    text-decoration:none; }
  .bp3-menu-item.bp3-disabled{
    background-color:inherit;
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-dark .bp3-menu-item{
    color:inherit; }
    .bp3-dark .bp3-menu-item:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
      background-color:rgba(138, 155, 168, 0.15);
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-disabled{
      background-color:inherit;
      color:rgba(167, 182, 194, 0.6); }
  .bp3-menu-item.bp3-intent-primary{
    color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-primary::before, .bp3-menu-item.bp3-intent-primary::after,
    .bp3-menu-item.bp3-intent-primary .bp3-menu-item-label{
      color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-menu-item.bp3-intent-primary.bp3-active{
      background-color:#137cbd; }
    .bp3-menu-item.bp3-intent-primary:active{
      background-color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-menu-item.bp3-intent-primary:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-menu-item.bp3-intent-primary:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-primary:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-primary:active, .bp3-menu-item.bp3-intent-primary:active::before, .bp3-menu-item.bp3-intent-primary:active::after,
    .bp3-menu-item.bp3-intent-primary:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-primary.bp3-active, .bp3-menu-item.bp3-intent-primary.bp3-active::before, .bp3-menu-item.bp3-intent-primary.bp3-active::after,
    .bp3-menu-item.bp3-intent-primary.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-success{
    color:#0d8050; }
    .bp3-menu-item.bp3-intent-success .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-success::before, .bp3-menu-item.bp3-intent-success::after,
    .bp3-menu-item.bp3-intent-success .bp3-menu-item-label{
      color:#0d8050; }
    .bp3-menu-item.bp3-intent-success:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-menu-item.bp3-intent-success.bp3-active{
      background-color:#0f9960; }
    .bp3-menu-item.bp3-intent-success:active{
      background-color:#0d8050; }
    .bp3-menu-item.bp3-intent-success:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-menu-item.bp3-intent-success:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-menu-item.bp3-intent-success:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-success:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-success:active, .bp3-menu-item.bp3-intent-success:active::before, .bp3-menu-item.bp3-intent-success:active::after,
    .bp3-menu-item.bp3-intent-success:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-success.bp3-active, .bp3-menu-item.bp3-intent-success.bp3-active::before, .bp3-menu-item.bp3-intent-success.bp3-active::after,
    .bp3-menu-item.bp3-intent-success.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-warning{
    color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-warning::before, .bp3-menu-item.bp3-intent-warning::after,
    .bp3-menu-item.bp3-intent-warning .bp3-menu-item-label{
      color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-menu-item.bp3-intent-warning.bp3-active{
      background-color:#d9822b; }
    .bp3-menu-item.bp3-intent-warning:active{
      background-color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-menu-item.bp3-intent-warning:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-menu-item.bp3-intent-warning:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-warning:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-warning:active, .bp3-menu-item.bp3-intent-warning:active::before, .bp3-menu-item.bp3-intent-warning:active::after,
    .bp3-menu-item.bp3-intent-warning:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-warning.bp3-active, .bp3-menu-item.bp3-intent-warning.bp3-active::before, .bp3-menu-item.bp3-intent-warning.bp3-active::after,
    .bp3-menu-item.bp3-intent-warning.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-danger{
    color:#c23030; }
    .bp3-menu-item.bp3-intent-danger .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-danger::before, .bp3-menu-item.bp3-intent-danger::after,
    .bp3-menu-item.bp3-intent-danger .bp3-menu-item-label{
      color:#c23030; }
    .bp3-menu-item.bp3-intent-danger:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-menu-item.bp3-intent-danger.bp3-active{
      background-color:#db3737; }
    .bp3-menu-item.bp3-intent-danger:active{
      background-color:#c23030; }
    .bp3-menu-item.bp3-intent-danger:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-menu-item.bp3-intent-danger:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-menu-item.bp3-intent-danger:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-danger:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-danger:active, .bp3-menu-item.bp3-intent-danger:active::before, .bp3-menu-item.bp3-intent-danger:active::after,
    .bp3-menu-item.bp3-intent-danger:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-danger.bp3-active, .bp3-menu-item.bp3-intent-danger.bp3-active::before, .bp3-menu-item.bp3-intent-danger.bp3-active::after,
    .bp3-menu-item.bp3-intent-danger.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item::before{
    line-height:1;
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-weight:400;
    font-style:normal;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    margin-right:7px; }
  .bp3-menu-item::before,
  .bp3-menu-item > .bp3-icon{
    margin-top:2px;
    color:#5c7080; }
  .bp3-menu-item .bp3-menu-item-label{
    color:#5c7080; }
  .bp3-menu-item:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
    color:inherit; }
  .bp3-menu-item.bp3-active, .bp3-menu-item:active{
    background-color:rgba(115, 134, 148, 0.3); }
  .bp3-menu-item.bp3-disabled{
    outline:none !important;
    background-color:inherit !important;
    cursor:not-allowed !important;
    color:rgba(92, 112, 128, 0.6) !important; }
    .bp3-menu-item.bp3-disabled::before,
    .bp3-menu-item.bp3-disabled > .bp3-icon,
    .bp3-menu-item.bp3-disabled .bp3-menu-item-label{
      color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-large .bp3-menu-item{
    padding:9px 7px;
    line-height:22px;
    font-size:16px; }
    .bp3-large .bp3-menu-item .bp3-icon{
      margin-top:3px; }
    .bp3-large .bp3-menu-item::before{
      line-height:1;
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-weight:400;
      font-style:normal;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased;
      margin-top:1px;
      margin-right:10px; }

button.bp3-menu-item{
  border:none;
  background:none;
  width:100%;
  text-align:left; }
.bp3-menu-header{
  display:block;
  margin:5px;
  border-top:1px solid rgba(16, 22, 26, 0.15);
  cursor:default;
  padding-left:2px; }
  .bp3-dark .bp3-menu-header{
    border-top-color:rgba(255, 255, 255, 0.15); }
  .bp3-menu-header:first-of-type{
    border-top:none; }
  .bp3-menu-header > h6{
    color:#182026;
    font-weight:600;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    margin:0;
    padding:10px 7px 0 1px;
    line-height:17px; }
    .bp3-dark .bp3-menu-header > h6{
      color:#f5f8fa; }
  .bp3-menu-header:first-of-type > h6{
    padding-top:0; }
  .bp3-large .bp3-menu-header > h6{
    padding-top:15px;
    padding-bottom:5px;
    font-size:18px; }
  .bp3-large .bp3-menu-header:first-of-type > h6{
    padding-top:0; }

.bp3-dark .bp3-menu{
  background:#30404d;
  color:#f5f8fa; }

.bp3-dark .bp3-menu-item.bp3-intent-primary{
  color:#48aff0; }
  .bp3-dark .bp3-menu-item.bp3-intent-primary .bp3-icon{
    color:inherit; }
  .bp3-dark .bp3-menu-item.bp3-intent-primary::before, .bp3-dark .bp3-menu-item.bp3-intent-primary::after,
  .bp3-dark .bp3-menu-item.bp3-intent-primary .bp3-menu-item-label{
    color:#48aff0; }
  .bp3-dark .bp3-menu-item.bp3-intent-primary:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active{
    background-color:#137cbd; }
  .bp3-dark .bp3-menu-item.bp3-intent-primary:active{
    background-color:#106ba3; }
  .bp3-dark .bp3-menu-item.bp3-intent-primary:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-primary:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-primary:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after,
  .bp3-dark .bp3-menu-item.bp3-intent-primary:hover .bp3-menu-item-label,
  .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label,
  .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-primary:active, .bp3-dark .bp3-menu-item.bp3-intent-primary:active::before, .bp3-dark .bp3-menu-item.bp3-intent-primary:active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-primary:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active .bp3-menu-item-label{
    color:#ffffff; }

.bp3-dark .bp3-menu-item.bp3-intent-success{
  color:#3dcc91; }
  .bp3-dark .bp3-menu-item.bp3-intent-success .bp3-icon{
    color:inherit; }
  .bp3-dark .bp3-menu-item.bp3-intent-success::before, .bp3-dark .bp3-menu-item.bp3-intent-success::after,
  .bp3-dark .bp3-menu-item.bp3-intent-success .bp3-menu-item-label{
    color:#3dcc91; }
  .bp3-dark .bp3-menu-item.bp3-intent-success:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active{
    background-color:#0f9960; }
  .bp3-dark .bp3-menu-item.bp3-intent-success:active{
    background-color:#0d8050; }
  .bp3-dark .bp3-menu-item.bp3-intent-success:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-success:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-success:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after,
  .bp3-dark .bp3-menu-item.bp3-intent-success:hover .bp3-menu-item-label,
  .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label,
  .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-success:active, .bp3-dark .bp3-menu-item.bp3-intent-success:active::before, .bp3-dark .bp3-menu-item.bp3-intent-success:active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-success:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active .bp3-menu-item-label{
    color:#ffffff; }

.bp3-dark .bp3-menu-item.bp3-intent-warning{
  color:#ffb366; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning .bp3-icon{
    color:inherit; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning::before, .bp3-dark .bp3-menu-item.bp3-intent-warning::after,
  .bp3-dark .bp3-menu-item.bp3-intent-warning .bp3-menu-item-label{
    color:#ffb366; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active{
    background-color:#d9822b; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning:active{
    background-color:#bf7326; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-warning:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-warning:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after,
  .bp3-dark .bp3-menu-item.bp3-intent-warning:hover .bp3-menu-item-label,
  .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label,
  .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-warning:active, .bp3-dark .bp3-menu-item.bp3-intent-warning:active::before, .bp3-dark .bp3-menu-item.bp3-intent-warning:active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-warning:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active .bp3-menu-item-label{
    color:#ffffff; }

.bp3-dark .bp3-menu-item.bp3-intent-danger{
  color:#ff7373; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger .bp3-icon{
    color:inherit; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger::before, .bp3-dark .bp3-menu-item.bp3-intent-danger::after,
  .bp3-dark .bp3-menu-item.bp3-intent-danger .bp3-menu-item-label{
    color:#ff7373; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active{
    background-color:#db3737; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger:active{
    background-color:#c23030; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-danger:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-danger:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after,
  .bp3-dark .bp3-menu-item.bp3-intent-danger:hover .bp3-menu-item-label,
  .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label,
  .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-danger:active, .bp3-dark .bp3-menu-item.bp3-intent-danger:active::before, .bp3-dark .bp3-menu-item.bp3-intent-danger:active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-danger:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active .bp3-menu-item-label{
    color:#ffffff; }

.bp3-dark .bp3-menu-item::before,
.bp3-dark .bp3-menu-item > .bp3-icon{
  color:#a7b6c2; }

.bp3-dark .bp3-menu-item .bp3-menu-item-label{
  color:#a7b6c2; }

.bp3-dark .bp3-menu-item.bp3-active, .bp3-dark .bp3-menu-item:active{
  background-color:rgba(138, 155, 168, 0.3); }

.bp3-dark .bp3-menu-item.bp3-disabled{
  color:rgba(167, 182, 194, 0.6) !important; }
  .bp3-dark .bp3-menu-item.bp3-disabled::before,
  .bp3-dark .bp3-menu-item.bp3-disabled > .bp3-icon,
  .bp3-dark .bp3-menu-item.bp3-disabled .bp3-menu-item-label{
    color:rgba(167, 182, 194, 0.6) !important; }

.bp3-dark .bp3-menu-divider,
.bp3-dark .bp3-menu-header{
  border-color:rgba(255, 255, 255, 0.15); }

.bp3-dark .bp3-menu-header > h6{
  color:#f5f8fa; }

.bp3-label .bp3-menu{
  margin-top:5px; }
.bp3-navbar{
  position:relative;
  z-index:10;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  background-color:#ffffff;
  width:100%;
  height:50px;
  padding:0 15px; }
  .bp3-navbar.bp3-dark,
  .bp3-dark .bp3-navbar{
    background-color:#394b59; }
  .bp3-navbar.bp3-dark{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-navbar{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-navbar.bp3-fixed-top{
    position:fixed;
    top:0;
    right:0;
    left:0; }

.bp3-navbar-heading{
  margin-right:15px;
  font-size:16px; }

.bp3-navbar-group{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  height:50px; }
  .bp3-navbar-group.bp3-align-left{
    float:left; }
  .bp3-navbar-group.bp3-align-right{
    float:right; }

.bp3-navbar-divider{
  margin:0 10px;
  border-left:1px solid rgba(16, 22, 26, 0.15);
  height:20px; }
  .bp3-dark .bp3-navbar-divider{
    border-left-color:rgba(255, 255, 255, 0.15); }
.bp3-non-ideal-state{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  width:100%;
  height:100%;
  text-align:center; }
  .bp3-non-ideal-state > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-non-ideal-state > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-non-ideal-state::before,
  .bp3-non-ideal-state > *{
    margin-bottom:20px; }
  .bp3-non-ideal-state:empty::before,
  .bp3-non-ideal-state > :last-child{
    margin-bottom:0; }
  .bp3-non-ideal-state > *{
    max-width:400px; }

.bp3-non-ideal-state-visual{
  color:rgba(92, 112, 128, 0.6);
  font-size:60px; }
  .bp3-dark .bp3-non-ideal-state-visual{
    color:rgba(167, 182, 194, 0.6); }

.bp3-overflow-list{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-wrap:nowrap;
      flex-wrap:nowrap;
  min-width:0; }

.bp3-overflow-list-spacer{
  -ms-flex-negative:1;
      flex-shrink:1;
  width:1px; }

body.bp3-overlay-open{
  overflow:hidden; }

.bp3-overlay{
  position:static;
  top:0;
  right:0;
  bottom:0;
  left:0;
  z-index:20; }
  .bp3-overlay:not(.bp3-overlay-open){
    pointer-events:none; }
  .bp3-overlay.bp3-overlay-container{
    position:fixed;
    overflow:hidden; }
    .bp3-overlay.bp3-overlay-container.bp3-overlay-inline{
      position:absolute; }
  .bp3-overlay.bp3-overlay-scroll-container{
    position:fixed;
    overflow:auto; }
    .bp3-overlay.bp3-overlay-scroll-container.bp3-overlay-inline{
      position:absolute; }
  .bp3-overlay.bp3-overlay-inline{
    display:inline;
    overflow:visible; }

.bp3-overlay-content{
  position:fixed;
  z-index:20; }
  .bp3-overlay-inline .bp3-overlay-content,
  .bp3-overlay-scroll-container .bp3-overlay-content{
    position:absolute; }

.bp3-overlay-backdrop{
  position:fixed;
  top:0;
  right:0;
  bottom:0;
  left:0;
  opacity:1;
  z-index:20;
  background-color:rgba(16, 22, 26, 0.7);
  overflow:auto;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-overlay-backdrop.bp3-overlay-enter, .bp3-overlay-backdrop.bp3-overlay-appear{
    opacity:0; }
  .bp3-overlay-backdrop.bp3-overlay-enter-active, .bp3-overlay-backdrop.bp3-overlay-appear-active{
    opacity:1;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-overlay-backdrop.bp3-overlay-exit{
    opacity:1; }
  .bp3-overlay-backdrop.bp3-overlay-exit-active{
    opacity:0;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-overlay-backdrop:focus{
    outline:none; }
  .bp3-overlay-inline .bp3-overlay-backdrop{
    position:absolute; }
.bp3-panel-stack{
  position:relative;
  overflow:hidden; }

.bp3-panel-stack-header{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-negative:0;
      flex-shrink:0;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  z-index:1;
  -webkit-box-shadow:0 1px rgba(16, 22, 26, 0.15);
          box-shadow:0 1px rgba(16, 22, 26, 0.15);
  height:30px; }
  .bp3-dark .bp3-panel-stack-header{
    -webkit-box-shadow:0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 1px rgba(255, 255, 255, 0.15); }
  .bp3-panel-stack-header > span{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1;
            flex:1;
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch; }
  .bp3-panel-stack-header .bp3-heading{
    margin:0 5px; }

.bp3-button.bp3-panel-stack-header-back{
  margin-left:5px;
  padding-left:0;
  white-space:nowrap; }
  .bp3-button.bp3-panel-stack-header-back .bp3-icon{
    margin:0 2px; }

.bp3-panel-stack-view{
  position:absolute;
  top:0;
  right:0;
  bottom:0;
  left:0;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin-right:-1px;
  border-right:1px solid rgba(16, 22, 26, 0.15);
  background-color:#ffffff;
  overflow-y:auto; }
  .bp3-dark .bp3-panel-stack-view{
    background-color:#30404d; }

.bp3-panel-stack-push .bp3-panel-stack-enter, .bp3-panel-stack-push .bp3-panel-stack-appear{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0; }

.bp3-panel-stack-push .bp3-panel-stack-enter-active, .bp3-panel-stack-push .bp3-panel-stack-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease;
  -webkit-transition-delay:0;
          transition-delay:0; }

.bp3-panel-stack-push .bp3-panel-stack-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack-push .bp3-panel-stack-exit-active{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease;
  -webkit-transition-delay:0;
          transition-delay:0; }

.bp3-panel-stack-pop .bp3-panel-stack-enter, .bp3-panel-stack-pop .bp3-panel-stack-appear{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0; }

.bp3-panel-stack-pop .bp3-panel-stack-enter-active, .bp3-panel-stack-pop .bp3-panel-stack-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease;
  -webkit-transition-delay:0;
          transition-delay:0; }

.bp3-panel-stack-pop .bp3-panel-stack-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack-pop .bp3-panel-stack-exit-active{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease;
  -webkit-transition-delay:0;
          transition-delay:0; }
.bp3-popover{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  -webkit-transform:scale(1);
          transform:scale(1);
  display:inline-block;
  z-index:20;
  border-radius:3px; }
  .bp3-popover .bp3-popover-arrow{
    position:absolute;
    width:30px;
    height:30px; }
    .bp3-popover .bp3-popover-arrow::before{
      margin:5px;
      width:20px;
      height:20px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover{
    margin-top:-17px;
    margin-bottom:17px; }
    .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow{
      bottom:-11px; }
      .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(-90deg);
                transform:rotate(-90deg); }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover{
    margin-left:17px; }
    .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow{
      left:-11px; }
      .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(0);
                transform:rotate(0); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover{
    margin-top:17px; }
    .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow{
      top:-11px; }
      .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(90deg);
                transform:rotate(90deg); }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover{
    margin-right:17px;
    margin-left:-17px; }
    .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow{
      right:-11px; }
      .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(180deg);
                transform:rotate(180deg); }
  .bp3-tether-element-attached-middle > .bp3-popover > .bp3-popover-arrow{
    top:50%;
    -webkit-transform:translateY(-50%);
            transform:translateY(-50%); }
  .bp3-tether-element-attached-center > .bp3-popover > .bp3-popover-arrow{
    right:50%;
    -webkit-transform:translateX(50%);
            transform:translateX(50%); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow{
    top:-0.3934px; }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow{
    right:-0.3934px; }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow{
    left:-0.3934px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow{
    bottom:-0.3934px; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:top left;
            transform-origin:top left; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:top center;
            transform-origin:top center; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:top right;
            transform-origin:top right; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:center left;
            transform-origin:center left; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:center center;
            transform-origin:center center; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:center right;
            transform-origin:center right; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:bottom left;
            transform-origin:bottom left; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:bottom center;
            transform-origin:bottom center; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:bottom right;
            transform-origin:bottom right; }
  .bp3-popover .bp3-popover-content{
    background:#ffffff;
    color:inherit; }
  .bp3-popover .bp3-popover-arrow::before{
    -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2);
            box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2); }
  .bp3-popover .bp3-popover-arrow-border{
    fill:#10161a;
    fill-opacity:0.1; }
  .bp3-popover .bp3-popover-arrow-fill{
    fill:#ffffff; }
  .bp3-popover-enter > .bp3-popover, .bp3-popover-appear > .bp3-popover{
    -webkit-transform:scale(0.3);
            transform:scale(0.3); }
  .bp3-popover-enter-active > .bp3-popover, .bp3-popover-appear-active > .bp3-popover{
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-popover-exit > .bp3-popover{
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-popover-exit-active > .bp3-popover{
    -webkit-transform:scale(0.3);
            transform:scale(0.3);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-popover .bp3-popover-content{
    position:relative;
    border-radius:3px; }
  .bp3-popover.bp3-popover-content-sizing .bp3-popover-content{
    max-width:350px;
    padding:20px; }
  .bp3-popover-target + .bp3-overlay .bp3-popover.bp3-popover-content-sizing{
    width:350px; }
  .bp3-popover.bp3-minimal{
    margin:0 !important; }
    .bp3-popover.bp3-minimal .bp3-popover-arrow{
      display:none; }
    .bp3-popover.bp3-minimal.bp3-popover{
      -webkit-transform:scale(1);
              transform:scale(1); }
      .bp3-popover-enter > .bp3-popover.bp3-minimal.bp3-popover, .bp3-popover-appear > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1); }
      .bp3-popover-enter-active > .bp3-popover.bp3-minimal.bp3-popover, .bp3-popover-appear-active > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1);
        -webkit-transition-property:-webkit-transform;
        transition-property:-webkit-transform;
        transition-property:transform;
        transition-property:transform, -webkit-transform;
        -webkit-transition-duration:100ms;
                transition-duration:100ms;
        -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
                transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
        -webkit-transition-delay:0;
                transition-delay:0; }
      .bp3-popover-exit > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1); }
      .bp3-popover-exit-active > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1);
        -webkit-transition-property:-webkit-transform;
        transition-property:-webkit-transform;
        transition-property:transform;
        transition-property:transform, -webkit-transform;
        -webkit-transition-duration:100ms;
                transition-duration:100ms;
        -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
                transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
        -webkit-transition-delay:0;
                transition-delay:0; }
  .bp3-popover.bp3-dark,
  .bp3-dark .bp3-popover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-popover.bp3-dark .bp3-popover-content,
    .bp3-dark .bp3-popover .bp3-popover-content{
      background:#30404d;
      color:inherit; }
    .bp3-popover.bp3-dark .bp3-popover-arrow::before,
    .bp3-dark .bp3-popover .bp3-popover-arrow::before{
      -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4);
              box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4); }
    .bp3-popover.bp3-dark .bp3-popover-arrow-border,
    .bp3-dark .bp3-popover .bp3-popover-arrow-border{
      fill:#10161a;
      fill-opacity:0.2; }
    .bp3-popover.bp3-dark .bp3-popover-arrow-fill,
    .bp3-dark .bp3-popover .bp3-popover-arrow-fill{
      fill:#30404d; }

.bp3-popover-arrow::before{
  display:block;
  position:absolute;
  -webkit-transform:rotate(45deg);
          transform:rotate(45deg);
  border-radius:2px;
  content:""; }

.bp3-tether-pinned .bp3-popover-arrow{
  display:none; }

.bp3-popover-backdrop{
  background:rgba(255, 255, 255, 0); }

.bp3-transition-container{
  opacity:1;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  z-index:20; }
  .bp3-transition-container.bp3-popover-enter, .bp3-transition-container.bp3-popover-appear{
    opacity:0; }
  .bp3-transition-container.bp3-popover-enter-active, .bp3-transition-container.bp3-popover-appear-active{
    opacity:1;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-transition-container.bp3-popover-exit{
    opacity:1; }
  .bp3-transition-container.bp3-popover-exit-active{
    opacity:0;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-transition-container:focus{
    outline:none; }
  .bp3-transition-container.bp3-popover-leave .bp3-popover-content{
    pointer-events:none; }
  .bp3-transition-container[data-x-out-of-boundaries]{
    display:none; }

span.bp3-popover-target{
  display:inline-block; }

.bp3-popover-wrapper.bp3-fill{
  width:100%; }

.bp3-portal{
  position:absolute;
  top:0;
  right:0;
  left:0; }
@-webkit-keyframes linear-progress-bar-stripes{
  from{
    background-position:0 0; }
  to{
    background-position:30px 0; } }
@keyframes linear-progress-bar-stripes{
  from{
    background-position:0 0; }
  to{
    background-position:30px 0; } }

.bp3-progress-bar{
  display:block;
  position:relative;
  border-radius:40px;
  background:rgba(92, 112, 128, 0.2);
  width:100%;
  height:8px;
  overflow:hidden; }
  .bp3-progress-bar .bp3-progress-meter{
    position:absolute;
    border-radius:40px;
    background:linear-gradient(-45deg, rgba(255, 255, 255, 0.2) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.2) 50%, rgba(255, 255, 255, 0.2) 75%, transparent 75%);
    background-color:rgba(92, 112, 128, 0.8);
    background-size:30px 30px;
    width:100%;
    height:100%;
    -webkit-transition:width 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:width 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-progress-bar:not(.bp3-no-animation):not(.bp3-no-stripes) .bp3-progress-meter{
    animation:linear-progress-bar-stripes 300ms linear infinite reverse; }
  .bp3-progress-bar.bp3-no-stripes .bp3-progress-meter{
    background-image:none; }

.bp3-dark .bp3-progress-bar{
  background:rgba(16, 22, 26, 0.5); }
  .bp3-dark .bp3-progress-bar .bp3-progress-meter{
    background-color:#8a9ba8; }

.bp3-progress-bar.bp3-intent-primary .bp3-progress-meter{
  background-color:#137cbd; }

.bp3-progress-bar.bp3-intent-success .bp3-progress-meter{
  background-color:#0f9960; }

.bp3-progress-bar.bp3-intent-warning .bp3-progress-meter{
  background-color:#d9822b; }

.bp3-progress-bar.bp3-intent-danger .bp3-progress-meter{
  background-color:#db3737; }
@-webkit-keyframes skeleton-glow{
  from{
    border-color:rgba(206, 217, 224, 0.2);
    background:rgba(206, 217, 224, 0.2); }
  to{
    border-color:rgba(92, 112, 128, 0.2);
    background:rgba(92, 112, 128, 0.2); } }
@keyframes skeleton-glow{
  from{
    border-color:rgba(206, 217, 224, 0.2);
    background:rgba(206, 217, 224, 0.2); }
  to{
    border-color:rgba(92, 112, 128, 0.2);
    background:rgba(92, 112, 128, 0.2); } }
.bp3-skeleton{
  border-color:rgba(206, 217, 224, 0.2) !important;
  border-radius:2px;
  -webkit-box-shadow:none !important;
          box-shadow:none !important;
  background:rgba(206, 217, 224, 0.2);
  background-clip:padding-box !important;
  cursor:default;
  color:transparent !important;
  -webkit-animation:1000ms linear infinite alternate skeleton-glow;
          animation:1000ms linear infinite alternate skeleton-glow;
  pointer-events:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-skeleton::before, .bp3-skeleton::after,
  .bp3-skeleton *{
    visibility:hidden !important; }
.bp3-slider{
  width:100%;
  min-width:150px;
  height:40px;
  position:relative;
  outline:none;
  cursor:default;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-slider:hover{
    cursor:pointer; }
  .bp3-slider:active{
    cursor:-webkit-grabbing;
    cursor:grabbing; }
  .bp3-slider.bp3-disabled{
    opacity:0.5;
    cursor:not-allowed; }
  .bp3-slider.bp3-slider-unlabeled{
    height:16px; }

.bp3-slider-track,
.bp3-slider-progress{
  top:5px;
  right:0;
  left:0;
  height:6px;
  position:absolute; }

.bp3-slider-track{
  border-radius:3px;
  overflow:hidden; }

.bp3-slider-progress{
  background:rgba(92, 112, 128, 0.2); }
  .bp3-dark .bp3-slider-progress{
    background:rgba(16, 22, 26, 0.5); }
  .bp3-slider-progress.bp3-intent-primary{
    background-color:#137cbd; }
  .bp3-slider-progress.bp3-intent-success{
    background-color:#0f9960; }
  .bp3-slider-progress.bp3-intent-warning{
    background-color:#d9822b; }
  .bp3-slider-progress.bp3-intent-danger{
    background-color:#db3737; }

.bp3-slider-handle{
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
  background-color:#f5f8fa;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
  color:#182026;
  position:absolute;
  top:0;
  left:0;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
  cursor:pointer;
  width:16px;
  height:16px; }
  .bp3-slider-handle:hover{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-clip:padding-box;
    background-color:#ebf1f5; }
  .bp3-slider-handle:active, .bp3-slider-handle.bp3-active{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#d8e1e8;
    background-image:none; }
  .bp3-slider-handle:disabled, .bp3-slider-handle.bp3-disabled{
    outline:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    background-color:rgba(206, 217, 224, 0.5);
    background-image:none;
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
    .bp3-slider-handle:disabled.bp3-active, .bp3-slider-handle:disabled.bp3-active:hover, .bp3-slider-handle.bp3-disabled.bp3-active, .bp3-slider-handle.bp3-disabled.bp3-active:hover{
      background:rgba(206, 217, 224, 0.7); }
  .bp3-slider-handle:focus{
    z-index:1; }
  .bp3-slider-handle:hover{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-clip:padding-box;
    background-color:#ebf1f5;
    z-index:2;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
    cursor:-webkit-grab;
    cursor:grab; }
  .bp3-slider-handle.bp3-active{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 1px rgba(16, 22, 26, 0.1);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 1px rgba(16, 22, 26, 0.1);
    cursor:-webkit-grabbing;
    cursor:grabbing; }
  .bp3-disabled .bp3-slider-handle{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:#bfccd6;
    pointer-events:none; }
  .bp3-dark .bp3-slider-handle{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background-color:#394b59;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
    color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle:hover, .bp3-dark .bp3-slider-handle:active, .bp3-dark .bp3-slider-handle.bp3-active{
      color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle:hover{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      background-color:#30404d; }
    .bp3-dark .bp3-slider-handle:active, .bp3-dark .bp3-slider-handle.bp3-active{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#202b33;
      background-image:none; }
    .bp3-dark .bp3-slider-handle:disabled, .bp3-dark .bp3-slider-handle.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(57, 75, 89, 0.5);
      background-image:none;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-slider-handle:disabled.bp3-active, .bp3-dark .bp3-slider-handle.bp3-disabled.bp3-active{
        background:rgba(57, 75, 89, 0.7); }
    .bp3-dark .bp3-slider-handle .bp3-button-spinner .bp3-spinner-head{
      background:rgba(16, 22, 26, 0.5);
      stroke:#8a9ba8; }
    .bp3-dark .bp3-slider-handle, .bp3-dark .bp3-slider-handle:hover{
      background-color:#394b59; }
    .bp3-dark .bp3-slider-handle.bp3-active{
      background-color:#293742; }
  .bp3-dark .bp3-disabled .bp3-slider-handle{
    border-color:#5c7080;
    -webkit-box-shadow:none;
            box-shadow:none;
    background:#5c7080; }
  .bp3-slider-handle .bp3-slider-label{
    margin-left:8px;
    border-radius:3px;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
    background:#394b59;
    color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle .bp3-slider-label{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
      background:#e1e8ed;
      color:#394b59; }
    .bp3-disabled .bp3-slider-handle .bp3-slider-label{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-slider-handle.bp3-start, .bp3-slider-handle.bp3-end{
    width:8px; }
  .bp3-slider-handle.bp3-start{
    border-top-right-radius:0;
    border-bottom-right-radius:0; }
  .bp3-slider-handle.bp3-end{
    margin-left:8px;
    border-top-left-radius:0;
    border-bottom-left-radius:0; }
    .bp3-slider-handle.bp3-end .bp3-slider-label{
      margin-left:0; }

.bp3-slider-label{
  -webkit-transform:translate(-50%, 20px);
          transform:translate(-50%, 20px);
  display:inline-block;
  position:absolute;
  padding:2px 5px;
  vertical-align:top;
  line-height:1;
  font-size:12px; }

.bp3-slider.bp3-vertical{
  width:40px;
  min-width:40px;
  height:150px; }
  .bp3-slider.bp3-vertical .bp3-slider-track,
  .bp3-slider.bp3-vertical .bp3-slider-progress{
    top:0;
    bottom:0;
    left:5px;
    width:6px;
    height:auto; }
  .bp3-slider.bp3-vertical .bp3-slider-progress{
    top:auto; }
  .bp3-slider.bp3-vertical .bp3-slider-label{
    -webkit-transform:translate(20px, 50%);
            transform:translate(20px, 50%); }
  .bp3-slider.bp3-vertical .bp3-slider-handle{
    top:auto; }
    .bp3-slider.bp3-vertical .bp3-slider-handle .bp3-slider-label{
      margin-top:-8px;
      margin-left:0; }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-end, .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start{
      margin-left:0;
      width:16px;
      height:8px; }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start{
      border-top-left-radius:0;
      border-bottom-right-radius:3px; }
      .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start .bp3-slider-label{
        -webkit-transform:translate(20px);
                transform:translate(20px); }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-end{
      margin-bottom:8px;
      border-top-left-radius:3px;
      border-bottom-left-radius:0;
      border-bottom-right-radius:0; }

@-webkit-keyframes pt-spinner-animation{
  from{
    -webkit-transform:rotate(0deg);
            transform:rotate(0deg); }
  to{
    -webkit-transform:rotate(360deg);
            transform:rotate(360deg); } }

@keyframes pt-spinner-animation{
  from{
    -webkit-transform:rotate(0deg);
            transform:rotate(0deg); }
  to{
    -webkit-transform:rotate(360deg);
            transform:rotate(360deg); } }

.bp3-spinner{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  overflow:visible;
  vertical-align:middle; }
  .bp3-spinner svg{
    display:block; }
  .bp3-spinner path{
    fill-opacity:0; }
  .bp3-spinner .bp3-spinner-head{
    -webkit-transform-origin:center;
            transform-origin:center;
    -webkit-transition:stroke-dashoffset 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:stroke-dashoffset 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    stroke:rgba(92, 112, 128, 0.8);
    stroke-linecap:round; }
  .bp3-spinner .bp3-spinner-track{
    stroke:rgba(92, 112, 128, 0.2); }

.bp3-spinner-animation{
  -webkit-animation:pt-spinner-animation 500ms linear infinite;
          animation:pt-spinner-animation 500ms linear infinite; }
  .bp3-no-spin > .bp3-spinner-animation{
    -webkit-animation:none;
            animation:none; }

.bp3-dark .bp3-spinner .bp3-spinner-head{
  stroke:#8a9ba8; }

.bp3-dark .bp3-spinner .bp3-spinner-track{
  stroke:rgba(16, 22, 26, 0.5); }

.bp3-spinner.bp3-intent-primary .bp3-spinner-head{
  stroke:#137cbd; }

.bp3-spinner.bp3-intent-success .bp3-spinner-head{
  stroke:#0f9960; }

.bp3-spinner.bp3-intent-warning .bp3-spinner-head{
  stroke:#d9822b; }

.bp3-spinner.bp3-intent-danger .bp3-spinner-head{
  stroke:#db3737; }
.bp3-tabs.bp3-vertical{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }
  .bp3-tabs.bp3-vertical > .bp3-tab-list{
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column;
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start; }
    .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab{
      border-radius:3px;
      width:100%;
      padding:0 10px; }
      .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab[aria-selected="true"]{
        -webkit-box-shadow:none;
                box-shadow:none;
        background-color:rgba(19, 124, 189, 0.2); }
    .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab-indicator-wrapper .bp3-tab-indicator{
      top:0;
      right:0;
      bottom:0;
      left:0;
      border-radius:3px;
      background-color:rgba(19, 124, 189, 0.2);
      height:auto; }
  .bp3-tabs.bp3-vertical > .bp3-tab-panel{
    margin-top:0;
    padding-left:20px; }

.bp3-tab-list{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  -webkit-box-align:end;
      -ms-flex-align:end;
          align-items:flex-end;
  position:relative;
  margin:0;
  border:none;
  padding:0;
  list-style:none; }
  .bp3-tab-list > *:not(:last-child){
    margin-right:20px; }

.bp3-tab{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  position:relative;
  cursor:pointer;
  max-width:100%;
  vertical-align:top;
  line-height:30px;
  color:#182026;
  font-size:14px; }
  .bp3-tab a{
    display:block;
    text-decoration:none;
    color:inherit; }
  .bp3-tab-indicator-wrapper ~ .bp3-tab{
    -webkit-box-shadow:none !important;
            box-shadow:none !important;
    background-color:transparent !important; }
  .bp3-tab[aria-disabled="true"]{
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-tab[aria-selected="true"]{
    border-radius:0;
    -webkit-box-shadow:inset 0 -3px 0 #106ba3;
            box-shadow:inset 0 -3px 0 #106ba3; }
  .bp3-tab[aria-selected="true"], .bp3-tab:not([aria-disabled="true"]):hover{
    color:#106ba3; }
  .bp3-tab:focus{
    -moz-outline-radius:0; }
  .bp3-large > .bp3-tab{
    line-height:40px;
    font-size:16px; }

.bp3-tab-panel{
  margin-top:20px; }
  .bp3-tab-panel[aria-hidden="true"]{
    display:none; }

.bp3-tab-indicator-wrapper{
  position:absolute;
  top:0;
  left:0;
  -webkit-transform:translateX(0), translateY(0);
          transform:translateX(0), translateY(0);
  -webkit-transition:height, width, -webkit-transform;
  transition:height, width, -webkit-transform;
  transition:height, transform, width;
  transition:height, transform, width, -webkit-transform;
  -webkit-transition-duration:200ms;
          transition-duration:200ms;
  -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
          transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
  pointer-events:none; }
  .bp3-tab-indicator-wrapper .bp3-tab-indicator{
    position:absolute;
    right:0;
    bottom:0;
    left:0;
    background-color:#106ba3;
    height:3px; }
  .bp3-tab-indicator-wrapper.bp3-no-animation{
    -webkit-transition:none;
    transition:none; }

.bp3-dark .bp3-tab{
  color:#f5f8fa; }
  .bp3-dark .bp3-tab[aria-disabled="true"]{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-tab[aria-selected="true"]{
    -webkit-box-shadow:inset 0 -3px 0 #48aff0;
            box-shadow:inset 0 -3px 0 #48aff0; }
  .bp3-dark .bp3-tab[aria-selected="true"], .bp3-dark .bp3-tab:not([aria-disabled="true"]):hover{
    color:#48aff0; }

.bp3-dark .bp3-tab-indicator{
  background-color:#48aff0; }

.bp3-flex-expander{
  -webkit-box-flex:1;
      -ms-flex:1 1;
          flex:1 1; }
.bp3-tag{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  position:relative;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:none;
          box-shadow:none;
  background-color:#5c7080;
  min-width:20px;
  max-width:100%;
  min-height:20px;
  padding:2px 6px;
  line-height:16px;
  color:#f5f8fa;
  font-size:12px; }
  .bp3-tag.bp3-interactive{
    cursor:pointer; }
    .bp3-tag.bp3-interactive:hover{
      background-color:rgba(92, 112, 128, 0.85); }
    .bp3-tag.bp3-interactive.bp3-active, .bp3-tag.bp3-interactive:active{
      background-color:rgba(92, 112, 128, 0.7); }
  .bp3-tag > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-tag > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-tag::before,
  .bp3-tag > *{
    margin-right:4px; }
  .bp3-tag:empty::before,
  .bp3-tag > :last-child{
    margin-right:0; }
  .bp3-tag:focus{
    outline:rgba(19, 124, 189, 0.6) auto 2px;
    outline-offset:0;
    -moz-outline-radius:6px; }
  .bp3-tag.bp3-round{
    border-radius:30px;
    padding-right:8px;
    padding-left:8px; }
  .bp3-dark .bp3-tag{
    background-color:#bfccd6;
    color:#182026; }
    .bp3-dark .bp3-tag.bp3-interactive{
      cursor:pointer; }
      .bp3-dark .bp3-tag.bp3-interactive:hover{
        background-color:rgba(191, 204, 214, 0.85); }
      .bp3-dark .bp3-tag.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-interactive:active{
        background-color:rgba(191, 204, 214, 0.7); }
    .bp3-dark .bp3-tag > .bp3-icon, .bp3-dark .bp3-tag .bp3-icon-standard, .bp3-dark .bp3-tag .bp3-icon-large{
      fill:currentColor; }
  .bp3-tag > .bp3-icon, .bp3-tag .bp3-icon-standard, .bp3-tag .bp3-icon-large{
    fill:#ffffff; }
  .bp3-tag.bp3-large,
  .bp3-large .bp3-tag{
    min-width:30px;
    min-height:30px;
    padding:0 10px;
    line-height:20px;
    font-size:14px; }
    .bp3-tag.bp3-large::before,
    .bp3-tag.bp3-large > *,
    .bp3-large .bp3-tag::before,
    .bp3-large .bp3-tag > *{
      margin-right:7px; }
    .bp3-tag.bp3-large:empty::before,
    .bp3-tag.bp3-large > :last-child,
    .bp3-large .bp3-tag:empty::before,
    .bp3-large .bp3-tag > :last-child{
      margin-right:0; }
    .bp3-tag.bp3-large.bp3-round,
    .bp3-large .bp3-tag.bp3-round{
      padding-right:12px;
      padding-left:12px; }
  .bp3-tag.bp3-intent-primary{
    background:#137cbd;
    color:#ffffff; }
    .bp3-tag.bp3-intent-primary.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-primary.bp3-interactive:hover{
        background-color:rgba(19, 124, 189, 0.85); }
      .bp3-tag.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-primary.bp3-interactive:active{
        background-color:rgba(19, 124, 189, 0.7); }
  .bp3-tag.bp3-intent-success{
    background:#0f9960;
    color:#ffffff; }
    .bp3-tag.bp3-intent-success.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-success.bp3-interactive:hover{
        background-color:rgba(15, 153, 96, 0.85); }
      .bp3-tag.bp3-intent-success.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-success.bp3-interactive:active{
        background-color:rgba(15, 153, 96, 0.7); }
  .bp3-tag.bp3-intent-warning{
    background:#d9822b;
    color:#ffffff; }
    .bp3-tag.bp3-intent-warning.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-warning.bp3-interactive:hover{
        background-color:rgba(217, 130, 43, 0.85); }
      .bp3-tag.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-warning.bp3-interactive:active{
        background-color:rgba(217, 130, 43, 0.7); }
  .bp3-tag.bp3-intent-danger{
    background:#db3737;
    color:#ffffff; }
    .bp3-tag.bp3-intent-danger.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-danger.bp3-interactive:hover{
        background-color:rgba(219, 55, 55, 0.85); }
      .bp3-tag.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-danger.bp3-interactive:active{
        background-color:rgba(219, 55, 55, 0.7); }
  .bp3-tag.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-tag.bp3-minimal > .bp3-icon, .bp3-tag.bp3-minimal .bp3-icon-standard, .bp3-tag.bp3-minimal .bp3-icon-large{
    fill:#5c7080; }
  .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]){
    background-color:rgba(138, 155, 168, 0.2);
    color:#182026; }
    .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:hover{
        background-color:rgba(92, 112, 128, 0.3); }
      .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive.bp3-active, .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:active{
        background-color:rgba(92, 112, 128, 0.4); }
    .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]){
      color:#f5f8fa; }
      .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:hover{
          background-color:rgba(191, 204, 214, 0.3); }
        .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:active{
          background-color:rgba(191, 204, 214, 0.4); }
      .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) > .bp3-icon, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) .bp3-icon-standard, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) .bp3-icon-large{
        fill:#a7b6c2; }
  .bp3-tag.bp3-minimal.bp3-intent-primary{
    background-color:rgba(19, 124, 189, 0.15);
    color:#106ba3; }
    .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:hover{
        background-color:rgba(19, 124, 189, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:active{
        background-color:rgba(19, 124, 189, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-primary > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-primary .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-primary .bp3-icon-large{
      fill:#137cbd; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary{
      background-color:rgba(19, 124, 189, 0.25);
      color:#48aff0; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:hover{
          background-color:rgba(19, 124, 189, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:active{
          background-color:rgba(19, 124, 189, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-success{
    background-color:rgba(15, 153, 96, 0.15);
    color:#0d8050; }
    .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:hover{
        background-color:rgba(15, 153, 96, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:active{
        background-color:rgba(15, 153, 96, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-success > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-success .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-success .bp3-icon-large{
      fill:#0f9960; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success{
      background-color:rgba(15, 153, 96, 0.25);
      color:#3dcc91; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:hover{
          background-color:rgba(15, 153, 96, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:active{
          background-color:rgba(15, 153, 96, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-warning{
    background-color:rgba(217, 130, 43, 0.15);
    color:#bf7326; }
    .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:hover{
        background-color:rgba(217, 130, 43, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:active{
        background-color:rgba(217, 130, 43, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-warning > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-warning .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-warning .bp3-icon-large{
      fill:#d9822b; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning{
      background-color:rgba(217, 130, 43, 0.25);
      color:#ffb366; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:hover{
          background-color:rgba(217, 130, 43, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:active{
          background-color:rgba(217, 130, 43, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-danger{
    background-color:rgba(219, 55, 55, 0.15);
    color:#c23030; }
    .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:hover{
        background-color:rgba(219, 55, 55, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:active{
        background-color:rgba(219, 55, 55, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-danger > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-danger .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-danger .bp3-icon-large{
      fill:#db3737; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger{
      background-color:rgba(219, 55, 55, 0.25);
      color:#ff7373; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:hover{
          background-color:rgba(219, 55, 55, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:active{
          background-color:rgba(219, 55, 55, 0.45); }

.bp3-tag-remove{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  opacity:0.5;
  margin-top:-2px;
  margin-right:-6px !important;
  margin-bottom:-2px;
  border:none;
  background:none;
  cursor:pointer;
  padding:2px;
  padding-left:0;
  color:inherit; }
  .bp3-tag-remove:hover{
    opacity:0.8;
    background:none;
    text-decoration:none; }
  .bp3-tag-remove:active{
    opacity:1; }
  .bp3-tag-remove:empty::before{
    line-height:1;
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-weight:400;
    font-style:normal;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    content:""; }
  .bp3-large .bp3-tag-remove{
    margin-right:-10px !important;
    padding:5px;
    padding-left:0; }
    .bp3-large .bp3-tag-remove:empty::before{
      line-height:1;
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-weight:400;
      font-style:normal; }
.bp3-tag-input{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  cursor:text;
  height:auto;
  min-height:30px;
  padding-right:0;
  padding-left:5px;
  line-height:inherit; }
  .bp3-tag-input > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-tag-input > .bp3-tag-input-values{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-tag-input .bp3-tag-input-icon{
    margin-top:7px;
    margin-right:7px;
    margin-left:2px;
    color:#5c7080; }
  .bp3-tag-input .bp3-tag-input-values{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-orient:horizontal;
    -webkit-box-direction:normal;
        -ms-flex-direction:row;
            flex-direction:row;
    -ms-flex-wrap:wrap;
        flex-wrap:wrap;
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center;
    -ms-flex-item-align:stretch;
        align-self:stretch;
    margin-top:5px;
    margin-right:7px;
    min-width:0; }
    .bp3-tag-input .bp3-tag-input-values > *{
      -webkit-box-flex:0;
          -ms-flex-positive:0;
              flex-grow:0;
      -ms-flex-negative:0;
          flex-shrink:0; }
    .bp3-tag-input .bp3-tag-input-values > .bp3-fill{
      -webkit-box-flex:1;
          -ms-flex-positive:1;
              flex-grow:1;
      -ms-flex-negative:1;
          flex-shrink:1; }
    .bp3-tag-input .bp3-tag-input-values::before,
    .bp3-tag-input .bp3-tag-input-values > *{
      margin-right:5px; }
    .bp3-tag-input .bp3-tag-input-values:empty::before,
    .bp3-tag-input .bp3-tag-input-values > :last-child{
      margin-right:0; }
    .bp3-tag-input .bp3-tag-input-values:first-child .bp3-input-ghost:first-child{
      padding-left:5px; }
    .bp3-tag-input .bp3-tag-input-values > *{
      margin-bottom:5px; }
  .bp3-tag-input .bp3-tag{
    overflow-wrap:break-word; }
    .bp3-tag-input .bp3-tag.bp3-active{
      outline:rgba(19, 124, 189, 0.6) auto 2px;
      outline-offset:0;
      -moz-outline-radius:6px; }
  .bp3-tag-input .bp3-input-ghost{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:80px;
    line-height:20px; }
    .bp3-tag-input .bp3-input-ghost:disabled, .bp3-tag-input .bp3-input-ghost.bp3-disabled{
      cursor:not-allowed; }
  .bp3-tag-input .bp3-button,
  .bp3-tag-input .bp3-spinner{
    margin:3px;
    margin-left:0; }
  .bp3-tag-input .bp3-button{
    min-width:24px;
    min-height:24px;
    padding:0 7px; }
  .bp3-tag-input.bp3-large{
    height:auto;
    min-height:40px; }
    .bp3-tag-input.bp3-large::before,
    .bp3-tag-input.bp3-large > *{
      margin-right:10px; }
    .bp3-tag-input.bp3-large:empty::before,
    .bp3-tag-input.bp3-large > :last-child{
      margin-right:0; }
    .bp3-tag-input.bp3-large .bp3-tag-input-icon{
      margin-top:10px;
      margin-left:5px; }
    .bp3-tag-input.bp3-large .bp3-input-ghost{
      line-height:30px; }
    .bp3-tag-input.bp3-large .bp3-button{
      min-width:30px;
      min-height:30px;
      padding:5px 10px;
      margin:5px;
      margin-left:0; }
    .bp3-tag-input.bp3-large .bp3-spinner{
      margin:8px;
      margin-left:0; }
  .bp3-tag-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
    background-color:#ffffff; }
    .bp3-tag-input.bp3-active.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-success{
      -webkit-box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-tag-input .bp3-tag-input-icon, .bp3-tag-input.bp3-dark .bp3-tag-input-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-tag-input .bp3-input-ghost, .bp3-tag-input.bp3-dark .bp3-input-ghost{
    color:#f5f8fa; }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-webkit-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-moz-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost:-ms-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-ms-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::placeholder{
      color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-tag-input.bp3-active, .bp3-tag-input.bp3-dark.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    background-color:rgba(16, 22, 26, 0.3); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-primary, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-success, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-success{
      -webkit-box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-warning, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-danger, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-input-ghost{
  border:none;
  -webkit-box-shadow:none;
          box-shadow:none;
  background:none;
  padding:0; }
  .bp3-input-ghost::-webkit-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input-ghost::-moz-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input-ghost:-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input-ghost::-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input-ghost::placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input-ghost:focus{
    outline:none !important; }
.bp3-toast{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  position:relative !important;
  margin:20px 0 0;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  background-color:#ffffff;
  min-width:300px;
  max-width:500px;
  pointer-events:all; }
  .bp3-toast.bp3-toast-enter, .bp3-toast.bp3-toast-appear{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px); }
  .bp3-toast.bp3-toast-enter-active, .bp3-toast.bp3-toast-appear-active{
    -webkit-transform:translateY(0);
            transform:translateY(0);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-toast.bp3-toast-enter ~ .bp3-toast, .bp3-toast.bp3-toast-appear ~ .bp3-toast{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px); }
  .bp3-toast.bp3-toast-enter-active ~ .bp3-toast, .bp3-toast.bp3-toast-appear-active ~ .bp3-toast{
    -webkit-transform:translateY(0);
            transform:translateY(0);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-toast.bp3-toast-exit{
    opacity:1;
    -webkit-filter:blur(0);
            filter:blur(0); }
  .bp3-toast.bp3-toast-exit-active{
    opacity:0;
    -webkit-filter:blur(10px);
            filter:blur(10px);
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:opacity, filter;
    transition-property:opacity, filter, -webkit-filter;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-toast.bp3-toast-exit ~ .bp3-toast{
    -webkit-transform:translateY(0);
            transform:translateY(0); }
  .bp3-toast.bp3-toast-exit-active ~ .bp3-toast{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:50ms;
            transition-delay:50ms; }
  .bp3-toast .bp3-button-group{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    padding:5px;
    padding-left:0; }
  .bp3-toast > .bp3-icon{
    margin:12px;
    margin-right:0;
    color:#5c7080; }
  .bp3-toast.bp3-dark,
  .bp3-dark .bp3-toast{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
    background-color:#394b59; }
    .bp3-toast.bp3-dark > .bp3-icon,
    .bp3-dark .bp3-toast > .bp3-icon{
      color:#a7b6c2; }
  .bp3-toast[class*="bp3-intent-"] a{
    color:rgba(255, 255, 255, 0.7); }
    .bp3-toast[class*="bp3-intent-"] a:hover{
      color:#ffffff; }
  .bp3-toast[class*="bp3-intent-"] > .bp3-icon{
    color:#ffffff; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button, .bp3-toast[class*="bp3-intent-"] .bp3-button::before,
  .bp3-toast[class*="bp3-intent-"] .bp3-button .bp3-icon, .bp3-toast[class*="bp3-intent-"] .bp3-button:active{
    color:rgba(255, 255, 255, 0.7) !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:focus{
    outline-color:rgba(255, 255, 255, 0.5); }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:hover{
    background-color:rgba(255, 255, 255, 0.15) !important;
    color:#ffffff !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:active{
    background-color:rgba(255, 255, 255, 0.3) !important;
    color:#ffffff !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button::after{
    background:rgba(255, 255, 255, 0.3) !important; }
  .bp3-toast.bp3-intent-primary{
    background-color:#137cbd;
    color:#ffffff; }
  .bp3-toast.bp3-intent-success{
    background-color:#0f9960;
    color:#ffffff; }
  .bp3-toast.bp3-intent-warning{
    background-color:#d9822b;
    color:#ffffff; }
  .bp3-toast.bp3-intent-danger{
    background-color:#db3737;
    color:#ffffff; }

.bp3-toast-message{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  padding:11px;
  word-break:break-word; }

.bp3-toast-container{
  display:-webkit-box !important;
  display:-ms-flexbox !important;
  display:flex !important;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  position:fixed;
  right:0;
  left:0;
  z-index:40;
  overflow:hidden;
  padding:0 20px 20px;
  pointer-events:none; }
  .bp3-toast-container.bp3-toast-container-top{
    top:0;
    bottom:auto; }
  .bp3-toast-container.bp3-toast-container-bottom{
    -webkit-box-orient:vertical;
    -webkit-box-direction:reverse;
        -ms-flex-direction:column-reverse;
            flex-direction:column-reverse;
    top:auto;
    bottom:0; }
  .bp3-toast-container.bp3-toast-container-left{
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start; }
  .bp3-toast-container.bp3-toast-container-right{
    -webkit-box-align:end;
        -ms-flex-align:end;
            align-items:flex-end; }

.bp3-toast-container-bottom .bp3-toast.bp3-toast-enter:not(.bp3-toast-enter-active),
.bp3-toast-container-bottom .bp3-toast.bp3-toast-enter:not(.bp3-toast-enter-active) ~ .bp3-toast, .bp3-toast-container-bottom .bp3-toast.bp3-toast-appear:not(.bp3-toast-appear-active),
.bp3-toast-container-bottom .bp3-toast.bp3-toast-appear:not(.bp3-toast-appear-active) ~ .bp3-toast,
.bp3-toast-container-bottom .bp3-toast.bp3-toast-leave-active ~ .bp3-toast{
  -webkit-transform:translateY(60px);
          transform:translateY(60px); }
.bp3-tooltip{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  -webkit-transform:scale(1);
          transform:scale(1); }
  .bp3-tooltip .bp3-popover-arrow{
    position:absolute;
    width:22px;
    height:22px; }
    .bp3-tooltip .bp3-popover-arrow::before{
      margin:4px;
      width:14px;
      height:14px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip{
    margin-top:-11px;
    margin-bottom:11px; }
    .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow{
      bottom:-8px; }
      .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(-90deg);
                transform:rotate(-90deg); }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip{
    margin-left:11px; }
    .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow{
      left:-8px; }
      .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(0);
                transform:rotate(0); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip{
    margin-top:11px; }
    .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow{
      top:-8px; }
      .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(90deg);
                transform:rotate(90deg); }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip{
    margin-right:11px;
    margin-left:-11px; }
    .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow{
      right:-8px; }
      .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(180deg);
                transform:rotate(180deg); }
  .bp3-tether-element-attached-middle > .bp3-tooltip > .bp3-popover-arrow{
    top:50%;
    -webkit-transform:translateY(-50%);
            transform:translateY(-50%); }
  .bp3-tether-element-attached-center > .bp3-tooltip > .bp3-popover-arrow{
    right:50%;
    -webkit-transform:translateX(50%);
            transform:translateX(50%); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow{
    top:-0.22183px; }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow{
    right:-0.22183px; }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow{
    left:-0.22183px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow{
    bottom:-0.22183px; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:top left;
            transform-origin:top left; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:top center;
            transform-origin:top center; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:top right;
            transform-origin:top right; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:center left;
            transform-origin:center left; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:center center;
            transform-origin:center center; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:center right;
            transform-origin:center right; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:bottom left;
            transform-origin:bottom left; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:bottom center;
            transform-origin:bottom center; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:bottom right;
            transform-origin:bottom right; }
  .bp3-tooltip .bp3-popover-content{
    background:#394b59;
    color:#f5f8fa; }
  .bp3-tooltip .bp3-popover-arrow::before{
    -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2);
            box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2); }
  .bp3-tooltip .bp3-popover-arrow-border{
    fill:#10161a;
    fill-opacity:0.1; }
  .bp3-tooltip .bp3-popover-arrow-fill{
    fill:#394b59; }
  .bp3-popover-enter > .bp3-tooltip, .bp3-popover-appear > .bp3-tooltip{
    -webkit-transform:scale(0.8);
            transform:scale(0.8); }
  .bp3-popover-enter-active > .bp3-tooltip, .bp3-popover-appear-active > .bp3-tooltip{
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-popover-exit > .bp3-tooltip{
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-popover-exit-active > .bp3-tooltip{
    -webkit-transform:scale(0.8);
            transform:scale(0.8);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-tooltip .bp3-popover-content{
    padding:10px 12px; }
  .bp3-tooltip.bp3-dark,
  .bp3-dark .bp3-tooltip{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-tooltip.bp3-dark .bp3-popover-content,
    .bp3-dark .bp3-tooltip .bp3-popover-content{
      background:#e1e8ed;
      color:#394b59; }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow::before,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow::before{
      -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4);
              box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4); }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow-border,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow-border{
      fill:#10161a;
      fill-opacity:0.2; }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow-fill,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow-fill{
      fill:#e1e8ed; }
  .bp3-tooltip.bp3-intent-primary .bp3-popover-content{
    background:#137cbd;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-primary .bp3-popover-arrow-fill{
    fill:#137cbd; }
  .bp3-tooltip.bp3-intent-success .bp3-popover-content{
    background:#0f9960;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-success .bp3-popover-arrow-fill{
    fill:#0f9960; }
  .bp3-tooltip.bp3-intent-warning .bp3-popover-content{
    background:#d9822b;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-warning .bp3-popover-arrow-fill{
    fill:#d9822b; }
  .bp3-tooltip.bp3-intent-danger .bp3-popover-content{
    background:#db3737;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-danger .bp3-popover-arrow-fill{
    fill:#db3737; }

.bp3-tooltip-indicator{
  border-bottom:dotted 1px;
  cursor:help; }
.bp3-tree .bp3-icon, .bp3-tree .bp3-icon-standard, .bp3-tree .bp3-icon-large{
  color:#5c7080; }
  .bp3-tree .bp3-icon.bp3-intent-primary, .bp3-tree .bp3-icon-standard.bp3-intent-primary, .bp3-tree .bp3-icon-large.bp3-intent-primary{
    color:#137cbd; }
  .bp3-tree .bp3-icon.bp3-intent-success, .bp3-tree .bp3-icon-standard.bp3-intent-success, .bp3-tree .bp3-icon-large.bp3-intent-success{
    color:#0f9960; }
  .bp3-tree .bp3-icon.bp3-intent-warning, .bp3-tree .bp3-icon-standard.bp3-intent-warning, .bp3-tree .bp3-icon-large.bp3-intent-warning{
    color:#d9822b; }
  .bp3-tree .bp3-icon.bp3-intent-danger, .bp3-tree .bp3-icon-standard.bp3-intent-danger, .bp3-tree .bp3-icon-large.bp3-intent-danger{
    color:#db3737; }

.bp3-tree-node-list{
  margin:0;
  padding-left:0;
  list-style:none; }

.bp3-tree-root{
  position:relative;
  background-color:transparent;
  cursor:default;
  padding-left:0; }

.bp3-tree-node-content-0{
  padding-left:0px; }

.bp3-tree-node-content-1{
  padding-left:23px; }

.bp3-tree-node-content-2{
  padding-left:46px; }

.bp3-tree-node-content-3{
  padding-left:69px; }

.bp3-tree-node-content-4{
  padding-left:92px; }

.bp3-tree-node-content-5{
  padding-left:115px; }

.bp3-tree-node-content-6{
  padding-left:138px; }

.bp3-tree-node-content-7{
  padding-left:161px; }

.bp3-tree-node-content-8{
  padding-left:184px; }

.bp3-tree-node-content-9{
  padding-left:207px; }

.bp3-tree-node-content-10{
  padding-left:230px; }

.bp3-tree-node-content-11{
  padding-left:253px; }

.bp3-tree-node-content-12{
  padding-left:276px; }

.bp3-tree-node-content-13{
  padding-left:299px; }

.bp3-tree-node-content-14{
  padding-left:322px; }

.bp3-tree-node-content-15{
  padding-left:345px; }

.bp3-tree-node-content-16{
  padding-left:368px; }

.bp3-tree-node-content-17{
  padding-left:391px; }

.bp3-tree-node-content-18{
  padding-left:414px; }

.bp3-tree-node-content-19{
  padding-left:437px; }

.bp3-tree-node-content-20{
  padding-left:460px; }

.bp3-tree-node-content{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  width:100%;
  height:30px;
  padding-right:5px; }
  .bp3-tree-node-content:hover{
    background-color:rgba(191, 204, 214, 0.4); }

.bp3-tree-node-caret,
.bp3-tree-node-caret-none{
  min-width:30px; }

.bp3-tree-node-caret{
  color:#5c7080;
  -webkit-transform:rotate(0deg);
          transform:rotate(0deg);
  cursor:pointer;
  padding:7px;
  -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-tree-node-caret:hover{
    color:#182026; }
  .bp3-dark .bp3-tree-node-caret{
    color:#a7b6c2; }
    .bp3-dark .bp3-tree-node-caret:hover{
      color:#f5f8fa; }
  .bp3-tree-node-caret.bp3-tree-node-caret-open{
    -webkit-transform:rotate(90deg);
            transform:rotate(90deg); }
  .bp3-tree-node-caret.bp3-icon-standard::before{
    content:""; }

.bp3-tree-node-icon{
  position:relative;
  margin-right:7px; }

.bp3-tree-node-label{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  position:relative;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-tree-node-label span{
    display:inline; }

.bp3-tree-node-secondary-label{
  padding:0 5px;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-tree-node-secondary-label .bp3-popover-wrapper,
  .bp3-tree-node-secondary-label .bp3-popover-target{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center; }

.bp3-tree-node.bp3-disabled .bp3-tree-node-content{
  background-color:inherit;
  cursor:not-allowed;
  color:rgba(92, 112, 128, 0.6); }

.bp3-tree-node.bp3-disabled .bp3-tree-node-caret,
.bp3-tree-node.bp3-disabled .bp3-tree-node-icon{
  cursor:not-allowed;
  color:rgba(92, 112, 128, 0.6); }

.bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content{
  background-color:#137cbd; }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content,
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon, .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon-standard, .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon-large{
    color:#ffffff; }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-tree-node-caret::before{
    color:rgba(255, 255, 255, 0.7); }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-tree-node-caret:hover::before{
    color:#ffffff; }

.bp3-dark .bp3-tree-node-content:hover{
  background-color:rgba(92, 112, 128, 0.3); }

.bp3-dark .bp3-tree .bp3-icon, .bp3-dark .bp3-tree .bp3-icon-standard, .bp3-dark .bp3-tree .bp3-icon-large{
  color:#a7b6c2; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-primary, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-primary, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-primary{
    color:#137cbd; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-success, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-success, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-success{
    color:#0f9960; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-warning, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-warning, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-warning{
    color:#d9822b; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-danger, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-danger, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-danger{
    color:#db3737; }

.bp3-dark .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content{
  background-color:#137cbd; }
/*!

Copyright 2017-present Palantir Technologies, Inc. All rights reserved.
Licensed under the Apache License, Version 2.0.

*/
.bp3-omnibar{
  -webkit-filter:blur(0);
          filter:blur(0);
  opacity:1;
  top:20vh;
  left:calc(50% - 250px);
  z-index:21;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  background-color:#ffffff;
  width:500px; }
  .bp3-omnibar.bp3-overlay-enter, .bp3-omnibar.bp3-overlay-appear{
    -webkit-filter:blur(20px);
            filter:blur(20px);
    opacity:0.2; }
  .bp3-omnibar.bp3-overlay-enter-active, .bp3-omnibar.bp3-overlay-appear-active{
    -webkit-filter:blur(0);
            filter:blur(0);
    opacity:1;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:filter, opacity;
    transition-property:filter, opacity, -webkit-filter;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-omnibar.bp3-overlay-exit{
    -webkit-filter:blur(0);
            filter:blur(0);
    opacity:1; }
  .bp3-omnibar.bp3-overlay-exit-active{
    -webkit-filter:blur(20px);
            filter:blur(20px);
    opacity:0.2;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:filter, opacity;
    transition-property:filter, opacity, -webkit-filter;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-omnibar .bp3-input{
    border-radius:0;
    background-color:transparent; }
    .bp3-omnibar .bp3-input, .bp3-omnibar .bp3-input:focus{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-omnibar .bp3-menu{
    border-radius:0;
    -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
    background-color:transparent;
    max-height:calc(60vh - 40px);
    overflow:auto; }
    .bp3-omnibar .bp3-menu:empty{
      display:none; }
  .bp3-dark .bp3-omnibar, .bp3-omnibar.bp3-dark{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    background-color:#30404d; }

.bp3-omnibar-overlay .bp3-overlay-backdrop{
  background-color:rgba(16, 22, 26, 0.2); }

.bp3-select-popover .bp3-popover-content{
  padding:5px; }

.bp3-select-popover .bp3-input-group{
  margin-bottom:0; }

.bp3-select-popover .bp3-menu{
  max-width:400px;
  max-height:300px;
  overflow:auto;
  padding:0; }
  .bp3-select-popover .bp3-menu:not(:first-child){
    padding-top:5px; }

.bp3-multi-select{
  min-width:150px; }

.bp3-multi-select-popover .bp3-menu{
  max-width:400px;
  max-height:300px;
  overflow:auto; }

.bp3-select-popover .bp3-popover-content{
  padding:5px; }

.bp3-select-popover .bp3-input-group{
  margin-bottom:0; }

.bp3-select-popover .bp3-menu{
  max-width:400px;
  max-height:300px;
  overflow:auto;
  padding:0; }
  .bp3-select-popover .bp3-menu:not(:first-child){
    padding-top:5px; }
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensureUiComponents() in @jupyterlab/buildutils */

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

/* Icons urls */

:root {
  --jp-icon-add: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDEzaC02djZoLTJ2LTZINXYtMmg2VjVoMnY2aDZ2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-bug: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwIDhoLTIuODFjLS40NS0uNzgtMS4wNy0xLjQ1LTEuODItMS45NkwxNyA0LjQxIDE1LjU5IDNsLTIuMTcgMi4xN0MxMi45NiA1LjA2IDEyLjQ5IDUgMTIgNWMtLjQ5IDAtLjk2LjA2LTEuNDEuMTdMOC40MSAzIDcgNC40MWwxLjYyIDEuNjNDNy44OCA2LjU1IDcuMjYgNy4yMiA2LjgxIDhINHYyaDIuMDljLS4wNS4zMy0uMDkuNjYtLjA5IDF2MUg0djJoMnYxYzAgLjM0LjA0LjY3LjA5IDFINHYyaDIuODFjMS4wNCAxLjc5IDIuOTcgMyA1LjE5IDNzNC4xNS0xLjIxIDUuMTktM0gyMHYtMmgtMi4wOWMuMDUtLjMzLjA5LS42Ni4wOS0xdi0xaDJ2LTJoLTJ2LTFjMC0uMzQtLjA0LS42Ny0uMDktMUgyMFY4em0tNiA4aC00di0yaDR2MnptMC00aC00di0yaDR2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-build: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTYiIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE0LjkgMTcuNDVDMTYuMjUgMTcuNDUgMTcuMzUgMTYuMzUgMTcuMzUgMTVDMTcuMzUgMTMuNjUgMTYuMjUgMTIuNTUgMTQuOSAxMi41NUMxMy41NCAxMi41NSAxMi40NSAxMy42NSAxMi40NSAxNUMxMi40NSAxNi4zNSAxMy41NCAxNy40NSAxNC45IDE3LjQ1Wk0yMC4xIDE1LjY4TDIxLjU4IDE2Ljg0QzIxLjcxIDE2Ljk1IDIxLjc1IDE3LjEzIDIxLjY2IDE3LjI5TDIwLjI2IDE5LjcxQzIwLjE3IDE5Ljg2IDIwIDE5LjkyIDE5LjgzIDE5Ljg2TDE4LjA5IDE5LjE2QzE3LjczIDE5LjQ0IDE3LjMzIDE5LjY3IDE2LjkxIDE5Ljg1TDE2LjY0IDIxLjdDMTYuNjIgMjEuODcgMTYuNDcgMjIgMTYuMyAyMkgxMy41QzEzLjMyIDIyIDEzLjE4IDIxLjg3IDEzLjE1IDIxLjdMMTIuODkgMTkuODVDMTIuNDYgMTkuNjcgMTIuMDcgMTkuNDQgMTEuNzEgMTkuMTZMOS45NjAwMiAxOS44NkM5LjgxMDAyIDE5LjkyIDkuNjIwMDIgMTkuODYgOS41NDAwMiAxOS43MUw4LjE0MDAyIDE3LjI5QzguMDUwMDIgMTcuMTMgOC4wOTAwMiAxNi45NSA4LjIyMDAyIDE2Ljg0TDkuNzAwMDIgMTUuNjhMOS42NTAwMSAxNUw5LjcwMDAyIDE0LjMxTDguMjIwMDIgMTMuMTZDOC4wOTAwMiAxMy4wNSA4LjA1MDAyIDEyLjg2IDguMTQwMDIgMTIuNzFMOS41NDAwMiAxMC4yOUM5LjYyMDAyIDEwLjEzIDkuODEwMDIgMTAuMDcgOS45NjAwMiAxMC4xM0wxMS43MSAxMC44NEMxMi4wNyAxMC41NiAxMi40NiAxMC4zMiAxMi44OSAxMC4xNUwxMy4xNSA4LjI4OTk4QzEzLjE4IDguMTI5OTggMTMuMzIgNy45OTk5OCAxMy41IDcuOTk5OThIMTYuM0MxNi40NyA3Ljk5OTk4IDE2LjYyIDguMTI5OTggMTYuNjQgOC4yODk5OEwxNi45MSAxMC4xNUMxNy4zMyAxMC4zMiAxNy43MyAxMC41NiAxOC4wOSAxMC44NEwxOS44MyAxMC4xM0MyMCAxMC4wNyAyMC4xNyAxMC4xMyAyMC4yNiAxMC4yOUwyMS42NiAxMi43MUMyMS43NSAxMi44NiAyMS43MSAxMy4wNSAyMS41OCAxMy4xNkwyMC4xIDE0LjMxTDIwLjE1IDE1TDIwLjEgMTUuNjhaIi8+CiAgICA8cGF0aCBkPSJNNy4zMjk2NiA3LjQ0NDU0QzguMDgzMSA3LjAwOTU0IDguMzM5MzIgNi4wNTMzMiA3LjkwNDMyIDUuMjk5ODhDNy40NjkzMiA0LjU0NjQzIDYuNTA4MSA0LjI4MTU2IDUuNzU0NjYgNC43MTY1NkM1LjM5MTc2IDQuOTI2MDggNS4xMjY5NSA1LjI3MTE4IDUuMDE4NDkgNS42NzU5NEM0LjkxMDA0IDYuMDgwNzEgNC45NjY4MiA2LjUxMTk4IDUuMTc2MzQgNi44NzQ4OEM1LjYxMTM0IDcuNjI4MzIgNi41NzYyMiA3Ljg3OTU0IDcuMzI5NjYgNy40NDQ1NFpNOS42NTcxOCA0Ljc5NTkzTDEwLjg2NzIgNC45NTE3OUMxMC45NjI4IDQuOTc3NDEgMTEuMDQwMiA1LjA3MTMzIDExLjAzODIgNS4xODc5M0wxMS4wMzg4IDYuOTg4OTNDMTEuMDQ1NSA3LjEwMDU0IDEwLjk2MTYgNy4xOTUxOCAxMC44NTUgNy4yMTA1NEw5LjY2MDAxIDcuMzgwODNMOS4yMzkxNSA4LjEzMTg4TDkuNjY5NjEgOS4yNTc0NUM5LjcwNzI5IDkuMzYyNzEgOS42NjkzNCA5LjQ3Njk5IDkuNTc0MDggOS41MzE5OUw4LjAxNTIzIDEwLjQzMkM3LjkxMTMxIDEwLjQ5MiA3Ljc5MzM3IDEwLjQ2NzcgNy43MjEwNSAxMC4zODI0TDYuOTg3NDggOS40MzE4OEw2LjEwOTMxIDkuNDMwODNMNS4zNDcwNCAxMC4zOTA1QzUuMjg5MDkgMTAuNDcwMiA1LjE3MzgzIDEwLjQ5MDUgNS4wNzE4NyAxMC40MzM5TDMuNTEyNDUgOS41MzI5M0MzLjQxMDQ5IDkuNDc2MzMgMy4zNzY0NyA5LjM1NzQxIDMuNDEwNzUgOS4yNTY3OUwzLjg2MzQ3IDguMTQwOTNMMy42MTc0OSA3Ljc3NDg4TDMuNDIzNDcgNy4zNzg4M0wyLjIzMDc1IDcuMjEyOTdDMi4xMjY0NyA3LjE5MjM1IDIuMDQwNDkgNy4xMDM0MiAyLjA0MjQ1IDYuOTg2ODJMMi4wNDE4NyA1LjE4NTgyQzIuMDQzODMgNS4wNjkyMiAyLjExOTA5IDQuOTc5NTggMi4yMTcwNCA0Ljk2OTIyTDMuNDIwNjUgNC43OTM5M0wzLjg2NzQ5IDQuMDI3ODhMMy40MTEwNSAyLjkxNzMxQzMuMzczMzcgMi44MTIwNCAzLjQxMTMxIDIuNjk3NzYgMy41MTUyMyAyLjYzNzc2TDUuMDc0MDggMS43Mzc3NkM1LjE2OTM0IDEuNjgyNzYgNS4yODcyOSAxLjcwNzA0IDUuMzU5NjEgMS43OTIzMUw2LjExOTE1IDIuNzI3ODhMNi45ODAwMSAyLjczODkzTDcuNzI0OTYgMS43ODkyMkM3Ljc5MTU2IDEuNzA0NTggNy45MTU0OCAxLjY3OTIyIDguMDA4NzkgMS43NDA4Mkw5LjU2ODIxIDIuNjQxODJDOS42NzAxNyAyLjY5ODQyIDkuNzEyODUgMi44MTIzNCA5LjY4NzIzIDIuOTA3OTdMOS4yMTcxOCA0LjAzMzgzTDkuNDYzMTYgNC4zOTk4OEw5LjY1NzE4IDQuNzk1OTNaIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iOS45LDEzLjYgMy42LDcuNCA0LjQsNi42IDkuOSwxMi4yIDE1LjQsNi43IDE2LjEsNy40ICIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNS45TDksOS43bDMuOC0zLjhsMS4yLDEuMmwtNC45LDVsLTQuOS01TDUuMiw1Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNy41TDksMTEuMmwzLjgtMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-left: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik0xMC44LDEyLjhMNy4xLDlsMy44LTMuOGwwLDcuNkgxMC44eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-right: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik03LjIsNS4yTDEwLjksOWwtMy44LDMuOFY1LjJINy4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-up-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iMTUuNCwxMy4zIDkuOSw3LjcgNC40LDEzLjIgMy42LDEyLjUgOS45LDYuMyAxNi4xLDEyLjYgIi8+Cgk8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-up: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik01LjIsMTAuNUw5LDYuOGwzLjgsMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-case-sensitive: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgogIDxnIGNsYXNzPSJqcC1pY29uLWFjY2VudDIiIGZpbGw9IiNGRkYiPgogICAgPHBhdGggZD0iTTcuNiw4aDAuOWwzLjUsOGgtMS4xTDEwLDE0SDZsLTAuOSwySDRMNy42LDh6IE04LDkuMUw2LjQsMTNoMy4yTDgsOS4xeiIvPgogICAgPHBhdGggZD0iTTE2LjYsOS44Yy0wLjIsMC4xLTAuNCwwLjEtMC43LDAuMWMtMC4yLDAtMC40LTAuMS0wLjYtMC4yYy0wLjEtMC4xLTAuMi0wLjQtMC4yLTAuNyBjLTAuMywwLjMtMC42LDAuNS0wLjksMC43Yy0wLjMsMC4xLTAuNywwLjItMS4xLDAuMmMtMC4zLDAtMC41LDAtMC43LTAuMWMtMC4yLTAuMS0wLjQtMC4yLTAuNi0wLjNjLTAuMi0wLjEtMC4zLTAuMy0wLjQtMC41IGMtMC4xLTAuMi0wLjEtMC40LTAuMS0wLjdjMC0wLjMsMC4xLTAuNiwwLjItMC44YzAuMS0wLjIsMC4zLTAuNCwwLjQtMC41QzEyLDcsMTIuMiw2LjksMTIuNSw2LjhjMC4yLTAuMSwwLjUtMC4xLDAuNy0wLjIgYzAuMy0wLjEsMC41LTAuMSwwLjctMC4xYzAuMiwwLDAuNC0wLjEsMC42LTAuMWMwLjIsMCwwLjMtMC4xLDAuNC0wLjJjMC4xLTAuMSwwLjItMC4yLDAuMi0wLjRjMC0xLTEuMS0xLTEuMy0xIGMtMC40LDAtMS40LDAtMS40LDEuMmgtMC45YzAtMC40LDAuMS0wLjcsMC4yLTFjMC4xLTAuMiwwLjMtMC40LDAuNS0wLjZjMC4yLTAuMiwwLjUtMC4zLDAuOC0wLjNDMTMuMyw0LDEzLjYsNCwxMy45LDQgYzAuMywwLDAuNSwwLDAuOCwwLjFjMC4zLDAsMC41LDAuMSwwLjcsMC4yYzAuMiwwLjEsMC40LDAuMywwLjUsMC41QzE2LDUsMTYsNS4yLDE2LDUuNnYyLjljMCwwLjIsMCwwLjQsMCwwLjUgYzAsMC4xLDAuMSwwLjIsMC4zLDAuMmMwLjEsMCwwLjIsMCwwLjMsMFY5Ljh6IE0xNS4yLDYuOWMtMS4yLDAuNi0zLjEsMC4yLTMuMSwxLjRjMCwxLjQsMy4xLDEsMy4xLTAuNVY2Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-check: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkgMTYuMTdMNC44MyAxMmwtMS40MiAxLjQxTDkgMTkgMjEgN2wtMS40MS0xLjQxeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-circle-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyIDJDNi40NyAyIDIgNi40NyAyIDEyczQuNDcgMTAgMTAgMTAgMTAtNC40NyAxMC0xMFMxNy41MyAyIDEyIDJ6bTAgMThjLTQuNDEgMC04LTMuNTktOC04czMuNTktOCA4LTggOCAzLjU5IDggOC0zLjU5IDgtOCA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-circle: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iOSIgY3k9IjkiIHI9IjgiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-clear: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8bWFzayBpZD0iZG9udXRIb2xlIj4KICAgIDxyZWN0IHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgZmlsbD0id2hpdGUiIC8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSI4IiBmaWxsPSJibGFjayIvPgogIDwvbWFzaz4KCiAgPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxyZWN0IGhlaWdodD0iMTgiIHdpZHRoPSIyIiB4PSIxMSIgeT0iMyIgdHJhbnNmb3JtPSJyb3RhdGUoMzE1LCAxMiwgMTIpIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIxMCIgbWFzaz0idXJsKCNkb251dEhvbGUpIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-close: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1ub25lIGpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIGpwLWljb24zLWhvdmVyIiBmaWxsPSJub25lIj4KICAgIDxjaXJjbGUgY3g9IjEyIiBjeT0iMTIiIHI9IjExIi8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIGpwLWljb24tYWNjZW50Mi1ob3ZlciIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMTkgNi40MUwxNy41OSA1IDEyIDEwLjU5IDYuNDEgNSA1IDYuNDEgMTAuNTkgMTIgNSAxNy41OSA2LjQxIDE5IDEyIDEzLjQxIDE3LjU5IDE5IDE5IDE3LjU5IDEzLjQxIDEyeiIvPgogIDwvZz4KCiAgPGcgY2xhc3M9ImpwLWljb24tbm9uZSBqcC1pY29uLWJ1c3kiIGZpbGw9Im5vbmUiPgogICAgPGNpcmNsZSBjeD0iMTIiIGN5PSIxMiIgcj0iNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-console: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwMCAyMDAiPgogIDxnIGNsYXNzPSJqcC1pY29uLWJyYW5kMSBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMjg4RDEiPgogICAgPHBhdGggZD0iTTIwIDE5LjhoMTYwdjE1OS45SDIweiIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNmZmYiPgogICAgPHBhdGggZD0iTTEwNSAxMjcuM2g0MHYxMi44aC00MHpNNTEuMSA3N0w3NCA5OS45bC0yMy4zIDIzLjMgMTAuNSAxMC41IDIzLjMtMjMuM0w5NSA5OS45IDg0LjUgODkuNCA2MS42IDY2LjV6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-copy: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTExLjksMUgzLjJDMi40LDEsMS43LDEuNywxLjcsMi41djEwLjJoMS41VjIuNWg4LjdWMXogTTE0LjEsMy45aC04Yy0wLjgsMC0xLjUsMC43LTEuNSwxLjV2MTAuMmMwLDAuOCwwLjcsMS41LDEuNSwxLjVoOCBjMC44LDAsMS41LTAuNywxLjUtMS41VjUuNEMxNS41LDQuNiwxNC45LDMuOSwxNC4xLDMuOXogTTE0LjEsMTUuNWgtOFY1LjRoOFYxNS41eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-cut: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkuNjQgNy42NGMuMjMtLjUuMzYtMS4wNS4zNi0xLjY0IDAtMi4yMS0xLjc5LTQtNC00UzIgMy43OSAyIDZzMS43OSA0IDQgNGMuNTkgMCAxLjE0LS4xMyAxLjY0LS4zNkwxMCAxMmwtMi4zNiAyLjM2QzcuMTQgMTQuMTMgNi41OSAxNCA2IDE0Yy0yLjIxIDAtNCAxLjc5LTQgNHMxLjc5IDQgNCA0IDQtMS43OSA0LTRjMC0uNTktLjEzLTEuMTQtLjM2LTEuNjRMMTIgMTRsNyA3aDN2LTFMOS42NCA3LjY0ek02IDhjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTAgMTJjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTYtNy41Yy0uMjggMC0uNS0uMjItLjUtLjVzLjIyLS41LjUtLjUuNS4yMi41LjUtLjIyLjUtLjUuNXpNMTkgM2wtNiA2IDIgMiA3LTdWM3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-download: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDloLTRWM0g5djZINWw3IDcgNy03ek01IDE4djJoMTR2LTJINXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-edit: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMgMTcuMjVWMjFoMy43NUwxNy44MSA5Ljk0bC0zLjc1LTMuNzVMMyAxNy4yNXpNMjAuNzEgNy4wNGMuMzktLjM5LjM5LTEuMDIgMC0xLjQxbC0yLjM0LTIuMzRjLS4zOS0uMzktMS4wMi0uMzktMS40MSAwbC0xLjgzIDEuODMgMy43NSAzLjc1IDEuODMtMS44M3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-ellipses: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iNSIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxOSIgY3k9IjEyIiByPSIyIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-extension: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwLjUgMTFIMTlWN2MwLTEuMS0uOS0yLTItMmgtNFYzLjVDMTMgMi4xMiAxMS44OCAxIDEwLjUgMVM4IDIuMTIgOCAzLjVWNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAydjMuOEgzLjVjMS40OSAwIDIuNyAxLjIxIDIuNyAyLjdzLTEuMjEgMi43LTIuNyAyLjdIMlYyMGMwIDEuMS45IDIgMiAyaDMuOHYtMS41YzAtMS40OSAxLjIxLTIuNyAyLjctMi43IDEuNDkgMCAyLjcgMS4yMSAyLjcgMi43VjIySDE3YzEuMSAwIDItLjkgMi0ydi00aDEuNWMxLjM4IDAgMi41LTEuMTIgMi41LTIuNVMyMS44OCAxMSAyMC41IDExeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-fast-forward: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTQgMThsOC41LTZMNCA2djEyem05LTEydjEybDguNS02TDEzIDZ6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-file-upload: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkgMTZoNnYtNmg0bC03LTctNyA3aDR6bS00IDJoMTR2Mkg1eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-file: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuMyA4LjJsLTUuNS01LjVjLS4zLS4zLS43LS41LTEuMi0uNUgzLjljLS44LjEtMS42LjktMS42IDEuOHYxNC4xYzAgLjkuNyAxLjYgMS42IDEuNmgxNC4yYy45IDAgMS42LS43IDEuNi0xLjZWOS40Yy4xLS41LS4xLS45LS40LTEuMnptLTUuOC0zLjNsMy40IDMuNmgtMy40VjQuOXptMy45IDEyLjdINC43Yy0uMSAwLS4yIDAtLjItLjJWNC43YzAtLjIuMS0uMy4yLS4zaDcuMnY0LjRzMCAuOC4zIDEuMWMuMy4zIDEuMS4zIDEuMS4zaDQuM3Y3LjJzLS4xLjItLjIuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-filter-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEwIDE4aDR2LTJoLTR2MnpNMyA2djJoMThWNkgzem0zIDdoMTJ2LTJINnYyeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY4YzAtMS4xLS45LTItMi0yaC04bC0yLTJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-html5: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMDAiIGQ9Ik0xMDguNCAwaDIzdjIyLjhoMjEuMlYwaDIzdjY5aC0yM1Y0NmgtMjF2MjNoLTIzLjJNMjA2IDIzaC0yMC4zVjBoNjMuN3YyM0gyMjl2NDZoLTIzbTUzLjUtNjloMjQuMWwxNC44IDI0LjNMMzEzLjIgMGgyNC4xdjY5aC0yM1YzNC44bC0xNi4xIDI0LjgtMTYuMS0yNC44VjY5aC0yMi42bTg5LjItNjloMjN2NDYuMmgzMi42VjY5aC01NS42Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI2U0NGQyNiIgZD0iTTEwNy42IDQ3MWwtMzMtMzcwLjRoMzYyLjhsLTMzIDM3MC4yTDI1NS43IDUxMiIvPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNmMTY1MjkiIGQ9Ik0yNTYgNDgwLjVWMTMxaDE0OC4zTDM3NiA0NDciLz4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNlYmViZWIiIGQ9Ik0xNDIgMTc2LjNoMTE0djQ1LjRoLTY0LjJsNC4yIDQ2LjVoNjB2NDUuM0gxNTQuNG0yIDIyLjhIMjAybDMuMiAzNi4zIDUwLjggMTMuNnY0Ny40bC05My4yLTI2Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIiBmaWxsPSIjZmZmIiBkPSJNMzY5LjYgMTc2LjNIMjU1Ljh2NDUuNGgxMDkuNm0tNC4xIDQ2LjVIMjU1Ljh2NDUuNGg1NmwtNS4zIDU5LTUwLjcgMTMuNnY0Ny4ybDkzLTI1LjgiLz4KPC9zdmc+Cg==);
  --jp-icon-image: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1icmFuZDQganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNGRkYiIGQ9Ik0yLjIgMi4yaDE3LjV2MTcuNUgyLjJ6Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzNGNTFCNSIgZD0iTTIuMiAyLjJ2MTcuNWgxNy41bC4xLTE3LjVIMi4yem0xMi4xIDIuMmMxLjIgMCAyLjIgMSAyLjIgMi4ycy0xIDIuMi0yLjIgMi4yLTIuMi0xLTIuMi0yLjIgMS0yLjIgMi4yLTIuMnpNNC40IDE3LjZsMy4zLTguOCAzLjMgNi42IDIuMi0zLjIgNC40IDUuNEg0LjR6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-inspector: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY2YzAtMS4xLS45LTItMi0yem0tNSAxNEg0di00aDExdjR6bTAtNUg0VjloMTF2NHptNSA1aC00VjloNHY5eiIvPgo8L3N2Zz4K);
  --jp-icon-json: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMSBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNGOUE4MjUiPgogICAgPHBhdGggZD0iTTIwLjIgMTEuOGMtMS42IDAtMS43LjUtMS43IDEgMCAuNC4xLjkuMSAxLjMuMS41LjEuOS4xIDEuMyAwIDEuNy0xLjQgMi4zLTMuNSAyLjNoLS45di0xLjloLjVjMS4xIDAgMS40IDAgMS40LS44IDAtLjMgMC0uNi0uMS0xIDAtLjQtLjEtLjgtLjEtMS4yIDAtMS4zIDAtMS44IDEuMy0yLTEuMy0uMi0xLjMtLjctMS4zLTIgMC0uNC4xLS44LjEtMS4yLjEtLjQuMS0uNy4xLTEgMC0uOC0uNC0uNy0xLjQtLjhoLS41VjQuMWguOWMyLjIgMCAzLjUuNyAzLjUgMi4zIDAgLjQtLjEuOS0uMSAxLjMtLjEuNS0uMS45LS4xIDEuMyAwIC41LjIgMSAxLjcgMXYxLjh6TTEuOCAxMC4xYzEuNiAwIDEuNy0uNSAxLjctMSAwLS40LS4xLS45LS4xLTEuMy0uMS0uNS0uMS0uOS0uMS0xLjMgMC0xLjYgMS40LTIuMyAzLjUtMi4zaC45djEuOWgtLjVjLTEgMC0xLjQgMC0xLjQuOCAwIC4zIDAgLjYuMSAxIDAgLjIuMS42LjEgMSAwIDEuMyAwIDEuOC0xLjMgMkM2IDExLjIgNiAxMS43IDYgMTNjMCAuNC0uMS44LS4xIDEuMi0uMS4zLS4xLjctLjEgMSAwIC44LjMuOCAxLjQuOGguNXYxLjloLS45Yy0yLjEgMC0zLjUtLjYtMy41LTIuMyAwLS40LjEtLjkuMS0xLjMuMS0uNS4xLS45LjEtMS4zIDAtLjUtLjItMS0xLjctMXYtMS45eiIvPgogICAgPGNpcmNsZSBjeD0iMTEiIGN5PSIxMy44IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY3g9IjExIiBjeT0iOC4yIiByPSIyLjEiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-jupyter-favicon: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTUyIiBoZWlnaHQ9IjE2NSIgdmlld0JveD0iMCAwIDE1MiAxNjUiIHZlcnNpb249IjEuMSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA3ODk0NywgMTEwLjU4MjkyNykiIGQ9Ik03NS45NDIyODQyLDI5LjU4MDQ1NjEgQzQzLjMwMjM5NDcsMjkuNTgwNDU2MSAxNC43OTY3ODMyLDE3LjY1MzQ2MzQgMCwwIEM1LjUxMDgzMjExLDE1Ljg0MDY4MjkgMTUuNzgxNTM4OSwyOS41NjY3NzMyIDI5LjM5MDQ5NDcsMzkuMjc4NDE3MSBDNDIuOTk5Nyw0OC45ODk4NTM3IDU5LjI3MzcsNTQuMjA2NzgwNSA3NS45NjA1Nzg5LDU0LjIwNjc4MDUgQzkyLjY0NzQ1NzksNTQuMjA2NzgwNSAxMDguOTIxNDU4LDQ4Ljk4OTg1MzcgMTIyLjUzMDY2MywzOS4yNzg0MTcxIEMxMzYuMTM5NDUzLDI5LjU2Njc3MzIgMTQ2LjQxMDI4NCwxNS44NDA2ODI5IDE1MS45MjExNTgsMCBDMTM3LjA4Nzg2OCwxNy42NTM0NjM0IDEwOC41ODI1ODksMjkuNTgwNDU2MSA3NS45NDIyODQyLDI5LjU4MDQ1NjEgTDc1Ljk0MjI4NDIsMjkuNTgwNDU2MSBaIiAvPgogICAgPHBhdGggdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMzczNjgsIDAuNzA0ODc4KSIgZD0iTTc1Ljk3ODQ1NzksMjQuNjI2NDA3MyBDMTA4LjYxODc2MywyNC42MjY0MDczIDEzNy4xMjQ0NTgsMzYuNTUzNDQxNSAxNTEuOTIxMTU4LDU0LjIwNjc4MDUgQzE0Ni40MTAyODQsMzguMzY2MjIyIDEzNi4xMzk0NTMsMjQuNjQwMTMxNyAxMjIuNTMwNjYzLDE0LjkyODQ4NzggQzEwOC45MjE0NTgsNS4yMTY4NDM5IDkyLjY0NzQ1NzksMCA3NS45NjA1Nzg5LDAgQzU5LjI3MzcsMCA0Mi45OTk3LDUuMjE2ODQzOSAyOS4zOTA0OTQ3LDE0LjkyODQ4NzggQzE1Ljc4MTUzODksMjQuNjQwMTMxNyA1LjUxMDgzMjExLDM4LjM2NjIyMiAwLDU0LjIwNjc4MDUgQzE0LjgzMzA4MTYsMzYuNTg5OTI5MyA0My4zMzg1Njg0LDI0LjYyNjQwNzMgNzUuOTc4NDU3OSwyNC42MjY0MDczIEw3NS45Nzg0NTc5LDI0LjYyNjQwNzMgWiIgLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-jupyter: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzkiIGhlaWdodD0iNTEiIHZpZXdCb3g9IjAgMCAzOSA1MSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMTYzOCAtMjI4MSkiPgogICAgPGcgY2xhc3M9ImpwLWljb24td2FybjAiIGZpbGw9IiNGMzc3MjYiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5Ljc0IDIzMTEuOTgpIiBkPSJNIDE4LjI2NDYgNy4xMzQxMUMgMTAuNDE0NSA3LjEzNDExIDMuNTU4NzIgNC4yNTc2IDAgMEMgMS4zMjUzOSAzLjgyMDQgMy43OTU1NiA3LjEzMDgxIDcuMDY4NiA5LjQ3MzAzQyAxMC4zNDE3IDExLjgxNTIgMTQuMjU1NyAxMy4wNzM0IDE4LjI2OSAxMy4wNzM0QyAyMi4yODIzIDEzLjA3MzQgMjYuMTk2MyAxMS44MTUyIDI5LjQ2OTQgOS40NzMwM0MgMzIuNzQyNCA3LjEzMDgxIDM1LjIxMjYgMy44MjA0IDM2LjUzOCAwQyAzMi45NzA1IDQuMjU3NiAyNi4xMTQ4IDcuMTM0MTEgMTguMjY0NiA3LjEzNDExWiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5LjczIDIyODUuNDgpIiBkPSJNIDE4LjI3MzMgNS45MzkzMUMgMjYuMTIzNSA1LjkzOTMxIDMyLjk3OTMgOC44MTU4MyAzNi41MzggMTMuMDczNEMgMzUuMjEyNiA5LjI1MzAzIDMyLjc0MjQgNS45NDI2MiAyOS40Njk0IDMuNjAwNEMgMjYuMTk2MyAxLjI1ODE4IDIyLjI4MjMgMCAxOC4yNjkgMEMgMTQuMjU1NyAwIDEwLjM0MTcgMS4yNTgxOCA3LjA2ODYgMy42MDA0QyAzLjc5NTU2IDUuOTQyNjIgMS4zMjUzOSA5LjI1MzAzIDAgMTMuMDczNEMgMy41Njc0NSA4LjgyNDYzIDEwLjQyMzIgNS45MzkzMSAxOC4yNzMzIDUuOTM5MzFaIi8+CiAgICA8L2c+CiAgICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjY5LjMgMjI4MS4zMSkiIGQ9Ik0gNS44OTM1MyAyLjg0NEMgNS45MTg4OSAzLjQzMTY1IDUuNzcwODUgNC4wMTM2NyA1LjQ2ODE1IDQuNTE2NDVDIDUuMTY1NDUgNS4wMTkyMiA0LjcyMTY4IDUuNDIwMTUgNC4xOTI5OSA1LjY2ODUxQyAzLjY2NDMgNS45MTY4OCAzLjA3NDQ0IDYuMDAxNTEgMi40OTgwNSA1LjkxMTcxQyAxLjkyMTY2IDUuODIxOSAxLjM4NDYzIDUuNTYxNyAwLjk1NDg5OCA1LjE2NDAxQyAwLjUyNTE3IDQuNzY2MzMgMC4yMjIwNTYgNC4yNDkwMyAwLjA4MzkwMzcgMy42Nzc1N0MgLTAuMDU0MjQ4MyAzLjEwNjExIC0wLjAyMTIzIDIuNTA2MTcgMC4xNzg3ODEgMS45NTM2NEMgMC4zNzg3OTMgMS40MDExIDAuNzM2ODA5IDAuOTIwODE3IDEuMjA3NTQgMC41NzM1MzhDIDEuNjc4MjYgMC4yMjYyNTkgMi4yNDA1NSAwLjAyNzU5MTkgMi44MjMyNiAwLjAwMjY3MjI5QyAzLjYwMzg5IC0wLjAzMDcxMTUgNC4zNjU3MyAwLjI0OTc4OSA0Ljk0MTQyIDAuNzgyNTUxQyA1LjUxNzExIDEuMzE1MzEgNS44NTk1NiAyLjA1Njc2IDUuODkzNTMgMi44NDRaIi8+CiAgICAgIDxwYXRoIHRyYW5zZm9ybT0idHJhbnNsYXRlKDE2MzkuOCAyMzIzLjgxKSIgZD0iTSA3LjQyNzg5IDMuNTgzMzhDIDcuNDYwMDggNC4zMjQzIDcuMjczNTUgNS4wNTgxOSA2Ljg5MTkzIDUuNjkyMTNDIDYuNTEwMzEgNi4zMjYwNyA1Ljk1MDc1IDYuODMxNTYgNS4yODQxMSA3LjE0NDZDIDQuNjE3NDcgNy40NTc2MyAzLjg3MzcxIDcuNTY0MTQgMy4xNDcwMiA3LjQ1MDYzQyAyLjQyMDMyIDcuMzM3MTIgMS43NDMzNiA3LjAwODcgMS4yMDE4NCA2LjUwNjk1QyAwLjY2MDMyOCA2LjAwNTIgMC4yNzg2MSA1LjM1MjY4IDAuMTA1MDE3IDQuNjMyMDJDIC0wLjA2ODU3NTcgMy45MTEzNSAtMC4wMjYyMzYxIDMuMTU0OTQgMC4yMjY2NzUgMi40NTg1NkMgMC40Nzk1ODcgMS43NjIxNyAwLjkzMTY5NyAxLjE1NzEzIDEuNTI1NzYgMC43MjAwMzNDIDIuMTE5ODMgMC4yODI5MzUgMi44MjkxNCAwLjAzMzQzOTUgMy41NjM4OSAwLjAwMzEzMzQ0QyA0LjU0NjY3IC0wLjAzNzQwMzMgNS41MDUyOSAwLjMxNjcwNiA2LjIyOTYxIDAuOTg3ODM1QyA2Ljk1MzkzIDEuNjU4OTYgNy4zODQ4NCAyLjU5MjM1IDcuNDI3ODkgMy41ODMzOEwgNy40Mjc4OSAzLjU4MzM4WiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM4LjM2IDIyODYuMDYpIiBkPSJNIDIuMjc0NzEgNC4zOTYyOUMgMS44NDM2MyA0LjQxNTA4IDEuNDE2NzEgNC4zMDQ0NSAxLjA0Nzk5IDQuMDc4NDNDIDAuNjc5MjY4IDMuODUyNCAwLjM4NTMyOCAzLjUyMTE0IDAuMjAzMzcxIDMuMTI2NTZDIDAuMDIxNDEzNiAyLjczMTk4IC0wLjA0MDM3OTggMi4yOTE4MyAwLjAyNTgxMTYgMS44NjE4MUMgMC4wOTIwMDMxIDEuNDMxOCAwLjI4MzIwNCAxLjAzMTI2IDAuNTc1MjEzIDAuNzEwODgzQyAwLjg2NzIyMiAwLjM5MDUxIDEuMjQ2OTEgMC4xNjQ3MDggMS42NjYyMiAwLjA2MjA1OTJDIDIuMDg1NTMgLTAuMDQwNTg5NyAyLjUyNTYxIC0wLjAxNTQ3MTQgMi45MzA3NiAwLjEzNDIzNUMgMy4zMzU5MSAwLjI4Mzk0MSAzLjY4NzkyIDAuNTUxNTA1IDMuOTQyMjIgMC45MDMwNkMgNC4xOTY1MiAxLjI1NDYyIDQuMzQxNjkgMS42NzQzNiA0LjM1OTM1IDIuMTA5MTZDIDQuMzgyOTkgMi42OTEwNyA0LjE3Njc4IDMuMjU4NjkgMy43ODU5NyAzLjY4NzQ2QyAzLjM5NTE2IDQuMTE2MjQgMi44NTE2NiA0LjM3MTE2IDIuMjc0NzEgNC4zOTYyOUwgMi4yNzQ3MSA0LjM5NjI5WiIvPgogICAgPC9nPgogIDwvZz4+Cjwvc3ZnPgo=);
  --jp-icon-jupyterlab-wordmark: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyMDAiIHZpZXdCb3g9IjAgMCAxODYwLjggNDc1Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0RTRFNEUiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ4MC4xMzY0MDEsIDY0LjI3MTQ5MykiPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMDAwMDAsIDU4Ljg3NTU2NikiPgogICAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA4NzYwMywgMC4xNDAyOTQpIj4KICAgICAgICA8cGF0aCBkPSJNLTQyNi45LDE2OS44YzAsNDguNy0zLjcsNjQuNy0xMy42LDc2LjRjLTEwLjgsMTAtMjUsMTUuNS0zOS43LDE1LjVsMy43LDI5IGMyMi44LDAuMyw0NC44LTcuOSw2MS45LTIzLjFjMTcuOC0xOC41LDI0LTQ0LjEsMjQtODMuM1YwSC00Mjd2MTcwLjFMLTQyNi45LDE2OS44TC00MjYuOSwxNjkuOHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTU1LjA0NTI5NiwgNTYuODM3MTA0KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuNTYyNDUzLCAxLjc5OTg0MikiPgogICAgICAgIDxwYXRoIGQ9Ik0tMzEyLDE0OGMwLDIxLDAsMzkuNSwxLjcsNTUuNGgtMzEuOGwtMi4xLTMzLjNoLTAuOGMtNi43LDExLjYtMTYuNCwyMS4zLTI4LDI3LjkgYy0xMS42LDYuNi0yNC44LDEwLTM4LjIsOS44Yy0zMS40LDAtNjktMTcuNy02OS04OVYwaDM2LjR2MTEyLjdjMCwzOC43LDExLjYsNjQuNyw0NC42LDY0LjdjMTAuMy0wLjIsMjAuNC0zLjUsMjguOS05LjQgYzguNS01LjksMTUuMS0xNC4zLDE4LjktMjMuOWMyLjItNi4xLDMuMy0xMi41LDMuMy0xOC45VjAuMmgzNi40VjE0OEgtMzEyTC0zMTIsMTQ4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzOTAuMDEzMzIyLCA1My40Nzk2MzgpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS43MDY0NTgsIDAuMjMxNDI1KSI+CiAgICAgICAgPHBhdGggZD0iTS00NzguNiw3MS40YzAtMjYtMC44LTQ3LTEuNy02Ni43aDMyLjdsMS43LDM0LjhoMC44YzcuMS0xMi41LDE3LjUtMjIuOCwzMC4xLTI5LjcgYzEyLjUtNywyNi43LTEwLjMsNDEtOS44YzQ4LjMsMCw4NC43LDQxLjcsODQuNywxMDMuM2MwLDczLjEtNDMuNywxMDkuMi05MSwxMDkuMmMtMTIuMSwwLjUtMjQuMi0yLjItMzUtNy44IGMtMTAuOC01LjYtMTkuOS0xMy45LTI2LjYtMjQuMmgtMC44VjI5MWgtMzZ2LTIyMEwtNDc4LjYsNzEuNEwtNDc4LjYsNzEuNHogTS00NDIuNiwxMjUuNmMwLjEsNS4xLDAuNiwxMC4xLDEuNywxNS4xIGMzLDEyLjMsOS45LDIzLjMsMTkuOCwzMS4xYzkuOSw3LjgsMjIuMSwxMi4xLDM0LjcsMTIuMWMzOC41LDAsNjAuNy0zMS45LDYwLjctNzguNWMwLTQwLjctMjEuMS03NS42LTU5LjUtNzUuNiBjLTEyLjksMC40LTI1LjMsNS4xLTM1LjMsMTMuNGMtOS45LDguMy0xNi45LDE5LjctMTkuNiwzMi40Yy0xLjUsNC45LTIuMywxMC0yLjUsMTUuMVYxMjUuNkwtNDQyLjYsMTI1LjZMLTQ0Mi42LDEyNS42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSg2MDYuNzQwNzI2LCA1Ni44MzcxMDQpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC43NTEyMjYsIDEuOTg5Mjk5KSI+CiAgICAgICAgPHBhdGggZD0iTS00NDAuOCwwbDQzLjcsMTIwLjFjNC41LDEzLjQsOS41LDI5LjQsMTIuOCw0MS43aDAuOGMzLjctMTIuMiw3LjktMjcuNywxMi44LTQyLjQgbDM5LjctMTE5LjJoMzguNUwtMzQ2LjksMTQ1Yy0yNiw2OS43LTQzLjcsMTA1LjQtNjguNiwxMjcuMmMtMTIuNSwxMS43LTI3LjksMjAtNDQuNiwyMy45bC05LjEtMzEuMSBjMTEuNy0zLjksMjIuNS0xMC4xLDMxLjgtMTguMWMxMy4yLTExLjEsMjMuNy0yNS4yLDMwLjYtNDEuMmMxLjUtMi44LDIuNS01LjcsMi45LTguOGMtMC4zLTMuMy0xLjItNi42LTIuNS05LjdMLTQ4MC4yLDAuMSBoMzkuN0wtNDQwLjgsMEwtNDQwLjgsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoODIyLjc0ODEwNCwgMC4wMDAwMDApIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS40NjQwNTAsIDAuMzc4OTE0KSI+CiAgICAgICAgPHBhdGggZD0iTS00MTMuNywwdjU4LjNoNTJ2MjguMmgtNTJWMTk2YzAsMjUsNywzOS41LDI3LjMsMzkuNWM3LjEsMC4xLDE0LjItMC43LDIxLjEtMi41IGwxLjcsMjcuN2MtMTAuMywzLjctMjEuMyw1LjQtMzIuMiw1Yy03LjMsMC40LTE0LjYtMC43LTIxLjMtMy40Yy02LjgtMi43LTEyLjktNi44LTE3LjktMTIuMWMtMTAuMy0xMC45LTE0LjEtMjktMTQuMS01Mi45IFY4Ni41aC0zMVY1OC4zaDMxVjkuNkwtNDEzLjcsMEwtNDEzLjcsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOTc0LjQzMzI4NiwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAuOTkwMDM0LCAwLjYxMDMzOSkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDQ1LjgsMTEzYzAuOCw1MCwzMi4yLDcwLjYsNjguNiw3MC42YzE5LDAuNiwzNy45LTMsNTUuMy0xMC41bDYuMiwyNi40IGMtMjAuOSw4LjktNDMuNSwxMy4xLTY2LjIsMTIuNmMtNjEuNSwwLTk4LjMtNDEuMi05OC4zLTEwMi41Qy00ODAuMiw0OC4yLTQ0NC43LDAtMzg2LjUsMGM2NS4yLDAsODIuNyw1OC4zLDgyLjcsOTUuNyBjLTAuMSw1LjgtMC41LDExLjUtMS4yLDE3LjJoLTE0MC42SC00NDUuOEwtNDQ1LjgsMTEzeiBNLTMzOS4yLDg2LjZjMC40LTIzLjUtOS41LTYwLjEtNTAuNC02MC4xIGMtMzYuOCwwLTUyLjgsMzQuNC01NS43LDYwLjFILTMzOS4yTC0zMzkuMiw4Ni42TC0zMzkuMiw4Ni42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxMjAxLjk2MTA1OCwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuMTc5NjQwLCAwLjcwNTA2OCkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDc4LjYsNjhjMC0yMy45LTAuNC00NC41LTEuNy02My40aDMxLjhsMS4yLDM5LjloMS43YzkuMS0yNy4zLDMxLTQ0LjUsNTUuMy00NC41IGMzLjUtMC4xLDcsMC40LDEwLjMsMS4ydjM0LjhjLTQuMS0wLjktOC4yLTEuMy0xMi40LTEuMmMtMjUuNiwwLTQzLjcsMTkuNy00OC43LDQ3LjRjLTEsNS43LTEuNiwxMS41LTEuNywxNy4ydjEwOC4zaC0zNlY2OCBMLTQ3OC42LDY4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCBkPSJNMTM1Mi4zLDMyNi4yaDM3VjI4aC0zN1YzMjYuMnogTTE2MDQuOCwzMjYuMmMtMi41LTEzLjktMy40LTMxLjEtMy40LTQ4Ljd2LTc2IGMwLTQwLjctMTUuMS04My4xLTc3LjMtODMuMWMtMjUuNiwwLTUwLDcuMS02Ni44LDE4LjFsOC40LDI0LjRjMTQuMy05LjIsMzQtMTUuMSw1My0xNS4xYzQxLjYsMCw0Ni4yLDMwLjIsNDYuMiw0N3Y0LjIgYy03OC42LTAuNC0xMjIuMywyNi41LTEyMi4zLDc1LjZjMCwyOS40LDIxLDU4LjQsNjIuMiw1OC40YzI5LDAsNTAuOS0xNC4zLDYyLjItMzAuMmgxLjNsMi45LDI1LjZIMTYwNC44eiBNMTU2NS43LDI1Ny43IGMwLDMuOC0wLjgsOC0yLjEsMTEuOGMtNS45LDE3LjItMjIuNywzNC00OS4yLDM0Yy0xOC45LDAtMzQuOS0xMS4zLTM0LjktMzUuM2MwLTM5LjUsNDUuOC00Ni42LDg2LjItNDUuOFYyNTcuN3ogTTE2OTguNSwzMjYuMiBsMS43LTMzLjZoMS4zYzE1LjEsMjYuOSwzOC43LDM4LjIsNjguMSwzOC4yYzQ1LjQsMCw5MS4yLTM2LjEsOTEuMi0xMDguOGMwLjQtNjEuNy0zNS4zLTEwMy43LTg1LjctMTAzLjcgYy0zMi44LDAtNTYuMywxNC43LTY5LjMsMzcuNGgtMC44VjI4aC0zNi42djI0NS43YzAsMTguMS0wLjgsMzguNi0xLjcsNTIuNUgxNjk4LjV6IE0xNzA0LjgsMjA4LjJjMC01LjksMS4zLTEwLjksMi4xLTE1LjEgYzcuNi0yOC4xLDMxLjEtNDUuNCw1Ni4zLTQ1LjRjMzkuNSwwLDYwLjUsMzQuOSw2MC41LDc1LjZjMCw0Ni42LTIzLjEsNzguMS02MS44LDc4LjFjLTI2LjksMC00OC4zLTE3LjYtNTUuNS00My4zIGMtMC44LTQuMi0xLjctOC44LTEuNy0xMy40VjIwOC4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgZmlsbD0iIzYxNjE2MSIgZD0iTTE1IDlIOXY2aDZWOXptLTIgNGgtMnYtMmgydjJ6bTgtMlY5aC0yVjdjMC0xLjEtLjktMi0yLTJoLTJWM2gtMnYyaC0yVjNIOXYySDdjLTEuMSAwLTIgLjktMiAydjJIM3YyaDJ2MkgzdjJoMnYyYzAgMS4xLjkgMiAyIDJoMnYyaDJ2LTJoMnYyaDJ2LTJoMmMxLjEgMCAyLS45IDItMnYtMmgydi0yaC0ydi0yaDJ6bS00IDZIN1Y3aDEwdjEweiIvPgo8L3N2Zz4K);
  --jp-icon-keyboard: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMTdjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY3YzAtMS4xLS45LTItMi0yem0tOSAzaDJ2MmgtMlY4em0wIDNoMnYyaC0ydi0yek04IDhoMnYySDhWOHptMCAzaDJ2Mkg4di0yem0tMSAySDV2LTJoMnYyem0wLTNINVY4aDJ2MnptOSA3SDh2LTJoOHYyem0wLTRoLTJ2LTJoMnYyem0wLTNoLTJWOGgydjJ6bTMgM2gtMnYtMmgydjJ6bTAtM2gtMlY4aDJ2MnoiLz4KPC9zdmc+Cg==);
  --jp-icon-launcher: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkgMTlINVY1aDdWM0g1YTIgMiAwIDAwLTIgMnYxNGEyIDIgMCAwMDIgMmgxNGMxLjEgMCAyLS45IDItMnYtN2gtMnY3ek0xNCAzdjJoMy41OWwtOS44MyA5LjgzIDEuNDEgMS40MUwxOSA2LjQxVjEwaDJWM2gtN3oiLz4KPC9zdmc+Cg==);
  --jp-icon-line-form: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGZpbGw9IndoaXRlIiBkPSJNNS44OCA0LjEyTDEzLjc2IDEybC03Ljg4IDcuODhMOCAyMmwxMC0xMEw4IDJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-link: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMuOSAxMmMwLTEuNzEgMS4zOS0zLjEgMy4xLTMuMWg0VjdIN2MtMi43NiAwLTUgMi4yNC01IDVzMi4yNCA1IDUgNWg0di0xLjlIN2MtMS43MSAwLTMuMS0xLjM5LTMuMS0zLjF6TTggMTNoOHYtMkg4djJ6bTktNmgtNHYxLjloNGMxLjcxIDAgMy4xIDEuMzkgMy4xIDMuMXMtMS4zOSAzLjEtMy4xIDMuMWgtNFYxN2g0YzIuNzYgMCA1LTIuMjQgNS01cy0yLjI0LTUtNS01eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiIGQ9Ik0xOSA1djE0SDVWNWgxNG0xLjEtMkgzLjljLS41IDAtLjkuNC0uOS45djE2LjJjMCAuNC40LjkuOS45aDE2LjJjLjQgMCAuOS0uNS45LS45VjMuOWMwLS41LS41LS45LS45LS45ek0xMSA3aDZ2MmgtNlY3em0wIDRoNnYyaC02di0yem0wIDRoNnYyaC02ek03IDdoMnYySDd6bTAgNGgydjJIN3ptMCA0aDJ2Mkg3eiIvPgo8L3N2Zz4=);
  --jp-icon-listings-info: url(data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iaXNvLTg4NTktMSI/Pg0KPHN2ZyB2ZXJzaW9uPSIxLjEiIGlkPSJDYXBhXzEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiIHg9IjBweCIgeT0iMHB4Ig0KCSB2aWV3Qm94PSIwIDAgNTAuOTc4IDUwLjk3OCIgc3R5bGU9ImVuYWJsZS1iYWNrZ3JvdW5kOm5ldyAwIDAgNTAuOTc4IDUwLjk3ODsiIHhtbDpzcGFjZT0icHJlc2VydmUiPg0KPGc+DQoJPGc+DQoJCTxnPg0KCQkJPHBhdGggc3R5bGU9ImZpbGw6IzAxMDAwMjsiIGQ9Ik00My41Miw3LjQ1OEMzOC43MTEsMi42NDgsMzIuMzA3LDAsMjUuNDg5LDBDMTguNjcsMCwxMi4yNjYsMi42NDgsNy40NTgsNy40NTgNCgkJCQljLTkuOTQzLDkuOTQxLTkuOTQzLDI2LjExOSwwLDM2LjA2MmM0LjgwOSw0LjgwOSwxMS4yMTIsNy40NTYsMTguMDMxLDcuNDU4YzAsMCwwLjAwMSwwLDAuMDAyLDANCgkJCQljNi44MTYsMCwxMy4yMjEtMi42NDgsMTguMDI5LTcuNDU4YzQuODA5LTQuODA5LDcuNDU3LTExLjIxMiw3LjQ1Ny0xOC4wM0M1MC45NzcsMTguNjcsNDguMzI4LDEyLjI2Niw0My41Miw3LjQ1OHoNCgkJCQkgTTQyLjEwNiw0Mi4xMDVjLTQuNDMyLDQuNDMxLTEwLjMzMiw2Ljg3Mi0xNi42MTUsNi44NzJoLTAuMDAyYy02LjI4NS0wLjAwMS0xMi4xODctMi40NDEtMTYuNjE3LTYuODcyDQoJCQkJYy05LjE2Mi05LjE2My05LjE2Mi0yNC4wNzEsMC0zMy4yMzNDMTMuMzAzLDQuNDQsMTkuMjA0LDIsMjUuNDg5LDJjNi4yODQsMCwxMi4xODYsMi40NCwxNi42MTcsNi44NzINCgkJCQljNC40MzEsNC40MzEsNi44NzEsMTAuMzMyLDYuODcxLDE2LjYxN0M0OC45NzcsMzEuNzcyLDQ2LjUzNiwzNy42NzUsNDIuMTA2LDQyLjEwNXoiLz4NCgkJPC9nPg0KCQk8Zz4NCgkJCTxwYXRoIHN0eWxlPSJmaWxsOiMwMTAwMDI7IiBkPSJNMjMuNTc4LDMyLjIxOGMtMC4wMjMtMS43MzQsMC4xNDMtMy4wNTksMC40OTYtMy45NzJjMC4zNTMtMC45MTMsMS4xMS0xLjk5NywyLjI3Mi0zLjI1Mw0KCQkJCWMwLjQ2OC0wLjUzNiwwLjkyMy0xLjA2MiwxLjM2Ny0xLjU3NWMwLjYyNi0wLjc1MywxLjEwNC0xLjQ3OCwxLjQzNi0yLjE3NWMwLjMzMS0wLjcwNywwLjQ5NS0xLjU0MSwwLjQ5NS0yLjUNCgkJCQljMC0xLjA5Ni0wLjI2LTIuMDg4LTAuNzc5LTIuOTc5Yy0wLjU2NS0wLjg3OS0xLjUwMS0xLjMzNi0yLjgwNi0xLjM2OWMtMS44MDIsMC4wNTctMi45ODUsMC42NjctMy41NSwxLjgzMg0KCQkJCWMtMC4zMDEsMC41MzUtMC41MDMsMS4xNDEtMC42MDcsMS44MTRjLTAuMTM5LDAuNzA3LTAuMjA3LDEuNDMyLTAuMjA3LDIuMTc0aC0yLjkzN2MtMC4wOTEtMi4yMDgsMC40MDctNC4xMTQsMS40OTMtNS43MTkNCgkJCQljMS4wNjItMS42NCwyLjg1NS0yLjQ4MSw1LjM3OC0yLjUyN2MyLjE2LDAuMDIzLDMuODc0LDAuNjA4LDUuMTQxLDEuNzU4YzEuMjc4LDEuMTYsMS45MjksMi43NjQsMS45NSw0LjgxMQ0KCQkJCWMwLDEuMTQyLTAuMTM3LDIuMTExLTAuNDEsMi45MTFjLTAuMzA5LDAuODQ1LTAuNzMxLDEuNTkzLTEuMjY4LDIuMjQzYy0wLjQ5MiwwLjY1LTEuMDY4LDEuMzE4LTEuNzMsMi4wMDINCgkJCQljLTAuNjUsMC42OTctMS4zMTMsMS40NzktMS45ODcsMi4zNDZjLTAuMjM5LDAuMzc3LTAuNDI5LDAuNzc3LTAuNTY1LDEuMTk5Yy0wLjE2LDAuOTU5LTAuMjE3LDEuOTUxLTAuMTcxLDIuOTc5DQoJCQkJQzI2LjU4OSwzMi4yMTgsMjMuNTc4LDMyLjIxOCwyMy41NzgsMzIuMjE4eiBNMjMuNTc4LDM4LjIydi0zLjQ4NGgzLjA3NnYzLjQ4NEgyMy41Nzh6Ii8+DQoJCTwvZz4NCgk8L2c+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8L3N2Zz4NCg==);
  --jp-icon-markdown: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjN0IxRkEyIiBkPSJNNSAxNC45aDEybC02LjEgNnptOS40LTYuOGMwLTEuMy0uMS0yLjktLjEtNC41LS40IDEuNC0uOSAyLjktMS4zIDQuM2wtMS4zIDQuM2gtMkw4LjUgNy45Yy0uNC0xLjMtLjctMi45LTEtNC4zLS4xIDEuNi0uMSAzLjItLjIgNC42TDcgMTIuNEg0LjhsLjctMTFoMy4zTDEwIDVjLjQgMS4yLjcgMi43IDEgMy45LjMtMS4yLjctMi42IDEtMy45bDEuMi0zLjdoMy4zbC42IDExaC0yLjRsLS4zLTQuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-new-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwIDZoLThsLTItMkg0Yy0xLjExIDAtMS45OS44OS0xLjk5IDJMMiAxOGMwIDEuMTEuODkgMiAyIDJoMTZjMS4xMSAwIDItLjg5IDItMlY4YzAtMS4xMS0uODktMi0yLTJ6bS0xIDhoLTN2M2gtMnYtM2gtM3YtMmgzVjloMnYzaDN2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-not-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI1IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDMgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMTkgMTcuMTg0NCAyLjk2OTY4IDE0LjMwMzIgMS44NjA5NCAxMS40NDA5WiIvPgogICAgPHBhdGggY2xhc3M9ImpwLWljb24yIiBzdHJva2U9IiMzMzMzMzMiIHN0cm9rZS13aWR0aD0iMiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOS4zMTU5MiA5LjMyMDMxKSIgZD0iTTcuMzY4NDIgMEwwIDcuMzY0NzkiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDkuMzE1OTIgMTYuNjgzNikgc2NhbGUoMSAtMSkiIGQ9Ik03LjM2ODQyIDBMMCA3LjM2NDc5Ii8+Cjwvc3ZnPgo=);
  --jp-icon-notebook: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNFRjZDMDAiPgogICAgPHBhdGggZD0iTTE4LjcgMy4zdjE1LjRIMy4zVjMuM2gxNS40bTEuNS0xLjVIMS44djE4LjNoMTguM2wuMS0xOC4zeiIvPgogICAgPHBhdGggZD0iTTE2LjUgMTYuNWwtNS40LTQuMy01LjYgNC4zdi0xMWgxMXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-palette: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE4IDEzVjIwSDRWNkg5LjAyQzkuMDcgNS4yOSA5LjI0IDQuNjIgOS41IDRINEMyLjkgNCAyIDQuOSAyIDZWMjBDMiAyMS4xIDIuOSAyMiA0IDIySDE4QzE5LjEgMjIgMjAgMjEuMSAyMCAyMFYxNUwxOCAxM1pNMTkuMyA4Ljg5QzE5Ljc0IDguMTkgMjAgNy4zOCAyMCA2LjVDMjAgNC4wMSAxNy45OSAyIDE1LjUgMkMxMy4wMSAyIDExIDQuMDEgMTEgNi41QzExIDguOTkgMTMuMDEgMTEgMTUuNDkgMTFDMTYuMzcgMTEgMTcuMTkgMTAuNzQgMTcuODggMTAuM0wyMSAxMy40MkwyMi40MiAxMkwxOS4zIDguODlaTTE1LjUgOUMxNC4xMiA5IDEzIDcuODggMTMgNi41QzEzIDUuMTIgMTQuMTIgNCAxNS41IDRDMTYuODggNCAxOCA1LjEyIDE4IDYuNUMxOCA3Ljg4IDE2Ljg4IDkgMTUuNSA5WiIvPgogICAgPHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik00IDZIOS4wMTg5NEM5LjAwNjM5IDYuMTY1MDIgOSA2LjMzMTc2IDkgNi41QzkgOC44MTU3NyAxMC4yMTEgMTAuODQ4NyAxMi4wMzQzIDEySDlWMTRIMTZWMTIuOTgxMUMxNi41NzAzIDEyLjkzNzcgMTcuMTIgMTIuODIwNyAxNy42Mzk2IDEyLjYzOTZMMTggMTNWMjBINFY2Wk04IDhINlYxMEg4VjhaTTYgMTJIOFYxNEg2VjEyWk04IDE2SDZWMThIOFYxNlpNOSAxNkgxNlYxOEg5VjE2WiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-paste: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE5IDJoLTQuMThDMTQuNC44NCAxMy4zIDAgMTIgMGMtMS4zIDAtMi40Ljg0LTIuODIgMkg1Yy0xLjEgMC0yIC45LTIgMnYxNmMwIDEuMS45IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjRjMC0xLjEtLjktMi0yLTJ6bS03IDBjLjU1IDAgMSAuNDUgMSAxcy0uNDUgMS0xIDEtMS0uNDUtMS0xIC40NS0xIDEtMXptNyAxOEg1VjRoMnYzaDEwVjRoMnYxNnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-python: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1icmFuZDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMEQ0N0ExIj4KICAgIDxwYXRoIGQ9Ik0xMS4xIDYuOVY1LjhINi45YzAtLjUgMC0xLjMuMi0xLjYuNC0uNy44LTEuMSAxLjctMS40IDEuNy0uMyAyLjUtLjMgMy45LS4xIDEgLjEgMS45LjkgMS45IDEuOXY0LjJjMCAuNS0uOSAxLjYtMiAxLjZIOC44Yy0xLjUgMC0yLjQgMS40LTIuNCAyLjh2Mi4ySDQuN0MzLjUgMTUuMSAzIDE0IDMgMTMuMVY5Yy0uMS0xIC42LTIgMS44LTIgMS41LS4xIDYuMy0uMSA2LjMtLjF6Ii8+CiAgICA8cGF0aCBkPSJNMTAuOSAxNS4xdjEuMWg0LjJjMCAuNSAwIDEuMy0uMiAxLjYtLjQuNy0uOCAxLjEtMS43IDEuNC0xLjcuMy0yLjUuMy0zLjkuMS0xLS4xLTEuOS0uOS0xLjktMS45di00LjJjMC0uNS45LTEuNiAyLTEuNmgzLjhjMS41IDAgMi40LTEuNCAyLjQtMi44VjYuNmgxLjdDMTguNSA2LjkgMTkgOCAxOSA4LjlWMTNjMCAxLS43IDIuMS0xLjkgMi4xaC02LjJ6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-r-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjE5NkYzIiBkPSJNNC40IDIuNWMxLjItLjEgMi45LS4zIDQuOS0uMyAyLjUgMCA0LjEuNCA1LjIgMS4zIDEgLjcgMS41IDEuOSAxLjUgMy41IDAgMi0xLjQgMy41LTIuOSA0LjEgMS4yLjQgMS43IDEuNiAyLjIgMyAuNiAxLjkgMSAzLjkgMS4zIDQuNmgtMy44Yy0uMy0uNC0uOC0xLjctMS4yLTMuN3MtMS4yLTIuNi0yLjYtMi42aC0uOXY2LjRINC40VjIuNXptMy43IDYuOWgxLjRjMS45IDAgMi45LS45IDIuOS0yLjNzLTEtMi4zLTIuOC0yLjNjLS43IDAtMS4zIDAtMS42LjJ2NC41aC4xdi0uMXoiLz4KPC9zdmc+Cg==);
  --jp-icon-react: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMTUwIDE1MCA1NDEuOSAyOTUuMyI+CiAgPGcgY2xhc3M9ImpwLWljb24tYnJhbmQyIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzYxREFGQiI+CiAgICA8cGF0aCBkPSJNNjY2LjMgMjk2LjVjMC0zMi41LTQwLjctNjMuMy0xMDMuMS04Mi40IDE0LjQtNjMuNiA4LTExNC4yLTIwLjItMTMwLjQtNi41LTMuOC0xNC4xLTUuNi0yMi40LTUuNnYyMi4zYzQuNiAwIDguMy45IDExLjQgMi42IDEzLjYgNy44IDE5LjUgMzcuNSAxNC45IDc1LjctMS4xIDkuNC0yLjkgMTkuMy01LjEgMjkuNC0xOS42LTQuOC00MS04LjUtNjMuNS0xMC45LTEzLjUtMTguNS0yNy41LTM1LjMtNDEuNi01MCAzMi42LTMwLjMgNjMuMi00Ni45IDg0LTQ2LjlWNzhjLTI3LjUgMC02My41IDE5LjYtOTkuOSA1My42LTM2LjQtMzMuOC03Mi40LTUzLjItOTkuOS01My4ydjIyLjNjMjAuNyAwIDUxLjQgMTYuNSA4NCA0Ni42LTE0IDE0LjctMjggMzEuNC00MS4zIDQ5LjktMjIuNiAyLjQtNDQgNi4xLTYzLjYgMTEtMi4zLTEwLTQtMTkuNy01LjItMjktNC43LTM4LjIgMS4xLTY3LjkgMTQuNi03NS44IDMtMS44IDYuOS0yLjYgMTEuNS0yLjZWNzguNWMtOC40IDAtMTYgMS44LTIyLjYgNS42LTI4LjEgMTYuMi0zNC40IDY2LjctMTkuOSAxMzAuMS02Mi4yIDE5LjItMTAyLjcgNDkuOS0xMDIuNyA4Mi4zIDAgMzIuNSA0MC43IDYzLjMgMTAzLjEgODIuNC0xNC40IDYzLjYtOCAxMTQuMiAyMC4yIDEzMC40IDYuNSAzLjggMTQuMSA1LjYgMjIuNSA1LjYgMjcuNSAwIDYzLjUtMTkuNiA5OS45LTUzLjYgMzYuNCAzMy44IDcyLjQgNTMuMiA5OS45IDUzLjIgOC40IDAgMTYtMS44IDIyLjYtNS42IDI4LjEtMTYuMiAzNC40LTY2LjcgMTkuOS0xMzAuMSA2Mi0xOS4xIDEwMi41LTQ5LjkgMTAyLjUtODIuM3ptLTEzMC4yLTY2LjdjLTMuNyAxMi45LTguMyAyNi4yLTEzLjUgMzkuNS00LjEtOC04LjQtMTYtMTMuMS0yNC00LjYtOC05LjUtMTUuOC0xNC40LTIzLjQgMTQuMiAyLjEgMjcuOSA0LjcgNDEgNy45em0tNDUuOCAxMDYuNWMtNy44IDEzLjUtMTUuOCAyNi4zLTI0LjEgMzguMi0xNC45IDEuMy0zMCAyLTQ1LjIgMi0xNS4xIDAtMzAuMi0uNy00NS0xLjktOC4zLTExLjktMTYuNC0yNC42LTI0LjItMzgtNy42LTEzLjEtMTQuNS0yNi40LTIwLjgtMzkuOCA2LjItMTMuNCAxMy4yLTI2LjggMjAuNy0zOS45IDcuOC0xMy41IDE1LjgtMjYuMyAyNC4xLTM4LjIgMTQuOS0xLjMgMzAtMiA0NS4yLTIgMTUuMSAwIDMwLjIuNyA0NSAxLjkgOC4zIDExLjkgMTYuNCAyNC42IDI0LjIgMzggNy42IDEzLjEgMTQuNSAyNi40IDIwLjggMzkuOC02LjMgMTMuNC0xMy4yIDI2LjgtMjAuNyAzOS45em0zMi4zLTEzYzUuNCAxMy40IDEwIDI2LjggMTMuOCAzOS44LTEzLjEgMy4yLTI2LjkgNS45LTQxLjIgOCA0LjktNy43IDkuOC0xNS42IDE0LjQtMjMuNyA0LjYtOCA4LjktMTYuMSAxMy0yNC4xek00MjEuMiA0MzBjLTkuMy05LjYtMTguNi0yMC4zLTI3LjgtMzIgOSAuNCAxOC4yLjcgMjcuNS43IDkuNCAwIDE4LjctLjIgMjcuOC0uNy05IDExLjctMTguMyAyMi40LTI3LjUgMzJ6bS03NC40LTU4LjljLTE0LjItMi4xLTI3LjktNC43LTQxLTcuOSAzLjctMTIuOSA4LjMtMjYuMiAxMy41LTM5LjUgNC4xIDggOC40IDE2IDEzLjEgMjQgNC43IDggOS41IDE1LjggMTQuNCAyMy40ek00MjAuNyAxNjNjOS4zIDkuNiAxOC42IDIwLjMgMjcuOCAzMi05LS40LTE4LjItLjctMjcuNS0uNy05LjQgMC0xOC43LjItMjcuOC43IDktMTEuNyAxOC4zLTIyLjQgMjcuNS0zMnptLTc0IDU4LjljLTQuOSA3LjctOS44IDE1LjYtMTQuNCAyMy43LTQuNiA4LTguOSAxNi0xMyAyNC01LjQtMTMuNC0xMC0yNi44LTEzLjgtMzkuOCAxMy4xLTMuMSAyNi45LTUuOCA0MS4yLTcuOXptLTkwLjUgMTI1LjJjLTM1LjQtMTUuMS01OC4zLTM0LjktNTguMy01MC42IDAtMTUuNyAyMi45LTM1LjYgNTguMy01MC42IDguNi0zLjcgMTgtNyAyNy43LTEwLjEgNS43IDE5LjYgMTMuMiA0MCAyMi41IDYwLjktOS4yIDIwLjgtMTYuNiA0MS4xLTIyLjIgNjAuNi05LjktMy4xLTE5LjMtNi41LTI4LTEwLjJ6TTMxMCA0OTBjLTEzLjYtNy44LTE5LjUtMzcuNS0xNC45LTc1LjcgMS4xLTkuNCAyLjktMTkuMyA1LjEtMjkuNCAxOS42IDQuOCA0MSA4LjUgNjMuNSAxMC45IDEzLjUgMTguNSAyNy41IDM1LjMgNDEuNiA1MC0zMi42IDMwLjMtNjMuMiA0Ni45LTg0IDQ2LjktNC41LS4xLTguMy0xLTExLjMtMi43em0yMzcuMi03Ni4yYzQuNyAzOC4yLTEuMSA2Ny45LTE0LjYgNzUuOC0zIDEuOC02LjkgMi42LTExLjUgMi42LTIwLjcgMC01MS40LTE2LjUtODQtNDYuNiAxNC0xNC43IDI4LTMxLjQgNDEuMy00OS45IDIyLjYtMi40IDQ0LTYuMSA2My42LTExIDIuMyAxMC4xIDQuMSAxOS44IDUuMiAyOS4xem0zOC41LTY2LjdjLTguNiAzLjctMTggNy0yNy43IDEwLjEtNS43LTE5LjYtMTMuMi00MC0yMi41LTYwLjkgOS4yLTIwLjggMTYuNi00MS4xIDIyLjItNjAuNiA5LjkgMy4xIDE5LjMgNi41IDI4LjEgMTAuMiAzNS40IDE1LjEgNTguMyAzNC45IDU4LjMgNTAuNi0uMSAxNS43LTIzIDM1LjYtNTguNCA1MC42ek0zMjAuOCA3OC40eiIvPgogICAgPGNpcmNsZSBjeD0iNDIwLjkiIGN5PSIyOTYuNSIgcj0iNDUuNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-refresh: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTkgMTMuNWMtMi40OSAwLTQuNS0yLjAxLTQuNS00LjVTNi41MSA0LjUgOSA0LjVjMS4yNCAwIDIuMzYuNTIgMy4xNyAxLjMzTDEwIDhoNVYzbC0xLjc2IDEuNzZDMTIuMTUgMy42OCAxMC42NiAzIDkgMyA1LjY5IDMgMy4wMSA1LjY5IDMuMDEgOVM1LjY5IDE1IDkgMTVjMi45NyAwIDUuNDMtMi4xNiA1LjktNWgtMS41MmMtLjQ2IDItMi4yNCAzLjUtNC4zOCAzLjV6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-regex: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi1hY2NlbnQyIiBmaWxsPSIjRkZGIj4KICAgIDxjaXJjbGUgY2xhc3M9InN0MiIgY3g9IjUuNSIgY3k9IjE0LjUiIHI9IjEuNSIvPgogICAgPHJlY3QgeD0iMTIiIHk9IjQiIGNsYXNzPSJzdDIiIHdpZHRoPSIxIiBoZWlnaHQ9IjgiLz4KICAgIDxyZWN0IHg9IjguNSIgeT0iNy41IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjg2NiAtMC41IDAuNSAwLjg2NiAtMi4zMjU1IDcuMzIxOSkiIGNsYXNzPSJzdDIiIHdpZHRoPSI4IiBoZWlnaHQ9IjEiLz4KICAgIDxyZWN0IHg9IjEyIiB5PSI0IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjUgLTAuODY2IDAuODY2IDAuNSAtMC42Nzc5IDE0LjgyNTIpIiBjbGFzcz0ic3QyIiB3aWR0aD0iMSIgaGVpZ2h0PSI4Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-run: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTggNXYxNGwxMS03eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-running: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMjU2IDhDMTE5IDggOCAxMTkgOCAyNTZzMTExIDI0OCAyNDggMjQ4IDI0OC0xMTEgMjQ4LTI0OFMzOTMgOCAyNTYgOHptOTYgMzI4YzAgOC44LTcuMiAxNi0xNiAxNkgxNzZjLTguOCAwLTE2LTcuMi0xNi0xNlYxNzZjMC04LjggNy4yLTE2IDE2LTE2aDE2MGM4LjggMCAxNiA3LjIgMTYgMTZ2MTYweiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-save: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE3IDNINWMtMS4xMSAwLTIgLjktMiAydjE0YzAgMS4xLjg5IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjdsLTQtNHptLTUgMTZjLTEuNjYgMC0zLTEuMzQtMy0zczEuMzQtMyAzLTMgMyAxLjM0IDMgMy0xLjM0IDMtMyAzem0zLTEwSDVWNWgxMHY0eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-search: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjEsMTAuOWgtMC43bC0wLjItMC4yYzAuOC0wLjksMS4zLTIuMiwxLjMtMy41YzAtMy0yLjQtNS40LTUuNC01LjRTMS44LDQuMiwxLjgsNy4xczIuNCw1LjQsNS40LDUuNCBjMS4zLDAsMi41LTAuNSwzLjUtMS4zbDAuMiwwLjJ2MC43bDQuMSw0LjFsMS4yLTEuMkwxMi4xLDEwLjl6IE03LjEsMTAuOWMtMi4xLDAtMy43LTEuNy0zLjctMy43czEuNy0zLjcsMy43LTMuN3MzLjcsMS43LDMuNywzLjcgUzkuMiwxMC45LDcuMSwxMC45eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-settings: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuNDMgMTIuOThjLjA0LS4zMi4wNy0uNjQuMDctLjk4cy0uMDMtLjY2LS4wNy0uOThsMi4xMS0xLjY1Yy4xOS0uMTUuMjQtLjQyLjEyLS42NGwtMi0zLjQ2Yy0uMTItLjIyLS4zOS0uMy0uNjEtLjIybC0yLjQ5IDFjLS41Mi0uNC0xLjA4LS43My0xLjY5LS45OGwtLjM4LTIuNjVBLjQ4OC40ODggMCAwMDE0IDJoLTRjLS4yNSAwLS40Ni4xOC0uNDkuNDJsLS4zOCAyLjY1Yy0uNjEuMjUtMS4xNy41OS0xLjY5Ljk4bC0yLjQ5LTFjLS4yMy0uMDktLjQ5IDAtLjYxLjIybC0yIDMuNDZjLS4xMy4yMi0uMDcuNDkuMTIuNjRsMi4xMSAxLjY1Yy0uMDQuMzItLjA3LjY1LS4wNy45OHMuMDMuNjYuMDcuOThsLTIuMTEgMS42NWMtLjE5LjE1LS4yNC40Mi0uMTIuNjRsMiAzLjQ2Yy4xMi4yMi4zOS4zLjYxLjIybDIuNDktMWMuNTIuNCAxLjA4LjczIDEuNjkuOThsLjM4IDIuNjVjLjAzLjI0LjI0LjQyLjQ5LjQyaDRjLjI1IDAgLjQ2LS4xOC40OS0uNDJsLjM4LTIuNjVjLjYxLS4yNSAxLjE3LS41OSAxLjY5LS45OGwyLjQ5IDFjLjIzLjA5LjQ5IDAgLjYxLS4yMmwyLTMuNDZjLjEyLS4yMi4wNy0uNDktLjEyLS42NGwtMi4xMS0xLjY1ek0xMiAxNS41Yy0xLjkzIDAtMy41LTEuNTctMy41LTMuNXMxLjU3LTMuNSAzLjUtMy41IDMuNSAxLjU3IDMuNSAzLjUtMS41NyAzLjUtMy41IDMuNXoiLz4KPC9zdmc+Cg==);
  --jp-icon-spreadsheet: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNENBRjUwIiBkPSJNMi4yIDIuMnYxNy42aDE3LjZWMi4ySDIuMnptMTUuNCA3LjdoLTUuNVY0LjRoNS41djUuNXpNOS45IDQuNHY1LjVINC40VjQuNGg1LjV6bS01LjUgNy43aDUuNXY1LjVINC40di01LjV6bTcuNyA1LjV2LTUuNWg1LjV2NS41aC01LjV6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-stop: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik02IDZoMTJ2MTJINnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-tab: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIxIDNIM2MtMS4xIDAtMiAuOS0yIDJ2MTRjMCAxLjEuOSAyIDIgMmgxOGMxLjEgMCAyLS45IDItMlY1YzAtMS4xLS45LTItMi0yem0wIDE2SDNWNWgxMHY0aDh2MTB6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-terminal: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0IiA+CiAgICA8cmVjdCBjbGFzcz0ianAtaWNvbjIganAtaWNvbi1zZWxlY3RhYmxlIiB3aWR0aD0iMjAiIGhlaWdodD0iMjAiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMikiIGZpbGw9IiMzMzMzMzMiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uLWFjY2VudDIganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGQ9Ik01LjA1NjY0IDguNzYxNzJDNS4wNTY2NCA4LjU5NzY2IDUuMDMxMjUgOC40NTMxMiA0Ljk4MDQ3IDguMzI4MTJDNC45MzM1OSA4LjE5OTIyIDQuODU1NDcgOC4wODIwMyA0Ljc0NjA5IDcuOTc2NTZDNC42NDA2MiA3Ljg3MTA5IDQuNSA3Ljc3NTM5IDQuMzI0MjIgNy42ODk0NUM0LjE1MjM0IDcuNTk5NjEgMy45NDMzNiA3LjUxMTcyIDMuNjk3MjcgNy40MjU3OEMzLjMwMjczIDcuMjg1MTYgMi45NDMzNiA3LjEzNjcyIDIuNjE5MTQgNi45ODA0N0MyLjI5NDkyIDYuODI0MjIgMi4wMTc1OCA2LjY0MjU4IDEuNzg3MTEgNi40MzU1NUMxLjU2MDU1IDYuMjI4NTIgMS4zODQ3NyA1Ljk4ODI4IDEuMjU5NzcgNS43MTQ4NEMxLjEzNDc3IDUuNDM3NSAxLjA3MjI3IDUuMTA5MzggMS4wNzIyNyA0LjczMDQ3QzEuMDcyMjcgNC4zOTg0NCAxLjEyODkxIDQuMDk1NyAxLjI0MjE5IDMuODIyMjdDMS4zNTU0NyAzLjU0NDkyIDEuNTE1NjIgMy4zMDQ2OSAxLjcyMjY2IDMuMTAxNTZDMS45Mjk2OSAyLjg5ODQ0IDIuMTc5NjkgMi43MzQzNyAyLjQ3MjY2IDIuNjA5MzhDMi43NjU2MiAyLjQ4NDM4IDMuMDkxOCAyLjQwNDMgMy40NTExNyAyLjM2OTE0VjEuMTA5MzhINC4zODg2N1YyLjM4MDg2QzQuNzQwMjMgMi40Mjc3MyA1LjA1NjY0IDIuNTIzNDQgNS4zMzc4OSAyLjY2Nzk3QzUuNjE5MTQgMi44MTI1IDUuODU3NDIgMy4wMDE5NSA2LjA1MjczIDMuMjM2MzNDNi4yNTE5NSAzLjQ2NjggNi40MDQzIDMuNzQwMjMgNi41MDk3NyA0LjA1NjY0QzYuNjE5MTQgNC4zNjkxNCA2LjY3MzgzIDQuNzIwNyA2LjY3MzgzIDUuMTExMzNINS4wNDQ5MkM1LjA0NDkyIDQuNjM4NjcgNC45Mzc1IDQuMjgxMjUgNC43MjI2NiA0LjAzOTA2QzQuNTA3ODEgMy43OTI5NyA0LjIxNjggMy42Njk5MiAzLjg0OTYxIDMuNjY5OTJDMy42NTAzOSAzLjY2OTkyIDMuNDc2NTYgMy42OTcyNyAzLjMyODEyIDMuNzUxOTVDMy4xODM1OSAzLjgwMjczIDMuMDY0NDUgMy44NzY5NSAyLjk3MDcgMy45NzQ2MUMyLjg3Njk1IDQuMDY4MzYgMi44MDY2NCA0LjE3OTY5IDIuNzU5NzcgNC4zMDg1OUMyLjcxNjggNC40Mzc1IDIuNjk1MzEgNC41NzgxMiAyLjY5NTMxIDQuNzMwNDdDMi42OTUzMSA0Ljg4MjgxIDIuNzE2OCA1LjAxOTUzIDIuNzU5NzcgNS4xNDA2MkMyLjgwNjY0IDUuMjU3ODEgMi44ODI4MSA1LjM2NzE5IDIuOTg4MjggNS40Njg3NUMzLjA5NzY2IDUuNTcwMzEgMy4yNDAyMyA1LjY2Nzk3IDMuNDE2MDIgNS43NjE3MkMzLjU5MTggNS44NTE1NiAzLjgxMDU1IDUuOTQzMzYgNC4wNzIyNyA2LjAzNzExQzQuNDY2OCA2LjE4NTU1IDQuODI0MjIgNi4zMzk4NCA1LjE0NDUzIDYuNUM1LjQ2NDg0IDYuNjU2MjUgNS43MzgyOCA2LjgzOTg0IDUuOTY0ODQgNy4wNTA3OEM2LjE5NTMxIDcuMjU3ODEgNi4zNzEwOSA3LjUgNi40OTIxOSA3Ljc3NzM0QzYuNjE3MTkgOC4wNTA3OCA2LjY3OTY5IDguMzc1IDYuNjc5NjkgOC43NUM2LjY3OTY5IDkuMDkzNzUgNi42MjMwNSA5LjQwNDMgNi41MDk3NyA5LjY4MTY0QzYuMzk2NDggOS45NTUwOCA2LjIzNDM4IDEwLjE5MTQgNi4wMjM0NCAxMC4zOTA2QzUuODEyNSAxMC41ODk4IDUuNTU4NTkgMTAuNzUgNS4yNjE3MiAxMC44NzExQzQuOTY0ODQgMTAuOTg4MyA0LjYzMjgxIDExLjA2NDUgNC4yNjU2MiAxMS4wOTk2VjEyLjI0OEgzLjMzMzk4VjExLjA5OTZDMy4wMDE5NSAxMS4wNjg0IDIuNjc5NjkgMTAuOTk2MSAyLjM2NzE5IDEwLjg4MjhDMi4wNTQ2OSAxMC43NjU2IDEuNzc3MzQgMTAuNTk3NyAxLjUzNTE2IDEwLjM3ODlDMS4yOTY4OCAxMC4xNjAyIDEuMTA1NDcgOS44ODQ3NyAwLjk2MDkzOCA5LjU1MjczQzAuODE2NDA2IDkuMjE2OCAwLjc0NDE0MSA4LjgxNDQ1IDAuNzQ0MTQxIDguMzQ1N0gyLjM3ODkxQzIuMzc4OTEgOC42MjY5NSAyLjQxOTkyIDguODYzMjggMi41MDE5NSA5LjA1NDY5QzIuNTgzOTggOS4yNDIxOSAyLjY4OTQ1IDkuMzkyNTggMi44MTgzNiA5LjUwNTg2QzIuOTUxMTcgOS42MTUyMyAzLjEwMTU2IDkuNjkzMzYgMy4yNjk1MyA5Ljc0MDIzQzMuNDM3NSA5Ljc4NzExIDMuNjA5MzggOS44MTA1NSAzLjc4NTE2IDkuODEwNTVDNC4yMDMxMiA5LjgxMDU1IDQuNTE5NTMgOS43MTI4OSA0LjczNDM4IDkuNTE3NThDNC45NDkyMiA5LjMyMjI3IDUuMDU2NjQgOS4wNzAzMSA1LjA1NjY0IDguNzYxNzJaTTEzLjQxOCAxMi4yNzE1SDguMDc0MjJWMTFIMTMuNDE4VjEyLjI3MTVaIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzLjk1MjY0IDYpIiBmaWxsPSJ3aGl0ZSIvPgo8L3N2Zz4K);
  --jp-icon-text-editor: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTUgMTVIM3YyaDEydi0yem0wLThIM3YyaDEyVjd6TTMgMTNoMTh2LTJIM3Yyem0wIDhoMTh2LTJIM3Yyek0zIDN2MmgxOFYzSDN6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMiAxNy4xODQ0IDIuOTY5NjggMTQuMzAzMiAxLjg2MDk0IDExLjQ0MDlaIi8+CiAgICA8cGF0aCBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiMzMzMzMzMiIHN0cm9rZT0iIzMzMzMzMyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOCA5Ljg2NzE5KSIgZD0iTTIuODYwMTUgNC44NjUzNUwwLjcyNjU0OSAyLjk5OTU5TDAgMy42MzA0NUwyLjg2MDE1IDYuMTMxNTdMOCAwLjYzMDg3Mkw3LjI3ODU3IDBMMi44NjAxNSA0Ljg2NTM1WiIvPgo8L3N2Zz4K);
  --jp-icon-undo: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjUgOGMtMi42NSAwLTUuMDUuOTktNi45IDIuNkwyIDd2OWg5bC0zLjYyLTMuNjJjMS4zOS0xLjE2IDMuMTYtMS44OCA1LjEyLTEuODggMy41NCAwIDYuNTUgMi4zMSA3LjYgNS41bDIuMzctLjc4QzIxLjA4IDExLjAzIDE3LjE1IDggMTIuNSA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-vega: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbjEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjEyMTIxIj4KICAgIDxwYXRoIGQ9Ik0xMC42IDUuNGwyLjItMy4ySDIuMnY3LjNsNC02LjZ6Ii8+CiAgICA8cGF0aCBkPSJNMTUuOCAyLjJsLTQuNCA2LjZMNyA2LjNsLTQuOCA4djUuNWgxNy42VjIuMmgtNHptLTcgMTUuNEg1LjV2LTQuNGgzLjN2NC40em00LjQgMEg5LjhWOS44aDMuNHY3Ljh6bTQuNCAwaC0zLjRWNi41aDMuNHYxMS4xeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-yaml: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1jb250cmFzdDIganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjRDgxQjYwIj4KICAgIDxwYXRoIGQ9Ik03LjIgMTguNnYtNS40TDMgNS42aDMuM2wxLjQgMy4xYy4zLjkuNiAxLjYgMSAyLjUuMy0uOC42LTEuNiAxLTIuNWwxLjQtMy4xaDMuNGwtNC40IDcuNnY1LjVsLTIuOS0uMXoiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxNi41IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxMSIgcj0iMi4xIi8+CiAgPC9nPgo8L3N2Zz4K);
}

/* Icon CSS class declarations */

.jp-AddIcon {
  background-image: var(--jp-icon-add);
}
.jp-BugIcon {
  background-image: var(--jp-icon-bug);
}
.jp-BuildIcon {
  background-image: var(--jp-icon-build);
}
.jp-CaretDownEmptyIcon {
  background-image: var(--jp-icon-caret-down-empty);
}
.jp-CaretDownEmptyThinIcon {
  background-image: var(--jp-icon-caret-down-empty-thin);
}
.jp-CaretDownIcon {
  background-image: var(--jp-icon-caret-down);
}
.jp-CaretLeftIcon {
  background-image: var(--jp-icon-caret-left);
}
.jp-CaretRightIcon {
  background-image: var(--jp-icon-caret-right);
}
.jp-CaretUpEmptyThinIcon {
  background-image: var(--jp-icon-caret-up-empty-thin);
}
.jp-CaretUpIcon {
  background-image: var(--jp-icon-caret-up);
}
.jp-CaseSensitiveIcon {
  background-image: var(--jp-icon-case-sensitive);
}
.jp-CheckIcon {
  background-image: var(--jp-icon-check);
}
.jp-CircleEmptyIcon {
  background-image: var(--jp-icon-circle-empty);
}
.jp-CircleIcon {
  background-image: var(--jp-icon-circle);
}
.jp-ClearIcon {
  background-image: var(--jp-icon-clear);
}
.jp-CloseIcon {
  background-image: var(--jp-icon-close);
}
.jp-ConsoleIcon {
  background-image: var(--jp-icon-console);
}
.jp-CopyIcon {
  background-image: var(--jp-icon-copy);
}
.jp-CutIcon {
  background-image: var(--jp-icon-cut);
}
.jp-DownloadIcon {
  background-image: var(--jp-icon-download);
}
.jp-EditIcon {
  background-image: var(--jp-icon-edit);
}
.jp-EllipsesIcon {
  background-image: var(--jp-icon-ellipses);
}
.jp-ExtensionIcon {
  background-image: var(--jp-icon-extension);
}
.jp-FastForwardIcon {
  background-image: var(--jp-icon-fast-forward);
}
.jp-FileIcon {
  background-image: var(--jp-icon-file);
}
.jp-FileUploadIcon {
  background-image: var(--jp-icon-file-upload);
}
.jp-FilterListIcon {
  background-image: var(--jp-icon-filter-list);
}
.jp-FolderIcon {
  background-image: var(--jp-icon-folder);
}
.jp-Html5Icon {
  background-image: var(--jp-icon-html5);
}
.jp-ImageIcon {
  background-image: var(--jp-icon-image);
}
.jp-InspectorIcon {
  background-image: var(--jp-icon-inspector);
}
.jp-JsonIcon {
  background-image: var(--jp-icon-json);
}
.jp-JupyterFaviconIcon {
  background-image: var(--jp-icon-jupyter-favicon);
}
.jp-JupyterIcon {
  background-image: var(--jp-icon-jupyter);
}
.jp-JupyterlabWordmarkIcon {
  background-image: var(--jp-icon-jupyterlab-wordmark);
}
.jp-KernelIcon {
  background-image: var(--jp-icon-kernel);
}
.jp-KeyboardIcon {
  background-image: var(--jp-icon-keyboard);
}
.jp-LauncherIcon {
  background-image: var(--jp-icon-launcher);
}
.jp-LineFormIcon {
  background-image: var(--jp-icon-line-form);
}
.jp-LinkIcon {
  background-image: var(--jp-icon-link);
}
.jp-ListIcon {
  background-image: var(--jp-icon-list);
}
.jp-ListingsInfoIcon {
  background-image: var(--jp-icon-listings-info);
}
.jp-MarkdownIcon {
  background-image: var(--jp-icon-markdown);
}
.jp-NewFolderIcon {
  background-image: var(--jp-icon-new-folder);
}
.jp-NotTrustedIcon {
  background-image: var(--jp-icon-not-trusted);
}
.jp-NotebookIcon {
  background-image: var(--jp-icon-notebook);
}
.jp-PaletteIcon {
  background-image: var(--jp-icon-palette);
}
.jp-PasteIcon {
  background-image: var(--jp-icon-paste);
}
.jp-PythonIcon {
  background-image: var(--jp-icon-python);
}
.jp-RKernelIcon {
  background-image: var(--jp-icon-r-kernel);
}
.jp-ReactIcon {
  background-image: var(--jp-icon-react);
}
.jp-RefreshIcon {
  background-image: var(--jp-icon-refresh);
}
.jp-RegexIcon {
  background-image: var(--jp-icon-regex);
}
.jp-RunIcon {
  background-image: var(--jp-icon-run);
}
.jp-RunningIcon {
  background-image: var(--jp-icon-running);
}
.jp-SaveIcon {
  background-image: var(--jp-icon-save);
}
.jp-SearchIcon {
  background-image: var(--jp-icon-search);
}
.jp-SettingsIcon {
  background-image: var(--jp-icon-settings);
}
.jp-SpreadsheetIcon {
  background-image: var(--jp-icon-spreadsheet);
}
.jp-StopIcon {
  background-image: var(--jp-icon-stop);
}
.jp-TabIcon {
  background-image: var(--jp-icon-tab);
}
.jp-TerminalIcon {
  background-image: var(--jp-icon-terminal);
}
.jp-TextEditorIcon {
  background-image: var(--jp-icon-text-editor);
}
.jp-TrustedIcon {
  background-image: var(--jp-icon-trusted);
}
.jp-UndoIcon {
  background-image: var(--jp-icon-undo);
}
.jp-VegaIcon {
  background-image: var(--jp-icon-vega);
}
.jp-YamlIcon {
  background-image: var(--jp-icon-yaml);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

:root {
  --jp-icon-search-white: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjEsMTAuOWgtMC43bC0wLjItMC4yYzAuOC0wLjksMS4zLTIuMiwxLjMtMy41YzAtMy0yLjQtNS40LTUuNC01LjRTMS44LDQuMiwxLjgsNy4xczIuNCw1LjQsNS40LDUuNCBjMS4zLDAsMi41LTAuNSwzLjUtMS4zbDAuMiwwLjJ2MC43bDQuMSw0LjFsMS4yLTEuMkwxMi4xLDEwLjl6IE03LjEsMTAuOWMtMi4xLDAtMy43LTEuNy0zLjctMy43czEuNy0zLjcsMy43LTMuN3MzLjcsMS43LDMuNywzLjcgUzkuMiwxMC45LDcuMSwxMC45eiIvPgogIDwvZz4KPC9zdmc+Cg==);
}

.jp-Icon,
.jp-MaterialIcon {
  background-position: center;
  background-repeat: no-repeat;
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-cover {
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

/**
 * (DEPRECATED) Support for specific CSS icon sizes
 */

.jp-Icon-16 {
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-18 {
  background-size: 18px;
  min-width: 18px;
  min-height: 18px;
}

.jp-Icon-20 {
  background-size: 20px;
  min-width: 20px;
  min-height: 20px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for icons as inline SVG HTMLElements
 */

/* recolor the primary elements of an icon */
.jp-icon0[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon1[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon2[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon3[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}
/* recolor the accent elements of an icon */
.jp-icon-accent0[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-accent1[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-accent2[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-accent3[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-accent4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-accent0[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-accent1[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-accent2[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-accent3[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-accent4[stroke] {
  stroke: var(--jp-layout-color4);
}
/* set the color of an icon to transparent */
.jp-icon-none[fill] {
  fill: none;
}

.jp-icon-none[stroke] {
  stroke: none;
}
/* brand icon colors. Same for light and dark */
.jp-icon-brand0[fill] {
  fill: var(--jp-brand-color0);
}
.jp-icon-brand1[fill] {
  fill: var(--jp-brand-color1);
}
.jp-icon-brand2[fill] {
  fill: var(--jp-brand-color2);
}
.jp-icon-brand3[fill] {
  fill: var(--jp-brand-color3);
}
.jp-icon-brand4[fill] {
  fill: var(--jp-brand-color4);
}

.jp-icon-brand0[stroke] {
  stroke: var(--jp-brand-color0);
}
.jp-icon-brand1[stroke] {
  stroke: var(--jp-brand-color1);
}
.jp-icon-brand2[stroke] {
  stroke: var(--jp-brand-color2);
}
.jp-icon-brand3[stroke] {
  stroke: var(--jp-brand-color3);
}
.jp-icon-brand4[stroke] {
  stroke: var(--jp-brand-color4);
}
/* warn icon colors. Same for light and dark */
.jp-icon-warn0[fill] {
  fill: var(--jp-warn-color0);
}
.jp-icon-warn1[fill] {
  fill: var(--jp-warn-color1);
}
.jp-icon-warn2[fill] {
  fill: var(--jp-warn-color2);
}
.jp-icon-warn3[fill] {
  fill: var(--jp-warn-color3);
}

.jp-icon-warn0[stroke] {
  stroke: var(--jp-warn-color0);
}
.jp-icon-warn1[stroke] {
  stroke: var(--jp-warn-color1);
}
.jp-icon-warn2[stroke] {
  stroke: var(--jp-warn-color2);
}
.jp-icon-warn3[stroke] {
  stroke: var(--jp-warn-color3);
}
/* icon colors that contrast well with each other and most backgrounds */
.jp-icon-contrast0[fill] {
  fill: var(--jp-icon-contrast-color0);
}
.jp-icon-contrast1[fill] {
  fill: var(--jp-icon-contrast-color1);
}
.jp-icon-contrast2[fill] {
  fill: var(--jp-icon-contrast-color2);
}
.jp-icon-contrast3[fill] {
  fill: var(--jp-icon-contrast-color3);
}

.jp-icon-contrast0[stroke] {
  stroke: var(--jp-icon-contrast-color0);
}
.jp-icon-contrast1[stroke] {
  stroke: var(--jp-icon-contrast-color1);
}
.jp-icon-contrast2[stroke] {
  stroke: var(--jp-icon-contrast-color2);
}
.jp-icon-contrast3[stroke] {
  stroke: var(--jp-icon-contrast-color3);
}

/* CSS for icons in selected items in the settings editor */
#setting-editor .jp-PluginList .jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}
#setting-editor
  .jp-PluginList
  .jp-mod-selected
  .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* CSS for icons in selected filebrowser listing items */
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* CSS for icons in selected tabs in the sidebar tab manager */
#tab-manager .lm-TabBar-tab.jp-mod-active .jp-icon-selectable[fill] {
  fill: #fff;
}

#tab-manager .lm-TabBar-tab.jp-mod-active .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}
#tab-manager
  .lm-TabBar-tab.jp-mod-active
  .jp-icon-hover
  :hover
  .jp-icon-selectable[fill] {
  fill: var(--jp-brand-color1);
}

#tab-manager
  .lm-TabBar-tab.jp-mod-active
  .jp-icon-hover
  :hover
  .jp-icon-selectable-inverse[fill] {
  fill: #fff;
}

/**
 * TODO: come up with non css-hack solution for showing the busy icon on top
 *  of the close icon
 * CSS for complex behavior of close icon of tabs in the sidebar tab manager
 */
#tab-manager
  .lm-TabBar-tab.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon3[fill] {
  fill: none;
}
#tab-manager
  .lm-TabBar-tab.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: var(--jp-inverse-layout-color3);
}

#tab-manager
  .lm-TabBar-tab.jp-mod-dirty.jp-mod-active
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: #fff;
}

/**
* TODO: come up with non css-hack solution for showing the busy icon on top
*  of the close icon
* CSS for complex behavior of close icon of tabs in the main area tabbar
*/
.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon3[fill] {
  fill: none;
}
.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: var(--jp-inverse-layout-color3);
}

/* CSS for icons in status bar */
#jp-main-statusbar .jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}

#jp-main-statusbar .jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}
/* special handling for splash icon CSS. While the theme CSS reloads during
   splash, the splash icon can loose theming. To prevent that, we set a
   default for its color variable */
:root {
  --jp-warn-color0: var(--md-orange-700);
}

/* not sure what to do with this one, used in filebrowser listing */
.jp-DragIcon {
  margin-right: 4px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for alt colors for icons as inline SVG HTMLElements
 */

/* alt recolor the primary elements of an icon */
.jp-icon-alt .jp-icon0[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-alt .jp-icon1[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-alt .jp-icon2[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-alt .jp-icon3[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-alt .jp-icon4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-alt .jp-icon0[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-alt .jp-icon1[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-alt .jp-icon2[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-alt .jp-icon3[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-alt .jp-icon4[stroke] {
  stroke: var(--jp-layout-color4);
}

/* alt recolor the accent elements of an icon */
.jp-icon-alt .jp-icon-accent0[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-alt .jp-icon-accent1[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-alt .jp-icon-accent2[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-alt .jp-icon-accent3[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-alt .jp-icon-accent4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-alt .jp-icon-accent0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-alt .jp-icon-accent1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-alt .jp-icon-accent2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-alt .jp-icon-accent3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-alt .jp-icon-accent4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-icon-hoverShow:not(:hover) svg {
  display: none !important;
}

/**
 * Support for hover colors for icons as inline SVG HTMLElements
 */

/**
 * regular colors
 */

/* recolor the primary elements of an icon */
.jp-icon-hover :hover .jp-icon0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-hover :hover .jp-icon1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-hover :hover .jp-icon2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-hover :hover .jp-icon3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-hover :hover .jp-icon4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-hover :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-hover :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-hover :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-hover :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/* recolor the accent elements of an icon */
.jp-icon-hover :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-hover :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-hover :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-hover :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-hover :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-hover :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-hover :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-hover :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-hover :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* set the color of an icon to transparent */
.jp-icon-hover :hover .jp-icon-none-hover[fill] {
  fill: none;
}

.jp-icon-hover :hover .jp-icon-none-hover[stroke] {
  stroke: none;
}

/**
 * inverse colors
 */

/* inverse recolor the primary elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[fill] {
  fill: var(--jp-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[fill] {
  fill: var(--jp-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[fill] {
  fill: var(--jp-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[fill] {
  fill: var(--jp-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* inverse recolor the accent elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* Sibling imports */

/* Override Blueprint's _reset.scss styles */
html {
  box-sizing: unset;
}

*,
*::before,
*::after {
  box-sizing: unset;
}

body {
  color: unset;
  font-family: var(--jp-ui-font-family);
}

p {
  margin-top: unset;
  margin-bottom: unset;
}

small {
  font-size: unset;
}

strong {
  font-weight: unset;
}

/* Override Blueprint's _typography.scss styles */
a {
  text-decoration: unset;
  color: unset;
}
a:hover {
  text-decoration: unset;
  color: unset;
}

/* Override Blueprint's _accessibility.scss styles */
:focus {
  outline: unset;
  outline-offset: unset;
  -moz-outline-radius: unset;
}

/* Styles for ui-components */
.jp-Button {
  border-radius: var(--jp-border-radius);
  padding: 0px 12px;
  font-size: var(--jp-ui-font-size1);
}

/* Use our own theme for hover styles */
button.jp-Button.bp3-button.bp3-minimal:hover {
  background-color: var(--jp-layout-color2);
}
.jp-Button.minimal {
  color: unset !important;
}

.jp-Button.jp-ToolbarButtonComponent {
  text-transform: none;
}

.jp-InputGroup input {
  box-sizing: border-box;
  border-radius: 0;
  background-color: transparent;
  color: var(--jp-ui-font-color0);
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.jp-InputGroup input:focus {
  box-shadow: inset 0 0 0 var(--jp-border-width)
      var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.jp-InputGroup input::placeholder,
input::placeholder {
  color: var(--jp-ui-font-color3);
}

.jp-BPIcon {
  display: inline-block;
  vertical-align: middle;
  margin: auto;
}

/* Stop blueprint futzing with our icon fills */
.bp3-icon.jp-BPIcon > svg:not([fill]) {
  fill: var(--jp-inverse-layout-color3);
}

.jp-InputGroupAction {
  padding: 6px;
}

.jp-HTMLSelect.jp-DefaultStyle select {
  background-color: initial;
  border: none;
  border-radius: 0;
  box-shadow: none;
  color: var(--jp-ui-font-color0);
  display: block;
  font-size: var(--jp-ui-font-size1);
  height: 24px;
  line-height: 14px;
  padding: 0 25px 0 10px;
  text-align: left;
  -moz-appearance: none;
  -webkit-appearance: none;
}

/* Use our own theme for hover and option styles */
.jp-HTMLSelect.jp-DefaultStyle select:hover,
.jp-HTMLSelect.jp-DefaultStyle select > option {
  background-color: var(--jp-layout-color2);
  color: var(--jp-ui-font-color0);
}
select {
  box-sizing: border-box;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapse {
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-top: 1px solid var(--jp-border-color2);
  border-bottom: 1px solid var(--jp-border-color2);
}

.jp-Collapse-header {
  padding: 1px 12px;
  color: var(--jp-ui-font-color1);
  background-color: var(--jp-layout-color1);
  font-size: var(--jp-ui-font-size2);
}

.jp-Collapse-header:hover {
  background-color: var(--jp-layout-color2);
}

.jp-Collapse-contents {
  padding: 0px 12px 0px 12px;
  background-color: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  overflow: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-commandpalette-search-height: 28px;
}

/*-----------------------------------------------------------------------------
| Overall styles
|----------------------------------------------------------------------------*/

.lm-CommandPalette {
  padding-bottom: 0px;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Search
|----------------------------------------------------------------------------*/

.lm-CommandPalette-search {
  padding: 4px;
  background-color: var(--jp-layout-color1);
  z-index: 2;
}

.lm-CommandPalette-wrapper {
  overflow: overlay;
  padding: 0px 9px;
  background-color: var(--jp-input-active-background);
  height: 30px;
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.lm-CommandPalette.lm-mod-focused .lm-CommandPalette-wrapper {
  box-shadow: inset 0 0 0 1px var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.lm-CommandPalette-wrapper::after {
  content: ' ';
  color: white;
  background-color: var(--jp-brand-color1);
  position: absolute;
  top: 4px;
  right: 4px;
  height: 30px;
  width: 10px;
  padding: 0px 10px;
  background-image: var(--jp-icon-search-white);
  background-size: 20px;
  background-repeat: no-repeat;
  background-position: center;
}

.lm-CommandPalette-input {
  background: transparent;
  width: calc(100% - 18px);
  float: left;
  border: none;
  outline: none;
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  line-height: var(--jp-private-commandpalette-search-height);
}

.lm-CommandPalette-input::-webkit-input-placeholder,
.lm-CommandPalette-input::-moz-placeholder,
.lm-CommandPalette-input:-ms-input-placeholder {
  color: var(--jp-ui-font-color3);
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Results
|----------------------------------------------------------------------------*/

.lm-CommandPalette-header:first-child {
  margin-top: 0px;
}

.lm-CommandPalette-header {
  border-bottom: solid var(--jp-border-width) var(--jp-border-color2);
  color: var(--jp-ui-font-color1);
  cursor: pointer;
  display: flex;
  font-size: var(--jp-ui-font-size0);
  font-weight: 600;
  letter-spacing: 1px;
  margin-top: 8px;
  padding: 8px 0 8px 12px;
  text-transform: uppercase;
}

.lm-CommandPalette-header.lm-mod-active {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-header > mark {
  background-color: transparent;
  font-weight: bold;
  color: var(--jp-ui-font-color1);
}

.lm-CommandPalette-item {
  padding: 4px 12px 4px 4px;
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
  font-weight: 400;
  display: flex;
}

.lm-CommandPalette-item.lm-mod-disabled {
  color: var(--jp-ui-font-color3);
}

.lm-CommandPalette-item.lm-mod-active {
  background: var(--jp-layout-color3);
}

.lm-CommandPalette-item.lm-mod-active:hover:not(.lm-mod-disabled) {
  background: var(--jp-layout-color4);
}

.lm-CommandPalette-item:hover:not(.lm-mod-active):not(.lm-mod-disabled) {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-itemContent {
  overflow: hidden;
}

.lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-font-color0);
  background-color: transparent;
  font-weight: bold;
}

.lm-CommandPalette-item.lm-mod-disabled mark {
  color: var(--jp-ui-font-color3);
}

.lm-CommandPalette-item .lm-CommandPalette-itemIcon {
  margin: 0 4px 0 0;
  position: relative;
  width: 16px;
  top: 2px;
  flex: 0 0 auto;
}

.lm-CommandPalette-item.lm-mod-disabled .lm-CommandPalette-itemIcon {
  opacity: 0.4;
}

.lm-CommandPalette-item .lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}

.lm-CommandPalette-itemCaption {
  display: none;
}

.lm-CommandPalette-content {
  background-color: var(--jp-layout-color1);
}

.lm-CommandPalette-content:empty:after {
  content: 'No results';
  margin: auto;
  margin-top: 20px;
  width: 100px;
  display: block;
  font-size: var(--jp-ui-font-size2);
  font-family: var(--jp-ui-font-family);
  font-weight: lighter;
}

.lm-CommandPalette-emptyMessage {
  text-align: center;
  margin-top: 24px;
  line-height: 1.32;
  padding: 0px 8px;
  color: var(--jp-content-font-color3);
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Dialog {
  position: absolute;
  z-index: 10000;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  top: 0px;
  left: 0px;
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-dialog-background);
}

.jp-Dialog-content {
  display: flex;
  flex-direction: column;
  margin-left: auto;
  margin-right: auto;
  background: var(--jp-layout-color1);
  padding: 24px;
  padding-bottom: 12px;
  min-width: 300px;
  min-height: 150px;
  max-width: 1000px;
  max-height: 500px;
  box-sizing: border-box;
  box-shadow: var(--jp-elevation-z20);
  word-wrap: break-word;
  border-radius: var(--jp-border-radius);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color1);
}

.jp-Dialog-button {
  overflow: visible;
}

button.jp-Dialog-button:focus {
  outline: 1px solid var(--jp-brand-color1);
  outline-offset: 4px;
  -moz-outline-radius: 0px;
}

button.jp-Dialog-button:focus::-moz-focus-inner {
  border: 0;
}

.jp-Dialog-header {
  flex: 0 0 auto;
  padding-bottom: 12px;
  font-size: var(--jp-ui-font-size3);
  font-weight: 400;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-body {
  display: flex;
  flex-direction: column;
  flex: 1 1 auto;
  font-size: var(--jp-ui-font-size1);
  background: var(--jp-layout-color1);
  overflow: auto;
}

.jp-Dialog-footer {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  flex: 0 0 auto;
  margin-left: -12px;
  margin-right: -12px;
  padding: 12px;
}

.jp-Dialog-title {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.jp-Dialog-body > .jp-select-wrapper {
  width: 100%;
}

.jp-Dialog-body > button {
  padding: 0px 16px;
}

.jp-Dialog-body > label {
  line-height: 1.4;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-button.jp-mod-styled:not(:last-child) {
  margin-right: 12px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-HoverBox {
  position: fixed;
}

.jp-HoverBox.jp-mod-outofview {
  display: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-IFrame {
  width: 100%;
  height: 100%;
}

.jp-IFrame > iframe {
  border: none;
}

/*
When drag events occur, `p-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-IFrame {
  position: relative;
}

body.lm-mod-override-cursor .jp-IFrame:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MainAreaWidget > :focus {
  outline: none;
}

/**
 * google-material-color v1.2.6
 * https://github.com/danlevan/google-material-color
 */
:root {
  --md-red-50: #ffebee;
  --md-red-100: #ffcdd2;
  --md-red-200: #ef9a9a;
  --md-red-300: #e57373;
  --md-red-400: #ef5350;
  --md-red-500: #f44336;
  --md-red-600: #e53935;
  --md-red-700: #d32f2f;
  --md-red-800: #c62828;
  --md-red-900: #b71c1c;
  --md-red-A100: #ff8a80;
  --md-red-A200: #ff5252;
  --md-red-A400: #ff1744;
  --md-red-A700: #d50000;

  --md-pink-50: #fce4ec;
  --md-pink-100: #f8bbd0;
  --md-pink-200: #f48fb1;
  --md-pink-300: #f06292;
  --md-pink-400: #ec407a;
  --md-pink-500: #e91e63;
  --md-pink-600: #d81b60;
  --md-pink-700: #c2185b;
  --md-pink-800: #ad1457;
  --md-pink-900: #880e4f;
  --md-pink-A100: #ff80ab;
  --md-pink-A200: #ff4081;
  --md-pink-A400: #f50057;
  --md-pink-A700: #c51162;

  --md-purple-50: #f3e5f5;
  --md-purple-100: #e1bee7;
  --md-purple-200: #ce93d8;
  --md-purple-300: #ba68c8;
  --md-purple-400: #ab47bc;
  --md-purple-500: #9c27b0;
  --md-purple-600: #8e24aa;
  --md-purple-700: #7b1fa2;
  --md-purple-800: #6a1b9a;
  --md-purple-900: #4a148c;
  --md-purple-A100: #ea80fc;
  --md-purple-A200: #e040fb;
  --md-purple-A400: #d500f9;
  --md-purple-A700: #aa00ff;

  --md-deep-purple-50: #ede7f6;
  --md-deep-purple-100: #d1c4e9;
  --md-deep-purple-200: #b39ddb;
  --md-deep-purple-300: #9575cd;
  --md-deep-purple-400: #7e57c2;
  --md-deep-purple-500: #673ab7;
  --md-deep-purple-600: #5e35b1;
  --md-deep-purple-700: #512da8;
  --md-deep-purple-800: #4527a0;
  --md-deep-purple-900: #311b92;
  --md-deep-purple-A100: #b388ff;
  --md-deep-purple-A200: #7c4dff;
  --md-deep-purple-A400: #651fff;
  --md-deep-purple-A700: #6200ea;

  --md-indigo-50: #e8eaf6;
  --md-indigo-100: #c5cae9;
  --md-indigo-200: #9fa8da;
  --md-indigo-300: #7986cb;
  --md-indigo-400: #5c6bc0;
  --md-indigo-500: #3f51b5;
  --md-indigo-600: #3949ab;
  --md-indigo-700: #303f9f;
  --md-indigo-800: #283593;
  --md-indigo-900: #1a237e;
  --md-indigo-A100: #8c9eff;
  --md-indigo-A200: #536dfe;
  --md-indigo-A400: #3d5afe;
  --md-indigo-A700: #304ffe;

  --md-blue-50: #e3f2fd;
  --md-blue-100: #bbdefb;
  --md-blue-200: #90caf9;
  --md-blue-300: #64b5f6;
  --md-blue-400: #42a5f5;
  --md-blue-500: #2196f3;
  --md-blue-600: #1e88e5;
  --md-blue-700: #1976d2;
  --md-blue-800: #1565c0;
  --md-blue-900: #0d47a1;
  --md-blue-A100: #82b1ff;
  --md-blue-A200: #448aff;
  --md-blue-A400: #2979ff;
  --md-blue-A700: #2962ff;

  --md-light-blue-50: #e1f5fe;
  --md-light-blue-100: #b3e5fc;
  --md-light-blue-200: #81d4fa;
  --md-light-blue-300: #4fc3f7;
  --md-light-blue-400: #29b6f6;
  --md-light-blue-500: #03a9f4;
  --md-light-blue-600: #039be5;
  --md-light-blue-700: #0288d1;
  --md-light-blue-800: #0277bd;
  --md-light-blue-900: #01579b;
  --md-light-blue-A100: #80d8ff;
  --md-light-blue-A200: #40c4ff;
  --md-light-blue-A400: #00b0ff;
  --md-light-blue-A700: #0091ea;

  --md-cyan-50: #e0f7fa;
  --md-cyan-100: #b2ebf2;
  --md-cyan-200: #80deea;
  --md-cyan-300: #4dd0e1;
  --md-cyan-400: #26c6da;
  --md-cyan-500: #00bcd4;
  --md-cyan-600: #00acc1;
  --md-cyan-700: #0097a7;
  --md-cyan-800: #00838f;
  --md-cyan-900: #006064;
  --md-cyan-A100: #84ffff;
  --md-cyan-A200: #18ffff;
  --md-cyan-A400: #00e5ff;
  --md-cyan-A700: #00b8d4;

  --md-teal-50: #e0f2f1;
  --md-teal-100: #b2dfdb;
  --md-teal-200: #80cbc4;
  --md-teal-300: #4db6ac;
  --md-teal-400: #26a69a;
  --md-teal-500: #009688;
  --md-teal-600: #00897b;
  --md-teal-700: #00796b;
  --md-teal-800: #00695c;
  --md-teal-900: #004d40;
  --md-teal-A100: #a7ffeb;
  --md-teal-A200: #64ffda;
  --md-teal-A400: #1de9b6;
  --md-teal-A700: #00bfa5;

  --md-green-50: #e8f5e9;
  --md-green-100: #c8e6c9;
  --md-green-200: #a5d6a7;
  --md-green-300: #81c784;
  --md-green-400: #66bb6a;
  --md-green-500: #4caf50;
  --md-green-600: #43a047;
  --md-green-700: #388e3c;
  --md-green-800: #2e7d32;
  --md-green-900: #1b5e20;
  --md-green-A100: #b9f6ca;
  --md-green-A200: #69f0ae;
  --md-green-A400: #00e676;
  --md-green-A700: #00c853;

  --md-light-green-50: #f1f8e9;
  --md-light-green-100: #dcedc8;
  --md-light-green-200: #c5e1a5;
  --md-light-green-300: #aed581;
  --md-light-green-400: #9ccc65;
  --md-light-green-500: #8bc34a;
  --md-light-green-600: #7cb342;
  --md-light-green-700: #689f38;
  --md-light-green-800: #558b2f;
  --md-light-green-900: #33691e;
  --md-light-green-A100: #ccff90;
  --md-light-green-A200: #b2ff59;
  --md-light-green-A400: #76ff03;
  --md-light-green-A700: #64dd17;

  --md-lime-50: #f9fbe7;
  --md-lime-100: #f0f4c3;
  --md-lime-200: #e6ee9c;
  --md-lime-300: #dce775;
  --md-lime-400: #d4e157;
  --md-lime-500: #cddc39;
  --md-lime-600: #c0ca33;
  --md-lime-700: #afb42b;
  --md-lime-800: #9e9d24;
  --md-lime-900: #827717;
  --md-lime-A100: #f4ff81;
  --md-lime-A200: #eeff41;
  --md-lime-A400: #c6ff00;
  --md-lime-A700: #aeea00;

  --md-yellow-50: #fffde7;
  --md-yellow-100: #fff9c4;
  --md-yellow-200: #fff59d;
  --md-yellow-300: #fff176;
  --md-yellow-400: #ffee58;
  --md-yellow-500: #ffeb3b;
  --md-yellow-600: #fdd835;
  --md-yellow-700: #fbc02d;
  --md-yellow-800: #f9a825;
  --md-yellow-900: #f57f17;
  --md-yellow-A100: #ffff8d;
  --md-yellow-A200: #ffff00;
  --md-yellow-A400: #ffea00;
  --md-yellow-A700: #ffd600;

  --md-amber-50: #fff8e1;
  --md-amber-100: #ffecb3;
  --md-amber-200: #ffe082;
  --md-amber-300: #ffd54f;
  --md-amber-400: #ffca28;
  --md-amber-500: #ffc107;
  --md-amber-600: #ffb300;
  --md-amber-700: #ffa000;
  --md-amber-800: #ff8f00;
  --md-amber-900: #ff6f00;
  --md-amber-A100: #ffe57f;
  --md-amber-A200: #ffd740;
  --md-amber-A400: #ffc400;
  --md-amber-A700: #ffab00;

  --md-orange-50: #fff3e0;
  --md-orange-100: #ffe0b2;
  --md-orange-200: #ffcc80;
  --md-orange-300: #ffb74d;
  --md-orange-400: #ffa726;
  --md-orange-500: #ff9800;
  --md-orange-600: #fb8c00;
  --md-orange-700: #f57c00;
  --md-orange-800: #ef6c00;
  --md-orange-900: #e65100;
  --md-orange-A100: #ffd180;
  --md-orange-A200: #ffab40;
  --md-orange-A400: #ff9100;
  --md-orange-A700: #ff6d00;

  --md-deep-orange-50: #fbe9e7;
  --md-deep-orange-100: #ffccbc;
  --md-deep-orange-200: #ffab91;
  --md-deep-orange-300: #ff8a65;
  --md-deep-orange-400: #ff7043;
  --md-deep-orange-500: #ff5722;
  --md-deep-orange-600: #f4511e;
  --md-deep-orange-700: #e64a19;
  --md-deep-orange-800: #d84315;
  --md-deep-orange-900: #bf360c;
  --md-deep-orange-A100: #ff9e80;
  --md-deep-orange-A200: #ff6e40;
  --md-deep-orange-A400: #ff3d00;
  --md-deep-orange-A700: #dd2c00;

  --md-brown-50: #efebe9;
  --md-brown-100: #d7ccc8;
  --md-brown-200: #bcaaa4;
  --md-brown-300: #a1887f;
  --md-brown-400: #8d6e63;
  --md-brown-500: #795548;
  --md-brown-600: #6d4c41;
  --md-brown-700: #5d4037;
  --md-brown-800: #4e342e;
  --md-brown-900: #3e2723;

  --md-grey-50: #fafafa;
  --md-grey-100: #f5f5f5;
  --md-grey-200: #eeeeee;
  --md-grey-300: #e0e0e0;
  --md-grey-400: #bdbdbd;
  --md-grey-500: #9e9e9e;
  --md-grey-600: #757575;
  --md-grey-700: #616161;
  --md-grey-800: #424242;
  --md-grey-900: #212121;

  --md-blue-grey-50: #eceff1;
  --md-blue-grey-100: #cfd8dc;
  --md-blue-grey-200: #b0bec5;
  --md-blue-grey-300: #90a4ae;
  --md-blue-grey-400: #78909c;
  --md-blue-grey-500: #607d8b;
  --md-blue-grey-600: #546e7a;
  --md-blue-grey-700: #455a64;
  --md-blue-grey-800: #37474f;
  --md-blue-grey-900: #263238;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Spinner {
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 10;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-layout-color0);
  outline: none;
}

.jp-SpinnerContent {
  font-size: 10px;
  margin: 50px auto;
  text-indent: -9999em;
  width: 3em;
  height: 3em;
  border-radius: 50%;
  background: var(--jp-brand-color3);
  background: linear-gradient(
    to right,
    #f37626 10%,
    rgba(255, 255, 255, 0) 42%
  );
  position: relative;
  animation: load3 1s infinite linear, fadeIn 1s;
}

.jp-SpinnerContent:before {
  width: 50%;
  height: 50%;
  background: #f37626;
  border-radius: 100% 0 0 0;
  position: absolute;
  top: 0;
  left: 0;
  content: '';
}

.jp-SpinnerContent:after {
  background: var(--jp-layout-color0);
  width: 75%;
  height: 75%;
  border-radius: 50%;
  content: '';
  margin: auto;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

@keyframes load3 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

button.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: none;
  box-sizing: border-box;
  text-align: center;
  line-height: 32px;
  height: 32px;
  padding: 0px 12px;
  letter-spacing: 0.8px;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input.jp-mod-styled {
  background: var(--jp-input-background);
  height: 28px;
  box-sizing: border-box;
  border: var(--jp-border-width) solid var(--jp-border-color1);
  padding-left: 7px;
  padding-right: 7px;
  font-size: var(--jp-ui-font-size2);
  color: var(--jp-ui-font-color0);
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input.jp-mod-styled:focus {
  border: var(--jp-border-width) solid var(--md-blue-500);
  box-shadow: inset 0 0 4px var(--md-blue-300);
}

.jp-select-wrapper {
  display: flex;
  position: relative;
  flex-direction: column;
  padding: 1px;
  background-color: var(--jp-layout-color1);
  height: 28px;
  box-sizing: border-box;
  margin-bottom: 12px;
}

.jp-select-wrapper.jp-mod-focused select.jp-mod-styled {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-input-active-background);
}

select.jp-mod-styled:hover {
  background-color: var(--jp-layout-color1);
  cursor: pointer;
  color: var(--jp-ui-font-color0);
  background-color: var(--jp-input-hover-background);
  box-shadow: inset 0 0px 1px rgba(0, 0, 0, 0.5);
}

select.jp-mod-styled {
  flex: 1 1 auto;
  height: 32px;
  width: 100%;
  font-size: var(--jp-ui-font-size2);
  background: var(--jp-input-background);
  color: var(--jp-ui-font-color0);
  padding: 0 25px 0 8px;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0px;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

:root {
  --jp-private-toolbar-height: calc(
    28px + var(--jp-border-width)
  ); /* leave 28px for content */
}

.jp-Toolbar {
  color: var(--jp-ui-font-color1);
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  border-bottom: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  box-shadow: var(--jp-toolbar-box-shadow);
  background: var(--jp-toolbar-background);
  min-height: var(--jp-toolbar-micro-height);
  padding: 2px;
  z-index: 1;
}

/* Toolbar items */

.jp-Toolbar > .jp-Toolbar-item.jp-Toolbar-spacer {
  flex-grow: 1;
  flex-shrink: 1;
}

.jp-Toolbar-item.jp-Toolbar-kernelStatus {
  display: inline-block;
  width: 32px;
  background-repeat: no-repeat;
  background-position: center;
  background-size: 16px;
}

.jp-Toolbar > .jp-Toolbar-item {
  flex: 0 0 auto;
  display: flex;
  padding-left: 1px;
  padding-right: 1px;
  font-size: var(--jp-ui-font-size1);
  line-height: var(--jp-private-toolbar-height);
  height: 100%;
}

/* Toolbar buttons */

/* This is the div we use to wrap the react component into a Widget */
div.jp-ToolbarButton {
  color: transparent;
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0px;
  margin: 0px;
}

button.jp-ToolbarButtonComponent {
  background: var(--jp-layout-color1);
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0px 6px;
  margin: 0px;
  height: 24px;
  border-radius: var(--jp-border-radius);
  display: flex;
  align-items: center;
  text-align: center;
  font-size: 14px;
  min-width: unset;
  min-height: unset;
}

button.jp-ToolbarButtonComponent:disabled {
  opacity: 0.4;
}

button.jp-ToolbarButtonComponent span {
  padding: 0px;
  flex: 0 0 auto;
}

button.jp-ToolbarButtonComponent .jp-ToolbarButtonComponent-label {
  font-size: var(--jp-ui-font-size1);
  line-height: 100%;
  padding-left: 2px;
  color: var(--jp-ui-font-color1);
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ body.p-mod-override-cursor *, /* </DEPRECATED> */
body.lm-mod-override-cursor * {
  cursor: inherit !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-JSONEditor {
  display: flex;
  flex-direction: column;
  width: 100%;
}

.jp-JSONEditor-host {
  flex: 1 1 auto;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0px;
  background: var(--jp-layout-color0);
  min-height: 50px;
  padding: 1px;
}

.jp-JSONEditor.jp-mod-error .jp-JSONEditor-host {
  border-color: red;
  outline-color: red;
}

.jp-JSONEditor-header {
  display: flex;
  flex: 1 0 auto;
  padding: 0 0 0 12px;
}

.jp-JSONEditor-header label {
  flex: 0 0 auto;
}

.jp-JSONEditor-commitButton {
  height: 16px;
  width: 16px;
  background-size: 18px;
  background-repeat: no-repeat;
  background-position: center;
}

.jp-JSONEditor-host.jp-mod-focused {
  background-color: var(--jp-input-active-background);
  border: 1px solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

.jp-Editor.jp-mod-dropTarget {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* BASICS */

.CodeMirror {
  /* Set height, width, borders, and global font properties here */
  font-family: monospace;
  height: 300px;
  color: black;
  direction: ltr;
}

/* PADDING */

.CodeMirror-lines {
  padding: 4px 0; /* Vertical padding around content */
}
.CodeMirror pre.CodeMirror-line,
.CodeMirror pre.CodeMirror-line-like {
  padding: 0 4px; /* Horizontal padding of content */
}

.CodeMirror-scrollbar-filler, .CodeMirror-gutter-filler {
  background-color: white; /* The little square between H and V scrollbars */
}

/* GUTTER */

.CodeMirror-gutters {
  border-right: 1px solid #ddd;
  background-color: #f7f7f7;
  white-space: nowrap;
}
.CodeMirror-linenumbers {}
.CodeMirror-linenumber {
  padding: 0 3px 0 5px;
  min-width: 20px;
  text-align: right;
  color: #999;
  white-space: nowrap;
}

.CodeMirror-guttermarker { color: black; }
.CodeMirror-guttermarker-subtle { color: #999; }

/* CURSOR */

.CodeMirror-cursor {
  border-left: 1px solid black;
  border-right: none;
  width: 0;
}
/* Shown when moving in bi-directional text */
.CodeMirror div.CodeMirror-secondarycursor {
  border-left: 1px solid silver;
}
.cm-fat-cursor .CodeMirror-cursor {
  width: auto;
  border: 0 !important;
  background: #7e7;
}
.cm-fat-cursor div.CodeMirror-cursors {
  z-index: 1;
}
.cm-fat-cursor-mark {
  background-color: rgba(20, 255, 20, 0.5);
  -webkit-animation: blink 1.06s steps(1) infinite;
  -moz-animation: blink 1.06s steps(1) infinite;
  animation: blink 1.06s steps(1) infinite;
}
.cm-animate-fat-cursor {
  width: auto;
  border: 0;
  -webkit-animation: blink 1.06s steps(1) infinite;
  -moz-animation: blink 1.06s steps(1) infinite;
  animation: blink 1.06s steps(1) infinite;
  background-color: #7e7;
}
@-moz-keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}
@-webkit-keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}
@keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}

/* Can style cursor different in overwrite (non-insert) mode */
.CodeMirror-overwrite .CodeMirror-cursor {}

.cm-tab { display: inline-block; text-decoration: inherit; }

.CodeMirror-rulers {
  position: absolute;
  left: 0; right: 0; top: -50px; bottom: 0;
  overflow: hidden;
}
.CodeMirror-ruler {
  border-left: 1px solid #ccc;
  top: 0; bottom: 0;
  position: absolute;
}

/* DEFAULT THEME */

.cm-s-default .cm-header {color: blue;}
.cm-s-default .cm-quote {color: #090;}
.cm-negative {color: #d44;}
.cm-positive {color: #292;}
.cm-header, .cm-strong {font-weight: bold;}
.cm-em {font-style: italic;}
.cm-link {text-decoration: underline;}
.cm-strikethrough {text-decoration: line-through;}

.cm-s-default .cm-keyword {color: #708;}
.cm-s-default .cm-atom {color: #219;}
.cm-s-default .cm-number {color: #164;}
.cm-s-default .cm-def {color: #00f;}
.cm-s-default .cm-variable,
.cm-s-default .cm-punctuation,
.cm-s-default .cm-property,
.cm-s-default .cm-operator {}
.cm-s-default .cm-variable-2 {color: #05a;}
.cm-s-default .cm-variable-3, .cm-s-default .cm-type {color: #085;}
.cm-s-default .cm-comment {color: #a50;}
.cm-s-default .cm-string {color: #a11;}
.cm-s-default .cm-string-2 {color: #f50;}
.cm-s-default .cm-meta {color: #555;}
.cm-s-default .cm-qualifier {color: #555;}
.cm-s-default .cm-builtin {color: #30a;}
.cm-s-default .cm-bracket {color: #997;}
.cm-s-default .cm-tag {color: #170;}
.cm-s-default .cm-attribute {color: #00c;}
.cm-s-default .cm-hr {color: #999;}
.cm-s-default .cm-link {color: #00c;}

.cm-s-default .cm-error {color: #f00;}
.cm-invalidchar {color: #f00;}

.CodeMirror-composing { border-bottom: 2px solid; }

/* Default styles for common addons */

div.CodeMirror span.CodeMirror-matchingbracket {color: #0b0;}
div.CodeMirror span.CodeMirror-nonmatchingbracket {color: #a22;}
.CodeMirror-matchingtag { background: rgba(255, 150, 0, .3); }
.CodeMirror-activeline-background {background: #e8f2ff;}

/* STOP */

/* The rest of this file contains styles related to the mechanics of
   the editor. You probably shouldn't touch them. */

.CodeMirror {
  position: relative;
  overflow: hidden;
  background: white;
}

.CodeMirror-scroll {
  overflow: scroll !important; /* Things will break if this is overridden */
  /* 30px is the magic margin used to hide the element's real scrollbars */
  /* See overflow: hidden in .CodeMirror */
  margin-bottom: -30px; margin-right: -30px;
  padding-bottom: 30px;
  height: 100%;
  outline: none; /* Prevent dragging from highlighting the element */
  position: relative;
}
.CodeMirror-sizer {
  position: relative;
  border-right: 30px solid transparent;
}

/* The fake, visible scrollbars. Used to force redraw during scrolling
   before actual scrolling happens, thus preventing shaking and
   flickering artifacts. */
.CodeMirror-vscrollbar, .CodeMirror-hscrollbar, .CodeMirror-scrollbar-filler, .CodeMirror-gutter-filler {
  position: absolute;
  z-index: 6;
  display: none;
}
.CodeMirror-vscrollbar {
  right: 0; top: 0;
  overflow-x: hidden;
  overflow-y: scroll;
}
.CodeMirror-hscrollbar {
  bottom: 0; left: 0;
  overflow-y: hidden;
  overflow-x: scroll;
}
.CodeMirror-scrollbar-filler {
  right: 0; bottom: 0;
}
.CodeMirror-gutter-filler {
  left: 0; bottom: 0;
}

.CodeMirror-gutters {
  position: absolute; left: 0; top: 0;
  min-height: 100%;
  z-index: 3;
}
.CodeMirror-gutter {
  white-space: normal;
  height: 100%;
  display: inline-block;
  vertical-align: top;
  margin-bottom: -30px;
}
.CodeMirror-gutter-wrapper {
  position: absolute;
  z-index: 4;
  background: none !important;
  border: none !important;
}
.CodeMirror-gutter-background {
  position: absolute;
  top: 0; bottom: 0;
  z-index: 4;
}
.CodeMirror-gutter-elt {
  position: absolute;
  cursor: default;
  z-index: 4;
}
.CodeMirror-gutter-wrapper ::selection { background-color: transparent }
.CodeMirror-gutter-wrapper ::-moz-selection { background-color: transparent }

.CodeMirror-lines {
  cursor: text;
  min-height: 1px; /* prevents collapsing before first draw */
}
.CodeMirror pre.CodeMirror-line,
.CodeMirror pre.CodeMirror-line-like {
  /* Reset some styles that the rest of the page might have set */
  -moz-border-radius: 0; -webkit-border-radius: 0; border-radius: 0;
  border-width: 0;
  background: transparent;
  font-family: inherit;
  font-size: inherit;
  margin: 0;
  white-space: pre;
  word-wrap: normal;
  line-height: inherit;
  color: inherit;
  z-index: 2;
  position: relative;
  overflow: visible;
  -webkit-tap-highlight-color: transparent;
  -webkit-font-variant-ligatures: contextual;
  font-variant-ligatures: contextual;
}
.CodeMirror-wrap pre.CodeMirror-line,
.CodeMirror-wrap pre.CodeMirror-line-like {
  word-wrap: break-word;
  white-space: pre-wrap;
  word-break: normal;
}

.CodeMirror-linebackground {
  position: absolute;
  left: 0; right: 0; top: 0; bottom: 0;
  z-index: 0;
}

.CodeMirror-linewidget {
  position: relative;
  z-index: 2;
  padding: 0.1px; /* Force widget margins to stay inside of the container */
}

.CodeMirror-widget {}

.CodeMirror-rtl pre { direction: rtl; }

.CodeMirror-code {
  outline: none;
}

/* Force content-box sizing for the elements where we expect it */
.CodeMirror-scroll,
.CodeMirror-sizer,
.CodeMirror-gutter,
.CodeMirror-gutters,
.CodeMirror-linenumber {
  -moz-box-sizing: content-box;
  box-sizing: content-box;
}

.CodeMirror-measure {
  position: absolute;
  width: 100%;
  height: 0;
  overflow: hidden;
  visibility: hidden;
}

.CodeMirror-cursor {
  position: absolute;
  pointer-events: none;
}
.CodeMirror-measure pre { position: static; }

div.CodeMirror-cursors {
  visibility: hidden;
  position: relative;
  z-index: 3;
}
div.CodeMirror-dragcursors {
  visibility: visible;
}

.CodeMirror-focused div.CodeMirror-cursors {
  visibility: visible;
}

.CodeMirror-selected { background: #d9d9d9; }
.CodeMirror-focused .CodeMirror-selected { background: #d7d4f0; }
.CodeMirror-crosshair { cursor: crosshair; }
.CodeMirror-line::selection, .CodeMirror-line > span::selection, .CodeMirror-line > span > span::selection { background: #d7d4f0; }
.CodeMirror-line::-moz-selection, .CodeMirror-line > span::-moz-selection, .CodeMirror-line > span > span::-moz-selection { background: #d7d4f0; }

.cm-searching {
  background-color: #ffa;
  background-color: rgba(255, 255, 0, .4);
}

/* Used to force a border model for a node */
.cm-force-border { padding-right: .1px; }

@media print {
  /* Hide the cursor when printing */
  .CodeMirror div.CodeMirror-cursors {
    visibility: hidden;
  }
}

/* See issue #2901 */
.cm-tab-wrap-hack:after { content: ''; }

/* Help users use markselection to safely style text background */
span.CodeMirror-selectedtext { background: none; }

.CodeMirror-dialog {
  position: absolute;
  left: 0; right: 0;
  background: inherit;
  z-index: 15;
  padding: .1em .8em;
  overflow: hidden;
  color: inherit;
}

.CodeMirror-dialog-top {
  border-bottom: 1px solid #eee;
  top: 0;
}

.CodeMirror-dialog-bottom {
  border-top: 1px solid #eee;
  bottom: 0;
}

.CodeMirror-dialog input {
  border: none;
  outline: none;
  background: transparent;
  width: 20em;
  color: inherit;
  font-family: monospace;
}

.CodeMirror-dialog button {
  font-size: 70%;
}

.CodeMirror-foldmarker {
  color: blue;
  text-shadow: #b9f 1px 1px 2px, #b9f -1px -1px 2px, #b9f 1px -1px 2px, #b9f -1px 1px 2px;
  font-family: arial;
  line-height: .3;
  cursor: pointer;
}
.CodeMirror-foldgutter {
  width: .7em;
}
.CodeMirror-foldgutter-open,
.CodeMirror-foldgutter-folded {
  cursor: pointer;
}
.CodeMirror-foldgutter-open:after {
  content: "\25BE";
}
.CodeMirror-foldgutter-folded:after {
  content: "\25B8";
}

/*
  Name:       material
  Author:     Mattia Astorino (http://github.com/equinusocio)
  Website:    https://material-theme.site/
*/

.cm-s-material.CodeMirror {
  background-color: #263238;
  color: #EEFFFF;
}

.cm-s-material .CodeMirror-gutters {
  background: #263238;
  color: #546E7A;
  border: none;
}

.cm-s-material .CodeMirror-guttermarker,
.cm-s-material .CodeMirror-guttermarker-subtle,
.cm-s-material .CodeMirror-linenumber {
  color: #546E7A;
}

.cm-s-material .CodeMirror-cursor {
  border-left: 1px solid #FFCC00;
}

.cm-s-material div.CodeMirror-selected {
  background: rgba(128, 203, 196, 0.2);
}

.cm-s-material.CodeMirror-focused div.CodeMirror-selected {
  background: rgba(128, 203, 196, 0.2);
}

.cm-s-material .CodeMirror-line::selection,
.cm-s-material .CodeMirror-line>span::selection,
.cm-s-material .CodeMirror-line>span>span::selection {
  background: rgba(128, 203, 196, 0.2);
}

.cm-s-material .CodeMirror-line::-moz-selection,
.cm-s-material .CodeMirror-line>span::-moz-selection,
.cm-s-material .CodeMirror-line>span>span::-moz-selection {
  background: rgba(128, 203, 196, 0.2);
}

.cm-s-material .CodeMirror-activeline-background {
  background: rgba(0, 0, 0, 0.5);
}

.cm-s-material .cm-keyword {
  color: #C792EA;
}

.cm-s-material .cm-operator {
  color: #89DDFF;
}

.cm-s-material .cm-variable-2 {
  color: #EEFFFF;
}

.cm-s-material .cm-variable-3,
.cm-s-material .cm-type {
  color: #f07178;
}

.cm-s-material .cm-builtin {
  color: #FFCB6B;
}

.cm-s-material .cm-atom {
  color: #F78C6C;
}

.cm-s-material .cm-number {
  color: #FF5370;
}

.cm-s-material .cm-def {
  color: #82AAFF;
}

.cm-s-material .cm-string {
  color: #C3E88D;
}

.cm-s-material .cm-string-2 {
  color: #f07178;
}

.cm-s-material .cm-comment {
  color: #546E7A;
}

.cm-s-material .cm-variable {
  color: #f07178;
}

.cm-s-material .cm-tag {
  color: #FF5370;
}

.cm-s-material .cm-meta {
  color: #FFCB6B;
}

.cm-s-material .cm-attribute {
  color: #C792EA;
}

.cm-s-material .cm-property {
  color: #C792EA;
}

.cm-s-material .cm-qualifier {
  color: #DECB6B;
}

.cm-s-material .cm-variable-3,
.cm-s-material .cm-type {
  color: #DECB6B;
}


.cm-s-material .cm-error {
  color: rgba(255, 255, 255, 1.0);
  background-color: #FF5370;
}

.cm-s-material .CodeMirror-matchingbracket {
  text-decoration: underline;
  color: white !important;
}
/**
 * "
 *  Using Zenburn color palette from the Emacs Zenburn Theme
 *  https://github.com/bbatsov/zenburn-emacs/blob/master/zenburn-theme.el
 *
 *  Also using parts of https://github.com/xavi/coderay-lighttable-theme
 * "
 * From: https://github.com/wisenomad/zenburn-lighttable-theme/blob/master/zenburn.css
 */

.cm-s-zenburn .CodeMirror-gutters { background: #3f3f3f !important; }
.cm-s-zenburn .CodeMirror-foldgutter-open, .CodeMirror-foldgutter-folded { color: #999; }
.cm-s-zenburn .CodeMirror-cursor { border-left: 1px solid white; }
.cm-s-zenburn { background-color: #3f3f3f; color: #dcdccc; }
.cm-s-zenburn span.cm-builtin { color: #dcdccc; font-weight: bold; }
.cm-s-zenburn span.cm-comment { color: #7f9f7f; }
.cm-s-zenburn span.cm-keyword { color: #f0dfaf; font-weight: bold; }
.cm-s-zenburn span.cm-atom { color: #bfebbf; }
.cm-s-zenburn span.cm-def { color: #dcdccc; }
.cm-s-zenburn span.cm-variable { color: #dfaf8f; }
.cm-s-zenburn span.cm-variable-2 { color: #dcdccc; }
.cm-s-zenburn span.cm-string { color: #cc9393; }
.cm-s-zenburn span.cm-string-2 { color: #cc9393; }
.cm-s-zenburn span.cm-number { color: #dcdccc; }
.cm-s-zenburn span.cm-tag { color: #93e0e3; }
.cm-s-zenburn span.cm-property { color: #dfaf8f; }
.cm-s-zenburn span.cm-attribute { color: #dfaf8f; }
.cm-s-zenburn span.cm-qualifier { color: #7cb8bb; }
.cm-s-zenburn span.cm-meta { color: #f0dfaf; }
.cm-s-zenburn span.cm-header { color: #f0efd0; }
.cm-s-zenburn span.cm-operator { color: #f0efd0; }
.cm-s-zenburn span.CodeMirror-matchingbracket { box-sizing: border-box; background: transparent; border-bottom: 1px solid; }
.cm-s-zenburn span.CodeMirror-nonmatchingbracket { border-bottom: 1px solid; background: none; }
.cm-s-zenburn .CodeMirror-activeline { background: #000000; }
.cm-s-zenburn .CodeMirror-activeline-background { background: #000000; }
.cm-s-zenburn div.CodeMirror-selected { background: #545454; }
.cm-s-zenburn .CodeMirror-focused div.CodeMirror-selected { background: #4f4f4f; }

.cm-s-abcdef.CodeMirror { background: #0f0f0f; color: #defdef; }
.cm-s-abcdef div.CodeMirror-selected { background: #515151; }
.cm-s-abcdef .CodeMirror-line::selection, .cm-s-abcdef .CodeMirror-line > span::selection, .cm-s-abcdef .CodeMirror-line > span > span::selection { background: rgba(56, 56, 56, 0.99); }
.cm-s-abcdef .CodeMirror-line::-moz-selection, .cm-s-abcdef .CodeMirror-line > span::-moz-selection, .cm-s-abcdef .CodeMirror-line > span > span::-moz-selection { background: rgba(56, 56, 56, 0.99); }
.cm-s-abcdef .CodeMirror-gutters { background: #555; border-right: 2px solid #314151; }
.cm-s-abcdef .CodeMirror-guttermarker { color: #222; }
.cm-s-abcdef .CodeMirror-guttermarker-subtle { color: azure; }
.cm-s-abcdef .CodeMirror-linenumber { color: #FFFFFF; }
.cm-s-abcdef .CodeMirror-cursor { border-left: 1px solid #00FF00; }

.cm-s-abcdef span.cm-keyword { color: darkgoldenrod; font-weight: bold; }
.cm-s-abcdef span.cm-atom { color: #77F; }
.cm-s-abcdef span.cm-number { color: violet; }
.cm-s-abcdef span.cm-def { color: #fffabc; }
.cm-s-abcdef span.cm-variable { color: #abcdef; }
.cm-s-abcdef span.cm-variable-2 { color: #cacbcc; }
.cm-s-abcdef span.cm-variable-3, .cm-s-abcdef span.cm-type { color: #def; }
.cm-s-abcdef span.cm-property { color: #fedcba; }
.cm-s-abcdef span.cm-operator { color: #ff0; }
.cm-s-abcdef span.cm-comment { color: #7a7b7c; font-style: italic;}
.cm-s-abcdef span.cm-string { color: #2b4; }
.cm-s-abcdef span.cm-meta { color: #C9F; }
.cm-s-abcdef span.cm-qualifier { color: #FFF700; }
.cm-s-abcdef span.cm-builtin { color: #30aabc; }
.cm-s-abcdef span.cm-bracket { color: #8a8a8a; }
.cm-s-abcdef span.cm-tag { color: #FFDD44; }
.cm-s-abcdef span.cm-attribute { color: #DDFF00; }
.cm-s-abcdef span.cm-error { color: #FF0000; }
.cm-s-abcdef span.cm-header { color: aquamarine; font-weight: bold; }
.cm-s-abcdef span.cm-link { color: blueviolet; }

.cm-s-abcdef .CodeMirror-activeline-background { background: #314151; }

/*

    Name:       Base16 Default Light
    Author:     Chris Kempson (http://chriskempson.com)

    CodeMirror template by Jan T. Sott (https://github.com/idleberg/base16-codemirror)
    Original Base16 color scheme by Chris Kempson (https://github.com/chriskempson/base16)

*/

.cm-s-base16-light.CodeMirror { background: #f5f5f5; color: #202020; }
.cm-s-base16-light div.CodeMirror-selected { background: #e0e0e0; }
.cm-s-base16-light .CodeMirror-line::selection, .cm-s-base16-light .CodeMirror-line > span::selection, .cm-s-base16-light .CodeMirror-line > span > span::selection { background: #e0e0e0; }
.cm-s-base16-light .CodeMirror-line::-moz-selection, .cm-s-base16-light .CodeMirror-line > span::-moz-selection, .cm-s-base16-light .CodeMirror-line > span > span::-moz-selection { background: #e0e0e0; }
.cm-s-base16-light .CodeMirror-gutters { background: #f5f5f5; border-right: 0px; }
.cm-s-base16-light .CodeMirror-guttermarker { color: #ac4142; }
.cm-s-base16-light .CodeMirror-guttermarker-subtle { color: #b0b0b0; }
.cm-s-base16-light .CodeMirror-linenumber { color: #b0b0b0; }
.cm-s-base16-light .CodeMirror-cursor { border-left: 1px solid #505050; }

.cm-s-base16-light span.cm-comment { color: #8f5536; }
.cm-s-base16-light span.cm-atom { color: #aa759f; }
.cm-s-base16-light span.cm-number { color: #aa759f; }

.cm-s-base16-light span.cm-property, .cm-s-base16-light span.cm-attribute { color: #90a959; }
.cm-s-base16-light span.cm-keyword { color: #ac4142; }
.cm-s-base16-light span.cm-string { color: #f4bf75; }

.cm-s-base16-light span.cm-variable { color: #90a959; }
.cm-s-base16-light span.cm-variable-2 { color: #6a9fb5; }
.cm-s-base16-light span.cm-def { color: #d28445; }
.cm-s-base16-light span.cm-bracket { color: #202020; }
.cm-s-base16-light span.cm-tag { color: #ac4142; }
.cm-s-base16-light span.cm-link { color: #aa759f; }
.cm-s-base16-light span.cm-error { background: #ac4142; color: #505050; }

.cm-s-base16-light .CodeMirror-activeline-background { background: #DDDCDC; }
.cm-s-base16-light .CodeMirror-matchingbracket { color: #f5f5f5 !important; background-color: #6A9FB5 !important}

/*

    Name:       Base16 Default Dark
    Author:     Chris Kempson (http://chriskempson.com)

    CodeMirror template by Jan T. Sott (https://github.com/idleberg/base16-codemirror)
    Original Base16 color scheme by Chris Kempson (https://github.com/chriskempson/base16)

*/

.cm-s-base16-dark.CodeMirror { background: #151515; color: #e0e0e0; }
.cm-s-base16-dark div.CodeMirror-selected { background: #303030; }
.cm-s-base16-dark .CodeMirror-line::selection, .cm-s-base16-dark .CodeMirror-line > span::selection, .cm-s-base16-dark .CodeMirror-line > span > span::selection { background: rgba(48, 48, 48, .99); }
.cm-s-base16-dark .CodeMirror-line::-moz-selection, .cm-s-base16-dark .CodeMirror-line > span::-moz-selection, .cm-s-base16-dark .CodeMirror-line > span > span::-moz-selection { background: rgba(48, 48, 48, .99); }
.cm-s-base16-dark .CodeMirror-gutters { background: #151515; border-right: 0px; }
.cm-s-base16-dark .CodeMirror-guttermarker { color: #ac4142; }
.cm-s-base16-dark .CodeMirror-guttermarker-subtle { color: #505050; }
.cm-s-base16-dark .CodeMirror-linenumber { color: #505050; }
.cm-s-base16-dark .CodeMirror-cursor { border-left: 1px solid #b0b0b0; }

.cm-s-base16-dark span.cm-comment { color: #8f5536; }
.cm-s-base16-dark span.cm-atom { color: #aa759f; }
.cm-s-base16-dark span.cm-number { color: #aa759f; }

.cm-s-base16-dark span.cm-property, .cm-s-base16-dark span.cm-attribute { color: #90a959; }
.cm-s-base16-dark span.cm-keyword { color: #ac4142; }
.cm-s-base16-dark span.cm-string { color: #f4bf75; }

.cm-s-base16-dark span.cm-variable { color: #90a959; }
.cm-s-base16-dark span.cm-variable-2 { color: #6a9fb5; }
.cm-s-base16-dark span.cm-def { color: #d28445; }
.cm-s-base16-dark span.cm-bracket { color: #e0e0e0; }
.cm-s-base16-dark span.cm-tag { color: #ac4142; }
.cm-s-base16-dark span.cm-link { color: #aa759f; }
.cm-s-base16-dark span.cm-error { background: #ac4142; color: #b0b0b0; }

.cm-s-base16-dark .CodeMirror-activeline-background { background: #202020; }
.cm-s-base16-dark .CodeMirror-matchingbracket { text-decoration: underline; color: white !important; }

/*

    Name:       dracula
    Author:     Michael Kaminsky (http://github.com/mkaminsky11)

    Original dracula color scheme by Zeno Rocha (https://github.com/zenorocha/dracula-theme)

*/


.cm-s-dracula.CodeMirror, .cm-s-dracula .CodeMirror-gutters {
  background-color: #282a36 !important;
  color: #f8f8f2 !important;
  border: none;
}
.cm-s-dracula .CodeMirror-gutters { color: #282a36; }
.cm-s-dracula .CodeMirror-cursor { border-left: solid thin #f8f8f0; }
.cm-s-dracula .CodeMirror-linenumber { color: #6D8A88; }
.cm-s-dracula .CodeMirror-selected { background: rgba(255, 255, 255, 0.10); }
.cm-s-dracula .CodeMirror-line::selection, .cm-s-dracula .CodeMirror-line > span::selection, .cm-s-dracula .CodeMirror-line > span > span::selection { background: rgba(255, 255, 255, 0.10); }
.cm-s-dracula .CodeMirror-line::-moz-selection, .cm-s-dracula .CodeMirror-line > span::-moz-selection, .cm-s-dracula .CodeMirror-line > span > span::-moz-selection { background: rgba(255, 255, 255, 0.10); }
.cm-s-dracula span.cm-comment { color: #6272a4; }
.cm-s-dracula span.cm-string, .cm-s-dracula span.cm-string-2 { color: #f1fa8c; }
.cm-s-dracula span.cm-number { color: #bd93f9; }
.cm-s-dracula span.cm-variable { color: #50fa7b; }
.cm-s-dracula span.cm-variable-2 { color: white; }
.cm-s-dracula span.cm-def { color: #50fa7b; }
.cm-s-dracula span.cm-operator { color: #ff79c6; }
.cm-s-dracula span.cm-keyword { color: #ff79c6; }
.cm-s-dracula span.cm-atom { color: #bd93f9; }
.cm-s-dracula span.cm-meta { color: #f8f8f2; }
.cm-s-dracula span.cm-tag { color: #ff79c6; }
.cm-s-dracula span.cm-attribute { color: #50fa7b; }
.cm-s-dracula span.cm-qualifier { color: #50fa7b; }
.cm-s-dracula span.cm-property { color: #66d9ef; }
.cm-s-dracula span.cm-builtin { color: #50fa7b; }
.cm-s-dracula span.cm-variable-3, .cm-s-dracula span.cm-type { color: #ffb86c; }

.cm-s-dracula .CodeMirror-activeline-background { background: rgba(255,255,255,0.1); }
.cm-s-dracula .CodeMirror-matchingbracket { text-decoration: underline; color: white !important; }

/*

    Name:       Hopscotch
    Author:     Jan T. Sott

    CodeMirror template by Jan T. Sott (https://github.com/idleberg/base16-codemirror)
    Original Base16 color scheme by Chris Kempson (https://github.com/chriskempson/base16)

*/

.cm-s-hopscotch.CodeMirror {background: #322931; color: #d5d3d5;}
.cm-s-hopscotch div.CodeMirror-selected {background: #433b42 !important;}
.cm-s-hopscotch .CodeMirror-gutters {background: #322931; border-right: 0px;}
.cm-s-hopscotch .CodeMirror-linenumber {color: #797379;}
.cm-s-hopscotch .CodeMirror-cursor {border-left: 1px solid #989498 !important;}

.cm-s-hopscotch span.cm-comment {color: #b33508;}
.cm-s-hopscotch span.cm-atom {color: #c85e7c;}
.cm-s-hopscotch span.cm-number {color: #c85e7c;}

.cm-s-hopscotch span.cm-property, .cm-s-hopscotch span.cm-attribute {color: #8fc13e;}
.cm-s-hopscotch span.cm-keyword {color: #dd464c;}
.cm-s-hopscotch span.cm-string {color: #fdcc59;}

.cm-s-hopscotch span.cm-variable {color: #8fc13e;}
.cm-s-hopscotch span.cm-variable-2 {color: #1290bf;}
.cm-s-hopscotch span.cm-def {color: #fd8b19;}
.cm-s-hopscotch span.cm-error {background: #dd464c; color: #989498;}
.cm-s-hopscotch span.cm-bracket {color: #d5d3d5;}
.cm-s-hopscotch span.cm-tag {color: #dd464c;}
.cm-s-hopscotch span.cm-link {color: #c85e7c;}

.cm-s-hopscotch .CodeMirror-matchingbracket { text-decoration: underline; color: white !important;}
.cm-s-hopscotch .CodeMirror-activeline-background { background: #302020; }

/****************************************************************/
/*   Based on mbonaci's Brackets mbo theme                      */
/*   https://github.com/mbonaci/global/blob/master/Mbo.tmTheme  */
/*   Create your own: http://tmtheme-editor.herokuapp.com       */
/****************************************************************/

.cm-s-mbo.CodeMirror { background: #2c2c2c; color: #ffffec; }
.cm-s-mbo div.CodeMirror-selected { background: #716C62; }
.cm-s-mbo .CodeMirror-line::selection, .cm-s-mbo .CodeMirror-line > span::selection, .cm-s-mbo .CodeMirror-line > span > span::selection { background: rgba(113, 108, 98, .99); }
.cm-s-mbo .CodeMirror-line::-moz-selection, .cm-s-mbo .CodeMirror-line > span::-moz-selection, .cm-s-mbo .CodeMirror-line > span > span::-moz-selection { background: rgba(113, 108, 98, .99); }
.cm-s-mbo .CodeMirror-gutters { background: #4e4e4e; border-right: 0px; }
.cm-s-mbo .CodeMirror-guttermarker { color: white; }
.cm-s-mbo .CodeMirror-guttermarker-subtle { color: grey; }
.cm-s-mbo .CodeMirror-linenumber { color: #dadada; }
.cm-s-mbo .CodeMirror-cursor { border-left: 1px solid #ffffec; }

.cm-s-mbo span.cm-comment { color: #95958a; }
.cm-s-mbo span.cm-atom { color: #00a8c6; }
.cm-s-mbo span.cm-number { color: #00a8c6; }

.cm-s-mbo span.cm-property, .cm-s-mbo span.cm-attribute { color: #9ddfe9; }
.cm-s-mbo span.cm-keyword { color: #ffb928; }
.cm-s-mbo span.cm-string { color: #ffcf6c; }
.cm-s-mbo span.cm-string.cm-property { color: #ffffec; }

.cm-s-mbo span.cm-variable { color: #ffffec; }
.cm-s-mbo span.cm-variable-2 { color: #00a8c6; }
.cm-s-mbo span.cm-def { color: #ffffec; }
.cm-s-mbo span.cm-bracket { color: #fffffc; font-weight: bold; }
.cm-s-mbo span.cm-tag { color: #9ddfe9; }
.cm-s-mbo span.cm-link { color: #f54b07; }
.cm-s-mbo span.cm-error { border-bottom: #636363; color: #ffffec; }
.cm-s-mbo span.cm-qualifier { color: #ffffec; }

.cm-s-mbo .CodeMirror-activeline-background { background: #494b41; }
.cm-s-mbo .CodeMirror-matchingbracket { color: #ffb928 !important; }
.cm-s-mbo .CodeMirror-matchingtag { background: rgba(255, 255, 255, .37); }

/*
  MDN-LIKE Theme - Mozilla
  Ported to CodeMirror by Peter Kroon <plakroon@gmail.com>
  Report bugs/issues here: https://github.com/codemirror/CodeMirror/issues
  GitHub: @peterkroon

  The mdn-like theme is inspired on the displayed code examples at: https://developer.mozilla.org/en-US/docs/Web/CSS/animation

*/
.cm-s-mdn-like.CodeMirror { color: #999; background-color: #fff; }
.cm-s-mdn-like div.CodeMirror-selected { background: #cfc; }
.cm-s-mdn-like .CodeMirror-line::selection, .cm-s-mdn-like .CodeMirror-line > span::selection, .cm-s-mdn-like .CodeMirror-line > span > span::selection { background: #cfc; }
.cm-s-mdn-like .CodeMirror-line::-moz-selection, .cm-s-mdn-like .CodeMirror-line > span::-moz-selection, .cm-s-mdn-like .CodeMirror-line > span > span::-moz-selection { background: #cfc; }

.cm-s-mdn-like .CodeMirror-gutters { background: #f8f8f8; border-left: 6px solid rgba(0,83,159,0.65); color: #333; }
.cm-s-mdn-like .CodeMirror-linenumber { color: #aaa; padding-left: 8px; }
.cm-s-mdn-like .CodeMirror-cursor { border-left: 2px solid #222; }

.cm-s-mdn-like .cm-keyword { color: #6262FF; }
.cm-s-mdn-like .cm-atom { color: #F90; }
.cm-s-mdn-like .cm-number { color:  #ca7841; }
.cm-s-mdn-like .cm-def { color: #8DA6CE; }
.cm-s-mdn-like span.cm-variable-2, .cm-s-mdn-like span.cm-tag { color: #690; }
.cm-s-mdn-like span.cm-variable-3, .cm-s-mdn-like span.cm-def, .cm-s-mdn-like span.cm-type { color: #07a; }

.cm-s-mdn-like .cm-variable { color: #07a; }
.cm-s-mdn-like .cm-property { color: #905; }
.cm-s-mdn-like .cm-qualifier { color: #690; }

.cm-s-mdn-like .cm-operator { color: #cda869; }
.cm-s-mdn-like .cm-comment { color:#777; font-weight:normal; }
.cm-s-mdn-like .cm-string { color:#07a; font-style:italic; }
.cm-s-mdn-like .cm-string-2 { color:#bd6b18; } /*?*/
.cm-s-mdn-like .cm-meta { color: #000; } /*?*/
.cm-s-mdn-like .cm-builtin { color: #9B7536; } /*?*/
.cm-s-mdn-like .cm-tag { color: #997643; }
.cm-s-mdn-like .cm-attribute { color: #d6bb6d; } /*?*/
.cm-s-mdn-like .cm-header { color: #FF6400; }
.cm-s-mdn-like .cm-hr { color: #AEAEAE; }
.cm-s-mdn-like .cm-link { color:#ad9361; font-style:italic; text-decoration:none; }
.cm-s-mdn-like .cm-error { border-bottom: 1px solid red; }

div.cm-s-mdn-like .CodeMirror-activeline-background { background: #efefff; }
div.cm-s-mdn-like span.CodeMirror-matchingbracket { outline:1px solid grey; color: inherit; }

.cm-s-mdn-like.CodeMirror { background-image: url(data:image/png;base64,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); }

/*

    Name:       seti
    Author:     Michael Kaminsky (http://github.com/mkaminsky11)

    Original seti color scheme by Jesse Weed (https://github.com/jesseweed/seti-syntax)

*/


.cm-s-seti.CodeMirror {
  background-color: #151718 !important;
  color: #CFD2D1 !important;
  border: none;
}
.cm-s-seti .CodeMirror-gutters {
  color: #404b53;
  background-color: #0E1112;
  border: none;
}
.cm-s-seti .CodeMirror-cursor { border-left: solid thin #f8f8f0; }
.cm-s-seti .CodeMirror-linenumber { color: #6D8A88; }
.cm-s-seti.CodeMirror-focused div.CodeMirror-selected { background: rgba(255, 255, 255, 0.10); }
.cm-s-seti .CodeMirror-line::selection, .cm-s-seti .CodeMirror-line > span::selection, .cm-s-seti .CodeMirror-line > span > span::selection { background: rgba(255, 255, 255, 0.10); }
.cm-s-seti .CodeMirror-line::-moz-selection, .cm-s-seti .CodeMirror-line > span::-moz-selection, .cm-s-seti .CodeMirror-line > span > span::-moz-selection { background: rgba(255, 255, 255, 0.10); }
.cm-s-seti span.cm-comment { color: #41535b; }
.cm-s-seti span.cm-string, .cm-s-seti span.cm-string-2 { color: #55b5db; }
.cm-s-seti span.cm-number { color: #cd3f45; }
.cm-s-seti span.cm-variable { color: #55b5db; }
.cm-s-seti span.cm-variable-2 { color: #a074c4; }
.cm-s-seti span.cm-def { color: #55b5db; }
.cm-s-seti span.cm-keyword { color: #ff79c6; }
.cm-s-seti span.cm-operator { color: #9fca56; }
.cm-s-seti span.cm-keyword { color: #e6cd69; }
.cm-s-seti span.cm-atom { color: #cd3f45; }
.cm-s-seti span.cm-meta { color: #55b5db; }
.cm-s-seti span.cm-tag { color: #55b5db; }
.cm-s-seti span.cm-attribute { color: #9fca56; }
.cm-s-seti span.cm-qualifier { color: #9fca56; }
.cm-s-seti span.cm-property { color: #a074c4; }
.cm-s-seti span.cm-variable-3, .cm-s-seti span.cm-type { color: #9fca56; }
.cm-s-seti span.cm-builtin { color: #9fca56; }
.cm-s-seti .CodeMirror-activeline-background { background: #101213; }
.cm-s-seti .CodeMirror-matchingbracket { text-decoration: underline; color: white !important; }

/*
Solarized theme for code-mirror
http://ethanschoonover.com/solarized
*/

/*
Solarized color palette
http://ethanschoonover.com/solarized/img/solarized-palette.png
*/

.solarized.base03 { color: #002b36; }
.solarized.base02 { color: #073642; }
.solarized.base01 { color: #586e75; }
.solarized.base00 { color: #657b83; }
.solarized.base0 { color: #839496; }
.solarized.base1 { color: #93a1a1; }
.solarized.base2 { color: #eee8d5; }
.solarized.base3  { color: #fdf6e3; }
.solarized.solar-yellow  { color: #b58900; }
.solarized.solar-orange  { color: #cb4b16; }
.solarized.solar-red { color: #dc322f; }
.solarized.solar-magenta { color: #d33682; }
.solarized.solar-violet  { color: #6c71c4; }
.solarized.solar-blue { color: #268bd2; }
.solarized.solar-cyan { color: #2aa198; }
.solarized.solar-green { color: #859900; }

/* Color scheme for code-mirror */

.cm-s-solarized {
  line-height: 1.45em;
  color-profile: sRGB;
  rendering-intent: auto;
}
.cm-s-solarized.cm-s-dark {
  color: #839496;
  background-color: #002b36;
  text-shadow: #002b36 0 1px;
}
.cm-s-solarized.cm-s-light {
  background-color: #fdf6e3;
  color: #657b83;
  text-shadow: #eee8d5 0 1px;
}

.cm-s-solarized .CodeMirror-widget {
  text-shadow: none;
}

.cm-s-solarized .cm-header { color: #586e75; }
.cm-s-solarized .cm-quote { color: #93a1a1; }

.cm-s-solarized .cm-keyword { color: #cb4b16; }
.cm-s-solarized .cm-atom { color: #d33682; }
.cm-s-solarized .cm-number { color: #d33682; }
.cm-s-solarized .cm-def { color: #2aa198; }

.cm-s-solarized .cm-variable { color: #839496; }
.cm-s-solarized .cm-variable-2 { color: #b58900; }
.cm-s-solarized .cm-variable-3, .cm-s-solarized .cm-type { color: #6c71c4; }

.cm-s-solarized .cm-property { color: #2aa198; }
.cm-s-solarized .cm-operator { color: #6c71c4; }

.cm-s-solarized .cm-comment { color: #586e75; font-style:italic; }

.cm-s-solarized .cm-string { color: #859900; }
.cm-s-solarized .cm-string-2 { color: #b58900; }

.cm-s-solarized .cm-meta { color: #859900; }
.cm-s-solarized .cm-qualifier { color: #b58900; }
.cm-s-solarized .cm-builtin { color: #d33682; }
.cm-s-solarized .cm-bracket { color: #cb4b16; }
.cm-s-solarized .CodeMirror-matchingbracket { color: #859900; }
.cm-s-solarized .CodeMirror-nonmatchingbracket { color: #dc322f; }
.cm-s-solarized .cm-tag { color: #93a1a1; }
.cm-s-solarized .cm-attribute { color: #2aa198; }
.cm-s-solarized .cm-hr {
  color: transparent;
  border-top: 1px solid #586e75;
  display: block;
}
.cm-s-solarized .cm-link { color: #93a1a1; cursor: pointer; }
.cm-s-solarized .cm-special { color: #6c71c4; }
.cm-s-solarized .cm-em {
  color: #999;
  text-decoration: underline;
  text-decoration-style: dotted;
}
.cm-s-solarized .cm-error,
.cm-s-solarized .cm-invalidchar {
  color: #586e75;
  border-bottom: 1px dotted #dc322f;
}

.cm-s-solarized.cm-s-dark div.CodeMirror-selected { background: #073642; }
.cm-s-solarized.cm-s-dark.CodeMirror ::selection { background: rgba(7, 54, 66, 0.99); }
.cm-s-solarized.cm-s-dark .CodeMirror-line::-moz-selection, .cm-s-dark .CodeMirror-line > span::-moz-selection, .cm-s-dark .CodeMirror-line > span > span::-moz-selection { background: rgba(7, 54, 66, 0.99); }

.cm-s-solarized.cm-s-light div.CodeMirror-selected { background: #eee8d5; }
.cm-s-solarized.cm-s-light .CodeMirror-line::selection, .cm-s-light .CodeMirror-line > span::selection, .cm-s-light .CodeMirror-line > span > span::selection { background: #eee8d5; }
.cm-s-solarized.cm-s-light .CodeMirror-line::-moz-selection, .cm-s-ligh .CodeMirror-line > span::-moz-selection, .cm-s-ligh .CodeMirror-line > span > span::-moz-selection { background: #eee8d5; }

/* Editor styling */



/* Little shadow on the view-port of the buffer view */
.cm-s-solarized.CodeMirror {
  -moz-box-shadow: inset 7px 0 12px -6px #000;
  -webkit-box-shadow: inset 7px 0 12px -6px #000;
  box-shadow: inset 7px 0 12px -6px #000;
}

/* Remove gutter border */
.cm-s-solarized .CodeMirror-gutters {
  border-right: 0;
}

/* Gutter colors and line number styling based of color scheme (dark / light) */

/* Dark */
.cm-s-solarized.cm-s-dark .CodeMirror-gutters {
  background-color: #073642;
}

.cm-s-solarized.cm-s-dark .CodeMirror-linenumber {
  color: #586e75;
  text-shadow: #021014 0 -1px;
}

/* Light */
.cm-s-solarized.cm-s-light .CodeMirror-gutters {
  background-color: #eee8d5;
}

.cm-s-solarized.cm-s-light .CodeMirror-linenumber {
  color: #839496;
}

/* Common */
.cm-s-solarized .CodeMirror-linenumber {
  padding: 0 5px;
}
.cm-s-solarized .CodeMirror-guttermarker-subtle { color: #586e75; }
.cm-s-solarized.cm-s-dark .CodeMirror-guttermarker { color: #ddd; }
.cm-s-solarized.cm-s-light .CodeMirror-guttermarker { color: #cb4b16; }

.cm-s-solarized .CodeMirror-gutter .CodeMirror-gutter-text {
  color: #586e75;
}

/* Cursor */
.cm-s-solarized .CodeMirror-cursor { border-left: 1px solid #819090; }

/* Fat cursor */
.cm-s-solarized.cm-s-light.cm-fat-cursor .CodeMirror-cursor { background: #77ee77; }
.cm-s-solarized.cm-s-light .cm-animate-fat-cursor { background-color: #77ee77; }
.cm-s-solarized.cm-s-dark.cm-fat-cursor .CodeMirror-cursor { background: #586e75; }
.cm-s-solarized.cm-s-dark .cm-animate-fat-cursor { background-color: #586e75; }

/* Active line */
.cm-s-solarized.cm-s-dark .CodeMirror-activeline-background {
  background: rgba(255, 255, 255, 0.06);
}
.cm-s-solarized.cm-s-light .CodeMirror-activeline-background {
  background: rgba(0, 0, 0, 0.06);
}

.cm-s-the-matrix.CodeMirror { background: #000000; color: #00FF00; }
.cm-s-the-matrix div.CodeMirror-selected { background: #2D2D2D; }
.cm-s-the-matrix .CodeMirror-line::selection, .cm-s-the-matrix .CodeMirror-line > span::selection, .cm-s-the-matrix .CodeMirror-line > span > span::selection { background: rgba(45, 45, 45, 0.99); }
.cm-s-the-matrix .CodeMirror-line::-moz-selection, .cm-s-the-matrix .CodeMirror-line > span::-moz-selection, .cm-s-the-matrix .CodeMirror-line > span > span::-moz-selection { background: rgba(45, 45, 45, 0.99); }
.cm-s-the-matrix .CodeMirror-gutters { background: #060; border-right: 2px solid #00FF00; }
.cm-s-the-matrix .CodeMirror-guttermarker { color: #0f0; }
.cm-s-the-matrix .CodeMirror-guttermarker-subtle { color: white; }
.cm-s-the-matrix .CodeMirror-linenumber { color: #FFFFFF; }
.cm-s-the-matrix .CodeMirror-cursor { border-left: 1px solid #00FF00; }

.cm-s-the-matrix span.cm-keyword { color: #008803; font-weight: bold; }
.cm-s-the-matrix span.cm-atom { color: #3FF; }
.cm-s-the-matrix span.cm-number { color: #FFB94F; }
.cm-s-the-matrix span.cm-def { color: #99C; }
.cm-s-the-matrix span.cm-variable { color: #F6C; }
.cm-s-the-matrix span.cm-variable-2 { color: #C6F; }
.cm-s-the-matrix span.cm-variable-3, .cm-s-the-matrix span.cm-type { color: #96F; }
.cm-s-the-matrix span.cm-property { color: #62FFA0; }
.cm-s-the-matrix span.cm-operator { color: #999; }
.cm-s-the-matrix span.cm-comment { color: #CCCCCC; }
.cm-s-the-matrix span.cm-string { color: #39C; }
.cm-s-the-matrix span.cm-meta { color: #C9F; }
.cm-s-the-matrix span.cm-qualifier { color: #FFF700; }
.cm-s-the-matrix span.cm-builtin { color: #30a; }
.cm-s-the-matrix span.cm-bracket { color: #cc7; }
.cm-s-the-matrix span.cm-tag { color: #FFBD40; }
.cm-s-the-matrix span.cm-attribute { color: #FFF700; }
.cm-s-the-matrix span.cm-error { color: #FF0000; }

.cm-s-the-matrix .CodeMirror-activeline-background { background: #040; }

/*
Copyright (C) 2011 by MarkLogic Corporation
Author: Mike Brevoort <mike@brevoort.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
*/
.cm-s-xq-light span.cm-keyword { line-height: 1em; font-weight: bold; color: #5A5CAD; }
.cm-s-xq-light span.cm-atom { color: #6C8CD5; }
.cm-s-xq-light span.cm-number { color: #164; }
.cm-s-xq-light span.cm-def { text-decoration:underline; }
.cm-s-xq-light span.cm-variable { color: black; }
.cm-s-xq-light span.cm-variable-2 { color:black; }
.cm-s-xq-light span.cm-variable-3, .cm-s-xq-light span.cm-type { color: black; }
.cm-s-xq-light span.cm-property {}
.cm-s-xq-light span.cm-operator {}
.cm-s-xq-light span.cm-comment { color: #0080FF; font-style: italic; }
.cm-s-xq-light span.cm-string { color: red; }
.cm-s-xq-light span.cm-meta { color: yellow; }
.cm-s-xq-light span.cm-qualifier { color: grey; }
.cm-s-xq-light span.cm-builtin { color: #7EA656; }
.cm-s-xq-light span.cm-bracket { color: #cc7; }
.cm-s-xq-light span.cm-tag { color: #3F7F7F; }
.cm-s-xq-light span.cm-attribute { color: #7F007F; }
.cm-s-xq-light span.cm-error { color: #f00; }

.cm-s-xq-light .CodeMirror-activeline-background { background: #e8f2ff; }
.cm-s-xq-light .CodeMirror-matchingbracket { outline:1px solid grey;color:black !important;background:yellow; }

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.CodeMirror {
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  border: 0;
  border-radius: 0;
  height: auto;
  /* Changed to auto to autogrow */
}

.CodeMirror pre {
  padding: 0 var(--jp-code-padding);
}

.jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-dialog {
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
}

/* This causes https://github.com/jupyter/jupyterlab/issues/522 */
/* May not cause it not because we changed it! */
.CodeMirror-lines {
  padding: var(--jp-code-padding) 0;
}

.CodeMirror-linenumber {
  padding: 0 8px;
}

.jp-CodeMirrorEditor-static {
  margin: var(--jp-code-padding);
}

.jp-CodeMirrorEditor,
.jp-CodeMirrorEditor-static {
  cursor: text;
}

.jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
  border-left: var(--jp-code-cursor-width0) solid var(--jp-editor-cursor-color);
}

/* When zoomed out 67% and 33% on a screen of 1440 width x 900 height */
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
    border-left: var(--jp-code-cursor-width1) solid
      var(--jp-editor-cursor-color);
  }
}

/* When zoomed out less than 33% */
@media screen and (min-width: 4320px) {
  .jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
    border-left: var(--jp-code-cursor-width2) solid
      var(--jp-editor-cursor-color);
  }
}

.CodeMirror.jp-mod-readOnly .CodeMirror-cursor {
  display: none;
}

.CodeMirror-gutters {
  border-right: 1px solid var(--jp-border-color2);
  background-color: var(--jp-layout-color0);
}

.jp-CollaboratorCursor {
  border-left: 5px solid transparent;
  border-right: 5px solid transparent;
  border-top: none;
  border-bottom: 3px solid;
  background-clip: content-box;
  margin-left: -5px;
  margin-right: -5px;
}

.CodeMirror-selectedtext.cm-searching {
  background-color: var(--jp-search-selected-match-background-color) !important;
  color: var(--jp-search-selected-match-color) !important;
}

.cm-searching {
  background-color: var(
    --jp-search-unselected-match-background-color
  ) !important;
  color: var(--jp-search-unselected-match-color) !important;
}

.CodeMirror-focused .CodeMirror-selected {
  background-color: var(--jp-editor-selected-focused-background);
}

.CodeMirror-selected {
  background-color: var(--jp-editor-selected-background);
}

.jp-CollaboratorCursor-hover {
  position: absolute;
  z-index: 1;
  transform: translateX(-50%);
  color: white;
  border-radius: 3px;
  padding-left: 4px;
  padding-right: 4px;
  padding-top: 1px;
  padding-bottom: 1px;
  text-align: center;
  font-size: var(--jp-ui-font-size1);
  white-space: nowrap;
}

.jp-CodeMirror-ruler {
  border-left: 1px dashed var(--jp-border-color2);
}

/**
 * Here is our jupyter theme for CodeMirror syntax highlighting
 * This is used in our marked.js syntax highlighting and CodeMirror itself
 * The string "jupyter" is set in ../codemirror/widget.DEFAULT_CODEMIRROR_THEME
 * This came from the classic notebook, which came form highlight.js/GitHub
 */

/**
 * CodeMirror themes are handling the background/color in this way. This works
 * fine for CodeMirror editors outside the notebook, but the notebook styles
 * these things differently.
 */
.CodeMirror.cm-s-jupyter {
  background: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
}

/* In the notebook, we want this styling to be handled by its container */
.jp-CodeConsole .CodeMirror.cm-s-jupyter,
.jp-Notebook .CodeMirror.cm-s-jupyter {
  background: transparent;
}

.cm-s-jupyter .CodeMirror-cursor {
  border-left: var(--jp-code-cursor-width0) solid var(--jp-editor-cursor-color);
}
.cm-s-jupyter span.cm-keyword {
  color: var(--jp-mirror-editor-keyword-color);
  font-weight: bold;
}
.cm-s-jupyter span.cm-atom {
  color: var(--jp-mirror-editor-atom-color);
}
.cm-s-jupyter span.cm-number {
  color: var(--jp-mirror-editor-number-color);
}
.cm-s-jupyter span.cm-def {
  color: var(--jp-mirror-editor-def-color);
}
.cm-s-jupyter span.cm-variable {
  color: var(--jp-mirror-editor-variable-color);
}
.cm-s-jupyter span.cm-variable-2 {
  color: var(--jp-mirror-editor-variable-2-color);
}
.cm-s-jupyter span.cm-variable-3 {
  color: var(--jp-mirror-editor-variable-3-color);
}
.cm-s-jupyter span.cm-punctuation {
  color: var(--jp-mirror-editor-punctuation-color);
}
.cm-s-jupyter span.cm-property {
  color: var(--jp-mirror-editor-property-color);
}
.cm-s-jupyter span.cm-operator {
  color: var(--jp-mirror-editor-operator-color);
  font-weight: bold;
}
.cm-s-jupyter span.cm-comment {
  color: var(--jp-mirror-editor-comment-color);
  font-style: italic;
}
.cm-s-jupyter span.cm-string {
  color: var(--jp-mirror-editor-string-color);
}
.cm-s-jupyter span.cm-string-2 {
  color: var(--jp-mirror-editor-string-2-color);
}
.cm-s-jupyter span.cm-meta {
  color: var(--jp-mirror-editor-meta-color);
}
.cm-s-jupyter span.cm-qualifier {
  color: var(--jp-mirror-editor-qualifier-color);
}
.cm-s-jupyter span.cm-builtin {
  color: var(--jp-mirror-editor-builtin-color);
}
.cm-s-jupyter span.cm-bracket {
  color: var(--jp-mirror-editor-bracket-color);
}
.cm-s-jupyter span.cm-tag {
  color: var(--jp-mirror-editor-tag-color);
}
.cm-s-jupyter span.cm-attribute {
  color: var(--jp-mirror-editor-attribute-color);
}
.cm-s-jupyter span.cm-header {
  color: var(--jp-mirror-editor-header-color);
}
.cm-s-jupyter span.cm-quote {
  color: var(--jp-mirror-editor-quote-color);
}
.cm-s-jupyter span.cm-link {
  color: var(--jp-mirror-editor-link-color);
}
.cm-s-jupyter span.cm-error {
  color: var(--jp-mirror-editor-error-color);
}
.cm-s-jupyter span.cm-hr {
  color: #999;
}

.cm-s-jupyter span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}

.cm-s-jupyter .CodeMirror-activeline-background,
.cm-s-jupyter .CodeMirror-gutter {
  background-color: var(--jp-layout-color2);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| RenderedText
|----------------------------------------------------------------------------*/

.jp-RenderedText {
  text-align: left;
  padding-left: var(--jp-code-padding);
  line-height: var(--jp-code-line-height);
  font-family: var(--jp-code-font-family);
}

.jp-RenderedText pre,
.jp-RenderedJavaScript pre,
.jp-RenderedHTMLCommon pre {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-code-font-size);
  border: none;
  margin: 0px;
  padding: 0px;
  line-height: normal;
}

.jp-RenderedText pre a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}
.jp-RenderedText pre a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}
.jp-RenderedText pre a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* console foregrounds and backgrounds */
.jp-RenderedText pre .ansi-black-fg {
  color: #3e424d;
}
.jp-RenderedText pre .ansi-red-fg {
  color: #e75c58;
}
.jp-RenderedText pre .ansi-green-fg {
  color: #00a250;
}
.jp-RenderedText pre .ansi-yellow-fg {
  color: #ddb62b;
}
.jp-RenderedText pre .ansi-blue-fg {
  color: #208ffb;
}
.jp-RenderedText pre .ansi-magenta-fg {
  color: #d160c4;
}
.jp-RenderedText pre .ansi-cyan-fg {
  color: #60c6c8;
}
.jp-RenderedText pre .ansi-white-fg {
  color: #c5c1b4;
}

.jp-RenderedText pre .ansi-black-bg {
  background-color: #3e424d;
}
.jp-RenderedText pre .ansi-red-bg {
  background-color: #e75c58;
}
.jp-RenderedText pre .ansi-green-bg {
  background-color: #00a250;
}
.jp-RenderedText pre .ansi-yellow-bg {
  background-color: #ddb62b;
}
.jp-RenderedText pre .ansi-blue-bg {
  background-color: #208ffb;
}
.jp-RenderedText pre .ansi-magenta-bg {
  background-color: #d160c4;
}
.jp-RenderedText pre .ansi-cyan-bg {
  background-color: #60c6c8;
}
.jp-RenderedText pre .ansi-white-bg {
  background-color: #c5c1b4;
}

.jp-RenderedText pre .ansi-black-intense-fg {
  color: #282c36;
}
.jp-RenderedText pre .ansi-red-intense-fg {
  color: #b22b31;
}
.jp-RenderedText pre .ansi-green-intense-fg {
  color: #007427;
}
.jp-RenderedText pre .ansi-yellow-intense-fg {
  color: #b27d12;
}
.jp-RenderedText pre .ansi-blue-intense-fg {
  color: #0065ca;
}
.jp-RenderedText pre .ansi-magenta-intense-fg {
  color: #a03196;
}
.jp-RenderedText pre .ansi-cyan-intense-fg {
  color: #258f8f;
}
.jp-RenderedText pre .ansi-white-intense-fg {
  color: #a1a6b2;
}

.jp-RenderedText pre .ansi-black-intense-bg {
  background-color: #282c36;
}
.jp-RenderedText pre .ansi-red-intense-bg {
  background-color: #b22b31;
}
.jp-RenderedText pre .ansi-green-intense-bg {
  background-color: #007427;
}
.jp-RenderedText pre .ansi-yellow-intense-bg {
  background-color: #b27d12;
}
.jp-RenderedText pre .ansi-blue-intense-bg {
  background-color: #0065ca;
}
.jp-RenderedText pre .ansi-magenta-intense-bg {
  background-color: #a03196;
}
.jp-RenderedText pre .ansi-cyan-intense-bg {
  background-color: #258f8f;
}
.jp-RenderedText pre .ansi-white-intense-bg {
  background-color: #a1a6b2;
}

.jp-RenderedText pre .ansi-default-inverse-fg {
  color: var(--jp-ui-inverse-font-color0);
}
.jp-RenderedText pre .ansi-default-inverse-bg {
  background-color: var(--jp-inverse-layout-color0);
}

.jp-RenderedText pre .ansi-bold {
  font-weight: bold;
}
.jp-RenderedText pre .ansi-underline {
  text-decoration: underline;
}

.jp-RenderedText[data-mime-type='application/vnd.jupyter.stderr'] {
  background: var(--jp-rendermime-error-background);
  padding-top: var(--jp-code-padding);
}

/*-----------------------------------------------------------------------------
| RenderedLatex
|----------------------------------------------------------------------------*/

.jp-RenderedLatex {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);
}

/* Left-justify outputs.*/
.jp-OutputArea-output.jp-RenderedLatex {
  padding: var(--jp-code-padding);
  text-align: left;
}

/*-----------------------------------------------------------------------------
| RenderedHTML
|----------------------------------------------------------------------------*/

.jp-RenderedHTMLCommon {
  color: var(--jp-content-font-color1);
  font-family: var(--jp-content-font-family);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);
  /* Give a bit more R padding on Markdown text to keep line lengths reasonable */
  padding-right: 20px;
}

.jp-RenderedHTMLCommon em {
  font-style: italic;
}

.jp-RenderedHTMLCommon strong {
  font-weight: bold;
}

.jp-RenderedHTMLCommon u {
  text-decoration: underline;
}

.jp-RenderedHTMLCommon a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* Headings */

.jp-RenderedHTMLCommon h1,
.jp-RenderedHTMLCommon h2,
.jp-RenderedHTMLCommon h3,
.jp-RenderedHTMLCommon h4,
.jp-RenderedHTMLCommon h5,
.jp-RenderedHTMLCommon h6 {
  line-height: var(--jp-content-heading-line-height);
  font-weight: var(--jp-content-heading-font-weight);
  font-style: normal;
  margin: var(--jp-content-heading-margin-top) 0
    var(--jp-content-heading-margin-bottom) 0;
}

.jp-RenderedHTMLCommon h1:first-child,
.jp-RenderedHTMLCommon h2:first-child,
.jp-RenderedHTMLCommon h3:first-child,
.jp-RenderedHTMLCommon h4:first-child,
.jp-RenderedHTMLCommon h5:first-child,
.jp-RenderedHTMLCommon h6:first-child {
  margin-top: calc(0.5 * var(--jp-content-heading-margin-top));
}

.jp-RenderedHTMLCommon h1:last-child,
.jp-RenderedHTMLCommon h2:last-child,
.jp-RenderedHTMLCommon h3:last-child,
.jp-RenderedHTMLCommon h4:last-child,
.jp-RenderedHTMLCommon h5:last-child,
.jp-RenderedHTMLCommon h6:last-child {
  margin-bottom: calc(0.5 * var(--jp-content-heading-margin-bottom));
}

.jp-RenderedHTMLCommon h1 {
  font-size: var(--jp-content-font-size5);
}

.jp-RenderedHTMLCommon h2 {
  font-size: var(--jp-content-font-size4);
}

.jp-RenderedHTMLCommon h3 {
  font-size: var(--jp-content-font-size3);
}

.jp-RenderedHTMLCommon h4 {
  font-size: var(--jp-content-font-size2);
}

.jp-RenderedHTMLCommon h5 {
  font-size: var(--jp-content-font-size1);
}

.jp-RenderedHTMLCommon h6 {
  font-size: var(--jp-content-font-size0);
}

/* Lists */

.jp-RenderedHTMLCommon ul:not(.list-inline),
.jp-RenderedHTMLCommon ol:not(.list-inline) {
  padding-left: 2em;
}

.jp-RenderedHTMLCommon ul {
  list-style: disc;
}

.jp-RenderedHTMLCommon ul ul {
  list-style: square;
}

.jp-RenderedHTMLCommon ul ul ul {
  list-style: circle;
}

.jp-RenderedHTMLCommon ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol ol {
  list-style: upper-alpha;
}

.jp-RenderedHTMLCommon ol ol ol {
  list-style: lower-alpha;
}

.jp-RenderedHTMLCommon ol ol ol ol {
  list-style: lower-roman;
}

.jp-RenderedHTMLCommon ol ol ol ol ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol,
.jp-RenderedHTMLCommon ul {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon ul ul,
.jp-RenderedHTMLCommon ul ol,
.jp-RenderedHTMLCommon ol ul,
.jp-RenderedHTMLCommon ol ol {
  margin-bottom: 0em;
}

.jp-RenderedHTMLCommon hr {
  color: var(--jp-border-color2);
  background-color: var(--jp-border-color1);
  margin-top: 1em;
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon > pre {
  margin: 1.5em 2em;
}

.jp-RenderedHTMLCommon pre,
.jp-RenderedHTMLCommon code {
  border: 0;
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  line-height: var(--jp-code-line-height);
  padding: 0;
  white-space: pre-wrap;
}

.jp-RenderedHTMLCommon :not(pre) > code {
  background-color: var(--jp-layout-color2);
  padding: 1px 5px;
}

/* Tables */

.jp-RenderedHTMLCommon table {
  border-collapse: collapse;
  border-spacing: 0;
  border: none;
  color: var(--jp-ui-font-color1);
  font-size: 12px;
  table-layout: fixed;
  margin-left: auto;
  margin-right: auto;
}

.jp-RenderedHTMLCommon thead {
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  vertical-align: bottom;
}

.jp-RenderedHTMLCommon td,
.jp-RenderedHTMLCommon th,
.jp-RenderedHTMLCommon tr {
  vertical-align: middle;
  padding: 0.5em 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}

.jp-RenderedMarkdown.jp-RenderedHTMLCommon td,
.jp-RenderedMarkdown.jp-RenderedHTMLCommon th {
  max-width: none;
}

:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon td,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon th,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon tr {
  text-align: right;
}

.jp-RenderedHTMLCommon th {
  font-weight: bold;
}

.jp-RenderedHTMLCommon tbody tr:nth-child(odd) {
  background: var(--jp-layout-color0);
}

.jp-RenderedHTMLCommon tbody tr:nth-child(even) {
  background: var(--jp-rendermime-table-row-background);
}

.jp-RenderedHTMLCommon tbody tr:hover {
  background: var(--jp-rendermime-table-row-hover-background);
}

.jp-RenderedHTMLCommon table {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon p {
  text-align: left;
  margin: 0px;
}

.jp-RenderedHTMLCommon p {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon img {
  -moz-force-broken-image-icon: 1;
}

/* Restrict to direct children as other images could be nested in other content. */
.jp-RenderedHTMLCommon > img {
  display: block;
  margin-left: 0;
  margin-right: 0;
  margin-bottom: 1em;
}

/* Change color behind transparent images if they need it... */
[data-jp-theme-light='false'] .jp-RenderedImage img.jp-needs-light-background {
  background-color: var(--jp-inverse-layout-color1);
}
[data-jp-theme-light='true'] .jp-RenderedImage img.jp-needs-dark-background {
  background-color: var(--jp-inverse-layout-color1);
}
/* ...or leave it untouched if they don't */
[data-jp-theme-light='false'] .jp-RenderedImage img.jp-needs-dark-background {
}
[data-jp-theme-light='true'] .jp-RenderedImage img.jp-needs-light-background {
}

.jp-RenderedHTMLCommon img,
.jp-RenderedImage img,
.jp-RenderedHTMLCommon svg,
.jp-RenderedSVG svg {
  max-width: 100%;
  height: auto;
}

.jp-RenderedHTMLCommon img.jp-mod-unconfined,
.jp-RenderedImage img.jp-mod-unconfined,
.jp-RenderedHTMLCommon svg.jp-mod-unconfined,
.jp-RenderedSVG svg.jp-mod-unconfined {
  max-width: none;
}

.jp-RenderedHTMLCommon .alert {
  padding: var(--jp-notebook-padding);
  border: var(--jp-border-width) solid transparent;
  border-radius: var(--jp-border-radius);
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon .alert-info {
  color: var(--jp-info-color0);
  background-color: var(--jp-info-color3);
  border-color: var(--jp-info-color2);
}
.jp-RenderedHTMLCommon .alert-info hr {
  border-color: var(--jp-info-color3);
}
.jp-RenderedHTMLCommon .alert-info > p:last-child,
.jp-RenderedHTMLCommon .alert-info > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-warning {
  color: var(--jp-warn-color0);
  background-color: var(--jp-warn-color3);
  border-color: var(--jp-warn-color2);
}
.jp-RenderedHTMLCommon .alert-warning hr {
  border-color: var(--jp-warn-color3);
}
.jp-RenderedHTMLCommon .alert-warning > p:last-child,
.jp-RenderedHTMLCommon .alert-warning > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-success {
  color: var(--jp-success-color0);
  background-color: var(--jp-success-color3);
  border-color: var(--jp-success-color2);
}
.jp-RenderedHTMLCommon .alert-success hr {
  border-color: var(--jp-success-color3);
}
.jp-RenderedHTMLCommon .alert-success > p:last-child,
.jp-RenderedHTMLCommon .alert-success > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-danger {
  color: var(--jp-error-color0);
  background-color: var(--jp-error-color3);
  border-color: var(--jp-error-color2);
}
.jp-RenderedHTMLCommon .alert-danger hr {
  border-color: var(--jp-error-color3);
}
.jp-RenderedHTMLCommon .alert-danger > p:last-child,
.jp-RenderedHTMLCommon .alert-danger > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon blockquote {
  margin: 1em 2em;
  padding: 0 1em;
  border-left: 5px solid var(--jp-border-color2);
}

a.jp-InternalAnchorLink {
  visibility: hidden;
  margin-left: 8px;
  color: var(--md-blue-800);
}

h1:hover .jp-InternalAnchorLink,
h2:hover .jp-InternalAnchorLink,
h3:hover .jp-InternalAnchorLink,
h4:hover .jp-InternalAnchorLink,
h5:hover .jp-InternalAnchorLink,
h6:hover .jp-InternalAnchorLink {
  visibility: visible;
}

.jp-RenderedHTMLCommon kbd {
  background-color: var(--jp-rendermime-table-row-background);
  border: 1px solid var(--jp-border-color0);
  border-bottom-color: var(--jp-border-color2);
  border-radius: 3px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
  display: inline-block;
  font-size: 0.8em;
  line-height: 1em;
  padding: 0.2em 0.5em;
}

/* Most direct children of .jp-RenderedHTMLCommon have a margin-bottom of 1.0.
 * At the bottom of cells this is a bit too much as there is also spacing
 * between cells. Going all the way to 0 gets too tight between markdown and
 * code cells.
 */
.jp-RenderedHTMLCommon > *:last-child {
  margin-bottom: 0.5em;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MimeDocument {
  outline: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-filebrowser-button-height: 28px;
  --jp-private-filebrowser-button-width: 48px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-FileBrowser {
  display: flex;
  flex-direction: column;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  border-bottom: none;
  height: auto;
  margin: var(--jp-toolbar-header-margin);
  box-shadow: none;
}

.jp-BreadCrumbs {
  flex: 0 0 auto;
  margin: 4px 12px;
}

.jp-BreadCrumbs-item {
  margin: 0px 2px;
  padding: 0px 2px;
  border-radius: var(--jp-border-radius);
  cursor: pointer;
}

.jp-BreadCrumbs-item:hover {
  background-color: var(--jp-layout-color2);
}

.jp-BreadCrumbs-item:first-child {
  margin-left: 0px;
}

.jp-BreadCrumbs-item.jp-mod-dropTarget {
  background-color: var(--jp-brand-color2);
  opacity: 0.7;
}

/*-----------------------------------------------------------------------------
| Buttons
|----------------------------------------------------------------------------*/

.jp-FileBrowser-toolbar.jp-Toolbar {
  padding: 0px;
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  justify-content: space-evenly;
}

.jp-FileBrowser-toolbar.jp-Toolbar .jp-Toolbar-item {
  flex: 1;
}

.jp-FileBrowser-toolbar.jp-Toolbar .jp-ToolbarButtonComponent {
  width: 100%;
}

/*-----------------------------------------------------------------------------
| DirListing
|----------------------------------------------------------------------------*/

.jp-DirListing {
  flex: 1 1 auto;
  display: flex;
  flex-direction: column;
  outline: 0;
}

.jp-DirListing-header {
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  overflow: hidden;
  border-top: var(--jp-border-width) solid var(--jp-border-color2);
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  box-shadow: var(--jp-toolbar-box-shadow);
  z-index: 2;
}

.jp-DirListing-headerItem {
  padding: 4px 12px 2px 12px;
  font-weight: 500;
}

.jp-DirListing-headerItem:hover {
  background: var(--jp-layout-color2);
}

.jp-DirListing-headerItem.jp-id-name {
  flex: 1 0 84px;
}

.jp-DirListing-headerItem.jp-id-modified {
  flex: 0 0 112px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
}

.jp-DirListing-narrow .jp-id-modified,
.jp-DirListing-narrow .jp-DirListing-itemModified {
  display: none;
}

.jp-DirListing-headerItem.jp-mod-selected {
  font-weight: 600;
}

/* increase specificity to override bundled default */
.jp-DirListing-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  list-style-type: none;
  overflow: auto;
  background-color: var(--jp-layout-color1);
}

/* Style the directory listing content when a user drops a file to upload */
.jp-DirListing.jp-mod-native-drop .jp-DirListing-content {
  outline: 5px dashed rgba(128, 128, 128, 0.5);
  outline-offset: -10px;
  cursor: copy;
}

.jp-DirListing-item {
  display: flex;
  flex-direction: row;
  padding: 4px 12px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-DirListing-item.jp-mod-selected {
  color: white;
  background: var(--jp-brand-color1);
}

.jp-DirListing-item.jp-mod-dropTarget {
  background: var(--jp-brand-color3);
}

.jp-DirListing-item:hover:not(.jp-mod-selected) {
  background: var(--jp-layout-color2);
}

.jp-DirListing-itemIcon {
  flex: 0 0 20px;
  margin-right: 4px;
}

.jp-DirListing-itemText {
  flex: 1 0 64px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  user-select: none;
}

.jp-DirListing-itemModified {
  flex: 0 0 125px;
  text-align: right;
}

.jp-DirListing-editor {
  flex: 1 0 64px;
  outline: none;
  border: none;
}

.jp-DirListing-item.jp-mod-running .jp-DirListing-itemIcon:before {
  color: limegreen;
  content: '\25CF';
  font-size: 8px;
  position: absolute;
  left: -8px;
}

.jp-DirListing-item.lm-mod-drag-image,
.jp-DirListing-item.jp-mod-selected.lm-mod-drag-image {
  font-size: var(--jp-ui-font-size1);
  padding-left: 4px;
  margin-left: 4px;
  width: 160px;
  background-color: var(--jp-ui-inverse-font-color2);
  box-shadow: var(--jp-elevation-z2);
  border-radius: 0px;
  color: var(--jp-ui-font-color1);
  transform: translateX(-40%) translateY(-58%);
}

.jp-DirListing-deadSpace {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  list-style-type: none;
  overflow: auto;
  background-color: var(--jp-layout-color1);
}

.jp-Document {
  min-width: 120px;
  min-height: 120px;
  outline: none;
}

.jp-FileDialog.jp-mod-conflict input {
  color: red;
}

.jp-FileDialog .jp-new-name-title {
  margin-top: 12px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
}

/*-----------------------------------------------------------------------------
| Main OutputArea
| OutputArea has a list of Outputs
|----------------------------------------------------------------------------*/

.jp-OutputArea {
  overflow-y: auto;
}

.jp-OutputArea-child {
  display: flex;
  flex-direction: row;
}

.jp-OutputPrompt {
  flex: 0 0 var(--jp-cell-prompt-width);
  color: var(--jp-cell-outprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
  opacity: var(--jp-cell-prompt-opacity);
  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-OutputArea-output {
  height: auto;
  overflow: auto;
  user-select: text;
  -moz-user-select: text;
  -webkit-user-select: text;
  -ms-user-select: text;
}

.jp-OutputArea-child .jp-OutputArea-output {
  flex-grow: 1;
  flex-shrink: 1;
}

/**
 * Isolated output.
 */
.jp-OutputArea-output.jp-mod-isolated {
  width: 100%;
  display: block;
}

/*
When drag events occur, `p-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated {
  position: relative;
}

body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

/* pre */

.jp-OutputArea-output pre {
  border: none;
  margin: 0px;
  padding: 0px;
  overflow-x: auto;
  overflow-y: auto;
  word-break: break-all;
  word-wrap: break-word;
  white-space: pre-wrap;
}

/* tables */

.jp-OutputArea-output.jp-RenderedHTMLCommon table {
  margin-left: 0;
  margin-right: 0;
}

/* description lists */

.jp-OutputArea-output dl,
.jp-OutputArea-output dt,
.jp-OutputArea-output dd {
  display: block;
}

.jp-OutputArea-output dl {
  width: 100%;
  overflow: hidden;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dt {
  font-weight: bold;
  float: left;
  width: 20%;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dd {
  float: left;
  width: 80%;
  padding: 0;
  margin: 0;
}

/* Hide the gutter in case of
 *  - nested output areas (e.g. in the case of output widgets)
 *  - mirrored output areas
 */
.jp-OutputArea .jp-OutputArea .jp-OutputArea-prompt {
  display: none;
}

/*-----------------------------------------------------------------------------
| executeResult is added to any Output-result for the display of the object
| returned by a cell
|----------------------------------------------------------------------------*/

.jp-OutputArea-output.jp-OutputArea-executeResult {
  margin-left: 0px;
  flex: 1 1 auto;
}

.jp-OutputArea-executeResult.jp-RenderedText {
  padding-top: var(--jp-code-padding);
}

/*-----------------------------------------------------------------------------
| The Stdin output
|----------------------------------------------------------------------------*/

.jp-OutputArea-stdin {
  line-height: var(--jp-code-line-height);
  padding-top: var(--jp-code-padding);
  display: flex;
}

.jp-Stdin-prompt {
  color: var(--jp-content-font-color0);
  padding-right: var(--jp-code-padding);
  vertical-align: baseline;
  flex: 0 0 auto;
}

.jp-Stdin-input {
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  color: inherit;
  background-color: inherit;
  width: 42%;
  min-width: 200px;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
  flex: 0 0 70%;
}

.jp-Stdin-input:focus {
  box-shadow: none;
}

/*-----------------------------------------------------------------------------
| Output Area View
|----------------------------------------------------------------------------*/

.jp-LinkedOutputView .jp-OutputArea {
  height: 100%;
  display: block;
}

.jp-LinkedOutputView .jp-OutputArea-output:only-child {
  height: 100%;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapser {
  flex: 0 0 var(--jp-cell-collapser-width);
  padding: 0px;
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
  border-radius: var(--jp-border-radius);
  opacity: 1;
}

.jp-Collapser-child {
  display: block;
  width: 100%;
  box-sizing: border-box;
  /* height: 100% doesn't work because the height of its parent is computed from content */
  position: absolute;
  top: 0px;
  bottom: 0px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Header/Footer
|----------------------------------------------------------------------------*/

/* Hidden by zero height by default */
.jp-CellHeader,
.jp-CellFooter {
  height: 0px;
  width: 100%;
  padding: 0px;
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Input
|----------------------------------------------------------------------------*/

/* All input areas */
.jp-InputArea {
  display: flex;
  flex-direction: row;
}

.jp-InputArea-editor {
  flex: 1 1 auto;
}

.jp-InputArea-editor {
  /* This is the non-active, default styling */
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  border-radius: 0px;
  background: var(--jp-cell-editor-background);
}

.jp-InputPrompt {
  flex: 0 0 var(--jp-cell-prompt-width);
  color: var(--jp-cell-inprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  opacity: var(--jp-cell-prompt-opacity);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
  opacity: var(--jp-cell-prompt-opacity);
  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Placeholder
|----------------------------------------------------------------------------*/

.jp-Placeholder {
  display: flex;
  flex-direction: row;
  flex: 1 1 auto;
}

.jp-Placeholder-prompt {
  box-sizing: border-box;
}

.jp-Placeholder-content {
  flex: 1 1 auto;
  border: none;
  background: transparent;
  height: 20px;
  box-sizing: border-box;
}

.jp-Placeholder-content .jp-MoreHorizIcon {
  width: 32px;
  height: 16px;
  border: 1px solid transparent;
  border-radius: var(--jp-border-radius);
}

.jp-Placeholder-content .jp-MoreHorizIcon:hover {
  border: 1px solid var(--jp-border-color1);
  box-shadow: 0px 0px 2px 0px rgba(0, 0, 0, 0.25);
  background-color: var(--jp-layout-color0);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-cell-scrolling-output-offset: 5px;
}

/*-----------------------------------------------------------------------------
| Cell
|----------------------------------------------------------------------------*/

.jp-Cell {
  padding: var(--jp-cell-padding);
  margin: 0px;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Common input/output
|----------------------------------------------------------------------------*/

.jp-Cell-inputWrapper,
.jp-Cell-outputWrapper {
  display: flex;
  flex-direction: row;
  padding: 0px;
  margin: 0px;
  /* Added to reveal the box-shadow on the input and output collapsers. */
  overflow: visible;
}

/* Only input/output areas inside cells */
.jp-Cell-inputArea,
.jp-Cell-outputArea {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Collapser
|----------------------------------------------------------------------------*/

/* Make the output collapser disappear when there is not output, but do so
 * in a manner that leaves it in the layout and preserves its width.
 */
.jp-Cell.jp-mod-noOutputs .jp-Cell-outputCollapser {
  border: none !important;
  background: transparent !important;
}

.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputCollapser {
  min-height: var(--jp-cell-collapser-min-height);
}

/*-----------------------------------------------------------------------------
| Output
|----------------------------------------------------------------------------*/

/* Put a space between input and output when there IS output */
.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputWrapper {
  margin-top: 5px;
}

/* Text output with the Out[] prompt needs a top padding to match the
 * alignment of the Out[] prompt itself.
 */
.jp-OutputArea-executeResult .jp-RenderedText.jp-OutputArea-output {
  padding-top: var(--jp-code-padding);
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-Cell-outputArea {
  overflow-y: auto;
  max-height: 200px;
  box-shadow: inset 0 0 6px 2px rgba(0, 0, 0, 0.3);
  margin-left: var(--jp-private-cell-scrolling-output-offset);
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-prompt {
  flex: 0 0
    calc(
      var(--jp-cell-prompt-width) -
        var(--jp-private-cell-scrolling-output-offset)
    );
}

/*-----------------------------------------------------------------------------
| CodeCell
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| MarkdownCell
|----------------------------------------------------------------------------*/

.jp-MarkdownOutput {
  flex: 1 1 auto;
  margin-top: 0;
  margin-bottom: 0;
  padding-left: var(--jp-code-padding);
}

.jp-MarkdownOutput.jp-RenderedHTMLCommon {
  overflow: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------

/*-----------------------------------------------------------------------------
| Styles
|----------------------------------------------------------------------------*/

.jp-NotebookPanel-toolbar {
  padding: 2px;
}

.jp-Toolbar-item.jp-Notebook-toolbarCellType .jp-select-wrapper.jp-mod-focused {
  border: none;
  box-shadow: none;
}

.jp-Notebook-toolbarCellTypeDropdown select {
  height: 24px;
  font-size: var(--jp-ui-font-size1);
  line-height: 14px;
  border-radius: 0;
  display: block;
}

.jp-Notebook-toolbarCellTypeDropdown span {
  top: 5px !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-notebook-dragImage-width: 304px;
  --jp-private-notebook-dragImage-height: 36px;
  --jp-private-notebook-selected-color: var(--md-blue-400);
  --jp-private-notebook-active-color: var(--md-green-400);
}

/*-----------------------------------------------------------------------------
| Imports
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Notebook
|----------------------------------------------------------------------------*/

.jp-NotebookPanel {
  display: block;
  height: 100%;
}

.jp-NotebookPanel.jp-Document {
  min-width: 240px;
  min-height: 120px;
}

.jp-Notebook {
  padding: var(--jp-notebook-padding);
  outline: none;
  overflow: auto;
  background: var(--jp-layout-color0);
}

.jp-Notebook.jp-mod-scrollPastEnd::after {
  display: block;
  content: '';
  min-height: var(--jp-notebook-scroll-padding);
}

.jp-Notebook .jp-Cell {
  overflow: visible;
}

.jp-Notebook .jp-Cell .jp-InputPrompt {
  cursor: move;
}

/*-----------------------------------------------------------------------------
| Notebook state related styling
|
| The notebook and cells each have states, here are the possibilities:
|
| - Notebook
|   - Command
|   - Edit
| - Cell
|   - None
|   - Active (only one can be active)
|   - Selected (the cells actions are applied to)
|   - Multiselected (when multiple selected, the cursor)
|   - No outputs
|----------------------------------------------------------------------------*/

/* Command or edit modes */

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-InputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-OutputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

/* cell is active */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser {
  background: var(--jp-brand-color1);
}

/* collapser is hovered */
.jp-Notebook .jp-Cell .jp-Collapser:hover {
  box-shadow: var(--jp-elevation-z2);
  background: var(--jp-brand-color1);
  opacity: var(--jp-cell-collapser-not-active-hover-opacity);
}

/* cell is active and collapser is hovered */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser:hover {
  background: var(--jp-brand-color0);
  opacity: 1;
}

/* Command mode */

.jp-Notebook.jp-mod-commandMode .jp-Cell.jp-mod-selected {
  background: var(--jp-notebook-multiselected-color);
}

.jp-Notebook.jp-mod-commandMode
  .jp-Cell.jp-mod-active.jp-mod-selected:not(.jp-mod-multiSelected) {
  background: transparent;
}

/* Edit mode */

.jp-Notebook.jp-mod-editMode .jp-Cell.jp-mod-active .jp-InputArea-editor {
  border: var(--jp-border-width) solid var(--jp-cell-editor-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-cell-editor-active-background);
}

/*-----------------------------------------------------------------------------
| Notebook drag and drop
|----------------------------------------------------------------------------*/

.jp-Notebook-cell.jp-mod-dropSource {
  opacity: 0.5;
}

.jp-Notebook-cell.jp-mod-dropTarget,
.jp-Notebook.jp-mod-commandMode
  .jp-Notebook-cell.jp-mod-active.jp-mod-selected.jp-mod-dropTarget {
  border-top-color: var(--jp-private-notebook-selected-color);
  border-top-style: solid;
  border-top-width: 2px;
}

.jp-dragImage {
  display: flex;
  flex-direction: row;
  width: var(--jp-private-notebook-dragImage-width);
  height: var(--jp-private-notebook-dragImage-height);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background);
  overflow: visible;
}

.jp-dragImage-singlePrompt {
  box-shadow: 2px 2px 4px 0px rgba(0, 0, 0, 0.12);
}

.jp-dragImage .jp-dragImage-content {
  flex: 1 1 auto;
  z-index: 2;
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  line-height: var(--jp-code-line-height);
  padding: var(--jp-code-padding);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background-color);
  color: var(--jp-content-font-color3);
  text-align: left;
  margin: 4px 4px 4px 0px;
}

.jp-dragImage .jp-dragImage-prompt {
  flex: 0 0 auto;
  min-width: 36px;
  color: var(--jp-cell-inprompt-font-color);
  padding: var(--jp-code-padding);
  padding-left: 12px;
  font-family: var(--jp-cell-prompt-font-family);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: 1.9;
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
}

.jp-dragImage-multipleBack {
  z-index: -1;
  position: absolute;
  height: 32px;
  width: 300px;
  top: 8px;
  left: 8px;
  background: var(--jp-layout-color2);
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  box-shadow: 2px 2px 4px 0px rgba(0, 0, 0, 0.12);
}

/*-----------------------------------------------------------------------------
| Cell toolbar
|----------------------------------------------------------------------------*/

.jp-NotebookTools {
  display: block;
  min-width: var(--jp-sidebar-min-width);
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
    * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  overflow: auto;
}

.jp-NotebookTools-tool {
  padding: 0px 12px 0 12px;
}

.jp-ActiveCellTool {
  padding: 12px;
  background-color: var(--jp-layout-color1);
  border-top: none !important;
}

.jp-ActiveCellTool .jp-InputArea-prompt {
  flex: 0 0 auto;
  padding-left: 0px;
}

.jp-ActiveCellTool .jp-InputArea-editor {
  flex: 1 1 auto;
  background: var(--jp-cell-editor-background);
  border-color: var(--jp-cell-editor-border-color);
}

.jp-ActiveCellTool .jp-InputArea-editor .CodeMirror {
  background: transparent;
}

.jp-MetadataEditorTool {
  flex-direction: column;
  padding: 12px 0px 12px 0px;
}

.jp-RankedPanel > :not(:first-child) {
  margin-top: 12px;
}

.jp-KeySelector select.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: var(--jp-border-width) solid var(--jp-border-color1);
}

.jp-KeySelector label,
.jp-MetadataEditorTool label {
  line-height: 1.4;
}

/*-----------------------------------------------------------------------------
| Presentation Mode (.jp-mod-presentationMode)
|----------------------------------------------------------------------------*/

.jp-mod-presentationMode .jp-Notebook {
  --jp-content-font-size1: var(--jp-content-presentation-font-size1);
  --jp-code-font-size: var(--jp-code-presentation-font-size);
}

.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-InputPrompt,
.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-OutputPrompt {
  flex: 0 0 110px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

</style>

    <style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
The following CSS variables define the main, public API for styling JupyterLab.
These variables should be used by all plugins wherever possible. In other
words, plugins should not define custom colors, sizes, etc unless absolutely
necessary. This enables users to change the visual theme of JupyterLab
by changing these variables.

Many variables appear in an ordered sequence (0,1,2,3). These sequences
are designed to work well together, so for example, `--jp-border-color1` should
be used with `--jp-layout-color1`. The numbers have the following meanings:

* 0: super-primary, reserved for special emphasis
* 1: primary, most important under normal situations
* 2: secondary, next most important under normal situations
* 3: tertiary, next most important under normal situations

Throughout JupyterLab, we are mostly following principles from Google's
Material Design when selecting colors. We are not, however, following
all of MD as it is not optimized for dense, information rich UIs.
*/

:root {
  /* Elevation
   *
   * We style box-shadows using Material Design's idea of elevation. These particular numbers are taken from here:
   *
   * https://github.com/material-components/material-components-web
   * https://material-components-web.appspot.com/elevation.html
   */

  --jp-shadow-base-lightness: 0;
  --jp-shadow-umbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.2
  );
  --jp-shadow-penumbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.14
  );
  --jp-shadow-ambient-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.12
  );
  --jp-elevation-z0: none;
  --jp-elevation-z1: 0px 2px 1px -1px var(--jp-shadow-umbra-color),
    0px 1px 1px 0px var(--jp-shadow-penumbra-color),
    0px 1px 3px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z2: 0px 3px 1px -2px var(--jp-shadow-umbra-color),
    0px 2px 2px 0px var(--jp-shadow-penumbra-color),
    0px 1px 5px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z4: 0px 2px 4px -1px var(--jp-shadow-umbra-color),
    0px 4px 5px 0px var(--jp-shadow-penumbra-color),
    0px 1px 10px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z6: 0px 3px 5px -1px var(--jp-shadow-umbra-color),
    0px 6px 10px 0px var(--jp-shadow-penumbra-color),
    0px 1px 18px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z8: 0px 5px 5px -3px var(--jp-shadow-umbra-color),
    0px 8px 10px 1px var(--jp-shadow-penumbra-color),
    0px 3px 14px 2px var(--jp-shadow-ambient-color);
  --jp-elevation-z12: 0px 7px 8px -4px var(--jp-shadow-umbra-color),
    0px 12px 17px 2px var(--jp-shadow-penumbra-color),
    0px 5px 22px 4px var(--jp-shadow-ambient-color);
  --jp-elevation-z16: 0px 8px 10px -5px var(--jp-shadow-umbra-color),
    0px 16px 24px 2px var(--jp-shadow-penumbra-color),
    0px 6px 30px 5px var(--jp-shadow-ambient-color);
  --jp-elevation-z20: 0px 10px 13px -6px var(--jp-shadow-umbra-color),
    0px 20px 31px 3px var(--jp-shadow-penumbra-color),
    0px 8px 38px 7px var(--jp-shadow-ambient-color);
  --jp-elevation-z24: 0px 11px 15px -7px var(--jp-shadow-umbra-color),
    0px 24px 38px 3px var(--jp-shadow-penumbra-color),
    0px 9px 46px 8px var(--jp-shadow-ambient-color);

  /* Borders
   *
   * The following variables, specify the visual styling of borders in JupyterLab.
   */

  --jp-border-width: 1px;
  --jp-border-color0: var(--md-grey-400);
  --jp-border-color1: var(--md-grey-400);
  --jp-border-color2: var(--md-grey-300);
  --jp-border-color3: var(--md-grey-200);
  --jp-border-radius: 2px;

  /* UI Fonts
   *
   * The UI font CSS variables are used for the typography all of the JupyterLab
   * user interface elements that are not directly user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-ui-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-ui-font-scale-factor: 1.2;
  --jp-ui-font-size0: 0.83333em;
  --jp-ui-font-size1: 13px; /* Base font size */
  --jp-ui-font-size2: 1.2em;
  --jp-ui-font-size3: 1.44em;

  --jp-ui-font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica,
    Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol';

  /*
   * Use these font colors against the corresponding main layout colors.
   * In a light theme, these go from dark to light.
   */

  /* Defaults use Material Design specification */
  --jp-ui-font-color0: rgba(0, 0, 0, 1);
  --jp-ui-font-color1: rgba(0, 0, 0, 0.87);
  --jp-ui-font-color2: rgba(0, 0, 0, 0.54);
  --jp-ui-font-color3: rgba(0, 0, 0, 0.38);

  /*
   * Use these against the brand/accent/warn/error colors.
   * These will typically go from light to darker, in both a dark and light theme.
   */

  --jp-ui-inverse-font-color0: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color1: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color2: rgba(255, 255, 255, 0.7);
  --jp-ui-inverse-font-color3: rgba(255, 255, 255, 0.5);

  /* Content Fonts
   *
   * Content font variables are used for typography of user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-content-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-content-line-height: 1.6;
  --jp-content-font-scale-factor: 1.2;
  --jp-content-font-size0: 0.83333em;
  --jp-content-font-size1: 14px; /* Base font size */
  --jp-content-font-size2: 1.2em;
  --jp-content-font-size3: 1.44em;
  --jp-content-font-size4: 1.728em;
  --jp-content-font-size5: 2.0736em;

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-content-presentation-font-size1: 17px;

  --jp-content-heading-line-height: 1;
  --jp-content-heading-margin-top: 1.2em;
  --jp-content-heading-margin-bottom: 0.8em;
  --jp-content-heading-font-weight: 500;

  /* Defaults use Material Design specification */
  --jp-content-font-color0: rgba(0, 0, 0, 1);
  --jp-content-font-color1: rgba(0, 0, 0, 0.87);
  --jp-content-font-color2: rgba(0, 0, 0, 0.54);
  --jp-content-font-color3: rgba(0, 0, 0, 0.38);

  --jp-content-link-color: var(--md-blue-700);

  --jp-content-font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji',
    'Segoe UI Symbol';

  /*
   * Code Fonts
   *
   * Code font variables are used for typography of code and other monospaces content.
   */

  --jp-code-font-size: 13px;
  --jp-code-line-height: 1.3077; /* 17px for 13px base */
  --jp-code-padding: 5px; /* 5px for 13px base, codemirror highlighting needs integer px value */
  --jp-code-font-family-default: Menlo, Consolas, 'DejaVu Sans Mono', monospace;
  --jp-code-font-family: var(--jp-code-font-family-default);

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-code-presentation-font-size: 16px;

  /* may need to tweak cursor width if you change font size */
  --jp-code-cursor-width0: 1.4px;
  --jp-code-cursor-width1: 2px;
  --jp-code-cursor-width2: 4px;

  /* Layout
   *
   * The following are the main layout colors use in JupyterLab. In a light
   * theme these would go from light to dark.
   */

  --jp-layout-color0: white;
  --jp-layout-color1: white;
  --jp-layout-color2: var(--md-grey-200);
  --jp-layout-color3: var(--md-grey-400);
  --jp-layout-color4: var(--md-grey-600);

  /* Inverse Layout
   *
   * The following are the inverse layout colors use in JupyterLab. In a light
   * theme these would go from dark to light.
   */

  --jp-inverse-layout-color0: #111111;
  --jp-inverse-layout-color1: var(--md-grey-900);
  --jp-inverse-layout-color2: var(--md-grey-800);
  --jp-inverse-layout-color3: var(--md-grey-700);
  --jp-inverse-layout-color4: var(--md-grey-600);

  /* Brand/accent */

  --jp-brand-color0: var(--md-blue-700);
  --jp-brand-color1: var(--md-blue-500);
  --jp-brand-color2: var(--md-blue-300);
  --jp-brand-color3: var(--md-blue-100);
  --jp-brand-color4: var(--md-blue-50);

  --jp-accent-color0: var(--md-green-700);
  --jp-accent-color1: var(--md-green-500);
  --jp-accent-color2: var(--md-green-300);
  --jp-accent-color3: var(--md-green-100);

  /* State colors (warn, error, success, info) */

  --jp-warn-color0: var(--md-orange-700);
  --jp-warn-color1: var(--md-orange-500);
  --jp-warn-color2: var(--md-orange-300);
  --jp-warn-color3: var(--md-orange-100);

  --jp-error-color0: var(--md-red-700);
  --jp-error-color1: var(--md-red-500);
  --jp-error-color2: var(--md-red-300);
  --jp-error-color3: var(--md-red-100);

  --jp-success-color0: var(--md-green-700);
  --jp-success-color1: var(--md-green-500);
  --jp-success-color2: var(--md-green-300);
  --jp-success-color3: var(--md-green-100);

  --jp-info-color0: var(--md-cyan-700);
  --jp-info-color1: var(--md-cyan-500);
  --jp-info-color2: var(--md-cyan-300);
  --jp-info-color3: var(--md-cyan-100);

  /* Cell specific styles */

  --jp-cell-padding: 5px;

  --jp-cell-collapser-width: 8px;
  --jp-cell-collapser-min-height: 20px;
  --jp-cell-collapser-not-active-hover-opacity: 0.6;

  --jp-cell-editor-background: var(--md-grey-100);
  --jp-cell-editor-border-color: var(--md-grey-300);
  --jp-cell-editor-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-cell-editor-active-background: var(--jp-layout-color0);
  --jp-cell-editor-active-border-color: var(--jp-brand-color1);

  --jp-cell-prompt-width: 64px;
  --jp-cell-prompt-font-family: 'Source Code Pro', monospace;
  --jp-cell-prompt-letter-spacing: 0px;
  --jp-cell-prompt-opacity: 1;
  --jp-cell-prompt-not-active-opacity: 0.5;
  --jp-cell-prompt-not-active-font-color: var(--md-grey-700);
  /* A custom blend of MD grey and blue 600
   * See https://meyerweb.com/eric/tools/color-blend/#546E7A:1E88E5:5:hex */
  --jp-cell-inprompt-font-color: #307fc1;
  /* A custom blend of MD grey and orange 600
   * https://meyerweb.com/eric/tools/color-blend/#546E7A:F4511E:5:hex */
  --jp-cell-outprompt-font-color: #bf5b3d;

  /* Notebook specific styles */

  --jp-notebook-padding: 10px;
  --jp-notebook-select-background: var(--jp-layout-color1);
  --jp-notebook-multiselected-color: var(--md-blue-50);

  /* The scroll padding is calculated to fill enough space at the bottom of the
  notebook to show one single-line cell (with appropriate padding) at the top
  when the notebook is scrolled all the way to the bottom. We also subtract one
  pixel so that no scrollbar appears if we have just one single-line cell in the
  notebook. This padding is to enable a 'scroll past end' feature in a notebook.
  */
  --jp-notebook-scroll-padding: calc(
    100% - var(--jp-code-font-size) * var(--jp-code-line-height) -
      var(--jp-code-padding) - var(--jp-cell-padding) - 1px
  );

  /* Rendermime styles */

  --jp-rendermime-error-background: #fdd;
  --jp-rendermime-table-row-background: var(--md-grey-100);
  --jp-rendermime-table-row-hover-background: var(--md-light-blue-50);

  /* Dialog specific styles */

  --jp-dialog-background: rgba(0, 0, 0, 0.25);

  /* Console specific styles */

  --jp-console-padding: 10px;

  /* Toolbar specific styles */

  --jp-toolbar-border-color: var(--jp-border-color1);
  --jp-toolbar-micro-height: 8px;
  --jp-toolbar-background: var(--jp-layout-color1);
  --jp-toolbar-box-shadow: 0px 0px 2px 0px rgba(0, 0, 0, 0.24);
  --jp-toolbar-header-margin: 4px 4px 0px 4px;
  --jp-toolbar-active-background: var(--md-grey-300);

  /* Input field styles */

  --jp-input-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-input-active-background: var(--jp-layout-color1);
  --jp-input-hover-background: var(--jp-layout-color1);
  --jp-input-background: var(--md-grey-100);
  --jp-input-border-color: var(--jp-border-color1);
  --jp-input-active-border-color: var(--jp-brand-color1);
  --jp-input-active-box-shadow-color: rgba(19, 124, 189, 0.3);

  /* General editor styles */

  --jp-editor-selected-background: #d9d9d9;
  --jp-editor-selected-focused-background: #d7d4f0;
  --jp-editor-cursor-color: var(--jp-ui-font-color0);

  /* Code mirror specific styles */

  --jp-mirror-editor-keyword-color: #008000;
  --jp-mirror-editor-atom-color: #88f;
  --jp-mirror-editor-number-color: #080;
  --jp-mirror-editor-def-color: #00f;
  --jp-mirror-editor-variable-color: var(--md-grey-900);
  --jp-mirror-editor-variable-2-color: #05a;
  --jp-mirror-editor-variable-3-color: #085;
  --jp-mirror-editor-punctuation-color: #05a;
  --jp-mirror-editor-property-color: #05a;
  --jp-mirror-editor-operator-color: #aa22ff;
  --jp-mirror-editor-comment-color: #408080;
  --jp-mirror-editor-string-color: #ba2121;
  --jp-mirror-editor-string-2-color: #708;
  --jp-mirror-editor-meta-color: #aa22ff;
  --jp-mirror-editor-qualifier-color: #555;
  --jp-mirror-editor-builtin-color: #008000;
  --jp-mirror-editor-bracket-color: #997;
  --jp-mirror-editor-tag-color: #170;
  --jp-mirror-editor-attribute-color: #00c;
  --jp-mirror-editor-header-color: blue;
  --jp-mirror-editor-quote-color: #090;
  --jp-mirror-editor-link-color: #00c;
  --jp-mirror-editor-error-color: #f00;
  --jp-mirror-editor-hr-color: #999;

  /* Vega extension styles */

  --jp-vega-background: white;

  /* Sidebar-related styles */

  --jp-sidebar-min-width: 180px;

  /* Search-related styles */

  --jp-search-toggle-off-opacity: 0.5;
  --jp-search-toggle-hover-opacity: 0.8;
  --jp-search-toggle-on-opacity: 1;
  --jp-search-selected-match-background-color: rgb(245, 200, 0);
  --jp-search-selected-match-color: black;
  --jp-search-unselected-match-background-color: var(
    --jp-inverse-layout-color0
  );
  --jp-search-unselected-match-color: var(--jp-ui-inverse-font-color0);

  /* Icon colors that work well with light or dark backgrounds */
  --jp-icon-contrast-color0: var(--md-purple-600);
  --jp-icon-contrast-color1: var(--md-green-600);
  --jp-icon-contrast-color2: var(--md-pink-600);
  --jp-icon-contrast-color3: var(--md-blue-600);
}
</style>

<style type="text/css">
a.anchor-link {
   display: none;
}
.highlight  {
    margin: 0.4em;
}

/* Input area styling */
.jp-InputArea {
    overflow: hidden;
}

.jp-InputArea-editor {
    overflow: hidden;
}

@media print {
  body {
    margin: 0;
  }
}
</style>



<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/latest.js?config=TeX-MML-AM_CHTML-full,Safe"> </script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    init_mathjax = function() {
        if (window.MathJax) {
        // MathJax loaded
            MathJax.Hub.Config({
                TeX: {
                    equationNumbers: {
                    autoNumber: "AMS",
                    useLabelIds: true
                    }
                },
                tex2jax: {
                    inlineMath: [ ['$','$'], ["\\(","\\)"] ],
                    displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
                    processEscapes: true,
                    processEnvironments: true
                },
                displayAlign: 'center',
                CommonHTML: {
                    linebreaks: { 
                    automatic: true 
                    }
                },
                "HTML-CSS": {
                    linebreaks: { 
                    automatic: true 
                    }
                }
            });
        
            MathJax.Hub.Queue(["Typeset", MathJax.Hub]);
        }
    }
    init_mathjax();
    </script>
    <!-- End of mathjax configuration --></head>
<body class="jp-Notebook" data-jp-theme-light="true" data-jp-theme-name="JupyterLab Light">

<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h1 id="Scikit-Learn&#24211;--&#20915;&#31574;&#26641;&#21644;&#38543;&#26426;&#26862;&#26519;">Scikit-Learn&#24211;--&#20915;&#31574;&#26641;&#21644;&#38543;&#26426;&#26862;&#26519;<a class="anchor-link" href="#Scikit-Learn&#24211;--&#20915;&#31574;&#26641;&#21644;&#38543;&#26426;&#26862;&#26519;">&#182;</a></h1>
</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="&#20998;&#31867;&#22238;&#24402;&#30340;&#22522;&#26412;&#27010;&#24565;">&#20998;&#31867;&#22238;&#24402;&#30340;&#22522;&#26412;&#27010;&#24565;<a class="anchor-link" href="#&#20998;&#31867;&#22238;&#24402;&#30340;&#22522;&#26412;&#27010;&#24565;">&#182;</a></h2><ul>
<li>数据 $(\mathbf{x_1},y_1),(\mathbf{x_2},y_2),\ldots,(\mathbf{x_N},y_N)$</li>
<li>有监督学习: $\hat{y}_i=f(\mathbf{x_i})$</li>
<li>分类和回归</li>
<li>训练样本(training data)，检验样本（test data） </li>
</ul>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<ul>
<li>评估：错误率,有多少样本被错误分类，定义为： $$\frac{1}{N}\sum_{i=1}^N{I}(f(\mathbf{x}_i)\neq y_i)$$</li>
<li><p>评估：查准率，查全率</p>
<ul>
<li><p>True Positive （真正, TP）被模型预测为正的正样本；<br>
True Negative（真负 , TN）被模型预测为负的负样本；<br>
False Positive （假正, FP）被模型预测为正的负样本；<br>
False Negative（假负 , FN）被模型预测为负的正样本；</p>
</li>
<li><p>查准率（ precision, TPR),被预测为正的样本的确是正的概率：$P = \frac{TP}{（TP + FP）}$</p>
</li>
<li><p>查全率（recall） ,正的样本被识别出来的概率, $R =  \frac{TP}{TP + FN} $</p>
</li>
</ul>
</li>
</ul>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="&#21010;&#20998;&#20934;&#21017;">&#21010;&#20998;&#20934;&#21017;<a class="anchor-link" href="#&#21010;&#20998;&#20934;&#21017;">&#182;</a></h2><ul>
<li>选择什么变量？
如果变量包含了n个变量，在根节点，或者在任何一个结点，选择哪个变量其实是很复杂的。如果只是随机的选择，结果可能会比较差。</li>
<li>例如利用变量分割</li>
<li>遵循什么法则</li>
</ul>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<ul>
<li>Information gain,信息增益，基于信息熵的准则。  <ul>
<li>熵(Entropy)用来度量一个随机变量的随机性或者说不确定性。<br>
熵的定义为：
$$H(X)=-\sum_{x\in \mathbb{X}}p(x)\log_2 p(x)$$ </li>
<li>对于一个两分类问题（正负），如果所有样本都是正或者都是负，熵为0，确定性最高，熵最低；  </li>
<li>如果有一半是正的，一半是负的，则熵为1，随机性最高，熵最高。  </li>
</ul>
</li>
</ul>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<ul>
<li><p>Gini index，基尼指数准则</p>
<ul>
<li>记分类变量 Y的水平数为$|Y|$，$p_k=P(Y=k)$
$$\mbox{Gini index}=\sum_{k=1}^{|Y|}\sum_{k'\neq k}p_kp_{k'}=1-\sum_{j}p_j^2$$</li>
<li>直观反映从数据中随机抽取两个样本，其类别标记$Y$的取值不一致的概率。上述值越小，数据类别的纯度越高。</li>
</ul>
</li>
</ul>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="&#20915;&#31574;&#26641;&#30340;&#31639;&#27861;">&#20915;&#31574;&#26641;&#30340;&#31639;&#27861;<a class="anchor-link" href="#&#20915;&#31574;&#26641;&#30340;&#31639;&#27861;">&#182;</a></h3><ul>
<li>连续特征</li>
<li>离散特征</li>
<li>树的生长算法</li>
<li>剪枝</li>
</ul>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="&#20915;&#31574;&#26641;&#23454;&#20363;">&#20915;&#31574;&#26641;&#23454;&#20363;<a class="anchor-link" href="#&#20915;&#31574;&#26641;&#23454;&#20363;">&#182;</a></h3>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[1]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="c1"># import matplotlib as mpl</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="o">%</span><span class="k">matplotlib</span> inline
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">from</span> <span class="nn">sklearn.datasets</span> <span class="kn">import</span> <span class="n">load_iris</span>
<span class="kn">from</span> <span class="nn">sklearn</span> <span class="kn">import</span> <span class="n">tree</span>
<span class="kn">import</span> <span class="nn">pydotplus</span>

<span class="n">iris</span> <span class="o">=</span> <span class="n">load_iris</span><span class="p">()</span>
<span class="n">clf</span> <span class="o">=</span> <span class="n">tree</span><span class="o">.</span><span class="n">DecisionTreeClassifier</span><span class="p">()</span>
<span class="n">clf</span> <span class="o">=</span> <span class="n">clf</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">iris</span><span class="o">.</span><span class="n">data</span><span class="p">,</span> <span class="n">iris</span><span class="o">.</span><span class="n">target</span><span class="p">)</span>
<span class="n">dot_data</span> <span class="o">=</span> <span class="n">tree</span><span class="o">.</span><span class="n">export_graphviz</span><span class="p">(</span><span class="n">clf</span><span class="p">,</span> <span class="n">out_file</span><span class="o">=</span><span class="s2">&quot;temptree.dot&quot;</span><span class="p">,</span>
                                <span class="n">feature_names</span><span class="o">=</span><span class="n">iris</span><span class="o">.</span><span class="n">feature_names</span><span class="p">,</span>
                                <span class="n">class_names</span><span class="o">=</span><span class="n">iris</span><span class="o">.</span><span class="n">target_names</span><span class="p">,</span>
                                <span class="n">filled</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">rounded</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span>
                                <span class="n">special_characters</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>


<span class="n">dot_file</span><span class="o">=</span><span class="sa">r</span><span class="s1">&#39;.\temptree.dot&#39;</span>
<span class="n">graph</span> <span class="o">=</span> <span class="n">pydotplus</span><span class="o">.</span><span class="n">graph_from_dot_file</span><span class="p">(</span><span class="n">dot_file</span><span class="p">)</span>  
</pre></div>

     </div>
</div>
</div>
</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[2]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="o">%</span><span class="k">matplotlib</span> inline
<span class="kn">from</span> <span class="nn">IPython.display</span> <span class="kn">import</span> <span class="n">Image</span>
<span class="c1">#写到pdf文件</span>
<span class="c1">#graph.write_pdf(&quot;iris1.pdf&quot;)</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[3]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">Image</span><span class="p">(</span><span class="n">graph</span><span class="o">.</span><span class="n">create_png</span><span class="p">())</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[3]:</div>




<div class="jp-RenderedImage jp-OutputArea-output jp-OutputArea-executeResult">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAABKsAAAN/CAYAAAARdls/AAAABmJLR0QA/wD/AP+gvaeTAAAgAElEQVR4nOzde3iU9Z3//9dwFE8DUkHUBstaEC1NKi0HqWUJ1Rb83mPtik2g1PZXyU4q1ANp7WGy1iZu6W4irlyW7AxWvdJkolCVzEpqS4aNLCayHmakKkltMamsSzzNqLsCIvfvj+w9ZpKZZCane5I8H9c118Xc8zm8P/eEy/jm83nfDtM0TQEAAAAAAAD2Wz/G7ggAAAAAAAAAC8kqAAAAAAAAZAySVQAAAAAAAMgY4+wOAAAAjB7Hjx/XSy+9pNdff13vv/++3eEAvTr99NM1Y8YMXXzxxZowYYLd4QAAMCqQrAIAAIMqEonoN7/5jR577DHt3btXx48ftzskIG0TJkzQ5Zdfrq997Wv65je/qcmTJ9sdEgAAI5aDpwECAIDB8MEHH+gf//Efddddd2ncuHG69tprdeWVV+pzn/ucZsyYoTPOOMPuEIFevffee3r99df1/PPP64knntBvf/tbnThxQrfeeqt+8pOfaNKkSXaHCADASLOeZBUAABhwjzzyiG655RZFIhEVFxfL7Xbr9NNPtzssoN/ef/99VVRUqKSkRJMnT9bmzZv19a9/3e6wAAAYSdZTYB0AAAwY0zT1D//wD1q1apWWL1+ugwcPqqioiEQVRozTTz9dRUVFOnjwoJYvX65Vq1bpH/7hH8S//wIAMHDYWQUAAAbE8ePHtWbNGgUCAW3btk3f/OY37Q4JGHS/+c1vdMMNN8gwDFVVVVGEHQCA/mNnFQAAGBjf/e531dDQoN27d5OowqjxzW9+U7t371ZDQ4O++93v2h0OAAAjAskqAADQb5s2bdIjjzyiQCCgL37xi3aHAwypL37xiwoEAnrkkUe0adMmu8MBAGDYI1kFAAD6Ze/evfrpT3+qyspKLVy40JYY2tra+tTP4XDI4XAMcDTpjZuobdf1DFSc4XBYPp+v3+OkyufzKRwOD9l80WhUPp9PLpdLDodDLpdLNTU1ikajKfevqanpU/+FCxeqsrJSP/3pT7V3797+LgUAgFGNmlUAAKDPPvroI33+85/XlVdeqV/+8pe2xFBeXq6ioqI+Fbi2EkAD/etQOuN2bZtoPQMRZ1tbm9avX6/Kyko5nc4+j5OOaDSqyZMnq7W1VVlZWYM+X2FhoSoqKrpdNwxDtbW1PfZtb2/XDTfcoEAgkLD/tm3bNG3atF5juO222/T73/9ezzzzjMaOHZt68AAAwELNKgAA0Hc+n09vvPGGiouLbYuhqKjItrmTMU2zz4mlwVrPL37xC918881DlqiSJKfTqfr6ev3iF7/o1zjhcFjl5eW9tqmoqJDH41Fra6tM01Rra6vcbrcCgYBaWlp67L9z504FAgH5/f7Y92eapvx+vwKBgHbu3JlSrMXFxXrjjTeGdAcbAAAjDTurAABAn/zv//6vLrjgAv3yl7/Ud77zHdvi6M+uo8HaWdWfGBLF1N84g8Ggli9frkgkMqTJKunj3VX19fXKzc1Nq29TU5MefPDB2G6pntbv8/lUUFCg5uZmzZ49O3Y9HA4rJydHfr9feXl5Sfv3dI/Tvf/333+/brvtNr366qs69dRTU+oDAABi2FkFAAD6xtqBsmbNmpTad667VFNTE3vfU02gYDCowsLCWP2gYDDYbcxE40sf78axrlv1h1LV1NQkh8PRbddYS0uLHA5Ht1pMVpzhcDhpjanO9ZASxdLTejqPke567r77bnm93m6Jqq41mgoLC7vtQOocRyAQiM3d+bhc1++zM6fTKa/Xq7vvvjulWKPRqAKBgFwulxYvXixJqq2t1ZEjR3rsZ9X5mj59etz1GTNmSJJefPHFHvsbhtGvzztbvXq1TNNM6+cNAAB0YgIAAPTBlVdead5www0pt5dkSjJra2tjf7ZehmF0a+/xeLq1k2R6PJ5uY3Z+maaZcA7r5ff7u/VPJBKJJPzc7/ebkkyv15twfcnGdbvd3WIpKytL2K/rehK1T7SeRBobG01JZmNjY7fPDMNIOGcoFOq2rkT3NBQKJfyeusbUUwyW1tbW2L01DMP0+/1ma2trj2vrrKfvsqfPLNb6usZuxVRbW5tyLKZpmjfccIN55ZVXptUHAACYpmmaN7KzCgAApO348eNqaGjQFVdckXZfn88XV1PI4/EoEAjE7ZoKBoMqLS2Vx+NRJBKRaZqKRCLyeDwqLS2N7WoyOx3LMjvViXK5XJKkxsbG2PXW1lZJUn5+fkpxOp1OeTweSYrbbVRdXS1JKigoiF2zPvd6vQnHCgaDCespRSKRuHbJ1mOJRCKx+2EVDLfiSebAgQOSpHPPPTfueiAQUCAQiLvHfr9fkhIWKd+/f3+sXX19vSQpJycnFlfn613vsTW3FUsiM2fOVH5+vvx+v2pra5WXlzckRdkthmGovr5e1dXVsV1iDodD1dXVqq+vT2tnlSRdccUVamho0IcffjhIEQMAMHKRrAIAAGl7+eWXdezYMWVnZ6fdt6ysLJaEyMrK0rp16yRJ27dvj7XZs2ePpI5i49bRNafTGSs+vnv37h7nsBI9s2bNUjgcViAQ6FPB66uuukqS1NzcLKkjKWUV4ZYUS5q99tprkqQFCxYkHMdaz7p16+LWvnbt2rTi2bBhQ+x+WMmTRE+v68z6vGviZ9euXd3GzMvLk2ma2rp1a49zd6491fk7SlaTypq7p1hbW1vl9/uVn58fO+JoHe0bKs8//3y3GAOBgP785z+nPdZnP/tZHTt2TC+//PJAhQcAwKhBgXUAAJC2uro6rVy5Uu+++67OOOOMlPqkU8A6Ua2mrrq27TpucXGxSktL+9TXYhUH93g8KikpUU1NjfLz82WaphwOh7xer9atW6fy8nIVFRUlHbcva+/cNln/VAp/96dvX/r3d75oNKonn3xSPp9PgUBAbrdbK1eu1MKFCzVt2rS040x1buu77VqIPdn13rz33ns688wzVVdXp69+9asp9wMAABRYBwAAfWAVRE81UTXUfD6fSktL5Xa7VV9fr1Ao1GuB7kSso4BW0qu6ujp21M/r9caOAhYVFamsrGzgFjCKOZ1OGYah2tpaNTY2Suo41tm1cHpX1pHNrsX6rffW58lYRxe7JqSs970dt+zK+rvR9agnAADoHckqAACQtpMnT/a5b9ejXVa9p87JBLfbLenjWkiJXj2xkkhbt25Vbm6usrOzNXHixD7Fax0FtGo8WUf95s2bJ0mxJ74tWbIk6RiJal9J3e/FYLDuZbLr7e3tgx5Db7Eks2jRIm3dulWhUKjXZOAll1wiSd2Skq+++qqk7scg09Xbcctk+vN3BQCA0YpkFQAAGFI+ny+WpGlra1NlZaUkadmyZbE2q1atktRR36pzMiUYDMrhcKi8vLzbuF131EgfJ4ei0Wifdz7NnTtX0sdF2y+44IK469aOHOt9ItbaioqK4tbeUx2tROvpi0svvTQ2X2dLly6VJG3ZsiU2V01NjRwOhwoLCwdkbos1txVLurKzs7Vx48Ye21j3v7KyMu4e79ixQ1LyemIW6+cjGAzG3XsrGcnOOQAAhtDAP2EQAACMdFVVVWa6v0ZIMiWZHo8n9ufO17pK1E6SaRiGeeTIkVg7wzBin7ndbtM0TdPv9yfsa72am5vjYuqNFUvXON1ud8LricZNtB6v19utbaL1JIszlfhDoZApyWxsbOz2Wee5Or9CoVCvc6RzvbGxsdu4yfr19OpNsvVY97GnOI8cOZK0f9efuVRJMquqqtLuBwDAKHcjO6sAAMCQKikpie1SMQxD9fX1KikpSdjO7/fHHR3zer3atm1bXKHtkpKSWJvDhw9L6qgzZNWWkjqO4TU3NysUCkmSGhoa0orZOgrYefeXJK1cuTLu855Y67Ge4uf3+2NPQuzarut6+iM7O1uGYejxxx/v9lllZWXC+9SXpzz25PHHH5dhGAM+blfbtm2T1+uN3WPDMOT1erVp06Ze+06bNk2VlZVx35FhGPL7/aqsrOyxuDsAABhYPA0QAACkrbq6WmvWrOm1dlRnqT4NDgMvGAxq+fLlikQicjqdQzq39UTF+vp65ebmDuncdnM4HKqqqtLq1avtDgUAgOGEpwECAACMdLm5uXK73aqrqxvyuevq6uR2u0ddogoAAPTdOLsDAAAAwOD78Y9/rJkzZ2rFihVDtrsqGo0qPz9fra2tQzIfAAAYGdhZBQAAMApkZWUpFArp4YcfHrI5H374YYVCIWVlZQ3ZnAAAYPhjZxUAABgS1KqyX3Z29qAXOe8sUQF5AACA3rCzCgAAAAAAABmDZBUAAECaHA5H7OmGQ9EvXdFoVD6fTy6XSw6HQy6XSzU1NYpGoymP0dLSouLi4ljMPp9P7e3tfW5rfdbTCwAAQOIYIAAAwIjzox/9SBUVFbH3gUBAgUBAhmGotra21/7hcFg5OTlx1woKChQIBFRZWRlXoD2dtj0xDCOldgAAYORjZxUAAECaTNPsUw2uvvZLRzgcVkVFhTwej1pbW2WaplpbW+V2uxUIBNTS0tJj/2g0qpycHBmGEesfiURUVlamQCCgurq6PrW11t71FQqFJEllZWWDc0MAAMCwQ7IKAABgBNm/f78kae3atbGn8GVlZcntdkuSnnvuuR77v/zyy5Kk1atXx/o7nU7dcMMNkqTq6uo+tU2kvb1dOTk58nq9mj17duqLBAAAIxrJKgAAgE5qampitZ6Ki4vV0tLSraZSsvft7e0qLy+PqxPVWSq1mfpb26mtrU2SNH369LjrM2bMkCS9+OKLPfbft2+fJOmyyy6Lu+50OmWaZtwxwnTaJrJlyxYZhsFTAwEAQBySVQAAAP+nuLhY+fn5CgQCkqTS0lLNmTMn5f433HCDioqKJHXUicrPz++WsBpspaWlktStVtS0adPiPk+moaFBUsdurM6Ju/Ly8m5F09Np21UwGFRpaaluvvnm1BcHAABGBZJVAAAA+jh5kqjWU6qys7MViURkmqbq6+sl9X4UrqtktZ06vwaTlajrmrgrKirSDTfcEPdEwXTadnX33XfLMAzl5uYO1lIAAMAwRbIKAABA0p49eyRJ69ati6v1dMstt6Q8xoYNG2I7mqwkjJXAGY6OHDkSS5D5/f5uRdP72rapqUmBQIDjfwAAICGSVQAAAPr4eJyVqLKkU/jbOmrXH/2tWTVQioqK4tazYsUKSYl3iqXTVpIefPBBSdKXvvSlAYsXAACMHCSrAAAARhCPxyNJ3Y7gWe+tz3vr37XmlfW+806xdNpa2tvbVVFRIY/H060fAACARLIKAABA0seJF+tpepau7wdbf2tWXXLJJZI6juV19uqrr0rqvnMsWf+u67aSXZ1reKXT1vKXv/xFkrRgwYIe4wAAAKMXySoAAABJy5YtkyT5fL5Y8qWtrU0+n8/OsNI2d+5cSVJlZWXcOnbs2CGp9yTRZZddJqnjPnTenWXVn1q5cmWf2loOHDggSWk9ZREAAIwuDnOwHykDAABGnOrqaq1Zs2bQn0w31IqLi2O1qxKx1mvVjUr23pJqu4HmcrkSHsFzu93aunVrjzFKUk1NjfLz81Pqn05bSSosLFRFRYWOHDkyIDW+MpnD4VBVVZVWr15tdygAAAwn69lZBQAA8H9KSkrk9/tlGIakjqOBzc3NNkeVvm3btsnr9cbWYRiGvF6vNm3alFL/vLw8NTY2xo7xGYYhv9+fMPmUTltJqqiokDQwxegBAMDIxM4qAACQtpG6syoZh8ORdKcQkAw7qwAA6BN2VgEAAEgdiQWHw6GmpqbYtWg0qvLycknS0qVL7QoNAABgVBlndwAAAACZoLa2Vi6XS4sXL+72mWEYWrFihQ1RAQAAjD7srAIAAFBHQqq+vl4ejyd2ze12y+/3q7KyUk6n08boAAAARg92VgEAAPyf3Nxc5ebmqqSkxO5QAAAARi12VgEAAAAAACBjkKwCAADIIFah9+EuEAj0uA5rnYleXUWjUfl8PrlcLjkcDrlcLtXU1CgajQ7mEgAAgE04BggAAIABFQ6H5XK5kn7e1taW1ng/+tGPVFFREXsfCAQUCARkGIZqa2v7HCcAAMhM7KwCAADAgGlqalJOTk5KbcvKymSaZrdXZ+FwWBUVFfJ4PGptbZVpmmptbZXb7VYgEFBLS8tgLAMAANiIZBUAAAAGRHl5uRYvXiy/399ju1deeUWS9LnPfa7XMffv3y9JWrt2rbKysiRJWVlZcrvdkqTnnnuuPyEDAIAMRLIKAACMSMFgUIWFhbE6SMXFxQqHw93ahcNhlZeXx9pZ9ZA661xLyarF5HK5FAgEYm1qampi7Xrq37VdqnWXOq/H5XIpGAz2a91d9VRDKtU6WkVFRaqtrVVeXl5Ka0qFdWRw+vTpcddnzJghSXrxxRcHbC4AAJAhTAAAgDRVVVWZmfxrRG1trSkp4au+vj6ldn6/P9bOupaofSgUMj0eT5/7G4YRF7t1vbNE40syPR5Pn9adSLJ+nV/p6KlPWVlZ7N55vd5YW6/Xa0YikZTH6UtcQ0mSWVVVZXcYAAAMNzeyswoAAIw4VnFvq8aRaZpqbGyUJG3fvr1bu8bGxli71tZWSVJ+fn63cffv369IJCLTNFVfXy9JsfpMXa8n6u/z+eLqLnk8HgUCgaS7pKSOnVKlpaXyeDyxOSKRiDwej0pLS+N2TaW67kTMBLWjur4GWk5OjgoKCmLvCwoKtHbtWp7yBwDAKEeyCgAAjDiGYUjqSNAEg0FFo1EtWrRIpmlq69atsXZWEmbWrFkKh8MKBALy+XxJx92wYYOcTqckKTc3N3a9qKgo4fWuysrK4uourVu3LhZnMnv27Ok2h9PpVFFRkSRp9+7daa/bblbsnZOEpmnK7/crEAiorq7O5ggBAICdHOZg/DMZAAAY0aqrq7VmzZpB2W0zEMLhcNwT6QzD0M0335wwkVRcXKzS0tKE41jrs+o1dV1vqteTtUulbSq1oqy26aw7WRypzJOKntbcWz/DMFRbW9vrOH2dY6g4HA5VVVVp9erVdocCAMBwsp6dVQAAYMTJzs6WaZoKhUIqKytTIBDQ8uXL5XK54o7N+Xw+lZaWyu12q76+XqFQSEeOHLEx8v5Jdd2ZrnPheo/HI0ndjgZa763PAQDAyEGyCgAAjFjZ2dnauHGjWltbVV9fr0AgELfzyKqXtHXrVuXm5io7O1sTJ04ctHisJ9tZWlpaJPWccHG73ZI+romVSi2p3tadyFDWrHK5XHI4HEkTUNaaJemSSy6RpG5JxFdffVWSYscqAQDAyEGyCgAAjDiFhYVyOBxqamqS1JHQuPDCC5O2t5JG0WhUZWVlgxaXz+eLJaza2tpUWVkpSVq2bFnSPqtWrZLUUe+qvb09dj0YDMrhcKi8vDx2Ld1128U6Fte1NpX13lqzJM2dO1eSVFlZGXfvduzYIUlasGDBoMcLAACG1ji7AwAAABho119/vSoqKrR48eJun3m93tif/X6/8vPzNWfOnITjtLS0aPbs2QMa28yZM+PeezyeHmtK5ebmxp7817W2lmEYWrt2bex9quu224oVK2QYhvLz87s9NbHr/cjOzpZhGAnX73a7lZ2dPSQxAwCAocPOKgAAMOIsWrRIoVAo7nidx+NRbW1t7Al8kpSXlxeXxPF4PGpublYoFJIkNTQ0DGhcJSUlsZ1bhmGovr5eJSUlKfXz+/1xx+O8Xq+2bdumadOmxa6lum67OZ1OVVZWyu/3x55gaNUNS3Q/tm3bJq/XG2trGIa8Xq82bdo0pHEDAIChwdMAAQBA2jL9aYCZJtOfWofBwdMAAQDoE54GCAAAAAAAgMxBsgoAAAAAAAAZg2QVAAAAAAAAMgZPAwQAABhk1KoCAABIHTurAAAAAAAAkDFIVgEAgBHJ4XDEnsI3nFhxd42/6/VEbSzRaFQ+n08ul0sOh0Mul0s1NTWKRqMDFtdwn7+3MQAAgH0cJvvSAQBAmqqrq7VmzZqMPt5mJSAyOcZEuiZOTNNUW1ubZs6cmbRP1zUWFhaqoqKiWzvDMFRbW5t2TCNx/kT3eaA5HA5VVVVp9erVAz42AAAj2Hp2VgEAAGQg0zS7JVDKyspi1zu/OguHw6qoqJDH41Fra6tM01Rra6vcbrcCgYBaWlr6HNNImj9RXwAAkBlIVgEAAGS4V155RZL0uc99rte2+/fvlyStXbtWWVlZkqSsrCy53W5J0nPPPcf8AAAgo5GsAgAAGcHhcKiwsDDhZ4WFhXI4HLGaQ+FwWOXl5bF6Q1ZNot7GT1SbKNn1YDAYm9flcikYDKa8jt5eg6mtrU2SNH369LjrM2bMkCS9+OKLzA8AADIaySoAAJARysrKVFFRofb29rjr7e3tqqioUFlZmZxOpwKBgHJyclRUVBRrEwgElJ+f32vCKlXFxcVavnx5rO5RIBDQ8uXLVVxcPCDjp+v555+XJE2dOlU+ny+W9PL5fN2KlpeWlkqSnE5n3PVp06bFfc78AAAgU5GsAgAAGeHLX/6yJHXbwWS9NwxDkuRyuSRJjY2NsbpDra2tkqT8/Px+xxEMBlVaWiqPx6NIJCLTNBWJROTxeFRaWqpwONxj/0Q1lXqqsZSOnJwcFRQUxN4XFBRo7dq1/XrKHvMDAIBMQ7IKAABkhOzsbBmGoerq6rjr1dXVcrvdmj17tqSPk0GzZs1SOBxWIBCQz+cbsDj27NkjSSoqKortznE6nbGdXLt37x6wuVJlzd05QWeapvx+vwKBgOrq6pgfAACMGA6Tx6AAAIA0VVdXa82aNQP+NLVgMKjly5erublZs2fPVktLi+bMmaP6+nrl5ubG2hUXFyc9zmXFZNWGSvbekqxdT3pa90D1T/XeOhwOGYah2traXvunO/ZomH8wYuo8dlVVlVavXj3gYwMAMIKtZ2cVAADIGPPnz5ckNTQ0SPr4yW3WdUny+XwqLS2V2+1WfX29QqGQjhw5MvTBZpBAIBD7s8fjkaRuR+Os99bnzA8AADIVySoAAJAxnE6nvF6vCgoK1N7ervz8fHm93rhi2VbNoq1btyo3N1fZ2dmaOHFin+brWsxdktxutyTF6lWlW3NqMGpWuVyuuKchWqz3VsySdMkll0hStwTeq6++KknKyspifgAAkNFIVgEAgIyydOlSSdL06dMlSV/5ylcStmtpaZHUkbAoKyvrdVyrQHtTU1Os35YtW7q1W7VqlaSOpxN2TmYFg0E5HA6Vl5enupQBYx0j61qbyXpvxSxJc+fOlSRVVlaqra1NktTW1qYdO3ZIkhYsWMD8AAAgs5kAAABpqqqqMgfz1wi3221KMt1ud7fP/H6/KSnpq7m52TRNM/a+p35lZWXd2pmmaXo8noRjG4ZhHjlyZNDWnShu0zTNSCRiGoaRMCaPx9NtjGRtu97PRHMlMlLnTyeGvpBkVlVVDcrYAACMYDeyswoAAGQca6fM9ddf3+2zvLw8eb3e2HuPx6Pm5maFQiFJH9e7StTP7/fHdlh5vV5t3LgxYduSkhL5/f6442Ver1fbtm3TtGnT+raofnA6naqsrIyL36rZVVJS0q39tm3b5PV6Y20Nw5DX69WmTZuYHwAAZDyeBggAANI2WE8DxOA+nS7ZfHZ+j5kwv8TTAAEAyCA8DRAAAGC0ampqitulNtrmBwAAmYlkFQAAQAZyOByxXT+DZd++fVq3bt2gzpGp8w/F/QUAAH1DsgoAAGCUSlaza7TMDwAAMtM4uwMAAADAx6gDNjS4zwAAZC52VgEAAAAAACBjkKwCAACjHvWL0tfW1mZ3CAAAYIQiWQUAAIC0lJeXa+bMmXaHAQAARiiSVQAAAEhLUVGR3SEAAIARjGQVAAAAAAAAMgbJKgAAMKJFo1HV1NTI5XLJ4XCosLBQLS0tvfYLh8MqLy+P1bNyuVyqqanp1i4YDKqwsDDWrri4WOFwuM/turLa9/TqTTpzd27rcrkUDAa7xdM1ts463+tk9yydmFL9HgAAwAhiAgAApKmqqsocLr9GGIZhSur2CoVCsTbWNUttbW3CPpJMv9+fUrv6+vq02yWSrF/nV0/Smdvj8SRs5/F4eownnf4Ddd86fw+ZSpJZVVVldxgAAAw3N7KzCgAAjFiBQECBQEAej0eRSESmacrv90uSKioqkvZzuVySpMbGRpmmKdM01draKknKz8/v1q61tTXWrrGxUZK0ffv2tNslYrXv6dWTVOcOBoMqLS2Nu1eRSEQej0elpaWxXU+d5+s8f+f+1lytra2x/p13aKV733r7HgAAwMhCsgoAAIxYu3btkiRt2LBBTqdTkpSXlyfTNLV169ak/azEyKxZsxQOhxUIBOTz+bq1MwxDUkeCJRgMKhqNatGiRd3GT7XdYEh17j179kjqKJ5u3Sun0xkrpr579+4e57GSTOvWrVNWVpYkKSsrS+vWrYv7PJ2YUv0eAADAyOIwe/vnOAAAgC5qa2t19dVX64MPPtApp5xidzhJWfWUevt1J1G74uJilZaWJmxvtQuHw8rJyYldNwxDN998s3Jzc+Pap9qup9h60tP6Up07nXkS3a+e7nXXz9K5H6l8D5no6NGjmjRpknbu3BnbIQYAAFKynp1VAAAgbVOnTpUkvf322zZHMjh8Pp9KS0vldrtVX1+vUCikI0eOdGuXnZ0t0zQVCoVUVlamQCCg5cuXy+VyxRULT7XdYLBz7v7GlOr3kIneeustSdLZZ59tcyQAAAw/7KwCAABpe+edd3TWWWfp97//va644gq7w0mqsLBQFRUVOnLkiKZNm5a0XdedP4l2CUWjUU2ePLnb9c7a2tr0yiuvaPny5QPSbjAkm9u6V5FIJHYMMJlE98fq39raGjsGKEktLS2aM2eO3G530iOPyWLq6/eQCf7whz/oyiuvTOl+AgCAOOysAgAA6ZsyZYrmzZunvXv32h1Kj5YuXSpJ2rJli6LRqCSppqZGDodDhYWFvfZvaWmR1JEgKSsr6/Jhg/kAACAASURBVPZ5YWGhHA6HmpqaJHXUaLrwwgv73G4wpDr3qlWrJEllZWVqb2+PXQ8Gg3I4HCovL+/Wx7qnnfv7fD61tbVJ6khCVVZWSpJWrlyZdkyW3r6HTLR3717NmzePRBUAAH0xAI8UBAAAo5DH4zHnzZtndxi9MgzDlNTtFQqFYm2saxa/35+wj/Vqbm42TdM0Gxsbk7bxer2x8VJtNxjSmdvj8SRsZxiGeeTIkVi7zvfU7Xb32t/j8fQpplS/h0w0b948s7i42O4wAAAYjm4kWQUAAPrk1VdfNceOHWs+9dRTdofSo0gkYnq93rjESdckR9dklWmaCfuEQqFuCZVQKBSXpPF4PGZtbW23OFJtNxjSmdvv95tutzsuedQ5UWWNZ7UxDKNbfyuZZRiG6ff7+xVTqt9DJnnqqafMsWPHmq+++qrdoQAAMBzdSM0qAADQZ263Wy0tLQoGg3aHAmSM3NxczZ49WxUVFXaHAgDAcETNKgAA0HclJSV6/vnntWPHDrtDATLCjh079Pzzz6ukpMTuUAAAGLZIVgEAgD47++yzdccdd+h73/ueDh06ZHc4gK0OHTqk733ve7rjjjt09tln2x0OAADDFscAAQBAv5w4cUJf+cpX9MYbb2jv3r08/QyjUjQa1eWXX66zzz5bTzzxhMaNG2d3SAAADFccAwQAAP0zbtw4PfLIIzp27JiuueYavffee3aHBAyp9957T9dcc42OHTumRx55hEQVAAD9RLIKAAD0m9Pp1OOPP67m5mYtWbJEbW1tdocEDIm2tjYtWbJEzc3Nevzxx9lZCADAACBZBQAABsSFF16o/fv3a8KECVq4cKHq6ursDgkYVHV1dVq4cKEmTJig/fv368ILL7Q7JAAARgSSVQAAYMCcd955amho0LJly7Ry5UpdddVVeuWVV+wOCxhQr7zyiq666iqtXLlSy5YtU0NDg8477zy7wwIAYMQgWQUAAAbUaaedpurqau3Zs0dtbW26+OKL9Y1vfEO7du3S0aNH7Q4P6JOjR49q165d+sY3vqGLL75YbW1t2rNnj6qrq3XaaafZHR4AACMKTwMEAACD5sSJE3rooYfk8/n0H//xHxozZozmzp2rGTNm6Mwzz7Q7vD47ceKExowZozFj+He/npw8eVInT54c1gXH3333Xb3++ut6+eWXdfLkSX3xi19UQUGBrrvuumG9LgAAMth6klUAAGBIvPnmm9qzZ4/C4bBef/31Yf3UwGeffVbvv/++li5dancoGa2hoUGnn3665s+fb3cofXbGGWdoxowZys7O1rJly/SJT3zC7pAAABjpSFYBAACk44knntCKFSv08MMP69prr7U7nIy2Y8cOXXfddaqrq9NXvvIVu8MBAADDA8kqAACAVEUiEc2bN09LlixRTU2N3eEMC3l5edq3b58OHDigyZMn2x0OAADIfOsptAAAAJCiW265RSdOnNC9995rdyjDxr333qsTJ07olltusTsUAAAwTJCsAgAASEEgENADDzygiooKTZ061e5who2pU6eqoqJCDzzwgAKBgN3hAACAYYBjgAAAAL14++23dckll+grX/mKHnjgAbvDGZa+/e1v64knntCLL76os846y+5wAABA5uIYIAAAQG/Wr1+vcePGafPmzXaHMmxt3rxZ48aN0/r169Pq53A4en2lq6/9AADA0CBZBQAA0IMdO3aopqZGPp9PU6ZMsTucYWvKlCny+XyqqanRjh077A4HAABkMI4BAgAAJNHe3q7PfOYzuvrqq+Xz+ewOZ0RYt26ddu7cqT/+8Y+aNm1ar+2tHVAD+SvrYIwJAAAGzHqSVQAAAEn83d/9nZ599lkdOHBAZ5xxht3hjAjvvfee5s2bp/nz5+u3v/1tr+1JVgEAMOpQswoAACCR6upqPfroo7rvvvtIVA2gM844Q/fdd58effRRVVdXD/j44XBY5eXlsbpULpdLNTU1vfYLBoMqLCyM9SsuLlY4HO61rcvlUjAYHOhlAAAwqrGzCgAAoIvXX39dn/nMZ7R69Wpt2bLF7nBGpA0bNqi6ulp//OMfNWPGjKTt0tkFFQgE5HK5En7m9/uVl5eXcMye+tXX1ys3Nzf2vri4WKWlpd3aeTwelZSU9BojAADoFTurAAAAuiooKNCUKVO0adMmu0MZsTZt2qQpU6aooKAgpfap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G8aEFRFR+8RkFRERERFZpKqqCrNmzcLx48cRHx8PuVwudUjUDjBhRUTU/jBZRURERET1qq6uxqxZs5Camor4+HiMHTtW6pCoHWHCioiofWGyioiIiIjqdOfOHcyaNQtHjx5FfHw8xo0bJ3VI1A4xYUVE1H4wWUVEREREZgmJqiNHjiA+Ph7jx4+XOiRqx5iwIiJqH5isIiIiIiKT7ty5gxdeeAGHDx9GfHw8JkyYIHVIRExYERG1A0xWEREREZGRO3fuYM6cOTh48CB++OEHTJw4UeqQiERMWBERtW1MVhERERGRnjt37iAwMBBJSUnYt28fJk+eLHVIREaYsCIiaruYrCIiIiIiUU1NDebNm4f4+Hjs27cPU6dOlTokIrOYsCIiapuYrCIiIiIiAMDdu3cxb948/Pjjj9i3bx8efvhhqUMiqhcTVkREbQ+TVURERETtSFxcHF566SWUlpbqnb937x7mzZuH/fv3Y9++fXjkkUckipDIepYkrGJiYqBUKiWIjoiIrCXTarVaqYMgIiIioubxyCOP4PDhwxg1ahR++ukn9OrVS0xU7dmzB/v378djjz0mdZhEDXLr1i0EBAQgPT0dCQkJGDNmDABg69atWLhwIQDg119/xfjx46UMk4iI6raEySoiIiKiduLXX38V3+rXuXNneHt7IzExEcuWLcPu3buxb98++Pj4SBwlUeMYJqxOnjyJV155Bffv30fnzp0xY8YM7N69W+owiYjIPCariIiIiNqL5557Dvv27UNNTQ2A2oRVr169UF5eDpVKBT8/P4kjJLINIWF1/PhxlJeX4/79++JnMpkMJ0+exMiRIyWMkIiI6rCEPauIiIiI2oEzZ84gLi5OTFQBtW/+u3HjBvr27YvRo0dLGB2RbT344IOYO3cuNBqNXqIKADp16oSPPvpIosiIiMgSTFYRERERtQNr165Fp06djM7X1NSgoKAAjz32GK5duyZBZES2t3XrVrz++uswtYmkpqYGO3bswLlz5ySIjIiILMFkFREREVEbl5eXh23btulVVemqqanB+fPnMWnSJBQWFjZzdES29e9//1vsUWVOx44dsWbNmmaMioiIrMFkFREREVEbt379enToUPf/9t29excXL17Ep59+2kxREdne3bt38eqrr9aZqAJqE7Rbt27FpUuXmikyIiKyBpNVRERERG1YUVER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xWQVERF1Wg8ePMD27dvh4OCAd955BwEBAUhPT8fHH38MU1NTqcMjIiIiEtna2iI6OhrvvfceVq9ejWeffRb5+flSh0XUITFZRUREnU5NTQ3+9a9/YfTo0Vi+fDmee+453LhxA59//jkGDx4sdXhEREREGvXs2RPvv/8+Tp8+jWvXrsHFxQW//PKL1GERdThMVhERUafx6NEj7NmzB46Ojnj99dfh7e2N1NRUfPXVV7C2tpY6PCIiIiKteHp64uLFi5g2bRpmzZqFFStWoLKyUuqwiDoMJquIiKjDq62txf79++Hs7IwXX3wREydOhFwux3fffQdbW1upwyMiIiJqNiMjI+zduxdhYWH417/+hccffxxXrlyROiyiDoHJKiIi6tAiIiLg5uaGv/71r3jsscdw+fJlhIWFwd7eXurQiIiIiFpt8eLFSExMRJ8+fTB+/HiEhoZKHRKR5JisIiKiDun48ePw8PDA3LlzMXz4cFy8eBH//ve/IZPJpA6NiIiISKfs7e0RExODVatW4c0338TcuXOhUCikDotIMkxWERFRhxIdHY0nn3wSM2bMgLm5OX7//XccPHgQjz32mNShEREREbWZXr164aOPPsLJkydx8eJFODs748SJE1KHRSQJJquIiKhDiI2NxfTp0zF16lQYGhri7NmzOHr0KMaNGyd1aERERETtZvLkybh48SK8vLzwzDPPYM2aNXjw4IHUYRG1KyariIhIUufPn8esWbPwxBNPoKqqCtHR0YiKioKnp6fUoRERERFJwsTEBPv27cN3332H7du3w9PTE9euXZM6LKJ2w2QVERFJ4tKlS3juuefg4eEBhUKB48eP48yZM5g8ebLUoRERERF1CK+88gouXLgAABg3bhx27NghcURE7YPJKiIialdyuRwLFiyAq6srbt68icOHD+O///0vfHx8pA6NiIiIqMMZNWoU4uLi8Pe//x2vvfYa/Pz8UFxcLHVYRG2KySoiImoXaWlpCAoKgpOTE1JSUvDjjz8iISEBvr6+UodGRERE1KHp6+vjs88+Q2RkJOLi4uDi4oLTp09LHRZRm2GyioiI2lRWVhZee+01yGQynDt3DmFhYUhOToafnx/09PSkDo+IiIio05g2bRqSkpLg7u6OadOm4b333kNNTY3UYRHpHJNVRETUJnJycrBs2TI4ODggKioK3333HVJS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1q148803hQ7HIaSlpeH9999HbW0tZs+eLXQ4RERExLcBEhEREU0emzZtwvnz53H+/HlMnTpV6HAcwt///ncsWbIES5YsweHDh4UOh4iIiLgNkIiIiGhyOHz4MP7whz9g3759TFSNwNSpU7Fv3z784Q9/YLKKiIjITrCyioiIiMjBabVaREREQKFQIDc3V+hwHFJSUhKUSiVqa2shkUiEDoeIiMiZsbKKiIiIyNGlpaXh9u3b2Llzp9ChOKydO3fi9u3bSEtLEzoUIiIip8dkFREREZEDKykpQU5ODt555x34+PgIHY7D8vHxwTvvvIOcnByUlJQIHQ4REZFT4zZAIiIiIgel1+uxbNkyLFiwAIWFhUKHMymsX78ely5dwtdffw2RSCR0OERERM6I2wCJiIiIHNWrr76K5uZm7NmzR+hQJo09e/agubkZr776qtChEBEROS0mq4iIiIgcUFVVFbKysvDaa69hzpw5QoczacyZMwevvfYasrKyUFVVJXQ4RERETonbAImIiIgcTG9vL9asWQMXFxeUlpbC1ZV//zie7ty5gzVr1sBgMKC0tBRubm5Ch0RERORMuA2QiIiIyNG8++67OHv2LHJycpiosgFXV1fk5OTg7NmzePfdd4UOh4iIyOnwTzdEREREDqSxsREvvvgi0tLSsGjRIqHDmbQWLVqEtLQ0vPjii2hsbBQ6HCIiIqfCbYBEREREDuThhx9GfX09vv76a3h6egodzqTW1dWFZcuWITQ0FJ9++qnQ4RARETkLbgMkIiIichT79+/HZ599hvfff5+Jqgng6emJ999/H5999hn2798vdDhEREROg5VVRERERA6gra0NERER2LRpE/bu3St0OE4lOTkZhw8fRm1tLXx9fYUOh4iIaLJjZRURERGRI3j22Wfh7u6ON954Q+hQnM4bb7wBd3d3PPvss0KHQkRE5BSYrCIiIiKyc0qlEh999BHeffddSCQSocNxOhKJBO+++y4++ugjKJVKocMhIiKa9LgNkIiIiMiOdXZ2YsmSJVi+fDkKCgqEDsepxcfH4+zZszh//jy8vb2FDoeIiGiy4jZAIiIiInv2yiuvoL29Hbt27RI6FKe3a9cutLe345VXXhE6FCIiokmNySoiIiIiO1VZWYm3334bWVlZmD17ttDhOL3Zs2cjKysLb7/9NiorK4UOh4iIaNLi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
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="DecisionTreeClassifier">DecisionTreeClassifier<a class="anchor-link" href="#DecisionTreeClassifier">&#182;</a></h2>
</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="scikit-learn-&#20915;&#31574;&#26641;&#31639;&#27861;&#31867;&#24211;">scikit-learn &#20915;&#31574;&#26641;&#31639;&#27861;&#31867;&#24211;<a class="anchor-link" href="#scikit-learn-&#20915;&#31574;&#26641;&#31639;&#27861;&#31867;&#24211;">&#182;</a></h3><p>scikit-learn决策树算法类库内部的实现是使用了调优过的CART树算法，既可以做分类，又可以做回归。分类决策树的类对应的是DecisionTreeClassifier，而回归决策树的类对应的是DecisionTreeRegressor。两者的参数定义几乎完全相同，但是意义不全相同。下面就对DecisionTreeClassifier和DecisionTreeRegressor的重要参数做一个总结，重点比较两者参数使用的不同点和调参的注意点。</p>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>DecisionTreeClassifier和DecisionTreeRegressor重要参数调参的注意点</p>
<table>
<thead><tr>
<th>参数</th>
<th>DecisionTreeClassifier </th>
</tr>
</thead>
<tbody>
<tr>
<td>特征选择标准criterion</td>
<td>可以使用"gini"或者"entropy"，前者代表基尼系数，后者代表信息增益。一般来说使用默认值基尼系数"gini"就可以了，即CART算法。除非你更喜欢类似ID3、C4.5的最优特征选择方法。 </td>
</tr>
<tr>
<td>特征划分点选择标准splitter</td>
<td>可以使用"best"或者"random"。前者在特征的所有划分点中找出最优的划分点。后者是随机的在部分划分点中找局部最优的划分点。默认值"best"适合样本量不大的时候，而如果样本数据量非常大，此时决策树构建推荐"random"。</td>
</tr>
<tr>
<td>划分时考虑的最大特征数max_features</td>
<td>可以使用很多种类型的值，默认是"None"，意味着划分时考虑所有的特征数；如果是"log2"意味着划分时最多考虑 $\log_2 N$个特征；如果是"sqrt"或者"auto"意味着划分时最多考虑$\sqrt{N}$个特征。如果是整数，代表考虑的特征绝对数。如果是浮点数，代表考虑特征百分比，即考虑（百分比$\times$N）取整后的特征数。其中N为样本总特征数。一般来说，如果样本特征数不多，比如小于50，我们用默认值"None"就可以了，如果特征数非常多，我们可以灵活使用刚才描述的其它取值来控制划分时考虑的最大特征数，以控制决策树的生成时间。</td>
</tr>
<tr>
<td>决策树最大深度max_depth</td>
<td>决策树的最大深度，默认可以不输入，如果不输入的话，决策树在建立子树的时候不会限制子树的深度。一般来说，数据少或者特征少的时候可以不管这个值。如果模型样本量多，特征也多的情况下，推荐限制这个最大深度，具体的取值取决于数据的分布。常用的可以取值10-100之间。</td>
</tr>
<tr>
<td>内部节点再划分所需最小样本数min_samples_split</td>
<td>这个值限制了子树继续划分的条件，如果某节点的样本数少于min_samples_split，则不会继续再尝试选择最优特征来进行划分。默认是2，如果样本量不大，不需要管这个值。如果样本量非常大，则推荐增大这个值。样本量有10万左右，建立决策树时，min_samples_split的参考值为10。</td>
</tr>
<tr>
<td>叶子节点最少样本数min_samples_leaf</td>
<td>这个值限制了叶子节点最少的样本数，如果某叶子节点数目小于样本数，则会和兄弟节点一起被剪枝。默认值是1，可以输入最少的样本数的整数，或者最少样本数占样本总数的百分比。如果样本量不大，不需要管这个值。如果样本量非常大，则推荐增大这个值。10万样本时min_samples_leaf的参考值为5。</td>
</tr>
<tr>
<td>叶子节点最小的样本权重和min_weight_fraction_leaf</td>
<td>这个值限制了叶子节点所有样本权重和的最小值，如果小于这个值，则会和兄弟节点一起被剪枝。默认值是0，就是不考虑权重问题。一般来说，如果较多样本有缺失值，或者分类树样本的分布类别偏差很大，就会引入样本权重。</td>
</tr>
<tr>
<td>最大叶子节点数max_leaf_nodes</td>
<td>通过限制最大叶子节点数，可以防止过拟合，默认是"None”，即不限制最大的叶子节点数。如果增加了该限制，算法会建立在最大叶子节点数内最优的决策树。如果特征不多，可以不考虑这个值，但是如果特征非常多的话，可以加以限制，具体的值可以通过交叉验证得到。</td>
</tr>
<tr>
<td>类别权重class_weight</td>
<td>指定样本各类别的权重，主要是为了防止训练集某些类别的样本过多，导致训练的决策树过于偏向这些类别。这里可以自己指定各个样本的权重或者用"balanced"，如果使用"balanced"，则算法会自己计算权重，样本量少的类别所对应的样本权重会高。当然，如果你的样本类别分布没有明显的偏倚，则可以不管这个参数，选择默认值"None"即可。  </td>
</tr>
<tr>
<td>节点划分最小不纯度min_impurity_split</td>
<td>这个值限制了决策树的增长，如果某节点的不纯度（基尼系数，信息增益，均方差，绝对差）小于这个阈值，则该节点不再生成子节点，即为叶子节点 。</td>
</tr>
<tr>
<td>数据是否预排序presort</td>
<td>这个值是布尔值，默认值是False即不进行预排序。一般来说，如果样本量少或者限制了一个深度很小的决策树，设置为true可以让划分点选择更加快，加快决策树的建立。如果样本量太大的话，反而没有什么好处。问题是样本量少的时候，速度本来就不慢，所以这个值一般不理它就可以了。</td>
</tr>
</tbody>
</table>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="&#20248;&#21270;&#21644;&#35780;&#20272;&#27169;&#22411;">&#20248;&#21270;&#21644;&#35780;&#20272;&#27169;&#22411;<a class="anchor-link" href="#&#20248;&#21270;&#21644;&#35780;&#20272;&#27169;&#22411;">&#182;</a></h2><ul>
<li><p>评估树模型的效果，并进行优化</p>
<ul>
<li>准确率： $\frac{1}{N}\sum_{i=1}^N{I(\hat{y_i}=y_i)}$<ul>
<li>from sklearn.metrics import accuracy_score</li>
<li>accuracy_score(y_true, y_pred, normalize=True, sample_weight=None)</li>
</ul>
</li>
<li>查准率和查全率      <ul>
<li>classification_report</li>
<li>from sklearn.metrics import precision_recall_curve (两分类问题适用)</li>
<li>precision_recall_curve(y_true, probas_pred, pos_label=None, sample_weight=None)</li>
</ul>
</li>
<li><p>F1 score<br>
查准率和查全率等贡献加权,达到1表示模型最好，0表示最差。</p>
<p>$F1 = 2 \times\frac{ (precision \times recall)}{  (precision + recall)}$</p>
</li>
<li><p>ROC 曲线（Receiver operating characteristic (ROC)）,       FPR  TPR cruve</p>
</li>
</ul>
</li>
</ul>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[4]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">accuracy_score</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">precision_recall_curve</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">classification_report</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="&#25968;&#25454;&#20998;&#21106;&#20026;training-data-&#21644;-test-data">&#25968;&#25454;&#20998;&#21106;&#20026;training data &#21644; test data<a class="anchor-link" href="#&#25968;&#25454;&#20998;&#21106;&#20026;training-data-&#21644;-test-data">&#182;</a></h3><ul>
<li>train_test_split(X,y,test_size=0.33,random_state=10)</li>
</ul>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[5]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>
<span class="n">X_train</span><span class="p">,</span><span class="n">X_test</span><span class="p">,</span> <span class="n">y_train</span><span class="p">,</span> <span class="n">y_test</span> <span class="o">=</span> <span class="n">train_test_split</span><span class="p">(</span><span class="n">iris</span><span class="o">.</span><span class="n">data</span><span class="p">,</span> <span class="n">iris</span><span class="o">.</span><span class="n">target</span><span class="p">,</span><span class="n">test_size</span><span class="o">=</span><span class="mf">0.33</span><span class="p">,</span><span class="n">random_state</span><span class="o">=</span><span class="mi">10</span><span class="p">)</span>  
<span class="nb">print</span><span class="p">(</span><span class="n">X_train</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">X_test</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>(100, 4)
(50, 4)
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="&#25968;&#25454;&#26631;&#20934;&#21270;">&#25968;&#25454;&#26631;&#20934;&#21270;<a class="anchor-link" href="#&#25968;&#25454;&#26631;&#20934;&#21270;">&#182;</a></h3><ul>
<li>机器学习中通常要出各变量进行标准化，使得数据的均值和方差一致</li>
<li>preprocessing.scale(X_train)</li>
</ul>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[6]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn</span> <span class="kn">import</span> <span class="n">preprocessing</span>
<span class="n">X_train_scaled</span> <span class="o">=</span> <span class="n">preprocessing</span><span class="o">.</span><span class="n">scale</span><span class="p">(</span><span class="n">X_train</span><span class="p">)</span>
<span class="c1">#print(X_trained_scaled)</span>

<span class="nb">print</span><span class="p">(</span><span class="n">X_train_scaled</span><span class="o">.</span><span class="n">mean</span><span class="p">(</span><span class="n">axis</span><span class="o">=</span><span class="mi">0</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="n">X_train_scaled</span><span class="o">.</span><span class="n">std</span><span class="p">(</span><span class="n">axis</span><span class="o">=</span><span class="mi">0</span><span class="p">))</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>[-1.98285832e-15  1.39013800e-15 -3.99680289e-17  1.02140518e-16]
[1. 1. 1. 1.]
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<ul>
<li>因为我们需要对训练数据和检验数据用同样的标准化，通常我们采用 Transformer API.</li>
<li>它可以让我们在整个拟合、检验、预测过程中都用同样的标准化,形如：<ul>
<li>利用训练数据生成transformer</li>
<li>利用transformer标准化训练数据</li>
<li>利用transformer标准化测试数据（用同样的均值和方差） </li>
</ul>
</li>
</ul>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[7]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">scaler</span> <span class="o">=</span> <span class="n">preprocessing</span><span class="o">.</span><span class="n">StandardScaler</span><span class="p">()</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">)</span> 
<span class="n">X_train_scaled</span> <span class="o">=</span> <span class="n">scaler</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="n">X_train</span><span class="p">)</span> 
<span class="nb">print</span><span class="p">(</span><span class="n">X_train_scaled</span><span class="o">.</span><span class="n">mean</span><span class="p">(</span><span class="n">axis</span><span class="o">=</span><span class="mi">0</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="n">X_train_scaled</span><span class="o">.</span><span class="n">std</span><span class="p">(</span><span class="n">axis</span><span class="o">=</span><span class="mi">0</span><span class="p">))</span> 
<span class="n">X_test_scaled</span> <span class="o">=</span> <span class="n">scaler</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span> 
<span class="nb">print</span><span class="p">(</span><span class="n">X_test_scaled</span><span class="o">.</span><span class="n">mean</span><span class="p">(</span><span class="n">axis</span><span class="o">=</span><span class="mi">0</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="n">X_test_scaled</span><span class="o">.</span><span class="n">std</span><span class="p">(</span><span class="n">axis</span><span class="o">=</span><span class="mi">0</span><span class="p">))</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>[-1.98285832e-15  1.39013800e-15 -3.99680289e-17  1.02140518e-16]
[1. 1. 1. 1.]
[ 0.04139649 -0.10980216  0.1107187   0.1443679 ]
[1.01388863 0.96108477 0.96033748 0.98774695]
</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<ul>
<li>注意标准化检验数据看起来并不是均值0和方差1？</li>
<li>不过在建模过程中我们可以用如下的方式，使得标准化过程简化。</li>
</ul>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[8]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.pipeline</span> <span class="kn">import</span> <span class="n">Pipeline</span>
<span class="n">pipeline</span> <span class="o">=</span> <span class="n">Pipeline</span><span class="p">([(</span><span class="s2">&quot;scal&quot;</span><span class="p">,</span><span class="n">preprocessing</span><span class="o">.</span><span class="n">StandardScaler</span><span class="p">()),</span> <span class="p">(</span><span class="s1">&#39;clf&#39;</span><span class="p">,</span><span class="n">tree</span><span class="o">.</span><span class="n">DecisionTreeClassifier</span><span class="p">(</span><span class="n">criterion</span><span class="o">=</span><span class="s1">&#39;gini&#39;</span><span class="p">))])</span> 
</pre></div>

     </div>
</div>
</div>
</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<ul>
<li>pipeline</li>
<li>定义一个依次执行的序列，前面是若干transfer,最后一个是需要估计的模型</li>
</ul>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="&#36229;&#21442;&#25968;">&#36229;&#21442;&#25968;<a class="anchor-link" href="#&#36229;&#21442;&#25968;">&#182;</a></h3><ul>
<li>有两种参数，模型参数和超参数，模型参数可以通过数据直接估计到，比如回归中的系数，决策树中的结点划分条件.</li>
<li>而超参数是描述模型的结构，通常需要在估计模型参数前指定，比如决策树中的树深度，叶结点个数等。</li>
</ul>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[9]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">pipeline</span><span class="o">.</span><span class="n">get_params</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[9]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>{&#39;memory&#39;: None,
 &#39;steps&#39;: [(&#39;scal&#39;, StandardScaler(copy=True, with_mean=True, with_std=True)),
  (&#39;clf&#39;,
   DecisionTreeClassifier(class_weight=None, criterion=&#39;gini&#39;, max_depth=None,
               max_features=None, max_leaf_nodes=None,
               min_impurity_decrease=0.0, min_impurity_split=None,
               min_samples_leaf=1, min_samples_split=2,
               min_weight_fraction_leaf=0.0, presort=False, random_state=None,
               splitter=&#39;best&#39;))],
 &#39;scal&#39;: StandardScaler(copy=True, with_mean=True, with_std=True),
 &#39;clf&#39;: DecisionTreeClassifier(class_weight=None, criterion=&#39;gini&#39;, max_depth=None,
             max_features=None, max_leaf_nodes=None,
             min_impurity_decrease=0.0, min_impurity_split=None,
             min_samples_leaf=1, min_samples_split=2,
             min_weight_fraction_leaf=0.0, presort=False, random_state=None,
             splitter=&#39;best&#39;),
 &#39;scal__copy&#39;: True,
 &#39;scal__with_mean&#39;: True,
 &#39;scal__with_std&#39;: True,
 &#39;clf__class_weight&#39;: None,
 &#39;clf__criterion&#39;: &#39;gini&#39;,
 &#39;clf__max_depth&#39;: None,
 &#39;clf__max_features&#39;: None,
 &#39;clf__max_leaf_nodes&#39;: None,
 &#39;clf__min_impurity_decrease&#39;: 0.0,
 &#39;clf__min_impurity_split&#39;: None,
 &#39;clf__min_samples_leaf&#39;: 1,
 &#39;clf__min_samples_split&#39;: 2,
 &#39;clf__min_weight_fraction_leaf&#39;: 0.0,
 &#39;clf__presort&#39;: False,
 &#39;clf__random_state&#39;: None,
 &#39;clf__splitter&#39;: &#39;best&#39;}</pre>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<ul>
<li>我们可以指定若干组超参数</li>
</ul>

<pre><code>    parameters = {  
    'clf__max_depth': (2, 3, 4,5),  
    'clf__min_samples_split': ( 2,3,5),  
    'clf__min_samples_leaf': (1, 2,3)  
    }  


</code></pre>
<ul>
<li>然后利用  GridSearchCV  函数进行模型选择</li>
<li>什么是CV</li>
</ul>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="CV">CV<a class="anchor-link" href="#CV">&#182;</a></h3><ul>
<li><p>交叉验证法，能更稳健地训练、评估和选择模型方法</p>
</li>
<li><p>步骤</p>
<ol>
<li>将数据等分为k等分(folds) (通常 k=10).</li>
<li>利用前 k-1 分(folds)训练样本，得到一个模型 (e.g. the first 9 folds).</li>
<li>利用最后一份评估该模型 (e.g. the 10th fold).</li>
<li>重复 (2) 和 (3) k 次, 每次使用不同的部分检验样本.</li>
<li>平均所有k个模型，得到最终的模型评估.
<img src="data/K-fold_cross_validation_EN.jpg" alt="K-Fold Cross-Validation diagram, courtesy of Wikipedia"><center>K-Fold Cross-Validation diagram, courtesy of Wikipedia</center></li>
</ol>
</li>
</ul>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="&#26426;&#22120;&#23398;&#20064;&#20013;&#20026;&#20160;&#20040;&#38656;&#35201;CV&#26041;&#27861;?">&#26426;&#22120;&#23398;&#20064;&#20013;&#20026;&#20160;&#20040;&#38656;&#35201;CV&#26041;&#27861;?<a class="anchor-link" href="#&#26426;&#22120;&#23398;&#20064;&#20013;&#20026;&#20160;&#20040;&#38656;&#35201;CV&#26041;&#27861;?">&#182;</a></h3><ul>
<li><p>比如在训练树模型时，超参数可能包括</p>

<pre><code>  parameters = {  
  'clf__max_depth': (2, 3, 4,5),  
  'clf__min_samples_split': ( 2,3,5),  
  'clf__min_samples_leaf': (1, 2,3)  
  }  </code></pre>
</li>
<li><p>我们如何选择这些超参数呢？</p>
</li>
<li><p>通过CV方法，我们可以仅仅利用训练数据(training data)就可以评估具有不同超参数的模型。</p>
</li>
<li><p>这样在训练选择数据的时候，我们没有使用test data。当选出最终的模型后，在利用test data 评估最终模型，这样得到的结果相对客观。</p>
</li>
<li><p>有时候我们也可以利用这个独立的test data 做不同统计模型的选择，比如决策树或者回归方法。</p>
</li>
</ul>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<ul>
<li>使用pipeline GridSearch数据标准化，模拟拟合和优化</li>
</ul>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[10]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span>GridSearchCV<span class="o">??</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>Object `GridSearchCV` not found.
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[11]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">GridSearchCV</span>
<span class="n">hyperparameters</span> <span class="o">=</span> <span class="p">{</span> 
    <span class="s1">&#39;clf__max_depth&#39;</span><span class="p">:</span> <span class="p">(</span><span class="mi">2</span><span class="p">,</span> <span class="mi">3</span><span class="p">,</span> <span class="mi">4</span><span class="p">,</span><span class="mi">5</span><span class="p">),</span>  
    <span class="s1">&#39;clf__min_samples_split&#39;</span><span class="p">:</span> <span class="p">(</span> <span class="mi">2</span><span class="p">,</span><span class="mi">3</span><span class="p">,</span><span class="mi">5</span><span class="p">),</span>  
    <span class="s1">&#39;clf__min_samples_leaf&#39;</span><span class="p">:</span> <span class="p">(</span><span class="mi">1</span><span class="p">,</span> <span class="mi">2</span><span class="p">,</span><span class="mi">3</span><span class="p">)</span>
<span class="p">}</span>  
<span class="n">clf</span> <span class="o">=</span> <span class="n">GridSearchCV</span><span class="p">(</span><span class="n">pipeline</span><span class="p">,</span> <span class="n">hyperparameters</span><span class="p">,</span> <span class="n">cv</span><span class="o">=</span><span class="mi">10</span><span class="p">,</span><span class="n">n_jobs</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">verbose</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="n">clf</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span> <span class="n">y_train</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>Fitting 10 folds for each of 36 candidates, totalling 360 fits
</pre>
</div>
</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="application/vnd.jupyter.stderr">
<pre>[Parallel(n_jobs=1)]: Done 360 out of 360 | elapsed:    1.2s finished
</pre>
</div>
</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[11]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>GridSearchCV(cv=10, error_score=&#39;raise&#39;,
       estimator=Pipeline(memory=None,
     steps=[(&#39;scal&#39;, StandardScaler(copy=True, with_mean=True, with_std=True)), (&#39;clf&#39;, DecisionTreeClassifier(class_weight=None, criterion=&#39;gini&#39;, max_depth=None,
            max_features=None, max_leaf_nodes=None,
            min_impurity_decrease=0.0, min_impurity_split=None,
            min_samples_leaf=1, min_samples_split=2,
            min_weight_fraction_leaf=0.0, presort=False, random_state=None,
            splitter=&#39;best&#39;))]),
       fit_params=None, iid=True, n_jobs=1,
       param_grid={&#39;clf__max_depth&#39;: (2, 3, 4, 5), &#39;clf__min_samples_split&#39;: (2, 3, 5), &#39;clf__min_samples_leaf&#39;: (1, 2, 3)},
       pre_dispatch=&#39;2*n_jobs&#39;, refit=True, return_train_score=&#39;warn&#39;,
       scoring=None, verbose=1)</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[12]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">clf</span><span class="o">.</span><span class="n">best_params_</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[12]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>{&#39;clf__max_depth&#39;: 4, &#39;clf__min_samples_leaf&#39;: 1, &#39;clf__min_samples_split&#39;: 2}</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[13]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span> <span class="p">(</span><span class="s1">&#39;最佳效果：</span><span class="si">%0.3f</span><span class="s1">&#39;</span> <span class="o">%</span><span class="k">clf</span>.best_score_)  
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;最优参数&#39;</span><span class="p">)</span>  
<span class="nb">print</span><span class="p">(</span><span class="n">clf</span><span class="o">.</span><span class="n">best_params_</span><span class="p">)</span>
<span class="n">predictions</span> <span class="o">=</span> <span class="n">clf</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>  
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>最佳效果：0.970
最优参数
{&#39;clf__max_depth&#39;: 4, &#39;clf__min_samples_leaf&#39;: 1, &#39;clf__min_samples_split&#39;: 2}
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[14]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span><span class="p">(</span><span class="n">classification_report</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">predictions</span><span class="p">))</span> 
<span class="n">predictions</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>             precision    recall  f1-score   support

          0       1.00      1.00      1.00        15
          1       0.94      0.79      0.86        19
          2       0.79      0.94      0.86        16

avg / total       0.91      0.90      0.90        50

</pre>
</div>
</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[14]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>array([1, 2, 0, 1, 0, 1, 2, 1, 0, 1, 1, 2, 1, 0, 0, 2, 1, 0, 0, 0, 2, 2,
       2, 0, 1, 0, 1, 1, 2, 2, 1, 1, 1, 2, 2, 0, 2, 2, 2, 2, 0, 0, 1, 0,
       1, 0, 2, 2, 2, 2])</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[15]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">besttree</span><span class="o">=</span><span class="n">clf</span><span class="o">.</span><span class="n">best_estimator_</span><span class="o">.</span><span class="n">get_params</span><span class="p">()[</span><span class="s2">&quot;clf&quot;</span><span class="p">]</span>
<span class="n">besttree</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span> <span class="n">y_train</span><span class="p">)</span>
<span class="n">dot_data</span> <span class="o">=</span> <span class="n">tree</span><span class="o">.</span><span class="n">export_graphviz</span><span class="p">(</span><span class="n">besttree</span><span class="p">,</span> <span class="n">out_file</span><span class="o">=</span><span class="s2">&quot;temptree.dot&quot;</span><span class="p">,</span>
                                <span class="n">feature_names</span><span class="o">=</span><span class="n">iris</span><span class="o">.</span><span class="n">feature_names</span><span class="p">,</span>
                                <span class="n">class_names</span><span class="o">=</span><span class="n">iris</span><span class="o">.</span><span class="n">target_names</span><span class="p">,</span>
                                <span class="n">filled</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">rounded</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span>
                                <span class="n">special_characters</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="n">dot_file</span><span class="o">=</span><span class="sa">r</span><span class="s1">&#39;.\temptree.dot&#39;</span>
<span class="n">graph</span> <span class="o">=</span> <span class="n">pydotplus</span><span class="o">.</span><span class="n">graph_from_dot_file</span><span class="p">(</span><span class="n">dot_file</span><span class="p">)</span>  
</pre></div>

     </div>
</div>
</div>
</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[16]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">Image</span><span class="p">(</span><span class="n">graph</span><span class="o">.</span><span class="n">create_png</span><span class="p">())</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[16]:</div>




<div class="jp-RenderedImage jp-OutputArea-output jp-OutputArea-executeResult">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[17]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">predictions</span> <span class="o">=</span> <span class="n">besttree</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>  
<span class="nb">print</span><span class="p">(</span><span class="n">classification_report</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">predictions</span><span class="p">))</span> 
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>             precision    recall  f1-score   support

          0       1.00      1.00      1.00        15
          1       0.94      0.79      0.86        19
          2       0.79      0.94      0.86        16

avg / total       0.91      0.90      0.90        50

</pre>
</div>
</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<ul>
<li>K-nearest neighbor classifirs (KNN)</li>
<li>Logistic regression (LR)</li>
<li>Discriminant analysis (DA)</li>
<li>Naive Bayesian classifir (NB)</li>
<li>Artificial neural networks (ANNs)</li>
<li>Classifiation trees (CTs)</li>
</ul>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h3 id="&#24314;&#27169;&#36807;&#31243;">&#24314;&#27169;&#36807;&#31243;<a class="anchor-link" href="#&#24314;&#27169;&#36807;&#31243;">&#182;</a></h3>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[18]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">data</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_excel</span><span class="p">(</span><span class="s2">&quot;default of credit card clients.xls&quot;</span><span class="p">,</span> <span class="n">skiprows</span><span class="o">=</span><span class="p">[</span><span class="mi">0</span><span class="p">])</span>
<span class="n">data</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[18]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>ID</th>
      <th>LIMIT_BAL</th>
      <th>SEX</th>
      <th>EDUCATION</th>
      <th>MARRIAGE</th>
      <th>AGE</th>
      <th>PAY_0</th>
      <th>PAY_2</th>
      <th>PAY_3</th>
      <th>PAY_4</th>
      <th>...</th>
      <th>BILL_AMT4</th>
      <th>BILL_AMT5</th>
      <th>BILL_AMT6</th>
      <th>PAY_AMT1</th>
      <th>PAY_AMT2</th>
      <th>PAY_AMT3</th>
      <th>PAY_AMT4</th>
      <th>PAY_AMT5</th>
      <th>PAY_AMT6</th>
      <th>default payment next month</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>20000</td>
      <td>2</td>
      <td>2</td>
      <td>1</td>
      <td>24</td>
      <td>2</td>
      <td>2</td>
      <td>-1</td>
      <td>-1</td>
      <td>...</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>689</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>120000</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>26</td>
      <td>-1</td>
      <td>2</td>
      <td>0</td>
      <td>0</td>
      <td>...</td>
      <td>3272</td>
      <td>3455</td>
      <td>3261</td>
      <td>0</td>
      <td>1000</td>
      <td>1000</td>
      <td>1000</td>
      <td>0</td>
      <td>2000</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>90000</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>34</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>...</td>
      <td>14331</td>
      <td>14948</td>
      <td>15549</td>
      <td>1518</td>
      <td>1500</td>
      <td>1000</td>
      <td>1000</td>
      <td>1000</td>
      <td>5000</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>50000</td>
      <td>2</td>
      <td>2</td>
      <td>1</td>
      <td>37</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>...</td>
      <td>28314</td>
      <td>28959</td>
      <td>29547</td>
      <td>2000</td>
      <td>2019</td>
      <td>1200</td>
      <td>1100</td>
      <td>1069</td>
      <td>1000</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>50000</td>
      <td>1</td>
      <td>2</td>
      <td>1</td>
      <td>57</td>
      <td>-1</td>
      <td>0</td>
      <td>-1</td>
      <td>0</td>
      <td>...</td>
      <td>20940</td>
      <td>19146</td>
      <td>19131</td>
      <td>2000</td>
      <td>36681</td>
      <td>10000</td>
      <td>9000</td>
      <td>689</td>
      <td>679</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 25 columns</p>
</div>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[19]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn</span> <span class="kn">import</span> <span class="n">tree</span>
<span class="kn">from</span> <span class="nn">sklearn.cross_validation</span> <span class="kn">import</span> <span class="n">train_test_split</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">accuracy_score</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">precision_recall_curve</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">classification_report</span>
<span class="kn">from</span> <span class="nn">sklearn.pipeline</span> <span class="kn">import</span> <span class="n">Pipeline</span>
<span class="kn">from</span> <span class="nn">sklearn.grid_search</span> <span class="kn">import</span> <span class="n">GridSearchCV</span>
<span class="kn">import</span> <span class="nn">pydotplus</span>
<span class="o">%</span><span class="k">matplotlib</span> inline
<span class="kn">from</span> <span class="nn">IPython.display</span> <span class="kn">import</span> <span class="n">Image</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">data</span><span class="p">[</span><span class="s1">&#39;default payment next month&#39;</span><span class="p">]</span>
<span class="n">X</span> <span class="o">=</span> <span class="n">data</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s2">&quot;ID&quot;</span><span class="p">,</span><span class="s1">&#39;default payment next month&#39;</span><span class="p">],</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="n">X_train</span><span class="p">,</span> <span class="n">X_test</span><span class="p">,</span> <span class="n">y_train</span><span class="p">,</span> <span class="n">y_test</span> <span class="o">=</span> <span class="n">train_test_split</span><span class="p">(</span><span class="n">X</span><span class="p">,</span> <span class="n">y</span><span class="p">,</span> 
                                                  <span class="n">test_size</span><span class="o">=</span><span class="mf">0.2</span><span class="p">,</span> 
                                                    <span class="n">random_state</span><span class="o">=</span><span class="mi">123</span><span class="p">,</span> 
                                                    <span class="n">stratify</span><span class="o">=</span><span class="n">y</span><span class="p">)</span>
<span class="n">pipeline</span> <span class="o">=</span> <span class="n">Pipeline</span><span class="p">([(</span><span class="s1">&#39;clf&#39;</span><span class="p">,</span><span class="n">tree</span><span class="o">.</span><span class="n">DecisionTreeClassifier</span><span class="p">(</span><span class="n">criterion</span><span class="o">=</span><span class="s1">&#39;gini&#39;</span><span class="p">))])</span> 
<span class="n">hyperparameters</span> <span class="o">=</span> <span class="p">{</span> 
    <span class="s1">&#39;clf__max_depth&#39;</span><span class="p">:</span> <span class="p">(</span><span class="mi">10</span><span class="p">,</span> <span class="mi">15</span><span class="p">,</span> <span class="mi">20</span><span class="p">),</span>  
    <span class="s1">&#39;clf__min_samples_split&#39;</span><span class="p">:</span> <span class="p">(</span> <span class="mi">2</span><span class="p">,</span><span class="mi">10</span><span class="p">,</span><span class="mi">20</span><span class="p">),</span>  
    <span class="s1">&#39;clf__min_samples_leaf&#39;</span><span class="p">:</span> <span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">5</span><span class="p">,</span><span class="mi">10</span><span class="p">),</span>
    <span class="s1">&#39;clf__max_features&#39;</span><span class="p">:</span> <span class="p">(</span><span class="mi">5</span><span class="p">,</span><span class="mi">10</span><span class="p">)</span>
<span class="p">}</span>  
<span class="n">clf</span> <span class="o">=</span> <span class="n">GridSearchCV</span><span class="p">(</span><span class="n">pipeline</span><span class="p">,</span> <span class="n">hyperparameters</span><span class="p">,</span> <span class="n">cv</span><span class="o">=</span><span class="mi">10</span><span class="p">,</span><span class="n">n_jobs</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span><span class="n">verbose</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="n">clf</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span> <span class="n">y_train</span><span class="p">)</span>
<span class="n">besttree</span><span class="o">=</span><span class="n">clf</span><span class="o">.</span><span class="n">best_estimator_</span><span class="o">.</span><span class="n">get_params</span><span class="p">()[</span><span class="s2">&quot;clf&quot;</span><span class="p">]</span>
<span class="n">besttree</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span> <span class="n">y_train</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="application/vnd.jupyter.stderr">
<pre>C:\Users\he\Anaconda3\lib\site-packages\sklearn\cross_validation.py:41: DeprecationWarning: This module was deprecated in version 0.18 in favor of the model_selection module into which all the refactored classes and functions are moved. Also note that the interface of the new CV iterators are different from that of this module. This module will be removed in 0.20.
  &#34;This module will be removed in 0.20.&#34;, DeprecationWarning)
C:\Users\he\Anaconda3\lib\site-packages\sklearn\grid_search.py:42: DeprecationWarning: This module was deprecated in version 0.18 in favor of the model_selection module into which all the refactored classes and functions are moved. This module will be removed in 0.20.
  DeprecationWarning)
</pre>
</div>
</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>Fitting 10 folds for each of 54 candidates, totalling 540 fits
</pre>
</div>
</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="application/vnd.jupyter.stderr">
<pre>[Parallel(n_jobs=1)]: Done 540 out of 540 | elapsed:  1.8min finished
</pre>
</div>
</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[19]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>DecisionTreeClassifier(class_weight=None, criterion=&#39;gini&#39;, max_depth=10,
            max_features=10, max_leaf_nodes=None,
            min_impurity_decrease=0.0, min_impurity_split=None,
            min_samples_leaf=1, min_samples_split=20,
            min_weight_fraction_leaf=0.0, presort=False, random_state=None,
            splitter=&#39;best&#39;)</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[20]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">dot_data</span> <span class="o">=</span> <span class="n">tree</span><span class="o">.</span><span class="n">export_graphviz</span><span class="p">(</span><span class="n">besttree</span><span class="p">,</span> <span class="n">out_file</span><span class="o">=</span><span class="s2">&quot;temptree.dot&quot;</span><span class="p">,</span>
                                 <span class="n">feature_names</span><span class="o">=</span><span class="n">X_train</span><span class="o">.</span><span class="n">columns</span><span class="p">,</span>
                                <span class="n">filled</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">rounded</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span>
                                <span class="n">special_characters</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="n">dot_file</span><span class="o">=</span><span class="sa">r</span><span class="s1">&#39;.\temptree.dot&#39;</span>
<span class="n">graph</span> <span class="o">=</span> <span class="n">pydotplus</span><span class="o">.</span><span class="n">graph_from_dot_file</span><span class="p">(</span><span class="n">dot_file</span><span class="p">)</span> 

<span class="n">graph</span><span class="o">.</span><span class="n">write_pdf</span><span class="p">(</span><span class="s2">&quot;default.pdf&quot;</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[20]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>True</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[21]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">predictions</span> <span class="o">=</span> <span class="n">besttree</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>  
<span class="nb">print</span><span class="p">(</span><span class="n">classification_report</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">predictions</span><span class="p">))</span> 
<span class="nb">print</span><span class="p">(</span><span class="n">besttree</span><span class="o">.</span><span class="n">feature_importances_</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>             precision    recall  f1-score   support

          0       0.83      0.94      0.88      4673
          1       0.62      0.32      0.42      1327

avg / total       0.78      0.81      0.78      6000

[0.03514316 0.         0.00652261 0.00628771 0.02154708 0.18420739
 0.39850398 0.01444067 0.03060112 0.01182362 0.03158272 0.04143561
 0.01872796 0.02544174 0.01437987 0.00919085 0.02192613 0.02377842
 0.01419559 0.02263757 0.03484195 0.01318168 0.01960257]
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[22]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Best Score: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">clf</span><span class="o">.</span><span class="n">best_score_</span><span class="p">))</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>Best Score: 0.810125
</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[23]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">predictions_prob</span> <span class="o">=</span> <span class="n">besttree</span><span class="o">.</span><span class="n">predict_proba</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>  
<span class="n">precision</span><span class="p">,</span><span class="n">recall</span><span class="p">,</span><span class="n">thresholds</span><span class="o">=</span><span class="n">precision_recall_curve</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span><span class="n">predictions_prob</span><span class="p">[:,</span><span class="mi">1</span><span class="p">])</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">roc_curve</span> 
<span class="n">fpr</span><span class="p">,</span> <span class="n">tpr</span><span class="p">,</span> <span class="n">thresholds</span> <span class="o">=</span> <span class="n">roc_curve</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">predictions_prob</span><span class="p">[:,</span><span class="mi">1</span><span class="p">])</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[24]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">y_test</span><span class="p">[</span><span class="mi">1</span><span class="p">:</span><span class="mi">10</span><span class="p">],</span><span class="n">predictions_prob</span><span class="p">[:,</span><span class="mi">1</span><span class="p">]</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[24]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>(29444    1
 12392    1
 5591     0
 7282     0
 18238    0
 18318    0
 22939    0
 16704    0
 25910    0
 Name: default payment next month, dtype: int64,
 array([0.1875    , 0.07821229, 0.78927911, ..., 0.09736124, 0.61728395,
        0.19664032]))</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[25]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">10</span><span class="p">,</span> <span class="mi">5</span><span class="p">))</span>
<span class="n">ax1</span> <span class="o">=</span> <span class="n">fig</span><span class="o">.</span><span class="n">add_subplot</span><span class="p">(</span><span class="mi">121</span><span class="p">,</span>  <span class="n">ylabel</span><span class="o">=</span><span class="s2">&quot;查全率&quot;</span><span class="p">,</span><span class="n">xlabel</span><span class="o">=</span><span class="s2">&quot;查准率&quot;</span><span class="p">)</span>
<span class="n">ax1</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">precision</span><span class="p">,</span><span class="n">recall</span><span class="p">)</span>
<span class="n">ax2</span> <span class="o">=</span> <span class="n">fig</span><span class="o">.</span><span class="n">add_subplot</span><span class="p">(</span><span class="mi">122</span><span class="p">,</span>  <span class="n">ylabel</span><span class="o">=</span><span class="s2">&quot;True positive rate&quot;</span><span class="p">,</span><span class="n">xlabel</span><span class="o">=</span><span class="s2">&quot;False positive rate&quot;</span><span class="p">)</span>
<span class="n">ax2</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">fpr</span><span class="p">,</span><span class="n">tpr</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[25]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>[&lt;matplotlib.lines.Line2D at 0x1b093909390&gt;]</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h1 id="&#38543;&#26426;&#26862;&#26519;-random-forrest">&#38543;&#26426;&#26862;&#26519; random forrest<a class="anchor-link" href="#&#38543;&#26426;&#26862;&#26519;-random-forrest">&#182;</a></h1><ul>
<li>利用重抽样方法抽取不同样本，学习简单的决策树，然后将若干简单的决策树联合起来进行决策的方法</li>
<li><p>实例分析. 预测某地(墨西哥)人年收入属于如下哪个区间：</p>
<ol>
<li><p>Below $40,000</p>
</li>
<li><p>$40,000 – 150,000</p>
</li>
<li><p>More than $150,000</p>
</li>
</ol>
</li>
<li><p>可以利用如下信息：</p>
<ol>
<li>Age ,     2. Gender,    3. Highest educational qualification,    4. Working in Industry,     5. Residence in Metro/Non-metro</li>
</ol>
</li>
<li><p>我们用随机森林预测具有下面特征的人的收入：</p>
<ol>
<li>Age : 35 years , 2, Gender : Male , 3. Highest Educational Qualification : Diploma holder, 4. Industry : Manufacturing, 5. Residence : Metro</li>
</ol>
</li>
</ul>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>随机森林中每一棵树都可以看做是一棵CART（分类回归树），这里假设森林中有5棵CART树，总特征个数N=5，我们取m=1（这里假设每个CART树对应一个不同的特征）。</p>
<p>CART 1 : Variable Age</p>
<p><img src="data\rf1.png" alt=""></p>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>CART 2 : Variable Gender</p>
<p><img src="data\rf2.png" alt=""></p>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>CART 3 : Variable Education</p>
<p><img src="data\rf3.png" alt=""></p>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>CART 4 : Variable Residence</p>
<p><img src="data\rf4.png" alt=""></p>
<p>CART 5 : Variable Industry</p>
<p><img src="data\rf5.png" alt=""></p>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<ul>
<li><p>我们可以利用这5个决策树模型的预测均值来计算每个工资水平的概率.</p>

<pre><code>  1. Age : 35 years , 2, Gender : Male , 3. Highest Educational Qualification : Diploma holder, 4. Industry : Manufacturing, 5. Residence : Metro</code></pre>
</li>
<li><p>每个决策树模型给出的预测如下：</p>
</li>
</ul>

</div>
</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p><img src="data\DF.png" alt=""></p>
<ul>
<li>因此如果我们用平均概率来预测，则可以进行如下预测：这个人的收入层次70%是一等，大约24%为二等，6%为三等，如果要给出确定的预测，可以预测该人属于一等收入层次（小于$40,000）。</li>
</ul>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[26]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.ensemble</span> <span class="kn">import</span> <span class="n">RandomForestClassifier</span>
<span class="n">parameter_gridsearch</span> <span class="o">=</span> <span class="p">{</span>
                 <span class="s1">&#39;max_depth&#39;</span> <span class="p">:</span> <span class="p">[</span><span class="mi">5</span><span class="p">,</span><span class="mi">7</span><span class="p">],</span>  <span class="c1">#depth of each decision tree</span>
                 <span class="s1">&#39;n_estimators&#39;</span><span class="p">:</span> <span class="p">[</span><span class="mi">50</span><span class="p">,</span><span class="mi">40</span><span class="p">],</span>  <span class="c1">#count of decision tree      </span>
       
                 <span class="p">}</span>
<span class="n">randomforest</span> <span class="o">=</span> <span class="n">RandomForestClassifier</span><span class="p">()</span>  
<span class="n">gridsearch</span> <span class="o">=</span> <span class="n">GridSearchCV</span><span class="p">(</span><span class="n">randomforest</span><span class="p">,</span>            
                               <span class="n">param_grid</span><span class="o">=</span><span class="n">parameter_gridsearch</span>
                                <span class="p">)</span>


<span class="n">gridsearch</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span><span class="n">y_train</span><span class="p">)</span>  
 
<span class="n">parameters</span> <span class="o">=</span> <span class="n">gridsearch</span><span class="o">.</span><span class="n">best_params_</span>
<span class="nb">print</span><span class="p">(</span><span class="n">parameters</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Best Score: </span><span class="si">{}</span><span class="s1">&#39;</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">gridsearch</span><span class="o">.</span><span class="n">best_score_</span><span class="p">))</span>
<span class="n">predictions</span> <span class="o">=</span> <span class="n">gridsearch</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>  
<span class="nb">print</span><span class="p">(</span><span class="n">classification_report</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">predictions</span><span class="p">))</span>  
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="application/vnd.jupyter.stderr">
<pre>C:\Users\he\Anaconda3\lib\site-packages\sklearn\ensemble\weight_boosting.py:29: DeprecationWarning: numpy.core.umath_tests is an internal NumPy module and should not be imported. It will be removed in a future NumPy release.
  from numpy.core.umath_tests import inner1d
</pre>
</div>
</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>


<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain">
<pre>{&#39;max_depth&#39;: 7, &#39;n_estimators&#39;: 50}
Best Score: 0.8181666666666667
             precision    recall  f1-score   support

          0       0.83      0.96      0.89      4673
          1       0.69      0.32      0.44      1327

avg / total       0.80      0.82      0.79      6000

</pre>
</div>
</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[27]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">predictions_prob1</span> <span class="o">=</span> <span class="n">gridsearch</span><span class="o">.</span><span class="n">predict_proba</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>  
<span class="n">precision1</span><span class="p">,</span><span class="n">recall1</span><span class="p">,</span><span class="n">thresholds</span><span class="o">=</span><span class="n">precision_recall_curve</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span><span class="n">predictions_prob1</span><span class="p">[:,</span><span class="mi">1</span><span class="p">])</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">roc_curve</span> 
<span class="n">fpr1</span><span class="p">,</span> <span class="n">tpr1</span><span class="p">,</span> <span class="n">thresholds</span> <span class="o">=</span> <span class="n">roc_curve</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">predictions_prob1</span><span class="p">[:,</span><span class="mi">1</span><span class="p">])</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[28]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">10</span><span class="p">,</span> <span class="mi">5</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">121</span><span class="p">,</span>  <span class="n">ylabel</span><span class="o">=</span><span class="s2">&quot;查全率&quot;</span><span class="p">,</span><span class="n">xlabel</span><span class="o">=</span><span class="s2">&quot;查准率&quot;</span><span class="p">,</span><span class="n">title</span><span class="o">=</span><span class="s2">&quot;precision recall curve&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">precision1</span><span class="p">,</span><span class="n">recall1</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="s2">&quot;random forrest&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">precision</span><span class="p">,</span><span class="n">recall</span><span class="p">,</span><span class="n">color</span><span class="o">=</span><span class="s2">&quot;red&quot;</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="s2">&quot;CART&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">loc</span><span class="o">=</span><span class="s2">&quot;best&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">122</span><span class="p">,</span>  <span class="n">ylabel</span><span class="o">=</span><span class="s2">&quot;True positive rate&quot;</span><span class="p">,</span><span class="n">xlabel</span><span class="o">=</span><span class="s2">&quot;False positive rate&quot;</span><span class="p">,</span><span class="n">title</span><span class="o">=</span><span class="s2">&quot;ROC curve&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">fpr1</span><span class="p">,</span><span class="n">tpr1</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="s2">&quot;random forrest&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">fpr</span><span class="p">,</span><span class="n">tpr</span><span class="p">,</span><span class="n">color</span><span class="o">=</span><span class="s2">&quot;red&quot;</span><span class="p">,</span><span class="n">label</span><span class="o">=</span><span class="s2">&quot;CART&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">loc</span><span class="o">=</span><span class="s2">&quot;best&quot;</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[28]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>&lt;matplotlib.legend.Legend at 0x1b093ca9dd8&gt;</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div>
</body>







</html>
