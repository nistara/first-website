---
layout: post
title: "Preview markdown documents as you work in emacs"
date: "2016-07-21"
tags:
 - emacs
 - markdown
published: true
comments: true
---

**App used:** [Marked 2](http://marked2app.com/)

**Reference:** [superuse.com](http://superuser.com/questions/569517/is-there-an-extension-that-previews-markdown-instantly)

Code to include in `.emacs` file:

```lisp
;; Getting emacs to use the 'Marked' app
(defun markdown-preview-file ()
  "run Marked on the current file and revert the buffer"
  (interactive)
  (shell-command
   (format "open -a /Applications/Marked\\ 2.app %s"
       (shell-quote-argument (buffer-file-name))))
)
```


Create a key-binding to open emacs markdown file in Marked:

```lisp
(eval-after-load 'markdown-mode
  '(define-key markdown-mode-map (kbd "C-x p") 'markdown-preview-file))
```

What's cool is that as you write and save changes, they're immediately updated in the Marked preview, with a dash at the most recent change

If you want to use different templates, you can get them at [Marked 2 templates](https://github.com/ttscoff/MarkedCustomStyles) by [Brett Terpstra](https://github.com/ttscoff)


