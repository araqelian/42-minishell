<h1 align="center"> 🗣 Subject &nbsp;&nbsp;&nbsp;&nbsp;minishell </h1>

<br>
<table>
  <tr>
    <td>Program &nbsp;name</td>
    <td>minishell</td>
  </tr>
  <tr>
    <td>Turn &nbsp;in &nbsp;files</td>
    <td>Makefile, &nbsp;*.h, &nbsp;*.c</td>
  </tr>
  <tr>
    <td>Makefile</td>
    <td>NAME, &nbsp;all, &nbsp;clean, &nbsp;fclean, &nbsp;re</td>
  </tr>
  <tr>
    <td>Arguments</td>
    <td></td>
  </tr>
  <tr>
    <td>External &nbsp;functs.</td>
    <td>readline, &nbsp;rl_clear_history,&nbsp; rl_on_new_line,&nbsp; rl_replace_line,&nbsp; rl_redisplay,<br>add_history,&nbsp; printf,&nbsp; malloc,&nbsp; free, &nbsp;write,&nbsp; access, &nbsp;open, &nbsp;read, &nbsp;close,<br>fork,&nbsp; wait, &nbsp;waitpid, &nbsp;wait3, &nbsp;wait4, &nbsp;signal,&nbsp; sigaction,&nbsp; sigemptyset, &nbsp;sigaddset,<br>kill, &nbsp;exit, &nbsp;getcwd, &nbsp;chdir, &nbsp;stat, &nbsp;lstat, &nbsp;fstat, &nbsp;unlink, &nbsp;execve, &nbsp;dup,&nbsp; dup2,&nbsp; pipe,<br>opendir,&nbsp; readdir, &nbsp;closedir, &nbsp;strerror,&nbsp; perror, &nbsp;isatty,&nbsp; ttyname, &nbsp;ttyslot, &nbsp;ioctl, &nbsp;getenv,<br>tcsetattr, &nbsp;tcgetattr, &nbsp;tgetent, &nbsp;tgetflag, &nbsp;tgetnum, &nbsp;tgetstr,&nbsp; tgoto, &nbsp;tputs</td>
  </tr>
  <tr>
    <td>Libft &nbsp;authorized</td>
    <td>Yes</td>
  </tr>
  <tr>
    <td>Description</td>
    <td>Write &nbsp;a &nbsp;shell</td>
  </tr>
</table>

<br>
Your &nbsp;shell &nbsp;should:<br>
<ul>
<li>Display &nbsp;a &nbsp;prompt &nbsp;when &nbsp;waiting &nbsp;for&nbsp; a &nbsp;new &nbsp;command.
<li>Have &nbsp;a&nbsp; working&nbsp; history.
<li>Search&nbsp; and &nbsp;launch &nbsp;the &nbsp;right&nbsp; executable&nbsp; (based &nbsp;on&nbsp; the &nbsp;PATH &nbsp;variable&nbsp; or &nbsp;using &nbsp;a&nbsp;
relative&nbsp; or &nbsp;an &nbsp;absolute &nbsp;path).
<li>Not&nbsp; use&nbsp; more&nbsp; than&nbsp; one &nbsp;global &nbsp;variable.&nbsp; Think &nbsp;about&nbsp; it. &nbsp;You will&nbsp; have &nbsp;to&nbsp; explain&nbsp;
its &nbsp;purpose.
<li>Not &nbsp;interpret &nbsp;unclosed &nbsp;quotes&nbsp; or &nbsp;special &nbsp;characters&nbsp; which&nbsp; are&nbsp; not&nbsp; required&nbsp; by &nbsp;the&nbsp;
subject &nbsp;such &nbsp;as&nbsp; \ &nbsp;(backslash)&nbsp; or &nbsp;;&nbsp; (semicolon).
<li>Handle&nbsp; ’ &nbsp;(single&nbsp; quote) &nbsp;which &nbsp;should &nbsp;prevent&nbsp; the&nbsp; shell &nbsp;from &nbsp;interpreting &nbsp;the &nbsp;metacharacters &nbsp;in &nbsp;the &nbsp;quoted &nbsp;sequence.
<li>Handle &nbsp;" &nbsp;(double&nbsp; quote) &nbsp;which &nbsp;should &nbsp;prevent&nbsp; the &nbsp;shell &nbsp;from &nbsp;interpreting &nbsp;the &nbsp;metacharacters &nbsp;in &nbsp;the &nbsp;quoted &nbsp;sequence &nbsp;except &nbsp;for&nbsp; $ &nbsp;(dollar &nbsp;sign).
<li>Implement &nbsp;redirections:
<ul>
<li>< &nbsp;should &nbsp;redirect&nbsp; input.
<li>>&nbsp; should &nbsp;redirect&nbsp; output.
<li><<&nbsp; should &nbsp;be &nbsp;given&nbsp; a &nbsp;delimiter, &nbsp;then &nbsp;read &nbsp;the &nbsp;input &nbsp;until &nbsp;a &nbsp;line &nbsp;containing&nbsp; the&nbsp;
delimiter &nbsp;is&nbsp; seen.&nbsp; However, &nbsp;it &nbsp;doesn’t&nbsp; have &nbsp;to &nbsp;update &nbsp;the &nbsp;history!
<li>>>&nbsp; should&nbsp; redirect&nbsp; output&nbsp; in&nbsp; append &nbsp;mode.
</ul>
<li>Implement &nbsp;pipes&nbsp; (|&nbsp; character).&nbsp; The&nbsp; output&nbsp; of &nbsp;each &nbsp;command &nbsp;in &nbsp;the &nbsp;pipeline&nbsp; is&nbsp;
connected&nbsp; to&nbsp; the&nbsp; input&nbsp; of&nbsp; the&nbsp; next&nbsp; command &nbsp;via &nbsp;a &nbsp;pipe.
<li>Handle&nbsp; environment &nbsp;variables &nbsp;($&nbsp; followed &nbsp;by &nbsp;a &nbsp;sequence &nbsp;of &nbsp;characters)&nbsp; which&nbsp;
should &nbsp;expand&nbsp; to&nbsp; their&nbsp; values.
<li>Handle &nbsp;$?&nbsp; which&nbsp; should&nbsp; expand&nbsp; to&nbsp; the&nbsp; exit&nbsp; status&nbsp; of&nbsp; the&nbsp; most&nbsp; recently&nbsp; executed&nbsp;
foreground &nbsp;pipeline.
<li>Handle &nbsp;ctrl-C, &nbsp;ctrl-D&nbsp; and &nbsp;ctrl-\ &nbsp;which &nbsp;should &nbsp;behave &nbsp;like &nbsp;in &nbsp;bash.
<li>In &nbsp;interactive&nbsp; mode:
<ul>
<li><b>ctrl-C</b>&nbsp; displays&nbsp; a &nbsp;new&nbsp; prompt&nbsp; on &nbsp;a &nbsp;new&nbsp; line.
<li><b>ctrl-D</b> &nbsp;exits&nbsp; the&nbsp; shell.
<li><b>ctrl-\</b> &nbsp;does&nbsp; nothing.
</ul>
<li>Your&nbsp; shell &nbsp;must&nbsp; implement&nbsp; the &nbsp;following &nbsp;builtins:
<ul>
<li><b>echo</b>&nbsp; with &nbsp;option&nbsp; -n
<li><b>cd</b>&nbsp; with &nbsp;only &nbsp;a&nbsp; relative&nbsp; or&nbsp; absolute&nbsp; path
<li><b>pwd</b> &nbsp;with&nbsp; no&nbsp; options
<li><b>export</b> &nbsp;with&nbsp; no&nbsp; options
<li><b>unset</b>&nbsp; with &nbsp;no&nbsp; options
<li><b>env</b>&nbsp; with&nbsp; no &nbsp;options&nbsp; or&nbsp; arguments
<li><b>exit</b> &nbsp;with&nbsp; no &nbsp;options
</ul>
</ul>
<br>
The&nbsp; readline()&nbsp; function &nbsp;can&nbsp; cause&nbsp; memory&nbsp; leaks.&nbsp; You&nbsp; don’t &nbsp;have&nbsp; to&nbsp; fix&nbsp; them.&nbsp; But&nbsp;
that &nbsp;doesn’t &nbsp;mean &nbsp;your&nbsp; own&nbsp; code, &nbsp;yes &nbsp;the &nbsp;code &nbsp;you&nbsp; wrote, &nbsp;can &nbsp;have &nbsp;memory&nbsp;
leaks.

<br><br>

> [!NOTE]  
> Because of 42 School norm requirements:
> * Each function can't have more than 25 lines of code.
> * All variables are declared and aligned at the top of each function.
> * Project should be created just with allowed functions otherwise it's cheating.
