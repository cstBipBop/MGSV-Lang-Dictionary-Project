# MGSV-Lang-Dictionary-Project
A project to resolve MGSV:TPP's and MGO3's entry keys in .lng and .lng2 game files. 

.lng and .lng2 files can be decompiled into .xml files by LangTool.exe (FoxTranslationTools) with the option of diciphering entry keys to
create usable LangIds through entries in lang_dictionary.txt. The project started from Tex's .lua file scrapes and grew from there through
brute-force and dictionary attack methods of generating lang_dictionary entries via lua script.

Individual entry keys can be resolved to multiple LangIds (hash collisions), though the "correct" entries are preferable over the "technically correct" ones.The reasons being that improper entries can mask the actual LangId when found, and that having the proper LangId assists in pattern finding for future entries. These reasons aside, the "technically correct" entries seem to work fine when used in game with TppUiCommand.AnnounceLogViewLangId().

```Example:
  Key: 1876234  Value: "Wolbachia bananas"
  LangId (proper): "cmmn_name_vocalStrain_bana"   Hash: 1876234
  LangId (improper): "aH329rBLo_vQ"               Hash: 1876234
  
  Either would work to in a lua script to use the value associated with the hash.
  e.g.
    function printTest()
      TppUiCommand.AnnounceLogViewLangId("cmmn_name_vocalStrain_bana")
    end
    
    printTest() -- the text 'Wolbachia bananas' appears in the lower left.
```

#### 7,536/17,885 (resolved/total hashes) in 55 .lng and .lng2 files
#### 42.1% of unique hashes resolved
