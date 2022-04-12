# spring-annotations
Anotaciones de Spring Framework

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<!--[if IE]><meta http-equiv="X-UA-Compatible" content="IE=edge"><![endif]-->
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="generator" content="Asciidoctor 1.5.5">
<title>Spring Annotation Cheat Sheet</title>
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Open+Sans:300,300italic,400,400italic,600,600italic%7CNoto+Serif:400,400italic,700,700italic%7CDroid+Sans+Mono:400,700">
<style>
/* Asciidoctor default stylesheet | MIT License | http://asciidoctor.org */
/* Remove comment around @import statement below when using as a custom stylesheet */
/*@import "https://fonts.googleapis.com/css?family=Open+Sans:300,300italic,400,400italic,600,600italic%7CNoto+Serif:400,400italic,700,700italic%7CDroid+Sans+Mono:400,700";*/
article,aside,details,figcaption,figure,footer,header,hgroup,main,nav,section,summary{display:block}
audio,canvas,video{display:inline-block}
audio:not([controls]){display:none;height:0}
[hidden],template{display:none}
script{display:none!important}
html{font-family:sans-serif;-ms-text-size-adjust:100%;-webkit-text-size-adjust:100%}
a{background:transparent}
a:focus{outline:thin dotted}
a:active,a:hover{outline:0}
h1{font-size:2em;margin:.67em 0}
abbr[title]{border-bottom:1px dotted}
b,strong{font-weight:bold}
dfn{font-style:italic}
hr{-moz-box-sizing:content-box;box-sizing:content-box;height:0}
mark{background:#ff0;color:#000}
code,kbd,pre,samp{font-family:monospace;font-size:1em}
pre{white-space:pre-wrap}
q{quotes:"\201C" "\201D" "\2018" "\2019"}
small{font-size:80%}
sub,sup{font-size:75%;line-height:0;position:relative;vertical-align:baseline}
sup{top:-.5em}
sub{bottom:-.25em}
img{border:0}
svg:not(:root){overflow:hidden}
figure{margin:0}
fieldset{border:1px solid silver;margin:0 2px;padding:.35em .625em .75em}
legend{border:0;padding:0}
button,input,select,textarea{font-family:inherit;font-size:100%;margin:0}
button,input{line-height:normal}
button,select{text-transform:none}
button,html input[type="button"],input[type="reset"],input[type="submit"]{-webkit-appearance:button;cursor:pointer}
button[disabled],html input[disabled]{cursor:default}
input[type="checkbox"],input[type="radio"]{box-sizing:border-box;padding:0}
input[type="search"]{-webkit-appearance:textfield;-moz-box-sizing:content-box;-webkit-box-sizing:content-box;box-sizing:content-box}
input[type="search"]::-webkit-search-cancel-button,input[type="search"]::-webkit-search-decoration{-webkit-appearance:none}
button::-moz-focus-inner,input::-moz-focus-inner{border:0;padding:0}
textarea{overflow:auto;vertical-align:top}
table{border-collapse:collapse;border-spacing:0}
*,*:before,*:after{-moz-box-sizing:border-box;-webkit-box-sizing:border-box;box-sizing:border-box}
html,body{font-size:100%}
body{background:#fff;color:rgba(0,0,0,.8);padding:0;margin:0;font-family:"Noto Serif","DejaVu Serif",serif;font-weight:400;font-style:normal;line-height:1;position:relative;cursor:auto;tab-size:4;-moz-osx-font-smoothing:grayscale;-webkit-font-smoothing:antialiased}
a:hover{cursor:pointer}
img,object,embed{max-width:100%;height:auto}
object,embed{height:100%}
img{-ms-interpolation-mode:bicubic}
.left{float:left!important}
.right{float:right!important}
.text-left{text-align:left!important}
.text-right{text-align:right!important}
.text-center{text-align:center!important}
.text-justify{text-align:justify!important}
.hide{display:none}
img,object,svg{display:inline-block;vertical-align:middle}
textarea{height:auto;min-height:50px}
select{width:100%}
.center{margin-left:auto;margin-right:auto}
.spread{width:100%}
p.lead,.paragraph.lead>p,#preamble>.sectionbody>.paragraph:first-of-type p{font-size:1.21875em;line-height:1.6}
.subheader,.admonitionblock td.content>.title,.audioblock>.title,.exampleblock>.title,.imageblock>.title,.listingblock>.title,.literalblock>.title,.stemblock>.title,.openblock>.title,.paragraph>.title,.quoteblock>.title,table.tableblock>.title,.verseblock>.title,.videoblock>.title,.dlist>.title,.olist>.title,.ulist>.title,.qlist>.title,.hdlist>.title{line-height:1.45;color:#7a2518;font-weight:400;margin-top:0;margin-bottom:.25em}
div,dl,dt,dd,ul,ol,li,h1,h2,h3,#toctitle,.sidebarblock>.content>.title,h4,h5,h6,pre,form,p,blockquote,th,td{margin:0;padding:0;direction:ltr}
a{color:#2156a5;text-decoration:underline;line-height:inherit}
a:hover,a:focus{color:#1d4b8f}
a img{border:none}
p{font-family:inherit;font-weight:400;font-size:1em;line-height:1.6;margin-bottom:1.25em;text-rendering:optimizeLegibility}
p aside{font-size:.875em;line-height:1.35;font-style:italic}
h1,h2,h3,#toctitle,.sidebarblock>.content>.title,h4,h5,h6{font-family:"Open Sans","DejaVu Sans",sans-serif;font-weight:300;font-style:normal;color:#ba3925;text-rendering:optimizeLegibility;margin-top:1em;margin-bottom:.5em;line-height:1.0125em}
h1 small,h2 small,h3 small,#toctitle small,.sidebarblock>.content>.title small,h4 small,h5 small,h6 small{font-size:60%;color:#e99b8f;line-height:0}
h1{font-size:2.125em}
h2{font-size:1.6875em}
h3,#toctitle,.sidebarblock>.content>.title{font-size:1.375em}
h4,h5{font-size:1.125em}
h6{font-size:1em}
hr{border:solid #ddddd8;border-width:1px 0 0;clear:both;margin:1.25em 0 1.1875em;height:0}
em,i{font-style:italic;line-height:inherit}
strong,b{font-weight:bold;line-height:inherit}
small{font-size:60%;line-height:inherit}
code{font-family:"Droid Sans Mono","DejaVu Sans Mono",monospace;font-weight:400;color:rgba(0,0,0,.9)}
ul,ol,dl{font-size:1em;line-height:1.6;margin-bottom:1.25em;list-style-position:outside;font-family:inherit}
ul,ol,ul.no-bullet,ol.no-bullet{margin-left:1.5em}
ul li ul,ul li ol{margin-left:1.25em;margin-bottom:0;font-size:1em}
ul.square li ul,ul.circle li ul,ul.disc li ul{list-style:inherit}
ul.square{list-style-type:square}
ul.circle{list-style-type:circle}
ul.disc{list-style-type:disc}
ul.no-bullet{list-style:none}
ol li ul,ol li ol{margin-left:1.25em;margin-bottom:0}
dl dt{margin-bottom:.3125em;font-weight:bold}
dl dd{margin-bottom:1.25em}
abbr,acronym{text-transform:uppercase;font-size:90%;color:rgba(0,0,0,.8);border-bottom:1px dotted #ddd;cursor:help}
abbr{text-transform:none}
blockquote{margin:0 0 1.25em;padding:.5625em 1.25em 0 1.1875em;border-left:1px solid #ddd}
blockquote cite{display:block;font-size:.9375em;color:rgba(0,0,0,.6)}
blockquote cite:before{content:"\2014 \0020"}
blockquote cite a,blockquote cite a:visited{color:rgba(0,0,0,.6)}
blockquote,blockquote p{line-height:1.6;color:rgba(0,0,0,.85)}
@media only screen and (min-width:768px){h1,h2,h3,#toctitle,.sidebarblock>.content>.title,h4,h5,h6{line-height:1.2}
h1{font-size:2.75em}
h2{font-size:2.3125em}
h3,#toctitle,.sidebarblock>.content>.title{font-size:1.6875em}
h4{font-size:1.4375em}}
table{background:#fff;margin-bottom:1.25em;border:solid 1px #dedede}
table thead,table tfoot{background:#f7f8f7;font-weight:bold}
table thead tr th,table thead tr td,table tfoot tr th,table tfoot tr td{padding:.5em .625em .625em;font-size:inherit;color:rgba(0,0,0,.8);text-align:left}
table tr th,table tr td{padding:.5625em .625em;font-size:inherit;color:rgba(0,0,0,.8)}
table tr.even,table tr.alt,table tr:nth-of-type(even){background:#f8f8f7}
table thead tr th,table tfoot tr th,table tbody tr td,table tr td,table tfoot tr td{display:table-cell;line-height:1.6}
h1,h2,h3,#toctitle,.sidebarblock>.content>.title,h4,h5,h6{line-height:1.2;word-spacing:-.05em}
h1 strong,h2 strong,h3 strong,#toctitle strong,.sidebarblock>.content>.title strong,h4 strong,h5 strong,h6 strong{font-weight:400}
.clearfix:before,.clearfix:after,.float-group:before,.float-group:after{content:" ";display:table}
.clearfix:after,.float-group:after{clear:both}
*:not(pre)>code{font-size:.9375em;font-style:normal!important;letter-spacing:0;padding:.1em .5ex;word-spacing:-.15em;background-color:#f7f7f8;-webkit-border-radius:4px;border-radius:4px;line-height:1.45;text-rendering:optimizeSpeed;word-wrap:break-word}
*:not(pre)>code.nobreak{word-wrap:normal}
*:not(pre)>code.nowrap{white-space:nowrap}
pre,pre>code{line-height:1.45;color:rgba(0,0,0,.9);font-family:"Droid Sans Mono","DejaVu Sans Mono",monospace;font-weight:400;text-rendering:optimizeSpeed}
em em{font-style:normal}
strong strong{font-weight:400}
.keyseq{color:rgba(51,51,51,.8)}
kbd{font-family:"Droid Sans Mono","DejaVu Sans Mono",monospace;display:inline-block;color:rgba(0,0,0,.8);font-size:.65em;line-height:1.45;background-color:#f7f7f7;border:1px solid #ccc;-webkit-border-radius:3px;border-radius:3px;-webkit-box-shadow:0 1px 0 rgba(0,0,0,.2),0 0 0 .1em white inset;box-shadow:0 1px 0 rgba(0,0,0,.2),0 0 0 .1em #fff inset;margin:0 .15em;padding:.2em .5em;vertical-align:middle;position:relative;top:-.1em;white-space:nowrap}
.keyseq kbd:first-child{margin-left:0}
.keyseq kbd:last-child{margin-right:0}
.menuseq,.menu{color:rgba(0,0,0,.8)}
b.button:before,b.button:after{position:relative;top:-1px;font-weight:400}
b.button:before{content:"[";padding:0 3px 0 2px}
b.button:after{content:"]";padding:0 2px 0 3px}
p a>code:hover{color:rgba(0,0,0,.9)}
#header,#content,#footnotes,#footer{width:100%;margin-left:auto;margin-right:auto;margin-top:0;margin-bottom:0;max-width:62.5em;*zoom:1;position:relative;padding-left:.9375em;padding-right:.9375em}
#header:before,#header:after,#content:before,#content:after,#footnotes:before,#footnotes:after,#footer:before,#footer:after{content:" ";display:table}
#header:after,#content:after,#footnotes:after,#footer:after{clear:both}
#content{margin-top:1.25em}
#content:before{content:none}
#header>h1:first-child{color:rgba(0,0,0,.85);margin-top:2.25rem;margin-bottom:0}
#header>h1:first-child+#toc{margin-top:8px;border-top:1px solid #ddddd8}
#header>h1:only-child,body.toc2 #header>h1:nth-last-child(2){border-bottom:1px solid #ddddd8;padding-bottom:8px}
#header .details{border-bottom:1px solid #ddddd8;line-height:1.45;padding-top:.25em;padding-bottom:.25em;padding-left:.25em;color:rgba(0,0,0,.6);display:-ms-flexbox;display:-webkit-flex;display:flex;-ms-flex-flow:row wrap;-webkit-flex-flow:row wrap;flex-flow:row wrap}
#header .details span:first-child{margin-left:-.125em}
#header .details span.email a{color:rgba(0,0,0,.85)}
#header .details br{display:none}
#header .details br+span:before{content:"\00a0\2013\00a0"}
#header .details br+span.author:before{content:"\00a0\22c5\00a0";color:rgba(0,0,0,.85)}
#header .details br+span#revremark:before{content:"\00a0|\00a0"}
#header #revnumber{text-transform:capitalize}
#header #revnumber:after{content:"\00a0"}
#content>h1:first-child:not([class]){color:rgba(0,0,0,.85);border-bottom:1px solid #ddddd8;padding-bottom:8px;margin-top:0;padding-top:1rem;margin-bottom:1.25rem}
#toc{border-bottom:1px solid #efefed;padding-bottom:.5em}
#toc>ul{margin-left:.125em}
#toc ul.sectlevel0>li>a{font-style:italic}
#toc ul.sectlevel0 ul.sectlevel1{margin:.5em 0}
#toc ul{font-family:"Open Sans","DejaVu Sans",sans-serif;list-style-type:none}
#toc li{line-height:1.3334;margin-top:.3334em}
#toc a{text-decoration:none}
#toc a:active{text-decoration:underline}
#toctitle{color:#7a2518;font-size:1.2em}
@media only screen and (min-width:768px){#toctitle{font-size:1.375em}
body.toc2{padding-left:15em;padding-right:0}
#toc.toc2{margin-top:0!important;background-color:#f8f8f7;position:fixed;width:15em;left:0;top:0;border-right:1px solid #efefed;border-top-width:0!important;border-bottom-width:0!important;z-index:1000;padding:1.25em 1em;height:100%;overflow:auto}
#toc.toc2 #toctitle{margin-top:0;margin-bottom:.8rem;font-size:1.2em}
#toc.toc2>ul{font-size:.9em;margin-bottom:0}
#toc.toc2 ul ul{margin-left:0;padding-left:1em}
#toc.toc2 ul.sectlevel0 ul.sectlevel1{padding-left:0;margin-top:.5em;margin-bottom:.5em}
body.toc2.toc-right{padding-left:0;padding-right:15em}
body.toc2.toc-right #toc.toc2{border-right-width:0;border-left:1px solid #efefed;left:auto;right:0}}
@media only screen and (min-width:1280px){body.toc2{padding-left:20em;padding-right:0}
#toc.toc2{width:20em}
#toc.toc2 #toctitle{font-size:1.375em}
#toc.toc2>ul{font-size:.95em}
#toc.toc2 ul ul{padding-left:1.25em}
body.toc2.toc-right{padding-left:0;padding-right:20em}}
#content #toc{border-style:solid;border-width:1px;border-color:#e0e0dc;margin-bottom:1.25em;padding:1.25em;background:#f8f8f7;-webkit-border-radius:4px;border-radius:4px}
#content #toc>:first-child{margin-top:0}
#content #toc>:last-child{margin-bottom:0}
#footer{max-width:100%;background-color:rgba(0,0,0,.8);padding:1.25em}
#footer-text{color:rgba(255,255,255,.8);line-height:1.44}
.sect1{padding-bottom:.625em}
@media only screen and (min-width:768px){.sect1{padding-bottom:1.25em}}
.sect1+.sect1{border-top:1px solid #efefed}
#content h1>a.anchor,h2>a.anchor,h3>a.anchor,#toctitle>a.anchor,.sidebarblock>.content>.title>a.anchor,h4>a.anchor,h5>a.anchor,h6>a.anchor{position:absolute;z-index:1001;width:1.5ex;margin-left:-1.5ex;display:block;text-decoration:none!important;visibility:hidden;text-align:center;font-weight:400}
#content h1>a.anchor:before,h2>a.anchor:before,h3>a.anchor:before,#toctitle>a.anchor:before,.sidebarblock>.content>.title>a.anchor:before,h4>a.anchor:before,h5>a.anchor:before,h6>a.anchor:before{content:"\00A7";font-size:.85em;display:block;padding-top:.1em}
#content h1:hover>a.anchor,#content h1>a.anchor:hover,h2:hover>a.anchor,h2>a.anchor:hover,h3:hover>a.anchor,#toctitle:hover>a.anchor,.sidebarblock>.content>.title:hover>a.anchor,h3>a.anchor:hover,#toctitle>a.anchor:hover,.sidebarblock>.content>.title>a.anchor:hover,h4:hover>a.anchor,h4>a.anchor:hover,h5:hover>a.anchor,h5>a.anchor:hover,h6:hover>a.anchor,h6>a.anchor:hover{visibility:visible}
#content h1>a.link,h2>a.link,h3>a.link,#toctitle>a.link,.sidebarblock>.content>.title>a.link,h4>a.link,h5>a.link,h6>a.link{color:#ba3925;text-decoration:none}
#content h1>a.link:hover,h2>a.link:hover,h3>a.link:hover,#toctitle>a.link:hover,.sidebarblock>.content>.title>a.link:hover,h4>a.link:hover,h5>a.link:hover,h6>a.link:hover{color:#a53221}
.audioblock,.imageblock,.literalblock,.listingblock,.stemblock,.videoblock{margin-bottom:1.25em}
.admonitionblock td.content>.title,.audioblock>.title,.exampleblock>.title,.imageblock>.title,.listingblock>.title,.literalblock>.title,.stemblock>.title,.openblock>.title,.paragraph>.title,.quoteblock>.title,table.tableblock>.title,.verseblock>.title,.videoblock>.title,.dlist>.title,.olist>.title,.ulist>.title,.qlist>.title,.hdlist>.title{text-rendering:optimizeLegibility;text-align:left;font-family:"Noto Serif","DejaVu Serif",serif;font-size:1rem;font-style:italic}
table.tableblock>caption.title{white-space:nowrap;overflow:visible;max-width:0}
.paragraph.lead>p,#preamble>.sectionbody>.paragraph:first-of-type p{color:rgba(0,0,0,.85)}
table.tableblock #preamble>.sectionbody>.paragraph:first-of-type p{font-size:inherit}
.admonitionblock>table{border-collapse:separate;border:0;background:none;width:100%}
.admonitionblock>table td.icon{text-align:center;width:80px}
.admonitionblock>table td.icon img{max-width:none}
.admonitionblock>table td.icon .title{font-weight:bold;font-family:"Open Sans","DejaVu Sans",sans-serif;text-transform:uppercase}
.admonitionblock>table td.content{padding-left:1.125em;padding-right:1.25em;border-left:1px solid #ddddd8;color:rgba(0,0,0,.6)}
.admonitionblock>table td.content>:last-child>:last-child{margin-bottom:0}
.exampleblock>.content{border-style:solid;border-width:1px;border-color:#e6e6e6;margin-bottom:1.25em;padding:1.25em;background:#fff;-webkit-border-radius:4px;border-radius:4px}
.exampleblock>.content>:first-child{margin-top:0}
.exampleblock>.content>:last-child{margin-bottom:0}
.sidebarblock{border-style:solid;border-width:1px;border-color:#e0e0dc;margin-bottom:1.25em;padding:1.25em;background:#f8f8f7;-webkit-border-radius:4px;border-radius:4px}
.sidebarblock>:first-child{margin-top:0}
.sidebarblock>:last-child{margin-bottom:0}
.sidebarblock>.content>.title{color:#7a2518;margin-top:0;text-align:center}
.exampleblock>.content>:last-child>:last-child,.exampleblock>.content .olist>ol>li:last-child>:last-child,.exampleblock>.content .ulist>ul>li:last-child>:last-child,.exampleblock>.content .qlist>ol>li:last-child>:last-child,.sidebarblock>.content>:last-child>:last-child,.sidebarblock>.content .olist>ol>li:last-child>:last-child,.sidebarblock>.content .ulist>ul>li:last-child>:last-child,.sidebarblock>.content .qlist>ol>li:last-child>:last-child{margin-bottom:0}
.literalblock pre,.listingblock pre:not(.highlight),.listingblock pre[class="highlight"],.listingblock pre[class^="highlight "],.listingblock pre.CodeRay,.listingblock pre.prettyprint{background:#f7f7f8}
.sidebarblock .literalblock pre,.sidebarblock .listingblock pre:not(.highlight),.sidebarblock .listingblock pre[class="highlight"],.sidebarblock .listingblock pre[class^="highlight "],.sidebarblock .listingblock pre.CodeRay,.sidebarblock .listingblock pre.prettyprint{background:#f2f1f1}
.literalblock pre,.literalblock pre[class],.listingblock pre,.listingblock pre[class]{-webkit-border-radius:4px;border-radius:4px;word-wrap:break-word;padding:1em;font-size:.8125em}
.literalblock pre.nowrap,.literalblock pre[class].nowrap,.listingblock pre.nowrap,.listingblock pre[class].nowrap{overflow-x:auto;white-space:pre;word-wrap:normal}
@media only screen and (min-width:768px){.literalblock pre,.literalblock pre[class],.listingblock pre,.listingblock pre[class]{font-size:.90625em}}
@media only screen and (min-width:1280px){.literalblock pre,.literalblock pre[class],.listingblock pre,.listingblock pre[class]{font-size:1em}}
.literalblock.output pre{color:#f7f7f8;background-color:rgba(0,0,0,.9)}
.listingblock pre.highlightjs{padding:0}
.listingblock pre.highlightjs>code{padding:1em;-webkit-border-radius:4px;border-radius:4px}
.listingblock pre.prettyprint{border-width:0}
.listingblock>.content{position:relative}
.listingblock code[data-lang]:before{display:none;content:attr(data-lang);position:absolute;font-size:.75em;top:.425rem;right:.5rem;line-height:1;text-transform:uppercase;color:#999}
.listingblock:hover code[data-lang]:before{display:block}
.listingblock.terminal pre .command:before{content:attr(data-prompt);padding-right:.5em;color:#999}
.listingblock.terminal pre .command:not([data-prompt]):before{content:"$"}
table.pyhltable{border-collapse:separate;border:0;margin-bottom:0;background:none}
table.pyhltable td{vertical-align:top;padding-top:0;padding-bottom:0;line-height:1.45}
table.pyhltable td.code{padding-left:.75em;padding-right:0}
pre.pygments .lineno,table.pyhltable td:not(.code){color:#999;padding-left:0;padding-right:.5em;border-right:1px solid #ddddd8}
pre.pygments .lineno{display:inline-block;margin-right:.25em}
table.pyhltable .linenodiv{background:none!important;padding-right:0!important}
.quoteblock{margin:0 1em 1.25em 1.5em;display:table}
.quoteblock>.title{margin-left:-1.5em;margin-bottom:.75em}
.quoteblock blockquote,.quoteblock blockquote p{color:rgba(0,0,0,.85);font-size:1.15rem;line-height:1.75;word-spacing:.1em;letter-spacing:0;font-style:italic;text-align:justify}
.quoteblock blockquote{margin:0;padding:0;border:0}
.quoteblock blockquote:before{content:"\201c";float:left;font-size:2.75em;font-weight:bold;line-height:.6em;margin-left:-.6em;color:#7a2518;text-shadow:0 1px 2px rgba(0,0,0,.1)}
.quoteblock blockquote>.paragraph:last-child p{margin-bottom:0}
.quoteblock .attribution{margin-top:.5em;margin-right:.5ex;text-align:right}
.quoteblock .quoteblock{margin-left:0;margin-right:0;padding:.5em 0;border-left:3px solid rgba(0,0,0,.6)}
.quoteblock .quoteblock blockquote{padding:0 0 0 .75em}
.quoteblock .quoteblock blockquote:before{display:none}
.verseblock{margin:0 1em 1.25em 1em}
.verseblock pre{font-family:"Open Sans","DejaVu Sans",sans;font-size:1.15rem;color:rgba(0,0,0,.85);font-weight:300;text-rendering:optimizeLegibility}
.verseblock pre strong{font-weight:400}
.verseblock .attribution{margin-top:1.25rem;margin-left:.5ex}
.quoteblock .attribution,.verseblock .attribution{font-size:.9375em;line-height:1.45;font-style:italic}
.quoteblock .attribution br,.verseblock .attribution br{display:none}
.quoteblock .attribution cite,.verseblock .attribution cite{display:block;letter-spacing:-.025em;color:rgba(0,0,0,.6)}
.quoteblock.abstract{margin:0 0 1.25em 0;display:block}
.quoteblock.abstract blockquote,.quoteblock.abstract blockquote p{text-align:left;word-spacing:0}
.quoteblock.abstract blockquote:before,.quoteblock.abstract blockquote p:first-of-type:before{display:none}
table.tableblock{max-width:100%;border-collapse:separate}
table.tableblock td>.paragraph:last-child p>p:last-child,table.tableblock th>p:last-child,table.tableblock td>p:last-child{margin-bottom:0}
table.tableblock,th.tableblock,td.tableblock{border:0 solid #dedede}
table.grid-all th.tableblock,table.grid-all td.tableblock{border-width:0 1px 1px 0}
table.grid-all tfoot>tr>th.tableblock,table.grid-all tfoot>tr>td.tableblock{border-width:1px 1px 0 0}
table.grid-cols th.tableblock,table.grid-cols td.tableblock{border-width:0 1px 0 0}
table.grid-all *>tr>.tableblock:last-child,table.grid-cols *>tr>.tableblock:last-child{border-right-width:0}
table.grid-rows th.tableblock,table.grid-rows td.tableblock{border-width:0 0 1px 0}
table.grid-all tbody>tr:last-child>th.tableblock,table.grid-all tbody>tr:last-child>td.tableblock,table.grid-all thead:last-child>tr>th.tableblock,table.grid-rows tbody>tr:last-child>th.tableblock,table.grid-rows tbody>tr:last-child>td.tableblock,table.grid-rows thead:last-child>tr>th.tableblock{border-bottom-width:0}
table.grid-rows tfoot>tr>th.tableblock,table.grid-rows tfoot>tr>td.tableblock{border-width:1px 0 0 0}
table.frame-all{border-width:1px}
table.frame-sides{border-width:0 1px}
table.frame-topbot{border-width:1px 0}
th.halign-left,td.halign-left{text-align:left}
th.halign-right,td.halign-right{text-align:right}
th.halign-center,td.halign-center{text-align:center}
th.valign-top,td.valign-top{vertical-align:top}
th.valign-bottom,td.valign-bottom{vertical-align:bottom}
th.valign-middle,td.valign-middle{vertical-align:middle}
table thead th,table tfoot th{font-weight:bold}
tbody tr th{display:table-cell;line-height:1.6;background:#f7f8f7}
tbody tr th,tbody tr th p,tfoot tr th,tfoot tr th p{color:rgba(0,0,0,.8);font-weight:bold}
p.tableblock>code:only-child{background:none;padding:0}
p.tableblock{font-size:1em}
td>div.verse{white-space:pre}
ol{margin-left:1.75em}
ul li ol{margin-left:1.5em}
dl dd{margin-left:1.125em}
dl dd:last-child,dl dd:last-child>:last-child{margin-bottom:0}
ol>li p,ul>li p,ul dd,ol dd,.olist .olist,.ulist .ulist,.ulist .olist,.olist .ulist{margin-bottom:.625em}
ul.unstyled,ol.unnumbered,ul.checklist,ul.none{list-style-type:none}
ul.unstyled,ol.unnumbered,ul.checklist{margin-left:.625em}
ul.checklist li>p:first-child>.fa-square-o:first-child,ul.checklist li>p:first-child>.fa-check-square-o:first-child{width:1em;font-size:.85em}
ul.checklist li>p:first-child>input[type="checkbox"]:first-child{width:1em;position:relative;top:1px}
ul.inline{margin:0 auto .625em auto;margin-left:-1.375em;margin-right:0;padding:0;list-style:none;overflow:hidden}
ul.inline>li{list-style:none;float:left;margin-left:1.375em;display:block}
ul.inline>li>*{display:block}
.unstyled dl dt{font-weight:400;font-style:normal}
ol.arabic{list-style-type:decimal}
ol.decimal{list-style-type:decimal-leading-zero}
ol.loweralpha{list-style-type:lower-alpha}
ol.upperalpha{list-style-type:upper-alpha}
ol.lowerroman{list-style-type:lower-roman}
ol.upperroman{list-style-type:upper-roman}
ol.lowergreek{list-style-type:lower-greek}
.hdlist>table,.colist>table{border:0;background:none}
.hdlist>table>tbody>tr,.colist>table>tbody>tr{background:none}
td.hdlist1,td.hdlist2{vertical-align:top;padding:0 .625em}
td.hdlist1{font-weight:bold;padding-bottom:1.25em}
.literalblock+.colist,.listingblock+.colist{margin-top:-.5em}
.colist>table tr>td:first-of-type{padding:0 .75em;line-height:1}
.colist>table tr>td:last-of-type{padding:.25em 0}
.thumb,.th{line-height:0;display:inline-block;border:solid 4px #fff;-webkit-box-shadow:0 0 0 1px #ddd;box-shadow:0 0 0 1px #ddd}
.imageblock.left,.imageblock[style*="float: left"]{margin:.25em .625em 1.25em 0}
.imageblock.right,.imageblock[style*="float: right"]{margin:.25em 0 1.25em .625em}
.imageblock>.title{margin-bottom:0}
.imageblock.thumb,.imageblock.th{border-width:6px}
.imageblock.thumb>.title,.imageblock.th>.title{padding:0 .125em}
.image.left,.image.right{margin-top:.25em;margin-bottom:.25em;display:inline-block;line-height:0}
.image.left{margin-right:.625em}
.image.right{margin-left:.625em}
a.image{text-decoration:none;display:inline-block}
a.image object{pointer-events:none}
sup.footnote,sup.footnoteref{font-size:.875em;position:static;vertical-align:super}
sup.footnote a,sup.footnoteref a{text-decoration:none}
sup.footnote a:active,sup.footnoteref a:active{text-decoration:underline}
#footnotes{padding-top:.75em;padding-bottom:.75em;margin-bottom:.625em}
#footnotes hr{width:20%;min-width:6.25em;margin:-.25em 0 .75em 0;border-width:1px 0 0 0}
#footnotes .footnote{padding:0 .375em 0 .225em;line-height:1.3334;font-size:.875em;margin-left:1.2em;text-indent:-1.05em;margin-bottom:.2em}
#footnotes .footnote a:first-of-type{font-weight:bold;text-decoration:none}
#footnotes .footnote:last-of-type{margin-bottom:0}
#content #footnotes{margin-top:-.625em;margin-bottom:0;padding:.75em 0}
.gist .file-data>table{border:0;background:#fff;width:100%;margin-bottom:0}
.gist .file-data>table td.line-data{width:99%}
div.unbreakable{page-break-inside:avoid}
.big{font-size:larger}
.small{font-size:smaller}
.underline{text-decoration:underline}
.overline{text-decoration:overline}
.line-through{text-decoration:line-through}
.aqua{color:#00bfbf}
.aqua-background{background-color:#00fafa}
.black{color:#000}
.black-background{background-color:#000}
.blue{color:#0000bf}
.blue-background{background-color:#0000fa}
.fuchsia{color:#bf00bf}
.fuchsia-background{background-color:#fa00fa}
.gray{color:#606060}
.gray-background{background-color:#7d7d7d}
.green{color:#006000}
.green-background{background-color:#007d00}
.lime{color:#00bf00}
.lime-background{background-color:#00fa00}
.maroon{color:#600000}
.maroon-background{background-color:#7d0000}
.navy{color:#000060}
.navy-background{background-color:#00007d}
.olive{color:#606000}
.olive-background{background-color:#7d7d00}
.purple{color:#600060}
.purple-background{background-color:#7d007d}
.red{color:#bf0000}
.red-background{background-color:#fa0000}
.silver{color:#909090}
.silver-background{background-color:#bcbcbc}
.teal{color:#006060}
.teal-background{background-color:#007d7d}
.white{color:#bfbfbf}
.white-background{background-color:#fafafa}
.yellow{color:#bfbf00}
.yellow-background{background-color:#fafa00}
span.icon>.fa{cursor:default}
.admonitionblock td.icon [class^="fa icon-"]{font-size:2.5em;text-shadow:1px 1px 2px rgba(0,0,0,.5);cursor:default}
.admonitionblock td.icon .icon-note:before{content:"\f05a";color:#19407c}
.admonitionblock td.icon .icon-tip:before{content:"\f0eb";text-shadow:1px 1px 2px rgba(155,155,0,.8);color:#111}
.admonitionblock td.icon .icon-warning:before{content:"\f071";color:#bf6900}
.admonitionblock td.icon .icon-caution:before{content:"\f06d";color:#bf3400}
.admonitionblock td.icon .icon-important:before{content:"\f06a";color:#bf0000}
.conum[data-value]{display:inline-block;color:#fff!important;background-color:rgba(0,0,0,.8);-webkit-border-radius:100px;border-radius:100px;text-align:center;font-size:.75em;width:1.67em;height:1.67em;line-height:1.67em;font-family:"Open Sans","DejaVu Sans",sans-serif;font-style:normal;font-weight:bold}
.conum[data-value] *{color:#fff!important}
.conum[data-value]+b{display:none}
.conum[data-value]:after{content:attr(data-value)}
pre .conum[data-value]{position:relative;top:-.125em}
b.conum *{color:inherit!important}
.conum:not([data-value]):empty{display:none}
dt,th.tableblock,td.content,div.footnote{text-rendering:optimizeLegibility}
h1,h2,p,td.content,span.alt{letter-spacing:-.01em}
p strong,td.content strong,div.footnote strong{letter-spacing:-.005em}
p,blockquote,dt,td.content,span.alt{font-size:1.0625rem}
p{margin-bottom:1.25rem}
.sidebarblock p,.sidebarblock dt,.sidebarblock td.content,p.tableblock{font-size:1em}
.exampleblock>.content{background-color:#fffef7;border-color:#e0e0dc;-webkit-box-shadow:0 1px 4px #e0e0dc;box-shadow:0 1px 4px #e0e0dc}
.print-only{display:none!important}
@media print{@page{margin:1.25cm .75cm}
*{-webkit-box-shadow:none!important;box-shadow:none!important;text-shadow:none!important}
a{color:inherit!important;text-decoration:underline!important}
a.bare,a[href^="#"],a[href^="mailto:"]{text-decoration:none!important}
a[href^="http:"]:not(.bare):after,a[href^="https:"]:not(.bare):after{content:"(" attr(href) ")";display:inline-block;font-size:.875em;padding-left:.25em}
abbr[title]:after{content:" (" attr(title) ")"}
pre,blockquote,tr,img,object,svg{page-break-inside:avoid}
thead{display:table-header-group}
svg{max-width:100%}
p,blockquote,dt,td.content{font-size:1em;orphans:3;widows:3}
h2,h3,#toctitle,.sidebarblock>.content>.title{page-break-after:avoid}
#toc,.sidebarblock,.exampleblock>.content{background:none!important}
#toc{border-bottom:1px solid #ddddd8!important;padding-bottom:0!important}
.sect1{padding-bottom:0!important}
.sect1+.sect1{border:0!important}
#header>h1:first-child{margin-top:1.25rem}
body.book #header{text-align:center}
body.book #header>h1:first-child{border:0!important;margin:2.5em 0 1em 0}
body.book #header .details{border:0!important;display:block;padding:0!important}
body.book #header .details span:first-child{margin-left:0!important}
body.book #header .details br{display:block}
body.book #header .details br+span:before{content:none!important}
body.book #toc{border:0!important;text-align:left!important;padding:0!important;margin:0!important}
body.book #toc,body.book #preamble,body.book h1.sect0,body.book .sect1>h2{page-break-before:always}
.listingblock code[data-lang]:before{display:block}
#footer{background:none!important;padding:0 .9375em}
#footer-text{color:rgba(0,0,0,.6)!important;font-size:.9em}
.hide-on-print{display:none!important}
.print-only{display:block!important}
.hide-for-print{display:none!important}
.show-for-print{display:inherit!important}}
</style>
</head>
<body class="article">
<div id="header">
</div>
<div id="content">
<div class="sect1">
<h2 id="_spring_annotation_cheat_sheet">Spring Annotation Cheat Sheet</h2>
<div class="sectionbody">
<div class="paragraph">
<p>Spring includes a lot of annotations. Some are annotations created within Spring. Some are annotations called for by various Java specifications. The annotations fall into categories, as follows:</p>
</div>
<div class="ulist">
<ul>
<li>
<p><a href="#_spring_framework">Spring Framework</a></p>
</li>
<li>
<p><a href="#_rest">REST</a></p>
</li>
<li>
<p><a href="#_hateoas">HATEOAS</a></p>
</li>
<li>
<p><a href="#_session">Session</a></p>
</li>
<li>
<p><a href="#_boot">Boot</a></p>
</li>
<li>
<p><a href="#_integration">Integration</a></p>
</li>
<li>
<p><a href="#_cloud">Cloud</a></p>
</li>
<li>
<p><a href="#_data">Data</a></p>
</li>
<li>
<p><a href="#_batch">Batch</a></p>
</li>
<li>
<p><a href="#_aspect_oriented_programming">Aspect-oriented Programming</a></p>
</li>
<li>
<p><a href="#_integration_testing">Integration Testing</a></p>
</li>
<li>
<p><a href="#_jmx">JMX</a></p>
</li>
<li>
<p><a href="#_task_execution_and_scheduling">Task Execution and Scheduling</a></p>
</li>
<li>
<p><a href="#_cache_abstraction">Cache Abstraction</a></p>
</li>
<li>
<p><a href="#_other">Other</a></p>
</li>
</ul>
</div>
<div class="sect2">
<h3 id="_spring_framework">Spring Framework</h3>
<div class="paragraph">
<p>The Spring Framework is the core project within Spring. The Spring Framework includes annotations in the following categories:</p>
</div>
<div class="ulist">
<ul>
<li>
<p><a href="#_dependency_injection">Dependency Injection</a></p>
</li>
<li>
<p><a href="#_configuration">Configuration</a></p>
</li>
<li>
<p><a href="#_jms">JMS</a></p>
</li>
<li>
<p><a href="#_amqp">AMQP</a></p>
</li>
<li>
<p><a href="#_bean_lifecycle">Bean Lifecycle</a></p>
</li>
<li>
<p><a href="#_mvc_web">MVC/Web</a></p>
</li>
<li>
<p><a href="#_cors_support">CORS Support</a></p>
</li>
</ul>
</div>
<div class="sect3">
<h4 id="_dependency_injection">Dependency Injection</h4>
<div class="paragraph">
<p>Spring&#8217;s dependency injection capability includes the following annotations:</p>
</div>
<div class="hdlist">
<table>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-resource-annotation">@Resource</a>
</td>
<td class="hdlist2">
<p>Injects the requested resource.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-autowired-annotation">@Autowired</a>
</td>
<td class="hdlist2">
<p>Widely used dependency injection mechanism for constructors, methods, and interfaces.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-inject-named">@Inject</a>
</td>
<td class="hdlist2">
<p>A dependency injection mechanism that can replace @Autowired. @Named may also be used in place of @Autowired and @Inject.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-inject-named">@Named</a>
</td>
<td class="hdlist2">
<p>A dependency injection mechanism that can replace @Autowired and @Inject. @Named may also be used in place of @Autowired and @Inject. @Named is also equivalent to @Component and @ManagedBean.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-named">@ManagedBean</a>
</td>
<td class="hdlist2">
<p>A dependency injection mechanism that can replace @Autowired and @Inject. @ManagedBean is also equivalent to @Component and @Named. However, it is not composable.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/beans/factory/annotation/Value.html">@Value</a>
</td>
<td class="hdlist2">
<p>Injection mechanism for fields and methods that indicates a default value. Often used to get values from property files.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/javadoc-api/index.html?org/springframework/beans/factory/annotation/Required.html">@Required</a>
</td>
<td class="hdlist2">
<p>Marks a method (typically a JavaBean setter method) as being 'required'. That is, the method must be configured to be dependency-injected with a value.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-autowired-annotation-primary">@Primary</a>
</td>
<td class="hdlist2">
<p>Indicates that a particular bean should be given preference when multiple beans are candidates to be autowired to a single-valued dependency. If exactly one 'primary' bean exists among the candidates, it will be the autowired value.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-stereotype-annotations">@Component</a>
</td>
<td class="hdlist2">
<p>Generic stereotype for any Spring-managed component.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/stereotype/Service.html">@Service</a>
</td>
<td class="hdlist2">
<p>Indicates that an annotated class is a service.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-java-using-import">@Import</a>
</td>
<td class="hdlist2">
<p>Allows for loading <code>@Bean</code> definitions from another configuration class.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/context/annotation/DependsOn.html">@DependsOn</a>
</td>
<td class="hdlist2">
<p>Indicates beans on which the current bean depends.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-factory-collaborators">@ConstructorProperties</a>
</td>
<td class="hdlist2">
<p>Used to explicitly name your constructor arguments.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/beans/factory/annotation/Lookup.html">@Lookup</a>
</td>
<td class="hdlist2">
<p>Indicates 'lookup' methods, to be overridden by the container to redirect them back to the BeanFactory for a getBean call. This is essentially an annotation-based version of the XML lookup-method attribute.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring/docs/4.3.0.RC1/javadoc-api//org/springframework/core/annotation/AliasFor.html">@AliasFor</a>
</td>
<td class="hdlist2">
<p>Used to declare aliases for annotation attributes.</p>
</td>
</tr>
</table>
</div>
</div>
<div class="sect3">
<h4 id="_configuration">Configuration</h4>
<div class="paragraph">
<p>Spring&#8217;s configuration capability includes the following annotations:</p>
</div>
<div class="hdlist">
<table>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/context/annotation/ComponentScan.html">@ComponentScan</a>
</td>
<td class="hdlist2">
<p>Configures component scanning directives for use with @Configuration classes.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-java-basic-concepts">@Configuration</a>
</td>
<td class="hdlist2">
<p>Indicates that the primary purpose of the annotated class is to provide a source of bean definitions.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/core/annotation/Order.html">@Order</a>
</td>
<td class="hdlist2">
<p>Defines the sort order for an annotated component. Lower values have higher priority. @Priority can replace @Order.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.oracle.com/javaee/7/api/javax/annotation/Priority.html">@Priority</a>
</td>
<td class="hdlist2">
<p>Defines the sort order for an annotated component. Lower values have higher priority. @Order can replace @Priority.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-autowired-annotation-qualifiers">@Qualifier</a>
</td>
<td class="hdlist2">
<p>Associates a value with a particular argument. More finely tuned way than @Order and @Priority to control selection.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.oracle.com/javase/8/docs/api/java/lang/annotation/Target.html">@Target</a>
</td>
<td class="hdlist2">
<p>Indicates the contexts in which an annotation type is applicable.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.oracle.com/javase/8/docs/api/java/lang/annotation/Retention.html">@Retention</a>
</td>
<td class="hdlist2">
<p>Indicates how long annotations with the annotated type are to be retained.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-autowired-annotation-qualifiers">@interface</a>
</td>
<td class="hdlist2">
<p>Lets you create custom annotations to use as qualifiers.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/stereotype/Repository.html">@Repository</a>
</td>
<td class="hdlist2">
<p>Indicates that an annotated class is a repository.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-definition-profiles">@Profile</a>
</td>
<td class="hdlist2">
<p>Indicates that a component is eligible for registration when one or more specified profiles are active.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/context/annotation/Conditional.html">@Conditional</a>
</td>
<td class="hdlist2">
<p>Indicates that a component is only eligible for registration when all specified conditions match.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-java-using-import">@ImportResource</a>
</td>
<td class="hdlist2">
<p>Allows for loading @Bean definitions from another configuration class. Also allows for importing XML configuration files.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#context-load-time-weaver">@EnableLoadTimeWeaving</a>
</td>
<td class="hdlist2">
<p>Enables load-time weaving, which is used by Spring to dynamically transform classes as they are loaded into the JVM.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#context-functionality-events-annotation">@EventListener</a>
</td>
<td class="hdlist2">
<p>Registers an event listener on a public method of a bean.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#context-functionality-events-async">@Async</a>
</td>
<td class="hdlist2">
<p>Specifies that an event listener is asynchronous. See also: Async under <a href="#_task_execution_and_scheduling">Task Execution and Scheduling</a>.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/context/annotation/PropertySource.html">@PropertySource</a>
</td>
<td class="hdlist2">
<p>Adds a PropertySource to Spring&#8217;s Environment.</p>
</td>
</tr>
</table>
</div>
</div>
<div class="sect3">
<h4 id="_jms">JMS</h4>
<div class="paragraph">
<p>Spring&#8217;s support for JMS includes the following annotations:</p>
</div>
<div class="hdlist">
<table>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/jms.html#jms-annotated-support">@EnableJms</a>
</td>
<td class="hdlist2">
<p>Add to an @configuration class to enable support for @JmsListener annotations.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/jms.html#jms-mdp">@JmsListener</a>
</td>
<td class="hdlist2">
<p>Indicates that a method of a managed bean is a JMS listener endpoint.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/jms/annotation/JmsListeners.html">@JmsListeners</a>
</td>
<td class="hdlist2">
<p>Aggregates several @JmsListener annotations. On Java 8, it can be replaced by repeatable @JmsListener annotations.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-integration/reference/html/message-publishing.html">@Payload</a>
</td>
<td class="hdlist2">
<p>Indicates that a method provides the payload of a message.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/jms.html#jms-annotated-response">@SendTo</a>
</td>
<td class="hdlist2">
<p>Indicates the method (or sometimes class) that responds to a message.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/messaging/simp/annotation/SendToUser.html">@SendToUser</a>
</td>
<td class="hdlist2">
<p>Indicates that the return value of a message-handling method should be sent as a Message to the specified destination(s) prepended with <code>/user/{username}</code> where the user name is extracted from the headers of the input message being handled.</p>
</td>
</tr>
</table>
</div>
</div>
<div class="sect3">
<h4 id="_amqp">AMQP</h4>
<div class="paragraph">
<p>Spring AMQP provides the following annotations:</p>
</div>
<div class="hdlist">
<table>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-amqp/docs/current/api/org/springframework/amqp/rabbit/annotation/Queue.html">@Queue</a>
</td>
<td class="hdlist2">
<p>A queue definition used within the bindings attribute of an <code>@QueueBinding</code>.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-amqp/docs/current/api/org/springframework/amqp/rabbit/annotation/QueueBinding.html">@QueueBinding</a>
</td>
<td class="hdlist2">
<p>Defines a queue, the exchange it is to be bound to, and an optional binding key. Used with <code>@RabbitListener</code>.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-amqp/docs/current/api/org/springframework/amqp/rabbit/annotation/Exchange.html">@Exchange</a>
</td>
<td class="hdlist2">
<p>Defines an exchange to which to bind a RabbitListener queue.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-amqp/docs/current/api/org/springframework/amqp/rabbit/annotation/Argument.html">@Argument</a>
</td>
<td class="hdlist2">
<p>Represents an argument used when declaring queues etc within a QueueBinding.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-amqp/docs/current/api/org/springframework/amqp/rabbit/annotation/EnableRabbit.html">@EnableRabbit</a>
</td>
<td class="hdlist2">
<p>Enable Rabbit listener annotated endpoints that are created behind the scenes by a <code>RabbitListenerContainerFactory</code>. To be used on <code>@Configuration</code> classes.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-amqp/docs/current/api/org/springframework/amqp/rabbit/annotation/RabbitHandler.html">@RabbitHandler</a>
</td>
<td class="hdlist2">
<p>marks a method to be the target of a Rabbit message listener within a class that is annotated with <code>@RabbitListener</code>.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-amqp/api/org/springframework/amqp/rabbit/annotation/RabbitListener.html">@RabbitListener</a>
</td>
<td class="hdlist2">
<p>Marks a method as the target of a Rabbit message listener on the specified <code>queues</code> (or <code>bindings</code>).</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-amqp/docs/current/api/org/springframework/amqp/rabbit/annotation/RabbitListeners.html">@RabbitListeners</a>
</td>
<td class="hdlist2">
<p>Container annotation that aggregates several <code>@RabbitListener</code> annotations.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-amqp/docs/current/api/org/springframework/amqp/rabbit/test/RabbitListenerTest.html">@RabbitListenerTest</a>
</td>
<td class="hdlist2">
<p>Enables proxying of @RabbitListener beans to capture arguments and results (if any). Used on @Configuration classes.</p>
</td>
</tr>
</table>
</div>
</div>
<div class="sect3">
<h4 id="_bean_lifecycle">Bean Lifecycle</h4>
<div class="paragraph">
<p>Spring&#8217;s bean lifecycle management capability includes the following annotations:</p>
</div>
<div class="hdlist">
<table>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/expressions.html#expressions-bean-references">@{BeanName}</a>
</td>
<td class="hdlist2">
<p>For example, <code>@foo</code> will find a bean named <code>foo</code>, provided the evaluation context has been configured with a bean resolver.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-java-basic-concepts">@Bean</a>
</td>
<td class="hdlist2">
<p>Indicates that a method instantiates, configures and initializes a new object to be managed by the Spring IoC container.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-java-bean-description">@Description</a>
</td>
<td class="hdlist2">
<p>Adds a description to a bean.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-stereotype-annotations">@Component</a>
</td>
<td class="hdlist2">
<p>Generic stereotype for any Spring-managed component.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-factorybeans-annotations">@Lazy</a>
</td>
<td class="hdlist2">
<p>Causes lazy resolution of a bean in the IoC container.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-scanning-scope-resolver">@Scope</a>
</td>
<td class="hdlist2">
<p>Specifies a non-default scope for a component.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-postconstruct-and-predestroy-annotations">@PostConstruct</a>
</td>
<td class="hdlist2">
<p>Identifies a method to be called after an instance of a bean has been constructed. Used to populate caches and similar operations.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/beans.html#beans-postconstruct-and-predestroy-annotations">@PreDestroy</a>
</td>
<td class="hdlist2">
<p>Identifies a method to be called before an instance of a bean is to be destroyed. Used to de-populate caches and similar operations.</p>
</td>
</tr>
</table>
</div>
</div>
<div class="sect3">
<h4 id="_mvc_web">MVC/Web</h4>
<div class="paragraph">
<p>Spring provides the following annotations for web applications:
Major source: <a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html" class="bare">https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html</a></p>
</div>
<div class="hdlist">
<table>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-config-enable">@EnableWebMvc</a>
</td>
<td class="hdlist2">
<p>Added to a @configuration class to enable Web MVC.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-ann-controller">@Controller</a>
</td>
<td class="hdlist2">
<p>Indicates that a class is an MVC controller.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-ann-restcontroller">@RESTController</a>
</td>
<td class="hdlist2">
<p>Indicates that a class is a REST controller.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-controller">@RequestMapping</a>
</td>
<td class="hdlist2">
<p>Associates a URI path with a method in a controller.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-ann-modelattrib-methods">@ModelAttribute</a>
</td>
<td class="hdlist2">
<p>Indicates that a method or argument contributes to a model.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-ann-sessionattrib-global">@SessionAttribute</a>
</td>
<td class="hdlist2">
<p>Provides access to pre-existing session attributes that are managed globally.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-ann-sessionattrib">@SessionAttributes</a>
</td>
<td class="hdlist2">
<p>Declares session attributes used by a specific handler.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-ann-responsebody">@ResponseBody</a>
</td>
<td class="hdlist2">
<p>Causes the return type to be written to the response body (rather than the model).</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-ann-requestparam">@RequestParam</a>
</td>
<td class="hdlist2">
<p>Binds a request parameter to a method.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-multipart-forms-non-browsers">@RequestPart</a>
</td>
<td class="hdlist2">
<p>Associates a handler method argument with part of a multi-part request.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-ann-requestmapping-uri-templates">@PathVariable</a>
</td>
<td class="hdlist2">
<p>Binds a method argument to the value of a URI template variable.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/Header.html">@Header</a>
</td>
<td class="hdlist2">
<p>Indicates that a method parameter&#8217;s value should be retrieved from the message headers.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/Headers.html">@Headers</a>
</td>
<td class="hdlist2">
<p>Deprecated. Use @header.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-ann-requestheader">@RequestHeader</a>
</td>
<td class="hdlist2">
<p>Binds a method parameter to a request header.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-ann-requestbody">@RequestBody</a>
</td>
<td class="hdlist2">
<p>Binds a method parameter to the value of the HTTP request body.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-ann-annotated-exceptions">@ResponseStatus</a>
</td>
<td class="hdlist2">
<p>Indicates a business exception.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-ann-controller-advice">@ControllerAdvice</a>
</td>
<td class="hdlist2">
<p>Allows implementation classes to be auto-detected through classpath scanning. It is automatically enabled when using the MVC namespace or the MVC Java config.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-ann-controller-advice">@RestControllerAdvice</a>
</td>
<td class="hdlist2">
<p>As @ControllerAdvice (previous) but <code>@ExceptionHandler</code> methods assume <code>@ResponseBody</code> semantics by default.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/portlet.html#portlet-ann-initbinder">@InitBinder</a>
</td>
<td class="hdlist2">
<p>Configures web data binding directly within a controller class.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-ann-matrix-variables">@MatrixVariable</a>
</td>
<td class="hdlist2">
<p>Identifies the value part of a name/value pair in a URI path.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-ann-cookievalue">@cookieValue</a>
</td>
<td class="hdlist2">
<p>Binds a method parameter to the value of an HTTP cookie.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/web/context/annotation/RequestScope.html">@RequestScope</a>
</td>
<td class="hdlist2">
<p>A specialization of @Scope for a component whose lifecycle is bound to the current web request.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/web/context/annotation/SessionScope.html">@SessionScope</a>
</td>
<td class="hdlist2">
<p>A specialization of @Scope for a component whose lifecycle is bound to the current web session.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/web/context/annotation/ApplicationScope.html">@ApplicationScope</a>
</td>
<td class="hdlist2">
<p>A specialization of @Scope for a component whose lifecycle is bound to the current web application.</p>
</td>
</tr>
</table>
</div>
<div class="paragraph">
<p>Spring MVC provides the following convenience annotations for request mapping:</p>
</div>
<div class="hdlist">
<table>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-ann-requestmapping-composed">@GetMapping</a>
</td>
<td class="hdlist2">
<p>Shortcut for @RequestMapping(method = RequestMethod.GET)</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-ann-requestmapping-composed">@PostMapping</a>
</td>
<td class="hdlist2">
<p>Shortcut for @RequestMapping(method = RequestMethod.POST)</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-ann-requestmapping-composed">@PutMapping</a>
</td>
<td class="hdlist2">
<p>Shortcut for @RequestMapping(method = RequestMethod.PUT)</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-ann-requestmapping-composed">@DeleteMapping</a>
</td>
<td class="hdlist2">
<p>Shortcut for @RequestMapping(method = RequestMethod.DELETE)</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/mvc.html#mvc-ann-requestmapping-composed">@PatchMapping</a>
</td>
<td class="hdlist2">
<p>Shortcut for @RequestMapping(method = RequestMethod.PATCH)</p>
</td>
</tr>
</table>
</div>
</div>
<div class="sect3">
<h4 id="_cors_support">CORS Support</h4>
<div class="paragraph">
<p>Spring MVC/Web includes a single annotation for managing Cross-Origin Resource Support (CORS):</p>
</div>
<div class="hdlist">
<table>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/cors.html#_controller_method_cors_configuration">@CrossOrigin</a>
</td>
<td class="hdlist2">
<p>Enables cross-origin resource sharing (CORS) on a path.</p>
</td>
</tr>
</table>
</div>
</div>
</div>
<div class="sect2">
<h3 id="_security">Security</h3>
<div class="paragraph">
<p>Spring Security provides the following annotations:</p>
</div>
<div class="hdlist">
<table>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring-security/site/docs/current/apidocs/org/springframework/security/config/annotation/web/configuration/EnableWebSecurity.html">@EnableWebSecurity</a>
</td>
<td class="hdlist2">
<p>Adds Spring Security configuration defined in a WebSecurityConfigurer (often by extending WebSecurityConfigurerAdapter). Must be added to an @Configuration class.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-security/site/docs/current/reference/htmlsingle/#enableglobalmethodsecurity">@EnableGlobalMethodSecurity</a>
</td>
<td class="hdlist2">
<p>Class-level annotation that turns on method-level security. Must be on an @Configuration class. You must add other annotations to each method to be secured.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring-security/site/docs/4.2.3.RELEASE/apidocs/">@Secured</a>
</td>
<td class="hdlist2">
<p>Defines a list of security configuration attributes for business methods.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-security/site/docs/current/reference/htmlsingle/#el-pre-post-annotations">@PreAuthorize</a>
</td>
<td class="hdlist2">
<p>Determines whether a method can actually be invoked or not, usually based on a user role.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-security/site/docs/current/reference/htmlsingle/#el-pre-post-annotations">@PostAuthorize</a>
</td>
<td class="hdlist2">
<p>Performs an access-control check after the method has been invoked.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-security/site/docs/current/apidocs/org/springframework/security/test/context/annotation/SecurityTestExecutionListeners.html">@SecurityTestExecutionListeners</a>
</td>
<td class="hdlist2">
<p>Enables only the Spring Security <code>TestExecutionListener</code> classes (rather than all Spring <code>TestExecutionListener</code> classes)</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-security/site/docs/current/reference/htmlsingle/#test-method-withmockuser">@WithMockUser</a>
</td>
<td class="hdlist2">
<p>Runs a test as a specified mock user.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-security/site/docs/current/reference/htmlsingle/#test-method-withanonymoususer">@WithAnonymousUser</a>
</td>
<td class="hdlist2">
<p>Runs a test as an anonymous user.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-security/site/docs/current/reference/htmlsingle/#test-method-withuserdetails">@WithUserDetails</a>
</td>
<td class="hdlist2">
<p>Runs a test with user details provided by a custom <code>UserDetailsService</code>.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-security/site/docs/current/reference/htmlsingle/#test-method-withsecuritycontext">@WithSecurityContext</a>
</td>
<td class="hdlist2">
<p>Runs a test with a custom <code>SecurityContext</code>.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-security/site/docs/current/reference/htmlsingle/#filtering-using-prefilter-and-postfilter">@PostFilter</a>
</td>
<td class="hdlist2">
<p>After a method has been called, iterates through a returned collection and removes any item that doesn&#8217;t match the filter.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-security/site/docs/current/reference/htmlsingle/#filtering-using-prefilter-and-postfilter">@PreFilter</a>
</td>
<td class="hdlist2">
<p>Before a method is called, iterates through a collection and removes any item that doesn&#8217;t match the filter. (Used much more rarely than @PostFilter).</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-security/site/docs/current/reference/htmlsingle/#mvc-enablewebmvcsecurity">@EnableWebMvcSecurity</a>
</td>
<td class="hdlist2">
<p>Enables Spring Security integration with Spring MVC.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-security/site/docs/current/reference/htmlsingle/#mvc-authentication-principal">@AuthenticationPrincipal</a>
</td>
<td class="hdlist2">
<p>Automatically resolves the current <code>Authentication.getPrincipal()</code> for Spring MVC arguments.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-security/oauth/apidocs/org/springframework/security/oauth2/config/annotation/web/configuration/EnableAuthorizationServer.html">@EnableAuthorizationServer</a>
</td>
<td class="hdlist2">
<p>Convenience annotation for enabling an authorization Server (that is, an <code>AuthorizationEndpoint</code> and a <code>TokenEndpoint</code>) in the current application context, which must be a <code>DispatcherServlet</code> context.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-security/oauth/apidocs/org/springframework/security/oauth2/config/annotation/web/configuration/EnableResourceServer.html">@EnableResourceServer</a>
</td>
<td class="hdlist2">
<p>Convenience annotation for OAuth2 Resource Servers, enabling a Spring Security filter that authenticates requests via an incoming OAuth2 token.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-security/oauth/apidocs/org/springframework/security/oauth2/config/annotation/web/configuration/EnableOAuth2Client.html">@EhableOAuth2Client</a>
</td>
<td class="hdlist2">
<p>Enables configuration for an OAuth2 client in a web application that wants to use the Authorization Code Grant from one or more OAuth2 Authorization servers.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring-integration/api/org/springframework/integration/security/channel/SecuredChannel.html">@SecuredChannel</a>
</td>
<td class="hdlist2">
<p>Applies the <code>ChannelSecurityInterceptor</code>(s) using provided <code>interceptor()</code> bean name(s).</p>
</td>
</tr>
</table>
</div>
<div class="sect3">
<h4 id="_spring_websocket">Spring WebSocket</h4>
<div class="paragraph">
<p>Spring MVC/Web includes the following annotations for working with WebSockets:</p>
</div>
<div class="hdlist">
<table>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/web/socket/config/annotation/EnableWebSocket.html">@EnableWebSocket</a>
</td>
<td class="hdlist2">
<p>Enables the processing of WebSocket requests. Must be added to an <code>@Configuration</code> class.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/web/socket/config/annotation/EnableWebSocketMessageBroker.html">@EnableWebSocketMessageBroker</a>
</td>
<td class="hdlist2">
<p>Enables broker-backed messaging over WebSocket using a higher-level messaging sub-protocol. Must be added to an <code>@Configuration</code> class.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/messaging/handler/annotation/MessageMapping.html">@MessageMapping</a>
</td>
<td class="hdlist2">
<p>Maps a Message onto message-handling methods by matching to the message destination.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/messaging/handler/annotation/DestinationVariable.html">@DestinationVariable</a>
</td>
<td class="hdlist2">
<p>Indicates that a method parameter should be bound to a template variable in a destination template string.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/messaging/simp/annotation/SubscribeMapping.html">@SubscribeMapping</a>
</td>
<td class="hdlist2">
<p>Maps subscription messages onto specific handler methods based on the destination of a subscription.</p>
</td>
</tr>
</table>
</div>
</div>
</div>
<div class="sect2">
<h3 id="_rest">REST</h3>
<div class="paragraph">
<p>Spring Data REST provides the following annotations:</p>
</div>
<div class="hdlist">
<table>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/autorepo/docs/spring-data-rest/2.1.x/api/org/springframework/data/rest/core/annotation/RepositoryRestResource.html">@RepositoryRestResource</a>
</td>
<td class="hdlist2">
<p>Marks a repository for custom export mapping and rel attributes.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/autorepo/docs/spring-data-rest/2.1.x/api/org/springframework/data/rest/core/annotation/Description.html">@Description</a>
</td>
<td class="hdlist2">
<p>Describes the semantics of a resource.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/rest/docs/current/api/org/springframework/data/rest/core/annotation/HandleAfterCreate.html">@HandleAfterCreate</a>
</td>
<td class="hdlist2">
<p>Indicates a component that should handle the <code>afterCreate</code> event.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/rest/docs/current/api/org/springframework/data/rest/core/annotation/HandleAfterDelete.html">@HandleAfterDelete</a>
</td>
<td class="hdlist2">
<p>Indicates a component that should handle the <code>afterDelete</code> event.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/rest/docs/current/api/org/springframework/data/rest/core/annotation/HandleAfterLinkSave.html">@HandleAfterLinkSave</a>
</td>
<td class="hdlist2">
<p>Indicates a component that should handle the <code>afterLinkSave</code> event.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/rest/docs/current/api/org/springframework/data/rest/core/annotation/HandleAfterSave.html">@HandleAfterSave</a>
</td>
<td class="hdlist2">
<p>Indicates a component that should handle the <code>afterSave</code> event.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/rest/docs/current/api/org/springframework/data/rest/core/annotation/HandleBeforeCreate.html">@HandleBeforeCreate</a>
</td>
<td class="hdlist2">
<p>Indicates a component that should handle the <code>beforeCreate</code> event.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/rest/docs/current/api/org/springframework/data/rest/core/annotation/HandleBeforeDelete.html">@HandleBeforeDelete</a>
</td>
<td class="hdlist2">
<p>Indicates a component that should handle the <code>beforeDelete</code> event.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/rest/docs/current/api/org/springframework/data/rest/core/annotation/HandleBeforeLinkDelete.html">@HandleBeforeLinkDelete</a>
</td>
<td class="hdlist2">
<p>Indicates a component that should handle the <code>beforeLinkDelete</code> event.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/rest/docs/current/api/org/springframework/data/rest/core/annotation/HandleBeforeLinkSave.html">@HandleBeforeLinkSave</a>
</td>
<td class="hdlist2">
<p>Indicates a component that should handle the <code>beforeLinkSave</code> event.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/rest/docs/current/api/org/springframework/data/rest/core/annotation/HandleBeforeSave.html">@HandleBeforeSave</a>
</td>
<td class="hdlist2">
<p>Indicates a component that should handle the <code>beforeSave</code> event.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/rest/docs/current/api/org/springframework/data/rest/core/annotation/RepositoryEventHandler.html">@RepositoryEvenHandler</a>
</td>
<td class="hdlist2">
<p>Class-level annotation that indicates that the class is an event handler for a repository.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/rest/docs/current/api/org/springframework/data/rest/core/annotation/RestResource.html">@RestResource</a>
</td>
<td class="hdlist2">
<p>Indicates how a repository should be exported and what the value of the rel attribute in links will be.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/rest/docs/current/api/org/springframework/data/rest/core/config/Projection.html">@Projection</a>
</td>
<td class="hdlist2">
<p>Ties a particular projection type to a source type. Used to find projection interfaces at startup time.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/commons/docs/current/api/org/springframework/data/annotation/Version.html">@Version</a>
</td>
<td class="hdlist2">
<p>Identifies a property to be used as version field to implement optimistic locking on entities.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/commons/docs/current/api/org/springframework/data/annotation/AccessType.html">@AccessType</a>
</td>
<td class="hdlist2">
<p>Defines how Spring Data accesses values of persistent properties.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/commons/docs/current/api/org/springframework/data/annotation/CreatedBy.html">@CreatedBy</a>
</td>
<td class="hdlist2">
<p>Declares a field as the one representing the principal that created the entity containing the field.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/commons/docs/current/api/org/springframework/data/annotation/CreatedDate.html">@CreatedDate</a>
</td>
<td class="hdlist2">
<p>Declares a field as the one representing the date the entity containing the field was created.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/commons/docs/current/api/org/springframework/data/annotation/Id.html">@Id</a>
</td>
<td class="hdlist2">
<p>Indicates an identifier.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/commons/docs/current/api/org/springframework/data/annotation/LastModifiedBy.html">@LastModifiedBy</a>
</td>
<td class="hdlist2">
<p>Declares a field as the one representing the principal that recently modified the entity containing the field.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/commons/docs/current/api/org/springframework/data/annotation/LastModifiedDate.html">@LastModifiedDate</a>
</td>
<td class="hdlist2">
<p>Declares a field as the one representing the date the entity containing the field was recently modified.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/commons/docs/current/api/org/springframework/data/annotation/PersistenceConstructor.html">@PersistenceConstructor</a>
</td>
<td class="hdlist2">
<p>Indicates that a constructor, even one that’s package protected, as the primary constructor used by the persistence logic.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/commons/docs/current/api/org/springframework/data/annotation/Persistent.html">@Persistent</a>
</td>
<td class="hdlist2">
<p>Indicates that a field should be persisted even if there are no getter and setter methods for it.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/commons/docs/current/api/org/springframework/data/annotation/QueryAnnotation.html">@QueryAnnotation</a>
</td>
<td class="hdlist2">
<p>Meta-Annotation to mark a store-specific annotation as a query annotation. This allows generic special handing of finder methods on Repository interfaces.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/commons/docs/current/api/org/springframework/data/annotation/ReadOnlyProperty.html">@ReadOnlyProperty</a>
</td>
<td class="hdlist2">
<p>Marks a field as read-only for the mapping framework. The field will not be persisted.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/commons/docs/current/api/org/springframework/data/annotation/Reference.html">@Reference</a>
</td>
<td class="hdlist2">
<p>Meta-annotation to indicate annotations that mark references to other objects.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/commons/docs/current/api/org/springframework/data/annotation/Transient.html">@Transient</a>
</td>
<td class="hdlist2">
<p>Marks a field to be transient for the mapping framework.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/commons/docs/current/api/org/springframework/data/annotation/TypeAlias.html">@TypeAlias</a>
</td>
<td class="hdlist2">
<p>Lets <code>String</code> based type aliases to be used when writing type information for <code>PersistentEntity</code> objects.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/rest/docs/current/api/org/springframework/data/rest/webmvc/BasePathAwareController.html">@BasePathAwareController</a>
</td>
<td class="hdlist2">
<p>Indicates a controller that declares request mappings to be augmented with a base URI in the Spring Data REST configuration.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/rest/docs/current/api/org/springframework/data/rest/webmvc/RepositoryRestController.html">@RepositoryRestController</a>
</td>
<td class="hdlist2">
<p>Identifies Spring MVC controllers provided by Spring Data REST.</p>
</td>
</tr>
</table>
</div>
</div>
<div class="sect2">
<h3 id="_hateoas">HATEOAS</h3>
<div class="paragraph">
<p>Spring HATEOAS provides the following annotations:</p>
</div>
<div class="dlist">
<dl>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-hateoas/docs/0.23.0.RELEASE/reference/html/#configuration.at-enable">@EnableHypermediaSupport</a></dt>
<dd>
<p>Enables support for a particular hypermedia representation type.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-hateoas/docs/0.23.0.RELEASE/reference/html/#fundamentals.obtaining-links.entity-links">@EnableEntityLinks</a></dt>
<dd>
<p>Enables dependency injection of <code>EntityLinks</code> objects.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-hateoas/docs/0.23.0.RELEASE/reference/html/#fundamentals.obtaining-links.entity-links">@ExposesResourceFor</a></dt>
<dd>
<p>Class-level annotation for controllers. Indicates which model type the controller manages.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-hateoas/docs/0.23.0.RELEASE/reference/html/#configuration.at-enable">@Relation</a></dt>
<dd>
<p>Indicates the relation to be used when embedding objects in hypermedia.</p>
</dd>
</dl>
</div>
</div>
<div class="sect2">
<h3 id="_session">Session</h3>
<div class="paragraph">
<p>Spring Session provides the following annotations:</p>
</div>
<div class="dlist">
<dl>
<dt class="hdlist1"><a href="https://docs.spring.io/spring-session/docs/current-SNAPSHOT/api/org/springframework/session/data/redis/config/annotation/web/http/EnableRedisHttpSession.html">@EnableRedisHttpSession</a></dt>
<dd>
<p>Exposes the SessionRepositoryFilter as a bean named "springSessionRepositoryFilter" and backed by Redis. Must be added to an @Configuration class.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-session/docs/current/api/org/springframework/session/data/gemfire/config/annotation/web/http/EnableGemFireHttpSession.html">@EnableGemFireHttpSession</a></dt>
<dd>
<p>Exposes the SessionRepositoryFilter as a bean named "springSessionRepositoryFilter" and backed by Pivotal GemFire or Apache Geode. Must be added to an @Configuration class.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-session/docs/current/api/org/springframework/session/jdbc/config/annotation/web/http/EnableJdbcHttpSession.html">@EnableJdbcHttpSession</a></dt>
<dd>
<p>Exposes the SessionRepositoryFilter as a bean named "springSessionRepositoryFilter" and backed by a relational database. Must be added to an @Configuration class.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-session/docs/current/api/org/springframework/session/data/mongo/config/annotation/web/http/EnableMongoHttpSession.html">@EnableMongoHttpSession</a></dt>
<dd>
<p>Exposes the SessionRepositoryFilter as a bean named "springSessionRepositoryFilter" and backed by Mongo. Must be added to an @Configuration class.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-session/docs/current/api/org/springframework/session/hazelcast/config/annotation/web/http/EnableHazelcastHttpSession.html">@EnableHazelcastHttpSession</a></dt>
<dd>
<p>Exposes the SessionRepositoryFilter as a bean named "springSessionRepositoryFilter" and backed by Hazelcast. Must be added to an @Configuration class.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-session/docs/current/api/org/springframework/session/config/annotation/web/http/EnableSpringHttpSession.html">@EnableSpringHttpSession</a></dt>
<dd>
<p>Exposes the SessionRepositoryFilter as a bean named "springSessionRepositoryFilter" and backed by a user provided implementation of SessionRepository. Must be added to an @Configuration class.</p>
</dd>
</dl>
</div>
</div>
<div class="sect2">
<h3 id="_boot">Boot</h3>
<div class="paragraph">
<p>Spring Boot provides the following annotations:</p>
</div>
<div class="dlist">
<dl>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#using-boot-using-springbootapplication-annotation">@SpringBootApplication</a></dt>
<dd>
<p>Convenience annotation that includes @Configuration, @EnableAutoConfiguration, and @ComponentScan</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#getting-started-first-application-auto-configuration">@EnableAutoConfiguration</a></dt>
<dd>
<p>tells Spring Boot to determine how you will want to configure Spring, based on the jar dependencies that you have added.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/autoconfigure/domain/EntityScan.html">@EntityScan</a></dt>
<dd>
<p>Configures the base packages used by auto-configuration when scanning for entity classes.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-external-config">@ConfigurationProperties</a></dt>
<dd>
<p>Identifies a class a configuration properties class, which can then be used to control and validate configuration.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/autorepo/docs/spring-boot/1.2.0.M2/api/org/springframework/boot/context/properties/EnableConfigurationProperties.html">@@EnableConfigurationProperties</a></dt>
<dd>
<p>Enables support for <code>@ConfigurationProperties</code> annotated beans.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/context/properties/ConfigurationPropertiesBinding.html">@ConfigurationPropertiesBinding</a></dt>
<dd>
<p>Qualifier for beans that are needed to configure the binding of <code>ConfigurationProperties</code> (often converters).</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-json-components">@JsonComponent</a></dt>
<dd>
<p>Provides JsonSerializer and/or JsonDeserializer implementations to be registered with Jackson when <code>JsonComponentModule</code> is in use.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-embedded-container-context-initializer">@ServletComponentScan</a></dt>
<dd>
<p>Enables automatic registration of classes annotated with @WebServlet, @WebFilter, and @WebListener.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/autoconfigure/security/oauth2/client/EnableOAuth2Sso.html">@EnableOAuth2Sso</a></dt>
<dd>
<p>Enables OAuth2 Single Sign On (SSO).</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-testing-spring-boot-applications">@SpringBootTest</a></dt>
<dd>
<p>Creates an <code>ApplicationContext</code> object that supports testing a Spring Boot application.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-testing-spring-boot-applications">@AutoConfigureMockMvc</a></dt>
<dd>
<p>Configures a <code>MockMvc</code> object for use when testing Spring Boot applications.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/SpringBootConfiguration.html">@SpringBootConfiguration</a></dt>
<dd>
<p>Indicates that a class provides Spring Boot application <code>@Configuration</code>. Can be used as an alternative to the Spring&#8217;s standard <code>@Configuration</code> annotation so that configuration can be found automatically (for example in tests). An application should include only one @SpringBootConfiguration, and most idiomatic Spring Boot applications will inherit it from @SpringBootApplication.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/test/context/TestConfiguration.html">@TestConfiguration</a></dt>
<dd>
<p>@Configuration that can be used to define additional beans or customizations for a test. Unlike regular @Configuration classes the use of @TestConfiguration does not prevent auto-detection of @SpringBootConfiguration.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/context/embedded/LocalServerPort.html">@LocalServerPort</a></dt>
<dd>
<p>Annotation at the field or method/constructor parameter level that injects the HTTP port that got allocated at runtime. Provides a convenient alternative for <code>@Value("${local.server.port}")</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/test/mock/mockito/MockBean.html">@MockBean</a></dt>
<dd>
<p>Adds a mock bean to a Spring <code>ApplicationContext</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/test/mock/mockito/SpyBean.html">@Spybean</a></dt>
<dd>
<p>Applies Mockito spies to a Spring <code>ApplicationContext</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/autoconfigure/ImportAutoConfiguration.html">@ImportAutoConfiguration</a></dt>
<dd>
<p>Imports and applies the specified auto-configuration classes. Sometimes useful for testing. Generally, @EnableAutoConfiguration should be preferred.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-testing-spring-boot-applications-testing-autoconfigured-json-tests">@JsonTest</a></dt>
<dd>
<p>Auto-configures Jackson <code>ObjectMapper</code>, any <code>@JsonComponent</code> beans and any Jackson <code>Modules</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/test/autoconfigure/web/servlet/WebMvcTest.html">@WebMvcTest</a></dt>
<dd>
<p>Used with @RunWith(SpringRunner.class) for a typical Spring MVC test. Can be used when a test focuses only on Spring MVC components. Using this annotation will disable full auto-configuration and instead apply only configuration relevant to MVC tests.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/test/autoconfigure/orm/jpa/DataJpaTest.html">@DataJpaTest</a></dt>
<dd>
<p>Annotation that can be used in combination with <code>@RunWith(SpringRunner.class)</code> for a typical JPA test. Can be used when a test focuses <strong>only</strong> on JPA components.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/test/autoconfigure/orm/jpa/AutoConfigureTestEntityManager.html">@AutoConfigureTestEntityManager</a></dt>
<dd>
<p>Can be applied to a test class to enable auto-configuration of a TestEntityManager.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/test/autoconfigure/orm/jpa/AutoConfigureTestDatabase.html">@AutoConfigureTestDatabase</a></dt>
<dd>
<p>Can be applied to a test class to configure a test database to use instead of any application defined or auto-configured DataSource.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-testing-spring-boot-applications-testing-autoconfigured-jdbc-test">@JdbcTest</a></dt>
<dd>
<p>Annotation that can be used in combination with <code>@RunWith(SpringRunner.class)</code> for a typical JDBC test. By default, it will also configure an in-memory embedded database and a <code>JdbcTemplate</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-testing-spring-boot-applications-testing-autoconfigured-mongo-test">@DataMongoTest</a></dt>
<dd>
<p>Used to test MongoDB applications. By default, it will configure an in-memory embedded MongoDB (if available), configure a MongoTemplate, scan for @Document classes and configure Spring Data MongoDB repositories.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-testing-spring-boot-applications-testing-autoconfigured-rest-client">@RestClientTest</a></dt>
<dd>
<p>Used to test REST clients. By default, it will auto-configure Jackson and GSON support, configure a RestTemplateBuilder and add support for MockRestServiceServer.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-testing-spring-boot-applications-testing-autoconfigured-rest-docs">@AutoConfigureRestDocs</a></dt>
<dd>
<p>Used to use Spring REST Docs in your tests. It will automatically configure MockMvc to use Spring REST Docs and remove the need for Spring REST Docs' JUnit rule.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/autorepo/docs/spring-boot/1.2.6.RELEASE/api/org/springframework/boot/test/WebIntegrationTest.html">@WebIntegrationTest</a></dt>
<dd>
<p>Test class annotation signifying that the tests are "web integration tests" and therefore require full startup in the same way as a production application (listening on normal ports). Normally used in conjunction with <code>@SpringApplicationConfiguration</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/autorepo/docs/spring-boot/1.2.6.RELEASE/api/org/springframework/boot/test/SpringApplicationConfiguration.html">@SpringApplicationConfiguration</a></dt>
<dd>
<p>Class-level annotation that is used to determine how to load and configure an ApplicationContext for integration tests. Similar to the standard <code>ContextConfiguration</code> but uses Spring Boot&#8217;s <code>SpringApplicationContextLoader</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/autoconfigure/condition/ConditionalOnClass.html">@ConditionalOnClass</a></dt>
<dd>
<p>Matches only when the specified classes are on the classpath.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/autoconfigure/condition/ConditionalOnMissingBean.html">@ConditionalOnMissingBean</a></dt>
<dd>
<p>Matches only when the specified bean classes and/or names are not already contained in the BeanFactory.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-locating-auto-configuration-candidates">@AutoConfigureBefore</a></dt>
<dd>
<p>Used when configurations need to be loaded in a particular order.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-locating-auto-configuration-candidates">@AutoConfigureAfter</a></dt>
<dd>
<p>Used when configurations need to be loaded in a particular order.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-locating-auto-configuration-candidates">@AutoconfigureOrder</a></dt>
<dd>
<p>Allows for ordering certain auto-configurations that shouldn’t have any direct knowledge of each other.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/autoconfigure/condition/ConditionalOnProperty.html">@ConditionalOnProperty</a></dt>
<dd>
<p>Checks whether the specified properties have the specified value.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/autoconfigure/condition/ConditionalOnResource.html">@ConditionalOnResource</a></dt>
<dd>
<p>Lets configuration to be included only when a specific resource is present.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/autoconfigure/condition/ConditionalOnWebApplication.html">@ConditionalOnWebApplication</a></dt>
<dd>
<p>Matches only when the application context is a web application</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/autoconfigure/condition/ConditionalOnNotWebApplication.html">@ConditionalOnNotWebApplication</a></dt>
<dd>
<p>Matches only when the application context is not a web application.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/autoconfigure/condition/ConditionalOnExpression.html">@ConditionalOnExpression</a></dt>
<dd>
<p>Lets configuration be included based on the result of a SpEL expression.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/actuate/autoconfigure/ManagementContextConfiguration.html">@ManagementContextConfiguration</a></dt>
<dd>
<p>Specialized @Configuration class that defines configuration specific for the management context. Configurations should be registered in /META-INF/spring.factories under the org.springframework.boot.actuate.autoconfigure.ManagementContextConfiguration key.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/actuate/autoconfigure/ExportMetricWriter.html">@ExportMetricWriter</a></dt>
<dd>
<p>Qualifier annotation for a metric repository that is to be used to export metrics from the ExportMetricReader readers.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/actuate/autoconfigure/ExportMetricReader.html">@ExportMetricReader</a></dt>
<dd>
<p>Qualifier annotation for a metric reader that can be exported (to distinguish it from others that might be installed by the user for other purposes).</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#howto-execute-flyway-database-migrations-on-startup">@FlywayDataSource</a></dt>
<dd>
<p>Specifies a DataSource to be injected into Flyway. If used for a second data source, the other (main) one would normally be marked as <code>{@code @Primary}</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#howto-execute-liquibase-database-migrations-on-startup">@LiquibaseDataSource</a></dt>
<dd>
<p>Specifies a DataSource to be injected into Liquibase. If used for a second data source, the other (main) one would normally be marked as <code>{@code @Primary}</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/context/properties/DeprecatedConfigurationProperty.html">@DeprecatedConfigurationProperty</a></dt>
<dd>
<p>Indicates that a getter in a <code>ConfigurationProperties</code> object is deprecated. This annotation has no bearing on the actual binding processes, but it is used by the <code>spring-boot-configuration-processor</code> to add deprecation meta-data.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/context/properties/NestedConfigurationProperty.html">@NestedConfigurationProperty</a></dt>
<dd>
<p>Indicates that a field in a ConfigurationProperties object should be treated as if it were a nested type.</p>
</dd>
</dl>
</div>
</div>
<div class="sect2">
<h3 id="_integration">Integration</h3>
<div class="paragraph">
<p>Spring integration includes the following annotations:</p>
</div>
<div class="dlist">
<dl>
<dt class="hdlist1"><a href="https://docs.spring.io/spring-integration/api/org/springframework/integration/config/EnableIntegration.html">@EnableIntegration</a></dt>
<dd>
<p>Enables Spring Integration infrastructure, registers built-in beans, adds BeanFactoryPostProcessors, adds BeanPostProcessors, and adds annotation processors.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/config/EnableIntegrationManagement.html">@EnableIntegrationManagement</a></dt>
<dd>
<p>Enables default configuration of management in Spring Integration components in an existing application.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/config/EnableMessageHistory.html">@EnableMessageHistory</a></dt>
<dd>
<p>Enables MessageHistory for Integration components.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/config/EnablePublisher.html">@EnablePublisher</a></dt>
<dd>
<p>Provides the registration for the PublisherAnnotationBeanPostProcessor to allow the use of the Publisher annotation.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/IntegrationComponentScan.html">@IntegrationComponentScan</a></dt>
<dd>
<p>Configures component scanning directives for use with Configuration classes.</p>
</dd>
<dt class="hdlist1"><a href="https://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/Publisher.html">@Publisher</a></dt>
<dd>
<p>Indicates that a method (or all public methods if applied at class-level) should publish Messages.</p>
</dd>
<dt class="hdlist1"><a href="https://docs.spring.io/spring-integration/api/org/springframework/integration/config/GlobalChannelInterceptor.html">@GlobalChannelInterceptor</a></dt>
<dd>
<p><code>ChannelInterceptor</code> components with this annotation will be applied as global channel interceptors using the provided patterns to match channel names.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/Aggregator.html">@Aggregator</a></dt>
<dd>
<p>Indicates that a method is capable of aggregating messages.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/BridgeFrom.html">@BridgeFrom</a></dt>
<dd>
<p>Marks a <code>Bean</code> method for a <code>MessageChannel</code> to produce a <code>BridgeHandler</code> and <code>Consumer Endpoint</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/BridgeTo.html">@BridgeTo</a></dt>
<dd>
<p>Marks a Bean method for a MessageChannel to produce a BridgeHandler and Consumer Endpoint.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/CorrelationStrategy.html">@CorrelationStrategy</a></dt>
<dd>
<p>Indicates that a given method is capable of determining the correlation key of a message sent as parameter.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/Filter.html">@Filter</a></dt>
<dd>
<p>Indicates that a method is capable of playing the role of a Message Filter.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/Gateway.html">@Gateway</a></dt>
<dd>
<p>Indicates that an interface method is capable of mapping its parameters to a message or message payload.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/GatewayHeader.html">@GatewayHeaer</a></dt>
<dd>
<p>Provides the message header value or expression.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/IdempotentReceiver.html">@IdempotentReceiver</a></dt>
<dd>
<p>A method that has a Messaging annotation (<code>@code</code>, <code>@ServiceActivator</code>, <code>@Router</code> etc.) that also has this annotation has an <code>IdempotentReceiverInterceptor</code> applied to the associated <code>MessageHandler.handleMessage(org.springframework.messaging.Message&lt;?&gt;)</code> method.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/InboundChannelAdapter.html">@InboundChannelAdapter</a></dt>
<dd>
<p>Indicates that a method is capable of producing a <code>Message</code> payload.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/IntegrationComponentScan.html">@IntegrationComponentScan</a></dt>
<dd>
<p>Configures component scanning directives for use with <code>Configuration</code> classes.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/MessageEndpoint.html">@MessageEndpoint</a></dt>
<dd>
<p>Stereotype annotation indicating that a class is capable of serving as a Message endpoint.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/MessagingGateway.html">@MessagingGateway</a></dt>
<dd>
<p>Provides an Integration Messaging Gateway Proxy (&lt;gateway/&gt;) as an abstraction over the messaging API.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/Payloads.html">@Payloads</a></dt>
<dd>
<p>Marks a method parameter as being a list of message payloads, for POJO handlers that deal with lists of messages.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/Poller.html">@Poller</a></dt>
<dd>
<p>Provides the <code>PollerMetadata</code> options for the Messaging annotations for polled endpoints.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/Publisher.html">@Publisher</a></dt>
<dd>
<p>Indicates that a method (or all public methods if applied at class-level) should publish Messages.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/ReleaseStrategy.html">@ReleaseStrategy</a></dt>
<dd>
<p>Indicates that a method is capable of asserting if a list of messages or payload objects is complete.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/Role.html">@Role</a></dt>
<dd>
<p>Assigns endpoints to a role. The assigned endpoints can be started and stopped as a group.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/Router.html">@Router</a></dt>
<dd>
<p>Indicates that a method is capable of resolving to a channel or channel name based on a message, message header(s), or both.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/ServiceActivator.html">@ServiceActivator</a></dt>
<dd>
<p>Indicates that a method is capable of handling a message or message payload.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/Splitter.html">@Splitter</a></dt>
<dd>
<p>Indicates that a method is capable of splitting a single message or message payload to produce multiple messages or payloads.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/annotation/Transformer.html">@Transformer</a></dt>
<dd>
<p>Indicates that a method is capable of transforming a message, message header, or message payload.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/config/IntegrationConverter.html">@IntegrationConverter</a></dt>
<dd>
<p>Registers <code>Converter</code>, <code>GenericConverter</code> or <code>ConverterFactory</code> beans for the <code>integrationConversionService</code>.</p>
</dd>
<dt class="hdlist1"><a href="https://docs.spring.io/spring-integration/api/org/springframework/integration/jmx/config/EnableIntegrationMBeanExport.html">@EnableIntegrationMBeanExport</a></dt>
<dd>
<p>Enables default exporting for Spring Integration components in an existing application and all @ManagedResource annotated beans.</p>
</dd>
<dt class="hdlist1"><a href="https://docs.spring.io/spring/docs/4.3.9.RELEASE/javadoc-api/org/springframework/context/annotation/EnableMBeanExport.html">@EnableMBeanExport</a></dt>
<dd>
<p>Enables default exporting of all standard MBeans from the Spring context and all @ManagedResource annotated beans.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-integration/api/org/springframework/integration/support/management/IntegrationManagedResource.html">@IntegrationManagedResource</a></dt>
<dd>
<p>Clone of ManagedResource limiting beans thus annotated so that they will only be exported by the IntegrationMBeanExporter and prevented from being exported by other MBeanExporters (if present).</p>
</dd>
<dt class="hdlist1"><a href="https://docs.spring.io/spring-integration/api/org/springframework/integration/http/config/EnableIntegrationGraphController.html">@EnableIntegrationGraphController</a></dt>
<dd>
<p>Enables the <code>IntegrationGraphController</code> if DispatcherServlet is present in the classpath.</p>
</dd>
</dl>
</div>
</div>
<div class="sect2">
<h3 id="_cloud">Cloud</h3>
<div class="paragraph">
<p>Spring Cloud includes the following annotations:</p>
</div>
<div class="paragraph">
<p>{JB: Start here: <a href="http://cloud.spring.io/spring-cloud-static/spring-cloud.html}" class="bare">http://cloud.spring.io/spring-cloud-static/spring-cloud.html}</a></p>
</div>
<div class="hdlist">
<table>
<tr>
<td class="hdlist1">
<a href="https://github.com/spring-cloud/spring-cloud-commons/blob/master/spring-cloud-context/src/main/java/org/springframework/cloud/context/scope/refresh/RefreshScope.java">@RefreshScope</a>
</td>
<td class="hdlist2">
<p>Lets beans be refreshed dynamically at runtime.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://github.com/spring-cloud/spring-cloud-commons/blob/master/spring-cloud-commons/src/main/java/org/springframework/cloud/client/discovery/EnableDiscoveryClient.java">@EnableDiscoveryClient</a>
</td>
<td class="hdlist2">
<p>looks for implementations of the <code>DiscoveryClient</code> interface via <code>META-INF/spring.factories</code>.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://cloud.spring.io/spring-cloud-static/spring-cloud.html#_embedding_the_config_server">@EnableConfigServer</a>
</td>
<td class="hdlist2">
<p>Embeds the Spring Cloud Config Server in another Spring application.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://cloud.spring.io/spring-cloud-static/spring-cloud.html#_service_discovery_eureka_clients">@EnableEurekaServer</a>
</td>
<td class="hdlist2">
<p>Enables the Netflix Eureka Service Discovery client.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://github.com/spring-cloud/spring-cloud-commons/blob/master/spring-cloud-commons/src/main/java/org/springframework/cloud/client/circuitbreaker/EnableCircuitBreaker.java">@EnableCircuitBreaker</a>
</td>
<td class="hdlist2">
<p>Enables a circuit breaker implementation for an application.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://projects.spring.io/spring-cloud/spring-cloud.html#_circuit_breaker_hystrix_clients">@EnableHystrix</a>
</td>
<td class="hdlist2">
<p>Enables the Hystrix circuit breaker. Must go on an application class (such as a class marked with @SpringBootApplication).</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://cloud.spring.io/spring-cloud-static/spring-cloud.html#_circuit_breaker_hystrix_clients">@HystrixCommand</a>
</td>
<td class="hdlist2">
<p>Indicates that a bean should be wrapped in a proxy that is connected to the Hystrix circuit breaker.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://cloud.spring.io/spring-cloud-static/spring-cloud.html#_circuit_breaker_hystrix_clients">@HystrixProperty</a>
</td>
<td class="hdlist2">
<p>Sets a property for the @HystrixCommand annotation. See the <a href="https://github.com/Netflix/Hystrix/wiki/Configuration">@Hystrix wiki</a>.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://cloud.spring.io/spring-cloud-static/spring-cloud.html#_circuit_breaker_hystrix_dashboard">@EnableHystrixDashboard</a>
</td>
<td class="hdlist2">
<p>Enables the Hystrix dashboard. Must go on a Spring Boot main class.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://cloud.spring.io/spring-cloud-static/spring-cloud.html#_turbine">@EnableTurbine</a>
</td>
<td class="hdlist2">
<p>Enables the Turbine application for a Spring application. Must go on a Spring Boot main class.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://cloud.spring.io/spring-cloud-static/spring-cloud.html#_turbine_stream">@EnableTurbineStream</a>
</td>
<td class="hdlist2">
<p>Enables the Turbine Stream application for a Spring application. Must go on a Spring Boot main class.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://github.com/spring-cloud/spring-cloud-netflix/blob/master/spring-cloud-netflix-core/src/main/java/org/springframework/cloud/netflix/feign/FeignClient.java">@FeignClient</a>
</td>
<td class="hdlist2">
<p>Declares that a REST client should be created for the specified interface.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://github.com/spring-cloud/spring-cloud-netflix/blob/master/spring-cloud-netflix-core/src/main/java/org/springframework/cloud/netflix/feign/EnableFeignClients.java">@EnableFeignCLients</a>
</td>
<td class="hdlist2">
<p>Scans for interfaces that declare they are feign clients. Must go on the application class.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://github.com/spring-cloud/spring-cloud-netflix/blob/master/spring-cloud-netflix-core/src/main/java/org/springframework/cloud/netflix/ribbon/RibbonClient.java">@RibbonClient</a>
</td>
<td class="hdlist2">
<p>Declares a ribbon client. Must go on an @Configuration class.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://github.com/spring-cloud/spring-cloud-netflix/blob/master/spring-cloud-netflix-core/src/main/java/org/springframework/cloud/netflix/ribbon/RibbonClients.java">@RibbonClients</a>
</td>
<td class="hdlist2">
<p>Convenience annotation that combines multiple <code>@RibbonClient</code> annotations on a single class (including in Java 7).</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://github.com/spring-cloud/spring-cloud-netflix/blob/master/spring-cloud-netflix-core/src/main/java/org/springframework/cloud/netflix/zuul/EnableZuulProxy.java">@EnableZuulProxy</a>
</td>
<td class="hdlist2">
<p>Sets up a Zuul server endpoint and installs some reverse proxy filters in it, so it can forward requests to backend servers. The backends can be registered manually through configuration or via a  <code>DiscoveryClient</code>.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://github.com/spring-cloud/spring-cloud-netflix/blob/master/spring-cloud-netflix-core/src/main/java/org/springframework/cloud/netflix/metrics/atlas/EnableAtlas.java">@EnableAtlas</a>
</td>
<td class="hdlist2">
<p>Enables Atlas metrics publishing.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://github.com/spring-cloud/spring-cloud-stream/blob/master/spring-cloud-stream/src/main/java/org/springframework/cloud/stream/annotation/EnableBinding.java">@EnableBinding</a>
</td>
<td class="hdlist2">
<p>Enables the binding of targets annotated with <code>Input</code> and <code>Output</code> to a broker, according to the list of interfaces passed as value to the annotation.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-cloud-stream/docs/Brooklyn.M1/api/org/springframework/cloud/stream/annotation/StreamListener.html">@StreamListener</a>
</td>
<td class="hdlist2">
<p>Indicates a method that is a listener to the inputs declared through <code>@EnableBinding</code>.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-cloud-stream/docs/Chelsea.SR2/api/org/springframework/cloud/stream/annotation/Input.html">@Input</a>
</td>
<td class="hdlist2">
<p>Indicates that an input binding target will be created by the framework.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-cloud-stream/docs/Chelsea.SR2/api/org/springframework/cloud/stream/annotation/Output.html">@Output</a>
</td>
<td class="hdlist2">
<p>Indicates that an output binding target will be created by the framework.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-cloud-stream/docs/Brooklyn.M1/api/org/springframework/cloud/stream/annotation/rxjava/EnableRxJavaProcessor.html">@EnableRxJavaProcessor</a>
</td>
<td class="hdlist2">
<p>Class annotation that identifies the class as an RxJava processor module.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://github.com/spring-cloud/spring-cloud-sleuth/blob/master/spring-cloud-sleuth-zipkin-stream/src/main/java/org/springframework/cloud/sleuth/zipkin/stream/EnableZipkinStreamServer.java">@EnableZipkinStreamServer</a>
</td>
<td class="hdlist2">
<p>Enables transporting of spans over a Spring Cloud Stream (such as RabbitMQ).</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://github.com/spring-cloud/spring-cloud-sleuth/blob/master/spring-cloud-sleuth-core/src/main/java/org/springframework/cloud/sleuth/SpanName.java">@SpanName</a>
</td>
<td class="hdlist2">
<p>Names a span for use with a stream.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://github.com/spring-cloud/spring-cloud-commons/blob/master/spring-cloud-commons/src/main/java/org/springframework/cloud/client/loadbalancer/LoadBalanced.java">@LoadBalanced</a>
</td>
<td class="hdlist2">
<p>Indicates that a <code>RestTemplate</code> bean should be configured to use a <code>LoadBalancerClient</code>.</p>
</td>
</tr>
</table>
</div>
</div>
<div class="sect2">
<h3 id="_data">Data</h3>
<div class="paragraph">
<p>Spring includes the following annotations:</p>
</div>
<div class="hdlist">
<table>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/jpa/docs/current/api/org/springframework/data/jpa/repository/config/EnableJpaRepositories.html">@EnableJpaRepositories</a>
</td>
<td class="hdlist2">
<p>Class-level annotation that enables JPA repositories. By default, scans the package of the annotated <code>@Configuration</code> class for Spring Data repositories.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/jpa/docs/current/api/org/springframework/data/jpa/repository/config/EnableJpaAuditing.html">@EnableJpaAuditing</a>
</td>
<td class="hdlist2">
<p>Class-level annotation that enables auditing in JPA. Must be on an <code>@Configuration</code> class.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/commons/docs/current/api/org/springframework/data/repository/RepositoryDefinition.html">@RepositoryDefinition</a>
</td>
<td class="hdlist2">
<p>Indicates the interfaces for which a repository proxy is to be created. Annotating an interface with <code>@RepositoryDefinition</code> will cause the same behavior as extending <code>Repository</code>.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/commons/docs/current/api/org/springframework/data/repository/NoRepositoryBean.html">@NoRepositoryBean</a>
</td>
<td class="hdlist2">
<p>Indicates an interface for which Spring should not create an instance at runtime.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/data-mongo/docs/1.10.4.RELEASE/api/http://docs.spring.io/spring-data/data-mongo/docs/1.10.4.RELEASE/api/org/springframework/data/mongodb/core/mapping/Document.html">@Document</a>
</td>
<td class="hdlist2">
<p>Identifies a domain object to be persisted to MongoDB.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/data-mongo/docs/1.10.4.RELEASE/api/org/springframework/data/mongodb/core/mapping/DBRef.html">@DBRef</a>
</td>
<td class="hdlist2">
<p>Indicates that the annotated field is to be stored using a DBRef.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/data-mongo/docs/1.10.4.RELEASE/api/org/springframework/data/mongodb/core/mapping/Field.html">@Field</a>
</td>
<td class="hdlist2">
<p>Defines custom metadata for a document field.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/data-mongo/docs/1.10.4.RELEASE/api/org/springframework/data/mongodb/core/mapping/Language.html">@Language</a>
</td>
<td class="hdlist2">
<p>Marks a property as being a language field.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/data-mongo/docs/1.10.4.RELEASE/api/org/springframework/data/mongodb/core/mapping/TextScore.html">@TextScore</a>
</td>
<td class="hdlist2">
<p>Marks a property to be considered when doing a full-text search. Important: The property will not be saved when the entity is saved.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/mongodb/docs/current/api/org/springframework/data/mongodb/repository/config/EnableMongoRepositories.html">@EnableMongoRepositories</a>
</td>
<td class="hdlist2">
<p>Activates MongoDB repositories. If no base package is configured through <code>value()</code>, <code>basePackages()</code>, or <code>basePackageClasses()</code>, it will trigger scanning of the package of annotated class.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/jpa/docs/1.11.4.RELEASE/api/org/springframework/data/jpa/repository/Query.html">@Query</a>
</td>
<td class="hdlist2">
<p>Declares a finder query on a repository method.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/jpa/docs/1.11.4.RELEASE/api/org/springframework/data/jpa/repository/EntityGraph.html">@EntityGraph</a>
</td>
<td class="hdlist2">
<p>Configures the JPA 2.1 EntityGraphs that should be used on repository methods.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/jpa/docs/1.11.4.RELEASE/api/org/springframework/data/jpa/repository/Lock.html">@Lock</a>
</td>
<td class="hdlist2">
<p>Specifies the <code>LockModeType</code> to be used when executing a query.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/jpa/docs/1.11.4.RELEASE/api/org/springframework/data/jpa/repository/Modifying.html">@Modifying</a>
</td>
<td class="hdlist2">
<p>Indicates a method should be regarded as a modifying query.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/jpa/docs/1.11.4.RELEASE/api/org/springframework/data/jpa/repository/QueryHints.html">@QueryHints</a>
</td>
<td class="hdlist2">
<p>Applies JPA query hints to a query declared in a repository interface.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/jpa/docs/1.11.4.RELEASE/api/org/springframework/data/jpa/repository/Temporal.html">@Temporal</a>
</td>
<td class="hdlist2">
<p>Declares an appropriate <code>TemporalType</code> on query method parameters. Can only be used on parameters of type <code>Date</code>.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/data-commons/docs/1.13.4.RELEASE/api/org/springframework/data/domain/DomainEvents.html">@DomainEvents</a>
</td>
<td class="hdlist2">
<p>Indicates a method that publishes domain events. A method marked with <code>@AfterDomainEventsPublication</code> can then be used to manipulated the published events.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/data-commons/docs/1.13.4.RELEASE/api/org/springframework/data/domain/AfterDomainEventPublication.html">@AfterDomainEventPublication</a>
</td>
<td class="hdlist2">
<p>Indicates a method that manipulates published domain events (often for selecting only events that meet some particular criterion).</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/commons/docs/current/api/org/springframework/data/web/config/EnableSpringDataWebSupport.html">@EnableSpringDataWebSupport</a>
</td>
<td class="hdlist2">
<p>Automatically register the following beans for usage with Spring MVC: <code>DomainClassConverter</code>, <code>PageableHandlerMethodArgumentResolver</code>, and <code>SortHandlerMethodArgumentResolver</code>. If Spring HATEOAS is on the classpath, it also registers <code>HateoasPageableHandlerMethodArgumentResolver</code>, <code>HateoasSortHandlerMethodArgumentResolver</code>, <code>PagedResourcesAssembler</code>, and <code>SortHandlerMethodArgumentResolver</code>.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/data-commons/docs/1.13.4.RELEASE/api/org/springframework/data/web/PageableDefault.html">@PageableDefault</a>
</td>
<td class="hdlist2">
<p>Set defaults when injecting a <code>Pageable</code> into a controller method.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/data-commons/docs/1.13.4.RELEASE/api/org/springframework/data/web/SortDefault.html">@SortDefault</a>
</td>
<td class="hdlist2">
<p>Defines the default Sort options to be used when injecting a Sort instance into a controller handler method.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/data-commons/docs/1.13.4.RELEASE/api/org/springframework/data/web/SortDefault.SortDefaults.html">@SortDefaults</a>
</td>
<td class="hdlist2">
<p>Wrapper annotation to allow declaring multiple SortDefault annotations on a method parameter.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/data-commons/docs/1.13.4.RELEASE/api/org/springframework/data/web/JsonPath.html">@JsonPath</a>
</td>
<td class="hdlist2">
<p>Declares a JSON Path expression on a projection interface.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/data-commons/docs/1.13.4.RELEASE/api/org/springframework/data/web/ProjectedPayload.html">@ProjectedPayload</a>
</td>
<td class="hdlist2">
<p>Enables projection and projection method annotations that contain JSON or XPath expressions.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/data-commons/docs/1.13.4.RELEASE/api/org/springframework/data/querydsl/binding/QuerydslPredicate.html">QuerydslPredicate</a>
</td>
<td class="hdlist2">
<p>Customizes the binding of HTTP request parameters to a <code>Querydsl com.mysema.query.types.Predicate</code> in Spring MVC handler methods.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-data/jpa/docs/current/api/org/springframework/data/jpa/repository/query/Procedure.html">@Procedure</a>
</td>
<td class="hdlist2">
<p>Declares a JPA 2.1 stored procedure mapping directly on a repository method.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring-framework/docs/3.2.0.M2/api/org/springframework/transaction/annotation/EnableTransactionManagement.html">@EnableTransactionManagement</a>
</td>
<td class="hdlist2">
<p>Enables Spring&#8217;s annotation-driven transaction management capability.</p>
</td>
</tr>
</table>
</div>
</div>
<div class="sect2">
<h3 id="_batch">Batch</h3>
<div class="paragraph">
<p>Spring Batch includes the following annotations:</p>
</div>
<div class="dlist">
<dl>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/annotation/AfterChunk.html">@AfterChunk</a></dt>
<dd>
<p>Marks a method to be called after a chunk is executed.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/annotation/AfterChunkError.html">@AfterChunkError</a></dt>
<dd>
<p>Marks a method to be called after a has failed and been marked for rollback.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/annotation/AfterJob.html">@AfterJob</a></dt>
<dd>
<p>Marks a method to be called after a Job has completed.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/annotation/AfterProcess.html">@AfterProcess</a></dt>
<dd>
<p>Marks a method to be called after an item is passed to an <code>ItemProcessor</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/annotation/AfterRead.html">@AfterRead</a></dt>
<dd>
<p>Marks a method to be called after an item is read from an <code>ItemReader</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/annotation/AfterStep.html">@AfterStep</a></dt>
<dd>
<p>Marks a method to be called after a <code>Step</code> has completed.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/annotation/AfterWrite.html">@AfterWrite</a></dt>
<dd>
<p>Marks a method to be called after an item is passed to an <code>ItemWriter</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/annotation/BeforeChunk.html">@BeforeChunk</a></dt>
<dd>
<p>Marks a method to be called before a chunk is executed.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/annotation/BeforeJob.html">@BeforeJob</a></dt>
<dd>
<p>Marks a method to be called before a <code>Job</code> is executed, which comes after a <code>JobExecution</code> is created and persisted, but before the first <code>Step</code> is executed.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/annotation/BeforeProcess.html">@BeforeProcess</a></dt>
<dd>
<p>Marks a method to be called before an item is passed to an <code>ItemProcessor</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/annotation/BeforeRead.html">@BeforeRead</a></dt>
<dd>
<p>Marks a method to be called before an item is read from an <code>ItemReader</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/annotation/BeforeStep.html">@BeforeStep</a></dt>
<dd>
<p>Marks a method to be called before a <code>Step</code> is executed, which comes after a <code>StepExecution</code> is created and persisted, but before the first item is read.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/annotation/BeforeWrite.html">@BeforeWrite</a></dt>
<dd>
<p>Marks a method to be called before an item is passed to an <code>ItemWriter</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/annotation/OnProcessError.html">@OnProcessError</a></dt>
<dd>
<p>Marks a method to be called if an exception is thrown by an <code>ItemProcessor</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/annotation/OnReadError.html">@OnReadError</a></dt>
<dd>
<p>Marks a method to be called if an exception is thrown by an <code>ItemReader</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/annotation/OnSkipInProcess.html">@OnSkipInProcess</a></dt>
<dd>
<p>Marks a method to be called when an item is skipped due to an exception thrown in the <code>ItemProcessor</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/annotation/OnSkipInRead.html">@OnSkipInRead</a></dt>
<dd>
<p>Marks a method to be called when an item is skipped due to an exception thrown in the <code>ItemReader</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/annotation/OnSkipInWrite.html">@OnSkipInWrite</a></dt>
<dd>
<p>Marks a method to be called when an item is skipped due to an exception thrown in the <code>ItemWriter</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/annotation/OnWriteError.html">@OnWriteError</a></dt>
<dd>
<p>Marks a method to be called if an exception is thrown by an <code>ItemWriter</code>.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/configuration/annotation/EnableBatchProcessing.html">@EnableBatchProcessing</a></dt>
<dd>
<p>Enable Spring Batch features and provide a base configuration for setting up batch jobs in an <code>@Configuration</code> class, roughly equivalent to using the <code>&lt;batch:*&gt;</code> XML namespace.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/configuration/annotation/JobScope.html">@JobScope</a></dt>
<dd>
<p>Convenience annotation for job-scoped beans that defaults the proxy mode, so that it doesn&#8217;t have to be specified explicitly on every bean definition.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/core/configuration/annotation/StepScope.html">@StepScope</a></dt>
<dd>
<p>Convenience annotation for step-scoped beans that defaults the proxy mode, so that it doesn&#8217;t have to be specified explicitly on every bean definition.</p>
</dd>
<dt class="hdlist1"><a href="http://docs.spring.io/spring-batch/trunk/apidocs/org/springframework/batch/support/annotation/Classifier.html">@Classifier</a></dt>
<dd>
<p>Mark a method as capable of classifying its input to an instance of its output.</p>
</dd>
</dl>
</div>
</div>
<div class="sect2">
<h3 id="_aspect_oriented_programming">Aspect-oriented Programming</h3>
<div class="paragraph">
<p>Spring includes a set of annotations for working with Aspect-oriented Programming (AOP):</p>
</div>
<div class="hdlist">
<table>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/context/annotation/EnableAspectJAutoProxy.html">@EnableAspectJAutoProxy</a>
</td>
<td class="hdlist2">
<p>Enables support for handling components marked with AspectJ&#8217;s @Aspect annotation. Must be used on a class that is also marked with the @Configuration annotation (or another annotation that includes the @Configuration annotation).</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/aop.html#aop-at-aspectj">@Aspect</a>
</td>
<td class="hdlist2">
<p>Indicates that a class is an aspect.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/aop.html#aop-pointcuts">@Pointcut</a>
</td>
<td class="hdlist2">
<p>Defines a join point.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/aop.html#aop-pointcuts-designators">@target</a>
</td>
<td class="hdlist2">
<p>Limits matching to join points. (Not to be confused with @Target for @Configuration classes.)</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/aop.html#aop-pointcuts-designators">@args</a>
</td>
<td class="hdlist2">
<p>Limits matching to join points</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/aop.html#aop-pointcuts-designators">@within</a>
</td>
<td class="hdlist2">
<p>Limits matching to join points within types that have the given annotation.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/aop.html#aop-pointcuts-designators">@annotation</a>
</td>
<td class="hdlist2">
<p>limits matching to join points where the subject of the join point has the given annotation</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/aop.html#aop-ajlib-other">@Transactional</a>
</td>
<td class="hdlist2">
<p>Class annotation that specifies the default transaction semantics for the execution of any public operation in the class.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/aop.html#aop-advice-before">@Before</a>
</td>
<td class="hdlist2">
<p>Declares pointcut advice that should run before methods matched by the pointcut.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/aop.html#aop-advice-after-returning">@AfterReturning</a>
</td>
<td class="hdlist2">
<p>Declares pointcut advice that should run after the methods matched by the pointcut. The methods must return normally. See @AfterThrowing and @After.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/aop.html#aop-schema-advice-after-throwing">@AfterThrowing</a>
</td>
<td class="hdlist2">
<p>Declares pointcut advice that should run after the methods matched by the pointcut have thrown an exception.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/aop.html#aop-schema-advice-after-finally">@After</a>
</td>
<td class="hdlist2">
<p>Declares pointcut advice to run after the methods matched by the pointcut have run, whether they returned normally or threw an exception. Parallel to <code>finally</code> in a try-catch-finally block.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/aop.html#aop-ataspectj-around-advice">@Around</a>
</td>
<td class="hdlist2">
<p>Declares advice that runs around (potentially both before and after) the methods matched by the pointcut. Can also determine if pointcut methods run. Do not use if @Before or @After suffice.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/aop.html#aop-introductions">@DeclareParents</a>
</td>
<td class="hdlist2">
<p>Declares that matching types have a new parent.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/aop.html#aop-atconfigurable">@Configurable</a>
</td>
<td class="hdlist2">
<p>Marks a class as eligible for Spring-driven configuration.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="http://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/context/annotation/aspectj/EnableSpringConfigured.html">@EnableSpringConfigured</a>
</td>
<td class="hdlist2">
<p>Tells the current application context to apply dependency injection to non-managed classes that are instantiated outside of the Spring bean factory.</p>
</td>
</tr>
</table>
</div>
</div>
<div class="sect2">
<h3 id="_integration_testing">Integration Testing</h3>
<div class="paragraph">
<p>Spring includes a set of annotations for working with integration testing:</p>
</div>
<div class="hdlist">
<table>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/integration-testing.html#__bootstrapwith">@BootstrapWith</a>
</td>
<td class="hdlist2">
<p>Specifies a custom <code>TestContextBootstrapper</code> class.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/integration-testing.html#__contextconfiguration">@ContextConfiguration</a>
</td>
<td class="hdlist2">
<p>Defines class-level metadata that determines how to load and configure an <code>ApplicationContext</code> for integration tests.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/integration-testing.html#__webappconfiguration">@WebAppConfiguration</a>
</td>
<td class="hdlist2">
<p>Class-level annotation that is used to declare that the <code>ApplicationContext</code> loaded for an integration test should be a <code>WebApplicationContext</code>.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/integration-testing.html#__contexthierarchy">@ContextHierarchy</a>
</td>
<td class="hdlist2">
<p>Class-level annotation that defines a hierarchy of ApplicationContexts for integration tests.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/integration-testing.html#__activeprofiles">@ActiveProfiles</a>
</td>
<td class="hdlist2">
<p>Class-level annotation that indicates which bean definition profiles should be active.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/integration-testing.html#__testpropertysource">@TestPropertySource</a>
</td>
<td class="hdlist2">
<p>Class-level annotation that configures the locations of properties files and inlined properties to be added to the set of PropertySources in the Environment for an ApplicationContext loaded for an integration test.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/integration-testing.html#__dirtiescontext">@DirtiesContext</a>
</td>
<td class="hdlist2">
<p>Indicates that the underlying Spring ApplicationContext has been modified or corrupted in some manner during the execution of a test and should be closed. When an application context is marked as dirty, it is removed from the testing framework’s cache and closed.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/integration-testing.html#__testexecutionlisteners">@TestExecutionListeners</a>
</td>
<td class="hdlist2">
<p>Defines class-level metadata for configuring the TestExecutionListener implementations that should be registered with the TestContextManager.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/integration-testing.html#__commit">@Commit</a>
</td>
<td class="hdlist2">
<p>Causes a transaction to commit rather than rollback during testing. Use only when you want a test to modify a database. See @Rollback.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/integration-testing.html#__rollback">@Rollback</a>
</td>
<td class="hdlist2">
<p>indicates whether the transaction for a transactional test method should be rolled back after the test method has completed. See @Commit.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/integration-testing.html#__beforetransaction">@BeforeTransaction</a>
</td>
<td class="hdlist2">
<p>Indicates that the annotated void method should be executed before a transaction is started for test methods configured to run within a transaction via Spring’s <code>@Transactional</code> annotation.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/integration-testing.html#__aftertransaction">@AfterTransaction</a>
</td>
<td class="hdlist2">
<p>Indicates that the annotated void method should be executed after a transaction is ended for test methods configured to run within a transaction via Spring’s <code>@Transactional</code> annotation.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/integration-testing.html#__sql">@Sql</a>
</td>
<td class="hdlist2">
<p>Annotates a test class or test method to configure SQL scripts to be executed against a given database during integration tests.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/integration-testing.html#__sqlconfig">@SqlConfig</a>
</td>
<td class="hdlist2">
<p>Defines metadata that is used to determine how to parse and execute SQL scripts configured via the <code>@Sql</code> annotation.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/integration-testing.html#__sqlgroup">@SqlGroup</a>
</td>
<td class="hdlist2">
<p>Container annotation that aggregates several <code>@Sql</code> annotations.</p>
</td>
</tr>
</table>
</div>
</div>
<div class="sect2">
<h3 id="_unit_testing">Unit Testing</h3>
<div class="paragraph">
<p>Spring includes a set of annotations for unit testing:</p>
</div>
<div class="hdlist">
<table>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/integration-testing.html#__ifprofilevalue">@IfProfileValue</a>
</td>
<td class="hdlist2">
<p>Indicates that, if the value returned by the <code>name</code> argument matches the value of the <code>value</code> argument, the annotated test is enabled for a specific testing environment.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/integration-testing.html#__profilevaluesourceconfiguration">@ProfileValueSourceConfiguration</a>
</td>
<td class="hdlist2">
<p>Class-level annotation that specifies what type of ProfileValueSource to use when retrieving profile values configured through the <code>@IfProfileValue</code> annotation.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/integration-testing.html#__timed">@Timed</a>
</td>
<td class="hdlist2">
<p>Indicates that the annotated test method must finish execution in a specified time period (in milliseconds).</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/integration-testing.html#__repeat">@Repeat</a>
</td>
<td class="hdlist2">
<p>Indicates that the annotated test method must be executed a number of times.</p>
</td>
</tr>
</table>
</div>
</div>
<div class="sect2">
<h3 id="_jmx">JMX</h3>
<div class="paragraph">
<p>Spring includes a set of annotations for working with Java Managed Extensions (JMX):</p>
</div>
<div class="hdlist">
<table>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/jmx.html#jmx-interface-metadata-types">@ManagedResource</a>
</td>
<td class="hdlist2">
<p>Marks all instances of a Class as JMX managed resources.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/jmx.html#jmx-interface-metadata-types">@ManagedAttribute</a>
</td>
<td class="hdlist2">
<p>Mark a getter or setter as one half of a JMX attribute.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/jmx.html#jmx-interface-metadata-types">@ManagedOperation</a>
</td>
<td class="hdlist2">
<p>Mark a method as a JMX operation.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/jmx.html#jmx-interface-metadata-types">@ManagedOperationParameters</a>
</td>
<td class="hdlist2">
<p>Define descriptions for operation parameters.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/jmx.html#jmx-interface-metadata-types">@ManagedOperationParameter</a>
</td>
<td class="hdlist2">
<p>Define the descriptions for an operation parameter.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/jmx.html#jmx-context-mbeanexport">@EnableMBeanExport</a>
</td>
<td class="hdlist2">
<p>Class-level application that indicates whether an application is an exporter of managed beans.</p>
</td>
</tr>
</table>
</div>
</div>
<div class="sect2">
<h3 id="_task_execution_and_scheduling">Task Execution and Scheduling</h3>
<div class="paragraph">
<p>Spring includes a set of annotations to support task execution and scheduling:</p>
</div>
<div class="hdlist">
<table>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/scheduling.html#scheduling-annotation-support-scheduled">@Scheduled</a>
</td>
<td class="hdlist2">
<p>Indicates that a method should be called on a scheduled basis.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/scheduling.html#scheduling-annotation-support-async">@Async</a>
</td>
<td class="hdlist2">
<p>Indicates that a method may be called asynchronously.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/scheduling.html#scheduling-enable-annotation-support">@EnableScheduling</a>
</td>
<td class="hdlist2">
<p>Enables support for the <code>@Schedule</code> annotation.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/scheduling.html#scheduling-enable-annotation-support">@EnableAsync</a>
</td>
<td class="hdlist2">
<p>Enables support for the <code>@Async</code> annotation.</p>
</td>
</tr>
</table>
</div>
</div>
<div class="sect2">
<h3 id="_cache_abstraction">Cache Abstraction</h3>
<div class="paragraph">
<p>Spring includes a set of annotations for working with caching:</p>
</div>
<div class="hdlist">
<table>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/cache.html#cache-annotations-cacheable">@Cacheable</a>
</td>
<td class="hdlist2">
<p>Indicates a method whose result is cacheable.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/cache.html#cache-annotations-evict">@CacheEvict</a>
</td>
<td class="hdlist2">
<p>Indicates that a method performs cache eviction (removes items from a cache).</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/cache.html#cache-annotations-put">@CachePut</a>
</td>
<td class="hdlist2">
<p>Indicates a method whose result will always be put in a cache.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/cache.html#cache-annotations-caching">@Caching</a>
</td>
<td class="hdlist2">
<p>Allows multiple nested <code>@Cacheable</code>, <code>@CachePut</code> and <code>@CacheEvict</code> to be used on the same method</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/cache.html#cache-annotations-config">@CacheConfig</a>
</td>
<td class="hdlist2">
<p>Class-level annotation that allows sharing of the cache names, the custom KeyGenerator, the custom CacheManager, and the custom CacheResolver. Placing this annotation on the class does not turn on any caching operation. See @EnableCaching.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/cache.html#cache-annotation-enable">@EnableCaching</a>
</td>
<td class="hdlist2">
<p>Turns on caching in an application. Must go on an <code>@Configuration</code> class.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/cache.html#cache-jsr-107-summary">@CacheResult</a>
</td>
<td class="hdlist2">
<p>Similar to <code>@Cacheable</code> but can cache specific exceptions and force the execution of the method regardless of the content of the cache.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/cache.html#cache-jsr-107-summary">@CacheRemove</a>
</td>
<td class="hdlist2">
<p>Similar to <code>@CacheEvict</code> but can support conditional removal if the method throws an exception.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/cache.html#cache-jsr-107-summary">@CacheRemoveAll</a>
</td>
<td class="hdlist2">
<p>Similar to <code>@CacheEvict(allEntries=true)</code> but can support conditional removal if the method throws an exception.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/cache.html#cache-jsr-107-summary">@CacheDefaults</a>
</td>
<td class="hdlist2">
<p>Similar to <code>@CacheConfig</code>.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/cache.html#cache-jsr-107-summary">@CacheValue</a>
</td>
<td class="hdlist2">
<p>Usable with @CachePut to update the cache before or after method invocation.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/cache.html#cache-jsr-107-summary">@CacheKey</a>
</td>
<td class="hdlist2">
<p>Optional method parameter annotation to indicate which argument(s) should be the key. (The default is to construct the key from all the parameters, unless one or more parameters are marked with <code>@CacheKey</code>.)</p>
</td>
</tr>
</table>
</div>
</div>
<div class="sect2">
<h3 id="_other">Other</h3>
<div class="paragraph">
<p>Spring includes a few other annotations that don&#8217;t fit into the preceding categories:</p>
</div>
<div class="hdlist">
<table>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/web/bind/annotation/ExceptionHandler.html">@ExceptionHandler</a>
</td>
<td class="hdlist2">
<p>Annotation for handling exceptions in specific handler classes and/or handler methods.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/validation.html#format">@NumberFormat</a>
</td>
<td class="hdlist2">
<p>Declares that a field or method parameter should be formatted as a number.</p>
</td>
</tr>
<tr>
<td class="hdlist1">
<a href="https://docs.spring.io/spring/docs/current/spring-framework-reference/html/validation.html#format">@DateTimeFormat</a>
</td>
<td class="hdlist2">
<p>Declares that a field or method parameter should be formatted as a date or time.</p>
</td>
</tr>
</table>
</div>
</div>
</div>
</div>
</div>
<div id="footer">
<div id="footer-text">
Last updated 2017-07-27 14:19:01 CDT
</div>
</div>
</body>
</html>
