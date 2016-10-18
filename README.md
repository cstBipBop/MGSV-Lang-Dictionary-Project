# MGSV-Lang-Dictionary-Project
A project to resolve MGSV:TPP's and MGO3's entry keys in .lng and .lng2 game files. 

.lng and .lng2 files can be decompiled into .xml files by LangTool.exe (FoxTranslationTools) with the option of diciphering entry keys to
create usable LangIds through entries in lang_dictionary.txt. The project started from Tex's .lua file scrapes and grew from there through
brute-force and dictionary attack methods of generating lang_dictionary entries via lua script.

Entry keys can be resolved to multiple LangIds, though the "correct" entries are preferable over the "technically correct" ones.
The reasons being that "technically correct" entries can mask the actual LangId when found, and that having the proper LangId assists in
pattern finding for future entries. These reasons aside, the "technically correct" entries seem to work fine when used in game with
TppUiCommand.AnnounceLogViewLangId().

#### 7,398/17,885 (resolved/total hashes) in 55 .lng and .lng2 files
#### 41.4% of unique hashes resolved
