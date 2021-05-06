---
layout: post
comments: true
title : Visualization [CHI]
categories: [Practices]
---


<html>
<head><meta charset="utf-8" />

<title>2019_Lec06_visualization</title>

<script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>



<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.7.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.7.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.7.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff2?v=4.7.0') format('woff2'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.7.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.7.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.7.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.fa-pull-left {
  float: left;
}
.fa-pull-right {
  float: right;
}
.fa.fa-pull-left {
  margin-right: .3em;
}
.fa.fa-pull-right {
  margin-left: .3em;
}
/* Deprecated as of 4.4.0 */
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
.fa-pulse {
  -webkit-animation: fa-spin 1s infinite steps(8);
  animation: fa-spin 1s infinite steps(8);
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=1)";
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2)";
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=3)";
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1)";
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1)";
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook-f:before,
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-feed:before,
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before,
.fa-gratipay:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper-pp:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-resistance:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-y-combinator-square:before,
.fa-yc-square:before,
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
.fa-buysellads:before {
  content: "\f20d";
}
.fa-connectdevelop:before {
  content: "\f20e";
}
.fa-dashcube:before {
  content: "\f210";
}
.fa-forumbee:before {
  content: "\f211";
}
.fa-leanpub:before {
  content: "\f212";
}
.fa-sellsy:before {
  content: "\f213";
}
.fa-shirtsinbulk:before {
  content: "\f214";
}
.fa-simplybuilt:before {
  content: "\f215";
}
.fa-skyatlas:before {
  content: "\f216";
}
.fa-cart-plus:before {
  content: "\f217";
}
.fa-cart-arrow-down:before {
  content: "\f218";
}
.fa-diamond:before {
  content: "\f219";
}
.fa-ship:before {
  content: "\f21a";
}
.fa-user-secret:before {
  content: "\f21b";
}
.fa-motorcycle:before {
  content: "\f21c";
}
.fa-street-view:before {
  content: "\f21d";
}
.fa-heartbeat:before {
  content: "\f21e";
}
.fa-venus:before {
  content: "\f221";
}
.fa-mars:before {
  content: "\f222";
}
.fa-mercury:before {
  content: "\f223";
}
.fa-intersex:before,
.fa-transgender:before {
  content: "\f224";
}
.fa-transgender-alt:before {
  content: "\f225";
}
.fa-venus-double:before {
  content: "\f226";
}
.fa-mars-double:before {
  content: "\f227";
}
.fa-venus-mars:before {
  content: "\f228";
}
.fa-mars-stroke:before {
  content: "\f229";
}
.fa-mars-stroke-v:before {
  content: "\f22a";
}
.fa-mars-stroke-h:before {
  content: "\f22b";
}
.fa-neuter:before {
  content: "\f22c";
}
.fa-genderless:before {
  content: "\f22d";
}
.fa-facebook-official:before {
  content: "\f230";
}
.fa-pinterest-p:before {
  content: "\f231";
}
.fa-whatsapp:before {
  content: "\f232";
}
.fa-server:before {
  content: "\f233";
}
.fa-user-plus:before {
  content: "\f234";
}
.fa-user-times:before {
  content: "\f235";
}
.fa-hotel:before,
.fa-bed:before {
  content: "\f236";
}
.fa-viacoin:before {
  content: "\f237";
}
.fa-train:before {
  content: "\f238";
}
.fa-subway:before {
  content: "\f239";
}
.fa-medium:before {
  content: "\f23a";
}
.fa-yc:before,
.fa-y-combinator:before {
  content: "\f23b";
}
.fa-optin-monster:before {
  content: "\f23c";
}
.fa-opencart:before {
  content: "\f23d";
}
.fa-expeditedssl:before {
  content: "\f23e";
}
.fa-battery-4:before,
.fa-battery:before,
.fa-battery-full:before {
  content: "\f240";
}
.fa-battery-3:before,
.fa-battery-three-quarters:before {
  content: "\f241";
}
.fa-battery-2:before,
.fa-battery-half:before {
  content: "\f242";
}
.fa-battery-1:before,
.fa-battery-quarter:before {
  content: "\f243";
}
.fa-battery-0:before,
.fa-battery-empty:before {
  content: "\f244";
}
.fa-mouse-pointer:before {
  content: "\f245";
}
.fa-i-cursor:before {
  content: "\f246";
}
.fa-object-group:before {
  content: "\f247";
}
.fa-object-ungroup:before {
  content: "\f248";
}
.fa-sticky-note:before {
  content: "\f249";
}
.fa-sticky-note-o:before {
  content: "\f24a";
}
.fa-cc-jcb:before {
  content: "\f24b";
}
.fa-cc-diners-club:before {
  content: "\f24c";
}
.fa-clone:before {
  content: "\f24d";
}
.fa-balance-scale:before {
  content: "\f24e";
}
.fa-hourglass-o:before {
  content: "\f250";
}
.fa-hourglass-1:before,
.fa-hourglass-start:before {
  content: "\f251";
}
.fa-hourglass-2:before,
.fa-hourglass-half:before {
  content: "\f252";
}
.fa-hourglass-3:before,
.fa-hourglass-end:before {
  content: "\f253";
}
.fa-hourglass:before {
  content: "\f254";
}
.fa-hand-grab-o:before,
.fa-hand-rock-o:before {
  content: "\f255";
}
.fa-hand-stop-o:before,
.fa-hand-paper-o:before {
  content: "\f256";
}
.fa-hand-scissors-o:before {
  content: "\f257";
}
.fa-hand-lizard-o:before {
  content: "\f258";
}
.fa-hand-spock-o:before {
  content: "\f259";
}
.fa-hand-pointer-o:before {
  content: "\f25a";
}
.fa-hand-peace-o:before {
  content: "\f25b";
}
.fa-trademark:before {
  content: "\f25c";
}
.fa-registered:before {
  content: "\f25d";
}
.fa-creative-commons:before {
  content: "\f25e";
}
.fa-gg:before {
  content: "\f260";
}
.fa-gg-circle:before {
  content: "\f261";
}
.fa-tripadvisor:before {
  content: "\f262";
}
.fa-odnoklassniki:before {
  content: "\f263";
}
.fa-odnoklassniki-square:before {
  content: "\f264";
}
.fa-get-pocket:before {
  content: "\f265";
}
.fa-wikipedia-w:before {
  content: "\f266";
}
.fa-safari:before {
  content: "\f267";
}
.fa-chrome:before {
  content: "\f268";
}
.fa-firefox:before {
  content: "\f269";
}
.fa-opera:before {
  content: "\f26a";
}
.fa-internet-explorer:before {
  content: "\f26b";
}
.fa-tv:before,
.fa-television:before {
  content: "\f26c";
}
.fa-contao:before {
  content: "\f26d";
}
.fa-500px:before {
  content: "\f26e";
}
.fa-amazon:before {
  content: "\f270";
}
.fa-calendar-plus-o:before {
  content: "\f271";
}
.fa-calendar-minus-o:before {
  content: "\f272";
}
.fa-calendar-times-o:before {
  content: "\f273";
}
.fa-calendar-check-o:before {
  content: "\f274";
}
.fa-industry:before {
  content: "\f275";
}
.fa-map-pin:before {
  content: "\f276";
}
.fa-map-signs:before {
  content: "\f277";
}
.fa-map-o:before {
  content: "\f278";
}
.fa-map:before {
  content: "\f279";
}
.fa-commenting:before {
  content: "\f27a";
}
.fa-commenting-o:before {
  content: "\f27b";
}
.fa-houzz:before {
  content: "\f27c";
}
.fa-vimeo:before {
  content: "\f27d";
}
.fa-black-tie:before {
  content: "\f27e";
}
.fa-fonticons:before {
  content: "\f280";
}
.fa-reddit-alien:before {
  content: "\f281";
}
.fa-edge:before {
  content: "\f282";
}
.fa-credit-card-alt:before {
  content: "\f283";
}
.fa-codiepie:before {
  content: "\f284";
}
.fa-modx:before {
  content: "\f285";
}
.fa-fort-awesome:before {
  content: "\f286";
}
.fa-usb:before {
  content: "\f287";
}
.fa-product-hunt:before {
  content: "\f288";
}
.fa-mixcloud:before {
  content: "\f289";
}
.fa-scribd:before {
  content: "\f28a";
}
.fa-pause-circle:before {
  content: "\f28b";
}
.fa-pause-circle-o:before {
  content: "\f28c";
}
.fa-stop-circle:before {
  content: "\f28d";
}
.fa-stop-circle-o:before {
  content: "\f28e";
}
.fa-shopping-bag:before {
  content: "\f290";
}
.fa-shopping-basket:before {
  content: "\f291";
}
.fa-hashtag:before {
  content: "\f292";
}
.fa-bluetooth:before {
  content: "\f293";
}
.fa-bluetooth-b:before {
  content: "\f294";
}
.fa-percent:before {
  content: "\f295";
}
.fa-gitlab:before {
  content: "\f296";
}
.fa-wpbeginner:before {
  content: "\f297";
}
.fa-wpforms:before {
  content: "\f298";
}
.fa-envira:before {
  content: "\f299";
}
.fa-universal-access:before {
  content: "\f29a";
}
.fa-wheelchair-alt:before {
  content: "\f29b";
}
.fa-question-circle-o:before {
  content: "\f29c";
}
.fa-blind:before {
  content: "\f29d";
}
.fa-audio-description:before {
  content: "\f29e";
}
.fa-volume-control-phone:before {
  content: "\f2a0";
}
.fa-braille:before {
  content: "\f2a1";
}
.fa-assistive-listening-systems:before {
  content: "\f2a2";
}
.fa-asl-interpreting:before,
.fa-american-sign-language-interpreting:before {
  content: "\f2a3";
}
.fa-deafness:before,
.fa-hard-of-hearing:before,
.fa-deaf:before {
  content: "\f2a4";
}
.fa-glide:before {
  content: "\f2a5";
}
.fa-glide-g:before {
  content: "\f2a6";
}
.fa-signing:before,
.fa-sign-language:before {
  content: "\f2a7";
}
.fa-low-vision:before {
  content: "\f2a8";
}
.fa-viadeo:before {
  content: "\f2a9";
}
.fa-viadeo-square:before {
  content: "\f2aa";
}
.fa-snapchat:before {
  content: "\f2ab";
}
.fa-snapchat-ghost:before {
  content: "\f2ac";
}
.fa-snapchat-square:before {
  content: "\f2ad";
}
.fa-pied-piper:before {
  content: "\f2ae";
}
.fa-first-order:before {
  content: "\f2b0";
}
.fa-yoast:before {
  content: "\f2b1";
}
.fa-themeisle:before {
  content: "\f2b2";
}
.fa-google-plus-circle:before,
.fa-google-plus-official:before {
  content: "\f2b3";
}
.fa-fa:before,
.fa-font-awesome:before {
  content: "\f2b4";
}
.fa-handshake-o:before {
  content: "\f2b5";
}
.fa-envelope-open:before {
  content: "\f2b6";
}
.fa-envelope-open-o:before {
  content: "\f2b7";
}
.fa-linode:before {
  content: "\f2b8";
}
.fa-address-book:before {
  content: "\f2b9";
}
.fa-address-book-o:before {
  content: "\f2ba";
}
.fa-vcard:before,
.fa-address-card:before {
  content: "\f2bb";
}
.fa-vcard-o:before,
.fa-address-card-o:before {
  content: "\f2bc";
}
.fa-user-circle:before {
  content: "\f2bd";
}
.fa-user-circle-o:before {
  content: "\f2be";
}
.fa-user-o:before {
  content: "\f2c0";
}
.fa-id-badge:before {
  content: "\f2c1";
}
.fa-drivers-license:before,
.fa-id-card:before {
  content: "\f2c2";
}
.fa-drivers-license-o:before,
.fa-id-card-o:before {
  content: "\f2c3";
}
.fa-quora:before {
  content: "\f2c4";
}
.fa-free-code-camp:before {
  content: "\f2c5";
}
.fa-telegram:before {
  content: "\f2c6";
}
.fa-thermometer-4:before,
.fa-thermometer:before,
.fa-thermometer-full:before {
  content: "\f2c7";
}
.fa-thermometer-3:before,
.fa-thermometer-three-quarters:before {
  content: "\f2c8";
}
.fa-thermometer-2:before,
.fa-thermometer-half:before {
  content: "\f2c9";
}
.fa-thermometer-1:before,
.fa-thermometer-quarter:before {
  content: "\f2ca";
}
.fa-thermometer-0:before,
.fa-thermometer-empty:before {
  content: "\f2cb";
}
.fa-shower:before {
  content: "\f2cc";
}
.fa-bathtub:before,
.fa-s15:before,
.fa-bath:before {
  content: "\f2cd";
}
.fa-podcast:before {
  content: "\f2ce";
}
.fa-window-maximize:before {
  content: "\f2d0";
}
.fa-window-minimize:before {
  content: "\f2d1";
}
.fa-window-restore:before {
  content: "\f2d2";
}
.fa-times-rectangle:before,
.fa-window-close:before {
  content: "\f2d3";
}
.fa-times-rectangle-o:before,
.fa-window-close-o:before {
  content: "\f2d4";
}
.fa-bandcamp:before {
  content: "\f2d5";
}
.fa-grav:before {
  content: "\f2d6";
}
.fa-etsy:before {
  content: "\f2d7";
}
.fa-imdb:before {
  content: "\f2d8";
}
.fa-ravelry:before {
  content: "\f2d9";
}
.fa-eercast:before {
  content: "\f2da";
}
.fa-microchip:before {
  content: "\f2db";
}
.fa-snowflake-o:before {
  content: "\f2dc";
}
.fa-superpowers:before {
  content: "\f2dd";
}
.fa-wpexplorer:before {
  content: "\f2de";
}
.fa-meetup:before {
  content: "\f2e0";
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
div.traceback-wrapper pre.traceback {
  max-height: 600px;
  overflow: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 5px;
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
[dir="rtl"] #ipython_notebook {
  margin-right: 10px;
  margin-left: 0;
}
[dir="rtl"] #ipython_notebook.pull-left {
  float: right !important;
  float: right;
}
.flex-spacer {
  flex: 1;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#kernel_logo_widget {
  margin: 0 10px;
}
span#login_widget {
  float: right;
}
[dir="rtl"] span#login_widget {
  float: left;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
.modal-header {
  cursor: move;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
[dir="rtl"] .center-nav form.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] .center-nav .navbar-text {
  float: right;
}
[dir="rtl"] .navbar-inner {
  text-align: right;
}
[dir="rtl"] div.text-left {
  text-align: right;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  position: absolute;
  display: block;
  width: 100%;
  height: 100%;
  overflow: hidden;
  cursor: pointer;
  opacity: 0;
  z-index: 2;
}
.alternate_upload .btn-xs > input.fileinput {
  margin: -1px -5px;
}
.alternate_upload .btn-upload {
  position: relative;
  height: 22px;
}
::-webkit-file-upload-button {
  cursor: pointer;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
ul#tabs {
  margin-bottom: 4px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
[dir="rtl"] ul#tabs.nav-tabs > li {
  float: right;
}
[dir="rtl"] ul#tabs.nav.nav-tabs {
  padding-right: 0;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons .pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .list_toolbar .col-sm-4,
[dir="rtl"] .list_toolbar .col-sm-8 {
  float: right;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: text-bottom;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
[dir="rtl"] .list_item > div input {
  margin-right: 0;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_modified {
  margin-right: 7px;
  margin-left: 7px;
}
[dir="rtl"] .item_modified.pull-right {
  float: left !important;
  float: left;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
[dir="rtl"] .item_buttons.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .item_buttons .kernel-name {
  margin-left: 7px;
  float: right;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
.sort_button {
  display: inline-block;
  padding-left: 7px;
}
[dir="rtl"] .sort_button.pull-right {
  float: left !important;
  float: left;
}
#tree-selector {
  padding-right: 0px;
}
#button-select-all {
  min-width: 50px;
}
[dir="rtl"] #button-select-all.btn {
  float: right ;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
  margin-top: 2px;
  height: 16px;
}
[dir="rtl"] #select-all.pull-left {
  float: right !important;
  float: right;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.fa-pull-left {
  margin-right: .3em;
}
.folder_icon:before.fa-pull-right {
  margin-left: .3em;
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.fa-pull-left {
  margin-right: .3em;
}
.file_icon:before.fa-pull-right {
  margin-left: .3em;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
#new-menu .dropdown-header {
  font-size: 10px;
  border-bottom: 1px solid #e5e5e5;
  padding: 0 0 3px;
  margin: -3px 20px 0;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.move-button {
  display: none;
}
.download-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
.CodeMirror-dialog {
  background-color: #fff;
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI escape sequences */
/* The color values are a mix of
   http://www.xcolors.net/dl/baskerville-ivorylight and
   http://www.xcolors.net/dl/euphrasia */
.ansi-black-fg {
  color: #3E424D;
}
.ansi-black-bg {
  background-color: #3E424D;
}
.ansi-black-intense-fg {
  color: #282C36;
}
.ansi-black-intense-bg {
  background-color: #282C36;
}
.ansi-red-fg {
  color: #E75C58;
}
.ansi-red-bg {
  background-color: #E75C58;
}
.ansi-red-intense-fg {
  color: #B22B31;
}
.ansi-red-intense-bg {
  background-color: #B22B31;
}
.ansi-green-fg {
  color: #00A250;
}
.ansi-green-bg {
  background-color: #00A250;
}
.ansi-green-intense-fg {
  color: #007427;
}
.ansi-green-intense-bg {
  background-color: #007427;
}
.ansi-yellow-fg {
  color: #DDB62B;
}
.ansi-yellow-bg {
  background-color: #DDB62B;
}
.ansi-yellow-intense-fg {
  color: #B27D12;
}
.ansi-yellow-intense-bg {
  background-color: #B27D12;
}
.ansi-blue-fg {
  color: #208FFB;
}
.ansi-blue-bg {
  background-color: #208FFB;
}
.ansi-blue-intense-fg {
  color: #0065CA;
}
.ansi-blue-intense-bg {
  background-color: #0065CA;
}
.ansi-magenta-fg {
  color: #D160C4;
}
.ansi-magenta-bg {
  background-color: #D160C4;
}
.ansi-magenta-intense-fg {
  color: #A03196;
}
.ansi-magenta-intense-bg {
  background-color: #A03196;
}
.ansi-cyan-fg {
  color: #60C6C8;
}
.ansi-cyan-bg {
  background-color: #60C6C8;
}
.ansi-cyan-intense-fg {
  color: #258F8F;
}
.ansi-cyan-intense-bg {
  background-color: #258F8F;
}
.ansi-white-fg {
  color: #C5C1B4;
}
.ansi-white-bg {
  background-color: #C5C1B4;
}
.ansi-white-intense-fg {
  color: #A1A6B2;
}
.ansi-white-intense-bg {
  background-color: #A1A6B2;
}
.ansi-default-inverse-fg {
  color: #FFFFFF;
}
.ansi-default-inverse-bg {
  background-color: #000000;
}
.ansi-bold {
  font-weight: bold;
}
.ansi-underline {
  text-decoration: underline;
}
/* The following styles are deprecated an will be removed in a future version */
.ansibold {
  font-weight: bold;
}
.ansi-inverse {
  outline: 0.5px dotted;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  position: relative;
  overflow: visible;
}
div.cell:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: transparent;
}
div.cell.jupyter-soft-selected {
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected,
div.cell.selected.jupyter-soft-selected {
  border-color: #ababab;
}
div.cell.selected:before,
div.cell.selected.jupyter-soft-selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #42A5F5;
}
@media print {
  div.cell.selected,
  div.cell.selected.jupyter-soft-selected {
    border-color: transparent;
  }
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
}
.edit_mode div.cell.selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #66BB6A;
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  /* Note that this should set vertical padding only, since CodeMirror assumes
       that horizontal padding will be set on CodeMirror pre */
  padding: 0.4em 0;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. This sets horizontal padding only,
    use .CodeMirror-lines for vertical */
  padding: 0 0.4em;
  border: 0;
  border-radius: 0;
}
.CodeMirror-cursor {
  border-left: 1.4px solid black;
}
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .CodeMirror-cursor {
    border-left: 2px solid black;
  }
}
@media screen and (min-width: 4320px) {
  .CodeMirror-cursor {
    border-left: 4px solid black;
  }
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
div.output_area .mglyph > img {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 1px 0 1px 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul:not(.list-inline),
.rendered_html ol:not(.list-inline) {
  padding-left: 2em;
}
.rendered_html ul {
  list-style: disc;
}
.rendered_html ul ul {
  list-style: square;
  margin-top: 0;
}
.rendered_html ul ul ul {
  list-style: circle;
}
.rendered_html ol {
  list-style: decimal;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin-top: 0;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
  padding: 0px;
  background-color: #fff;
}
.rendered_html code {
  background-color: #eff0f1;
}
.rendered_html p code {
  padding: 1px 5px;
}
.rendered_html pre code {
  background-color: #fff;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  color: #000;
  font-size: 100%;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: none;
  border-collapse: collapse;
  border-spacing: 0;
  color: black;
  font-size: 12px;
  table-layout: fixed;
}
.rendered_html thead {
  border-bottom: 1px solid black;
  vertical-align: bottom;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  text-align: right;
  vertical-align: middle;
  padding: 0.5em 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html tbody tr:nth-child(odd) {
  background: #f5f5f5;
}
.rendered_html tbody tr:hover {
  background: rgba(66, 165, 245, 0.2);
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
.rendered_html .alert {
  margin-bottom: initial;
}
.rendered_html * + .alert {
  margin-top: 1em;
}
[dir="rtl"] .rendered_html p {
  text-align: right;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.rendered .rendered_html tr,
.text_cell.rendered .rendered_html th,
.text_cell.rendered .rendered_html td {
  max-width: none;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.text_cell .dropzone .input_area {
  border: 2px dashed #bababa;
  margin: -1px;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
.jupyter-keybindings {
  padding: 1px;
  line-height: 24px;
  border-bottom: 1px solid gray;
}
.jupyter-keybindings input {
  margin: 0;
  padding: 0;
  border: none;
}
.jupyter-keybindings i {
  padding: 6px;
}
.well code {
  background-color: #ffffff;
  border-color: #ababab;
  border-width: 1px;
  border-style: solid;
  padding: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.tags_button_container {
  width: 100%;
  display: flex;
}
.tag-container {
  display: flex;
  flex-direction: row;
  flex-grow: 1;
  overflow: hidden;
  position: relative;
}
.tag-container > * {
  margin: 0 4px;
}
.remove-tag-btn {
  margin-left: 4px;
}
.tags-input {
  display: flex;
}
.cell-tag:last-child:after {
  content: "";
  position: absolute;
  right: 0;
  width: 40px;
  height: 100%;
  /* Fade to background color of cell toolbar */
  background: linear-gradient(to right, rgba(0, 0, 0, 0), #EEE);
}
.tags-input > * {
  margin-left: 4px;
}
.cell-tag,
.tags-input input,
.tags-input button {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  box-shadow: none;
  width: inherit;
  font-size: inherit;
  height: 22px;
  line-height: 22px;
  padding: 0px 4px;
  display: inline-block;
}
.cell-tag:focus,
.tags-input input:focus,
.tags-input button:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.cell-tag::-moz-placeholder,
.tags-input input::-moz-placeholder,
.tags-input button::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.cell-tag:-ms-input-placeholder,
.tags-input input:-ms-input-placeholder,
.tags-input button:-ms-input-placeholder {
  color: #999;
}
.cell-tag::-webkit-input-placeholder,
.tags-input input::-webkit-input-placeholder,
.tags-input button::-webkit-input-placeholder {
  color: #999;
}
.cell-tag::-ms-expand,
.tags-input input::-ms-expand,
.tags-input button::-ms-expand {
  border: 0;
  background-color: transparent;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
.cell-tag[readonly],
.tags-input input[readonly],
.tags-input button[readonly],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  background-color: #eeeeee;
  opacity: 1;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  cursor: not-allowed;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button {
  height: auto;
}
select.cell-tag,
select.tags-input input,
select.tags-input button {
  height: 30px;
  line-height: 30px;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button,
select[multiple].cell-tag,
select[multiple].tags-input input,
select[multiple].tags-input button {
  height: auto;
}
.cell-tag,
.tags-input button {
  padding: 0px 4px;
}
.cell-tag {
  background-color: #fff;
  white-space: nowrap;
}
.tags-input input[type=text]:focus {
  outline: none;
  box-shadow: none;
  border-color: #ccc;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
[dir="rtl"] #kernel_logo_widget {
  float: left !important;
  float: left;
}
.modal .modal-body .move-path {
  display: flex;
  flex-direction: row;
  justify-content: space;
  align-items: center;
}
.modal .modal-body .move-path .server-root {
  padding-right: 20px;
}
.modal .modal-body .move-path .path-input {
  flex: 1;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
[dir="rtl"] #menubar .navbar-toggle {
  float: right;
}
[dir="rtl"] #menubar .navbar-collapse {
  clear: right;
}
[dir="rtl"] #menubar .navbar-nav {
  float: right;
}
[dir="rtl"] #menubar .nav {
  padding-right: 0px;
}
[dir="rtl"] #menubar .navbar-nav > li {
  float: right;
}
[dir="rtl"] #menubar .navbar-right {
  float: left !important;
}
[dir="rtl"] ul.dropdown-menu {
  text-align: right;
  left: auto;
}
[dir="rtl"] ul#new-menu.dropdown-menu {
  right: auto;
  left: 0;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
[dir="rtl"] i.menu-icon.pull-right {
  float: left !important;
  float: left;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
[dir="rtl"] ul#help_menu li a {
  padding-left: 2.2em;
}
[dir="rtl"] ul#help_menu li a i {
  margin-right: 0;
  margin-left: -1.2em;
}
[dir="rtl"] ul#help_menu li a i.pull-right {
  float: left !important;
  float: left;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
[dir="rtl"] .dropdown-submenu > .dropdown-menu {
  right: 100%;
  margin-right: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.fa-pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.fa-pull-right {
  margin-left: .3em;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
[dir="rtl"] .dropdown-submenu > a:after {
  float: left;
  content: "\f0d9";
  margin-right: 0;
  margin-left: -10px;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
[dir="rtl"] #notification_area {
  float: left !important;
  float: left;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] .indicator_area {
  float: left !important;
  float: left;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
[dir="rtl"] #kernel_indicator {
  float: left !important;
  float: left;
  border-left: 0;
  border-right: 1px solid;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] #modal_indicator {
  float: left !important;
  float: left;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  height: 30px;
  margin-top: 4px;
  display: flex;
  justify-content: flex-start;
  align-items: baseline;
  width: 50%;
  flex: 1;
}
span.save_widget span.filename {
  height: 100%;
  line-height: 1em;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  text-overflow: ellipsis;
  overflow: hidden;
  white-space: nowrap;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
[dir="rtl"] span.save_widget.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] span.save_widget span.filename {
  margin-left: 0;
  margin-right: 16px;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
  white-space: nowrap;
  padding: 0 5px;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
    padding: 0 0 0 5px;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
.toolbar-btn-label {
  margin-left: 6px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
[dir="rtl"] .btn-group > .btn,
.btn-group-vertical > .btn {
  float: right;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
[dir="rtl"] ul.typeahead-list i {
  margin-left: 0;
  margin-right: -10px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
ul.typeahead-list  > li > a.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .typeahead-list {
  text-align: right;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  min-width: 20px;
  color: transparent;
}
[dir="rtl"] .no-shortcut.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .command-shortcut.pull-right {
  float: left !important;
  float: left;
}
.command-shortcut:before {
  content: "(command mode)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
[dir="rtl"] .edit-shortcut.pull-right {
  float: left !important;
  float: left;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
[dir="ltr"] #find-and-replace .input-group-btn + .form-control {
  border-left: none;
}
[dir="rtl"] #find-and-replace .input-group-btn + .form-control {
  border-right: none;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>
<style type="text/css">
    
/* Temporary definitions which will become obsolete with Notebook release 5.0 */
.ansi-black-fg { color: #3E424D; }
.ansi-black-bg { background-color: #3E424D; }
.ansi-black-intense-fg { color: #282C36; }
.ansi-black-intense-bg { background-color: #282C36; }
.ansi-red-fg { color: #E75C58; }
.ansi-red-bg { background-color: #E75C58; }
.ansi-red-intense-fg { color: #B22B31; }
.ansi-red-intense-bg { background-color: #B22B31; }
.ansi-green-fg { color: #00A250; }
.ansi-green-bg { background-color: #00A250; }
.ansi-green-intense-fg { color: #007427; }
.ansi-green-intense-bg { background-color: #007427; }
.ansi-yellow-fg { color: #DDB62B; }
.ansi-yellow-bg { background-color: #DDB62B; }
.ansi-yellow-intense-fg { color: #B27D12; }
.ansi-yellow-intense-bg { background-color: #B27D12; }
.ansi-blue-fg { color: #208FFB; }
.ansi-blue-bg { background-color: #208FFB; }
.ansi-blue-intense-fg { color: #0065CA; }
.ansi-blue-intense-bg { background-color: #0065CA; }
.ansi-magenta-fg { color: #D160C4; }
.ansi-magenta-bg { background-color: #D160C4; }
.ansi-magenta-intense-fg { color: #A03196; }
.ansi-magenta-intense-bg { background-color: #A03196; }
.ansi-cyan-fg { color: #60C6C8; }
.ansi-cyan-bg { background-color: #60C6C8; }
.ansi-cyan-intense-fg { color: #258F8F; }
.ansi-cyan-intense-bg { background-color: #258F8F; }
.ansi-white-fg { color: #C5C1B4; }
.ansi-white-bg { background-color: #C5C1B4; }
.ansi-white-intense-fg { color: #A1A6B2; }
.ansi-white-intense-bg { background-color: #A1A6B2; }

.ansi-bold { font-weight: bold; }

    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="&#30011;&#22270;&#22522;&#30784;">&#30011;&#22270;&#22522;&#30784;<a class="anchor-link" href="#&#30011;&#22270;&#22522;&#30784;">&#182;</a></h2><p>画图参考 <a href="http://matplotlib.org/">matplotlib</a></p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">matplotlib</span> <span class="k">as</span> <span class="nn">mpl</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="c1">#import warnings; warnings.simplefilter(&#39;ignore&#39;)</span>
<span class="c1"># import seaborn as sns; sns.set()</span>
<span class="o">%</span><span class="k">matplotlib</span> inline
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="One-Dimensional-Data-Set">One-Dimensional Data Set<a class="anchor-link" href="#One-Dimensional-Data-Set">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>随机数</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[2]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">seed</span><span class="p">(</span><span class="mi">1000</span><span class="p">)</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">standard_normal</span><span class="p">(</span><span class="mi">20</span><span class="p">)</span> 
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>画图</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">x</span> <span class="o">=</span> <span class="nb">range</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">y</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">,</span> <span class="n">y</span><span class="p">)</span>
<span class="c1"># tag: matplotlib_0</span>
<span class="c1"># title: Plot given x- and y-values</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[3]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[&lt;matplotlib.lines.Line2D at 0x174f30e0b38&gt;]</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>增加网格，让坐标紧凑</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="o">.</span><span class="n">cumsum</span><span class="p">())</span>
<span class="n">plt</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>  <span class="c1"># adds a grid</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axis</span><span class="p">(</span><span class="s1">&#39;tight&#39;</span><span class="p">)</span>  <span class="c1"># adjusts the axis ranges</span>
<span class="c1"># tag: matplotlib_3_a</span>
<span class="c1"># title: Plot with grid and tight axes</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[4]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(-0.9500000000000001, 19.95, -2.322818663749045, 0.5655085808655865)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAYAAAAD8CAYAAAB+UHOxAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADl0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDIuMi4zLCBodHRwOi8vbWF0cGxvdGxpYi5vcmcvIxREBQAAIABJREFUeJzt3Xl81PWd+PHXZyZ3MrkvEhISSCCcBkEUEJXigdiKWq9ut9VWiz1ce7rq+mu31263teu2a7XWWreua0VtFa2CyKkiioCcISEJ4QpJJgk5J3cyn98fM8EYckwyx3cm834+Hnkwx2fm++abZN75fo73R2mtEUIIEXxMRgcghBDCGJIAhBAiSEkCEEKIICUJQAghgpQkACGECFKSAIQQIkhJAhBCiCAlCUAIIYKUJAAhhAhSIUYHMJLk5GSdk5Mzrte2tbURHR3t2YA8SOJzj8TnHonPPf4c3969e+u11ikuNdZa++3XggUL9Hht27Zt3K/1BYnPPRKfeyQ+9/hzfMAe7eJnrEe6gJRSK5VSR5VS5UqpB4d4/k6lVJ1Sar/z625PHFcIIcT4ud0FpJQyA48DVwGVwG6l1Ota6yODmr6otb7X3eMJIYTwDE9cASwCyrXWFVrrbmAtsNoD7yuEEMKLlHazHLRS6mZgpdb6buf9LwEXD/xrXyl1J/ALoA4oBb6rtT49zPutAdYApKWlLVi7du244rLZbMTExIzrtb4g8blH4nOPxOcef45v+fLle7XWC11q7OpgwXBfwC3A0wPufwl4bFCbJCDcefvrwFZX3lsGgY0j8blH4nOPxDd++HgQuBLIGnB/MlA1KMmc1Vp3Oe/+EVjggeMKIYRwgycSwG4gXymVq5QKA24HXh/YQCk1acDd64FiDxxXCCGEG9yeBaS17lVK3QtsBMzAM1rrIqXUT3FcirwO3KeUuh7oBRqAO909rhD+as+JBo419XGF0YEIMQqPrATWWq8H1g967EcDbj8EPOSJYwnhz7TW/NML+1B9Xdx1g9HRCDEyqQUkhAcdrGymurmTKpumtqXT6HCEGJEkACE8aGNRzbnbO4+dNTASIUYnCUAID9Fa89bhGhZPTSI6FHaU1xsdkhAjkgQghIeU19qoqG9j1dx0Ziaa2Vle378ORgi/JAlACA/p7/65alY6s5LMVDV3cry+zeCohBieJAAhPOStohrmZ8eTHhfB7CQzAO9LN5DwY5IAhPCA0w3tHD7TwsrZ6QCkRiky4yN5v1wGgoX/kgQghAe8fcQKwDXOBKCUYmleEjuP1dNnl3EA4Z8kAQjhARsP11CQbiEn+ZNtApfmJdPS2UtRVbOBkQkxPEkAQriprrWL3Scbzv3132/JtGRApoMK/yUJQAg3bS62ojXnJYAUSzgF6RZ2yjiA8FOSAIRw01uHa8hOjGLmJMt5zy2ZlsxHJxro7OkzIDIhRiYJQAg3tHT2sPNYPSvnpKOUOu/5S/OT6O61s/dkowHRCTEySQBiwqlr7aK5vccnx9pWUktPn+aa2WlDPr8oN4kQk5L1AMIvSQIQ5/nTjuNsON5DW1ev0aGMmdaaL/zxQ+56drdPjvfW4RpSLOHMz0oY8vmY8BAKs+IlAQi/JAlAfMr+00387I0jvHi0m8t+tY2n3j1GR3fg9F/vP91Eea2NPScb2XOiwavH6uzpY/vROq6ZnYbJdH73T78leckcOtPss6sSIVwlCUCco7XmF+uLSYoO4/6FEczKiOXf15ew7Fdbefq9ioAYyHxtfxVhISbio0L5w7sVXj3Wu6V1dPT0nTf7Z7BL85Kxa/igQmYDCf8iCUCcs7Wkll3HG/jOlfnMTjbz3F0X89evL2ZGuoWfv1nMsl9t45kdx/02EfT02fn7gSqunJnKly+ZwqYjVsprbV473ltFNcRGhHDJ1KQR2xVmxRMVZmbnMekGEv5FEoAAoLfPzn9sKCE3OZrbF2Wfe3xhTiLP330JL92zmLyUGH76xhEu+9U2nt15wu8SwY7yes62dXNDYSZfXpJDeIiJp9/zzlVAT5+dLcW1XDkzjVDzyL9GYSEmFuUmyoIw4XckAQgA/vZxJWW1Nh5YOWPID7RFuYm8sOYSXvjaJeQkR/OvrxdxxSPbee6DE3T1+kciWLfvDHGRoVwxI5XkmHBuXjCZVz4+Q22r57dm3FXRQHNHD9fMGbn7p9+leclU1LVR3dzh8ViEGC9JAIL27l4e3VTKhdnxo/ZnL56WxItrLuEvd19MVmIkP3ytiOWPbOf/PjxJd6/dRxGfr62rl7eLrFw3bxJhIY4f67uXTaXHbufZnSc8fry3iqqJDDVzWX6KS+37y0JIdVDhTyQB+BmtNTc98T4/e+OIz475zI7jWFu6+JdVM4dczDSYUoolecm8dM9inrtrEelxEfy/dYdZ/uvtvPDRKXr6fJ8I3j5SQ0dPHzcUZp57LDc5mmtmpfPcByexeXBKq92uebvIyuXTU4gMM7v0moJ0C0nRYTIdVPgVSQB+pqiqhY9PNfGnHcfZ5Cwx7E31ti6efKeCq2elsTAncUyvVUqxLD+Fv31jCc9+dREplnAeeuUQy3+93ecfdOv2VZEZH8nCKZ+ej7/m8qm0dPby4u7THjvWvtNN1LZ2sdLF7h8Ak0mxeFoS78s2kcKPSALwM+sPVWM2KWakWXjgbwe90n890GNbyujo6eOfVxaM+z2UUlw+PYVXv7mE/7nzIswmxYOvHPRZHfy61i7eK6tjdWHGefPxL8xOYFFOIs/sOO6xK5O3i2oINSuWF6SO6XWX5iVT29rl1ZlJQoyFJAA/orVm/aFqFk9N4vEvzqetq5f7Xz7otb8Yj9e38fyuU9x+URZ5qTFuv59Sjg/Fh64t4HRDB5uO1HggytG9cbAKu4Yb52cO+fyay6ZypqmD9Yeq3T6W1pq3impYPC2ZuMjQMb12aV7/OIB0Awn/IAnAjxRXt3LibDur5k4iL9XC/7tuJu+U1vG/H5z0yvF+vfEoYSEmvn1lvkff96pZ6WQlRvL0e8c9+r7DWbfvDLMzYslPO78aJ8BnClKZlhLNH96pcDuZltS0cvJs+7mtH8ciKzGK7MQodshAsPATkgD8yIbD1ZgUXO0sLPaPl0zhMwWp/Nv6YkqtrR491r5Tjbx5qJo1l00l1RLh0fc2mxRfWZLLnpON7D/d5NH3HqyizsaByuZPDf4OZjIp1lw2lSPVLW7Pxd9YVINScNWsoYu/jWZpXjK7Ks7Sa8BAuRCDSQLwE1pr3jxUzSVTk0iOCQccXSq//Pw8LOEh3PfCPo/Nt3eUfCghOSacry2b6pH3HOzWi7KwhIfwpx3evQpYt78KpeD6wowR290wP5MUSzhPuVke4q3DNSyckkCKJXxcr1+al0RrVy8Hz8g2kcJ4HkkASqmVSqmjSqlypdSDQzwfrpR60fn8LqVUjieOO5EctbZSUdfGtXMnferxFEs4v7p5HiU1rfx641GPHGtzcS0fnWjgu1flEx0e4pH3HCwmPITbF2Wx/lA1VU3eWfyktWbdvjMsmZZEWuzIVzHhIWa+sjSH98rqx71H78mzbZTUtI66VmIk59YDlMk4gDCe2wlAKWUGHgeuBWYBX1BKzRrU7C6gUWudB/wX8Et3jzvRrD/k6FoYqm95xcw0/vGSbP743nG3BxAdJR+KmZoSzW0Ls9x6r9HcsSQHwCsLscAxHfNUQ/uI3T8DffHiKUSHmfnjOK8CNhY5BrXdSQCJ0WHMmhTL+1IXSPgBT1wBLALKtdYVWutuYC2welCb1cCzztt/BVYoV1YcBZH1h6pZlJM4bNfCw6tmMS0lmu+/dICm9u5xH+elPZUcq2vjgZUFhIxSw8ZdkxOiWDknnb98dMorewus23eG8BCTy/Px4yJDuX1RNn8/WE1lY/uYj/fW4RpmZ8SSlRg15tcOdGl+Mh+fbAqoMttiYvLEJ0AmMHCVTaXzsSHbaK17gWZg5BKKQaTM2kp5rY3r5k0atk1kmJnf3j6fs21d/Murh8Y1m6W9u5f/2lzKwikJXD3OQcyxuvvSXFo7e3l5j+cWYgH02jVvHKzmyllpWCJcn4751UtzUcAzO06M6XjWlk4+PtU0rtk/gy3NS6a7z85uL+9XIMRoPNEBPNRf8oM/nVxp42io1BpgDUBaWhrbt28fV1A2m23cr/WFgfGtK+9GAbHNFWzffmLE190wLYSXD9Xw8+c3s2zy2Oahv1beTV1rD/fMUrzzzjsux+euvHgTT2wpJrv7BCYPXfjtqWyjoU2RF9Iw5jgvSjfx/IfHWRBhJTrUtXi2nnJs5pLYfprt28+M2n6k89fVqzEreGHbPuxVYS7H7UmB9Pvhj/w9Ppdprd36AhYDGwfcfwh4aFCbjcBi5+0QoB5Qo733ggUL9Hht27Zt3K/1hYHxXf3oO/qW3+906XW9fXZ92x926lk/3KBP1NtcPl5tS6ee9cMN+uvP7RlzfO5682CVnvLAG/qtw9Uee8/bfrNBX/CTjbqrp2/Mry0606ynPPCG/t3WMpdf88U/fqiXP7JN2+12l9qPdv5ufXKnXvXbd10+vqcF0u+HP/Ln+IA92sXPb090Ae0G8pVSuUqpMOB24PVBbV4H7nDevhnY6gw06JXX2jhqbeXaua51LZhNikdvLcRsUnznxf0uzyf/7y1ldPXauf+aGe6EOy5Xz0ojMz7SY1NCbV29fGzt47q5n1T+HItZGbEsy0/mzy7uadDU3s2HFWe5Zk66S8XyXLE0L5kj1S00tI1/PEcId7mdALSjT/9eHH/lFwMvaa2LlFI/VUpd72z2JyBJKVUOfA84b6posNrgLE9w7Zzh+/8Hy4iP5N9unMu+U008trV81PbH6mz85aNT/MPF2UxNcb/kw1iFmE18ZWkOHx1v4FCl+/Pf3y6qods+fOkHV3z98mnUtXaxbt/o3TlbimvptWu3Zv8MtjQvGa3hg2OyKlgYxyPTQLTW67XW07XW07TW/+Z87Eda69edtzu11rdorfO01ou01t7drDWAvHmomoVTEkiPG9tq3M9dkMFN8zN5bGsZe082jtj2kbeOEhFi4r4Vni35MBa3XZRFTHgIf9rh/rf+1X1nSI5ULBhU+XMslkxLYnZGLE+9V4F9lKJ1bxXVMCkugnmZceM+3mAXTI4jJjxEpoMKQ8lKYANV1NkoqWk9b/GXq36yejYZ8ZF898X9w9a733uygbeKarjn8mnnVhgbwRIRym0XZfHGwWpqmsdf4bS2tZP3y+tZPCnEre4YpRzlISrq2thSUjtsu/buXt4treOa2ennVRp1R4jZxCVTE6UwnDCUJAADbTjsWFh07Rjqyg9kiQjlN7cVUtnYzo9fLzrvea01/76+hBRLOHcvy3UrVk+4c0kOdq159oMT436Pvx+oxq5hcYb7E9iumzuJzPhInnr32LBt3jlaR1ev/Vx9Jk9ampfMybPtnG4Y+5oEITxBEoCB1h+qZn52PBnxkeN+j4U5iXxreR5/3Vt5Xrnjt49Y2Xuyke9dNZ2oMO+UfBiLrMQorpmdzl92naK9e3wLw9btO8OczFgyYtz/0Q0xm7h7WS67TzQO2432VlENCVGhLBrjZjmu6C8PvVO6gYRBJAEYpLbdTlFVC9eNs/tnoPtW5HNBVjwPvXLo3KbjPX12frmhhLzUGG5ZMNntY3jK3ctyae7o4W97K8f82vJaG4fOjFz5c6xuXZhFXGTokFcB3b12thbXctWsNK+sms5PjSHFEi7loYVhJAEYZHeN4y/gsWwrOJxQs4nf3FZIT5+d7790ALtd8+Lu01TUt/GgD0o+jMWF2QlckBXPM++fGHXwdbDX9p/BpOD6C0au/DkW0eEhfOmSKbx9xEpF3ad36tp5rJ7Wrl6Pzv4ZSCnF0mlJ7CyvH/O5EMIT/OeTIcjsrunjgqx4Jie4V1emX25yND/67Cx2HjvLb7eU8ZvNZSzKTWTFzLFtW+htSinuvjSX4/VtbB1h8HUwrTXr9p9haV4yqaNU/hyrO5bkEGo28fSgdQobi6xEh5nPddV4w9K8ZM62dXPUw/s9COEKSQAGOHW2nRMtdlZ54K//gW67KIurZ6Xx2y1l1Nu6+JdVMz22cMmTrp2TTkZcBE+PYUrox6caOd3QwWoPdv/0S7GE8/kLJ/PXvZXUtXYB0GfXbDpSw/KCVCJCzR4/Zj/ZJlIYSRKAATYcdgzWrvJA//9ASin+4/PzyIyP5Kb5mRRmxXv0/T0lxGzizqU5fFjRwGEXN0ZZt6+KiFAT13hhNg7A15bl0tNn538/OAHA3pON1Nu6vdb90y8jPpKpydGSAIQhJAEYYP2hanJjTW6XFR5KYnQYW75/Ob++5QKPv7cn3XZRNlFhZp5xoTxET5+dNw5WceXMsVX+HIupKTFcNTON5z48SXt3LxuLaggzm1he4P0utCV5Sew63kCPbBMpfEwSgI9VNrZzoLKZhene61aICDV7dNGSN8RFhnLrwiz+frAKa8vIC8PeLa2jsb3HrdIPrrjn8qk0tffw4u7TvHW4hkvzk4nx0o5pA12al0x7d5/X908WYjBJAD624ZBj8ddF6cbPyzfaV5bm0GvX57pdhvPqvjMkRIVy2fQUr8azYEoiC6ck8OimUs40dXik9r8rFk9NRinYIdtETgjvldXx9HuBUe1GEoCPrT9czeyMWFKj5NRPSYrm6llpPL/r1LC7Y7V29rDpiJXPzssg1AfTWddcNpXWzl5MCq700aY5cVGhzM2MkwVhE8T/vH+CX75V4lKlWaPJp5APVTV1sO9Uk8cHfwPZXZc6ul3+9vHQC8M2Flnp6rVzg5e7f/pdOTON6WkxLM1LJjHad5u1LM1LZt+pJq9snSl8q9TaSk+f5kh1i9GhjEoSgA/11/6RBPCJi3ISmDc5jmfePz7kYqh1+86QnRjFhdm+mdFkMileumcxj3/xQp8cr9/Sacn02jUfHZdtIgNZe3cvlY2O1fj7T/n/mI4kAB9af6iamZNiyU2ONjoUv6GU4q5Lc6moa2N76acXhllbOtl5rJ4bCjN8up4hPiqMWC/NNhrOwpwEwkJM7JDpoAGtvPaT1eSBMKgvCcBHapo72Xuy0eOLvyaCVXMnkR4bcd6OYX8/UIVdw2ofdf8YKSLUzMIpCbIeIMCVWh0JYEaahX2nR96nwx9IAvCRc4u/5kn3z2ChZhN3LMnh/fKzHKn6pN903f4zzJscxzQDdjEzwtK8ZEpqWs+tRhaBp8zaSpjZxOr5GZxu6OCszb+/l5IAfGTDoRpmpFmC5sNsrP5hUTaRoWaeed9xFVBe28rhMy1eKf3gry6V8tABr9TaytSUaBZkO3ar8/duIEkAPlDb0snukw0y+DuCuKhQblk4mdf3V1Hb2sm6fVWYFHzuguA5Z3My44iNCGGnlIcOWKVWG/lpFuZOjsNsUpIAhGNTEa3hunnS/z+SryzNpcdu57kPTn5S+dPi2cqf/sxsUiyelsSO8nq0lvLQgaatq5czTR1MT40hKiyEGWkWSQAC3jxYTX5qDHmpFqND8Wu5ydGsKEjjD+9UUNnY4fXSD/5oaV4yZ5o6OCXbRAac/hlA+WmO3/PC7Hj2n2ry670eJAF4WW1rJx+dkO4fV929LJfuPjsRoSau9lEpBn/SXx5apoMGnlLnng7T0xzjfIVZ8bR29VJRbxvpZYaSBOBlG4usaC2Lv1x1cW4iF+cm8vkLJ/ukEJu/mZocTXpshIwDBKCyWhthISamJDnW+cx3lmPf58cLwoLvN8zH1h+sZlpK9Lm/CsTIlFK8eM9io8MwjFKKBTkJHKz03w8NMbRSayvTUmIwOyvxTkuJwRIewv7TTdyyMMvg6IYmVwBeVG/rYtfxs6yaO8kvd+YS/mlmuoXTDR3YpC5QQCmz2shP/eQPPZNJcUFWvF8PBEsC8KKNRTXYpftHjNGM9FgAjtbIPsGB4twMoEFX+oVZ8ZTUtA5b7dZokgC8aMOhGnKToylIl9k/wnX9Py8lNf5fTVI4lA2aAdSvMCuePrvmkItbn/qaJAAvaWjr5oOKs6yamy7dP2JMJidEEhMeIlcAAeSTGUCDEoCziu1+P60LJAnAS94uqqHPrrl2jnT/iLFRSjEj3UJJtSSAQFFmbSU8xET2oH2+k2PCmZwQ6bfjAG4lAKVUolJqk1KqzPlvwjDt+pRS+51fr7tzzEDx5qFqpiRFMTsj1uhQRACakW6hpKZFVgQHiFKr7VMzgAaan53gt3sDuHsF8CCwRWudD2xx3h9Kh9a60Pl1vZvH9LodZfW8fqCKvScbsbZ0jnklX2NbNzuPyewfMX4z0y20dPZS3dxpdCjCBeW1NvKHmepdmBVPVXMn1hb/+166uw5gNXCF8/azwHbgATff01D7TjXy5Wd2MfAzP9SsmBQXSWZ8JBnxkWQmRDJ5wO1JcRFEhJrPtd90xEqfXbNKun/EOA2cCZQRH2lwNGIkNucMoH9Iyx7y+cIBC8JW+tl+IO4mgDStdTWA1rpaKZU6TLsIpdQeoBf4D631OjeP6xWdPX3c/9eDpMVG8NSXFlJv66KyqYMzjR1UNXVwpqmD98vrsbZ2MvjKPDkmnMyESDLjIyipaSUrMZI5mdL9I8ZnhnMmUHFNC8sLhvu1Ev6gzDkAPHANwECzM2IJNTsqg/pbAlCj9TEqpTYDQ0X9MPCs1jp+QNtGrfV54wBKqQytdZVSaiqwFVihtT42zPHWAGsA0tLSFqxdu9bl/8xANpuNmJixrb59+Wg3bx7v4fsLwpmbMnxu7LVrGjs19R2ahk479R2as52asx12znZoGro0108L5bNTh99UfDzx+ZLE5x5PxPe97e1MTzDx9Qs8XxE1GM6fNw2M793KHp453M0vl0WSFj10r/pPdnYQHgIPLvL+1dzy5cv3aq0XutRYaz3uL+AoMMl5exJw1IXX/Bm42ZX3X7BggR6vbdu2jan9/lONOvfBN/T9L+8f9zHHYqzx+ZrE5x5PxPeV//lIX/3oO+4HM4RgOH/eNDC+n/29SE9/eL3u7bMP2/5H6w7pmT/cMGIbTwH2aBc/w90dBH4duMN5+w7gtcENlFIJSqlw5+1kYClwxM3jelRXbx/3//UAqZYIHr5ultHhCAE4FoQdq7PR3Ws3OhQxgtJaG3mpQ88A6leYHU97d9+59QL+wt0E8B/AVUqpMuAq532UUguVUk8728wE9iilDgDbcIwB+FUCeGxLOaVWG7+4aS5xkaFGhyME4BgH6LVrjtX5bzlhAeXW1mH7//sVZvnnFpFuDQJrrc8CK4Z4fA9wt/P2TmCuO8fxpkOVzfz+nWN8/sLJMtgm/MrMSY5JBCU1LeduC//S2tlDVXPneSUgBstJiiI+KpT9p5r4wqKhZwsZIahXAnf32rn/rwdIig7jR5+Vrh/hX3KTowk1K0qkJITf6q8BNLgExGBKKQr9sDJoUCeA320rp6SmlX+/cS5xUdL1I/xLqNlEXqqUhPBnZYN2ARtJYVY8pbWtflXmO2gTwOEzzTyxrZyb5mdy5aw0o8MRYkgF6RYpCufHSq02IkJNZCVEjdq2MCsereGgH10FBGUCcHT9HCQhOowffU66foT/Kki3UNPSSVN7t9GhiCGUWlvJS43BNMIMoH7nVgRLAjDWE9vLKa5u4d9umEN81PCLtYQw2oxzewPIVYA/Kq+1kZ/q2n4f8VFh5CZH+9U4QNAlgCNVLfxuazmrCzO4erZ/LcsWYrBzM4GqZXMYf9PS2UN1c+ewReCGMt85EKz9pMprUCWAnj7HrJ/4qFB+/LnZRocjxKhSLeHER4Vy1M8WEAnHHsAA0128AgDHgrC61i6q/KTKa1AlgCe3H6OoqoWf3zCHhGjp+hH+TylFQbqFYpkJ5HfKhtkFbCSfVAb1jx3CgiYBlNS08N9by/jsvEmslDLNIoAUpMdSam0d874Uwrv6ZwBNTnC9wFtBeixhISa/2SAmKBJAb5+d+18+SGxEKD+5Xrp+RGApSLfQ3t3H6cZ2o0MRA5TVuj4DqF9YiIk5GbF+MxAcFAngD+9WcOhMMz9dPYekmHCjwxFiTAqcA8HSDeRfyqy2MfX/95ufncChM8309Blf5G/CJ4BSayu/3VzGqrnpXDdPun5E4JmeFoNSyIIwP9LWo6lpGb0G0FAKs+Lp6rX7xfdzQieA3j7Hgq/ocDM/XT3H6HCEGJeosBCmJEZRUiNTQf1Flc3x17srJSAG86eB4AmdAJ7ecZwDp5v46eo5JEvXjwhgM6QkhF85cy4BjP0KYHJCJMkxYX6xInjCJoAqm51HN5Vyzew0PitdPyLAFaTHcvxsGx3dfUaHInAkgMhQM5nxY9/i0Z8qg07IBNBn1/zpUBdRYWZ+dsMclHJ9lF4If1SQbkFrx8wTYbwqm33MM4AGmp+dQEVdG83tPR6ObGwmZAJ4ZsdxjjXb+cn1s0m1eH5DbSF8reBcSQhJAP7gjE2PqQTEYP3jAAcqjb0KmHAJoLm9h//aXMr8VDPXX5BhdDhCeER2YhQRoSYpCucHmjt6aOrS4+r/7zdvchxKwT6DF4S5tSWkP4qLCuX5uy/m5JF90vUjJgyzSTEjzSIzgfzAWDaBGY4lIpS8lBj2nzZ2JtCEuwIAR/9afMSE/K+JIFaQHktJTavfVJIMVqXOInCuloEeTqEfVAaVT0khAsSMdAsNbd3U2bqMDiWolVpbCTczrhlAA83PTqCxvYdTDcaV+JAEIESAKJjk3BxGBoINVVbbSka0adwzgPr1DwQbOR1UEoAQAaIg3TETSBaEGavMaiMjxv2PzulpMUSGmg0dCJYEIESASIwOI9USTrEMBBumub2H2tYuMi3uTzAJMZuYOznO0BXBkgCECCBSEsJYpc6FeJkeuAIAxxaRxVUtdPUas8JbEoAQAWTmpFjKam30+kEp4WBUavVwAsiOp7vPzpEqY67qJAEIEUBmpFno7rVz4myb0aEEpTKrjegwM0kRnlljVJiVABg3ECwJQIgA0j8TSDaHMUap1bELmKcWmabHRZAeGyEJQAgxurzUGMwmJeMABimrtY1rE5iRFGbFGzYTyK0EoJS6RSlVpJSyK6UWjtBupVLqqFKqXCn1oDvHFCIKg5TDAAAWUklEQVSYhYeYmZocLSUhDNDU3k1da5dbJSCGUpgdz6mGds4asMDP3SuAw8BNwLvDNVBKmYHHgWuBWcAXlFKz3DyuEEGrYFKsFIUzwLkSEB6+AphvYGVQtxKA1rpYa310lGaLgHKtdYXWuhtYC6x257hCBLOCdAuVjR20dBpbSz7YlJ4rAufZBDB3chxmk2K/Ad1AvqgGmgmcHnC/Erh4uMZKqTXAGoC0tDS2b98+roPabLZxv9YXJD73BHN8PXW9ALy44V3yE8zjeo9gPn/jte1IFxFmKN33IW1tbR6NLyNasfXAcS4Mq/bYe7pi1ASglNoMpA/x1MNa69dcOMZQw+XDlr/TWj8FPAWwcOFCfcUVV7hwiPNt376d8b7WFyQ+9wRzfHmN7fzm421ETsrjikumjOs9gvn8jdcfSj9kRkYfy5cv9Xh8lzYc4o2DVVx22eVu1xgai1ETgNb6SjePUQlkDbg/Gahy8z2FCFqZ8ZFYwkNkINjHymptLJ+R4pX3np8dzwsfnaKivo28VM8OMo/EF9NAdwP5SqlcpVQYcDvwug+OK8SEpJSSkhA+1tjWTb2ty+P9//3mG1QZ1N1poDcqpSqBxcCbSqmNzsczlFLrAbTWvcC9wEagGHhJa13kXthCBLeCSRbZHMaH+geA3dkHeCTTUmKwhIf4fIcwtwaBtdavAq8O8XgVsGrA/fXAeneOJYT4xIz0WFo7T1HV3On2xiRidKW1jimg3roCMJkU87LiAusKQAhhjJnp/ZvDyDiAL5RZW4kJD2FSXITXjlGYFU9xdSsd3b6rDCoJQIgANL0/Acg4gE94ugbQUOZnJdBn1xyuavbaMQaTBCBEAIqNCCUzPlISgI+U19o8XgJisMJs50CwDxeESQIQIkDNnGThqEwF9bqGtm7qbd1e6//vlxwTzuSESJ+OA0gCECJAzUi3cKyuzbDdpILFJzOAvJsAwDEOIAlACDGqgvRY+uyacucMFeEdZedqAHl/gVZhVjxnmjqoben0+rFAEoAQAavAORAsC8K8q9RqwxIeQnqs92YA9Zuf7dghzFcbxUsCECJA5SZHE2Y2yUCwl5VaW8lL8+4MoH6zM2IJNSufdQNJAhAiQIWYTeSlxkgC8LLyWhvTU73f/w8QEWpm5qRYn80EkgQgRAArmGSRxWBedNbWxdm2bq+VgBhKYVY8RVXN2O3eL/MhCUCIAFaQbqG2tYuGtm6jQ5mQ+ncB8/YU0IG+vSKfD/9lhU/KQksCECKAFaTHAkhpaC8pq/XOLmAjSYoJJyrMF3t1SQIQIqAVTJKZQN5Uam3FEh5CWmy40aF4hSQAIQJYSkw4idFhlFRLAvCGUquNfB/NADKCJAAhAphSioJ0CyVWSQDe4KgB5LvuH1+TBCBEgJuRbqG0ppU+H8waCSb1Nsfgui9KQBhFEoAQAW5meiwdPX2camg3OpQJpdSHJSCMIglAiAA341xJCJkJ5EllBkwB9TVJAEIEuOlpFpSCYhkI9qhSayuWiBBSLRNzBhBIAhAi4EWGmclJipapoB5WZrU5k+vEnAEEkgCEmBAK0i2yGMyDtNaU1rZO6P5/kAQgxIQwI93CyYZ22rt7jQ5lQqi3ddPU3kO+j4rAGUUSgBATQEF6LFp/UrtGuOeTTWAkAQgh/NzMSTITyJOCYQooSAIQYkLISogiKswsM4E8pLTWRmxECCkTeAYQSAIQYkIwmRTT0ywyE8hDyqytE34GEEgCEGLC6J8JpLWUhHCH1tpZBG5i9/+DJAAhJoyCdAuN7T3UtnYZHUpAq7N10dzRM+H7/8HNBKCUukUpVaSUsiulFo7Q7oRS6pBSar9Sao87xxRCDG3Guc1hpBvIHcFQAqKfu1cAh4GbgHddaLtca12otR42UQghxq/AWRNI9gh2T/8MIF/uA2wUt/Yd01oXAxN+oESIQJAQHUZabLgMBLvpaE0rcZGhpMRM7BlA4LsxAA28rZTaq5Ra46NjChF0CtJjKZYEMG5aa94trWNRbmJQ/GGrRpsxoJTaDKQP8dTDWuvXnG22Az/QWg/Zv6+UytBaVymlUoFNwD9prYfsNnImiDUAaWlpC9auXevq/+VTbDYbMTH+ewkn8blH4hvaS0e7eftED09eFUWIafgPMDl/QzvV0sePdnbylTlhXD45dNh2/nz+li9fvtflrnattdtfwHZgoYttf4wjWYzadsGCBXq8tm3bNu7X+oLE5x6Jb2ivfHxaT3ngDX20pmXEdnL+hvbfm0v1lAfe0NaWjhHb+fP5A/ZoFz+7vd4FpJSKVkpZ+m8DV+MYPBZCeFiBzARyy+aSWgqz4km1RBgdik+4Ow30RqVUJbAYeFMptdH5eIZSar2zWRqwQyl1APgIeFNr/ZY7xxVCDG1aSgwhJiUzgcahtrWTA6ebuHJmqtGh+Iy7s4BeBV4d4vEqYJXzdgVwgTvHEUK4JizExLSUGIqqJAGM1dbiWgBWzEwzOBLfkZXAQkwwV8xI4b2yOsprpRtoLDYX15IZH3luPUUwkAQgxARzz+XTiAw1859vlxodSsDo7OljR3kdK2amBsX0z36SAISYYBKjw7h72VQ2HK7hYGWT0eEEhJ3H6unssXNlEHX/gCQAISaku5flEh8Vyq/lKsAlm4triQ4zc/HURKND8SlJAEJMQJaIUL55xTTeLa3jw4qzRofj17TWbCm2ctn0FMJDzEaH41OSAISYoL68OIe02HB+vfGo7BEwgsNnWrC2dAXV7J9+kgCEmKAiQs3ctyKfPScb2X60zuhw/NbmYitKwfIZKUaH4nOSAISYwG5dmEV2YhS/2ngUu12uAoaypcTKguwEkoKg+udgkgCEmMBCzSa+d9V0iqtbePNQtdHh+J3q5g4On2kJyu4fkAQgxIT3uQsymJFm4dFNpfT22Y0Ox69sca7+DabyDwNJAhBigjObFN+/ejrH69v428eVRofjV7YUW8lOjCIv1T9LO3ubJAAhgsBVs9IozIrnt5vL6OzpMzocv9De3cv7x84G3erfgSQBCBEElFL88zUzqGru5Pldp4wOxy/sKKunu9fOVUHa/w+SAIQIGkvyklmal8QT28rp6JUZQVuKa7FEhHBRbnCt/h1IEoAQQeQHV8/gbFs3m072GB2Koex2zZaSWi6fnkKoOXg/BoP3fy5EEJqfncBVs9LYcLyHpvZuo8MxzIHKJuptXUFX/G0wSQBCBJkfXD2Dzl548p0Ko0MxzJbiWswmxRVBuPp3IEkAQgSZGekWLskw8+edx6lt6TQ6HENsLraycEoC8VFhRodiKEkAQgShG/PC6O3TPLa13OhQfK6ysZ2Smtag7/4BSQBCBKXUKBO3XZTFCx+d4tTZdqPD8amtJf17/wbn6t+BJAEIEaT+6TP5mE2K32wJrk1jNh2xMjU5mqkpwbn6dyBJAEIEqfS4CO5YksOr+85Qag2ODeRtXb3sqmiQv/6dJAEIEcS+cfk0osNCeDRIto58r7SO7r7g2/t3OJIAhAhiCdFhfG3ZVN4qquHA6Ym/gfzm4lriIkNZMCXB6FD8giQAIYLcXctySYwO49dvHzU6FK/qs2u2Ha1l+YwUQoJ49e9AchaECHIx4SF884ppvFdWz85j9UaH4zX7TjXS0NYdtJu/DEUSgBCCf7xkCumxERN6A/nNxbWEmBSXB/nq34EkAQghzm0g//GppnPz5CeaLcVWLp6aSGxEqNGh+A1JAEIIAG5ZOJmcpCgemYAbyJ86205ZrY0VBdL9M5BbCUAp9YhSqkQpdVAp9apSKn6YdiuVUkeVUuVKqQfdOaYQwjtCzSa+e9V0Smpa+fvBKqPD8ajNxVYAmf45iLtXAJuAOVrreUAp8NDgBkopM/A4cC0wC/iCUmqWm8cVQnjB5+ZlUJBu4V9fL+Kj4w1Gh+MxW0qs5KfGkJ0UZXQofsWtBKC1fltr3eu8+yEweYhmi4ByrXWF1robWAusdue4QgjvMJkUf/jSAhKjwvjHp3fx2v4zRofktpbOHufqX/nrfzDlqRF/pdTfgRe11v836PGbgZVa67ud978EXKy1vneY91kDrAFIS0tbsHbt2nHFY7PZiInx31ofEp97JD73jBafrVvz2L5OjjbauTEvlOunhfp043RPnr9d1b38/kAXD18cQX6C2SPv6c/f3+XLl+/VWi90qbHWesQvYDNweIiv1QPaPAy8ijOhDHr9LcDTA+5/CXhstONqrVmwYIEer23bto37tb4g8blH4nOPK/F19fTp7764T0954A393bX7dGdPr/cDc/Lk+fv2Cx/r+T99W/f22T32nv78/QX2aBc+X7XWhLiQIK4c6Xml1B3AZ4EVzoMPVglkDbg/GZhYI0xCTEBhISb+85YLyEmK5tFNpVQ2dfDUlxYE1CYqvX12th2t48qZaZhNvruCCRTuzgJaCTwAXK+1Hq6o+G4gXymVq5QKA24HXnfnuEII31BKcd+KfH57eyH7TzVx4xM7OVHf5tVjNrR109zlma7pvScbae7o4Uqp/jkkd2cB/Q6wAJuUUvuVUk8CKKUylFLrAbRjkPheYCNQDLyktS5y87hCCB9aXZjJX752MU3t3dz4xPvsPuH5GUJVTR3862uHueQXW/j+9nYe31ZOT5/drffcXGwlzGxi2XRZ/TuUUbuARqK1zhvm8Spg1YD764H17hxLCGGshTmJvPrNpXz1z7v54h938cgt81hdmOn2+54828bvtx/jbx9XojV8/sLJVFRW8cjGo7x5sJpf3TyPOZlx43rvLcW1XDw1kZhwtz7qJiw5K0IIl+UkR/PKN5dwz3N7+fba/Zyob+e+FXnjmiFUXtvKE9uO8dqBKswmxRcWZXPP5dPIjI9k+/YGOpML+OFrh1n9+PusuWwq316RT0So67N4KupsVNS3cefSnDHHFiwkAQghxiQ+Kozn7rqYB185yH9tLuXk2TZ+8fm5hIe49uF8pKqFx7eVs/5wNREhZr66NIevLZtKamzEp9qtnJPO4qlJ/PzNI/x++zE2Hq7hlzfP46KcRJeOs6XYUdPoMwXS/z8cSQBCiDHrnyGUmxTNf7o4Q2j/6SZ+t7WMzcW1WMJD+NYVeXz1UsdeBMOJiwrlkVsu4PrCDB565RC3/uEDvnzJFO5fWTBqt87mYisF6RYmJ8jq3+FIAhBCjItSin9akU92UhT3v3yQG5/Yyf/ceRE5ydGfarer4iy/21bOe2X1xEeF8r2rpnPHkhziIl2vyrksP4WN37mMRzYe5dkPTrC5uJZf3DSXy4YZ3G1q72bPyUa+cfk0d/6LE55UAxVCuGWoGUJaa94rq+PWJz/gtqc+pLi6hYeuLWDHA5/hvhX5Y/rw7xcdHsKPr5/Ny/csJjzUxJef+YgfvHyApvbu89puP1pHn13L5u+jkCsAIYTbBs8Qyk+LoaiqhfTYCH78uVncvih7TAO4ox1r/X3LeGxrGU++U8H2o3X8bPVsrp076VybzcVWkmPCuWDykAWKhZNcAQghPKJ/htBFuQnYunr5xU1zeeefr+DOpbke+/DvFxFq5v5rCnjtW0tJtYTzjec/5hv/t5fa1k56+uy8U1rHioJUTLL6d0RyBSCE8Jj4qDD+766LfVY4bk5mHK/du5Sn3q3gt1vK2HnsLDfOz6S1s1e6f1wgVwBCCI/yZdVQcGxk863leay/bxn5qTH8eecJwkJMXJqf7NM4ApFcAQghJoS81Bheumcxa3efxqQgKkw+3kYjZ0gIMWGYTIp/uDjb6DAChnQBCSFEkJIEIIQQQUoSgBBCBClJAEIIEaQkAQghRJCSBCCEEEFKEoAQQgQpSQBCCBGklNba6BiGpZSqA06O8+XJQL0Hw/E0ic89Ep97JD73+HN8U7TWQ2+UMIhfJwB3KKX2aK0XGh3HcCQ+90h87pH43OPv8blKuoCEECJISQIQQoggNZETwFNGBzAKic89Ep97JD73+Ht8LpmwYwBCCCFGNpGvAIQQQowg4BOAUmqlUuqoUqpcKfXgEM+HK6VedD6/SymV48PYspRS25RSxUqpIqXUt4doc4VSqlkptd/59SNfxec8/gml1CHnsfcM8bxSSv238/wdVEpd6MPYZgw4L/uVUi1Kqe8MauPT86eUekYpVauUOjzgsUSl1CalVJnz34RhXnuHs02ZUuoOH8b3iFKqxPn9e1UpNeRO6aP9LHgxvh8rpc4M+B6uGua1I/6uezG+FwfEdkIptX+Y13r9/Hmc1jpgvwAzcAyYCoQBB4BZg9p8E3jSeft24EUfxjcJuNB52wKUDhHfFcAbBp7DE0DyCM+vAjYACrgE2GXg97oGxxxnw84fcBlwIXB4wGO/Ah503n4Q+OUQr0sEKpz/JjhvJ/govquBEOftXw4Vnys/C16M78fAD1z4/o/4u+6t+AY9/5/Aj4w6f57+CvQrgEVAuda6QmvdDawFVg9qsxp41nn7r8AK5aNNS7XW1Vrrj523W4FiINMXx/ag1cD/aocPgXil1CQD4lgBHNNaj3dhoEdord8FGgY9PPBn7FnghiFeeg2wSWvdoLVuBDYBK30Rn9b6ba11r/Puh8BkTx/XVcOcP1e48rvutpHic35u3Aq84OnjGiXQE0AmcHrA/UrO/4A918b5S9AMJPkkugGcXU/zgV1DPL1YKXVAKbVBKTXbp4GBBt5WSu1VSq0Z4nlXzrEv3M7wv3hGnj+ANK11NTiSPpA6RBt/OY9fxXFFN5TRfha86V5nF9Uzw3Sh+cP5WwZYtdZlwzxv5Pkbl0BPAEP9JT94WpMrbbxKKRUD/A34jta6ZdDTH+Po1rgAeAxY58vYgKVa6wuBa4FvKaUuG/S8P5y/MOB64OUhnjb6/LnKH87jw0Av8PwwTUb7WfCW3wPTgEKgGkc3y2CGnz/gC4z8179R52/cAj0BVAJZA+5PBqqGa6OUCgHiGN8l6LgopUJxfPg/r7V+ZfDzWusWrbXNeXs9EKqUSvZVfFrrKue/tcCrOC61B3LlHHvbtcDHWmvr4CeMPn9O1v5uMee/tUO0MfQ8OgedPwt8UTs7rAdz4WfBK7TWVq11n9baDvxxmOMaff5CgJuAF4drY9T5c0egJ4DdQL5SKtf5V+LtwOuD2rwO9M+4uBnYOtwvgKc5+wz/BBRrrR8dpk16/5iEUmoRju/JWR/FF62UsvTfxjFYeHhQs9eBLztnA10CNPd3d/jQsH95GXn+Bhj4M3YH8NoQbTYCVyulEpxdHFc7H/M6pdRK4AHgeq11+zBtXPlZ8FZ8A8eUbhzmuK78rnvTlUCJ1rpyqCeNPH9uMXoU2t0vHLNUSnHMEHjY+dhPcfywA0Tg6DooBz4CpvowtktxXKYeBPY7v1YBXwe+7mxzL1CEY1bDh8ASH8Y31XncA84Y+s/fwPgU8Ljz/B4CFvr4+xuF4wM9bsBjhp0/HImoGujB8VfpXTjGlLYAZc5/E51tFwJPD3jtV50/h+XAV3wYXzmO/vP+n8H+WXEZwPqRfhZ8FN9zzp+tgzg+1CcNjs95/7zfdV/E53z8z/0/cwPa+vz8efpLVgILIUSQCvQuICGEEOMkCUAIIYKUJAAhhAhSkgCEECJISQIQQoggJQlACCGClCQAIYQIUpIAhBAiSP1/qLa2zTVg2fMAAAAASUVORK5CYII=
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>修改坐标起始点</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="o">.</span><span class="n">cumsum</span><span class="p">())</span>
<span class="n">plt</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlim</span><span class="p">(</span><span class="o">-</span><span class="mi">1</span><span class="p">,</span> <span class="mi">20</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylim</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">min</span><span class="p">(</span><span class="n">y</span><span class="o">.</span><span class="n">cumsum</span><span class="p">())</span> <span class="o">-</span> <span class="mi">1</span><span class="p">,</span>
         <span class="n">np</span><span class="o">.</span><span class="n">max</span><span class="p">(</span><span class="n">y</span><span class="o">.</span><span class="n">cumsum</span><span class="p">())</span> <span class="o">+</span> <span class="mi">1</span><span class="p">)</span>
<span class="c1"># tag: matplotlib_3_b</span>
<span class="c1"># title: Plot with custom axes limits</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[5]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(-3.1915310617211072, 1.4342209788376488)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>设置图形大小，设置线点性状、颜色、宽度</li>
<li>设置图形横坐标，纵坐标标题</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">7</span><span class="p">,</span> <span class="mi">4</span><span class="p">))</span>
  <span class="c1"># the figsize parameter defines the</span>
  <span class="c1"># size of the figure in (width, height)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="o">.</span><span class="n">cumsum</span><span class="p">(),</span> <span class="s1">&#39;b&#39;</span><span class="p">,</span> <span class="n">lw</span><span class="o">=</span><span class="mf">1.5</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="o">.</span><span class="n">cumsum</span><span class="p">(),</span> <span class="s1">&#39;ro&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axis</span><span class="p">(</span><span class="s1">&#39;tight&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;value&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;A Simple Plot&#39;</span><span class="p">)</span>
<span class="c1"># tag: matplotlib_4</span>
<span class="c1"># title: Plot with typical labels</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[6]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0.5,1,&#39;A Simple Plot&#39;)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Two-Dimensional-Data-Set">Two-Dimensional Data Set<a class="anchor-link" href="#Two-Dimensional-Data-Set">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">seed</span><span class="p">(</span><span class="mi">2000</span><span class="p">)</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">standard_normal</span><span class="p">((</span><span class="mi">20</span><span class="p">,</span> <span class="mi">2</span><span class="p">))</span><span class="o">.</span><span class="n">cumsum</span><span class="p">(</span><span class="n">axis</span><span class="o">=</span><span class="mi">0</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">7</span><span class="p">,</span> <span class="mi">4</span><span class="p">))</span>
<span class="c1">#颜色自动匹配</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">,</span> <span class="n">lw</span><span class="o">=</span><span class="mf">1.5</span><span class="p">)</span>
  <span class="c1"># plots two lines</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">,</span> <span class="s1">&#39;ro&#39;</span><span class="p">)</span>
  <span class="c1"># plots two dotted lines</span>
<span class="n">plt</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axis</span><span class="p">(</span><span class="s1">&#39;tight&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;value&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;A Simple Plot&#39;</span><span class="p">)</span>
<span class="c1"># tag: matplotlib_5</span>
<span class="c1"># title: Plot with two data sets</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[8]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0.5,1,&#39;A Simple Plot&#39;)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>添加题注</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[9]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">7</span><span class="p">,</span> <span class="mi">4</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">[:,</span> <span class="mi">0</span><span class="p">],</span> <span class="n">lw</span><span class="o">=</span><span class="mf">1.5</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="s1">&#39;1st&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">[:,</span> <span class="mi">1</span><span class="p">],</span> <span class="n">lw</span><span class="o">=</span><span class="mf">1.5</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="s1">&#39;2nd&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">,</span> <span class="s1">&#39;ro&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">loc</span><span class="o">=</span><span class="mi">0</span><span class="p">)</span>
<span class="c1">#loc=0,best</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axis</span><span class="p">(</span><span class="s1">&#39;tight&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;value&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;A Simple Plot&#39;</span><span class="p">)</span>
<span class="c1"># tag: matplotlib_6</span>
<span class="c1"># title: Plot with labeled data sets</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[9]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0.5,1,&#39;A Simple Plot&#39;)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">y</span><span class="p">[:,</span> <span class="mi">0</span><span class="p">]</span> <span class="o">=</span> <span class="n">y</span><span class="p">[:,</span> <span class="mi">0</span><span class="p">]</span> <span class="o">*</span> <span class="mi">100</span>
<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">7</span><span class="p">,</span> <span class="mi">4</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">[:,</span> <span class="mi">0</span><span class="p">],</span> <span class="n">lw</span><span class="o">=</span><span class="mf">1.5</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="s1">&#39;1st&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">[:,</span> <span class="mi">1</span><span class="p">],</span> <span class="n">lw</span><span class="o">=</span><span class="mf">1.5</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="s1">&#39;2nd&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">,</span> <span class="s1">&#39;ro&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">loc</span><span class="o">=</span><span class="mi">0</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axis</span><span class="p">(</span><span class="s1">&#39;tight&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;value&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;A Simple Plot&#39;</span><span class="p">)</span>
<span class="c1"># tag: matplotlib_7</span>
<span class="c1"># title: Plot with two differently scaled data sets</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[10]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0.5,1,&#39;A Simple Plot&#39;)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[11]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="p">,</span> <span class="n">ax1</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">[:,</span> <span class="mi">0</span><span class="p">],</span> <span class="s1">&#39;b&#39;</span><span class="p">,</span> <span class="n">lw</span><span class="o">=</span><span class="mf">1.5</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="s1">&#39;1st&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">[:,</span> <span class="mi">0</span><span class="p">],</span> <span class="s1">&#39;ro&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">loc</span><span class="o">=</span><span class="mi">8</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axis</span><span class="p">(</span><span class="s1">&#39;tight&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;value 1st&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;A Simple Plot&#39;</span><span class="p">)</span>
<span class="n">ax2</span> <span class="o">=</span> <span class="n">ax1</span><span class="o">.</span><span class="n">twinx</span><span class="p">()</span>
<span class="c1">#共享横坐标，独立的纵坐标，坐标标在右边</span>

<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">[:,</span> <span class="mi">1</span><span class="p">],</span> <span class="s1">&#39;g&#39;</span><span class="p">,</span> <span class="n">lw</span><span class="o">=</span><span class="mf">1.5</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="s1">&#39;2nd&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">[:,</span> <span class="mi">1</span><span class="p">],</span> <span class="s1">&#39;ro&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">loc</span><span class="o">=</span><span class="mi">0</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;value 2nd&#39;</span><span class="p">)</span>
<span class="c1"># tag: matplotlib_8</span>
<span class="c1"># title: Plot with two data sets and two y-axes</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[11]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0,0.5,&#39;value 2nd&#39;)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[12]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">7</span><span class="p">,</span> <span class="mi">5</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">211</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">[:,</span> <span class="mi">0</span><span class="p">],</span> <span class="n">lw</span><span class="o">=</span><span class="mf">1.5</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="s1">&#39;1st&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">[:,</span> <span class="mi">0</span><span class="p">],</span> <span class="s1">&#39;ro&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">loc</span><span class="o">=</span><span class="mi">0</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axis</span><span class="p">(</span><span class="s1">&#39;tight&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;value&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;A Simple Plot&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">212</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">[:,</span> <span class="mi">1</span><span class="p">],</span> <span class="s1">&#39;g&#39;</span><span class="p">,</span> <span class="n">lw</span><span class="o">=</span><span class="mf">1.5</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="s1">&#39;2nd&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">[:,</span> <span class="mi">1</span><span class="p">],</span> <span class="s1">&#39;ro&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">loc</span><span class="o">=</span><span class="mi">0</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axis</span><span class="p">(</span><span class="s1">&#39;tight&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;value&#39;</span><span class="p">)</span>
<span class="c1"># tag: matplotlib_9</span>
<span class="c1"># title: Plot with two sub-plots</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[12]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0,0.5,&#39;value&#39;)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>plt.subplot()分割指定画图区域</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[13]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">9</span><span class="p">,</span> <span class="mi">4</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">221</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">[:,</span> <span class="mi">0</span><span class="p">],</span> <span class="n">lw</span><span class="o">=</span><span class="mf">1.5</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="s1">&#39;1st&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">[:,</span> <span class="mi">0</span><span class="p">],</span> <span class="s1">&#39;ro&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">loc</span><span class="o">=</span><span class="mi">0</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axis</span><span class="p">(</span><span class="s1">&#39;tight&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;value&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;1st Data Set&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">224</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">y</span><span class="p">)),</span> <span class="n">y</span><span class="p">[:,</span> <span class="mi">1</span><span class="p">],</span> <span class="n">width</span><span class="o">=</span><span class="mf">0.5</span><span class="p">,</span>
        <span class="n">color</span><span class="o">=</span><span class="s1">&#39;g&#39;</span><span class="p">,</span> <span class="n">label</span><span class="o">=</span><span class="s1">&#39;2nd&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">(</span><span class="n">loc</span><span class="o">=</span><span class="mi">0</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">axis</span><span class="p">(</span><span class="s1">&#39;tight&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;index&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;2nd Data Set&#39;</span><span class="p">)</span>
<span class="c1"># tag: matplotlib_10</span>
<span class="c1"># title: Plot combining line/point sub-plot with bar sub-plot</span>
<span class="c1"># size: 80</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[13]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0.5,1,&#39;2nd Data Set&#39;)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAjAAAAEWCAYAAAB47K3ZAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADl0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uIDIuMi4zLCBodHRwOi8vbWF0cGxvdGxpYi5vcmcvIxREBQAAIABJREFUeJzt3Xl8XFX9//HXJ2madEm3pHvaphvQltbu7JAiyqKIgP4Ey74UVFQE1Gr9Ksi3iAiCfkU2RRACuAGyyU6g7LSApdAFuqRN94UuaZpm+/z+mBsIbZaZNLPcyfv5eOQxM/eeO+dzOm3m03POPcfcHREREZEwyUh2ACIiIiKxUgIjIiIioaMERkREREJHCYyIiIiEjhIYERERCR0lMCIiIhI6SmBEREQkdJTAtENmdomZzTWz3WZ2VwzXrTCzY5o5X2RmdWZWHvyUmdnfzWxKDHVcaWb3Rlu+kes7mtkNQd3lZrbczG5MRN0iIpI4SmDapzXA/wJ3xuO93b0rkAscDCwC5pjZ5+NQV2N+AkwGpgYxTAPeSVDdIiKSIEpg2iF3f9DdHwY273nOzPLN7DEz22pmW8xsjpllmNk9wGDg0aBn40ct1OHuXubuPwf+BPy6QR2/M7NVZrbdzOaZ2RHB8eOAnwLfCOr4b3D8XDNbaGY7zGyZmV3UTNVTgIfcfU0Qwwp3/2uDugeY2b/MbGPQO/O95uoWEZHU1CHZAUjKuRwoA3oHrw8mko+cGSQaF7j7szG+54PAt82si7vvBN4CfglsA74P/MPMCt39STO7Bhjh7mc0uH4D8GVgGXAk8B8ze8vd326krteBy8ysCpgDLPBgvwwzywAeBf4NnA4UAM+a2eJm6hYRkRSkHhjZUzXQHxji7tXuPsf3fcOsNYABPQDc/V533+zuNe5+A5AN7N/Uxe7+uLsvDXpUXgSeBo5ooviviPT2TAfmAqvN7Ozg3BSgt7v/0t2r3H0ZcAdw2j62T0REEkwJjOzpN8BHwNPBcM3MNnjPgYADWwHM7PJgSGibmW0FugP5TV1sZseb2evBkNZW4ISmyrt7rbvf7O6HEUmYZgN3mtkoYAgwIBge2xq810+Bvm3QRhERSSAlMPIZ7r7D3S9392HAiUSGY+on4La2J+Zk4G133xkMQ/0Y+H9AT3fvQWQoyRqrw8yygX8B1wN9g/JPNCjfXFt2ufvNwMfAaGAVsNzdezT4yXX3E/axfSIikmBKYNohM+tgZjlAJpBpZjlm1iE492UzG2FmBmwHaoMfgPXAsCjrMDMbaGa/AC4g0tMBkTuDaoCNQAcz+znQrcGl64HCYL4KQEciQ0wbgRozOx74YjP1Xhrczt0paOfZQZ3vAG8C283sx8H5TDM7sMFt3nvWLSIiKUq/qNunnwG7gJnAGcHznwXnRgLPAuXAa8Af3b0kOPcr4GfB8MsVTbz3ADMrD65/CxgLFLn708H5p4D/AEuAUqCSSM9IvX8Ej5vN7G133wF8D/g7kZ6UbwKPNNO2XcANwDpgE/Ad4FR3X+butUR6lcYDy4PzfyIyhLVX3c3UISIiSWb7Pj9TREREJLHUAyMiIiKhowRGREREQkcJjIiIiISOEhgREREJnVBvJZCfn++FhYUtltu5cyddunSJf0BJoLaFT7q2a968eZvcvXfLJUVE9l2oE5jCwkLmzp3bYrmSkhKKioriH1ASqG3hk67tMrPSZMcgIu2HhpAk9RQXQ2EhRx19NBQWRl6LiIg0EOoeGElDxcUwYwZUVET2CigtjbwGmD49mZGJiEgKUQ+MpJZZs6Ci4rPHKioix0VERALqgZHUsnJlbMdDpLq6mrKyMrp3787ChQuTHU6r5eTkUFBQQFZWVrJDEZF2TAmMpBQfNAhrLFkZPDjxwbSxsrIycnNzycvLo1u3bi1fkILcnc2bN1NWVsbQoUOTHY6ItGMaQpKU8tr5l1PRIfuzBzt3htmzkxNQG6qsrCQvL4/IRt/hZGbk5eVRWVmZ7FBEpJ1TAiMpo7bO+Vnncdx8+o+oLhhEHcbOfgPh9tvTZgJvmJOXeunQBhEJPyUwkjKe+WAdyzbtZNQVF9NhZSnj/+cxZt34aNokLyIi0naUwEhKcHduKVnKkLzOHH9gf8yM0XkZvLp0M+6e7PDSxnnnnUefPn048MADmy1XUlLCq6++mqCoRERipwRGUsJryzbz37JtXHjEMDIzIkMUo3plsmHHbpZu3Jnk6NLHOeecw5NPPtliOSUwIpLqlMBISrj1xWXkd+3I1yYVfHJsVF4mAK8t3ZSssNLOkUceSa9evT5z7Pe//z2jR49m3LhxnHbaaaxYsYJbb72VG2+8kfHjxzNnzpwkRSsi0jTdRi1J9/6abby0ZCM/PHZ/crIyPzneu5MxsEcnXl26mTMPKUxegHFw1aPv88Ga7W36nqMHdOMXJ46J+bprr72W5cuXk52dzdatW+nRowcXX3wxXbt25YorrmjTGEVE2op6YCTpbntxGV2zO3DGwUM+c9zMOHR4Hq8t20xdnebBxMu4ceOYPn069957Lx066P80IhIO+m0lSbVqSwWPzV/DBUcMo3unvVd2PXREHv+YV8bCddsZM6B7EiKMj9b0lMTL448/zksvvcQjjzzC1Vdfzfvvv5/skEREWqQeGEmqO+YsIzPDOO+wxld1PWRYPgCvLd2cyLDajbq6OlatWsW0adO47rrr2Lp1K+Xl5eTm5rJjx45khyci0iQlMJI0m8p387e3VnHyhIH0657TaJl+3XMYlt+FV5XAtInTTz+dQw45hMWLF1NQUMAdd9zBGWecwdixY5kwYQI/+MEP6NGjByeeeCIPPfSQJvGKSMrSEJIkzd2vrqCqto4ZRw5vttwhw/N4+J3VVNfWkZWpnHtf3H///Xsdu+iii/Y6tt9++zF//vxEhCQi0ir6NpCk2Lm7hr++VsoXRvVlRJ+uzZY9dHg+O6tqeW/1tgRFJyIiqU4JjCTF/W+uZNuuai4uar73BeDgYZF1SzQPRkRE6imBkYSrqqnjzy8v56ChvZg4uGeL5fO6ZnNAv1xeTYMF7dJhW4R0aIOIhJ8SGEm4R/67hrXbKqPqfal36PB85q74mMrq2jhGFl85OTls3hzuvZ3cnc2bN5OT0/ikaxGRRNEkXkmoujrntheXckC/XIr26x31dYcOz+POV5bzzsqtHDI8L44Rxk9BQQFlZWVs3bo11AlATk4OBQUFLRcUEYkjJTCSUM8t2sCHG8q56RvjMbOor5s6rBcZFtkXKawJTFZWFkOHDqWkpIQJEyYkOxwRkVDTEJK0XnExFBZCRkbksbi4xbKfH9Of1287jxMXvBBTVd1yshhb0EPrwYiICKAERlqruBhmzIDSUnCPPM6Y0XgS06BsBk6/rRvIvPii5hOeRhw6PI93V21l5+6aNmqEiIiElYaQpHVmzYKKis8eq6hg+2U/4q5+U8kwyMgwMsyYfvmPyG2kLLNmwfTpUVd56PA8bilZylsrtlC0f582aISIiISVemCkdVaubPRw1w1r+e0zS7j+6SVc9+Rirv3PIrqsXxvTezRl8pBeZGVa+1gPJpbhORGRdkg9MNI6gwdHho32YIMHsfSaE6itc+rccQfuH9R4sjJ4cExVduqYyYTBPdN/Hkz9kFt9r1X98BzE1GMlIpLO1AMjrVLxi1+yKyv7swc7d8auuYbMDKNjhwxysjLp1DGTjGuugc6d9yrL7Nkx13vo8DzeX7ONbRXV+xB9imtieI5Zs5ITj4hIClICI63y12GH8eNjL6Fq4CAwgyFD4PbbG+8hmD49cm7IkJbLtuDQ4fnUObyxPI17YZoaWotxyE1EJJ1pCEliVl1bx12vrGD4SV+j46PXR3fR9OltMvwxflAPcrIyeHXpZr44pt8+v19KamJ4LtYhNxGRdKYeGInZ4/PXsm57JRccPizhdXfskMGUwl5pPZH3rQuvoKLD3sNzrRly2yeaSCwiKUwJjMTE3fnTy8sY0acrR8WwFUBbOmR4HovX72Djjt1JqT+eyj6u4Lyqkdx+xkx88GDcjNXd+1B9662JncAbyzo/IiJJoARGYvL6si0sWL2d8w8fSkZG9FsBtKVDh+cHscTYC5PiPQq1dc5lf/svDpx6w4+w0lKeW7CWwy6+kzcOPj6xwWgisYikOCUwEpM/v7yMvC4dOXnCwKTFcOCAbuRmd4jtduoQ9Cjc9tJS3lyxhau+MoZBvSJ3bR02Ip/sDhk8t2h9YoPRRGIRSXFKYCRqSzeW8+zCDZxx8BBysjKTFkeHzAwOGtaL15Zuiv6iFO9RWLB6G799eglfGtufUyZ+mhx26pjJIcPzeH7RBtw9cQE1NWFYE4lFJEUogZGo3fnycjp2yODMQ4YkOxQOGZ7Pis0VrN66K6rynsI9CruqavneA++Q3zWb2ScfuNcu3Z8/oA+lmytYtmln4oKaPZvq7JzPHkvGRGIRkSa0mMCYWV8z+7OZ/Sd4PdrMzo/iukFm9oKZLTSz983s+8HxXmb2jJl9GDz2DI6bmf3ezD4ys/lmNnFfGydtZ8vOKv45r4xTJgwkv2t2yxfE2aHD8wBavBupts656tH3WZ2b33iBFOhRuOaJhSzbuJMb/t/n6NG5417npx0Q2ffp+YUbEhfU9On85tTL2dir7z6v3SMiEg/R9MDcBTwFDAheLwEujeK6GuBydx8FHAx8x8xGAzOB59x9JPBc8BrgeGBk8DMDuCXKNkgCFL9eyu6aOs4/fGiyQwFg/7659OrSkVebGUaqqKrhonvm8ZdXVvDGBVfgbbQacFt6ftF67nm9lAuPGMphIxpPsgp6dmb/vrk8vyhxCcyS9Tu4fdAh/Oex16GuDlasUPIiIiklmgQm393/DtQBuHsNUNvSRe6+1t3fDp7vABYCA4GTgLuDYncDXw2enwT81SNeB3qYWf9YGiPxUVldy92vlVK0f29G9s1NdjhAZKfrQ4bl8drSzY3ODdmwvZJv3PY6zy9az1VfGRO5qydYDdjNKOvWm3XX/19Sv5Q3le/mR/+czwH9crni2P2bLXv0qD68tWIL23YlZguFx+evxQyOOzBNFwsUkdCLZiXenWaWBziAmR0MbIulEjMrBCYAbwB93X0tRJIcM+sTFBsIrGpwWVlw7DNbGZvZDCI9NPTt25eSkpIW6y8vL4+qXBglom1zyqrZVF7FlNwdCf1zbKltebXVrN1Wxd+eeIF+XT7Nxct21HHjvErKq53vTchmSNUKSkpWwMCBcNddbK9yrnixgknVmVyUhL8X5eXlvPDCC/zu7d1srajl0s9l8trLc5q9pteuWmrqnNsefpGp/eO/gPY/Xq9gvx4ZfDDvdT6Ie20iIrGL5jfhZcAjwHAzewXoDXwt2grMrCvwL+BSd9++5wTFhkUbObbXf63d/XbgdoDJkyd7UVFRizGUlJQQTbkwinfb3J1f3TSHA/pl8+1Tj9hrgmk8tdS2wRvL+esHL1KbP5yigyITi19aspFfF79Np44d+deFUzhwYPdGr51f9QF3vrKcX31zCoX5XVofZHFx5E6mlSsj82lmz26xV6ekpITVnYby7sYF/PzLozkjimG5I+qcm997hnWZ+RQVjW99vFFYsn4Ha558iV8eM5qiQwrjWpeISGu1OIQUDAMdBRwKXASMcff50by5mWURSV6K3f3B4PD6+qGh4LF+YL8MGNTg8gJgTTT1SPzM+XATi9fv4IIjhiU0eYnG0PwunLXsFY778sGQkcHO/gU8+MPrGNizEw9/57AmkxeAGUcOIyszgz+WfNT6AGJdWyZYSO+oo4+m6Nip/GjzXM45tDCqqjIzjKL9elOyeCO1dfG9nVrDRyISBtHchXQW8E1gEjAROD041tJ1BvwZWOjuv21w6hHg7OD52cC/Gxw/K7gb6WBgW/1QU6s1+MJIxZVXE2YfVqC9Y84y+uRm85XPDWi5cILZfffxs3/fSN6mdeBOl3Wr+fWTf+ChHisY0KNTs9f26ZbD6VMH8+Dbq1m1paLZsk1qYm2ZnVf8mEf/u4ZnP1jPKx9tYl7pFlb94U/UXXghlJZi7gzctoGLi68j4/77oq7u6FF92bKzindXbW1dvFF6/L21TC3sRZ/cnJYLi4gkSTRDSFMaPM8BPg+8Dfy1hesOA84E3jOzd4NjPwWuBf4e3Iq9Evh6cO4J4ATgI6ACODeaBjSp/n/HFRWRsan6/x1D+7qbosGfAxDTn8PidTuY8+Emfnjs/nTskIJLBs2aRceqys8cyq6qhCt/Due0mGNz0VHDuO+Nldz64lJmnzw29vqbWEOm07o1fPf+dz5z7OVbfkrGrs+uWZOxK1hIL8q/j0eN7E1mhvHCog1MGtIz9nijsGT9Dj7aUM5ZJ42Jy/uLiLSVFhMYd/9uw9dm1h24J4rrXqbxeS0QSYL2LO/Ad1p636g1t/Jqe0pg9uHP4U9zltEpK5PpByV/rZRG7ePidP27d+Lrkwv4x9wyLjl6BP27N99rs5fBgyMJ4R7qCgp45gdHUlldx67qWnZV1zLwuiZu945hIb3unbOYNKQnzy3a0OJdS631mIaPRCQkWvPf6goia7WkthReeTWhmmivr1zJpvKmd3PesKOSf7+7hq9NKmh0cbWU0AbL3X+raDh17tz24rKYq3/zwsup6LDHon6dO9Ph2l8xsm8uYwu6M3VoL47arzfWRkvzH31AHxau3c6aKFcgjtUTGj4SkZCIZg7Mo2b2SPDzGLCYT+etpC7t5QJAXcGgRo+vzs3n0Guf5ycPzuejDTv2On/Pa6VU19VxXoosXNeo2bMji9E1FOPidAU9O3PKxIHc/+ZKNuyobPmCwPtrtnHmrhH86cyZ+ODBLa9W2waxQmRbAYAXFrf9onb1w0dfHqfll0Qk9UXTA3M9cEPw8yvgSHef2fwlKaCNvjDC7l9f+3YTvQTXcurEAh58ezXH/PYlzv3Lm7z60Sa8uJi6IUP4wbGjeOuOCxj61MPJCTwa06dHEoYhQ/ZpuftvF42guraOO16Krhdma0UVF987j56dO3L6736ClZa2vFptg1h9H2Id0acrg3p1isu2AvXDR8dq+EhEQiCa26hfbPDziruXJSKwfdbwC4PIyqsVN9/Srua/vFe2jR9lH8gT371qry/5ft86j1+dMpZXZx7ND47Zj/ll23jgB9ey+9zzyVi5kgyc/M3rmr8tOBVMnx5JHPZhufvC/C58dfxA7n19JZubGVYDqKtzLv3bu6zbVskfz5hI79wY9oUKYn3x+edbHauZcfT+fXhl6SYqq1tcEDtq7q7hIxEJlSYTGDPbYWbbG/nZYWbbExlkqwVfGLf88xkO/9ZfePOQ45IdUcLU1jk/e/g98rpk84XZlzX5JZ/XNZvvHzOSV2Yeza/mPkBO9R5f4PUTftPct6eNoLKmlj+9vLzZcjc99yElizfy8xPHMHFwfO4EasnRo/pSWV3X4kaWsViyvlzDRyISKk0mMO6e6+7dGvnJdfduiQxyXw3vnkFmhjF3xcfJDiVh7n9zJf8t28b/fHkU3TtltVg+JyuTLuubWDewHUx8HtGnK18a25+/vrqCrRVVjZZ5buF6fv/ch3xtUgFnJPHOrIOG9qJzx0yeW7S+zd7z8fc0fCQi4RL1XUhm1sfMBtf/xDOotpbdwRgzoBtvrdiS7FASYlP5bq57chGHDMuLbQG6dj7x+ZKjR7CzqpY7X1mx17kVm3Zy6d/e5cCB3fjfrx6Y1FWJc7IyOWxEPi8s2tjoRpaxqh8+Omioho9EJDyiuQvpK2b2IbAceBFYAfwnznG1uclDevHuqq1U1dQlO5S4+9UTi9hVXcvVXx0T2xdtO5/4fEC/bhw3ph9/eWU52ys/3fW5oqqGi++dR2aGccv0SeRkZSYxyojPH9CH1Vt3sXj93neQxap++OhLYzV8JCLhEU0PzNXAwcASdx9KZBG6V+IaVRxMKezJ7po63l8T00baofPGss386+0yLjxiGCP65MZ2cRvd1RNmlxw9gh2VNdwd9MK4OzP/9R6L1+/g96dNYFCvzs2/QYJMC26nfq4N7kZ6/L21ZGj4SERCJpoEptrdNwMZZpbh7i8A8d0ONw4mFUYmXKbzPJjq2jr+598LGNijE989upVrDbbBXT1hduDA7vz047c59dTD8WCDSO4r5vIv7MeR+/VOdnif6NsthwMHduOFRfuWwLg7j89fw1QNH4lIyESTwGw1s67AHKDYzH4H1MQ3rLbXJzeHwrzOaT0P5s6Xl7NkfTlXfmUMnTomf5gjlIqLueCeXzFg2wbMna7r1/Cbp2/m22veTHZkezn6gL68vfJjtuxsfNJxNJasL2fpxp0aPhKR0IkmgXkJ6AF8H3gSWAqcGM+g4mXSkF7MLf24TSY+ppo1W3dx07MfcsyovnxhdN9khxNes2bttelidlUlGT9LvVvJjz6gD3UOLy5pfS+Mho9EJKyiSWAMeAooAboCfwuGlEJnSmFPtuysYtmmnckOpc398tEPcJxfnDg62aGEW4j20Bo3sDv5XTvy/KKNrbpew0ciEmbRrMR7lbuPIbJT9ADgRTN7Nu6RxcHkwl4AzEuzeTAvLNrAk++v47tHj0yZSaahFaJbyTMyjGn79+HFxRuoro397rpPho/GxXCrvYhIiohlN+oNwDpgM9AnPuHE1/DeXejZOSut5sFU1Tq/eOR9hvfuwoVHDEt2OOEXslvJjz6gD9sra5hXGntS/vj8NWQYHDdGw0ciEj7RrAPzLTMrAZ4D8oEL3X1cvAOLBzNjcmFkHkzoFRdDYSFfOObz3Df7G9xii+jYIZZ8VBoVslvJDx+ZT1amxXw3krvz+HtrmTq0V2z7OYmIpIhovvGGAJe6+xh3/4W7fxDvoOJpSmFPlm/aycYdzW/al9KKiyObLJaWYjgF2zey3/9cntqbLoZJiG4lz83J4qCheTwXYwKzeP0ODR+JSKhFMwdmpru/m4hgEmHSkGAeTGmIh5FmzYpssthQO9l0UfZ2/srXuOuqr+MZGVBYGFUi+8T8tRo+EpFQa3djDgcO7EZ2h4xwL2gXojtlJM6Kiznq+p9SsH0j5g6lpZHeuaaSmOJifMgQLj12FG/cfgG9H/lnYuMVEWkj7S6Bye6QyecG9eCtMM+DCdGdMhJnjaxbQ0UFu340kwWrt7FheyW1dcG6R8HQo61cSQZO7y3rmk92RERSWIdkB5AMUwp7ctuLy6ioqqFzx/D9EdRe/b9UnX8BnaobzONJ4TtlJI6a6HXLXrOaL//fywBkGOR3zeaxGy6nT1NDjyk8z0dEpDHtrgcGIuvB1NQ5767amuxQWuWZCcfw42MvYVf/AjwEd8pIHDXR61YzcCC3njGJq08aw3emjaBo/970/riJib4aehSREApf90MbmDi4J2aRjR0PHZ6f7HBiVvxGKR8dejxZD1/Hi3NeoqioKNkhSbLMnh0ZBmrYs9K5Mx1/fS3H7bk9wJDBkTkye9LQo4iEULvsgeneKYv9++aGcj2Y0s07mfPhJk6bMpgOme3y45OGYlm3JmSL9ImINKfdfgNOLuzJ26UffzrBMSTue3MlmRnGN6YMSnYokiqiXbcmZIv0iYg0p90mMFMKe1G+u4ZF67YnO5So7a6p5R9zyzhmVB/6ddfme9IKIVqkT0SkOe02ganf2DFM68E8uWAdW3ZWccbBQ5IdioiISFK12wRmYI9ODOieE6qNHYtfX8mQvM4cFsKJxyIiIm2p3SYwAJMKezF3xce4x3EeTLDpIjEs896YJet38OaKLXxz6mAyMqxNQxQREQmbdp3ATCnsybrtlazeuqvlwq3RYNNFolnmvRn3vbGSjpkZfG1SQRwCFRERCZd2ncBMHhK/eTA7d9ew64cz22TTxYqqGv71dhnHj+1HXtfsNoxSREQknNp1ArN/v1xyszvEPg+mkWEhd+f9Ndv4Y8lHnHb7a4z/5dNkr13d+PUxrnz62H/XsqOyhukHafKuiIgItNOVeOtlZhgTh/RkXiwL2tUPC9X3rJSWUnXeBVz18AKKhx8OwKj+3Tjv8KFUDRhIzpqyvd8jxpVPi98oZb++XZlS2DOm60RERNJVu05gACYP6clvn13CtopqunfOavmCWbP2GhbqWFXJ5SV3M2HmdzhyZD59ugVrtFx37V7LvFd0yOa/51/GIVHG917ZNv5bto2rvjIGM03eFRERgXY+hASR9WDc4e2VUfbCNDH802vzOr42qeDT5AX2WvnUBw/mL2f/hLN3j2R+WXQbSRa/UUqnrExOnjgwuvhERETagZRKYMzsODNbbGYfmdnMRNQ5flAPOmRY1PNgqgY0cRdQU8NCDVY+tdJSTv/dT+jdNZuL75nHpvLdzda1vbKaf7+7hq98bgDdcqLoHRIREWknUiaBMbNM4GbgeGA0cLqZjY53vZ06ZnLgwO5R3Ym0blslVx86nV1Ze9wJFMOGeL26dOTWMyaxaWcVl9z3NjW1dU2Wffid1eyqrmX6wdotWEREpKGUSWCAqcBH7r7M3auAB4CTElHxlMKe/LdsK7trapssU1FVwwV/fYsHDziKLTf9YZ82xBtb0J1rTh7L68u2cO1/FjVaxt0pfn0lYwd2Z1xBj5jbJCIiks5SaRLvQGBVg9dlwEF7FjKzGcAMgL59+1JSUtLiG5eXlzdbLqe8ht01ddzzaAkjembudb7OnT+8s5v3N9Ty/YnZfNhnBB/edddnC0URR0P5wOcHd+BPLy+nw/Y1HDzgsx/Fhx/Xsnh9Jece2LHZ2FtqW5ila9vStV0iIomUSglMY7fY7LXGv7vfDtwOMHnyZC8qKmrxjUtKSmiu3IHlu/m/d56ltlchRUcN3+v8tf9ZxNsblvLzL4/mvMOHtlhftA49vI5v3vE6dy3cxknTpjKqf7dPzj38wDvkZm/gh/9vGp07Nv0xtdS2MEvXtqVru0REEimVhpDKgEENXhcAaxJRcX7XbIbld+GtRubB/H3uKm59cSnTDxrMuYcVtmm9HTtk8MczJtItJ4uL7pnH1ooqALbsrOKJ99ZxysSBzSYvIiIi7VUqJTBvASPNbKiZdQROAx5JVOWTC3syr3TLZzZ2fH3ZZmY99B7IyPK/AAAVc0lEQVSHj8jnyjitw9InN4dbzpjE2m27uP/71+JDhtAzN4fn/3A2F61+o83rExERSQcpk8C4ew1wCfAUsBD4u7u/n6j6Jxf24uOKapZu3AnAik07ufjeeQzu1Zmbp08kKzN+f1SThvTkLx0/5Oy7rsFWrsTcKdi+kQE//F6rd68WERFJZymTwAC4+xPuvp+7D3f36O5LbiNTCus3dtzCtopqzrv7LQy485wpdO8U/zVYDrvzt3Su2WNdmFZs/CgiItIepFQCk0yFTz3Mq7eexzcOKqRq0GA+99Lj3HbmZIbkdUlI/bZqVeMnYtz4UUREpD1QAgNQXIzNmMGAbRswnN5b1vGbp29m6qv/SVwMTa3kG+PGjyIiIu2BEhhodIPGDpW7Ejt8M3t2ZEXfhmJY4VdERKQ9UQIDTQ/TJHL4Zo+NH1uzwq+IiEh7oUVGIDJMU1ra+PFEmj5dCYuIiEgU1AMDGr4REREJGSUwoOEbERGRkLGGK8+GjZltBBoZ+9lLPrApzuEki9oWPunariHu3jvZQYhI+xDqBCZaZjbX3ScnO454UNvCJ13bJSKSSBpCEhERkdBRAiMiIiKh014SmNuTHUAcqW3hk67tEhFJmHYxB0ZERFKPmZ0DXODuhyc7Fgmf9tIDIyIi+8jMss3sz2ZWamY7zOwdMzs+TnUVmpmbWXnws97MHjOzL8TwHueY2cv7GMdPzWx5EEOZmf0tUXVL85TAiIhItDoAq4CjgO7A/wB/N7PCONbZw927Ap8DngEeCnpu4s7MzgbOBI4JYpgMPJeIuqVlaZ/AmNlxZrbYzD4ys5nJjqctmdkKM3vPzN41s7nJjqe1zOxOM9tgZgsaHOtlZs+Y2YfBY89kxthaTbTtSjNbHXxu75rZCcmMUSRa7r7T3a909xXuXufujwHLgUkAZlYU9FJcHvy9X2tm59Zfb2Z5ZvaImW03szeB4THUvc7dfwdcCfzazDKC95xpZkuDHqEPzOzk4Pgo4FbgkKD3ZGtw/EtBz9F2M1tlZlc2U+0U4Cl3X9oghk/msJlZ96BHam3wb/p/zSyzqbqlbaV1AmNmmcDNwPHAaOB0Mxud3Kja3DR3Hx/ydUXuAo7b49hM4Dl3H0nkfzxhTT7vYu+2AdwYfG7j3f2JBMck0ibMrC+wH/B+g8P9iPTODATOB25u8B+Qm4FKoD9wXvATqweBPsD+weulwBFBnVcB95pZf3dfCFwMvObuXd29R1B+J3AW0AP4EvAtM/tqE3W9DpxlZj80s8nBd0pDdwM1wAhgAvBFInN6mqpb2lBaJzDAVOAjd1/m7lXAA8BJSY5J9uDuLwFb9jh8EpFfDgSPTf2CSWlNtE0k9MwsCygG7nb3RQ1OVQO/dPfqIDkvB/YPvvxPBX4e9OQs4NN/47FYEzz2AnD3f7j7mqBH6G/Ah0R+9zfK3Uvc/b2g/HzgfiJDYo2VvRf4LnAs8CKwob4nP0jejgcuDdqzAbgROK0VbZJWSPcEZiCR8dp6ZcGxdOHA02Y2z8xmJDuYNtbX3dcCBI99khxPW7vEzOYHQ0yhHB6T9isYvrkHqAIu2eP0ZnevafC6AugK9ObTOTT1otkKZk/1v8O3BLGcFQzFbg2Gag4ksl1HU7EfZGYvmNlGM9tGpKekyfLuXuzuxxDpsbkY+KWZHQsMAbKAtQ3qvo30+12VstI9gbFGjqXTfeOHuftEIv8L+I6ZHZnsgCQqtxAZ+x8PrAVuSG44ItEzMwP+DPQFTnX36igv3UhkuGVQg2ODWxHCycAGYLGZDQHuIJJE5QVDNQv49Hd/Y7/v7wMeAQa5e3cic1Ua+674jKBH6R/AfCJJ0ipgN5Dv7j2Cn27uPqaZuqUNpXsCU8Zn/7EU8Gn3Y+i5+5rgcQPwEM10m4bQejPrDxA8bkhyPG3G3de7e6271xH55ZtOn5ukv1uAUcCJ7r4r2ovcvZbI/JUrzaxzMB/x7GivN7O+ZnYJ8AvgJ8G/ny5EEoWNQZlziSQX9dYDBWbWscGxXGCLu1ea2VTgm83UeU4w6TfXzDKCW8bHAG8EPcNPAzeYWbfg/HAzqx+OaqxuaUPpnsC8BYw0s6HBX6LTiGTeoWdmXcwst/45kcljC5q/KlQe4dNfbmcD/05iLG2qPjELnEx6fW6SxoIej4uI9B6us0/XaJke5VtcQmQ4aR2RCe5/ieKarWa2E3gPOAH4urvfCeDuHxDpwXyNSMIwFnilwbXPE5lgvM7M6neA/zaRYaAdwM+BvzdT93bgp8BKYCtwHfAtd69f3+UsoCPwAfAx8E8iE5SbqlvaUNqvxBvconoTkAnc6e6zkxxSmzCzYUR6XSAyrnxfWNtmZvcDRUTGodcT+R/Ww0R+sQwm8svj6+4eusmwTbStiMgXgAMrgIvq5/uIiEh00j6BERERkfST7kNIIiIikoaUwIiIiEjoKIERERGR0OmQ7ABERJIpPz/fCwsLY7pm586ddOnSJT4BJYnaFB7p2K76Ns2bN2+Tu/eO5holMCLSrhUWFjJ3bmx7oZaUlFBUVBSfgJJEbQqPdGxXfZvMLOrVmTWEJG3KzF6NsXyRmT0Wr3hERCQ9KYGRNuXuhyY7BhERSX9KYKRNmVl58FhkZiVm9k8zW2RmxcEeKpjZccGxl4FTGlzbJdjc8C0ze8fMTgqOX2ZmdwbPx5rZAjPrnITmSTtmV9knP/PWzvvkuYgkhxIYiacJwKXAaGAYcJiZ5RDZ/+dE4AigX4Pys4Dn3X0KMA34TbBNwk3ACDM7mcjS4xe5e0XimiEiIqlGk3glnt509zIAM3sXKATKgeXu/mFw/F5gRlD+i8BXzOyK4HUOMNjdF5rZOUR2gb3N3RvudSKSchrrmfFfaNVzkbakBEbiaXeD57V8+vetqd/kBpzq7osbOTeSSPIzoO3CExGRsNIQkiTaImComQ0PXp/e4NxTwHcbzJWZEDx2B34HHAnkmdnXEhiviIikICUwklDuXklkyOjxYBJvw3v+rwaygPlmtiB4DXAj8Ed3XwKcD1xrZn0SGLaIiKQYDSFJm3L3rsFjCVDS4PglDZ4/CRzQyLW7gIsaOX5eg+ergBFtGbOIiISPemBEREQkdJTAiIiISOgogREREZHQUQIjIiIioaMERkREREJHCYyIpJVgr63FZvaRmc1MdjwiEh9KYEQkbZhZJnAzcDyRPbhON7PRyY1KROJBCYyIpJOpwEfuvszdq4AHgJOSHJOIxIG5a4MxEUkPwTYTx7n7BcHrM4GDGi6kGByfQbCJaN++fSc98MADMdVTXl5O165d2yTmeWvn7XVsUv9JUZWLpWxj5RqWLcguoGx3WdLqj8d7hrFN0ZStb1ey6m+uXKxl69X/m5o2bdo8d5/cbOGAEhgRSRtm9nXg2D0SmKnu/t2mrpk8ebLPnTs3pnpKSkooKiral1A/Ee3O1Y2Vi6VsU7th15e9fr/ruWLJFUmrPx7vGcY2RVO2vl3Jqr+5crGWrVf/b8rMok5gNIQkIumkDBjU4HUBsCZJsYhIHCmBEZF08hYw0syGmllH4DTgkSTHJCJxoM0cRSRtuHuNmV0CPAVkAne6+/tJDqtZLXWti0jjlMCISFpx9yeAJ5Idh4jEl4aQREREJHSUwIiIiEjoKIERERGR0FECIyIiIqGjSbwiIiGgu5VEPks9MCIiIhI6SmBEREQkdJTAiIiISOhoDoyISJrRfBlpD9QDIyIiIqGjBEZERERCRwmMiIiIhI4SGBEREQkdJTAiIiISOkpgREREJHSUwIiIiEjoaB0YEZF2rH7NmJKSEvx0rR8j4aEeGBEREQkd9cCIiEiLtLqvpBolMCIikjRKjKS1lMCIiEibUlIiiaA5MCIiIhI6SmBEREQkdJTAiIiISOgogREREZHQUQIjIiIioaMERkREREJHCYyIiIiEjhIYERERCR0lMCIiIhI6SmBEREQkdJTAiEhaMLMrzWy1mb0b/JyQ7JhEJH60F5KIpJMb3f36ZAchIvGnBEZERFKeNoiUPZm7/lKISPiZ2ZXAOcB2YC5wubt/3ETZGcAMgL59+0564IEHYqqrvLycrl277ku4KSed2jRv7TwACrILKNtdBsCk/pOaLLenaMs2Vi6Wsq2tv75dyaq/uXKxlq1X//dv2rRp89x9crOFA0pgRCQ0zOxZoF8jp2YBrwObAAeuBvq7+3ktvefkyZN97ty5McVRUlJCUVFRTNekunRqk11lAFy/3/VcseQKoPEenPpye4q2bFO9QtGWbW399e1KVv3NlYu1bL36v39mFnUCoyEkEQkNdz8mmnJmdgfwWJzDEZEk0l1IIpIWzKx/g5cnAwuSFYuIxJ96YEQkXVxnZuOJDCGtAC5KbjgiEk9KYEQkLbj7mcmOQUQSR0NIIiIiEjpKYERERCR0NIQkIiLtUroujpeu7dqTemBEREQkdJTAiIiISOgogREREZHQ0RwYERGRFrSXeSVhoh4YERERCR0lMCIiIhI6GkISERFJcQ2HsEpKSvDTNaSlBEZERCQJNK9m3yiBERHZQ3V1NWVlZVRWVjZ6vnv37ixcuDDBUe27nJwcCgoKyMrKSnYoIvtMCYyIyB7KysrIzc2lsLAQM9vr/I4dO8jNzU1CZK3n7mzevJmysjKGDh2a7HBE9pkSGBGRPVRWVjaZvISVmZGXl8fGjRuTHUrc1Q/NJGuuiIaGEkN3IYmINCKdkpd66dgmab+UwIiIiEjoaAhJRKQFdlXb9lxEM8SwatUqzjrrLNatW0dGRgYzZszg+9//ftR1FBUVcf311zN58uR9CVUkZSmBERFJQR06dOCGG25g4sSJ7Nixg0mTJvGFL3yB0aNHJzs0kZSgISQRkRTUv39/Jk6cCEBubi6jRo1i9erVFBUV8eMf/5ipU6ey3377MWfOHAB27drFaaedxrhx4/jGN77Brl27khm+SNypB0ZEJMWtWLGCd955h4MOOgiAmpoa3nzzTZ544gmuuuoqnn32WW655RY6d+7M/PnzmT9//ifJj0i6Ug+MiEgKKy8v59RTT+Wmm26iW7duAJxyyikATJo0iRUrVgDw0ksvccYZZwAwbtw4xo0bl5R4RRJFCYyISIqqrq7m1FNPZfr06Z8kLQDZ2dkAZGZmUlNT88lx3SYt7YkSGBGRFOTunH/++YwaNYrLLrusxfJHHnkkxcXFACxYsID58+fHO0SRpNIcGBGRFux523MithJ45ZVXuOeeexg7dizjx48H4Jprrmmy/Le+9S3OPfdcxo0bx/jx45k6dWpc4xNJNiUwIiIp6PDDD8d97/ViTjjhhE+e5+fnfzIHplOnTjzwwAOJCk8k6ZTAiIiItEOx7NmUivs7aQ6MiIiIhI4SGBGRRjQ2fBN26dgmab+UwIiI7CEnJ4fNmzen1Re+u7N582ZycnKSHYpIm9AcGBGRPRQUFFBWVsbGjRsbPV9ZWRnKRCAnJ4eCgoJkhyFpLlHzZZTAiEiomNnXgSuBUcBUd5/b4NxPgPOBWuB77v5Ua+rIyspi6NChTZ4vKSlhwoQJrXlrEWkjSmBEJGwWAKcAtzU8aGajgdOAMcAA4Fkz28/daxMfoojEm+bAiEiouPtCd1/cyKmTgAfcfbe7Lwc+ArSam0iaUg+MiKSLgcDrDV6XBcf2YmYzgBkAffv2paSkJKaKysvLY74m1alN4ZGO7WpNm5TAiEjKMbNngX6NnJrl7v9u6rJGjjU6m9DdbwduD+raOG3atNIYQ8wHNsV4TapTm8IjHdtV36Yh0V6gBEZEUo67H9OKy8qAQQ1eFwBroqird6wVmdlcd58c63WpTG0Kj3RsV2vapDkwIpIuHgFOM7NsMxsKjATeTHJMIhInSmBEJFTM7GQzKwMOAR43s6cA3P194O/AB8CTwHd0B5JI+tIQkoiEirs/BDzUxLnZwOwEhHF7AupINLUpPNKxXTG3ydJpqWwRERFpHzSEJCIiIqGjBEZERERCRwmMiEgMzOw4M1tsZh+Z2cxkx9MWzGyFmb1nZu+a2dyWr0g9ZnanmW0wswUNjvUys2fM7MPgsWcyY4xVE2260sxWB5/Vu2Z2QjJjjJWZDTKzF8xsoZm9b2bfD47H/FkpgRERiZKZZQI3A8cDo4HTgz2Y0sE0dx8f4vVF7gKO2+PYTOA5dx8JPBe8DpO72LtNADcGn9V4d38iwTHtqxrgcncfBRwMfCf4NxTzZ6UERkQkelOBj9x9mbtXAQ8Q2YNJkszdXwK27HH4JODu4PndwFcTGtQ+aqJNoebua9397eD5DmAhkS0/Yv6slMCIiERvILCqwesm91sKGQeeNrN5wT5R6aKvu6+FyBcn0CfJ8bSVS8xsfjDEFKphsYbMrBCYALxBKz4rJTAiItGLer+lkDnM3ScSGRr7jpkdmeyApEm3AMOB8cBa4IbkhtM6ZtYV+Bdwqbtvb817KIEREYleq/ZbSnXuviZ43EBkkcCpyY2ozaw3s/4AweOGJMezz9x9vbvXunsdcAch/KzMLItI8lLs7g8Gh2P+rJTAiIhE7y1gpJkNNbOOwGlE9mAKLTPrYma59c+BLwILmr8qNB4Bzg6enw00tZN5aNR/yQdOJmSflZkZ8Gdgobv/tsGpmD8rrcQrIhKD4LbVm4BM4M5g+4LQMrNhfLo1QwfgvjC2yczuB4qAfGA98AvgYSL7Yw0GVgJfd/fQTIptok1FRIaPHFgBXFQ/dyQMzOxwYA7wHlAXHP4pkXkwMX1WSmBEREQkdDSEJCIiIqGjBEZERERCRwmMiIiIhI4SGBEREQkdJTAiIiISOkpgREQkpZjZqzGWLzKzx+IVj6QmJTAiIpJS3P3QZMcgqU8JjIiIpBQzKw8ei8ysxMz+aWaLzKw4WMkVMzsuOPYycEqDa7sEmxy+ZWbvmNlJwfHLzOzO4PlYM1tgZp2T0DxpI0pgREQklU0ALgVGA8OAw8wsh8g+QCcCRwD9GpSfBTzv7lOAacBvgi0SbgJGmNnJwF+IrGBbkbhmSFtTAiMiIqnsTXcvCzYvfBcoBA4Alrv7hx5ZTv7eBuW/CMw0s3eBEiAHGBxcfw5wD/Ciu7+SuCZIPHRIdgAiIiLN2N3geS2ffm81tQ+OAae6++JGzo0EyoEBbReeJIt6YEREJGwWAUPNbHjw+vQG554CvttgrsyE4LE78DvgSCDPzL6WwHglDpTAiIhIqLh7JTADeDyYxFva4PTVQBYw38wWBK8BbgT+6O5LgPOBa82sTwLDljam3ahFREQkdNQDIyIiIqGjBEZERERCRwmMiIiIhI4SGBEREQkdJTAiIiISOkpgREREJHSUwIiIiEjo/H9k5BjUHP2nAgAAAABJRU5ErkJggg==
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Other-Plot-Styles">Other Plot Styles<a class="anchor-link" href="#Other-Plot-Styles">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[14]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">y</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">standard_normal</span><span class="p">((</span><span class="mi">1000</span><span class="p">,</span> <span class="mi">2</span><span class="p">))</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>散点图</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[15]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">7</span><span class="p">,</span> <span class="mi">5</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">y</span><span class="p">[:,</span> <span class="mi">0</span><span class="p">],</span> <span class="n">y</span><span class="p">[:,</span> <span class="mi">1</span><span class="p">],</span> <span class="s1">&#39;ro&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;1st&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;2nd&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Scatter Plot&#39;</span><span class="p">)</span>
<span class="c1"># tag: matplotlib_11_a</span>
<span class="c1"># title: Scatter plot via +plot+ function</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[15]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0.5,1,&#39;Scatter Plot&#39;)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>可以直接用plt.scatter函数</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[16]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">7</span><span class="p">,</span> <span class="mi">5</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">y</span><span class="p">[:,</span> <span class="mi">0</span><span class="p">],</span> <span class="n">y</span><span class="p">[:,</span> <span class="mi">1</span><span class="p">],</span> <span class="n">marker</span><span class="o">=</span><span class="s1">&#39;o&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;1st&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;2nd&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Scatter Plot&#39;</span><span class="p">)</span>
<span class="c1"># tag: matplotlib_11_b</span>
<span class="c1"># title: Scatter plot via +scatter+ function</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[16]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0.5,1,&#39;Scatter Plot&#39;)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<ul>
<li>plt.scatter可以指定颜色</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[17]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">c</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">random</span><span class="o">.</span><span class="n">randint</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">10</span><span class="p">,</span> <span class="nb">len</span><span class="p">(</span><span class="n">y</span><span class="p">))</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[18]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">7</span><span class="p">,</span> <span class="mi">5</span><span class="p">))</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">y</span><span class="p">[:,</span> <span class="mi">0</span><span class="p">],</span> <span class="n">y</span><span class="p">[:,</span> <span class="mi">1</span><span class="p">],</span> <span class="n">c</span><span class="o">=</span><span class="n">y</span><span class="p">[:,</span> <span class="mi">1</span><span class="p">],</span> <span class="n">marker</span><span class="o">=</span><span class="s1">&#39;o&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">colorbar</span><span class="p">()</span>
<span class="n">plt</span><span class="o">.</span><span class="n">grid</span><span class="p">(</span><span class="kc">True</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;1st&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;2nd&#39;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">&#39;Scatter Plot&#39;</span><span class="p">)</span>
<span class="c1"># tag: matplotlib_11_c</span>
<span class="c1"># title: Scatter plot with third dimension</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[18]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0.5,1,&#39;Scatter Plot&#39;)</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
