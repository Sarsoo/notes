---
date: 2026-03-12
title: Vim
---
0 - jump to the start of the line
$ - jump to the end of the line

gg - go to the first line of the document
G - go to the last line of the document

I - insert at the beginning of the line
A - insert (append) at the end of the line

o - append (open) a new line below the current line
O - append (open) a new line above the current line
ea - insert (append) at the end of the word

ciw - change (replace) entire word
diw - delete (cut) word under the cursor
D - delete (cut) to the end of the line

U - restore (undo) last changed line
Ctrl + r - redo

V - start linewise visual mode

- aw - mark a word
- ab - a block with ()
- aB - a block with {}
- at - a block with <> tags
- ib - inner block with ()
- iB - inner block with {}
- it - inner block with <> tags

- > - shift text right
- < - shift text left
- y - yank (copy) marked text
- d - delete marked text
- ~ - switch case
- u - change marked text to lowercase
- U - change marked text to uppercase

- >> - indent (move right) line one shiftwidth
- << - de-indent (move left) line one shiftwidth
- >% - indent a block with () or {} (cursor on brace)
- <% - de-indent a block with () or {} (cursor on brace)