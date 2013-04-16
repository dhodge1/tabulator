#!/bin/sh

cat << EOFILE
<HTML>
<HEAD><Title>TABULATOR</Title></HEAD>
<BODY>
<table border="1">
EOFILE

sed -r 's:&:\&amp;:g' $1 | sed -r 's:<:\&lt;:g' | sed -r 's:>:\&gt;:g' | sed -r 's:^\": :' | sed -r 's:\"$: :' | sed -r 's:\"\,\":</TD><TD>:g' | sed -r 's:([a-z])\,([A-Z]):\1</TD><TD>\2:g' | sed -r 's:([P])\,([P]):\1</TD><TD>\2:g' | s$

cat << EOFILE
</table>
</BODY>
</HTML>
EOFILE
