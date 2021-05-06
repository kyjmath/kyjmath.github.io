---
layout: post
comments: true
title : Machine Learning1 [CHI]
categories: [Practice]
---


<html>
<head><meta charset="utf-8" />

<title>2019_Lec10_Trading and machine learning_1</title>

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
<h2 id="&#26426;&#22120;&#23398;&#20064;">&#26426;&#22120;&#23398;&#20064;<a class="anchor-link" href="#&#26426;&#22120;&#23398;&#20064;">&#182;</a></h2><p>从数据进行学习和预测的模型方法或算法</p>
<ul>
<li><p>有监督学习</p>
<p>对特定的目标变量进行预测，并且有目标变量的数据可以利用。在监督学习Supervised learning,有一个变量可以对照，优化是一般有比较明确的目标。</p>
<ul>
<li>回归</li>
<li>分类</li>
</ul>
</li>
<li><p>无监督学习</p>
<p>无特定的目标变量，目的是探索数据内的规律</p>
<ul>
<li>聚类</li>
</ul>
</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="&#20998;&#31867;&#22238;&#24402;&#30340;&#22522;&#26412;&#27010;&#24565;">&#20998;&#31867;&#22238;&#24402;&#30340;&#22522;&#26412;&#27010;&#24565;<a class="anchor-link" href="#&#20998;&#31867;&#22238;&#24402;&#30340;&#22522;&#26412;&#27010;&#24565;">&#182;</a></h2><ul>
<li>数据 $(\mathbf{x_1},y_1),(\mathbf{x_2},y_2),\ldots,(\mathbf{x_N},y_N)$</li>
<li>有监督学习: $\hat{y}_i=f(\mathbf{x_i})$</li>
<li>分类和回归</li>
<li>训练样本(training data)，检验样本（test data） </li>
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
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Scikit-Learn&#24211;">Scikit-Learn&#24211;<a class="anchor-link" href="#Scikit-Learn&#24211;">&#182;</a></h1>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a href="http://scikit-learn.org/stable/index.html">scikit-learn: machine learning in Python — scikit-learn 0.19.1 documentation</a></p>
<p><img src="scikit_learn.png" alt=""></p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a href="http://python.jobbole.com/81721/">基于 Python 和 Scikit-Learn 的机器学习介绍 - Python - 伯乐在线</a></p>
<h3 id="&#36923;&#36753;&#22238;&#24402;-(logistic-regression)">&#36923;&#36753;&#22238;&#24402; (logistic regression)<a class="anchor-link" href="#&#36923;&#36753;&#22238;&#24402;-(logistic-regression)">&#182;</a></h3><p>大多数情况下被用来解决分类问题（二元分类），但多类的分类（所谓的一对多方法）也适用。这个算法的优点是对于每一个输出的对象都有一个对应类别的概率。</p>
<h3 id="&#26420;&#32032;&#36125;&#21494;&#26031;-&#65288;Naive-Bayesian&#65289;">&#26420;&#32032;&#36125;&#21494;&#26031; &#65288;Naive Bayesian&#65289;<a class="anchor-link" href="#&#26420;&#32032;&#36125;&#21494;&#26031;-&#65288;Naive-Bayesian&#65289;">&#182;</a></h3><p>它也是最有名的机器学习的算法之一，它的主要任务是恢复训练样本的数据分布密度。这个方法通常在多类的分类问题上表现的很好。</p>
<h3 id="k-&#26368;&#36817;&#37051;-(k-nearnest-neighbor)">k-&#26368;&#36817;&#37051; (k-nearnest neighbor)<a class="anchor-link" href="#k-&#26368;&#36817;&#37051;-(k-nearnest-neighbor)">&#182;</a></h3><p>kNN（k-最近邻）方法通常用于一个更复杂分类算法的一部分。例如，我们可以用它的估计值做为一个对象的特征。有时候，一个简单的kNN算法在良好选择的特征上会有很出色的表现。当参数（主要是metrics）被设置得当，这个算法在回归问题中通常表现出最好的质量</p>
<h2 id="&#20915;&#31574;&#26641;-(Decision-Tree)">&#20915;&#31574;&#26641; (Decision Tree)<a class="anchor-link" href="#&#20915;&#31574;&#26641;-(Decision-Tree)">&#182;</a></h2><p>分类和回归树（CART）经常被用于这么一类问题，在这类问题中对象有可分类的特征且被用于回归和分类问题。决策树很适用于多类分类。</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="&#20915;&#31574;&#26641;">&#20915;&#31574;&#26641;<a class="anchor-link" href="#&#20915;&#31574;&#26641;">&#182;</a></h1><p><a href="http://dataaspirant.com/2017/02/01/decision-tree-algorithm-python-with-scikit-learn/">http://dataaspirant.com/2017/02/01/decision-tree-algorithm-python-with-scikit-learn/</a></p>
<p><a href="http://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients">http://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients</a></p>
<p><a href="http://archive.ics.uci.edu/ml/datasets/Dow+Jones+Index">http://archive.ics.uci.edu/ml/datasets/Dow+Jones+Index</a></p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><img src="B03905_05_01-compressor.png" alt=""></p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="scikit-learn&#20915;&#31574;&#26641;&#32467;&#26524;&#30340;&#21487;&#35270;&#21270;">scikit-learn&#20915;&#31574;&#26641;&#32467;&#26524;&#30340;&#21487;&#35270;&#21270;<a class="anchor-link" href="#scikit-learn&#20915;&#31574;&#26641;&#32467;&#26524;&#30340;&#21487;&#35270;&#21270;">&#182;</a></h3><p>决策树可视化可以方便我们直观的观察模型，以及发现模型中的问题。</p>
<h3 id="&#20915;&#31574;&#26641;&#21487;&#35270;&#21270;&#29615;&#22659;&#25645;&#24314;">&#20915;&#31574;&#26641;&#21487;&#35270;&#21270;&#29615;&#22659;&#25645;&#24314;<a class="anchor-link" href="#&#20915;&#31574;&#26641;&#21487;&#35270;&#21270;&#29615;&#22659;&#25645;&#24314;">&#182;</a></h3><p>scikit-learn中决策树的可视化一般需要安装graphviz。主要包括graphviz的安装和python的graphviz插件的安装。</p>
<ul>
<li><p>第一步是安装graphviz。下载地址是： <a href="http://www.graphviz.org/">http://www.graphviz.org/</a> 。如果你是Linux系统，可以用apt-get或者yum的方法安装。如果是Windows，就在官网上下载msi文件安装。无论是Linux还是Windows，装完后都要设置环境变量，将graphviz的bin目录加到PATH中，比如我是Windows，则需要将C:\Program Files (x86)\Graphviz2.38\bin\加入到PATH中。</p>
</li>
<li><p>第二步是安装python的graphviz插件，执行下面的安装命令即可： pip install graphviz。(conda)</p>
</li>
<li><p>第三步是安装python的pydotplus插件，执行下面的安装命令即可：pip install pydotplus。(conda)</p>
</li>
<li><p>第四步是安装ipython的notebook，执行下面的安装命令即可：pip install notebook。</p>
</li>
</ul>
<p>这样环境就搭建好了，有时候python会很笨，仍然找不到graphviz，这时，可以在代码里面加入这一行：
    os.environ["PATH"] += os.pathsep + 'C:/Program Files (x86)/Graphviz2.38/bin/'
注意后面的路径是你自己的graphviz的bin目录。</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="&#20915;&#31574;&#26641;&#30340;&#22522;&#26412;&#20171;&#32461;">&#20915;&#31574;&#26641;&#30340;&#22522;&#26412;&#20171;&#32461;<a class="anchor-link" href="#&#20915;&#31574;&#26641;&#30340;&#22522;&#26412;&#20171;&#32461;">&#182;</a></h2><ul>
<li>决策树用于分类和回归。</li>
<li>其以一种树状的形式实现很多if then决策问题。</li>
</ul>
<p>方法：</p>
<ul>
<li>首先用"最好"的变量构成if 条件作为树的根</li>
<li>然后将训练集继续分割，每次使用一个变量</li>
<li>重复上述过程直到得到满意的叶子结点。 </li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="&#21010;&#20998;">&#21010;&#20998;<a class="anchor-link" href="#&#21010;&#20998;">&#182;</a></h2><ul>
<li>决策树将样本空间分割为很多小的子集。分割的目的是使得每个子集中的样本性质更加一致，即具有相同的类别或相近的目标取值。 </li>
<li>如何分割：连续变量，离散变量</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="&#21010;&#20998;&#20934;&#21017;">&#21010;&#20998;&#20934;&#21017;<a class="anchor-link" href="#&#21010;&#20998;&#20934;&#21017;">&#182;</a></h2><ul>
<li>选择什么变量？
如果变量包含了n个变量，在根节点，或者在任何一个结点，选择哪个变量其实是很复杂的。如果只是随机的选择，结果可能会比较差。</li>
<li>例如利用变量分割</li>
<li>遵循什么法则<ul>
<li>Information gain,信息增益，基于信息熵的准则。  <ul>
<li>熵(Entropy)用来度量一个随机变量的随机性或者说不确定性。<br>
对于一个两分类问题（正负），如果所有样本都是正或者都是负，熵为0，确定性最高，熵最低；<br>
如果有一半是正的，一半是负的，则熵为1，随机性最高，熵最高。<br>
熵的定义为：
$$H(X)=-\sum_{x\in \mathbb{X}}p(x)\log_2 p(x)$$     </li>
</ul>
</li>
<li>Gini index，基尼指数准则<ul>
<li>记分类变量 Y的水平数为$|Y|$，$p_k=P(Y=k)$
$$\mbox{Gini index}=\sum_{k=1}^{|Y|}\sum_{k'\neq k}p_kp_{k'}=1-\sum_{j}p_j^2$$</li>
<li>直观反映从数据中随机抽取两个样本，其类别标记$Y$的取值不一致的概率。上述值越小，数据类别的纯度越高。</li>
</ul>
</li>
</ul>
</li>
</ul>

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
<span class="o">%</span><span class="k">matplotlib</span> inline
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="n">A</span><span class="o">=</span><span class="p">[</span><span class="mf">4.8</span><span class="p">,</span><span class="mi">5</span><span class="p">,</span><span class="mi">5</span><span class="p">,</span><span class="mf">5.2</span><span class="p">,</span><span class="mf">5.2</span><span class="p">,</span><span class="mf">4.7</span><span class="p">,</span><span class="mf">4.8</span><span class="p">,</span><span class="mf">5.4</span><span class="p">,</span><span class="mi">7</span><span class="p">,</span><span class="mf">6.4</span><span class="p">,</span><span class="mf">6.9</span><span class="p">,</span><span class="mf">5.5</span><span class="p">,</span><span class="mf">6.5</span><span class="p">,</span><span class="mf">5.7</span><span class="p">,</span><span class="mf">6.3</span><span class="p">,</span><span class="mf">4.9</span><span class="p">]</span>
<span class="n">B</span><span class="o">=</span><span class="p">[</span><span class="mf">3.4</span><span class="p">,</span><span class="mi">3</span><span class="p">,</span><span class="mf">3.4</span><span class="p">,</span><span class="mf">3.5</span><span class="p">,</span><span class="mf">3.4</span><span class="p">,</span><span class="mf">3.2</span><span class="p">,</span><span class="mf">3.2</span><span class="p">,</span><span class="mf">3.4</span><span class="p">,</span><span class="mf">3.2</span><span class="p">,</span><span class="mf">3.2</span><span class="p">,</span><span class="mf">3.1</span><span class="p">,</span><span class="mf">2.3</span><span class="p">,</span><span class="mf">2.8</span><span class="p">,</span><span class="mf">2.8</span><span class="p">,</span><span class="mf">3.3</span><span class="p">,</span><span class="mf">2.4</span><span class="p">]</span>
<span class="n">C</span><span class="o">=</span><span class="p">[</span><span class="mf">1.9</span><span class="p">,</span><span class="mf">1.6</span><span class="p">,</span><span class="mf">1.6</span><span class="p">,</span><span class="mf">1.5</span><span class="p">,</span><span class="mf">1.4</span><span class="p">,</span><span class="mf">1.6</span><span class="p">,</span><span class="mf">1.6</span><span class="p">,</span><span class="mf">1.5</span><span class="p">,</span><span class="mf">4.7</span><span class="p">,</span><span class="mf">4.5</span><span class="p">,</span><span class="mf">4.9</span><span class="p">,</span><span class="mi">4</span><span class="p">,</span><span class="mf">4.6</span><span class="p">,</span><span class="mf">4.5</span><span class="p">,</span><span class="mf">4.7</span><span class="p">,</span><span class="mf">3.3</span><span class="p">]</span>
<span class="n">D</span><span class="o">=</span><span class="p">[</span><span class="mf">0.2</span><span class="p">,</span><span class="mf">0.2</span><span class="p">,</span><span class="mf">0.4</span><span class="p">,</span><span class="mf">0.2</span><span class="p">,</span><span class="mf">0.2</span><span class="p">,</span><span class="mf">0.2</span><span class="p">,</span><span class="mf">0.2</span><span class="p">,</span><span class="mf">0.4</span><span class="p">,</span><span class="mf">1.4</span><span class="p">,</span><span class="mf">1.5</span><span class="p">,</span><span class="mf">1.5</span><span class="p">,</span><span class="mf">1.3</span><span class="p">,</span><span class="mf">1.5</span><span class="p">,</span><span class="mf">1.3</span><span class="p">,</span><span class="mf">1.6</span><span class="p">,</span><span class="mi">1</span><span class="p">]</span>
<span class="n">cols</span><span class="o">=</span><span class="p">[</span><span class="s2">&quot;red&quot;</span><span class="p">]</span><span class="o">*</span><span class="mi">8</span><span class="o">+</span><span class="p">[</span><span class="s2">&quot;blue&quot;</span><span class="p">]</span><span class="o">*</span><span class="mi">8</span>
<span class="n">E</span><span class="o">=</span><span class="p">[</span><span class="s2">&quot;positive&quot;</span><span class="p">]</span><span class="o">*</span><span class="mi">8</span><span class="o">+</span><span class="p">[</span><span class="s2">&quot;negative&quot;</span><span class="p">]</span><span class="o">*</span><span class="mi">8</span>
<span class="n">data</span><span class="o">=</span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">([</span><span class="n">A</span><span class="p">,</span><span class="n">B</span><span class="p">,</span><span class="n">C</span><span class="p">,</span><span class="n">D</span><span class="p">,</span><span class="n">E</span><span class="p">])</span><span class="o">.</span><span class="n">T</span>
<span class="n">data</span><span class="o">.</span><span class="n">columns</span><span class="o">=</span> <span class="p">[</span><span class="s2">&quot;A&quot;</span><span class="p">,</span><span class="s2">&quot;B&quot;</span><span class="p">,</span><span class="s2">&quot;C&quot;</span><span class="p">,</span><span class="s2">&quot;D&quot;</span><span class="p">,</span><span class="s2">&quot;E&quot;</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[2]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">data</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[2]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
      <th>E</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>4.8</td>
      <td>3.4</td>
      <td>1.9</td>
      <td>0.2</td>
      <td>positive</td>
    </tr>
    <tr>
      <th>1</th>
      <td>5</td>
      <td>3</td>
      <td>1.6</td>
      <td>0.2</td>
      <td>positive</td>
    </tr>
    <tr>
      <th>2</th>
      <td>5</td>
      <td>3.4</td>
      <td>1.6</td>
      <td>0.4</td>
      <td>positive</td>
    </tr>
    <tr>
      <th>3</th>
      <td>5.2</td>
      <td>3.5</td>
      <td>1.5</td>
      <td>0.2</td>
      <td>positive</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5.2</td>
      <td>3.4</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>positive</td>
    </tr>
    <tr>
      <th>5</th>
      <td>4.7</td>
      <td>3.2</td>
      <td>1.6</td>
      <td>0.2</td>
      <td>positive</td>
    </tr>
    <tr>
      <th>6</th>
      <td>4.8</td>
      <td>3.2</td>
      <td>1.6</td>
      <td>0.2</td>
      <td>positive</td>
    </tr>
    <tr>
      <th>7</th>
      <td>5.4</td>
      <td>3.4</td>
      <td>1.5</td>
      <td>0.4</td>
      <td>positive</td>
    </tr>
    <tr>
      <th>8</th>
      <td>7</td>
      <td>3.2</td>
      <td>4.7</td>
      <td>1.4</td>
      <td>negative</td>
    </tr>
    <tr>
      <th>9</th>
      <td>6.4</td>
      <td>3.2</td>
      <td>4.5</td>
      <td>1.5</td>
      <td>negative</td>
    </tr>
    <tr>
      <th>10</th>
      <td>6.9</td>
      <td>3.1</td>
      <td>4.9</td>
      <td>1.5</td>
      <td>negative</td>
    </tr>
    <tr>
      <th>11</th>
      <td>5.5</td>
      <td>2.3</td>
      <td>4</td>
      <td>1.3</td>
      <td>negative</td>
    </tr>
    <tr>
      <th>12</th>
      <td>6.5</td>
      <td>2.8</td>
      <td>4.6</td>
      <td>1.5</td>
      <td>negative</td>
    </tr>
    <tr>
      <th>13</th>
      <td>5.7</td>
      <td>2.8</td>
      <td>4.5</td>
      <td>1.3</td>
      <td>negative</td>
    </tr>
    <tr>
      <th>14</th>
      <td>6.3</td>
      <td>3.3</td>
      <td>4.7</td>
      <td>1.6</td>
      <td>negative</td>
    </tr>
    <tr>
      <th>15</th>
      <td>4.9</td>
      <td>2.4</td>
      <td>3.3</td>
      <td>1</td>
      <td>negative</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="&#29992;-Gini-index-&#31034;&#33539;">&#29992; Gini index &#31034;&#33539;<a class="anchor-link" href="#&#29992;-Gini-index-&#31034;&#33539;">&#182;</a></h2><div style="float:left;border:solid 1px 000;margin:15px;"><img src="treedata.png"  width="400" height="520" ></div><ul>
<li><p>利用左边数据，我们使用Gini准则来生成决策树。</p>
<p>$\mbox{Gini index}=1-\sum_{j}p_j^2$</p>
</li>
<li>四个变量数据是连续型，最后一个两值变量是我们的分类目标。</li>
<li>假设我们在这个例子根据给定的值进行了如下离散化：</li>
</ul>
<table>
<thead><tr>
<th>A</th>
<th>B</th>
<th>C</th>
<th>D</th>
</tr>
</thead>
<tbody>
<tr>
<td>$\ge$ 5</td>
<td>$\ge$  3.0</td>
<td>$\ge$ 4.2</td>
<td>$\ge$  1.4</td>
</tr>
<tr>
<td>&lt; 5</td>
<td>&lt; 3.0</td>
<td>&lt; 4.2</td>
<td>&lt; 1.4</td>
</tr>
</tbody>
</table>
<ul>
<li>决策树算法中，我们可以遍历可能的分割点</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<div style="float:left;border:solid 1px 000;margin:15px;"><img src="treedata.png"  width="400" height="820" ></div><p>计算变量A的Gini Index，首先给出列联表</p>
<table>
<thead><tr>
<th>.</th>
<th>正</th>
<th>负    </th>
</tr>
</thead>
<tbody>
<tr>
<td>$A\ge$ 5</td>
<td>5</td>
<td>7 </td>
</tr>
<tr>
<td>A&lt; 5</td>
<td>3</td>
<td>1</td>
</tr>
</tbody>
</table>
<ul>
<li><p>For Var A $\ge$ 5 &amp; class == positive: 5/12</p>
</li>
<li><p>For Var A $\ge$ 5 &amp; class == negative: 7/12
   $$gini(5,7) = 1- ( (5/12)^2 + (7/12)^2 ) = 0.4860$$</p>
</li>
<li><p>For Var A &lt;5 &amp; class == positive: 3/4</p>
</li>
<li><p>For Var A &lt;5 &amp; class == negative: 1/4
   $$gini(3,1) = 1- ( (3/4)^2 + (1/4)^2 ) = 0.375$$<br>
A 的gini index 为 两部分的加权：
$$\begin{array}{ll}gini(Target,A)=&amp;(12/16)*(0.486)\\&amp;+(4/16)*(0.375)={\color{red}{0.45825}}\\\end{array}$$</p>
</li>
<li>同理，我们可以得到：
$$\begin{array}{rl}gini(Target,B)=&amp;{\color{red}{0.3345}}\\\end{array}$$
$$\begin{array}{rl}gini(Target,C)=&amp;{\color{red}{0.2}}\\\end{array}$$
$$\begin{array}{rl}gini(Target,D)=&amp;{\color{red}{0.273}}\\\end{array}$$</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">data</span><span class="p">[</span><span class="s2">&quot;D&quot;</span><span class="p">],</span><span class="n">data</span><span class="p">[</span><span class="s2">&quot;C&quot;</span><span class="p">],</span><span class="n">c</span><span class="o">=</span><span class="n">cols</span><span class="p">)</span> 
<span class="n">plt</span><span class="o">.</span><span class="n">xlim</span><span class="o">=</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span><span class="mi">2</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">2</span><span class="p">],[</span><span class="mf">4.2</span><span class="p">,</span><span class="mf">4.2</span><span class="p">])</span> 
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s2">&quot;D&quot;</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s2">&quot;C&quot;</span><span class="p">)</span>
<span class="c1">#C,D都可以完全区分样本的类别。</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[3]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Text(0,0.5,&#39;C&#39;)</pre>
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
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn</span> <span class="k">import</span> <span class="n">tree</span>
<span class="kn">import</span> <span class="nn">pydotplus</span>
<span class="o">%</span><span class="k">matplotlib</span> inline
<span class="kn">from</span> <span class="nn">IPython.display</span> <span class="k">import</span> <span class="n">Image</span>
<span class="n">clf</span> <span class="o">=</span> <span class="n">tree</span><span class="o">.</span><span class="n">DecisionTreeClassifier</span><span class="p">()</span>
<span class="n">clf</span> <span class="o">=</span> <span class="n">clf</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">data</span><span class="p">[[</span><span class="s2">&quot;A&quot;</span><span class="p">,</span><span class="s2">&quot;B&quot;</span><span class="p">,</span><span class="s2">&quot;C&quot;</span><span class="p">,</span><span class="s2">&quot;D&quot;</span><span class="p">]],</span> <span class="n">data</span><span class="p">[[</span><span class="s2">&quot;E&quot;</span><span class="p">]])</span>

<span class="c1">##注意：</span>
<span class="n">dot_data</span> <span class="o">=</span> <span class="n">tree</span><span class="o">.</span><span class="n">export_graphviz</span><span class="p">(</span><span class="n">clf</span><span class="p">,</span> <span class="n">out_file</span><span class="o">=</span><span class="s2">&quot;temptree.dot&quot;</span><span class="p">,</span> <span class="n">feature_names</span><span class="o">=</span><span class="p">[</span><span class="s2">&quot;A&quot;</span><span class="p">,</span><span class="s2">&quot;B&quot;</span><span class="p">,</span><span class="s2">&quot;C&quot;</span><span class="p">,</span><span class="s2">&quot;D&quot;</span><span class="p">],</span>
                                <span class="n">class_names</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">unique</span><span class="p">(</span><span class="n">data</span><span class="p">[[</span><span class="s2">&quot;E&quot;</span><span class="p">]]),</span>
                                <span class="n">filled</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">rounded</span><span class="o">=</span><span class="kc">True</span><span class="p">,)</span>


<span class="n">dot_file</span><span class="o">=</span><span class="sa">r</span><span class="s1">&#39;.\temptree.dot&#39;</span>
<span class="n">graph</span> <span class="o">=</span> <span class="n">pydotplus</span><span class="o">.</span><span class="n">graph_from_dot_file</span><span class="p">(</span><span class="n">dot_file</span><span class="p">)</span>  
<span class="n">Image</span><span class="p">(</span><span class="n">graph</span><span class="o">.</span><span class="n">create_png</span><span class="p">())</span>

<span class="c1">##</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[5]:</div>




<div class="output_png output_subarea output_execute_result">
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
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span>tree.export_graphviz<span class="o">?</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#预测分类,</span>
<span class="n">clf</span><span class="o">.</span><span class="n">predict</span><span class="p">([[</span><span class="mf">2.</span><span class="p">,</span> <span class="mf">2.</span><span class="p">,</span><span class="mf">2.</span><span class="p">,</span><span class="mi">2</span><span class="p">]])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[7]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([&#39;negative&#39;], dtype=object)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1">#预测概率</span>
<span class="n">clf</span><span class="o">.</span><span class="n">predict_proba</span><span class="p">([[</span><span class="mf">2.</span><span class="p">,</span> <span class="mf">2.</span><span class="p">,</span><span class="mi">2</span><span class="p">,</span><span class="mi">2</span><span class="p">]])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[8]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([[1., 0.]])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>对上述样本，C和D做分割会得到不同的预测。</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>下面看一个复杂一点的例子。</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[9]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.datasets</span> <span class="k">import</span> <span class="n">load_iris</span>

<span class="n">iris</span> <span class="o">=</span> <span class="n">load_iris</span><span class="p">()</span>
<span class="n">clf</span> <span class="o">=</span> <span class="n">tree</span><span class="o">.</span><span class="n">DecisionTreeClassifier</span><span class="p">()</span>
<span class="n">clf</span> <span class="o">=</span> <span class="n">clf</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">iris</span><span class="o">.</span><span class="n">data</span><span class="p">,</span> <span class="n">iris</span><span class="o">.</span><span class="n">target</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[10]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">iris</span><span class="o">.</span><span class="n">target</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[10]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,
       0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,
       0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1,
       1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1,
       1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2,
       2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2,
       2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2])</pre>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">dot_data</span> <span class="o">=</span> <span class="n">tree</span><span class="o">.</span><span class="n">export_graphviz</span><span class="p">(</span><span class="n">clf</span><span class="p">,</span> <span class="n">out_file</span><span class="o">=</span><span class="s2">&quot;temptree.dot&quot;</span><span class="p">,</span>
                                <span class="n">feature_names</span><span class="o">=</span><span class="n">iris</span><span class="o">.</span><span class="n">feature_names</span><span class="p">,</span>
                                <span class="n">class_names</span><span class="o">=</span><span class="n">iris</span><span class="o">.</span><span class="n">target_names</span><span class="p">,</span>
                                <span class="n">filled</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">rounded</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span>
                                <span class="n">special_characters</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>


<span class="n">dot_file</span><span class="o">=</span><span class="sa">r</span><span class="s1">&#39;.\temptree.dot&#39;</span>
<span class="n">graph</span> <span class="o">=</span> <span class="n">pydotplus</span><span class="o">.</span><span class="n">graph_from_dot_file</span><span class="p">(</span><span class="n">dot_file</span><span class="p">)</span>  
<span class="n">Image</span><span class="p">(</span><span class="n">graph</span><span class="o">.</span><span class="n">create_png</span><span class="p">())</span>
<span class="c1">#写到pdf文件</span>
<span class="c1">#graph.write_pdf(&quot;iris1.pdf&quot;)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[11]:</div>




<div class="output_png output_subarea output_execute_result">
<img src="data:image/png;base64,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vaZly5b1S7uBkGxu+15FIpHY8b1kEt0fu39bW1vs+J4ktba2avbs2XK73UmPKiaLqbffw1Dwhz/8QVdccUVa9xMAAJzATikAANCjyZMna+7cudq1a5fToaS0ZMkSSdL69esVjUYlSXV1dTIMQyUlJT32b21tlXQiEVJZWdnt85KSEhmGoebmZkknaiidf/75vW43ENKde/I20qQAACAASURBVOXKlZKkyspKdXR0xK4Hg0EZhqGqqqpufex72rm/z+dTe3u7pBPJppqaGknSihUrMo7J1tP3MBTt2rVLc+fOJSEFAEAm+uEJfgAAYBTweDzW3LlznQ6jR6ZpWpK6vUKhUKyNfc3m9/sT9rFfLS0tlmVZVlNTU9I2Xq83Nl667QZCJnN7PJ6E7UzTtA4ePBhr1/meut3uHvt7PJ5exZTu9zAUzZ071yorK3M6DAAAhhWSUgAAIC2vv/66NXbsWOvpp592OpSUIpGI5fV64xIkXZMZXZNSlmUl7BMKhbolTkKhUFwyxuPxWPX19d3iSLfdQMhkbr/fb7nd7rgkUeeElD2e3cY0zW797aSVaZqW3+/vU0zpfg9DydNPP22NHTvWev31150OBQCAYYWaUgAAIG1ut1utra0KBoNOhwIMGbm5uZo1a5aqq6udDgUAgGGFpBQAAEjbW2+9pVmzZsnn8+n66693OhzAcVu2bFFRUZFaW1t58h4AABmi0DkAAEjbWWedpV/84hf67ne/q/379zsdDuCo/fv367vf/a5+8YtfkJACAKAX2CkFAAAycuzYMV155ZV66623tGvXLp42hlEpGo3qsssu01lnnaUnn3xS48aNczokAACGHXZKAQCAjIwbN06PPvqojhw5omuvvVbvv/++0yEBg+r999/XtddeqyNHjujRRx8lIQUAQC+RlAIAABlzuVx64okn1NLSosWLF6u9vd3pkIBB0d7ersWLF6ulpUVPPPEEOwUBAOgDklIAAKBXzj//fO3Zs0cTJkzQggUL1NDQ4HRIwIBqaGjQggULNGHCBO3Zs0fnn3++0yEBADCskZQCAAC9ds4552jnzp1aunSpVqxYoauvvlqvvfaa02EB/eq1117T1VdfrRUrVmjp0qXauXOnzjnnHKfDAgBg2CMpBQAA+uTUU09VbW2tduzYofb2dl144YX6+te/rm3btunw4cNOhwf0yuHD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sIMRAgCA3iIpBQAAhr2nnnpK99xzj+666y6de+65ToeDfnbuuefq7rvv1j333KNt27bpm9/8pq655ppY8vHpp592OEIAANAbHN8DAADD2gcffKCcnBxdeOGFqq+vdzocDKBFixYpFArp448/1kcffSRJmjBhgkpLS3XHHXc4HB0AAMgUO6UAAMCwdtttt+nQoUPyer1Oh4IB8v7776uoqEjNzc06evRoLCElSUePHtV//Md/OBgdAADoLXZKAQCAYauxsVGXX365amtrlZ+f73Q4GADBYFCFhYV666234pJRnY0ZM0bvvPOOJk2aNMjRAQCAviApBQAAhqX33ntPc+fO1fz587V582anw8EA+PDDD3XKKaf02M4wDD322GO65pprBiEqAADQXzi+BwAAhqVbb71Vhw8f1q9//WunQ8EAOfnkk/Xggw/qlFNO0fjx45O2Gz9+vLZv3z6IkQEAgP7ATikAADDsNDQ0aMWKFXrkkUd03XXXOR0OBtirr76qa6+9Vi0tLTp27FjCNueff75effXVQY4MAAD0BUkpAAAwrBw6dEif//zn9X/+z//Rpk2bnA4Hg+Tw4cNau3atfv3rX8swDCX6FfbAgQM6++yzHYgOAAD0Bsf3AADAkPTSSy/pt7/9rY4fPx53/aabbpJlWVq/fr1DkcEJJ510ku699149/PDDCY/zjRkzRsFg0KHoAABAb5CUAgAAQ9K1116rwsJCfeUrX9H+/fslSY8//rhqamrk8/l05plnOhwhnLBy5Urt3btXF110kcaOHRu7PmbMGP3hD39wMDIAAJApju8BAIAh5/jx45o8ebLee+89jR8/XuPGjVN5ebkqKyu1fPly/eY3v3E6RDjsyJEjuu2223TPPffIMAwdP35cU6dO1cGDB50ODQAApImkFAAAGHJeeOEFXXLJJXHXDMPQWWedpR07dujCCy90KDIMNY8//ri++c1v6v3335ck7du3T7Nnz3Y4KgAAkI5xTgcAAADQ1fbt2zV+/Hh99NFHsWuWZenQoUOaP3++1q9fr+985zsORjj8vP3229qxY4fC4bDefPPNWBJnJPjKV76i3bt3KxKJ6Prrr9ecOXOcDgmDbMyYMZo8ebJmzpypL33pS7r00ks1YcIEp8MCAPSAnVIAAGDIufzyyxUMBrsVObcZhqHLLrtMdXV1mj59+iBHN3wcO3ZMDz30kLxer3bv3q0xY8bowgsv1Kc//WmdccYZTofXr44fP659+/bp7LPP1qRJk5wOB4Ps+PHjOnTokP7yl7+ora1NZ5xxhr72ta/pBz/4gebNm+d0eACAJEhKAQCAIeXIkSNyuVw6cuRIj21/85vfsGMqif/8z//UmjVr1NLSouuuu07f+ta3tHTpUp100klOhwYMqP/+7/9WfX29vF6vnn/+eeXn56uqqooENgAMQTx9DwAADCnPPPNMyoTUuHHjNH78eN1111369re/PXiBDRP/8z//o1WrVmnp0qXKysrSyy+/rLq6Oi1fvpyEFEaFT3/60youLtazzz6rRx55RM8884xmzZolr9frdGgAgC6oKQUAAIaU7du3a8KECTp69Gi3z8aPH69p06bpscce0xe/+EUHohvaDhw4oGuuuUYHDhzQtm3btHz5cqdDAhx17bXX6qqrrtK6detUUlKiffv26V//9V81duxYp0MDAIjjewAAYIiZP3++/vSnP3W7bhiGrr32Wv3mN7+Ry+VyILKh7bXXXtOSJUs0ZcoU/e53v1NWVpbTIQFDymOPPabCwkJdddVVeuihh0hMAcAQQFIKAAAMGe+9957OPPNMffzxx7Fr48aNk2EYuuuuu/S9733PweiGrmg0qvnz5+ucc87R1q1bdfrppzsdEjAkPffcc1q+fLlWrlype++91+lwAGDUo6YUAAAYMp566qluCalzzz1Xe/bsISGVxLFjx3Tddddp4sSJeuyxxxxJSLW3t/eqn2EYMgyjn6PJbNxEbbuup7/iDIfD8vl8fR4nXT6fT+FweNDm6ywQCGR0z+x7nOqVbvtU5s2bp4ceekgbN25UdXV1r9YGAOg/JKUAAMCQ0djYqPHjx0s68ZfOlStXKhwOKycnx+HIhq5f//rX2rt3r7Zu3erIscaqqirNmDFj0OcdKAO1nvb2dpWVlemGG27o97GTueGGG5STk9PrpGFvhcNh5eXl9euYpmnG/tzX9SxdulRer1e33HKL9u/f39fQAAB9wPE9AAAwZLhcLr333nuaOHGi7rnnHhUXFzsd0pD21ltvadasWfL5fLr++usdicHemdKbXyn70re/dI0hUUz9EWdJSYlWrlyp3NzcXo/RG8FgUJs3b9aGDRt6PUY4HNb27du1du3aHts2Nzdr0aJFsfd9/W7tpHRLS4tm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beDm5gY3NzepQxGFhIQgLi4OERERWLBggdThkIGGDh2KqVOnolevXti6dWujSEwREVHTw6QUEREREUli7dq1eP/99/HFF18wIdXETJw4EXv27MHUqVMhk8mwdetWyGQyqcMiIqImhkkpIiIiImpw69evx7vvvouNGzdi0aJFUodDJnjxxRc1ElORkZFMTBERkVGYlCIiIiKiBrVp0yYsX74c69evx9///nepw6E6mDRpEvbs2YNXXnkFFhYW+Pe//83EFBERGYxJKSIiIiJqMFu2bMGyZcuwdu1aLFu2TOpwyAwmT56MuLg4TJ8+HZaWltiyZQsTU0REZBAmpYiIiIioQURERODNN99ESEgI3n77banDITOSy+X4v//7P/zlL3+BpaUlNm/ezMQUERHVikkpIiIiIqp3X331FQICArB69Wr84x//kDocqgdTp05FTEwMfH19YWFhgU2bNjExRURENWJSioiIiIjq1bZt27Bw4UKsWrUKq1evljocqkfTpk1DdHS0mJjasGEDE1NERKQXk1JEREREVG927NiBBQsW4O2338aHH34odTjUAF599VUxMSWTybBhwwapQyIiokaKSSkiIiIiqhe7du3C3LlzsXTpUnz88cdSh0MNaPr06VCpVGJiav369VKHREREjRCTUkRERERkdnFxcZg1axYWL16M0NBQqcMhCcyYMQMqlQqzZs2CpaUlPvvsM6lDIiKiRoZJKSIiIiIyqz179mD27NkIDAxkhUwLN3PmTDx+/Bhz5syBpaUlPvnkE6lDIiKiRoRJKSIiIiIym++++w4+Pj6YP38+Pv/8cza5JsyaNQuVlZWYN28eLCws8NFHH0kdEhERNRJMShERERGRWezfvx+vvvoq/Pz8sGXLFiakSPTaa6+hsrIS8+fPh4WFBUJCQqQOiYiIGgEmpYiIiIiozuLj4zFt2jTMnj0bERERTEiRljlz5qCyshILFiyAhYUF1qxZI3VIREQkMSaliIiIiKhODhw4gFdeeQUzZsxAZGQkLCwspA6JGql58+ZBpVKJiakPPvhA6pCIiEhCTEoRERERkcmSk5MxZcoUyOVy/Oc//4GlpaXUIVEj99e//lUjMfX+++9LHRIREUmESSkiIiIiMsnhw4fx0ksv4aWXXsKOHTuYkCKDzZ8/HxUVFXj99ddhaWmJf/7zn1KHREREEmBSioiIiIiMdvToUbz00kuYOHEiE1JkEn9/f1RWViIwMBAWFhZ47733pA6JiIgaGJNSRERERGSU1NRUTJ48GePGjUNMTAxat24tdUjURL3++uuorKzEG2+8AQsLC7zzzjtSh0RERA2ISSkiIiIiMtiJEycwYcIEPPfcc4iNjUWbNm2kDomauMDAQFRWVmLx4sWwsLDA22+/LXVIRETUQJiUIiIiIiKDnD59GhMmTMCoUaOwe/duJqTIbN544w1UVlZiyZIlsLCwwPLly6UOiYiIGgCTUkRERERUq/T0dEyYMAHPPvssdu/eDSsrK6lDomZm8eLFqKysxNKlS2FpaYmlS5dKHRIREdUzJqWIiIiIqEbnzp2Dl5cXBg0ahL179+LJJ5+UOiRqppYsWYLKykq89dZbkMlkWLJkidQhERFRPWJSioiIiIj0unDhAjw9PdGvXz98//33TEhRvVu2bBkqKyuxbNkyWFhYYPHixVKHRERE9YRJKSIiIiLSKTMzE56enujTpw9++OEHJqSowSxfvlyjx9Qbb7whdUhERFQPmJQiIiIiIi2XL1+Gp6cnevToge+//x7t2rWTOiRqYd5++22Np/IFBgZKHRIREZkZk1JEREREpCE7Oxvjxo2Dk5MTfvzxR9ja2kodErVQ77zzDiorK/HGG2/AwsICr7/+utQhERGRGTEpRURERESia9euYdy4cXBwcEB8fDwTUiS59957DxUVFQgMDISlpSUWLFggdUhERGQmTEoREREREQDg+vXr8PDwgJ2dHeLj49GhQwepQyICAAQFBaGiogILFy6EhYUF5s+fL3VIRERkBkxKERERERFu3LiBcePGoV27dkhISECnTp2kDolIw+rVq6FSqeDv7w+ZTIa//vWvUodERER1xKQUERERUQt38+ZNeHh4wMrKComJiejcubPUIRHp9MEHH6CyslJMTM2bN0/qkIiIqA6YlCIiIiJqwfLz8+Hp6QlLS0smpKhJWLNmDSorK7FgwQJYWFhgzpw5UodEREQmspA6ACIiIiKqX6tXr4a/vz8ePXqkcfzu3bvw8PBARUUFEhMT0aVLF4kiJDJOSEgIVq5cifnz52P79u1a7x86dAi+vr5aP/NERNS4sFKKiIiIqBl79OgR1qxZAwDIy8vD3r170aZNG9y9exeenp54+PAhfv75Zzg5OUkcKZFxPvro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3HfffQCA48eP4/vvv8fkyZMljoyIiIj6o0GDBuHFF1/EqVOnUF1dDW9vb+zevVvqsIj6BCaliIioX8jMzMT//d//wc/PD9euXUNCQgISExMREBAgdWhEREQ0AHh6euLUqVMIDw9HWFgYwsPDUV1dLXVYRL0ak1JERNSnZWdnY9GiRfD29salS5ewf/9+/PLLL5g1a5bUoREREdEAY2pqik8//RQHDhxAXFwcfH198csvv0gdFlGvxaQUERH1SQUFBXjmmWfg4eGB1NRU7N69G2fOnMHcuXOlDo2IiIgGuDlz5iAjIwOurq4ICAjAu+++i19//VXqsIh6HSaliIioTykuLsbLL78Md3d3HDlyBP/4xz9w7tw5hIaG4o47+L81IiIi6h3s7e0RFxeH999/H2vXrsXMmTNx5coVqcMi6lX4t3ciIuoTVCoVVqxYATc3N+zduxfR0dFQKpWIiIiAkZGR1OERERERaRk0aBBee+01JCcno7S0FN7e3vj222+lDouo12BSioiIerXr16/j7bffhqurK/75z39i3bp1yM7ORmRkJAYPHix1eERERERt8vHxQWpqKhYuXIiQkBA8/fTTqKmpkTosIskxKUVERL1STU0N1q9fDxcXF3z88cd44403kJubi2XLlmHIkCFSh0dERETULkOHDsUXX3yBb7/9Fvv27cOkSZOQmpoqdVhEkmJSioiIepX6+np88skncHV1xbp16/D8888jLy8Pf/7znzFs2DCpwyMiIiLqlAULFiA9PR0ODg7w9/fHxo0bcfv2banDIpIEk1JERNQrNDY24m9/+xvc3d2xcuVKhIWFITc3F++88w4sLS2lDo+IiIioy9x99904fPgw3n77bfzpT3/CH/7wBxQXF0sdFlGPY1KKiIgkdfv2bezYsQMymQwvvfQS5syZg+zsbHz44YcYMWKE1OERERERdYs77rgDq1atwokTJ3D58mV4eXnhwIEDUodF1KOYlCIiIkk0NTVhz5498PLywpIlSxAQEIALFy7g888/h6Ojo9ThEREREfWIKVOmIC0tDXPmzMH8+fPx/PPPo7a2VuqwiHoEk1JERNTjvvvuO0yePBmPPvoo5HI5MjMz8a9//QujR4+WOjQiIiKiHmdubo5//vOf+Oqrr7B7925MmTIFGRkZUodF1O2YlCIioh7z448/Ytq0aZgzZw7u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RESzBiuliIiIiHzE//zP/2DVqlV49tln8b3vfU/scOgmN27cwJ133onr16+jvr4eEolE7JCIiIhmPCaliIiIiHyA1WrFhg0bYLFY0NDQwKSHD2ppacHq1avx05/+FE8++aTY4RAREc143L5HRERE5ANeeeUVNDQ04Je//CUTUj4qOTkZO3bswE9+8hOcO3dO7HCIiIhmPFZKEREREYlMr9dDpVIhPz8fe/bsETscGsPg4CBWrVqFxYsX409/+pPY4RAREc1oTEoRERERieyb3/wmWlpacPr0aQQHB4sdDo2jrq4OGzZsQHl5OXJycsQOh4iIaMZiUoqIiIhIRJWVlcjOzsb777+PjIwMscMhNxUUFKCyshKtra2IjIwUOxwiIqIZiUkpIiIiomlw5coVhIaGOhwzmUxITk7Gpk2b8Ktf/UqkyGgyLl++jOTkZNx999347W9/63Du2rVrsFqtCAoKEik6IiKimYGNzomIiIi87NKlS5DJZFi5cqVDg+yioiLcuHEDL7zwgnjB0aTMnz8fv/jFL1BeXo7q6mr78XfffRdBQUG46667xAuOiIhohmClFBEREZGXvffee9i0aRPmzJmDoKAgPPfcc1i+fDm+9rWv4fe//z2ys7PFDpEmKTs7Gx9//DFqamqwY8cOvPHGG/Zz169f55sUiYiIxsCkFBEREZGX/fjHP8YLL7yAa9euAQDmzJmDqKgoLF26FB988IG4wdGUdHd3IyUlBRaLBUNDQxgaGrKfO3HiBFauXClidERERL6N2/eIiIiIvKympsaekAKAGzduoK+vDx999BF+9KMfwWKxiBgdTVZ7eztycnJgMplw9epVh4TU3Llz8dFHH4kYHRERke9jUoqIiIjIi65du4ampian49evX8fw8DBKSkqgUqmg1WpFiI4m4/r163jxxRfxla98BXV1dbBarRi5+cBqteLDDz8UKUIiIqKZgdv3iIiIiLyorq4Od955p1tjL1++DJlM5uWIaKp+9atf4V//9V/HHRcZGYne3t5piIiIiGhmYqUUERERkRd99NFHCAwMHPW8RCJBYGAgXn31VSakZoj7778fW7duRUBAwJjjjEYj2tvbpykqIiKimYdJKSIiIiIv0mq1GB4ednkuMDAQCxcuxNGjR/HII49Mc2Q0WfPnz8dbb72Fn//855BIJKO+YU8ikbCvFBER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
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
<h2 id="DecisionTreeClassifier">DecisionTreeClassifier<a class="anchor-link" href="#DecisionTreeClassifier">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="scikit-learn-&#20915;&#31574;&#26641;&#31639;&#27861;&#31867;&#24211;">scikit-learn &#20915;&#31574;&#26641;&#31639;&#27861;&#31867;&#24211;<a class="anchor-link" href="#scikit-learn-&#20915;&#31574;&#26641;&#31639;&#27861;&#31867;&#24211;">&#182;</a></h3><p>scikit-learn决策树算法类库内部的实现是使用了调优过的CART树算法，既可以做分类，又可以做回归。分类决策树的类对应的是DecisionTreeClassifier，而回归决策树的类对应的是DecisionTreeRegressor。两者的参数定义几乎完全相同，但是意义不全相同。下面就对DecisionTreeClassifier和DecisionTreeRegressor的重要参数做一个总结，重点比较两者参数使用的不同点和调参的注意点。</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
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
</div>
    </div>
  </div>
</body>

 


</html>
