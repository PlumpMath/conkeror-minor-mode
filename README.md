conkeror-minor-mode
===================

Mode for editing conkeror javascript files.

Currently, this only defines a function (for sending current
javascript statement to be evaluated by conkeror) and binds it to a
key. This function is `eval-in-conkeror` bound to **C-c C-c**.

Installation:
=============

If you install manually, require it like this,

    (require 'conkeror-minor-mode)
    
then follow activation instructions below.

If you install from melpa just follow the activation instructions.

Activation
==========

It is up to you to define when `conkeror-minor-mode` should be
activated. If you want it on every javascript file, just do

    (add-hook 'js-mode-hook 'conkeror-minor-mode)

If you want it only on some files, do something like:

    (add-hook 'js-mode-hook (lambda ()
                              (when (string= "conkerorrc" (buffer-file-name))
                                (conkeror-minor-mode 1))))

