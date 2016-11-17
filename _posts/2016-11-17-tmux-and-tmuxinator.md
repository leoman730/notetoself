---
layout: post
title: "Tmux and Tmuxinator"
description: "Some helpful command for tmux and tmuxinator"
category: 
tags: [devtool]
---
{% include JB/setup %}


### Sessions

list all sessions  
``tmux ls``	

start a new session  
``tmux new -s [session-name]``

attach to a session   
``tmux attach -t [session-name]``

kill a session  
``tmux kill-session -t [session-name]``  
or  
``tmux kill-server``



### Windows
create a new session with window name  
``tmux new -s [session-name] -n [window-name]``

create a new window in the current session  
``[prefix-key] + c``

rename current window  
``[prefix-key] + ,``

moving through windows  

```
[prefix-key] + n/p - next or previous
[prefix-key] + [window index number]
[prefix-key] + w - show a list of windows 

```

### Panes
divide window vertically   
``[prefix-key] + %``

divide window horizontally   
``[prefix-key] + "``

use predefined arrangement  
``[prefix-key] + [spacebar]``

close current pane  
``[prefix-key] + x``


### Configuration
Create config file:  
``touch ~/.tmux.conf``

Sample of .tmux.config

```
// rebind prefix-key
set -g prefix C-a
unbind C-b
bind C-a send-prefix

// set delay for prefix-key and command
set -s escape-time 1

// change window and pane base index to 1. default: 0
set -g base-index 1
set -g pane-base-index 1

// create new key binding for reload config file
bind r source-file ~/.tmux.conf\; display "reload config file"

// more key binding for window spliting
bind v split-window -h 
bind h split-window -v

// modify status bar info
set -g status-left "Session: #S" 
set -g status-right "#H #[fg-white,bg-default]%a%l:%M:%S %p, %d %b#[default] "
```

##Tmuxinator  
Install  
``gem install tmuxinator``

create a new project  
``tmuxinator new [project-name]``

start a project  
``tmuxinator start [project] ``   






## References:

[Build podcast](https://build-podcast.com/tmux/)  
[Tmuxinator](https://github.com/tmuxinator/tmuxinator)
