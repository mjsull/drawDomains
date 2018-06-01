# drawDomains.py

Script to draw domains produced by CD-Search tool (https://www.ncbi.nlm.nih.gov/Structure/bwrpsb/bwrpsb.cgi)

Written in python 2.7, requires only the standard library

# usage

    python drawDomains.py <order_list> <fasta_file> <hitdata.txt> <out.svg>


Where:
**order_list** is is the order you want the proteins to be drawn in (from top to bottom).

**fasta_file** is the protein file submitted to CD-Search

**hitdata.txt** is the results from CD-search (options: Domain hits, concise)

**out.svg** is where to write the svg

 
**IMPORTANT**
To get this to work correctly the names in **order_list** must be contained within the headers of the FASTA file. If the name is contained in more than one entry, they will be drawn adjacent to one another.

e.g.
given the order_list

    ctg1
    ctg2
    ctg3

and a fasta file with the following headers

    >ctg1.pls
    >ctg2.pls_1
    >ctg2.pls_2
    >ctg3.pls

drawDomains.py will draw three rows, with ctg2.pls_1 and ctg2.pls_2 adjacent on the second row.
