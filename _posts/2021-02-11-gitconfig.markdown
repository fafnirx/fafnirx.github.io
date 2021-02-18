---
layout: post
title:  "Store your dotfiles in GIT!"
date:   2021-02-11 15:02:46 +0100
categories: git dev 
---
A typical linux/unix/macos/windows (wsl) user account contains a lot of configuration files. Some of those files may simple have the default settings, but if your setup looks anything like mine, apps like git, shell or (neo-)vim  have been highly customized to your needs. At the beginning most of us will probably copy the most important config files from one machine to the other. I know, I did that. In the last couple of years the number of machines I am using on a daily basis increased by a lot.
* Linux desktop home
* Windows WSL deskop home (dual boot, same machine, as above)
* Linux laptop
* Work laptop WSL

And some machines I do use on a irregular basis
* Couple of Raspberry Pis
* Couple of VMs on my desktop machine, mostly linux-based

I can tell from experience how annoying it is, if you are used to have certain key bindings, aliases, functions or even window manager configurations, but you forgot to copy over the latest version of those files from your desktop. Quite a lot of users will stick to the default settings, default shell, default apps for this particular reason.

For me this is a not a solution, because I really love optimizing my workflows and learning about new ways how to do that. Learning also eh especially means, learning from others and the internet provides a lot of sources for so-called `dotfiles`.

Here are a few examples I used in the past for inspiration (copy&paste):
* [Luke Smith](https://github.com/LukeSmithxyz/voidrice)
* [Brodie Roberson](https://github.com/BrodieRobertson/dotfiles)
* [Sebastian Daschner](https://github.com/sdaschner/dotfiles)

Now I established, why we need customized configuration and why we need them to be same on all the machines we use. A file server and some sort of synchronization, because every change to a config file should be available after a local update.

A version control system like git comes to mind plus an accessible repository, e.g on `Github` or `Gitlab`. Ok, this seems to be very straightforward. Let's clone an existing dotfiles repo, e.g [Luke Smith's voidrice dotfiles repo](https://github.com/LukeSmithxyz/voidrice). Let's assume for now that this would be our repo and not somebody elses. To actually use Luke's repo, you could fork it on github and use that for cloning.
{% highlight bash %}
cd $HOME/tmp; git clone https://github.com/LukeSmithxyz/voidrice
{% endhighlight %}

But how do we get those files from `$HOME/tmp/voidrice` to our home directory?
* We could clone into our $HOME directory
* We could write a Makefile or some script to automatically pull the latest changes from the repo and then copy over from repo to . In that case you would have to edit your config files in your repo dir, not in the home dir copy. 



[Miroslav (@eumiro) GPN 18 Talk  One Brain, One Keyboard, One Editor ](https://media.ccc.de/v/gpn18-98-one-brain-one-keyboard-one-editor)


