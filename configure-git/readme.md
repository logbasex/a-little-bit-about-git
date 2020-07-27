config git log:
1. open ~/.gitconfig
2. add: (https://stackoverflow.com/questions/1441010/the-shortest-possible-output-from-git-log-containing-author-and-date)
	[log]
	  date = relative
	[format]
 	  pretty = format:%h %Cblue%ad%Creset %ae %Cgreen%s%Creset
3. git log -g

Explain:
%ad: author date
%Cred: switch color to red
%Creset: reset color

-- MORE: https://mirrors.edge.kernel.org/pub/software/scm/git/docs/git-log.html

