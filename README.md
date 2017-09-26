# Tensorflow-Image-Tutorial
How to use Tensorflow for image manipulation

{::nomarkdown}

<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />
<title>Playground_Tensorflow</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
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
    color: #000 !important;
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
 *  Font Awesome 4.2.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.2.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.2.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.2.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.2.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.2.0#fontawesomeregular') format('svg');
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
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=1);
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2);
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=3);
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1);
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1);
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
.fa-gittip:before {
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
.fa-pied-piper:before {
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
@media (max-width: 991px) {
  #ipython_notebook {
    margin-left: 10px;
  }
}
[dir="rtl"] #ipython_notebook {
  float: right !important;
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
span#login_widget {
  float: right;
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
  text-align: center;
  vertical-align: middle;
  display: inline;
  opacity: 0;
  z-index: 2;
  width: 12ex;
  margin-right: -12ex;
}
.alternate_upload .btn-upload {
  height: 22px;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
[dir="rtl"] #tabs li {
  float: right;
}
ul#tabs {
  margin-bottom: 4px;
}
[dir="rtl"] ul#tabs {
  margin-right: 0px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
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
[dir="rtl"] .list_toolbar .tree-buttons {
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-right {
  padding-top: 1px;
  float: left !important;
}
[dir="rtl"] .list_toolbar .pull-left {
  float: right !important;
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
  vertical-align: baseline;
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
#tree-selector {
  padding-right: 0px;
}
[dir="rtl"] #tree-selector a {
  float: right;
}
#button-select-all {
  min-width: 50px;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
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
[dir="rtl"] #new-menu {
  text-align: right;
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
[dir="rtl"] #running .col-sm-8 {
  float: right !important;
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
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI colors. */
.ansibold {
  font-weight: bold;
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
  border-left-width: 1px;
  padding-left: 5px;
  background: linear-gradient(to right, transparent -40px, transparent 1px, transparent 1px, transparent 100%);
}
div.cell.jupyter-soft-selected {
  border-left-color: #90CAF9;
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
div.cell.selected {
  border-color: #ababab;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 5px, transparent 5px, transparent 100%);
}
@media print {
  div.cell.selected {
    border-color: transparent;
  }
}
div.cell.selected.jupyter-soft-selected {
  border-left-width: 0;
  padding-left: 6px;
  background: linear-gradient(to right, #42A5F5 -40px, #42A5F5 7px, #E3F2FD 7px, #E3F2FD 100%);
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
  border-left-width: 0px;
  padding-left: 6px;
  background: linear-gradient(to right, #66BB6A -40px, #66BB6A 5px, transparent 5px, transparent 100%);
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
  padding: 0.4em;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. We need the 0 value because of how we size */
  /* .CodeMirror-lines */
  padding: 0;
  border: 0;
  border-radius: 0;
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
  padding: 0;
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
.rendered_html ul {
  list-style: disc;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ul ul {
  list-style: square;
  margin: 0em 2em;
}
.rendered_html ul ul ul {
  list-style: circle;
  margin: 0em 2em;
}
.rendered_html ol {
  list-style: decimal;
  margin: 0em 2em;
  padding-left: 0px;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
  margin: 0em 2em;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
  margin: 0em 2em;
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
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  background-color: #fff;
  color: #000;
  font-size: 100%;
  padding: 0px;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: 1px solid black;
  border-collapse: collapse;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  border: 1px solid black;
  border-collapse: collapse;
  margin: 1em 2em;
}
.rendered_html td,
.rendered_html th {
  text-align: left;
  vertical-align: middle;
  padding: 4px;
}
.rendered_html th {
  font-weight: bold;
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
.text_cell.unrendered .text_cell_render {
  display: none;
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
#kernel_logo_widget {
  float: right !important;
  float: right;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
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
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
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
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
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
  margin-top: 6px;
}
span.save_widget span.filename {
  height: 1em;
  line-height: 1em;
  padding: 3px;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
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
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
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
  display: none;
}
.command-shortcut:before {
  content: "(command)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
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
}

@media print {
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
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS_HTML"></script>
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

<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Image-reshaping-for-Tensorflow">Image reshaping for Tensorflow<a class="anchor-link" href="#Image-reshaping-for-Tensorflow">&#182;</a></h1><p>References:</p>
<ul>
<li><a href="https://www.tensorflow.org/api_docs/python/tf/image/resize_images">https://www.tensorflow.org/api_docs/python/tf/image/resize_images</a> </li>
<li><a href="https://learningtensorflow.com/lesson3/">https://learningtensorflow.com/lesson3/</a></li>
<li><a href="https://stackoverflow.com/questions/39952592/tf-image-decode-jpeg-raise-invalidargumenterror">https://stackoverflow.com/questions/39952592/tf-image-decode-jpeg-raise-invalidargumenterror</a></li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="1.-Plotting-on-a-graph-via-Tensorflow">1. Plotting on a graph via Tensorflow<a class="anchor-link" href="#1.-Plotting-on-a-graph-via-Tensorflow">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">tensorflow</span> <span class="k">as</span> <span class="nn">tf</span>
<span class="kn">import</span> <span class="nn">matplotlib.image</span> <span class="k">as</span> <span class="nn">mpimg</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>

<span class="c1"># First, load the image again</span>
<span class="n">image</span> <span class="o">=</span> <span class="n">mpimg</span><span class="o">.</span><span class="n">imread</span><span class="p">(</span><span class="s2">&quot;jerry.png&quot;</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Type: &quot;</span><span class="p">,</span> <span class="nb">type</span><span class="p">(</span><span class="n">image</span><span class="p">))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Shape: &quot;</span><span class="p">,</span> <span class="nb">type</span><span class="p">(</span><span class="n">image</span><span class="o">.</span><span class="n">shape</span><span class="p">))</span>

<span class="c1"># Create a TensorFlow Variable</span>
<span class="n">x</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">Variable</span><span class="p">(</span><span class="n">image</span><span class="p">,</span> <span class="n">name</span><span class="o">=</span><span class="s1">&#39;x&#39;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;X: &quot;</span><span class="p">,</span> <span class="n">x</span><span class="p">)</span>

<span class="n">model</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">global_variables_initializer</span><span class="p">()</span>

<span class="k">with</span> <span class="n">tf</span><span class="o">.</span><span class="n">Session</span><span class="p">()</span> <span class="k">as</span> <span class="n">session</span><span class="p">:</span>
    <span class="n">session</span><span class="o">.</span><span class="n">run</span><span class="p">(</span><span class="n">model</span><span class="p">)</span>
    <span class="n">result</span> <span class="o">=</span> <span class="n">session</span><span class="o">.</span><span class="n">run</span><span class="p">(</span><span class="n">x</span><span class="p">)</span>
    
<span class="n">plt</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">result</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>

<div class="output_subarea output_stream output_stdout output_text">
<pre>Type:  &lt;class &#39;numpy.ndarray&#39;&gt;
Shape:  &lt;class &#39;tuple&#39;&gt;
X:  &lt;tf.Variable &#39;x:0&#39; shape=(268, 189, 3) dtype=float32_ref&gt;
</pre>
</div>
</div>

<div class="output_area">
<div class="prompt"></div>



<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
DubZlJ9Bfr0AAAAASUVORK5CYII=
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="2.-Reshaping-the-image">2. Reshaping the image<a class="anchor-link" href="#2.-Reshaping-the-image">&#182;</a></h2><p>References:</p>
<ul>
<li><a href="https://www.tensorflow.org/api_docs/python/tf/image/resize_images">https://www.tensorflow.org/api_docs/python/tf/image/resize_images</a> </li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The following code demonstrates how to reduce the resolution of the image by resizing the raw data.</p>
<p>The <strong>set_shape()</strong> method is used as the file_contents does not allow for the decoded png to be read when creating as a tf.Variable.</p>
<p>Other parameters options for the <strong>resize_image()</strong> method include:</p>
<ul>
<li>ResizeMethod.BILINEAR</li>
<li>ResizeMethod.NEAREST_NEIGHBOR (Best human results)</li>
<li>ResizeMethod.BICUBIC</li>
<li>ResizeMethod.AREA</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[24]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">tensorflow</span> <span class="k">as</span> <span class="nn">tf</span>
<span class="kn">import</span> <span class="nn">matplotlib.image</span> <span class="k">as</span> <span class="nn">mpimg</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>

<span class="c1"># First, load the image and graph the shape of the image.</span>
<span class="n">image</span> <span class="o">=</span> <span class="n">mpimg</span><span class="o">.</span><span class="n">imread</span><span class="p">(</span><span class="s2">&quot;jerry.png&quot;</span><span class="p">)</span>
<span class="n">original_shape</span> <span class="o">=</span> <span class="n">image</span><span class="o">.</span><span class="n">shape</span>

<span class="c1"># Read the image using tf&#39;s file reading method</span>
<span class="n">file_contents</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">read_file</span><span class="p">(</span><span class="s2">&quot;jerry.png&quot;</span><span class="p">)</span>
<span class="n">decoded_image</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">image</span><span class="o">.</span><span class="n">decode_png</span><span class="p">(</span><span class="n">file_contents</span><span class="p">,</span> <span class="n">dtype</span><span class="o">=</span><span class="n">tf</span><span class="o">.</span><span class="n">uint8</span><span class="p">,</span> <span class="n">channels</span><span class="o">=</span><span class="mi">3</span><span class="p">)</span>   

<span class="c1"># Set the shape of the image as this is unknown.</span>
<span class="n">decoded_image</span><span class="o">.</span><span class="n">set_shape</span><span class="p">(</span><span class="n">original_shape</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Initial shape: &quot;</span><span class="p">,</span> <span class="n">decoded_image</span><span class="o">.</span><span class="n">get_shape</span><span class="p">())</span>

<span class="c1"># Set a rescale value</span>
<span class="n">rescale_percentage</span> <span class="o">=</span> <span class="mf">0.4</span>
<span class="n">rescaled_row</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="n">original_shape</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="o">*</span> <span class="n">rescale_percentage</span><span class="p">)</span>
<span class="n">rescaled_col</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="n">original_shape</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span> <span class="o">*</span> <span class="n">rescale_percentage</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Rescale percentage: &quot;</span><span class="p">,</span> <span class="n">rescale_percentage</span> <span class="o">*</span> <span class="mi">100</span><span class="p">,</span> <span class="s2">&quot;%&quot;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Rescaled image to contain </span><span class="si">%s</span><span class="s2"> rows and </span><span class="si">%s</span><span class="s2"> columns&quot;</span> <span class="o">%</span> <span class="p">(</span><span class="n">rescaled_row</span><span class="p">,</span> <span class="n">rescaled_col</span><span class="p">))</span>

<span class="n">resize_shape</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">stack</span><span class="p">([</span><span class="n">rescaled_row</span><span class="p">,</span><span class="n">rescaled_col</span><span class="p">])</span>
<span class="n">resized_image</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">image</span><span class="o">.</span><span class="n">resize_images</span><span class="p">(</span>
    <span class="n">decoded_image</span><span class="p">,</span> 
    <span class="n">resize_shape</span><span class="p">,</span>
    <span class="n">method</span><span class="o">=</span><span class="n">tf</span><span class="o">.</span><span class="n">image</span><span class="o">.</span><span class="n">ResizeMethod</span><span class="o">.</span><span class="n">NEAREST_NEIGHBOR</span>
<span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Resized Shape: &quot;</span><span class="p">,</span> <span class="n">resized_image</span><span class="o">.</span><span class="n">get_shape</span><span class="p">())</span>

<span class="c1"># # Create a TensorFlow Variable</span>
<span class="n">x</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">Variable</span><span class="p">(</span><span class="n">decoded_image</span><span class="p">,</span> <span class="n">name</span><span class="o">=</span><span class="s1">&#39;x&#39;</span><span class="p">)</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">Variable</span><span class="p">(</span><span class="n">resized_image</span><span class="p">,</span> <span class="n">name</span><span class="o">=</span><span class="s1">&#39;y&#39;</span><span class="p">)</span>

<span class="n">model</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">global_variables_initializer</span><span class="p">()</span>

<span class="k">with</span> <span class="n">tf</span><span class="o">.</span><span class="n">Session</span><span class="p">()</span> <span class="k">as</span> <span class="n">session</span><span class="p">:</span>
    <span class="n">session</span><span class="o">.</span><span class="n">run</span><span class="p">(</span><span class="n">model</span><span class="p">)</span>
    <span class="n">original</span> <span class="o">=</span> <span class="n">session</span><span class="o">.</span><span class="n">run</span><span class="p">(</span><span class="n">x</span><span class="p">)</span>
    <span class="n">resized</span> <span class="o">=</span> <span class="n">session</span><span class="o">.</span><span class="n">run</span><span class="p">(</span><span class="n">y</span><span class="p">)</span>
        
<span class="n">fig</span><span class="p">,</span> <span class="n">axarr</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">)</span>
<span class="n">axarr</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">original</span><span class="p">)</span>
<span class="n">axarr</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">resized</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>

<div class="output_subarea output_stream output_stdout output_text">
<pre>Initial shape:  (268, 189, 3)
Rescale percentage:  40.0 %
Rescaled image to contain 107 rows and 75 columns
Resized Shape:  (107, 75, 3)
</pre>
</div>
</div>

<div class="output_area">
<div class="prompt"></div>



<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
SUVORK5CYII=
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="3.-Reshape-with-crop-and-pad">3. Reshape with crop and pad<a class="anchor-link" href="#3.-Reshape-with-crop-and-pad">&#182;</a></h3><p>References: <a href="https://www.tensorflow.org/api_docs/python/tf/image/resize_image_with_crop_or_pad">https://www.tensorflow.org/api_docs/python/tf/image/resize_image_with_crop_or_pad</a></p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered">
<div class="prompt input_prompt">
</div>
<div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Use the <strong>resize_image_with_crop_or_pad()</strong> method.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[27]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">tensorflow</span> <span class="k">as</span> <span class="nn">tf</span>
<span class="kn">import</span> <span class="nn">matplotlib.image</span> <span class="k">as</span> <span class="nn">mpimg</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>

<span class="c1"># First, load the image and graph the shape of the image.</span>
<span class="n">image</span> <span class="o">=</span> <span class="n">mpimg</span><span class="o">.</span><span class="n">imread</span><span class="p">(</span><span class="s2">&quot;jerry.png&quot;</span><span class="p">)</span>
<span class="n">original_shape</span> <span class="o">=</span> <span class="n">image</span><span class="o">.</span><span class="n">shape</span>

<span class="c1"># Read the image using tf&#39;s file reading method</span>
<span class="n">file_contents</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">read_file</span><span class="p">(</span><span class="s2">&quot;jerry.png&quot;</span><span class="p">)</span>
<span class="n">decoded_image</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">image</span><span class="o">.</span><span class="n">decode_png</span><span class="p">(</span><span class="n">file_contents</span><span class="p">,</span> <span class="n">dtype</span><span class="o">=</span><span class="n">tf</span><span class="o">.</span><span class="n">uint8</span><span class="p">,</span> <span class="n">channels</span><span class="o">=</span><span class="mi">3</span><span class="p">)</span>   

<span class="c1"># Set the shape of the image as this is unknown.</span>
<span class="n">decoded_image</span><span class="o">.</span><span class="n">set_shape</span><span class="p">(</span><span class="n">original_shape</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Initial shape: &quot;</span><span class="p">,</span> <span class="n">decoded_image</span><span class="o">.</span><span class="n">get_shape</span><span class="p">())</span>

<span class="n">resize_shape</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">stack</span><span class="p">([</span><span class="n">rescaled_row</span><span class="p">,</span><span class="n">rescaled_col</span><span class="p">])</span>
<span class="n">padded_image</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">image</span><span class="o">.</span><span class="n">resize_image_with_crop_or_pad</span><span class="p">(</span>
    <span class="n">decoded_image</span><span class="p">,</span> <span class="mi">400</span><span class="p">,</span> <span class="mi">140</span><span class="p">)</span>

<span class="n">cropped_image</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">image</span><span class="o">.</span><span class="n">resize_image_with_crop_or_pad</span><span class="p">(</span>
    <span class="n">decoded_image</span><span class="p">,</span> <span class="mi">140</span><span class="p">,</span><span class="mi">140</span><span class="p">)</span>

<span class="c1"># # Create a TensorFlow Variable</span>
<span class="n">x</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">Variable</span><span class="p">(</span><span class="n">decoded_image</span><span class="p">,</span> <span class="n">name</span><span class="o">=</span><span class="s1">&#39;x&#39;</span><span class="p">)</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">Variable</span><span class="p">(</span><span class="n">padded_image</span><span class="p">,</span> <span class="n">name</span><span class="o">=</span><span class="s1">&#39;y&#39;</span><span class="p">)</span>
<span class="n">z</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">Variable</span><span class="p">(</span><span class="n">cropped_image</span><span class="p">,</span> <span class="n">name</span><span class="o">=</span><span class="s1">&#39;z&#39;</span><span class="p">)</span>

<span class="n">model</span> <span class="o">=</span> <span class="n">tf</span><span class="o">.</span><span class="n">global_variables_initializer</span><span class="p">()</span>

<span class="k">with</span> <span class="n">tf</span><span class="o">.</span><span class="n">Session</span><span class="p">()</span> <span class="k">as</span> <span class="n">session</span><span class="p">:</span>
    <span class="n">session</span><span class="o">.</span><span class="n">run</span><span class="p">(</span><span class="n">model</span><span class="p">)</span>
    <span class="n">original</span> <span class="o">=</span> <span class="n">session</span><span class="o">.</span><span class="n">run</span><span class="p">(</span><span class="n">x</span><span class="p">)</span>
    <span class="n">padded</span> <span class="o">=</span> <span class="n">session</span><span class="o">.</span><span class="n">run</span><span class="p">(</span><span class="n">y</span><span class="p">)</span>
    <span class="n">cropped</span> <span class="o">=</span> <span class="n">session</span><span class="o">.</span><span class="n">run</span><span class="p">(</span><span class="n">z</span><span class="p">)</span>
    
<span class="n">fig</span><span class="p">,</span> <span class="n">axarr</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">3</span><span class="p">)</span>
<span class="n">axarr</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">original</span><span class="p">)</span>
<span class="n">axarr</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">padded</span><span class="p">)</span>
<span class="n">axarr</span><span class="p">[</span><span class="mi">2</span><span class="p">]</span><span class="o">.</span><span class="n">imshow</span><span class="p">(</span><span class="n">cropped</span><span class="p">)</span>

<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

</div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">
<div class="prompt"></div>

<div class="output_subarea output_stream output_stdout output_text">
<pre>Initial shape:  (268, 189, 3)
</pre>
</div>
</div>

<div class="output_area">
<div class="prompt"></div>



<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAXoAAAD8CAYAAAB5Pm/hAAAABHNCSVQICAgIfAhkiAAAAAlwSFlz
AAALEgAACxIB0t1+/AAAIABJREFUeJzsnXecFOX9x9/fZ2b3+tFBpCgiRcWKFRXBXhARiL3EbtRo
1ERNYjRNoyZqNIldf9aIvUUBFbui2BuKgEqR3q7f7s48398fM7u3e7cHd8BJcT68htudnXnmmXme
+Tzf59seUVUiRIgQIcLGC7OuKxAhQoQIEdoWEdFHiBAhwkaOiOgjRIgQYSNHRPQRIkSIsJEjIvoI
ESJE2MgREX2ECBEibOSIiD5Cm0FEDhaRaSIyQ0QuW9f1iRDhpwqJ/OgjtAVExAG+AQ4A5gLvA8eq
6tR1WrEIEX6CiCT6CG2FXYEZqvqtqiaBccAR67hOESL8JOGu6wpE2GjRA5iT9X0usNvKThCRaHrZ
SqiqrOs6RFj/ERF9hHUKETkTOHNd1yNChI0ZEdFHaCv8APTK+t4z3JcDVb0DuAMiiT5ChLZCpKOP
0FZ4H+gnIn1EJA4cAzy7jusUIcJPEpFEH6FNoKqeiJwHTAQc4B5V/XIdVytChJ8kIvfKCOsNItVN
6xEZYyO0BJHqJkKECBE2ckREHyFChAgbOSKijxAhQoSNHBHRR4gQIcJGjojoI0SIEGEjR0T0ESJE
iLCRIyL6CBEiRNjIERF9hAgRImzkiIg+QoQIETZyREQfIUKECBs5IqKPECFChI0cEdFHiBAhwkaO
iOgjRIgQYSNHRPQRIkSIsJEjIvoIESJE2MgREX2ECBEibOSIiD5ChAgRNnJERB8hQoQIGzmiNWMj
rDFE5HugCvABT1V3FpGOwCPA5sD3wFGqunxd1TFChJ8yIok+wtrCcFXdQVV3Dr9fBkxS1X7ApPB7
hAgR1gEioo/QVjgCuC/8fB8wah3WJUKEnzQioo+wNqDAyyLyoYicGe7rpqrzw88LgG7rpmoRIkSI
dPQR1gb2UtUfRKQr8JKIfJ39o6qqiGi+E8OB4cx8v0WIEGHtQFTzvn8RIqwWROSPQDVwBjBMVeeL
SHfgNVUdsIpzo87YSqiqrOs6RFj/EaluIqwRRKRERMrSn4EDgS+AZ4GTw8NOBp5ZNzWMECFCJNFH
WCOIyBbAU+FXF/ivql4lIp2AR4HewCwC98plqygr6oytRCTRR2gJIqKPsN4gIvrWIyL6CC1BpLqJ
ECFChI0cEdFHiBAhwkaOiOgjRIgQYSNHm/nRi8jBwE2AA9ylqte01bUibBzYabsteHf8dWtcjopi
ibN8ucv5F/+eB8c9RUG77qA1KB4IhP+lz1hFiZI5TBCQYrpsUsKJpx5O7y3KSGFR+fFV5Tf/ZeKP
fs0IGybaRKIXEQf4D3AIsDVwrIhs3RbXihChAYJgcNTFsT4dypM8dP/NXP3nS/nqo/dBBUEQJeB2
lWBjJSSdOc4gGEBQv5bFCyqprbQUOJ0xGEQVUV31mBEhwjpAW6ludgVmqOq3qpoExhHkPokQoQ2h
KBaLD2JxXR/xF3P5xSfw9ZRnmDT+fyAuoVwe0rtkiDy7HLDhrybc0mcIYgxoktv+/RhXXHoLrhbg
YHFQDIpRwsHENGwRIqxDtJXqpgcwJ+v7XGC35g7u3LFcN+/Vpcn+thWOBFBEYsyY+T3GGLbotxXZ
L/malF1dXcXyiiUUFMYBH7veSXpKPkn2h1nLlqhq08bY4CCgMQSL4jNi5FBeeucrHv/vA4w95ucE
eph0W7egccSgvo+Y8JmJAyRZvGgpBxy+I/sfsgexuE/DM428HiOsP1hnuW6yc5z07tGZKROaqvCt
CtomL0wwxVerqCi4JWCK2X3vMXz09ULQpYANX/9QGsvM9/NA08dJRkq0NsU5F5zG25Nf5YxfHEuC
atIS4frg+axZI0+GvIBLT3941rqoz9qHAh7p9lOpZ9iQrXnvg2k88tCdHH3cqWBiiCaxCIg2SPg5
EJBY8MkRoICGfhAMlrvvchglRXFSdj6oEvk4RFjf0FY98gegV9b3nuG+DFT1DlXdWVV37typHF9N
k61tSB6CKb4PxiKiGKoRfzEfvfc0W29iQDrgpfxAnwu0fnoPxrjc9u/HeODu5/nh+wSaSuAKGOx6
M7UXIzkkv3HBIpIkLSqIOrh47LbzlnRsZ3n+mUeBOIqiEgzSQNgeDqiLqAMS56mHx/HHyy5j6y22
ZJN2xXQrS28lDNi8B9S73HjNf3ClGFE3bE8hKFYj4T7COkdbSfTvA/1EpA8BwR8DHNdG11ojiMTA
BmSQqlnM1K/eYECfEqZ9twJsCsSnxdP7nIKDqf0OOwzmkt9ewMi+e5L0qkBS6QPW6n1EaAwJiBpF
RPA1aGPHGA7YZ0+2HbQn7UsL2W2/Q3AcF1WbaZJUMkW8oJCKpcu48LzzeeqJ5ykpdhi0zSB22Hob
SotLcB2HRCLBwsWLeeD2O5m/rJ7Pp3zD9rsPIuklqE/V4hZYEEHViVo7wjpFmxC9qnoich4wkcC9
8h5V/bItrrXm8AiqCOCTqF/EtE9fY0CvIqbN8YHaFk/v/WQdTryc3Kk9vDj+U/pt14HzfnUUnl3B
+jC1FyOo1Y1Wom+YXQUqN0n/rx5+Yimff/EaD/73Cbpt1pfemw8gHnexKEaKmDDhBc484WS27T+Q
rfoP4MTRR+AYgzEOohbf8xELRfFi2vfYjIE9++Krz7IF1Vx+7i0UlTtc9IczgQTW1GMVjI2G9gjr
Dm3GOKr6gqr2V9W+qnpVW11nTSGSQvARAt2qUSFRvZCpn79K354OrZnejzz4MDoWFdE1a2rfpbSE
vffYlt13GIpfZzAai6b26wAigogipPD8GupqljDmyEO48983EjeGFQsr2LbfINoXl/DfO/+PYw4d
yQ59+xP3lZivOJ6FRBJNeuBbxCr4FmMV4/m4ntIpVsypI49kzNAR3H71OJ7+v1cpdTujno9jnFVX
MkKENsJPfuER0Vj4yeKI4Ie869dXMfOLtxjUu4AvZq/AAVQVESd00XP54uP3GT1yFCQ9hu2zD317
9KbPkT0wCqiiVjGOQYxDfY3HXdc8QI2p4ZyLziBeCh7VqLGoddpcxhcRfkoJ7NKm85ywKPWw6mOt
oai4A2IK2HHQQJx4Z4bvvB0HDtkHP5nCpDxcP1D5NNhoAjurAiYrOMqqIsFkD0cVUimKDIzYbTdS
sUIuOuVmrvvPhRinlnqt+km1QYT1Bz95os9F+uUWPFtHTfUPfDH1LXbZfgDvf/otogJ4/N//3ct5
Z/+KEfvsxSFDhmF9HweDrU3iEBCBEUHEgA/iW0Th4D0OwovFePbeN5hXMZNL/3wRlamFWJNac4/O
VcD6diNS06SHxfT9ZHtECWBIpuopKorhpzxSKaWgsIRYrIxFC5Zzww138fCDz1NUGGOvITtz3tFH
BAFRdQliEOjVoal3lORX3IUhs4RTNBTFMS7GwnlHjeH2P93O/KparrrxlyRkBQlNZqJs0wOw4xh8
6+X460eIsLbwkyf6pt7kShDj5eE6MWqrKnnn1Rc5ccwRvDv5I7p26Uj/fv05bexo4p6PY0HFCdwV
JSAgm9bwhNKbKLjGINbHSSTZo98AUu72XHH2dRx56oFstdPmJKlqU6k7H8lv2MSfTYbZrSg4TiHF
sTIsho+/+JyvvpzJHbfdy/x5FWzVfyD9+2/FUaNG46WSFMZjqA2M7TmlhWTfMmijQUFAHATFtXDo
0IMxBXGuvuhfHHPGCPoM6ksilSSRTKBqcRyXosJC6pJLsao53mYbcgtFWH/wEyD65nKaBPtVAE0b
6wyq4FtDYdkmVK3wuPrqG7n33gnsvffu7L/XUMRPUeTG0UQqkPzSUp4IthmStsHMH0eDazhYTGIF
xx92JNM/ncvLz73GRX8+lWSqHk+TWLEZx86mdV/zVz/tQ79hE32DOkrEBF4zGMDBFHXk+2nf8rdr
b+TFl94jlYJtB/Znp0P2odANiN2qR2lRIb7vh6VpTrlrC761qFVSqQSjDjiMu//1PwYO7s78RQup
r7dYC2VlLkP22o1d9tgajxQ+Pio+GuVTiLCWsJETfTCNbyDHBv1ILF5MKpkk5aUoKCgADKJFfPXF
dP554528MPEDth6wNdttsx3HjT4y1LkLxnHBWjACIrkal2an9sGEPp1My8cBpwhHLQO79aDfppty
yam3sf3grpx87s9YUb8CMS4mJDJVC8ZD1W90P6v5VDZwgs9AFS/l4bgO8aKO3HXLfTz++LNMn7aU
XXfdg27dejD6kDHBlEoDg7tYD4PgGAffS7WSSluTCC1dRcVBiCEUSimnjT6GJEmczRyMOKGAYKmt
qOe+a59i4Yol7LHPIA4cOZxaW0XCT7SqhhEi5MNGTvQB8kl+fsqgWsZjjz7Ff265g0WL6yktLmbH
bQfTvVtfThzdGxEw4uH7oSF2DaW+fNQgIhgPzho9hqRfz2Wn/ydH4isshL59t+SAQ4ZQUFqERypH
2ttIKDtES3TT6QAoAVyK2nfhz5ddzn8feI2DDhzJtlvty/bbKH4qhcELwiAQ1AQBeJotJ4tpoipb
9fPMf0R238gtUbFisWIBH3yHIgOeTWaOFaDEwPAd90AKXCpqq7jinH9xzDmH0HtAd1KaaFArSRsb
cyJslFj3Dt0/AlQV13EAwfM8YiXt+ezTbxl75GlcefnNdCjvze677M7eQ/ahc8cO+Kl6RC1Yxfe8
cHBou7oZDDHfUCRFDB28E0u+W073wp7stNl29O0wkO8/+YF//vl+vnhnBiWmFONDTEzg3bNRQfNu
krMFJO+lDLO/X07P9nuyfEk7Djt0FLG4Qa2Hl/JQBIvBF4M1QTcPaF7SqccInnzDvyA75co2IZgV
5vYHQQMv2fTW5L6E7FiNwOhKkw0MmrCUO6WcdPgY5n9QyfW/v4dCpwyHAlwpWFsPOsJPDBuYRN8a
+TVL4lXB9yxucQlX/u42xj08nqFD92TAFtuzRc+tKYjHSSWTuK4bpCrJBNqQKwG2qBbpsXMluXEa
Q3xUPFCXvj36MHCLLfE8LyNtbttnIKoeFQtX8NcLb2XnvbZm6AF74rSvw8vomNsWInIPMAJYpKqD
wn0dgUeAzYHvCRYAXx7+9lvgNMAHzlfVFiVPb1bCVg29VArAlvPwA89yx+0PcMqJx1GfSGKth/pk
vKYa1b6RhaOhb2Rfzpjm7SwNZ+eSvUjoetnqqVXe+V3mN9/36N2lG4fvfSg3XnUb519+BnWJKlx3
45rDRfhxsIFJ9PklvvwbCBYsuLFSxj00if4992f5UsuY0WPp1LFrYCB1DNb6OK4TqmeCF8liwmhY
JyuXTUukvmwP7ob9TaW3hnvK5FAUHyM+fjKBWB+jFqMWFyUmDl1KO3PcoaPoKt2YcO8kxv1rIoW0
C4K2Um0+Zt8LHNxo32XAJFXtB0wKvxOuPXAMsE14zi3hGgWrgMGYgpwNKUClACsxfOKYgm5s2nsY
zz47iX2HH0R9IoGqFwRDZbJR2tBcsvI+YgHrCNY1EHPw1JL0UqxYsZy5c+cwY8Z0ZsyYzvTp3zB9
+jcsXDCfyooqvJTFmDjGxBGJBV5XxsHH4AfZjFh5H2lua4AAWKWUInbcbDCfvj2NYqdD5IcfYbWw
gUn0K0fwbofTaAlUNaZwM/beZThb9t2GI0aMxVof62VLwQ3J07L17jlSYaN3a+XSW27q20Di05zy
mn9Vs4koj1SqCj60L27HjgO2pyJRwzWX38Zl1/6CeqpWVqk1hqq+ISKbN9p9BDAs/Hwf8Bpwabh/
nKomgO9EZAbBGgWTV3aNWd/N5rSTLsCzKXzrB66G4cPyVfEp5O03Z3HKccdjvWpSfhWqgu97TZ6p
EYtjwqyToUQfbIF+RcNv7703mdmzF7LNVr0YOmQ3evXanM0360mXzp0pLS3F+n5Gyq+oqKCiopoZ
M2by1dRpzJ49m5kzZ7Ci0tJtk44M3HoQHTp3IdT6BUO9EBjvyUrIIOlZQWMX0UZ6frGI+mzepQd3
3P0sRW4pfQa3x/oexokibSO0HBsU0QcG1ZWxbPACKQbHlIIppmeXnTh67BgcE8hwgdQXHi3ZL1lz
nwQNvVQ0dMMUMcTcGJ7vAeA6LqqKb33AQdXHWj+wDbguVi2+2sz1Vtfg1/CrgoXyeCmj9j6Me256
iGPPOhJx/BY8o7WKbqo6P/y8AOgWfu4BvJt13NxwXxNkp6vu1K6Y/YfujVNgsW6DuVmAkqJ2vPrW
1/g7d0Z8i8HF+h6guK7TlOiRjCrdWh91XFQUtzDO99/P5OtpU6mtrmGHAZvz19/+iZ0G9ae8pDCY
wYngW59UMhVENofPs1enLqBd2HunLbF6IF7KY968ebz/4Zc8+/yLTH77DZzCUjp12YRtttuRAtfB
wYYhtRZRxReTqWt+lWBjF2BBfOjZtYwp73zAgD0OJ5mqoSW9KEKENDYooodSIEbMDdMWhJKWb204
pZXAB9kYbrjhfq75x32ccdwYUokEVmOkI19zIc18Di9hBHFdli1fzrczZ/LD7O9IpiyuQHlZIfGC
eJDXXpXa2lrq6i1qoagoTseOnWhXXk7Xbt1o37ETbszF8/zMgLFyNAngp8FuEHhyGrUUiYNUusST
5SQLFq+z919VVbJH0ZafdwdwB8AO22yph4wageensGqz7tgwb0E171z7EPvuth8xrx7PCVQvmeaU
XIK0KtgwhYEYh9rK5bz04iT2Gbodl5xzKlsN6EfcNWh9NfGYgUQdWl8ZGnGDqOYCI2g+G4gECjzX
99mse3v6jBrGUSOG4cVKSBGnorqa5ya8wE3/vhtipey513Bs0qO8pJjGYVhNoyOa0r9RYfddd+eJ
iS/hODFsvcVEuXMitAIbFNHHSztw9hnnMnirrYmTwikowBR4mYAkQTKS37ffrOCM407AenU4joNq
oLfNNq0GHhzpPPLBlNqaIBQ9pR5ffvkpc2fPZocBm3Pumaew06BTmpH6glB2YwwoGMcJg2Q8EokE
06bNYOLLbzP+pdeYszjBFv23zEh8cSz4Xo7EZyWY5Gc7UEqjqX36jg3C/rvtx4N3PsKJF2dLez+K
LnehiHRX1fki0h1YFO5f5XoE+TBv0XIu/9ezYXsKbszFcRxcMdx50x2cefRIjF+PLxLeefN3abFY
A/PmzuKdtz/ijhsu559/uYC4JBCS4C0DT4Oo2KSAGCT0zMpWs61sdiSOE9TCCxY4cVI1iNTSuVD5
+ZH7c9KoAxFTxBPPjufJ/73Ea1/O4NDDDsZ1C7AKjnFQf2XtFPZqEcrKyigqCr20gunpWoWIHAzc
ROAedJeqNl0JKMIGiw2K6D1rqUl6HH/qGSSqF+L5Pik/lTUVzpX8nEQtOLZZyU9Jk2rwaldVrOCL
zz6iqnI55//yVP508Y20Ky1uvdTnBeW5vk9BocvO2/Zh56035/LfnEWdxqmoTTSR+ArEEHPdVkt8
ooZUIsU3Xy/KlfZaL1yvDp4FTgauCf8+k7X/vyJyA7Ap0A+YsqrCCkvKGDhk32CR7fAp1ycT3HHz
vznjuONwktX44uCJi9vYzdFqqBAHUApiLk8/8SQ33/gXHr7tGkyiAtF60HB9AUmLBm74SNM2lXx+
VvmRrWqxogheej2r0C5jwBiOOXRvRh+yFwXtu3DZn67joScmcOTIw/FTSWKxeDgxTV+zwSirhAbm
9ALmAr7vkd0b1gZCQ/l/gAMI1Gzvi8izqjp1rV4owjrDBkX0KgYpKOGya+8i6Qfrc6YTDJeUliC+
zZH8dJWSXxDMkkwlWbJoAdVLfuClZx6gQFK4JglaC/U1qy31iZP25DGBnOQlKJBUXonvd3+5FTdO
6yS+8MYcx7SptBfe48MEhtfOIjIXuJKA4B8VkdOAWcBRAKr6pYg8CkwlSPh/rgZhvau6CGIc0p4z
MYS//P539OzUGddLhk7qJsgkKmmvJjLGToODiqAmxn0PPcKMDx/D2CD/vFoPN0fdEbZZekAMBxc0
Pey3gkwlMOk3calVhVQCESgwiq1azN8u+QVXXngmo449m6IOPejXf2vwFVI+6hhyffQltDhByktR
Xw8QDOR2pTOBVmNXYIaqfgsgIuMIDOoR0W8k2KCIXhCqaxIMHXkAValUqHoJvFxc13DjNdflSH4+
Dk7GCyZEluRn1eLVVvP5J+9zxe8vZb/dtsP4NcFx6tOgEFo9qS9DFSGZWPwgWhOaSHxHjToAp6i0
icTnunHIkevTcmRa6g0lvjaS9tJQ1WOb+Wm/Zo6/Cmj1OgTp4CNjhMSKCgZtthk7D9oOrasl7aEp
hN44kn4WwWBuTQF19XW8/MKTzPliIrZ+MVb90CU2aO/AmJ7tUZUvGC6bsFtA+pmu0Njek2s3MCh4
dRQJTHz8Xp6b9C6X/uFqhh94GMUFhWFdGi9XqSQ8j5nzZ1JQAp7vhfVfq0TfA5iT9X0usFvjg7IN
567rDu5UVhYMZnkfT9qeJCTq60ilEgzs3zfLA6mRSTqvsNTCvtx02tv0t7xlh+0czuqbv5dWIJ/D
3CpgLSyvqGTxkqV036QrpSWl1CaSfDd7Lp27tcfEHZq7keVLq6mpSqzyihsU0atvsdaihiAXDBbF
YhDqViyjzEvmSH6G5iU/D+GLr6cxdKce/P3puxG1eF4VcZN+sbNabK1JfemPWeWFEp/xarFVdU0k
voEDt0UTSawShr9rbikSjF1Npb0fTU+/lqGhW6Lwxquv0LdXb2wyGaZ9bia7Z5g1tLqmmkkvT+S+
2/+BSVYF6wFovpZqzZvY2jd/5cZ9IGiWVC2HHziUnj26c8p5l7Lf/gchmn2PWbYk1+GHBXPpuVlH
QEklPZx14F6ZbTjv1rGjHr///oGglZWWIYwfw7O1+Ko4sSKee+JpzjxtFBee9TMcX8PVlW260EaP
KVt5mS/MJy3iNDg0mLD9M14K2bDNDdgCJEE9cBxoJMyt4kk0Oi49UIRxNJKrVlQMvrW48cKAg9QH
34eSciorPH52/EmUSx3nn34Y5555MjHXpc46jD39VJIlLvudeAiiimP8Jte+6c8TWlDfNQyYEpHv
ReRzEflERD4I93UUkZdEZHr4t8OaXCMHqiFZNzRy8IiVN156mV0GbYtaL8gDH+7PsCGZAHo8P/CS
+eyzL7no/LNxCPKiIIofusI1NXzm6wDN7W/BoZpLxMFwpIhXR5Hr88j9d/L5J59TV1/bqCDJ2RQw
rkN6Jm9t+gXasN3vRGHS8xPoVFhM3A/uKR/JiwiOIyxcvohE9TzemvgIuwzogXhJHDW4ODhqQsJv
kkwhIIYwC2mwmWDgSG+kBYU12fK1RQrqF7Nj3048dPf1PP/CU7ihqi9AA525hXFmL67giJ+NQK22
BcmvhvFcUSya1xakFBQVYVwHz0/hujDy8EOwqbrQupUWRCR8xrnPKv2vYc4qmTc+903WzOyYdB/x
vJyNzFlktatkNWuDXWe11obOQIKyYrEsJV7DvNs4MRKJJDhxcAuhpB0P3fdfjhh7HPvudyC333Yr
vzrvbOKuxSarKXKUww8+hGlfLAwEgDBX0+q6Tq+NyNjhqrqDqu4cfs8bLbk24CCon3alDDqMo+Ba
mDxpEmXxOMZIOMXP84KFq0PVJj3ef+cV5n/2AnGvLlgYxComFC4awlvCzpeXz/PoZFsCTY/8WTON
xvB82sdSzPxoAu+8Np7qZDVWlFziaDAFWkfpv01HPD+F720MSa+UFUuWstsOO+LVJxsFuAWw2PDm
leXLltCxzOG2f/yBrkUeMWOwGs9pIZW0Cd1HxCJiM5KXVR8rGvYog+I0alpdsy3vu+mEM8QUW/Xu
yIN33sg7k99ACYSNIMQuuO9Z8+dy7oXH0GmT9oH32NrPPvo+0E9E+ohInCCq+dmVnRD03jRpN4aS
TPjEY0Uk6uu59T/XskXvnhS6RTRNT9FaCKISrMGrDqIuqnFwi6CoHCnt0LCVdIDCMnCLguhqdVF1
CJYBNWBjqA2X9tS0FL4a7zSBEPLk409w2MFHkRKXlBSQksJwi0O8jB+WVHPiWRexzW5jGXP8Oew+
7BBemvgsvzzjWPr16oKtWYHWVGNSKfyUzwljj2K7LbtQEisOB3e72nm32kJ101y05FqBn8ev+eP3
P2D0wYcS9y2eNC/5GSPMX7IQ16/ljeceQuorcJXgxQZIR2IaCSIb00vJSQOphqXldldtIN7VQ77O
FUh8k198hGGjjmOXXfbFMfEmx1sRvv52Wijt+etkSr/WIcqEx59g+56bBbMsk2v8VixWLQVujJrq
Smor53PndX8H/GDGF6Yl1jA4yYjg26CcWCzd1uEf45BIpnCIgTiBfQBpsO20mfeShTDZmvFTbN93
E047dQwTJn1Apy6bEjMOMetT5ykTJr/NX48/h9rkUsQhSFe9FrleVT0ROQ+YSOA2cI+qfrmKs5r9
RTDEHAdHhO9nTmer/mdjrA/qhKqe1tfR81LEYun+L9TXJyjs1IW6mgSfTp3G9Jkz+eTzL6iorKSm
poZ4LEZZaSmdOnWiZ48e9Nl8c4YM2QPreRS6BrwkXl01BXE3UKVI9roEra+gIIwYMZLHnn6OL76d
yybdN6WosJi5P/zA4oWLuOP225k+bSGHHbw7p590LIN33IHiokJSiWocAzatidBYWJpSVhjnoGH7
YOt9NO7nkHxrJfs1JXoFXhYRH7g91OE1Fy25xvA8D8/zAn91An2VYwzjHniAMw8fia2rg1iulGyx
GDWgyvKKpXQsc7ju8j9gvGrUxoJkYjQMHsaRgCQgowJCbRCObwxoOt+NIDmOJGtACM1KfB6ureb1
5x9h572PYPh+h6ES5KkXFCOWFC5vvvcZh54xjNrU4owP/4/kXrlWEeTeV+KxGB9/8AG7Hjka9VON
9K4KqjgqqKR4660X+fDV8eDXQKoO3PDFJXB/tapgDNVVSa7+9y28MfkDUsmGOVHXju3Yf9/hjD1y
JF27dCItNRmcUC1g1yqpAnnLc1GOH3UoTzzzPF9/8xX77n0AWlDOux+/wp/+dhZJXYEvCVziTU9e
C1DVF4DKPsTSAAAgAElEQVQXWn5Gcw8l3K+GRfMXMHvGbDoVx4n5qSyBqHV9U4CYG0NcB0wBsxZX
cP8jT/Li61PYdZ/9OfuXv2HwmC04sbQkT2YJn0RdLVVVlTz3yiTefustJj4+jj37bs49/7wOYoBX
A9Q1XDAjKErOn1VVMl4Y5+GHH+TjL6fy1qSJVNdUs9XArdh8067ce/u/KCwthZQf9FFr8T2LuuBr
4CzsGIMTd0HAMRbq6/jFyT/nmCt/w5CDdg3sjaH9xrby9V5Tot9LVX8Qka7ASyLydfaPK4uWzLbg
9+7RuUUX830fay0pL0Va7VHoOmxaUoZJefiu00jW1uYlP09BkoGWLyP5ATGXRKKOgtJiSHkBr6wT
qS+U+BSkZhkfvTuBbgMP5Kgxo4gZB0ctjigz58zi3N8d32bS3o8NEaFu+QoG9e2X8ZDK0ugCgopD
QWERTz/xMO+9+gjiVQVGNVGwHqSD18Rw26238uBDr3LBr47iqt9fQqygAGstvtXAiKeQSPq8MPFl
/n79rZQUG66/7hp2HDQQ9ZJgvVCF0rYDp2BxUtU8dtfN3PvQ03wwbRGLl82j13ZdcMtqSaqHbkA5
CJ1YnDlz5zCw/yY4hLELq0HwgXHaoiaO4vLwUy9w1U2306vvAMa/OYXSLj0zx6dSEAuD5pOpwMYq
xqGguAynuIyjjz2Jo489iclHHcsLd93Gqb+8iHPPOZ1B22yJSwrBx2QM4Y3IvgVQ9RELO267NTsO
GhgU4cbBuNQmLHPnLeHxJ55i/oJFzFuwgMrqGhKpVGZsirtxdhq0He3Lyzhy9Ag23bQr8dIyZn07
m711CFZSgV0kU7uW122NiF5Vfwj/LhKRpwj8cZuLlmx8bsaCP3j7vi3qAb7vZ/LLQPBef/nZ5+y6
02BQbaS7DIpsVvJL04ZxAo8WwJSU8cL/xnPj3feydEngZmlYB1JfY9OCMaQqlvHVlGfYf+QJ7Lv3
AYiJUSvCJ9M/4sDTdqbaX9pm0t6PBgFjDO9MnszWA/o3eaQSjsaKUptK0q1LESUxCSKLG5FI2o7z
yCOvcuklx3HE6DFYL4lfXw2kxYTAb7+4wGHM4cMYsusg3n77Q84+6xL++fffMWTvPaG+Lpza05BH
aPVm9yuFAqI+BV6Sk44ay79HnMz3lUv4281nk/SXbVAkD7BwxRKmffc9T9xzLY5N0uDG2gqytwpO
IMXOq/I4++JLufqOR5l6xW1A2OxZSJM8QDyW+1s20e0xdDh77DMc9Wp44X9PcOQBR/DxK89S7gqm
vpIG4a05ss+nqg3cgvFT4NWD40K7zlx73W2Me+p5jjj9QoYM249TrrqXdu3Lm79nheqqGt54/SVu
vvMZJkx4jnnzalg6x6NznzhJW4NVg8WGGoeWPc/V7j0iUiIiZenPwIHAFzRES0JutOQaw7cWz/MR
EYqKioi7Lg/ffQ9d23fIWcw5aIbg/4KiEp59+hlenxBKfn7a/VIRYzAi1NbWcOcdd3DcmCPZZaft
mPDo/bz/6lO898qTvPvK0zz72H2cddqJvPf++wzd7wgOGTmGL6bNhHhRRtJoSzFaRHDxaO8kOPv4
sVTWJbBFxdzx2NNcef0vSeryDY4I8kGAVE01Uya8SInr5kgvmbYVISaWV555gleeeRxJeQERB8no
ybS+gvo+r0x6iMNHjMAm64LF2dXiqMVYH2M9jHposg5JJejesZwxIw/izVceo6iwmD12OozZc5ZC
rCQoPlmf8fpqi7u3GKx6FBUoIw/Zh99c/nN8J4WniuIgsuF4Q3/3/bd0aB+n/5Z9WN3nJW4cnBji
FHLhpb9jeV2S7XYajA01pk52l7ct3DSrNm6cw0adyLinn+b6W+7Exoux4gRppxs5PbSswuFfJw4F
7Xj3nU/539uf8vtr/8Uf/3YtBx50YAPJazD2aWP7r0BpWQmHHj6KG266jbff+oDOXTtwzz0P4yWF
mFMQrmKqZKucV4U1YYduwFsi8ilBePvzqjqBIFryABGZDuwffl8r8BGSGgQS+qkU82bPZrNu3TJD
e1r7J6EhVYFZc77l+qsvo8yxYBMEo3XoVhcahqZ9/RVjRh/Bfx96kC7ty3BSdUiiCidZjUlW4tha
CqSGIw/ahSmvPcyrE59BvSR7DRnJ+1M+QZziwJoPQZltkTPcGBw/wZnH/4xXX32Z2+69nz/+/Uyq
6pfgKwTOEhs4FC755Xkcut8wClxDkE44QEZto5bHH3uKc07/GYmaFQiW7KCnwMNGMl42JuNt0yAA
CIIRE6hurDbsQzGaosDx2XarAUyePIF3przPMcefwWdfz4NYu4wBtW1uXzCkIFnBVZecxu033kvM
xAEXo4RqhfUfIsK8ubPZd9hQykuLw/fNaWRraQE8HzxQibNgeS3PjJ9Eyiom61XLs+DXKmFV8dXi
ISgeQ/Y5gvseeY77H30KjzgeLpYgAr4lXjgZ5480r5R04Mnxr3HSuZcy4a1PGHvqWbm3lQwWFcrx
4E2bNtJawnAA6NClO2+99QH7Dj+MLz6ZgZ9wMeKGh7f8xle716rqt6q6fbhtE0ZCoqpLVXU/Ve2n
qvur6rLVvUZjeAieVYwIMZQb//Jndh8wEEL3uMYz6ng8zvT33+OQffYIRgfNJgXJGDd2HrwTXbp0
ARtathWyl5cTqzgYXImhKQ9bX8WOgwbw5uvPEI+1Y+g+I/EoACthgMbquWitDBrqpq1fwwuP3ckW
3aC8UxFKIH2sudvause8uXM599gTcazN5JgPHEqDnu+LUFdfzR//cC6nnHoibiydMiDXNS6YCQSq
vOyog3zI1v1nvKnUw3V8rK1kzOgR3Pd/9/H5F1/z+FPPg4m1CdkLiuOAL07w9qequOCEI/Gqg6dg
wpZen5H2BFFVXE1w6glHBWoMQqInRmsoxy8q5bO5i+g7ZCRvTltA5979iSFrJkcpOCI4oWHYw+Bj
+aHS4/2v51AjxdiiDtRrPLDfhXywMmQ8YFShpCN9dhnB7PoSvqlSijs0VdO4cbdZF9nGxI/CJt23
4IH7n2SfPY7jsgvvJU4H4hTitiJWZoOa7yeTKTzPUhSLc8HpZ3Li2DGI0cBYQ/CyBGOwwXGE9959
g/Hjx4GjWE3rcUO3RAJKUA2y5ZhwLpVPG4dmB2hpuI5QCmMsW221OW9MnsQFF1/OQ+PGY3HDTr12
iTcwTCmO1rNlB2HiQ7fzynOv4JoCRM0GI+2tDO3LypGqWtwm3TIgehXL089M5KjRh6JePaoeGZJP
L76dQ/orQborZEuZGS+rIJrC4BHDo4BqjjtyP8YeNTIUGFr7rFvQF0I/bqe4PXOW1TN4t6M544Sz
ueOft4G6bZH2YK0i291PVdlyiz702aw31s9yW0wvqttCVHsef7nheobsP7RhZ7oIbf0EIbsMFGIq
OBgcDOBw1V+v47+PPo4TL8LPqG5WRZGBMwciEIsxZ848jj71XH71hz8Fv7ZW5su+J1EQS7Iu8Aj6
+Yln8+cr/8Sc7xbgEMO0wsS64Sj9ADxLkRPjr7+7nDH7HoCuqIbC9CpCARQfK4Ypk18Hv4by8kK8
+hrc9DJzK81Hvypkz7Es2FriBQZbt4JbbryOr76aiokVgq1baSmrA6NJMIX4xmHm9Kk8MO4xpk75
nIOPOIC6+lqccLDbkOEIGFfQrCmpJejsCa8e3wrnnjUKvBXEUIwRAjfUhpdRcoZkydqv4XKN6Vw6
2WHz2SkysucACnggSYzrhaq+VfWXRgrXdN0E0jrVTEi8G6rbvCSUlPPwoy9y+523csQRhzH53Udx
TR29O3airKQdFXUViFiMtGAQ+9HQcK/psc9ai/Ut5508lkKvAmNTpNsieKJ51mLQYJBWiYW+5D6I
w9gzfs3AwXvxr9vvbdBSZEm6a4SweU0g7iEYumzWn3ueeYV6Dy4+73RYMis8MI8hOSNNG6w4eMbl
5nsf4/b7H2P60tSa1VGyPwjxwiIAfE/57SVX0KVbIfsdOIR9hg9u8bi53kv0wa0GzoylBWUsnD2f
Ab160bG0hJJYg146PWlXsaj41FYv4+EH78QmapEmodphMrB0JyW3TdJlZb40RqAIJjD6KUZ98Few
1cDuoKkW3FW2ekdoSIfQsCmEpKKhYBGnqt5nn0PHMmP+Mi6+7Apu+fs/mPXN9yCxfK/PBgjNIfmG
fYpxHRYuWtAolB4yElWjEPrgzMbh84po82HzGcIHGsLl00ULudGTzd9DLiTjDpLpowQh8VacwHAX
hsNff9OtOaHwxngcfvAh1FbVISZIgPcjrh7WAmiTzXUdKior6NNrExxNZv22KmV68C5YJRhwYwV8
PWMOZ//y4uBnCT1h2uT2GzypjjvlDB55/GmWL1oavpem4ffG54SbYvDE5aa7HuaKa27Id8hageMG
quELL/gtL41/i6WLalp87npN9GkNa+DvXMDXX0wnWZVkYM9egWatkTuliiXhJahP1jJm9Ai69+iE
a2yYECtIfxAE/mUTQnaDSVpJ0ED+6SRn6Rc/YGByWlAsSDq6rqmrXy4a6fBzDrXh1QmWJUxPCQ1U
JlzGHn8aY0Yfxv77DqFdmcMu2/XjnTfeDhRP4iASEEFz2/qO4LVqSvQgxGNFfPzhJ6sfSm+cMHRe
mg2bp7AMCsuywuVdckPlodX+4GVlHHbwUVTVJ7PC4oOQ+IeeGM+JZ12UCYd/86UnckLh/do6Thh7
FBOeeA7HcYLV01YzBP7HgmMc5s37gV69emGtBoGGOaJU888u8wY6Lr4Vhg4bzjaDtg3ShGfOXcuz
GU1Hvwcln3DiCVTV1vLRp5/RLENnV8EY1DhU1ibZdY/dOfGMs4KAxbaYdClghPPOOZd2Ze35+MNP
Wnzqeq+6kXD66zqljBp1KmNGHIpfUx2Mbo3IS1HihcW88MJzfPrWC6Qql+NmJo25x6c/2axvaYnP
yXSo0LzvBJG1wYMOH5mvDRIf4Wf1aXB5auFQHo/z+UcfMWjbrQkGIMXi4BaXg1vEp198zS/OOp+j
jxrNc089hle7lJhXDR7EYu2Y/ulCRp/djqr6FZnsnBsThCBsXpMpzjx5DDE/Geis0wFSLYCJx4Ns
gYUlzJ63lN9ddR1ffzuHTp06s+0OO9Kte3es77NwwTwWL1nC9G+CuL8TjjmKXxw9BsevR/wEUAOZ
4KnGpv/80MoqbrvrZn5x0WXMW7wMMYaaqiTD9t6NX559FseNHYXjgk2lqEsl8DWG4xQgphCsT5kr
fPPRAkacJKTCNRh+5HWBWwUxwqxZswPVWBN1SzPtJQIapOIVAeKlPD/pXW694+7Mz1krB7W+UtlN
lbcKDfaPbpv25Fe/+z1X/uNGho27HaP1SOPBVSDt2GGliIRTzHm/u5QnXvsAcHImhq2uZ/Y1Gn8O
fy9v35k3X5vCTrsMoLCkXYuKXo+JPpw2KSBxfnnuZRx1xKHE48WABoY4yc3rYtTBNQ5d2pcgqXpc
P0iA1OK+EUrt9bVJCjt14/vZC3jzncl88vkXzJs/n3gsRqeOHSkrK2PvPfdkyJA9KI7H8Gqr8Oqq
KSyQUKq3ZAaJVUGFq6+7gd/8+a9s0n1TjHGY+sVU7rj9dhb8sJA/XXEZb7/yLMlUAk1VUxBzg0kD
gnGVi88aS6oigVti8BPhsLWeksDqQhE+++wznnzgRoz1WmwMNWHKX+spKeLsOGwkV93wHx5847PM
MeloymQKnFiDRtYFllRW8cdzT+eHbz7n3HNOZ7tteuOQyIqehECAaL4OYpRem3blwbv+TZBLSZB4
EbUJy6uvvcn0GTP58JPPqKyuoT4VqP3SEZL77TuU3XffkcMO3QtNWGLiYAlWVLO6vk3Gg4dQsaKC
VMpbxbHNnJ+2gZgYUz75kpG/6h7+tAb32ljeWmnXCX7cfvAu/H3JMqxjgoSHmm9QV1AfU1TMZ5/N
YPKHnwMOKc8j5q4erWoY9OklPdz4ysvosdnmDB9+IO9Oeb9FZa/HRA8OBh9wOvRg0kuTOeSgUagN
svflX+RbWDR/If/46xWtyq2RkRXCXBp/v2McL74+hd9e/U+OueT6IIdGjlTgs2TRAp57ZRJ/v+5a
titygrwZpHNmmCwyktyLNIKmkjn5McQIg3fcKciN0aFjwECej7oxfHURcvNhpHNh7HrwDhnNdDoh
20ouu0FBRZn23feUFgnUpW0gq2jT0KNGysr5YUElo87+DVOXNj0nHU2ZHUmZppXOZWX85YFHMhGU
/735Dq75zflB9KRkp0XIfsp5PIb8VGAPMA7zliYYcfzxHHH6hZx9/sXsVVTMr/JFSirMnD6dy/5z
PU+Of4sztujLZv16sDz5LVZNaHNa10bZxmKnsHDRInp060R2VsuGiVdz72I42w5nzcurapnwyhv8
Nb1gjGcx7uqRfbIuyciRhzPx5RepraqhqLQ4nI03f0+Dd9mDwtJ2LF++jC7loR0wk2eGnO9LltXw
q0uv4Pd/vhYAx1l9ShWEyhWVlDcXOZst2Qtcf/2/2HHw9i0qe70megCM4ZkHH2P4sAPCkN/midsC
r7/zJnff/FuoraIlOr1kfT2FJcXU1Sep9IoZcthRTP1uAX8ob597YE6fdujcrUcmdwbABSeMoUen
OBefdSJOzQrAz+rh+eZh4TexkEqwY//N2XFAH3CLmLMswehzrmTuomUMGz6cLbfsT2lZOQosmD+f
b2fMZM7sWcz6fhqX/f4i3n3zK4YfOoxafzG+GoJ8PEG8wYaOYMCyjBm1P9TXhHaWVfs2BxJijF9f
8mfe+/p7Ppi2INjdCu2WSrAqlXULOHTUsbRvX869T0/k5EP2DSR7LJLR2Td91hoSlxjB84RnX/uY
N6ct5ePFyaAqngZeRjZM35FVjFrou2U/bvjnbdxw022ceNJorrnuPq656edILEVK61t+I22Gpve8
ZMkCunYuxqgl2wOq4Yz8fTLItR78ramto6a2wXPNaqO471Z063v+7x5eefVVAB4e9zCnnn5a4N7V
bFYwJRaPU15WSsd2pdhUNY5xaDKLDL/PmTuXRYuXstfQfYCs9ParA4Ff/+bXuK7LLbfekvf3rGrS
o+fmJFMt69DrN9Gr4lmP62/8F7tsMxQjsvKsbaKUlsXRuopmpltNUVhcBmpQJ8boU85j5tLwBUqv
6raK56ihMPLPB8cx+fUX+MONt/HHX5xCzNYjzYYoN9RLbaiXNDEoKGPIiJO46Iq/8cKUqVnHhGdl
T0PD21u+eD5X3fQf5n5XySZbFJL0U/h4oafJ2vPnF5F7gBHAIlUdFO77I3AGsDg87HdhFkRE5LfA
aQRK7fNVdWJrr5nWRXupFMOG7kpoJKGhYZrvDCqCFJXxwutTeOKlN4GGWLYcle/K7pkgeZ1FSKLs
OewIjh5xJCePGomDi5+owcmkXshzfnq1KKcAt7wTF1x+Et9VZGVKdcNZV5odsopprK144P4nGbzz
Vbz+2tMMPWB7fNYHoofG/au2ppoeA/sRrBeRT6/etM0axDEJib4WP8vetCYCy7777cd++++HtcqB
Bx6El/JwY/lpryFbbRCbs3zZYrq0L11JNxO+/X4W3TbpTu/em4WvZMt4Jx/GvzCe+++7n0QqwdVX
/432HVaifw8vUV+faFHZ65uirxGUeEEB3363nHhBQWDNzoP0C+Wlklz5218H6YMlFmyreOieD3c/
Op6dD/wZb385h/S6HaqhbXUVEAJC8jAM2ecw+uwwhA+/+YE6KcZP58BZVUFuIY+/8gm9Bh/OG18v
aRIynRMqDTmOOx06d2fGzGVs0mkrXp/4NTEpxWDbIoDqXuDgPPtvDBee2SGL5LcmWLxim/CcW0Sk
VYny055C1lo+//QTDtx3aIO+tQV2bt8YfvaLc5i6tI6tdtkzSAaqhHlCWlEPGwTWxHBJeSk+/nwa
dz74KJX1fhAcl3bXyHuyQYwwZ3EFW+15OHMSiltgVjY+ZZ2b/qsZ6fFX5/+eXXc4nHnfVeBqrPlz
1wkCN8NFi6vZd5/hq0V1GXfYJsbm1aep/gP68b//Pc/EFyfQs3fPBpJv3AmyvvueJZlI0mXTTQM1
Wd7rC8QKeOfd99lh8C6079IlnN2tvkPEIYcdwrhx45gxfSZlZaX4qXy8Ebz4XiqYFaaSLXHnXs+J
XoyDMU6YPmYVOlmR1SKEGjfGq19OZ+rSYKropqW+VhBCmgzA5YxzL+P0835NvLwzFpeG5Eh5bzBD
BB/MrW85EWTfVxg515gEMpk11xJU9Q2gpeksjgDGqWpCVb8DZhBkNm3JlQiyg/qo+nipJHO/n0uh
VxFKWinQFE0WZ9dU6PkaeC7V+jE22WpPFHf13720cKZBnhnXjWWCaso7d0cI1xrNeY2E9CpiFhdt
vyn7Hns2L07+qPXXl/R/DS3520uu4N7bn6NYeq6XSw7EYtCjZ481KqOoqGitOhQ4af1+c14tjX6r
qKhgyZIlYIN1KJpFMkUsHsfzVsf4nB8jR46kb98tcBwHx21eNnLTBt8WPqb1mOgDkbq6qjKIVcn7
wEO/c/Xx/VQTQtCVEULoEjn2jF/z4HOvNxDCqm23TaqZPiedJ2fKzIXcdNu9oWtgmgyyWiQPEVxz
002tuChZ77/JRM5lk4AJc/tok/R4ax2/FJHPROSerPWBewBzso6ZG+5rehsiZ4rIByLyQW0ikVXX
YPvq66n02bwz4ifCl6653OaamV0hhiuv/gf/uv1exHHIBNusCTTw4FKBF155nUkvvUp2TEZWNUg3
jjUxTjjrQqYvraHXlv0b+soactjMaXN5efzba1bIWkSDXVjpvkln+m/Zd5WCWc75mS2Q6Xv26Em/
fv1yfgfWvAtnP/d82oFQIHjllZfp0KEcrMWRlURsxGP07NGdH+bOCnesRKhrDo2qYVyTK6Q2qebq
dZ71mOhB1cdxHbpvWpLHpS6XEAri8TyEkC94qSEy0ncK6dpzy8CTZy0QQrpLFLZrx133/5eG8Pys
6X0zRJAJslhDIkiTgKMS3oo22tYqbgW2AHYA5gPXt7YAVb1DVXdW1Z2LCwpyfjPGYdas2Rx04EEN
O4PGy1NS2g9bIV7CxLc+zDpHms7yWrD5eSU1pdumPbnyHzeSihehJp1np+H3dD7zhFNM8SZ9Ib1O
QEvbtXFTNVJxl7fvzFuvf4gx64OJLTv2GIqKCigrLSH/WrLNIwh6TZdl2WGbrdZ+VVuID6a8S+8e
3cnOcZUXySSdOranYnn2RPfHcoBo3XXWa6KHYHmtLfpsEYSArwRipCkh5H0WASH4Cs+/NoVb77g7
KxZDWk0KuWQQDMEG+NXvfk8qXoTvuiCphgFEIB8RiJGWtV0+zs7S3adJoKiwU2h0bLuOp6oLVdXX
YNpwJw3qmR+AXlmH9gz3tQIG47g4CMOHDVv14ZIOalOsU8DRP8+2c7R89Fy6aAmXXXIpc2fPwcnr
Dx08+BV1KaZ8+lmg+M9ujPRAZByu+NtN3PnQE/itXPfN+qvyAIAbrv8P1l+Xupt0uoq0cjIQrgZt
MwAxfquJnjDdtGDxaiu44JSxPPh/twIE4TJr+1Yz77pmrg2wcM48nnzgHs4/9UTwVqb/VnCEPXbb
mRXLFvHyc0+lC259XfLJYCvdpxm9srsS9U421muiV8CIoc8WW2DtyjxYDAsWLGwdIYjDA0/8j/Ku
PbICStcWGVhGjP4ZUz79jIq62jzFrj4RZEiguVNCEqiuSra4zNVFuIJYGkcSLDwDweIzx4hIgYj0
AfoRrFnQklJJP7BUyqNTx3I23aRhqUnJzIiaO0+oqKxmhx13bs2tZFBWXs61/7iOTp064aVW8qKL
YfmyZXlmmgQvYcrjrcnvhV9bKX0ZQ2VF5UqPGTZ8fxKJtm/jFsFqxiGie/dNaD0rZ013VXEMdO7S
mYfvuyfY/SMKyZMmPk9JQYxBA/sHThTajHdXOKD36NGNgf37MumlCQ2//Yjjb0G8ZetQrNdED8FL
UlJS0oyuKiOKU1lZ2YQQmlmtFhCM4/LdrFCN3MqGWRUZCNC1a3eWL1sWWscbRuDwplabCDIksJKW
GzZ8f76d+UPguUL2k1r9N0ZEHgYmAwNEZK6InAZcJyKfi8hnwHDgQgBV/RJ4FJgKTADOVW2JD1O6
jmEuImPYcbvedOtSkFkfoHHisjQsgorBYli0ZCn9BgzMX/Qqtu9nz+LAAw5i6bJluAVNPVvSLnhl
pcXUVy8PF4hvbAdSKCpGnOAlNK1UB44fP56uXbty+IjDm72HHj03p7Jq7WdJbS1ytEqqlJeXtb6b
ZasYTWCb86or+ez9D/js3TfzX6wtIPDM4+PYf5896dSulPRC3M17VYFRjz13G8zbr09q48o1ujAw
d+53FBRuDEQvQQUDos/3tNMvPsyeNSMPITRdkCNNCOK4VFY3k/1tDckADLFYLCACvy6jUshgDYgg
TQIiworlFXnr3aPn5kya9ClGDZK1rYmkoarHqmp3VY2pak9VvVtVT1TVbVV1O1Udqarzs46/SlX7
quoAVR3f+isK9Ykk++4zfCXBLY3qSHPueS1H/wH9Mq54QTXyl5NMJCkvLW7G/U7AibPD4F3C761z
+0m72T337HN5XOwa5vQtda1rSwRJywLVaTKZpHevXtDqFAjh4B6s/4hjE7h+LU/fcxPHHDyUlx65
P0c9udbNTel1gIHk0tn88dfn4Xq1ZC9SlB6MVqxYwbfffhssPiOCSVTyixPH0jGe1U5tNSBlJDbB
+imOHHMIRUVriehDb4pFIvJF1r6OIvKSiEwP/3bI+u23IjJDRKaJyEH5S20Z0o+5uKSEZLL5aWra
f7c1hADZaRRaN96tlAzCz75nKS8tDnxxm8SlrT4RNPa1zUXDGzB/3vwm525oqKqqYuBWA7Ghz/DK
/F2DX4L779qlK1OnNgScrREpNImIDP7UVFczYMCAlZ5XV9vyNLLZZQOMGj0KDDixxjpYyftxXSAd
63J1maEAACAASURBVKCiJD2PlOfRsX37pqt2t7xEMqSqyk7bbsMxY4/kNxddkP/QNFaX+LOXFHUM
Mz79kLNP+zklRXFSdbVkzy7T+ODDD/nbtdcGhgMxiPVw8fjZkYezZP6c3PLXxmDUTBkPPvQgU7+e
Rksnyi1huHtpGihzGTBJVfsBk8LvayVQJh/i8fgqJbSyMrdVhOB5KcrKynJ/XN2GyZHWAQtTp34Z
EIHn5X8fW0sEjUig75Zb5PGzbUoCqtoqV7f1AUaDxUEWLJhH/759ELtq4hANFpEwKO3blXHv3bdn
/cjakwDDcvpvuRk9u2/SvEOd6/D/7J13vBxV2ce/z5mZ3dtTSSFAQhJAekcivfcepfeXKlWkV1EU
REGwAoooKgqIgCCCggJSVHoo0kFCSEJCklt3d2bO8/5xZrbcu7fmhtyr/vKZ7N7Z2Z0zc848vbz5
espshrbiPFBoIs1bFBGffEeeSePHEffmTO4WiSaedFaS1o+45IwjuevGK/nSMYe4Q4pSbUrdk6gn
6fQM9jbfUvZGDDdccyV7bf9ZdpmxLrQvIuN3JvKOAe2www40t3ZAbROYDKgloyGH7LMr22/wGT56
/ZUq5+g/iopLlbV7ymnHcs5Fx3P+pcf3+Ry9rsBuEmX2AX6WvP8ZsG/Z/gEmylQ9e3ErpYmXz6K6
oAeUFSeO7xdBUGvZbcft3b6BD7A6DPzy1ltYaeKE7kO0BosQdLughxdxd3CRHGkUx4IFc10ER5+a
uVRGbXzwytPlPzvwSe4cnYGLzDjtmMPJdFviQtG2ZhZ/Mj/9kb6fTzu9rxZ5kezsa8TFsoSqBSPk
CwWiMCLwvKWssZRQchEghKidqauM58F7f8tlZ5/Z6bhqA+rDmCnJZinJuPjs87ns3DMhzCU7yxdN
yW4kDY1st8OOtDS34ooXOo1A8x2svtJELjvv7H5dbbfjK9s6X+pNN9/M/jN3Y+To2j4/5QOlMOPL
7LFzgfHJ+z4nyvQNZVy7y2sS2qVQDOvqB0Ew2GII11LrHMU02lKY1l233uwIQRRW8S8MkBBUfeg7
/+12jl1hRDK04dF0pAJJFEdra1KYrs8aSSlqY5ftt3O7BtuMnURm9BiVIWA15jOrT6sY2mCjrxEX
yxIiQtpaJJfLuzLa/f6R8jflkrRAFKFRyHXfuoo7fnELNtde/JrzyaQ+kuprvJxqpJk15X1BjA8P
/fY2vnzi59l/tx0q7fKdQhkAaG9jhx135M233gVNCL0VorZ2Ljv/XJ569C/Vx9GfZZzAqht7RKnL
xeNPPMIee2zJ2uusgdWwiw+yOyy1TqlaUZy7zyjPiFywsOdQsm5/A0At1lrWWGO1Pt5JN/UilpG1
Gc4/5eSSaj+I9HCfnbdF4kKZdFA5cGsLHHv4FyDKl4Y1KBBmz36XnXbaYtiZbMohIuTzCePs63Uk
nb5MnOPSs77IobtuDWm5o8Fw4CU5Fpefcwpj6wM3v2VRGcVG2CKIhlx5ydn869knHe0YrLUlAIbr
v3sVI0bUD+AS5L0kUuoFEXkm2detz603pOaF+oYGWtta8X1/YOtO0v/KNpOUl4gjtlxvCs899GuO
3m1zNphQx3WXnN2VDGvn33MvNordn1YRq3gCks+xwwbT2XhCgMx9mS8f8wWC/BIq/WXlv5743qxl
+mqrcf4FF9HeHkLdCFx2epY1p6zIkw/dy+RGw/e/fhGUVxjVMotTH5AaMIy4vHoPaGwSTj75YHbY
eQMK8XzCeAldMv+7+72+nbYL5qUx1MlrKpr2OVGmPCNy7Jhu6i+7I7v9xKprVVb09vdpgTkboCEq
evarevUHgsR7f/phM7nsy6c4Ip8+5Ym0nXrsDTEnHT6T8049PvnuAM9ZcX73334H7Ma6669SPSJ1
iENEsKIU4sgtzh6c8J2+SXqBopY6ItZYaSyLZ79X+rgc/ZnnVGOzylsvPst1X78E29GSdPRKI7yU
R/76V0KrYHwMMGVcE/vvsdNS9c3oDudfdB6VGbn9wnZJEbo02aCqz62/sFbxBrWvbTKfKIHN4Yct
XPPVC/nyiUdzzy9v5o4fXkf73I86H95lrlMTl2cEzyrf+trX2Hrzjdl1y02486c/YLvProeGOYoL
QrXbtSG4NfrxwpBXXn+z2HcYVUQjMibiaxeeyY3fuZIj99yp9D21Lvu9j7emELnlZQDNt/Cdqy5j
hdENNDRkKIRLgDxOXV22Ev29wJHJ+yOBe8r2DzBRphpSUcyW1aIvwRiD+B75fIGVJ07ox++mZQks
609fme9842Jm7jCjdMqeHDvdEYe0hrCBee++Rr0XJ4ynTA1FOeyoS8DPImLIap5H7r+rH+Ougi7j
sYxaoZ5c1IIawTrNEjsMiDw4B1/q3BvVWJM49vo6+DJnHgUuOeNIdtls9UpHXjUHXk9Ev9ysYEzR
YZfxO1GVxFH3w5tvdY46MWQ05OwTjqh00PVDiOhuWKecdmy/HHF9QHc+t14hlMoIx3FEtlMZi6WH
M7p4WsCzHYypVQ7be3sevP3HzFh9PL//2XXsuPaqbDZ1RbbeaB322n5LZu66AwfuvhP7bbclW3xm
Gp+dujKbrjyRY3fbiW+efTqH7LwV9958LV86an9WHVePT4gx4tZaesOLvsDOaoIQ5vMcdeTenH3p
pSCCNYZYFJUIz7ZzyC4zeP7hu/j+5Wex32bT2XDFev7+lwdY8OG73V9ip7N4As8+9RiH7rsnJ8/c
m21Wn8Jh++zNB+/MRiUPJkSl79FNvRrUkkSZbYGxIjIbuBS4Erg9SZp5H/gCgKq+IiJpokxEvxJl
qp4dgJGjRmKtpXMVhNjGWBU62jpYYdQoVDv6WHEy1YvAjxdz/63X8fcX3+Cys8/ksquvpULXTwm4
Vn41Refd43yPj565GwqtVNobHY44amdacpZG4+FpzF9/dxsn7Lc7N/zuD30ZeMV5U0dN+W3JNnh8
+3un0x4u6Fc53qEENZDLF2iqry22A+z7vJY57XPNPPbHe3j8udc54bCDuOEXv8bJh1I8usu5k9ei
pVZLavRqIw2vPv4HyC0uOx+4GYgR43HTTx9iy613YKPVVgZrOfrAmaw3YxNOvvByTjzr7BJfSJdW
T/eBJGJYSlf2xBOPMGfeG6y+4XrdXEGvUODPIhIDN6jqjXTvc6uAiBwPHA/QWFdbekpUaW1tJYpi
xJhBdkek85k+gzGqiocwfoTHzJ1nsM0ma7Jg0RJefP0t5s+bT2tbG6ilLtvElJ03YuSIJiaOH8+E
cePwfZ8afwmioetflzaHkfKmIZVXoIlAkNrDRS177r4bN/70XhDP9ZTwBNHYRclYQQt5shhuvPoy
/vHMs5x+zCFITQOnnnUBG2yyOZOnTqN+1MguLoCF8xfwr9de5ZJzv8S7b/2LGRuuwzeuuIDaQHhm
/Bg8BUymr5HkRfRK6FX14G4+2qGb468ArujfMHocAXV1teQ6cjTUd3I+iSC+x5LmFmozAa6NXy9I
bJzp9/ENYUc7m6y3FjnTwPYbr8Ujz75MBYHudFPLeb2TaCC3ZBHrrTyad/7+O7wotc11mkWU4088
kSu//X0u+OLxQEwdyi5bbMbtP7+FLxxxVOnIPhACSKR1wBCz8sqjuObac+gozCcfhWQ6tTUbLnQ/
tfk21Dc4It+XLxVtvJU7M3E7W643hVUnjWWDCXW88N48pKYsrLYTpy7+glU8I2g+xw6br8Piue/z
0p9+U2bH7Ty3zn573An7cv4FF/Hg3b+FfCu0LuHJh+7l5jt/x/e/fhFfPP8yEL+qPbnLfUiOSWfx
d3ffxiWXnsGJp32BXLyoz/bZTthSVT8UkXHAn0TkX5XnVBWpnsGXMIUbASaMHlkMCEnLiMdx1P3F
LBWk04tNRKgYjfJMGJVhwogxrDNlbDGc2Phe0eRmCyHGM6AREIHt1LSl2Haz+v1MUsIo5t+oZdL4
FfjiSYfS0t5BYzaLjUOE0OV8YYoi3phaw+5bbcLu234O8QIWtnTwwdtP8PBjd/LMc8/T0tJKrpAn
m83S1NTEpptszLRVJ3PP9y4kMIINO8jqYshbpk0aDxH42VryhYhuUv+rYiiUv+sRaVp1d3WhRYQw
LGC8AYTOJK5w3xiI82y+7jRWbvK57pJzOf3yq6ucrPQiQGwVYwTN5dhjm035/jcuoE5Su3x1iAiP
PvoYF5x5uiMEccjO227B2tvtwsez3+pKCHp4booOG+B3d9/O6NG1YNoRDclkstBt+N/wgO/7S2Hv
TR5eGxJoyMqja/nyiUez++YbcecfH6NuwsTyw7rAM8IrL8zixKMOYu8tN2HmHudSmzVQSO5pFee9
AFtvtRW3/PRubD5MO56SMRFHHbQPW+28B7vvsSerrr85opYuKmonGJMkmRr4zlWX8e1rr2alaaOd
jdbvu322HKr6YfI6X0R+hwt/niciE1X1o04+t6EPxRmzVcEDiWNXwTQVecU4At655+uAkKwpEQRl
u2225tnnX2TbLTdH41Iv43L6K57z36AFCHOMqQ8YM31F1pw8nj222QyrShhHRSe2Ebf2XPcywWQ9
iD0wAQ319c7qaFy57P5giGdyOLV97JjRtLS2VD3CSRIx2cxAbYOCECNxB9l4MT+9+iL2mrE2O66x
Iicf9Hn+9dwLtC5pKT1TEeQWtfD8409x0WlnMn38JL554Rn87oar2GnGOhDlKJp6qnhDRYSGpkbI
1hKrRSUmSzsvPXInm00dxZpjs8x961WquCSqwgB7bbkZ4bwPifJLUFkM5Ohr2NVQRGrzbWzonPnb
XyhoiKcFMtrBYXtvz+9++p0udt3Uprv3lp9li89MK9pz5778bIUtl3x7yY7bxYbr2P8G66zFUUfu
TTPOdmuNxbPt1NsWnn/4Lp66/7aizbbacMshODvtmmMb2Gb1Kbz+2MNFG21/7LPF3xOpF5HG9D2w
M64QXXc+tyEP12s3mYc4Ks1LGvqqLghz6Yl8CamOOX3yJP7y6ONY8YvSfheSqrbEiBK/ILZA1rN4
WsAnpMaz+BoSEOLZEKI8nuec2hopsXrEVqiprSeMGFCjkyEu0bsY3YnjR/LJJx8zceIkSre5RMoK
hRA/8NGlLeYXhhgRpqxQwwO/vI4Yn7feeYx7HriZd955F9QypqmJ8eNXYM3VV+PsA2dw8VHbEUiE
rwWIY4wR0jLEFdchgmCIch1cfeUVPPHPZ9l8jcmoWDzyNBpho9VW4fkH7+Dhe27iq9fdzObb7crx
p53DWuttAGWp8OV2vAmNPrdecxEjRjZw9qV5CjGoeFUMC4MYwbkMIYBapaW9hZpa11DFSfUDGX1y
F9IbYXNkyXHgDuty4I7rgfGI8YvmIc8VRUfDQuKaEYg/LrlsxOB5XcdhsUjygIetizn+mKO49Mpr
uerc01GNMBo6mpOPOGinGRyyy+d4fc4cTt13a954598saItZc+11WG211WjP5fjoo494edYsxo2s
46Ivn8qsv9yO5BbjhfPxYxC/DtUBFTQbD/wu0ZJ84Feq+kcR+SdVfG59v8uKEGPEAjGCLTU8/zSQ
mu26qeekSNJDunzfwI1MguJpjIY57rz7MbbdYSc+t9Fn8IvuyDJir6VvAUmkVrKgNE5WaOdBO5OT
Jj/gAagysqmBkSPAiOfsm1Jxgh4xpAm9S4SIaGjKMn/BR6zF+hU3JZ2o1Da4dASh9GKIMcT4mmed
Kc72Z+1mzu4HTqeO48Tm11om1KUj6ryolLTgVmrfO+zok3jyj3ehcR7RqGjXy9iwaNNTL8NLbzzB
D267njffeptcIc8KK6xQYcfz4hxZXYyEtmS/C8PhQdV7gTcQc1wf4IgQEIV4XpRIggYbRZgg49Tt
VArrIzVIxQ8jimrM/fc+zlUXn4PkCkDsCstRWh9rTKzjuxccB35APhT8IEMhCvHKVPjAKDbMY/Kf
gO9BHKIR+NkMYb7/hF5V3wHWr7J/Id343Ppy5ZAS+0TAsQMO+xwgyhy21T7txHC07LUv0+uoinba
p6CWtdacyJ8f/jMzNvoMJQ2vJ0NJZxrVfchXyTfsUr4yQZZsRsoiEP9jbPQlAjx3flmc66d1dide
AtZVmEydTdYVNBrALzoHMsqUSeOxQS0mMfUU+5KkzMrmEZtjg6lj2WDqbmiSgQiQxuRDB+IJlgyF
UAkLLhJpaaSVoQOlJpvp1kG2NHDqfkKM4qTMsMbOz5MGLw8QikFUOe3EA/ikLWS0V/7gJ9dStB8D
NiZrgDii1ijYQulQdep7jIfGQoQgAlGYOj2XHzd35MmWadcWKbZ5HNrZ2P0dWXkHrSISIeDrl57P
QYeexm47bM6WG66JDUNMl0J0Vb7r3iQnKCf2iU2/fG4TjaWhsZH6unqMmMQ63PcrGeI2+hjEomGe
VVaqL85QReadllTGnpygA4Mk1N7gctPSjQqbX38et1Ttu/SiC3n0qWeS0K30ASnvIp+YHTRR8WyI
STcNMRrjAtksHjESF0pqHWVMYRjCJbYnNW7ssphXHKMW4xzfEiRbwsDLlxe9z6+UHWmI8Yg5/JBD
+fZ3rsOK4hJbqvXuTc+V2pVtl02weBriaw7f5hk1UvC8aqWxlwMkKSeQlIWWNASyeG+HLrFferg5
mzJ5FaZOa+TRxx4HBOP7lOa5my21qwpVIme6/56g1NXWJBJ9/8JYhzihdw+HaszR/3cI1hawahNT
SHLxCoYIlyUoyyDtX8oWbrp4+7eA3TdscTNY1lhjdb76lYuJSAl9d990xLz0mqjHSZEtIWFyWBob
snjGK9r2hhvKxy1YrE0l12Uxr31H77NdrIRf3Grr63jqb48mM9sTu+js1C0jBhWEwek2mUzG5RYs
1RUNDhI3J2m9GU2DEIzvQsL+kwm9ABoT1GTYdttteerppxOhoT9GknJa0jtdEZQgCJxE388FMMQJ
vUNHRwtHHX0QL730PEHgJ0XjNAm5lMTEomC8XnvLLgv01c5XYuKKbWtmzOhGgrqkXonYbrb0Qbdl
EkAZ0U+ZIcqIxkZEPPcALkWT8+UJFU1yCIRcR5tjrstpXmEAc0t386u9zK9Wbn2Y4+UNRVDjE4lH
w5jxmNomCtZj/sIlfPjBh2BM7/1vhyuS7OtCrpkjjjgMVYGgAWwA6vdxSy0Efp82RRg1aqTLCegn
hjihdzckk/HJ1sL7/57L3Hlzk88ENR4mU4v6NeTyMXjZ4SFFiMVklK985TL++Y/ngQyVpqHuNlP2
2nUbO2bMMnNgflqwCJF4eDUNLMlFFGIZPvOaotr8alqaqi/zO1zm2LE2EY/58xdgLZz6xVM54rAj
efTRx8AY4m57PQ93lLSu2toatthiS5djESy7iqKB7yNiBhReOcQJfalVYBh28KMbv8MfH3mKbKaO
1JLbUbDgZTn99LPYftv9wffdNpQhQJRj9dWn842vXwV+La6udQ8bqa+gu03wfJ84HvwHS0RWFpG/
iMirIvKKiJye7F8GncYMSEBzW56XX36dvfc+YPjMa4pq81usXd7THPc0v8t2jvsLFcPiQjtPP/sE
d9x+B+tOH8U1Xz2T6791MX+87zYOOeRACEOCTJZKfWeIQo2TsNWrInlXmzsDksFTl0R38gkn8evf
3w9+TQ/aeRVtrh+wVslmMwNKCRjiT055QauInXafwcGH78xbc+az0ioTefqxh2n04JqvXsw6U8aS
NRGEoZuIbkIdlzm0vIhZcSedy59aPCjEtLTl3eKI21laDHQR9AERcJaqPpck3DwrIn8CjsJVPbxS
RM7DVT08t1OnsRVxtVVW763uUUo8Hrz7Ic4+/QiuueB2RmYs6BCY1+IgU2m6fH4716TvOr82Lrja
KkuJZTjH/YJV5c8PPcRK45q4+orT2X+PnfCJ8QrNpFEilfZnGF5+IykNt5o2mXzmAZGNaGqo58l/
PsvnD/wCy0rfUrUYM7BfHwaEvvTe+m2svNpE7nnwAZ57+jEevuvHTBhdj4fFJypbV8tTckgjKKBU
U6f4X3KIxWgBQTjokEP4pK2D0YMwE94AF0FvSApefZS8bxGR13ANZfbBFbwDV/Xwr8C5lHUaA94V
kbTT2FM9nWfJkmamj23gphd/j9gChB2d6MXyJvLgmsukIZOl8N/e5rfJl0FRn5fVHPcXrc3NzH76
Pmq8kDjuwIRLIPUcqKlC7Ic6EiZsKQVcSImpO79X8peI62ZnQxCDJwESZHj88Rd45533WW1C3TIb
5UDv5hA33VQ+0Cbj05FvZ1RTA9/8ykVMWWEkGQr4RC7zTYfCwuoURpcsGsVgxaDGhT+mWHfd9Vi4
YOFyGOfAICJTgA2BvzMIncbKG9BYtZx1wjFIoQUT5VymaoXpaiggJfTl8+vm1opBO9WuGG7z21dM
XnkSWe2AqB1PQ0QjV78HcPcIim2VyrehijSkFdzYxQMJsOpTUJ+QDBFZYqkhIgNBHWQbIdOABHXg
Bfg+vPjCCwDOCT3IAqeIYAfYA3qIS/TlEOLQsmDuHK48+//Y5bNrQ9SC0VIIHmilEgDLgT646B/w
INvkwq2MRxRGqAhhIU8cdfDxvE/4YPbrPPCnRzjqiMOAOuLY4g3Ao56iEIauh+cygog0AL8FzlDV
5vKkmJ6qHvaE8oqIG6+1mmajTxAvvQaDCyeVTvOqy4nup+GOBjJ1zuTmZbFRTGhd2G+Y60Bt1GV+
fX8McT6/VPMLy36O+4qG2izEHRAYutTM7ani1lDh151RXMsCXgBeBoIGjPHwo5g4aXJkUeIooqOj
g9aWFmbP/oD29g4WLFpMmIO11/wMkIgByyDU2zli/+MIvSvA6+pP13HoAQcTd4TsdOKZUPiE0GQw
ksVgE4kekjqhyxEuxvWNN97mlt/cRWQNVnz8bIZMNktj0whGjRrNSitOYPIqUzn3rLUZ2VCL2gID
oJMVaG4eWEvGvkBEAhyR/6Wqpt1Suqt62OdOYxXn0Ig4ADTj3I8VElbZvC4vYiGJdhFk+eZV32Jx
e558ZPCyWTI1NdTX1zNi5GgymUyX+bVROCjZostyjvuDdK4UQSRTbOherCnTuXkPDF0iDxSNG0GW
N157k7t/fz8LWkNiC142i/E8/CCgvr4eP8gwatRoRo0aweSVVmL82CyrfSbDU3/djmzgFZ/lZVHv
Z6DzP7QJvcROgBLBSD2ysJXbbv4JcZgHrwbP2qR5QOfvLUdKn4Rcrb76Knz9kjN7PdilzDsuvTSL
wjOGjz/+eMDf7wniKNRPgNdU9Zqyj9Kqh1fStdPYr0TkGpwztm+dxsTgEeBqw1T7fAio/gLYkHPO
OqkPqnlpfhU78PlNzrMs57jfEMEUC8IpplvpdXlpX/1EmpuoMdOnT+a0U45HvQAhSZIss88jrt6M
MZJUWk2EEBsXzVdmsAu6iWBtzOJFi/4TTTdOVVZV/vmPZ7j8K5fj+x6qNin8JEPU7peMqbexCUgx
EmPpr6O1tXWpf6MbbAEcDswSkReSfRfwqXUaG2Ioahp9n9/BymVdhnPcTwiSUMehkac7CBDARhgD
NVmPypIknVCe0N4lW37ZmNba29tpaW0dkGbYq8FQRG4Wkfki8nLZvstE5MOkk/wLIrJ72WcDjJ/u
dgSICPfddx+TJ09GP/XKeMsQg+ikMsajuZm+d2TqB1T1b6oqqrpe0lR6A1X9g6ouVNUdVHU1Vd1R
VT8p+84VqjpNVddQ1SrF16ueaZBHvpwxWPOb/MaynOOBwgynRLZlis6lLAYfcWwHlCwFfYu6uQXY
tcr+a8sfeoBO8dO7Aj8QkaWIB0szBIU333oTtRaNyzr8/A9A8uAboaMAUVjA6NCwcvwPgwNN+kqK
EcIoLcu9vPFfsMASM02v26cRWaRKISzQ1jawr/dK6FX1MeCT3o5LUIyfVtV3gTR+egAQVP2kNqOl
aVQT2UymVBak8tDhFbI7yBBx5dIydRBH+bII7yEePdsTpJv3/41ILYEI1oDBUqX/yf8w2KgWHrq8
QkZFmP/xAnJ5iCLXtrA/j8XSUIJTReSlxLSTpr73OX66b0jTwoU999qTRYs+wUb/OabeQUOiPq8w
vgnfN/850vx/MfOuBgUaRkIcO63tf/jvQOp87cjliSyotYkDvO+/MVBC/0NgKrABLmPy2/39gfJE
mQULewgZUtfcYM899+C711+PV18/wCH/Z0OBSSt15qn/owb/MVDF+AFjV1hhaDb1EP7rNetlhXS+
33j33aLW7qn2i3gPiNCr6jxVjdVlbtxEyTzT5/hpVb1RVTdR1U3Gjmmqeh5BMaKJTB/y4J+f45c/
u5UwSuqw22XvABna0KTlneWTJS1MmTrZlflNQjyH331x9s7/0YkyKKjGYHyam1uYOnUqwyZk8X8Y
VMyd/zE1deB5UqpY3kcMiNAnyTEp9sN1kgcXP32QiGRFZFX6Gj9dFY5QOeuzEMct3P3Xe/jhb+4j
GDkp6dmadmYqt5cNN+I2UKRZmgpGePP9d2kYX4+i7o4MS/uNJnHISrHUwH/TlHaBuw9GFDyfuZ8s
YMLU8djOicL/w382Eol+4cKFNDY2DUij6zWOXkRuwxWuGisis4FLgW1FZAPcSnwPOAEGP366Ij5X
LStMns5aG2/O7x98mF02nUrGeAlxT6pcCgxrB2R/kdweG0XMnTefphFNQKEsA10ZTqKf49MJCaue
MfVpDmcIILkHnmtxuOCTT8jUBsBQaBT53zYXyx9vvPlmFfNs39AroVfVg6vs/kkPx18BXDGg0VRB
WTUVcmHEYivc8sDj1DVl2Xadz+BpATQCiVwNElWsLeth+V8ARXnttX8xcvPP0K65YnbucHsY2wsh
sTW4cjCJtibpdVQWC/uvQiLRv/Lqvxi/6nhyLC4zzy1HaKp1/w/LBJr8J4D4NC9pZsrUlSgy+n7c
+GEl/tb4MXGhhd0PPoJfPPI8x5x3BVFNE9Q0ui5EGDA+JsgUU5UHhN4aRHRpGLEcIYKXqeGfPMiI
0QAAIABJREFUzz1PEARDqPtQ/zHn40Xc/MATUDcKa2pccThNs59laCZBfxpIzJIvvvQSQRAMicYj
RTNb0VyamlBZ7vxn+CO9n0kLSRuD5/P23JaS6U60X+a7IV4CoXLN2CgkDAvEfsCmO+6BbV7Mridc
zLzZs1l/nbWYMHY0C957ndY5r3Lnb2+H2EIc9vOE/Zccu7qEy//qORTBfWLdQ9Pn05b/vgFreP39
T9jOthHZyBWaKhLG4fPUjRgzljm2kbW33ZMLvnQqe++8HY11GbAxamMWL5xHU0Md3kD7x+oAvied
zST9NykNrERA8h0RwKO5tYMXXnmV9Q7cCeOZ5NPlJ2RUmNmgB8/g/+T9pYMiienOegzYdDekCX3n
i1Egiq0r96vgNYzkwJPOxMYxURQRqOJJwE+uvwLiPKTpwv1ea50Jc0+3VV0tbqNlC78ToRcPbO8F
sCDJcq0s/+s+lW7Go0C2jnYLVmJEhrPkK4yeviZnXvszPvhoLod//VbmzJmDZ2NWbTCcevD2zNhk
A2w+7xok92detWeG2+3XVKs4tsv/7t2s5BzM/WHkyTkUR+gjyztz5vHhIqU1WuKYz3LWJItmNs9L
giLKTW24NV+8Tf8j9v1GhXsyRjyfmhoYPyEx3UGZibZ3DCvTjbWWOLbYhKBagQ4bkhdLHBg0m+Hm
X/3GhV3G0VKur4Qo+AHHHXecc4hVQRiGzsQgPmEMsRrXRi5T47YgC+InNa7dljYgcY0q0mbQUuIP
tbWl8yX7tLzhgHbagoCxE2sIwzApDZ6W4ht+UIEOG9M4cRw77LMnx5x6MieceQYfL2pm0003Q+MY
s1TmqZQw90VzU4QQIyFG826jgCFf2iTEaKH0ebrZnDtWC6TVr9S60rWloQhxFHXdXzEEBfF49qVZ
eDUQ2xjb3bGfIt7792ykaSyxyaCmvPF5gmStput2IBUX/wcHa52JbNQoLxHk+n8vh7RE3xlRFGNt
ZVliQYoZYrEqfn0jXqYG2lvLnuOBUHwLXsC3v3kV137nWhevnkjLxfICIgSNjbTnCrzw6mu88uqr
vP/+e8yd+xH5fL74S8b4jB49lgkTJjB58mSmTZvG+PHjGT16NDWZDBTa8eJ2VC3WxvgFy8KFSxg9
ejRqQ6f6F+t8dx1prq2dVaZNBSxCqtZbWGbdK5cdUj4VJze6EMeIVV545bWk9IUuNR9TVcT3QYTj
jj6Sm26+2YXrdkIYhgRZHwQ6Cu0EQYARg4gimYzT4CLFeY9TjcwWaw+l2pkkJjRXFkUdIy8UII4r
LqNCe0s/SL779nvvMWJ0jWMIxS5W1W+CiNwM7AnMV9V1kn2jgd8AU3CRcl9Q1UXJZ+cDx+I40mmq
+mBv9zBTW89PfnMPR8zcl6xE2HwrBuueExSMKcUDWAa9Lvt/E7xMFoDRo8fg+z42b5F+mi+HFaG3
NnbcLUGaNFC+3M+84GJ+ftdDHLHbDLD5fuosqWqfhGt6Pnf9/u+cddaZoEounyeoqcVraGDWCy/y
zauv5uP5n7DvPruz7dZbs+vWm9HUtKPrIlRhaTFYC3Ec09bayqLFi3njhad54403ePLJJ2ltaeGm
G29khRUnELe1Q6aWAw8+kT8//Wd00QJcdnAnL5ckMfRqeP2DD1h7/bXLIlSg5wtPf2voKXTF0StJ
GdxqDDwlcgNj4CIGamr49lcv7zMT78jlmDVrFu+//x5LliymUCgkkV0e9XUNTJg4kUmTJjFt2jQa
Ghq6MHJjC2ALXRh5GMd4KRGsyswVTIbnX55VhZl3i1uA7wE/L9t3HoPYyD31p+xy1Gl8/P4bXPCl
U5mx2SasPHYUQeC5+xnmaWtZQuCBjxm4b6UCgxQA0cX3At1LD30/39KXbK7U+Nz1GppbO5g8dQri
SZmPpu9jG2aE3naJOKiYc4VJU6Zz3rEXcsQ+OxPlYnwGEqGgoDFhR45jTzjMdYoRIfB9/vboY1x2
2fe49rpLuPkHPyLwDXjueIpRCNX6GRpQQ1NNEytNWoF115zGjjtvx8knHUchl+e3d93DT2+5nVt+
9kPG+lnuvu8Orrzsq5x9+hcRse5CE/unppKhGKznc+2NP2LTfXeijY8pTXzffAJDEamG1i0DrxHI
5fr5qykxdbbyxx95vF9MXGtqWHff3aipyWIMpYguFVSFOLYUCgUWLVpEodDRhZFvv912nHbWmV0Y
uYkWgGiJkZf7AyQROGqyvPnBPA7abetOzLw6VPWxpLdvOQa1kTvAuFWnM/OYE5n9zttccv3PqMv+
mvXXWYtx41YgE4fMff9Nlsx7l8svPIt1118Pwiix5y8FBql/sHYVnegaMtQXoan86CTctF+BFdVH
V3F+FT5etJiR40bSEbWhaL+DWocVoY9jS0dHRw9qoEfeGk7/yrd4d34rK42qQ7V1AFzWTdgbb7zB
FltuVbSLicBWMzbjLw/eCr4PGjlHQRfiXs155x5Qz/PRQlJ9Ls45E7sfcOCBX+CAmTP52c9v5Yij
/4+GUaO5975HOfuMU5xkW2aXc5KnARUKXg0PPvkaG83cir7ztPRhGZp20y4CWycGTv4T+v8kpdcb
gxiu+94N/WPiqfmsmLlb/rvOPh0FMG7USuB5XRj5kiUt7Lz93l0Y+XkXXYhtWdglaEXFuZo849OO
MGZSAxMnT+wnM69AT43cny47ro+FCIXID5CGkayy3sacvd7GCK6nqaJcf+ml7LfjVvzkxh9A29wk
Ai4eiD+82/N3/aG+rmfXCaoygCJF+d/izGS2v4OuHliBSJd+Gl1zfcq9sAlTz9bx2tvPs8Kk8WUB
F/3TaIee7t4DUvtn984IwcvUs+8Rx3PkyWcQS4aBrSo3saoWbMHtEcEYgwk88A2OYNiSJN/r4CGN
h65I5pLkumyMETjqiMORJP1/5UlNTknvVNrBiIeIj5gM/3zxFQ47YR/a8y19vzoxeN4w4fFq6MzA
rfpLkaaj4HnMmbuoWya+wTprEhCBDSEKnWM/jpO6Qlplc/v9IACraCFEoxg6cmihQOAHjBkzhvvu
u5377/8Diiky8rmzZ2PEQCfhRRU8FaxkuPPBh9jzoD2J/f5qMd3cAR1YrZDyQoStLS1uSYuTL2Ij
5DUm9gS/JkvDyFE89+JL5PIFZ2GM45IWNGgYSCRVufOj0zx2jnKQsuMkFeaqbKkZtTzA2mrXOyyC
jePK0/RluFHMvAULyNbUEMVRYr7u370cVoS+iO4CFFDEeMTGY87Cxfz5sSdYGsl18ior89brr9Jl
VtKC+P1aY1UWUtmik2Rz5n3L7PfeZ/fddquqYBbVVxVu+OktrDJ1CkEQdDpXdxA8ApoXtiADiStf
Lqhk4MYEDFwsFKitI8ozyEycotZVjZGj1Rn5mFEjKdb1KYMRF8llMvV8+ZLvM2JMU7+YeRXMS2tU
DbSRe3khwobGxtJlp85zI2DEOdCzNbzwymt8MHsOJukrW5yyQVQkVR3jTqPjWttau42QA7BWKRRC
MD5IQEchJrRCjIfFRyWATC1k68HPggTgZcBkXFJmslnxSxseFg+VNPqoNP/W2oooui66fueopGrk
obaGt997Dz/wOznj+07bholY55DejO4leiXIQHsU8bWbbuWEow7kwyfvhFxSBrnMzt3d951d1KlF
jaMbufmGH7LFZuswcvSYJDKjmsOsM6oQ0G7OK4lsqonrUYyP8T322+9Y/v7UvRC2UTGZ6uz9FijU
ZHm/YwkbmFbEpnZB2+3QPN9HrMc9v7qPs085h9c+mlW5AqQ6URORlXGOvfHJYG5U1etE5DLgOCDt
WH1BWbexfkdyVD+5JlEsJQZOpgZyedJ56ucPQkcHo0fCW6+/yhqrbN3lfP0fI10IdacPk3eKMUJc
xsiDbAY6cnR5YFVwUUew8vQGLOqyYjVNAOz3OAe3kTuVd77ceQ7g1dbj1zdy7XXf5YavnYWTfJN7
MWiSvXUEtcyx3tA0oopzPSGKIpjAI9M4hva29qKT/Z133uH999+jra2NJUsWE4ZhKWIqcbbX1NYy
cuRIJk2aRENDA9OmTWPUqFGMHj2aTCaD7/n4ohDlixF0ImAyGUic72PGjyfsCDHGlMzJ5eumy21x
6zvX1s7zL89ixW2mU3LG90+AHVaEHpxK1B2hj+MIz3iIWrbcfmfO/eo3+feCVlZpCkCjqm6WKmco
HhDn2vntXb+ktaUFsI5+LyOzdjrxYa6d0LZz523fLovBTheFONstEIph63324egLvsgSliAVj1k3
sAqRYf999mKHbbfmqR88TsPo+r6UTYiAs1T1ORFpBJ4VkT8ln12rqt+quJYBRnJ0j0oG/vQr77L5
2iv1g4FTwcDRiB9c9zXOPvuiATDxbmzD3XwnZeTune3CyAutLWS8VBVP1X3HzGNPOPDUL3LoKUcQ
0e7su70wc6C7QoTLpJF7ubegfEwtra1svd32PP/3P+OSp2y3gkT/UKYWCKBC3NrOnx/+O2edew6a
REMVna1J5IoiWGv54P0PuOOuu3n59TeYt/AT/IwrlzJl8hTq6uuYNm26E4gSRqEKba3tdORyvP/+
B/zzmWeJ45j29nY849HU1Ijn+6yz9jrss+furDZ1MnWeYxDWxniJs/68Cy7i2muuJfCDMldr9wJr
kY4LtHR0MG/hApamlN2wIvTWKrGNuylWJkRhhG9AbMySgmHfY07hyK3W5IGbv0mNzaPiJwSxbzfM
Zf0pDQ0NSXzwskcQBATAKpPGoVE7Ioorc+AWbGhjgvosr7z5Fmtu/znaZQmoRaV3q7WnHk8+9k9u
v/XHtC9oR/qYeJE48T5K3reIyGv07LAbcCRHlbN3YeA7rTmBB2+7YcAMHLVMnbbqp8bE0/MLXRl5
xpfEPFSSOlNr8JzWdmx9jJU24uSYvsjC3RQiBNihm+OXqhChaNfE75aOdvY+6FCeGDOKvBlBVtvB
tvbCRHs9U/Ka2tcBY/jaN65jlelTi0QeSbRjhL88+QQ33HQTcz5qZ/c9t2arLbbgjDNOwmAJvDIN
o/gsdHLGJky3C1JTnRFQiKOQf73xJr++5Y/cdfdDHHDA7hxzzDFYC2Gs7LbHXuy25+E8/sR9xB1t
gC09f+UMUEo/LwhWhPsf/SsL22IKUR6MpXKx9u2GDhcjLeBMNrYHgmvVqcaIJfYNzWFM/fgp+LUj
3feTf0MemtrsywhAshnf564HHmLvg89jgy02IFbFqCD03jB6yeJm5s9ZCHgUwg4knf6itNs7krC9
DYG/J7uWaUtJEZ8ojMsYuLLtzGM48oxLyZHUwXFH9sNdUnLAFZn4p5S5GQQBddmgyMjRfPKsOp8L
KoRxjKnx2Wzvo9npwF2xEmIlRmUoNAXvimph7ZL4GPb7/MG88sbbENSQxKUO4old051ZL7/CZ2d8
rmy/EkcReD6XX3gdMzbcmOu/eQlnnXQKMzbYiGwQOJ9Wl+benZ3ttsu+KF8gDkOXJGcEggCyGTw/
YNUpq3LkUUdyxBFf4PY7/sBxJ5zgTLKez8677s7oMQH4PQeIKI6OKQLGwxqPvz7xNyas1MDSSCLD
itBba7uGLHVCQ2MDiBDHIWieq39yO+dfeQOIyy4bbL//MkHRDFFyutjkrd/QwJe/eSOnXHYUqosx
mnTb6kU5ExHCKCaOXMZsPhBiSae/b3G/ItIA/BY4Q1WbGeSWkk667orODPycr3x9eDLwFBWMPPUz
lIwfKTM/5PjdyGkBwccQ9YmZDwmoi+rKW8M6n9uOQ049dxCipbqcxG1VIqjSKCpsxF8evJXTT/1i
MZLK2BDCfB+jqboyAD8ISiHSsXW+oo4cqKWurq4YKn3ffbdz1VVX8+Gcj4pRVhdcdDFzZ892voIq
kVZAMXRakoirNHx6z4P2xMrAcxCGFaGP44g4tj06Y41nULFYjV1dkJqAB//5AgXThKf02VyxfGE6
bYJRA+Jzzte+w8kXH0vt+EzC+ZOj+nBZVpVFi5cASm1tDaIGz3hUuvirQ0QCHJH/pareBTDYLSUb
Ghu7PX85A49EhicDT1HByBMOLoIasCJFZj55jYmIFhANETyGh6XVzUQQZLEYIi9A6kbw+wcfTgKY
BnmmkqVbU5NxZ0+EQFdGwrooqvKia6RSej9MsRVRMO5NF2FTScK/LdY6J/HIESNYadKK6Ye0tLSW
VViq/rwZjDMvq6DiEalh9XXHUT+inv4VJu78u8MIcWyJ46jHoj5+EFSEKsWiXPHDn/O1H/wKrD+I
Hv9PEYlqP3txB/c/8zRSL0SSw6oj3k4u7MNUKmQyTnWsratj4YIFeMY4WVLptrCWuFX9E+A1Vb2m
bP+n0FIyPRmoKFYtsbXUjWji7gf/BEEdHjpMGHgK6bolAV8xHq+9NZstd96YuMz/INo3Zr784QZZ
KMQEmVo6CrDHfgdw5z2/x/ODXr7bHyT3ra6OqAC59tbSJ2l4a0U12dJXlgo9yETlTtZ0i6Ow6BP8
x9+fZtSokRRDpqulM4g457UX4AU1PP/SLDb73Ax8f+nqVvVKHURkZRH5i4i8KiKviMjpyf7RIvIn
EXkzeR1V9p3zReQtEXldRHZZqhGWwdry8qyVNylV2Tyv8pKyYvjMWhvw5Ktvo/UjULzSt4ZsHHli
ilBN7LYuaejMyy/juDOOcppKJJ2Ekp6ogCBqyPoBtTUZwCOQWjz1CDSLb7P4tobaoKG7H9gCOBzY
XkReSLbdgW+KyCwReQnYDjgTXCQHkEZy/JGlbCkJ6mKIk6zUCMvifBtHfOlC3p5fgHi4FW/rTOhT
eLw852N2PuxkPrf7VqinWK0kH8MCoigRftYnUstJ51/K5E22IKoZgRifuJAjLBTSg+k79dXKTQRa
W9hr1/W49PwzIOMTxyGaZjKjdMl56fF01Q5MIrrE9rq5/tYxBoshRjR0r3GB6665lj8//BiBkaRh
S2q2K3tu02ddBWrq+ONT/+TgUy5k0morERKVyajlpr++oS+ULg2tWwvYHPhiEj6XFklaDXg4+btz
aN2uwA9EZKmexJRDR5FFk+gT1bioKmliQwvDqJjxaUQQY9AoJq8hP77/AVbf+SBCv7EY2QCZIUrs
lSjNtLNKbIVZcxdix9RigxwqHcSkceSpM0wxidRXGWlo8CSg0BYRSB21tTWce84F7LPPfqw0biUa
vHFcfemtbLzmbrz6zEddRgKgqn9TVVHV9VR1g2T7g6oerqrrJvv3LkuxR1WvUNVpqrqGqj6wtHfE
L8/ktYqncNixp7LTzCOhps6Vih5uKNIsATEQ1LDX4V9k90N3ZFHzIqI4SaaBhMgPE0IPIOqammMJ
xWOPmQfxzKx/QSaL8TyC2lp3XH+1FCkj3gAGDj34C4T5mMUfz3NReX4Vc+SAiX0/hlYM6kz9Zu41
qMnyi1vv56QT/49CPs2Z6HThWvoVK0JOLTfcegurrjWOguZQbFm8QO+m1s7oS8/Y7kLrBr1IUu8w
dFeK26qiassq5ImLuccQG2VeexvX/OYurvjudVx6yhEYbQebWxpH9jJFYAF1Urs01LHHMQfypatO
Iq/N5Wui5/Er2Ng6tTaC3/zit1x28UV8fuYuWNowSZjWMUfPZMbmO/LU069yw/cnLOtL62G4mkhj
SXBckcFHeInqKknonFHIxRHX/vJ2fvHg48zcZkM8QjwjGALAAyn0cLblCSUUJQDSBLjYZPjV/Q9w
3JcPYuSkEeS0zd0LTWURWxRQhz7UlXAwHtgYi1SExU4a0YRnc6nFivKF3Dtp7US8O4XKZmqzTlpe
5uGy3UPKr8UY2psXcedt32bylFUhSnpcFyPqSBh9Kaw2zZGZuPoqHHbk51nCElRlqazO/SviWxla
11ORpEEJresPjLgKgqWCZ47rWQxiY2qytUxdZwaFldfntr+8CNQ5KaoLlueTlPoWDOBStHXUGFbb
di/O+Pr/0W6a0WJmZPeqvCOETsLPtbSjBXj4wcf429/u4YCZW6E0I4S4ZVUAlvDUU4/xyMO/W+ZX
2Du006vzzXiJxJ62SBQgFMtqm3+W6+/+IzlTgxHB+AYkvbahCsWvcPAJrXHM1b+4iRErjaJADqtR
1Uii4SDXCy7/xAh4KDHQmo+IsiP5w1+extSOAM8nzR9IyeKArqtzqGx5FM2QgFKTCZg0cXxSciNK
TD3Fjyn6aPwANWBqs8xphc222xwN3FrWqmWV+44+E/oqoXWlSxlAkaTysLoFC5t7PLb30gcOqbe7
Yl/yp2fBiwwHHn8aX7r8Ksg0QmxAvDJFaAgQ+TSOxniECE8+/zzTN1gV44PRqPhY9Gm8CjZyKdNz
Zn/MqMbRidff4ixyTpKKo3aQDM89+8yyubQBIvW72IokOU0kHwNY8sDN9/6Zadvsg45YmY4wAFXi
sH3Iamuo85mgrjZK3NDEujt+niPPPprWaDGRdWY5Rbotvd5T5MbyRSk23YhbawrE4rHjXvvzm3se
YEkuJiqEoGlg7FBnXUuBlOEZBZuWaS75XUpqjVDI5/AyPrNef40d9v4cI8aNpCNqdz9TDMUdGPpE
6KuF1rGURZLKw+rGjmnqyxgodu/pRMzLCwhVFJQieVzE2TgLGqJBlr++NptpW+5DmBkD+MUOQPFy
04sVKzEFIvKiWONhxeevL8ziwu9dzR6H7IzVvBMExLgiXNKbGi+0trVixCffEfLbO24htouAHGAQ
aoA6YCyelwU+5u03X/8UrrU/SBk8XUpTKy6qwmAQr47jz7mY39z/CNmmcYBf7MrT+beWL8ofcANi
aI8s9z/6KJtsuwZkLJgYKVfre8BQJo/WWowRRJVY44r8h9PPvxzx3Pwoioqtqr38RyCtWIuWEfnq
DoPOyZA5LRQTIl0exTIk9N2F1lEqkgRdiyQNamidlqoTdTfK5LhqD4hN/NMC4jzioV/LI6/PY4uD
T+G51+dAdgxi6/BskEiKny4sQijOXeLZGMTnml/+ihvuu52Zx36BkBwqSUVDpBh93TOEOFIymRqe
ePwp1lt3IzyzEh+83caPv/9rDj7gSGbusw/HHnkIL7/4GiDMmztvmV7nQCAiXTQ1JyG690EseAXD
QadfyDPzOpi86Y5QMw6ocaY5EVJ35vIj9u7cisWRNA9rAuLael77aC5X33IT2+yzCzZsJ0CTPBpX
qqM3Zj5UYa2lvr4ejJPprY1RY5h5xPE89twbSFAPeC7QZHkPdpmiM+0qM74l/J4kvtl4hm//6Mes
+9kVgXaEKHnOEy1/KdCXDIw0tG6WiLyQ7LuAZVQkqRrSjDdjvOKDP5DfADAaU1CPZr+OO55+makr
BBy64/qcedzxbLjyShhCIKQfXTyWGgL4VpxNvrGJzfeeyUb77Mime21F3rZjxC82RO/Pw23V0NEe
8/7784AsW2yyBl//6oV87rPT2GabE/H8DLV1K/CVr1zNj37yExYtWrwsLm+p4Uw3JilWBaSRDeI8
DZg8YUfISRd8jRPPOJ/p667KE3f8hPEjMqgtYHEVjpZXfFXqLSokmY2BeNggwzrb7MUqa09gv2P3
pSP/EX4mcG0O1boSKsOYAioW8RImKxDbiEIsbLf3/iz85BPemtvM6uOb8MMlTutWGJY5Lr0idTSX
e1dSk03JbBPi89aHC5i2+YbM2PFzdNgFznSnLkNGtXszXl/Ql6ibv9E9dVkmRZI6Q5JmyZ4xGJGy
2OIev1V1rxHBM0JH2M7rs15i+/02pDWIOeEb57GiN4pbr/8ejaZQNfqpx/tcrpX3ByKAR3Poc++f
HuHyH/+A4750MLbJJyq04/s1WLXoACr/GePT3NxGJhD+9cqz3PTjq6gNQkQKqIRYbcVqA0Z8wKe9
vb3f51jWKHXT6Qwnp4s484CopS0X4nk1PPDSvznioD04ZNt1OPKgA/FaF2NNiC6l+jtQKIZQAnzy
xHHMxx3tbLT/Fzj3GycRUSAftZPJ1KMSIeo00CRidtjCla0wrtieOK08VqU138G2u+7K7dd/hXOO
/jwZlT6bqoYvOl+bVL6KR2h8fvrrO1nvsxtQIF+hf1b4bQeIoRhE3i0q7e8pV0wSDHCPvmcMGWvI
WMHXtHJzGt8qKAajSo2B3999K6PHZjCNEVM3nYq3eh2bHrk3h17wNdpkLGRHgnrkwxwdYa7CXVph
CCifAU1HYpPNEaQotCC+i/e21hVFqmlgdksHe5/6Jbb5vwP5/ay/scK08dSNyGBsSOAZlLSYleK0
jKjTCRPJoMpiEgyLFy2mtq6WZ599joaGDMbErlyxNXiJfyJfKAAeYfTpaTGDCUWoyQSoEQpiaMvU
8nLzEn71ypOstdP2XP/r32CaxiMasFRi0UCQ+lPCAn7taM7/3o856CsX8MVvncxibSbyCmSCjJPY
+pOWP8Qh4ppYl0PFJbs1jBnDz+/6Ax8sbAdr6DZm+j8eCrHFBjW8PvsjbrvvERrGNCJ+Eo2UBqHA
UjushxWhN55xRfvLGjOnBK6YVmxKVi3FSRLlhN6SFP0PIx5/7BEwTloONQ/1sO62axGt6LP5Qbuz
3QFH8ZenX8OrG0VN3QjnEPQ9xAgqhjQXrrNTRVGs2NKG4Nc1QVAP2dF81Obx1Wt+yg477Msv732E
WfPmsNaMz1C3gs8LL83D90fgkwEBm5iQ3KQbKnPPek/usFYZOWIEhTCs2C9q0j7ZtLW3AcEQEarK
5raMKBuRpEpn+q/yO4rgCfgSU5+JmPPWy4yfXMem+87gwbefZcqMbXn+vXcIjesIlAoIKUsuRxdr
fhXOXvpX7bj0jYAf0Go9fv/4P1hlxl78OwrZ79DtMbqAGqMEGBSDFmP+l6cvYfAgIpVJblBMdItj
OOXcr5WS3YJgeCa8DQRKaW2Li657atZrFYly+XyBOEmWS+tZLS2hHw5VkooQkWJTgK6fgdoY3xN8
33M3SEhq44AxBpKQWxGor6tj3vz5QLFyQxLOZ9FsnnW2X5f7fv4iK0yZzCmnn80bb702ruEbAAAg
AElEQVTD1ltvx+677cqkFcczcdxYvEyAFgpOIklLnlpFggDCkEKhwKJFS3h+1iweeuQxXnxpFhNW
GMOBM/fl6MP357xzv8SEzXdj56M2wtgWYhuz6qoNLPokT7audI026VYj4hhdFEXJNffMp+PYsqR5
CaNGjepSx0aTWtoiUCgUAEMmm8FF5SxnFBl46sR0kVa+Js0goCLkKM0aFU2MHjaifpSQK7Rh8Bgx
qYHJm47hgNPO4/qLLmXP7beCjmaI8xTCDmKgNqgpnrFyLJ3/1q7hTiYgyhfwfUNUKOAHvmseH9Qx
e8ECTrrgEl58Yw6b7bIes+f+G/HWQmInsNiKsLlUa1NcSzooaWzdDWh5oZpxgWLlSKFrpBRA4HlE
hZjd9tmPe399M+pl0UJH0TwvqeNRhcFpVDIUoGV3qswikQQLfOfGH7Hy9JGsue7q5E0HxRyQLlLE
wDGsCL0xxmU+Jl1jECUIDKqWD957nzvuuI3f/uYHNDe3ka2to3HkCKat/ln22f8gNtxoI7LZOlQE
sTGiSntLc6IulxaUlaTOncTscfBGXPndq/nxlVcixpDP5Zn1yqs8+/R7/OMfz/LGW2/T3tFBe1jA
JnbIwA+oz/hMmjCB6dOnM2HCBDbecD12OPdUgqyPV1NLmGvDNNSyyxGHs/HOqxDHzSDO0bzeeuvy
9N+fYNvtNykuCiMGG9fR1hYSxzG1tU3U1WUohIuq2K9Tb4IiRsnnOhg3ekzFfgBEigXC6hvqgA6a
GkcAPec0LHuUNBQpppJ30tQEF7KWCv/JkanmFuVzTJg41lUwVccUx04dy7hVJvKjP/6co077Cifs
tyM7bvM5ttp6fQIsEhfAGMRarCYNw6mm8iYGuSKx9/Aw+HUjwPhooHy0aAk/vvmn/PWhP7HzoYcw
a94ctt5/Q0wgvPDIPI7wR+DHi7ESYylFFDmBxKXvq1bei/LzDwU4xaWUxVz6oJTR7Hl+cX2aJKNZ
oxhjhEJtxpUlWXsyd/30h6wxvokgXgK+53L4CEAL/wHE3jHEKGF+vuIEQ2MIvSz/+vAj7Jhajjp2
H9riZtR2kLYWKf5C4rApr/yQ/nJfMawIvec5DU9EUOvh+T4vz3qan9z8PdZZfyLrbDgaL/AwjMJi
XGVHfZ0f3nAaH/x7Hh9/vISNNtyCvffan713O8AJSxqVFpPiWo+pISZGsgXmFD7mpXc+ZLM1ViRb
AzM2XxeDsPce26PqwsistQnxccyoaF5KaSpxkiwRQdRKkMlw58NPEI4yjFuxARNHWDwEg5/N8/B9
L7PjTjuQy0c8/fRzPPjgU6y0cpYxY8YgIsydO5/W1hC1cOJJRzJmrE8YNYOtVH8FaG9vZ/T06URR
SCpZqLGuVhAZYvVZc8014f/bO/M4KcprYT+nqtdZWAQEZBcBQVZFFhUXZBfFLQYSt2jUq8Ys+t3E
JZ9LNNEk3725Wbw3McarRuMSo1FxSQxiNFETJYqamKCRRaKAss/WXcv5/nirZ3qGgemGGboZ34df
0d013VVvdVedOue8ZyFLPF4ep4Pruog4+F6UVNPCUjPhemGrlpqgbFi3nt59+kB+/XYVcDwq+yWZ
euoYug/pX7y1JgJBiBOPg0J9XS0rV6/luRde5pmlz7N508dMn3YUY8aM3MFiC4IaNHRatdhM6YdI
ExYXx5E8q60s/GnFI0QKWdOKfJ0kcJS6wKf74CF89cZvct/3vkW1BiaxSMJILymPm1p7EMsJaYVc
c+86L8t137mJaQtPoD7MEBB02G28PK7sAkkmksRjSQI/QWVlmmuvvYz+/R1OOmUi6tQADVF0inFF
mH8eAwa69O8/gJg7DN/L8vJLd/PEYz/BjQPa0CToRTF1v034XkBI3xEHcMpFX2Hty79Baj/GCbNE
dwhMvAzkOpIBxjhodcLPJMgQT1AXKJd+8z+Y/ulDaQhqcHEIhKiqXQNBANdc9X167p9mxMhBzJs/
wpRfjobZf0B3oy2Fwj333E33/brwmUWnAD6qQZ6mG+L7Wbp16xIJ9pAQF8dJkUpWU1sf8v3v38GN
N5kAqXKZDFQCwtBHHOW5pc+wbNmfmllqPXr3Z8CgUa1basDGjz+muqoKZBM0TmhJo1ZV0SvOd2+/
k9dff7lwaw2TZpaMx+jRtZqDhgyla7eujB8/jtNmHc0lZ50aaSJOqxabIyYsoDWLzbS/i+F7SWq2
1QOQTnchmfLx/dZcaW3GgJWMxnmxXDhso8tQI8vLia6upqzmPzy9mKHHLGD9a0up37qBtDRALmgA
KddDLRBz8kij5SNRjf5KxkyZywlnHYVf6ZHx6nFzhQyRqNftrvMocjOChbBPCfp4IkUqXUksDpd8
4Qzmz59AMrmVkMiFISatvHmlvxARRdwsIvW4boLq6pAe3XuxYsUK0Bi5lJrWApdDyXD8orEMmzmb
d373JFK3BdpKC9hhO9HJqi5hopqDj5jDlNPG0KD1CBCIgASAiyMOo0b25KDhg3HiHuJmMALc1D5x
XZfAD1AccGDylFFs2xZyy813ctONl7N9+0aULCKmqmfWy+K6Lmed/TlOO3UuDkI2GzJw4IHMP3Eu
N950MxXVScAhKHH0g4hDGMRJxAK++/9uwIltZfjwAxg9IdHMUvNDD2jdUhs9aizvv7+KysqkcS1E
LjWV3OSrg6f1HHv6WNas+Ffh1hpRHJPjGCHWOGpFQg/IEGQ8BIgnK3ew2FQcQnV3sNi2bq3lvvvu
p6a2gQEDehCPx3Fdl3XrNrBuncfUqSM45dQ51DesA8IdrLZyo5kO31oHJUw8uIMpOChuiqNmzG/M
bF40bzps/yDaUmuKR/ne5JqTP3+RcwIKdX5AqmsVi597jonHjmDY2INpoN5kRCvmui7i+Ap9Z5kL
+uY/asyN4bouL770LAcN60Uq7QNZJKoA2CSmpPljoxkYIBJHowkvo/m6NE2Atdw3QAgp8NLC6g2b
GVydMH8rKgcsN6fgsnLdR6R6uThxRdSPTuemMFDP8+jStSsNmVoqEopxPzhIdLdX1Wa12JQslZWV
uC68994aevXqiogX7VUIg5B0Ok0qneb887+A68Q4+OCx+F7AmEMPhnArqAeS2Gnjkb2GCqtWr+D2
229i7tzJuMmuhGomp/IttZi6IPWtWmq/faqWN5a/y8w548znzIajST6XnPDw3Ezx1hq5j7e8vMzF
6SaSIC51sIPFFuYEVwuLbb8e3ZgydTRKLdDk0+4/oDuCsHVrhssu/j5fv/4MunappKXVVq60LEUC
kZ0crXIi5dVVB2JVfPrCLzJ7VD9iGvLpYyaYNn+OgIY0VcPJn7Qu5y8gL1AgVBMp57gEConqSl58
7TW+esMtXHjNJTixLI76OKKRoG/U6dvVc1Xm4ZX5PTVB4nGGHzyUP/7hl0w4tA9KLUqMpsOImgA0
xblh7mUJ0DhhVHs+V/DOCXOz/LnPhHnPc8IBMtl6ps2bzOQTP0uQqjRlEhyJej62fcKpQNYVvGSC
CXPO4rAZR5FSj2Tgm/aGkfBRwInH6dm7BytXr8VxovuwxlGNgyRRokdNomra6zmxWo4+djS3/ugh
wtDFkTiOuog6hH5IIpEE8Tn90ycw78QZ/P6FJfxjxXuEXh1IPUaAaptF4zocgZ/97AccN308Tqye
MDS1uzX6o+ZH42iI4COSxZF6oIbq6pCBg7rQp28S1w1oll+Qm0TJvwjF55BJvfnF40+CE8v/6Zsv
+RjfRPMl96ZQIFXJj3/+c8ZPO4hsVGk033mhqvTqCYcdNpyJh49n2PCBiFtHLO6hmgU8EglByYDT
QI+eFUw7tj+3//RB1qz5CFMIrTwv2/w2frl5qubnVH5Qqpk6z6pHVv3GGlTLNyu33PbLxjpUYHS0
QPJrUZW3kM/Vrco6IZ4jjbWr3IpqJsw+iWt+9F1OvuAknIqGxhpWDm4RdazyKey7KGuNXsRHNEF9
Q4ZEspLPXHw+Ty59ndMXHoYXbgZi+NrClG0ZkiSZvFeC5uIzQqiqdtkxASl3GeV8a0ar9rz1zDpn
MkNmzePO66/iuInjkZwG2IYfUdT8kKdccB4zzxyP566Nfsh44940iiIKFGIVHqvXbmfU2JyP0ifM
yZRGAsCLhi6I63PiSRO47trbuPmbF7F928e4JMhmTDNwcQKgG7NnzOG5Fx5lye/+yHXX/oSTTj6W
wycfAHhs3rK57R+lA3l/zXucet5kYvGNoF5kxkamrEbPG6NRIvHv+CgZYrE0Sj2+n6GuNoMrVQQa
GsurlcgkswWPPof05uqf/oAjp0xicHUaNEtx5S+aTPN6SXHcaYvYFNRxyPEjUW3AAXxxEAlwcAjD
kKEHDaVLNxc3vhlxQsIwIAxdTHll08TdcUzSjB9sp+8BXamq6soD9z/BOWefTq9eXaMbdOlYu2p1
zZfPvWCXVfAOGzp4t7d/1U8fKObtPYGPd3tn7UvbY/lwE8//8bH22t+gQt5U1oI+p1Il03GWvfUh
Kz9YzbwFE/CCLCpCKLqTic+d4RipG4XPBWHTJCyAhoHpzh7tO9JPgDiCQza7nWmzDuOS62/mqbvv
ZGDXGA4upo3Yzm/BgcT4+aPP8taGLUw9rD+BmnR31dzFagS+ibxSXBFqNptkJ6dg5U0QR5h29EAW
L17CkVPHk4yl2LIlS+4W93+vuYHzz/8y53/u33lnxWouufQLXP6Vr/HCiw8AAfFYNVBbxPfZvnTv
Xokb3wqANsaRRxqzSN5vbVormhuARGXriOrUO6g6OFQAG9nR1yt5/ze31j54+Umk3o+EbO5jbatW
npjonwef+R3xgb05bGg/CNdB4BNIzIRQkm+xdeUfK95mzNhBBNpgJmo1DlEyXNO9LAlkETdLVVe3
0Wq79roLibvt2X91t/iHqk4s9SAARORVO5ZdU542YERIBaIu8VQvjllwEQeNHYCbasAT057Ml91I
2c8P8fJzAj5sai2p4GicuCSJuylSySq2bc3w0ot/5+GH/8bTzy0j2L+CqZ86l+1ugsAJ8uKmmuNl
Tc2cv733T27+xU8ZeeRInl26nMcffoONH3kk4j0Q0kiUIJIr0qlhCHGKbAishGTp2bOK1/7yLqFf
wbJlrzN7ziQaGrYCaV77y7ukk9049ugFXPD5yxBc5sw+DagiDBzj4mkFEUmJyJ9FZHnUN/iGaH27
9g0W8XEICNQhIEYYLUoM1bxev+IbS00aQIIomsOIU8XBz4YodbT0vRi9W3CQvJjk5tbac6+9gTqJ
Zp8wiS07WRBcFbb6AVf98Fb6Dk/iuWvxxceXeNMNSwUVMzuUs9gCTLNzE6jl42vQfKEOHx8vFAJC
NM9qkzBFGJRHlJSl/ClrjV7DOCHKhRdewYmnj0SdGkx5gVSkoxZ5n9LcpQ5u3MWPSgDEJYaIi5uo
ZMvmWlatWscHH2ymocFkZ48Z24tDJ45jasrFTXj4XhaZlGbkUWfwwZ/uQ7J+Xr2OJk00XlFFTUMD
p5x/DYeePRY/2MKko4YTC6tYv34TDz7wKgcNSzN+/MEEUVtDRQn9LF2qwHVihKEpDNW2+zwkJECc
GDNmj+cnP7mb1Stf4xvXXoWXNROaBx04CNfNkkw4aBiigU+vHr2o315PujqGBjU723gGmK6qNVFv
gj+IyFPAqZi+wbeIyJWYvsFfa9E3+ADgdyIyvK0qpmaWpMknXzhNlprx5dOUxyCKiEZC0UGiUNr2
stYQcCp6MmTMLKYvGkVckvih24rFFrVzbmGxFRcn39xq071dt8eyz1K2Gr0ASQnYHLg8+uqrSIUY
PzUuKkHkFi9A41WnaSE38RnSkKmlpgaS8Uo2rK/jxT++zUMPLmfTxwFDhvbj+BnjmH/SGObMG0O/
/n2Ip30C6shmM6gGeG6W2WdPYvAxiwgru0Ai0TiZF/ghxNJ8795H6H3U2Rx6zlS8oAFIEnPAiW2n
bz+HBSePYuDAIdx/92ts3liHaBxXFA3r6NEjgZdRk6WJFjY7I4qqRyyRJZ4EVxQHIchmAIcNH21g
e009gUIogkqC515YSrq6KyAk3KrWv0JD7i4QjxbF9Ae+K1p/F3By9Lyxb7CqrgRyfYN3/VMheE6Y
l3VaBC0+onkWmqhEzp4YMU2QcFLE3XSR1tpOLLZEgnGzZzH/80ewesNH3H/vX1q32HB2YbEVWlOz
udWmpW1sf1spd94CO5Y2KGuNnlQFi047lzlzJ+M7tQShMd8d1byJOr+NjeSRi19CiScc6jbCA/e/
yuGHD2L82ENITVF89RE3izq56IDoIo0idFwFcEgQkAkbmHbKoUw4dgHLlzwOmU0QxnBjKZ5f9nfu
WfIwJ503nky4tTHrEUyhIgcHJEt1tcPCs8ex8p31/PXNN6mrg0kTD6Rfn6FkMxCviDUWNtsVjcGg
Aq4Is2Ydyte/fg2ViTjZbAPgsWnTFlLpCgTwg4B161az6LMzCcJ1uE6a7TVbd/7VmcEvAw4CblXV
P4nIrvoGv5z38YL7Bitu27p8y+i6PEst+nkIwsD8co7xfXu+x6pVm/nwgw1s2gR+AOl0sdZaXoyz
A/GKKi79ylcYfswIPHcDg4Z1ZciBB6CB24rFlonO25YWm2us08Zzc1c0t9oeufv1tj7QYahq2Qg0
O5a2KUuNXqOwtbowwZvvfkA2rCUMsibxJSzesG/asLlQVZWsV8epZ4/j5E+Npu+gGPGqOkK3ATeW
q2PigMZBXfLrd6gjhKYZJuJmySTrGTl7Ikd9eiFhuidIjFV1NZx349UMmzocL9GA06zetuBEYVQi
JmrED2oYNKQ7044ezcyZE6mp8Vm27G0ctx4TAVLc0eb6rP7o1qfo1n0/auvqQAOefuYRHnv8bv73
rv/i14/excTDh3PiSSfiOlVAilh856eDqgaqOh7TGnKSiIxu8ffW1d42yO8dnKnP9bEt5CCbMg0h
pxObJV0BruMiCCKV1G53eeG5f7B8+QbcGIwe24sZM4Yzbdpwevfen0RKUPHwvCwQEjgBQ8ZV85MH
fkmD5teojDIb/QCcBLUkeeiVf+FWpwlVkFBAPJxYht590syYOZx336lnzeqPiLkVqApCADSQSJpj
cCRWTCwduXyQWDxkH60qbSkBZSbojavBFRfVGJddfjXHz50Y1TZpeleuTO3ueSjN5F6oWRLpkEAb
iMWSxNw0gvGtyi4uvFDAc0wrO+NS8aivrCE1aH9mfuY8/G77MeGkc5k87xATXhcAGosSXPJlYS5b
Lh6NKUTxcGLb6D84xQkLhhFLNJhaPEUebaim7vfhU3rwwbqNhGGMdR98zD0//zH33HcH4yccSBBu
YeSoIVz51a9xxqc+C1RRXd266yYfVd0CLAXmsId9g6PtNfYOTqZdRN0CjjX6PhrLvUJjDoSEVHep
pq4Wlvz2HZ58/FXeX72K46ZP5KRTxjDpiFEMHtqDym4O6S4OTkIJJUugUV2bEBw8Bo8eym2P/5ql
r/wVX100CCDIgjrE4hU8vORFRh63gJnnHEGWTNSC0kHxULI4rkdllXDigtGEYZYnn3iV3y95m5hU
EHcq6denD9mMQ+C7hKEJ+23zu4+WUEMQn+rq8jbILeVDIT1jB4jIUhH5WxRx8aVo/fUi8i8ReT1a
5uV9puiIC8BkP2oSV9PEU/25d/GL+PE61GmIXClR7e4w8nOGxas0SuR3FYesl0FxyPo+XuATikMY
xtHQQUM19WHyllBDNFTcQCNhqmjo4OLRdWCKyrG9iY8+nhPOOQw/YfoZBRJGtcabNE6NLmuzRCkk
YpbGUjmOoCQBIZqcKODYIkEgiicB/YYM4LvfeRzXreLxx37HZxaexe0//iHfuuV7XPj5C3jqiSe4
5Ts/pHfPXkAl8USi1e2KSC8R6RY9TwMzgb/TIX2Dd+MW3vjdhEDA0GGDePudN5g6bSRz5o9ixCF9
UHc7OBlUfIIoRidECTUgVwZZHAHHMTVHXI8RR4zh8u9+m+UfrEe79DDJSm6cv3+0ga/+4D+ZMPcg
MrqFXFtDs5hoHPM8wHXrGTCoG7NnHcKRRxzMG6+v4LFfv8mWzVuprdlKIuFGpQIKP+ZcB7pEYu+H
WIrInOi6fjeagC/FGFaJyJuR3Hk1WrfTCLB23vcdIrJBRN7KW9eu0WcdQSEavQ9coaqjgCnApVFU
BcD3VHV8tDwJ0CLiYg7w39K8W8ZOMdercXOsXL2aEaO6GOEaaXk7yro9yeTc8cIqNjO0SXSbmP5k
lcvQsXG8IEMYFH4Tai0ZM3/ZnTEhSiKZBAXXjTNixAiyWZM89t6Kt1i8eDEjR47ki5d8LqpHX7sr
rbIvsFRE3gBeAZ5R1cWYvsEzReQdYEb0GlX9K5DrG/w0RfQNLq7SRw7BlA9wUFVicY/RYweTSGcJ
1DMiXTyTNCZEAZamWmh+Tf9QICtRmr74+FLP+BMm8qkvXcExp59JWNmbOsdh+nkXc8T8MVR0j0Mg
LfoC5DdFMYUUTA19n1RaGDtuKHNPOIQx4/rTtbsQNM5xF++e29uJzNF1fCswFxgFLMqTBXub4yK5
k4tZvxITATYMWBK97gjuxMi1fFrd957IwvamkJ6xHwIfRs+3i8jb7HpirTHiAlgpIrmIi5d2uZ/o
AkQ8glg18xfNYcyMMXhkyLk2Wi9y1I4UceHk3mq0K0ElxI/VMXbKQQTiF103pj2v2Sg7gKxXz/79
YeXKVTRktvPPf67g8/92EX9+8SVOP/00Jk6axBNPPE480YtdCRpVfQOY0Mr6jbR332AN2T0JplFc
u0a1YMxrjcpnoU7j99LaeaS5TYCJSjLHQEOwhYmzxhDWC9Mv+hzL31rLvHMnUB/UmHBYyVU71ebb
avl9ihprkgCJQyom+JFFqoSFT01Ej81r4u81JgHvqup7ACJyP+Z6/9veHkgrLACOjZ7fBTwHfK29
d6Kqz4vI4AL3vVuysCMoykcfHeAE4E/RqstE5I3InMmZK/2A9/M+VlDEhaggKoQSsG7rNvxUnAA/
0pZ2a55vr5CL9zDROCGKT1hUwbOOQlE8pkwbxZLnXuO3v3mSV175M4t//ShDhgxhyZJnueG667ju
xm+zZs0aIF6UFdJh7Gap5NyUqSklYYS6RhnQZm4/F2YruzSfcsEvYW5bgJ/woEtI5YFdOOrkQ8gE
tdHNIOdbb93W3OUioLg0JVQVc6xNxcH2Mrt1bXcAisnNWCYiF0brdhYBtjfYVfRZOXxfhQt6EakC
fgV8WVW3Af8DHAiMx2j8/1HMjvOjLT7euA2jiSlemGDhuZ9n/OSDUYKoRnpr1SXLBM3FaoOjDo46
UTXNvU+uI5MQgoYE+FRUu/QblOTyK75Gt277oarce++9vPnmG0ybdjQXnncmU6dOBero1q1bScZd
bjS5v3JCNSSQgIquceIVucJ4xd2Q2ss1t8MYP5kcFUWAzcW4ko/O/+PuRoC1B6Xc964oSNBH2ZC/
Au5V1YcBVHV9FHIXAj+lKSGmoIiL/GiLnj26ABCLJ/DCCtZt+QjSUlwZm7KgdL+xtFyibKHQCRhz
6Gh+dOuP2batlhNPWYiqMnnyZCZOnIgfBLz00ktAinQ6XZKxlysmXD8S7OLjSS0aqyeUYjNaOw0F
R1N1JKr6r+hxA/AIRvbsLAJsb7DH0WcdTSFRNwL8DHhbVf8zb33fvLedAuRmoXc74iITxDjz/AuZ
cMRo6oIGglKXzd3HMZPEIelKl18+9BjTj5vBTddfxVf+/Wo2bPiIG264njvueoRNGzcCIZWVlaUe
cllhrDSIhRBTwclVytEda63vPdrDHthtXgGGicgQEUlgJhrbrQxjIYhIpYhU554DszCyZ2cRYHuD
Dog+a18KCcQ9EjgLeFNEcql4V2Nm3MdjzrZVwEVgIi5EJBdx4VNgxIUi4Hbl1TdXcfTQsXkTZ59I
zakdiBKJBLJ+LVu3KFdfdTWXXHoBF33uTPoPGMgJ8+dx801XcPXVVwI+AwcOKu2QyxnNj6cpzXkZ
VfJp9npvoqq+iHwB+A2mqNMdUYTV3qQ38Eh0o40Bv1DVp0XkFeBBETkfWA2c0RE7F5H7MBOvPUVk
LXAdJtpsh33vrizskHGXvNkEMHHcUP394m/zpRv/h+3+x4SpBjxxcFQptAqIpdWAUUQEV4RVK7bx
2J2PsPzVP/LKsj+w7sP1jBk3mgsuPjey66p45KEnOfVTVy4rVZnV7vundPrp9mazM1pG2y95aDWb
NjRYTcjSJmWTGRtPVXLfI88SJkElwFWxunyRNDfqcwlYAV7oMWDYAYwdN4Uhg/uyaOEMLr9iEUuW
LAbHgTADYQN9+/RtYw8Wi2VfpCxyqBXhOz/6GdNnjyAga2rBEJa+td0+i+bVTxGQEKWe+jq46Rvf
oaoauu3Xg4svvgz1a5BYDPVDUulUSUdtsVg6hvLQ6B2Xb33vV1RUx3CdqIhXO6nzuYoy0kluGoXf
/KIvMFejnQwH9HdRCRHHo7ZuI/ffd0+Ufq9IrJI1q9d00Kgt7UF7hWZaPnmUhUa/adMWjjh+AOK2
7zyFEfKKl3EQN8CJOY1JMPsaJgtSTW11cciF67Z+sTcW7I1wcNVh3MThjBx5MAtPn8HWbdv44pf+
j2mKrR5InEzW2wtHYtkTrHC37A5lMRkrIh9hmpWWS4Pf9qCcGhYXwyBV7VWKHdvJ2GJQnn1oDZvt
ZKylAMpCo1fVXlKmTXV3l852POVGLgJFVdFOlryk+olNyLJ0EOXho7dYiiBXqszPCGHQRk/XfQVR
U6ZbjHPRBCTs8gN7Z1yWTkFZuG6g82nAne149gayq44vllZR2yHcUgDlpNGXZa/FPaCzHY/FYtlH
KRuN3mKxGn3xWI3eUgjlpNFbLBaLpQMouaAvhx6UxbKv9o20WCyfTEoq6MusB2Ux3Mk+2DdydxGR
lIj8WUSWi2kQf0O0vt0bxFsslvan1Bp9Yw9KVc0CuR6UZY2qPg9sarF6AaZfJICWQ98AAARvSURB
VNHjyXnr71fVjKquBHJ9I/clMsB0VR2H6Sg2R0SmRH9r1wbxFoul/Sm1oC+bnortQNn3jdxd1FAT
vYxHy64mTjvDzc1i6TSUWtB3Ssq1b+SeICJu1HhmA/CMqrZ7g3iLxdIxlFrQl01PxXag7PtG7glR
f+DxmPFPEpHR7GGDeGjeJL5dB2yxWBoptaAveQ/KdqTs+0a2B6q6BVgKzNnTBvHR9hqbxHfkuC2W
TzIlFfSq6gO5HpRvAw+WoAdl0UR9I18CRojI2qhX5C3ATBF5B5gRvSY6nlzfyKcpYd/I3UVEeolI
t+h5GpgJ/L0jGsRbLJb2x2bGWtpERMZiIolcjHLwoKp+Q0R+jnHbNDaIz01Ii8g1wHmYpshfVtWn
CtiPPRmLxGbGWgrBCnpL2WAFffFYQW8phFL76C0Wi8XSwVhBb7FYLJ0cK+gtFoulk2MFvcVisXRy
rKC3WCyWTo4V9BaLxdLJsYLeYrFYOjlW0FssFksnxwp6i8Vi6eRYQW+xWCydHCvoLRaLpZNjBb3F
YrF0cqygt1gslk6OFfQWi8XSybGC3mKxWDo5VtBbLBZLJ8cKeovFYunkWEFvsVgsnRwr6C0Wi6WT
YwW9pWBExBWR10RkcfR6PxF5RkTeiR675733KhF5V0T+ISKzSzdqi8ViBb2lGL4EvJ33+kpgiaoO
A5ZErxGRUcBC4BBgDvDfIuLu5bFaLJYIK+gtBSEi/YETgNvzVi8A7oqe3wWcnLf+flXNqOpK4F1g
0t4aq8ViaU6s1AOw7DP8F/BVoDpvXW9V/TB6vg7oHT3vB7yc97610bodEJELgQujlxngrfYacBnR
E/i4A7Y7qAO2aemEWEFvaRMRmQ9sUNVlInJsa+9RVRURLXbbqnobcFu0n1dVdeIeDbYM6azHZdl3
sILeUghHAieJyDwgBXQRkXuA9SLSV1U/FJG+wIbo/f8CBuR9vn+0zmKxlADro7e0iapepar9VXUw
ZpL1WVU9E3gMOCd62znAo9Hzx4CFIpIUkSHAMODPe3nYFoslwmr0lj3hFuBBETkfWA2cAaCqfxWR
B4G/AT5wqaoGBWzvtg4baWnprMdl2UcQ1aLdqhaLxWLZh7CuG4vFYunkWEFvKTkiMifKoH1XRK4s
9XiKRUTuEJENIvJW3jqbNWwpG6ygt5SUKGP2VmAuMApYFGXW7kvcickAzsdmDVvKBivoLaVmEvCu
qr6nqlngfkxm7T6Dqj4PbGqx2mYNW8oGK+gtpaYf8H7e651m0e5j7CpruDMer6WMsYLeYulg1IS2
2fA2S8mwgt5SajprFu36KFsYmzVsKTVW0FtKzSvAMBEZIiIJzETlYyUeU3tgs4YtZYPNjLWUFFX1
ReQLwG8AF7hDVf9a4mEVhYjcBxwL9BSRtcB1tH/WsMWy29jMWIvFYunkWNeNxWKxdHKsoLdYLJZO
jhX0FovF0smxgt5isVg6OVbQWywWSyfHCnqLxWLp5FhBb7FYLJ0cK+gtFoulk/P/AWQH/V32mwu/
AAAAAElFTkSuQmCC
"
>
</div>

</div>

</div>
</div>

</div>
    </div>
  </div>
</body>

 


</html>
{:/}
