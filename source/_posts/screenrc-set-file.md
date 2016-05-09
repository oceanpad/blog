---
title: screenrc set file
date: 2016-05-10 00:12:43
tags:
---
This my screenrc set file:
--------------------------I am commnet line------------------------------

#start from here

# Enable 256 color term
term xterm-256color

# Very nice tabbed colored hardstatus line
hardstatus alwayslastline 
hardstatus string '%{= Kd} %{= Kd}%-w%{= Kr}[%{= KW}%n %t%{= Kr}]%{= Kd}%+w %-= %{KG} %H%{KW}|%{KY}%101`%{KW}|%D %M %d %Y%{= Kc} %C%A%{-}'

#screen start from 1
bind c screen 1
bind ^c screen 1
bind 0 select 10                                                            
screen 1

----------------------------------------------------------------------------------------------------
zhy20090912@gmail.com 2016-04-26 at singapore orchard ikina office
----------------------------------------------------------------------------------------------------

#end at here
