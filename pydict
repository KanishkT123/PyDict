#!/usr/bin/env python
#
# Written by Kanishk and Jon (2016)
# Contact Info: jabrahams@hmc.edu
import sys
import ast

def getd():
    """
    Open and read the dictionary
    """
    try:
        dics = open("dictionary", "r+")
    except:
        dics = open("dictionary", "w+")
    dicstring = dics.read()
    dics.close()
    try:
        data = ast.literal_eval(dicstring)
        return data
    except:
        return {}

def add(word, defin):
    """
    Add a word and its definition to the dictionary
    """
    d = getd()
    d[str(word)] = str(defin)
    writed(d)
    return d

def look(words):
    """
    Look up a word in the dictionary
    """
    words = str(words)
    dic = getd()
    print words + " :"
    if words in dic:
        print dic[words]
    else:
        print "Words not found, maybe consider adding it in?"

def writed(stringd):
    """
    Write the dictionary to a file
    """
    dics = open("dictionary", "w+")
    dics.write(str(stringd))
    dics.close()

if __name__ == '__main__':
    function = getattr(sys.modules[__name__], sys.argv[1])
    word = sys.argv[2]
    try:
        defin = sys.argv[3]
        function(word, defin)
    except:
        function(word)
