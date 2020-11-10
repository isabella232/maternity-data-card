# Generating html documentation 
Prerequisites
> $ sudo apt-get install wget saxon
> $ brew install wget saxon

Assuming you run art-decor on localhost:8085
> $ wget "http://localhost:8085/decor/services/RetrieveProject?prefix=dk-mdc-&version=&language=en-US&mode=compiled&force=on&ignoreFilter=on&download=true&format=xml" -O dk-mdc-decor.xm
> $ saxon -xsl:http://art-decor.org/ADAR/rv/DECOR2schematron.xsl -o:dk-mdc-decor.html -s:dk-mdc-decor.xml
