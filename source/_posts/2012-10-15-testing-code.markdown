---
layout: post
title: "testing code"
date: 2012-10-15 19:08
comments: true
categories:
- code
- source
- test
---

# some code here

Bash.

```
$ sudo make love
```


Some python code from Nastya

```python Unknown code from Nastya https://github.com/anastasiagulenko/MDanalysis/blob/master/totalrdf_from_RDFDAT.py Source on github

def coeff(n, m):
    """Defines the coefficient for partial pdf for atom pair.

    n, m - indexes of the atoms.
    """
    c = 0
    if n != m:
        c = 2
    else:
        c = 1
    return c

rdfdat = open('RDFDAT', 'r')
# try to know how many lines of data I have for each pair in general case
def countr(i, j):
    """Counts the lines of the useful data.

    i, j = 0, len(atomtyp) - indexes of atoms.
    """
    while rdfdat:
        lname = rdfdat.readline()
        if len(lname) == 0:
            break
        data = lname.split()
        if data == [atomtyp[i], atomtyp[j]]:
            global nstr
            while rdfdat:
                lname = rdfdat.readline()
                data = lname.split()
                m = p.match(lname)
                if m:
                    break
                nstr += 1
    return nstr

countr(0, 0)
```


Now some gists

{% gist 3893054 %}
