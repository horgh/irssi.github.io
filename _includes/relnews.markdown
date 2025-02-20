## 1.3-head
{:#v1-3-head }

<span class="glyphicon glyphicon-download-alt"></span> `git clone https://github.com/irssi/irssi`

[Commit log](https://github.com/irssi/irssi/commits)

---

## 1.2.2
{:#v1-2-2 }

The Irssi team released this <abbr class="timeago" title="2019-08-29">2019-08-29</abbr> 

{% include relnews_artef_block.markdown ver="1.2.2" %}

### Fixes
{:#v1-2-2-fixes }

- Fix a use after free issue when receiving IRCv3 CAP information from the server ([GL#34](https://gitlab.com/irssi/irssi/issues/34))
- Fix a crash during startup when windows weren't fully initialised yet ([#1114](https://github.com/irssi/irssi/issues/1114 "fix crash on startup when resizing before active_win"), [bdo#935813](https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=935813))

---

## 1.2.1
{:#v1-2-1 }

The Irssi team released this <abbr class="timeago" title="2019-06-29">2019-06-29</abbr> 

{% include relnews_artef_block.markdown ver="1.2.1" %}

Contains all changes from 1.1.3

### Fixes
{:#v1-2-1-fixes }

- Fix a test on big endian machines ([#1014](https://github.com/irssi/irssi/issues/1014 "fix test on Big Endian 64bit, due to pointer size mismatch"))
- Fix the compile time conditionality of wcwidth implementation ([#1019](https://github.com/irssi/irssi/issues/1019 "make utf8proc configurable"), gentoo#677804, [#720](https://github.com/irssi/irssi/issues/720 "mk_wcwidth will return outdated widths when glibc 2.26 (unicode 9.0) is out"))
- Fix /save no longer working on old Solaris (pre POSIX.1-2008) ([#1042](https://github.com/irssi/irssi/issues/1042 "/SAVE fails in Solaris 10 ''Invalid argument''"), [#1043](https://github.com/irssi/irssi/issues/1043 "fix realpath on old solaris"))
- Fix regression of [#764](https://github.com/irssi/irssi/issues/764 "Add color support for input bar") where display of 8-bit (legacy encoding) in the input prompt was broken ([#1018](https://github.com/irssi/irssi/issues/1018 "Input line is echoing utf8 chars on non-utf8 terminal"), [#1057](https://github.com/irssi/irssi/issues/1057 "restore 8bit support in input entry")). Initial patch by Артём Курашов

---

## 1.1.3
{:#v1-1-3 }

The Irssi team released this <abbr class="timeago" title="2019-06-29">2019-06-29</abbr> 

{% include relnews_artef_block.markdown ver="1.1.3" %}

Contains all changes from 1.0.8

### Fixes
{:#v1-1-3-fixes }

- Fix regression of [#779](https://github.com/irssi/irssi/issues/779 "Allow selection of what kind of activity targets to ignore v2") where autolog_ignore_targets would not matching itemless windows anymore ([#1012](https://github.com/irssi/irssi/issues/1012 "autolog_ignore_targets cannot ignore non-windowed targets"), [#1013](https://github.com/irssi/irssi/issues/1013 "do not stop autolog_ignore_targets from matching itemless targets"))

---

## 1.0.8
{:#v1-0-8 }

The Irssi team released this <abbr class="timeago" title="2019-06-29">2019-06-29</abbr> 

{% include relnews_artef_block.markdown ver="1.0.8" %}

### Fixes
{:#v1-0-8-fixes }

- Fix a use after free issue when sending the SASL login on (automatic and manual) reconnects ([#1055](https://github.com/irssi/irssi/issues/1055 "memory corruption sasl reconnect? "), [#1058](https://github.com/irssi/irssi/issues/1058 "copy sasl username and password values")). Reported by ilbelkyr

---

## 1.2.0
{:#v1-2-0 }

The Irssi team released this <abbr class="timeago" title="2019-02-11">2019-02-11</abbr> 

{% include relnews_artef_block.markdown ver="1.2.0" %}

Contains all changes from 1.1.2

### Changes
{:#v1-2-0-changes }

- Improved the /STATUSBAR commands ([#858](https://github.com/irssi/irssi/issues/858 "change the statusbar commands so that no accidential status bars are created"))
- /SET no longer shows `=` between setting and value ([#886](https://github.com/irssi/irssi/issues/886 "remove = from format because people get confused by it"))
- /CUBES removed from default config (available as script) ([#956](https://github.com/irssi/irssi/issues/956 "Remove cubes from irssi.conf"))
- /1 /2 /3 ... removed from default config (available as new setting window_number_commands) ([#958](https://github.com/irssi/irssi/issues/958 "Make /1/2/3/... a setting"))
- Always redraw the screen on resize. By David Phillips ([#896](https://github.com/irssi/irssi/issues/896 "Don't ignore SIGWINCH when window size is unchanged"))
- Private notices intended for channels are now displayed on the channel (new setting notice_channel_context) ([#959](https://github.com/irssi/irssi/issues/959 "Route notices intended for channels into the channel"))

### Additions
{:#v1-2-0-additions }

- Imported the "Off-the-record" module into Irssi tree ([#854](https://github.com/irssi/irssi/issues/854 "OTR support, take 2"), [#589](https://github.com/irssi/irssi/issues/589 "''Native'' OTR Support"), [#196](https://github.com/irssi/irssi/issues/196 "Merge irssi-otr into the tree"), [#881](https://github.com/irssi/irssi/issues/881 "New release including OTR "))
- Initial support for sideways split windows ([#697](https://github.com/irssi/irssi/issues/697 "sideways split support for Irssi"), [#431](https://github.com/irssi/irssi/issues/431 "[WIP] Lemons code for horizontal splits [Do not merge]"), [#224](https://github.com/irssi/irssi/issues/224 "Vertical split windows / tmux-like ''panes''"), [#807](https://github.com/irssi/irssi/issues/807 "fix format_real_length expected test result"), [FS#310](https://github.com/irssi-import/bugs.irssi.org/issues/310 "vertical splits"), [#947](https://github.com/irssi/irssi/issues/947 "Fix broken display after resizing many windows very small"), [#955](https://github.com/irssi/irssi/issues/955 "fix and document window width on screen width dependency"), [#989](https://github.com/irssi/irssi/issues/989 "update sidewayssplit syntax"))
- Change the implementation of `wcwidth`. This is used to calculate the width of emojis on your terminal screen ([#917](https://github.com/irssi/irssi/issues/917 "Add a wrapper of wcwidth() that picks the best implementation"), [#720](https://github.com/irssi/irssi/issues/720 "mk_wcwidth will return outdated widths when glibc 2.26 (unicode 9.0) is out"))
- Make the wcwidth functions available from Perl ([#973](https://github.com/irssi/irssi/issues/973 "expose wcwidth and related to perl")):
  
  
      string_width(str)
      string_chars_for_width(str, width)
      wcwidth(char)
- Added completion_keep_word setting ([#979](https://github.com/irssi/irssi/issues/979 "add keep_word setting to completion"))
- Allow activity_hide_targets to hide activity in itemless windows ([#967](https://github.com/irssi/irssi/issues/967 "allow activity_hide_targets to hide activity in itemless windows"), [#997](https://github.com/irssi/irssi/issues/997 "some crash"), [#1001](https://github.com/irssi/irssi/issues/1001 "add missing NULL check"), [#1003](https://github.com/irssi/irssi/issues/1003 "correct fix for #997"))
- Added activity_hide_visible setting ([#990](https://github.com/irssi/irssi/issues/990 "add activity_hide_visible setting"))
- Allow hiding of lines through the /IGNORE system ([#901](https://github.com/irssi/irssi/issues/901 "core/ignore: fix #900"), [#900](https://github.com/irssi/irssi/issues/900 "NO_ACT ignores not working"), [#892](https://github.com/irssi/irssi/issues/892 "core/ignore: fix ignore_match_level handling of flag levels"), [#890](https://github.com/irssi/irssi/issues/890 "Lines matching NO_ACT ignores are hidden by /window hidelevel HIDDEN"), [#884](https://github.com/irssi/irssi/issues/884 "Added HIDDEN level to ignores"), [#937](https://github.com/irssi/irssi/issues/937 "correctly separate ignore flags (no_act, hidden) from level"))
- Add window_default_hidelevel setting. By Doug Freed ([#941](https://github.com/irssi/irssi/issues/941 "Add window_default_hidelevel setting"))
- Add activity_hide_window_hidelevel setting, defaulting to ON ([#938](https://github.com/irssi/irssi/issues/938 "Don't trigger activity on hidden lines by default"))
- Add autolog_only_saved_channels setting, to autolog only channels that are in the config ([#968](https://github.com/irssi/irssi/issues/968 "Only log saved channels"))
- Add format support for the input line. By Ben Paxton, originally by Jonas Hurrelmann ([#764](https://github.com/irssi/irssi/issues/764 "Add color support for input bar"), [FS#621](https://github.com/irssi-import/bugs.irssi.org/issues/621 "[PATCH] Color support for ''gui_entry'' to allow better spellcheckers."), [#1004](https://github.com/irssi/irssi/issues/1004 "fix gui_input_get_extent"))
  
  
      use Irssi::TextUI;
      gui_input_set_extent(pos, text)
      gui_input_set_extents(pos, len, left, right)
      gui_input_clear_extents(pos, len)
      gui_input_get_extent(pos)
      gui_input_get_text_and_extents()
      gui_input_set_text_and_extents(...)
- Parsing of IRCv3 CAP 3.2 ([#775](https://github.com/irssi/irssi/issues/775 "CAP 3.2 support"), [#869](https://github.com/irssi/irssi/issues/869 "signals.txt: add missing 'server cap new│delete' signals"))
- Show CAP-related events in the user interface ([#918](https://github.com/irssi/irssi/issues/918 "irc-cap: Don't show warning on CAP LIST response"), [#916](https://github.com/irssi/irssi/issues/916 "/quote cap list says ''Unhandled CAP subcommand'' but it is handled now"), [#870](https://github.com/irssi/irssi/issues/870 "Add fe-cap to show messages for CAP-related events in the UI "), [#704](https://github.com/irssi/irssi/issues/704 "output of any CAP command not shown"))
- Continue using separators when addressing multiple nicks with tab completion. By Manish Goregaokar ([#822](https://github.com/irssi/irssi/issues/822 "Insert colons after completing nicks preceded by a list of other autocompleted nicks"))
- Bind Shift-tab by default. By Niklas Luokkala ([#830](https://github.com/irssi/irssi/issues/830 "Add Shift-Tab completion to gui-readline"), [#829](https://github.com/irssi/irssi/issues/829 "Add <Shift><Tab> completion"))
- Fuzzing more things ([#913](https://github.com/irssi/irssi/issues/913 "Add server-fuzz to fe-fuzz"), [#780](https://github.com/irssi/irssi/issues/780 "Add event_get_params to fe-fuzz"), [#813](https://github.com/irssi/irssi/issues/813 "Add theme_load to fe-fuzz"))

### Fixes
{:#v1-2-0-fixes }

- Disconnect SASL properly in case the SASL module got unloaded from server ([#931](https://github.com/irssi/irssi/issues/931 "Disconnect SASL properly in case the sasl module got unloaded from server"), [#629](https://github.com/irssi/irssi/issues/629 "sasl_disconnect_on_failure not effective when server ignores CAP"), [#618](https://github.com/irssi/irssi/issues/618 "Print a warning if the server doesn't support SASL at all."), [#616](https://github.com/irssi/irssi/issues/616 "Display reason why when quitting because of sasl_disconnect_on_failure"))
- Fix backward completion jumping to the first instead of last word ([#979](https://github.com/irssi/irssi/issues/979 "add keep_word setting to completion"))
- Improve empty topic handling ([#961](https://github.com/irssi/irssi/issues/961 "Show the proper TXT when topic was unset"), [#905](https://github.com/irssi/irssi/issues/905 "Add tests for topic events"), [#911](https://github.com/irssi/irssi/issues/911 "Revert ''Flag topic as unset if it is zero length''"), [#897](https://github.com/irssi/irssi/issues/897 "Flag topic as unset if it is zero length"), [#888](https://github.com/irssi/irssi/issues/888 "/topic after topic is unset still shows topic as set"))
- Prevent config truncation when no space left. By dequis and Lukas Waymann ([#922](https://github.com/irssi/irssi/issues/922 "Fix /save not working if the config didn't previously exist"), [#925](https://github.com/irssi/irssi/issues/925 "Improve error message when failing to create the config dir"), [#910](https://github.com/irssi/irssi/issues/910 "ERROR: Couldn't create $HOME/.irssi directory"), [#909](https://github.com/irssi/irssi/issues/909 "Fix `/save` replacing symlinks with regular files"), [#906](https://github.com/irssi/irssi/issues/906 "/save replaces symlinks with regular files"), [#871](https://github.com/irssi/irssi/issues/871 "Make config_write more atomic to prevent truncation when out of space"), [#817](https://github.com/irssi/irssi/issues/817 "Disk full / write error on exit destroys config file? :-\"))
- Also time-out servers in lookup phase ([#866](https://github.com/irssi/irssi/issues/866 "reconnect lookup_servers also"), [#130](https://github.com/irssi/irssi/issues/130 "SSL connection does not timeout"))
- Fix build with LibreSSL 2.7. By Dorian Harmans ([#865](https://github.com/irssi/irssi/issues/865 "fix build with LibreSSL 2.7.0/2.7.1"))
- Fix a crash when appending to a textbuffer without line. Reported by Jari Matilainen ([#862](https://github.com/irssi/irssi/issues/862 "fix a crash when trying to append to a NULL line"))
- Fix segfault on sending large messages ([#803](https://github.com/irssi/irssi/issues/803 "Postpone server cleanup until after unref"), [#796](https://github.com/irssi/irssi/issues/796 "Segfault on sending large message"), [#802](https://github.com/irssi/irssi/issues/802 "Test for segfault on disconnect during signal processing"))
- Fix segfault on invalid statusbar config ([#993](https://github.com/irssi/irssi/issues/993 "segfault / null pointer dereference in statusbar_read()"), [#994](https://github.com/irssi/irssi/issues/994 "add more config checks and assertions in statusbar code"))
- Fix random memory writes on restoring queries of foreign protocols ([#999](https://github.com/irssi/irssi/issues/999 "do not touch uninitialised protocols on item restore"), [#1000](https://github.com/irssi/irssi/issues/1000 "Store window bounds type"))
- Make default keybinds deletable ([#859](https://github.com/irssi/irssi/issues/859 "make default keybinds deletable"), [#507](https://github.com/irssi/irssi/issues/507 "irssi doesn't remember /bind -delete on default build-in keybindings"))
- Fix freeze when resizing Irssi very small ([#946](https://github.com/irssi/irssi/issues/946 "fix irssi being stuck when resized very small"))
- Compare channels case-insensitively, avoiding confusions with the config file ([#857](https://github.com/irssi/irssi/issues/857 "Compare channels/networks fields case-insensitively"), [#856](https://github.com/irssi/irssi/issues/856 "/channel remove and case mismatch in buggy config"))
- Fix DCC GET on Android. By Martin Staron ([#844](https://github.com/irssi/irssi/issues/844 "dcc get shouldn't fail when file attrs can't be changed"))
- Improve rawlog performance ([#957](https://github.com/irssi/irssi/issues/957 "Improve rawlog performance"))
- Fix nick escaping erroneously escaping quotes ([#978](https://github.com/irssi/irssi/issues/978 "Fix inconsistent escaping from expand_escapes"), [#974](https://github.com/irssi/irssi/issues/974 "Inconsistent escaping/unescaping of quotes"), [#709](https://github.com/irssi/irssi/issues/709 "Escape nicks during nick completion when expand_escapes is enabled"))
- Protect against theme recursion, improve padding performance, limit alignment padding. Credit to Oss-Fuzz ([#835](https://github.com/irssi/irssi/issues/835 "protect theme recursion"), [#851](https://github.com/irssi/irssi/issues/851 "unblock theme elements when processing finished"), [#850](https://github.com/irssi/irssi/issues/850 "theme colours broken"), [#846](https://github.com/irssi/irssi/issues/846 "improve padding performance"), [#848](https://github.com/irssi/irssi/issues/848 "limit alignment padding to a screenful"))
- Fix recursive loop in replaces ([#833](https://github.com/irssi/irssi/issues/833 "we probably should not try to replace replaces"), [GL#23](https://gitlab.com/irssi/irssi/issues/23))
- Fix headers for compilation of C modules ([#939](https://github.com/irssi/irssi/issues/939 "some header fixes for C modules"))
- Documentation. By Zero King ([#814](https://github.com/irssi/irssi/issues/814 "Update Irssi website URLs")). ([#852](https://github.com/irssi/irssi/issues/852 "Document second parameter (seek position) of /cat command"))
- Sync NEWS, docs, scripts ([#849](https://github.com/irssi/irssi/issues/849 "add additional notes to NEWS"), [#855](https://github.com/irssi/irssi/issues/855 "run syncdocs.sh and syncscripts.sh"))
- Build system ([#868](https://github.com/irssi/irssi/issues/868 "Add libgcrypt.m4 so autogen doesn't require libgcrypt-dev"), [#867](https://github.com/irssi/irssi/issues/867 "irssi autogen now depends on libgcrypt-dev"), [#985](https://github.com/irssi/irssi/issues/985 "automake warns that subdir-objects will be enabled in 2.0"), [#988](https://github.com/irssi/irssi/issues/988 "show output of git describe as PACKAGE_VERSION"))
- Fix build on IBM i and AIX. By Calvin Buckley ([#975](https://github.com/irssi/irssi/issues/975 "Fix irssi build on IBM i and AIX"))
- Misc fixes ([#840](https://github.com/irssi/irssi/issues/840 "ensure cap_supported is existent yet"), [#839](https://github.com/irssi/irssi/issues/839 "some crash "), [#843](https://github.com/irssi/irssi/issues/843 "restore compat with glib <2.40"), [#953](https://github.com/irssi/irssi/issues/953 "Use ##__VA_ARGS__ extension to allow for argument-less ..."), [#962](https://github.com/irssi/irssi/issues/962 "Fix some indentation and add some comments")). Tests ([#806](https://github.com/irssi/irssi/issues/806 "only use nonfatal assertions for GLib that actually supports it"), [#875](https://github.com/irssi/irssi/issues/875 "Fix test compilation on old glib"), [#905](https://github.com/irssi/irssi/issues/905 "Add tests for topic events"), [#964](https://github.com/irssi/irssi/issues/964 "fix duplicate include guard and link libs of test"), [#1011](https://github.com/irssi/irssi/issues/1011 "Use memcpy() instead of strncpy() to silence the compiler warning.")). Fuzzing ([#929](https://github.com/irssi/irssi/issues/929 "Remove incorrectly copied automake commands from fuzzer")).

---

## 1.1.2
{:#v1-1-2 }

The Irssi team released this <abbr class="timeago" title="2019-01-09">2019-01-09</abbr> 

{% include relnews_artef_block.markdown ver="1.1.2" %}

### Fixes
{:#v1-1-2-fixes }

- Fix the resetting of window hiddenlevel ([#861](https://github.com/irssi/irssi/issues/861 "in fact hidden levels should not be re-set when you run /set"))
- Fix clearing of hidelevel in layout ([#951](https://github.com/irssi/irssi/issues/951 "fe-text: clear hidelevel in layout if default"))
- Fix accessing unallocated text when checking entry position ([#928](https://github.com/irssi/irssi/issues/928 "Uninitialized access in pos2scrpos (gui-entry.c)"), [#930](https://github.com/irssi/irssi/issues/930 "fix accessing unallocated text when checking entry position"))
- Fix uninitialised memory on empty lines ([#873](https://github.com/irssi/irssi/issues/873 "record line info on empty lines"), [GL#31](https://gitlab.com/irssi/irssi/issues/31), [#878](https://github.com/irssi/irssi/issues/878 "Revert ''record line info on empty lines''"), [#877](https://github.com/irssi/irssi/issues/877 "display corruption e.g. in trackbar"), [#907](https://github.com/irssi/irssi/issues/907 "HIDDEN level related crash"), [#914](https://github.com/irssi/irssi/issues/914 "properly record line info on empty lines"))
- Fix use-after-free on expiration of hidden lines ([#948](https://github.com/irssi/irssi/issues/948 "invalidate startline and bottom_startline when hidden"))
- Fix use-after-frees. By Maya Rashish ([#919](https://github.com/irssi/irssi/issues/919 "Use-after-frees"))
- Fix out of bounds access in help display when window width is small ([#949](https://github.com/irssi/irssi/issues/949 "Fix insufficient size of help column when the window width is small"))
- Fix paste_join_multiline ([#970](https://github.com/irssi/irssi/issues/970 "paste_join_multiline not working?"), [#971](https://github.com/irssi/irssi/issues/971 "fix paste_join_multiline"))
- Correctly check for errno when displaying SSL errors. By Janik Rabe ([#895](https://github.com/irssi/irssi/issues/895 "Keep errstr set to NULL if errno is not set"))
- Fix wrong signal emission argument count ([#965](https://github.com/irssi/irssi/issues/965 "Fix wrong signal emission arg count"))
- Documentation ([#920](https://github.com/irssi/irssi/issues/920 "Add information about crash on unload to perl.txt")). Sync NEWS, scripts ([#849](https://github.com/irssi/irssi/issues/849 "add additional notes to NEWS"))
- Fix Perl detection on MacOS. By Dominyk Tiller ([#927](https://github.com/irssi/irssi/issues/927 "configure: fix Perl detection on macOS Mojave"))
- Misc fixes. By Jaroslav Škarvada ([#981](https://github.com/irssi/irssi/issues/981 "Coverity static analysis scan results"), [#982](https://github.com/irssi/irssi/issues/982 "Fixed problem found by Coverity Scan"))

---

## 1.1.1
{:#v1-1-1 }

The Irssi team released this <abbr class="timeago" title="2018-02-15">2018-02-15</abbr> 

{% include relnews_artef_block.markdown ver="1.1.1" %}

Contains all changes from 1.0.7

### Fixes
{:#v1-1-1-fixes }

- Restore compatibility with OpenSSL &lt; 1.0.2 ([#820](https://github.com/irssi/irssi/issues/820 "crash in x509"), [#831](https://github.com/irssi/irssi/issues/831 "Do not use X509_STORE on OpenSSL < 1.0.2"))
- Fix test compilation on some platforms ([#815](https://github.com/irssi/irssi/issues/815 "irssi-1.1.0 make check link errors on Solaris 11.3"), [#816](https://github.com/irssi/irssi/issues/816 "fix test builds on some platforms"))
- Fix portability and backwards compatibility of test runner ([#818](https://github.com/irssi/irssi/issues/818 "add backwards compatible code for running tap tests"), [#845](https://github.com/irssi/irssi/issues/845 "warn if there is non-portable code in the test-driver"))

---

## 1.0.7
{:#v1-0-7 }

The Irssi team released this <abbr class="timeago" title="2018-02-15">2018-02-15</abbr> 

{% include relnews_artef_block.markdown ver="1.0.7" %}

### Fixes
{:#v1-0-7-fixes }

- Prevent use after free error during the execution of some commands. Found by Joseph Bisch ([GL#17](https://gitlab.com/irssi/irssi/issues/17), [GL!24](https://gitlab.com/irssi/irssi/merge_requests/24)).
- Revert netsplit print optimisation due to crashes ([#465](https://github.com/irssi/irssi/issues/465 "Some small adjustments to the netsplit code."), [#809](https://github.com/irssi/irssi/issues/809 "Netsplits don't show in all windows where users split"), [#812](https://github.com/irssi/irssi/issues/812 "revert netsplit print optimisation"), [#819](https://github.com/irssi/irssi/issues/819 "Segmentation fault in normal usage"), [#824](https://github.com/irssi/irssi/issues/824 "Revert more of the netsplit print optimisation to fix crashes"), [#832](https://github.com/irssi/irssi/issues/832 "try to make sure the server is still good enough to call ischannel when printing netsplit/join")).
- Fix use after free when SASL messages are received in unexpected order ([GL#26](https://gitlab.com/irssi/irssi/issues/26), [GL!33](https://gitlab.com/irssi/irssi/merge_requests/33)).
- Fix null pointer dereference in the tab completion when an empty nick is joined ([GL#24](https://gitlab.com/irssi/irssi/issues/24), [GL!31](https://gitlab.com/irssi/irssi/merge_requests/31)).
- Fix use after free when entering oper password ([GL#22](https://gitlab.com/irssi/irssi/issues/22), [GL!32](https://gitlab.com/irssi/irssi/merge_requests/32)).
- Fix null pointer dereference when too many windows are opened ([GL#27](https://gitlab.com/irssi/irssi/issues/27), [#837](https://github.com/irssi/irssi/issues/837 "check the error condition of mainwindow_create")).
- Fix out of bounds access in theme strings when the last escape is incomplete. Credit to Oss-Fuzz ([#842](https://github.com/irssi/irssi/issues/842 "Fix oob in escaped theme string")).
- Fix out of bounds write when using negative counts on window resize ([GL#25](https://gitlab.com/irssi/irssi/issues/25), [GL#29](https://gitlab.com/irssi/irssi/issues/29), [#836](https://github.com/irssi/irssi/issues/836 "Fix resizing of windows when used incorrectly")).
- Minor help correction. By William Jackson ([#834](https://github.com/irssi/irssi/issues/834 "Fix typo in help text for /ISON command")).

---

## 1.1.0
{:#v1-1-0 }

The Irssi team released this <abbr class="timeago" title="2018-01-15">2018-01-15</abbr> 

{% include relnews_artef_block.markdown ver="1.1.0" %}

**Warning**. Irssi is broken and will crash with OpenSSL &lt; 1.0.2 due to [openssl/openssl@`5b4b9ce97`](https://github.com/openssl/openssl/commit/5b4b9ce976fce09a7a92e2f25b91a1635cb840fe)

### Changes
{:#v1-1-0-changes }

- Colour is now re-set when reaching a comma, matching mIRC behaviour ([#742](https://github.com/irssi/irssi/issues/742 "Reset foreground and background while only comma is specified"), [#740](https://github.com/irssi/irssi/issues/740 "Color codes which end in commas both reset background and print comma as literal"), [#790](https://github.com/irssi/irssi/issues/790 "reset colour at comma, like mIRC"))
- Irssi now shows the initial nick and name on first start ([#785](https://github.com/irssi/irssi/issues/785 "IRSSI sends user's real name to all joined servers by default (originally: real_name defaults to actual name on OSX)"), [#786](https://github.com/irssi/irssi/issues/786 "show initial nick and name on first start"))
- lynx is no longer required to run autogen.sh ([#81](https://github.com/irssi/irssi/issues/81 "Build system requires lynx or elinks and fails without it"), [#781](https://github.com/irssi/irssi/issues/781 "remove lynx from autogen and make a separate syncdocs script"))
- The command history no longer permits wrapping around ([#686](https://github.com/irssi/irssi/issues/686 "Don't allow command history to wrap around"))
- /foreach now correctly sends arguments as commands, stopping you from embarassing AMSGs ([#659](https://github.com/irssi/irssi/issues/659 "make foreach send commands"))
- /server does not connect to servers anymore, use /server connect to change servers ([#559](https://github.com/irssi/irssi/issues/559 "Consider making /server <hostname> an error"), [#649](https://github.com/irssi/irssi/issues/649 "Do not alias /server <hostname> to /server connect <hostname>")).
- The net_ip_compare API function is now deprecated, and the previously deprecated net_connect has been removed. By Will Storey ([#770](https://github.com/irssi/irssi/issues/770 "Remove a couple unused functions")).

### Additions
{:#v1-1-0-additions }

- Add an option to ignore all channels or ignore all queries using /set activity_hide_targets. By Jari Matilainen ([#612](https://github.com/irssi/irssi/issues/612 "Allow selection of what kind of activity targets to ignore"), [#779](https://github.com/irssi/irssi/issues/779 "Allow selection of what kind of activity targets to ignore v2"))
- Add a startup warning if the TERM var is wrong inside tmux/screen ([#726](https://github.com/irssi/irssi/issues/726 "Add a startup warning if the TERM var is wrong inside tmux/screen"))
- Add option to hide certain levels from the textbuffer using /window hidelevel ([#746](https://github.com/irssi/irssi/issues/746 "Add method to hide lines in a view"), [#808](https://github.com/irssi/irssi/issues/808 "Add perl access to hidden_level in TEXT_BUFFER_VIEW_REC "))
- Irssi now has its first unit test (for mode parsing). By Will Storey ([#793](https://github.com/irssi/irssi/issues/793 "Add tests for mode parsing"))
- Added access to global command history when using window history, and a binding to erase entries from the command history (erase_history_entry) ([#762](https://github.com/irssi/irssi/issues/762 "allow access to global command history when using a specifc history"))
- -alternate_nick is now available as a network specific property. By Paul Townsend ([#120](https://github.com/irssi/irssi/issues/120 "Please add alternate_nick as being a NETWORK property"), [#771](https://github.com/irssi/irssi/issues/771 "Add alternate_nick as a network-specific property"))
- On FreeBSD, Irssi now supports Capsicum sandbox (/capsicum enter). By Edward Tomasz Napierala ([#735](https://github.com/irssi/irssi/issues/735 "Add Capsicum support"), [#755](https://github.com/irssi/irssi/issues/755 "Get rid of the zombies in Capsicum capability mode."), [#772](https://github.com/irssi/irssi/issues/772 "Capsicum"))
- Filenames (directories) ending with a / now tab-complete ([#741](https://github.com/irssi/irssi/issues/741 "Complete filenames ending with a slash"))
- UTF-8 should now work in regular expressions when using GRegex (the default) ([#636](https://github.com/irssi/irssi/issues/636 "GRegex not utf8 compliant?"), [#653](https://github.com/irssi/irssi/issues/653 "Enable UTF8 in GRegex"))
- Nicks are now properly escaped on completion. By Oscar Linderholm ([#693](https://github.com/irssi/irssi/issues/693 "Nick completion should escape nicks when expand_escapes is on"), [#709](https://github.com/irssi/irssi/issues/709 "Escape nicks during nick completion when expand_escapes is enabled"))
- /server add -port &lt;num> now works. By Jari Matilainen ([#703](https://github.com/irssi/irssi/issues/703 "Allow -port <num> or irc.host.tld <num> in /server add "))
- Add a setting key_timeout to make key sequences automatically re-set when not finished ([#644](https://github.com/irssi/irssi/issues/644 "Usage issues with multiple-key keybindings"), [#645](https://github.com/irssi/irssi/issues/645 "Timeout feature for keys"))
- Warn users about expired client certificates, as servers may refuse them ([#211](https://github.com/irssi/irssi/issues/211 "Warn if the client certificate is expired"), [#627](https://github.com/irssi/irssi/issues/627 "Check whether the client certificate is expired."))
- Add a new net_start_ssl function for StartTLS. This is available from ABI 8 and can be used by protocol modules ([#615](https://github.com/irssi/irssi/issues/615 "Make irssi_ssl_get_iochannel accessible for plugins"), [#622](https://github.com/irssi/irssi/issues/622 "provide net_start_ssl api")).
- The %# code is now stored in the textbuffer, so for example web scripts can make use of it ([#626](https://github.com/irssi/irssi/issues/626 "support storing and replaying the monospace attribute in textbuffer"))
- Add new setting break_wide which can be used to enable breaking of wide characters (for east-asian users). Originally from FreeBSD ports. ([#625](https://github.com/irssi/irssi/issues/625 "implement break_wide"))
- Add fuzzing code ([#610](https://github.com/irssi/irssi/issues/610 "Add frontend for fuzzing"), [#620](https://github.com/irssi/irssi/issues/620 "Add SUPPRESS_PRINTF_FALLBACK"), [#701](https://github.com/irssi/irssi/issues/701 "Add fuzz.diff for fuzzing with afl"), [#713](https://github.com/irssi/irssi/issues/713 "Use CXX for fe-fuzz linking"))

### Fixes
{:#v1-1-0-fixes }

- Netsplits show properly again ([#812](https://github.com/irssi/irssi/issues/812 "revert netsplit print optimisation"))
- Do not error on blank lines when using /exec -o. By Fabian Kurz ([FS#902](https://github.com/irssi-import/bugs.irssi.org/issues/902 "Empty lines in output of ''exec'' command cause ''Not enough parameters given'' errors"), [#805](https://github.com/irssi/irssi/issues/805 "fix /exec -o for blank lines"))
- Detect used nickname as reported by server. By Alexandre Morignot ([#219](https://github.com/irssi/irssi/issues/219 "handle an already used nick different from the one we send"), [#804](https://github.com/irssi/irssi/issues/804 "handle an already used nick different from the one we send"))
- Prevent use after free error during the execution of some commands. Found by Joseph Bisch. ([GL#17](https://gitlab.com/irssi/irssi/issues/17), [GL!24](https://gitlab.com/irssi/irssi/merge_requests/24))
- Fix MODE parameter parsing when colon was used at a place Irssi didn't expect ([#601](https://github.com/irssi/irssi/issues/601 "`MODE #foo +o :user` gets parsed as `+o :user`, not `+o user`"), [#766](https://github.com/irssi/irssi/issues/766 "Fix MODE parameter parsing"))
- Fixed code to compile with -Werror=declaration-after-statement ([#795](https://github.com/irssi/irssi/issues/795 "check for declaration-after-statement on travis"))
- Clang-format is now supported for git-clang-format ([#784](https://github.com/irssi/irssi/issues/784 "Turn the style guide into a clang-format file"))
- Fix use after free when changing the network of hilights. Reported by Rui Mathias. ([#787](https://github.com/irssi/irssi/issues/787 "/hilight generating garbage when passed with multiple -network parameters"), [#788](https://github.com/irssi/irssi/issues/788 "Keep a copy of the strings coming from the config"))
- Fix positioning error when tab-completing non-ascii strings. ([#752](https://github.com/irssi/irssi/issues/752 "tab completion miscounts characters "), [#754](https://github.com/irssi/irssi/issues/754 "add new function to set the position in bytes"))
- In-development issues ([#750](https://github.com/irssi/irssi/issues/750 "Segfault in SSL code / sk_num"), [#751](https://github.com/irssi/irssi/issues/751 "Increment the X509_STORE refcount during the connection"))
- Clarify Alis in /help list ([#699](https://github.com/irssi/irssi/issues/699 "Documentation for /list is incorrect(ish)"), [#712](https://github.com/irssi/irssi/issues/712 "Update list.in"))
- Improve /lastlog performance from O(N^2) to O(N) ([#715](https://github.com/irssi/irssi/issues/715 "Performance improvements for /lastlog"))
- Fix a segfault on "script destroyed" signal. By Stephen Oberholtzer ([#660](https://github.com/irssi/irssi/issues/660 "Segfault when unloading a script that registers for 'script destroyed' signals"), [#661](https://github.com/irssi/irssi/issues/661 "Fix for #660")).
- Fix early ISON error ([#596](https://github.com/irssi/irssi/issues/596 "ISON sent too early when using SASL"), [#647](https://github.com/irssi/irssi/issues/647 "notify-ison: Don't send ison before the connection is done"))
- Documentation improvements. By Paolo Martini ([#639](https://github.com/irssi/irssi/issues/639 "Make themes' docs more consistent.")). By Tristan Pepin ([#731](https://github.com/irssi/irssi/issues/731 "Clarified ambiguous autogen.sh error")).  By Paul Townsend ([#684](https://github.com/irssi/irssi/issues/684 "/help connect still says -ssl instead of -tls"), [#736](https://github.com/irssi/irssi/issues/736 "Update /CONNECT and /SERVER syntax tags (-ssl -> -tls).")). By Will Storey ([#777](https://github.com/irssi/irssi/issues/777 "Fix a typo in the readme"))
- Minor cleanups ([#590](https://github.com/irssi/irssi/issues/590 "Minor cleanup in the highlighting signal.")). By Edward Tomasz Napierala ([#734](https://github.com/irssi/irssi/issues/734 "Don't compute log_dir_create_mode in three different places."), [#738](https://github.com/irssi/irssi/issues/738 "Fix indentation; no functional changes."))
- Fix space issue in glib-2.0.m4 ([#621](https://github.com/irssi/irssi/issues/621 "Fix glib-2.0.m4 so that $PKG_CONFIG doesn't break configure script"))

---

## 1.0.6
{:#v1-0-6 }

The Irssi team released this <abbr class="timeago" title="2018-01-07">2018-01-07</abbr> 

{% include relnews_artef_block.markdown ver="1.0.6" %}

**Note**: Code and aliases using `$($`-like constructs are no longer supported due to issue [GL#18](https://gitlab.com/irssi/irssi/issues/18). Sorry about the inconvenience.

### Fixes
{:#v1-0-6-fixes }

- Fix invalid memory access when reading hilight configuration ([#787](https://github.com/irssi/irssi/issues/787 "/hilight generating garbage when passed with multiple -network parameters"), [#788](https://github.com/irssi/irssi/issues/788 "Keep a copy of the strings coming from the config")).
- Fix null pointer dereference when the channel topic is set without specifying a sender ([GL#20](https://gitlab.com/irssi/irssi/issues/20), [GL!25](https://gitlab.com/irssi/irssi/merge_requests/25)).
- Fix return of random memory when using incomplete escape codes ([GL#21](https://gitlab.com/irssi/irssi/issues/21), [GL!26](https://gitlab.com/irssi/irssi/merge_requests/26)).
- Fix heap buffer overflow when completing certain strings ([GL#19](https://gitlab.com/irssi/irssi/issues/19), [GL!27](https://gitlab.com/irssi/irssi/merge_requests/27)).
- Fix return of random memory when using an incomplete variable argument ([GL#18](https://gitlab.com/irssi/irssi/issues/18), [GL!28](https://gitlab.com/irssi/irssi/merge_requests/28)).

---

## 1.0.5
{:#v1-0-5 }

The Irssi team released this <abbr class="timeago" title="2017-10-23">2017-10-23</abbr> 

{% include relnews_artef_block.markdown ver="1.0.5" %}

### Fixes
{:#v1-0-5-fixes }

- Fix missing -sasl_method '' in /NETWORK ([#718](https://github.com/irssi/irssi/issues/718 "Add -nosasl flag to /network modify"), [#719](https://github.com/irssi/irssi/issues/719 "Setting sasl_mechanism to '' disables the auth")).
- Fix incorrect restoration of term state when hitting SUSP inside screen ([#737](https://github.com/irssi/irssi/issues/737 "Revert ''Merge pull request #452 from LemonBoy/terminfo-cup''"), [#733](https://github.com/irssi/irssi/issues/733 "Irssi terminal in inconsistent state after ignored suspend")).
- Fix out of bounds read when compressing colour sequences. Found by Hanno Böck ([GL#12](https://gitlab.com/irssi/irssi/issues/12), [GL!18](https://gitlab.com/irssi/irssi/merge_requests/18)).
- Fix use after free condition during a race condition when waiting on channel sync during a rejoin ([GL#13](https://gitlab.com/irssi/irssi/issues/13), [GL!19](https://gitlab.com/irssi/irssi/merge_requests/19)).
- Fix null pointer dereference when parsing certain malformed CTCP DCC messages ([GL#14](https://gitlab.com/irssi/irssi/issues/14), [GL!20](https://gitlab.com/irssi/irssi/merge_requests/20)).
- Fix crash due to null pointer dereference when failing to split messages due to overlong nick or target ([GL#15](https://gitlab.com/irssi/irssi/issues/15), [GL!21](https://gitlab.com/irssi/irssi/merge_requests/21)).
- Fix out of bounds read when trying to skip a safe channel ID without verifying that the ID is long enough ([GL#16](https://gitlab.com/irssi/irssi/issues/16), [GL!22](https://gitlab.com/irssi/irssi/merge_requests/22)).
- Fix return of random memory when inet_ntop failed ([#769](https://github.com/irssi/irssi/issues/769 "Set host to an empty string on error")).
- Minor statusbar help update. By Robert Bisewski ([#758](https://github.com/irssi/irssi/issues/758 "The /statusbar documentation is bad"), [#763](https://github.com/irssi/irssi/issues/763 "Improvements to statusbar documentation and help text.")).

---

## 1.0.4
{:#v1-0-4 }

The Irssi team released this <abbr class="timeago" title="2017-07-07">2017-07-07</abbr> 

{% include relnews_artef_block.markdown ver="1.0.4" %}

### Fixes
{:#v1-0-4-fixes }

- Fix null pointer dereference when parsing invalid timestamp ([GL#10](https://gitlab.com/irssi/irssi/issues/10), [GL!15](https://gitlab.com/irssi/irssi/merge_requests/15)). Reported by Brian 'geeknik' Carpenter.
- Fix use-after-free condition when removing nicks from the internal nicklist ([GL#11](https://gitlab.com/irssi/irssi/issues/11), [GL!16](https://gitlab.com/irssi/irssi/merge_requests/16)). Reported by Brian 'geeknik' Carpenter.
- Fix incorrect string comparison in DCC file names ([#714](https://github.com/irssi/irssi/issues/714 "fe-dcc-(get│send): Fix some -Wpointer-compare with newer gcc")).
- Fix regression in Irssi 1.0.3 where it would claim "Invalid time '-1'" ([#716](https://github.com/irssi/irssi/issues/716 "Warnings on start up: invalid time '-1'"), [#722](https://github.com/irssi/irssi/issues/722 "parse_time_interval: Allow negative time in settings")).
- Fix a bug when using \n to separate lines with expand_escapes ([#723](https://github.com/irssi/irssi/issues/723 "fix weird n-fold unescaping in expand_escapes")).
- Retain screen output on improper exit, to better see any error messages ([#287](https://github.com/irssi/irssi/issues/287 "Errors that call ''noperl_die()'' do exit(1) and the resulting error is not visible"), [#721](https://github.com/irssi/irssi/issues/721 "term-terminfo: Avoid switching out of alt screen on unexpected exits")).
- Minor help update ([#729](https://github.com/irssi/irssi/issues/729 "More accurately describe clear")).

---

## 1.0.3
{:#v1-0-3 }

The Irssi team released this <abbr class="timeago" title="2017-06-06">2017-06-06</abbr> 

{% include relnews_artef_block.markdown ver="1.0.3" %}

Regression info in 1.0.3: [#716](https://github.com/irssi/irssi/issues/716 "Warnings on start up: invalid time '-1'") Warnings on start up: invalid time '-1'

### Fixes
{:#v1-0-3-fixes }

- Fix out of bounds read when scanning expandos ([GL!11](https://gitlab.com/irssi/irssi/merge_requests/11)).
- Fix invalid memory access with quoted filenames in DCC ([GL#8](https://gitlab.com/irssi/irssi/issues/8), [GL!12](https://gitlab.com/irssi/irssi/merge_requests/12)).
- Fix null-pointer dereference on DCC without address ([GL#9](https://gitlab.com/irssi/irssi/issues/9), [GL!13](https://gitlab.com/irssi/irssi/merge_requests/13)).
- Improve integer overflow handling. Originally reported by [oss-fuzz#525](https://bugs.chromium.org/p/oss-fuzz/issues/detail?id=525) ([#706](https://github.com/irssi/irssi/issues/706 "Add parse_uint function to improve integer overflow handling")).
- Improve nicklist performance from O(N^2) to O(N) ([#705](https://github.com/irssi/irssi/issues/705 "improve nicklist performance")).
- Fix initial screen redraw delay. By Stephen Oberholtzer ([#680](https://github.com/irssi/irssi/issues/680 "Fix slow startup with glib 2.49.3"), [bdo#856201](https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=856201)).
- Fix incorrect reset of true colours when resetting background. ([#711](https://github.com/irssi/irssi/issues/711 "do not reset true colour bit on colour reset")).
- Fix missing -notls option in /SERVER. By Jari Matilainen ([#117](https://github.com/irssi/irssi/issues/117 "Add -nossl, -nossl_verify, and other missing -no* flags in /server"), [#702](https://github.com/irssi/irssi/issues/702 "Added support for -notls and -notls_verify")).
- Fix minor history glitch on overcounter ([#462](https://github.com/irssi/irssi/issues/462 "Window input history works strangely with window history cleared"), [#685](https://github.com/irssi/irssi/issues/685 "Fix strange history behavior when history is empty")).
- Improved OpenSSL detection at compile time. By Rodrigo Rebello ([#677](https://github.com/irssi/irssi/issues/677 "OpenSSL support detection and documentation fixes")).
- Improved NetBSD Terminfo detection. By Maya Rashish ([#694](https://github.com/irssi/irssi/issues/694 "Accept -lcurses as well"), [#698](https://github.com/irssi/irssi/issues/698 "detect Netbsd terminfo")).
- Add missing syntax info for COMPLETION ([#687](https://github.com/irssi/irssi/issues/687 "Syntax for /completion is missing in help"), [#688](https://github.com/irssi/irssi/issues/688 "Add syntax info for completion")).
- Minor typo correction in help. By Michael Hansen ([#707](https://github.com/irssi/irssi/issues/707 "dcc.in: fixed typo 'resolved' -> 'resolves'")).

---

## 1.0.2
{:#v1-0-2 }

The Irssi team released this <abbr class="timeago" title="2017-03-10">2017-03-10</abbr> 

{% include relnews_artef_block.markdown ver="1.0.2" %}

**Warning**. Irssi is broken on GLib 2.46 ([bgo#755496](https://bugzilla.gnome.org/show_bug.cgi?id=755496))

### Fixes
{:#v1-0-2-fixes }

- Prevent some null-pointer crashes ([GL!9](https://gitlab.com/irssi/irssi/merge_requests/9)).
- Fix compilation with OpenSSL 1.1.0 ([#628](https://github.com/irssi/irssi/issues/628 "Support OpenSSL 1.1.0."), [#597](https://github.com/irssi/irssi/issues/597 "OpenSSL 1.1 API deprecations")).
- Correct dereferencing of already freed server objects during output of netjoins. Found by APic ([GL!10](https://gitlab.com/irssi/irssi/merge_requests/10), [GL#7](https://gitlab.com/irssi/irssi/issues/7)).
- Fix in command arg parser to detect missing arguments in tail place ([#652](https://github.com/irssi/irssi/issues/652 "Properly check the command arguments in tail place."), [#651](https://github.com/irssi/irssi/issues/651 "Problem to parse options with captial letters with Irssi::command_parse_options")).
- Fix regression that broke incoming DCC file transfers ([#667](https://github.com/irssi/irssi/issues/667 "fix dcc get"), [#656](https://github.com/irssi/irssi/issues/656 "DCC autoget stopped working")).
- Fix issue with escaping \ in evaluated strings ([#669](https://github.com/irssi/irssi/issues/669 "expand_escape: expand double backslash as a backslash"), [#520](https://github.com/irssi/irssi/issues/520 "/set expand_escapes ON doesn't handle double-escaping (''\\n'')")).

---

## 1.0.1
{:#v1-0-1 }

The Irssi team released this <abbr class="timeago" title="2017-02-03">2017-02-03</abbr> 

{% include relnews_artef_block.markdown ver="1.0.1" %}

### Fixes
{:#v1-0-1-fixes }

- Fix Perl compilation in object dir. By Martijn Dekker ([#602](https://github.com/irssi/irssi/issues/602 "make irssi --with-perl build with separate object directory"), [#623](https://github.com/irssi/irssi/issues/623 "irssi-1.0.0 perl extension fails to build ")).
- Disable EC cryptography on Solaris to fix build ([#604](https://github.com/irssi/irssi/issues/604 "Add OPENSSL_NO_EC for solaris 11.3, see issue #598"), [#598](https://github.com/irssi/irssi/issues/598 "irssi 1.0.0 fails to compile on Solaris 11 because OpenSSL is not compiled with EC support")).
- Fix incorrect HELP SERVER example ([#606](https://github.com/irssi/irssi/issues/606 "Fix syntax on /help SERVER example"), [#519](https://github.com/irssi/irssi/issues/519 "/help SERVER ADD -port and -! examples incorrect")).
- Correct memory leak in /OP and /VOICE. By Tim Konick ([#608](https://github.com/irssi/irssi/issues/608 "Follow g_strsplit with call to g_strfreev")).
- Fix regression that broke second level completion ([#613](https://github.com/irssi/irssi/issues/613 "fix regression in completion"), [#609](https://github.com/irssi/irssi/issues/609 "Regression in tab completion of setting values (`/set <name> <space><tab>`)")).
- Correct missing NULL termination in perl_parse. By Hanno Böck ([#619](https://github.com/irssi/irssi/issues/619 "perl_parse needs NULL terminated parameter list.")).
- Sync broken mail.pl script ([#624](https://github.com/irssi/irssi/issues/624 "sync mail.pl"), [#607](https://github.com/irssi/irssi/issues/607 "scripts/mail.pl not suited for 'use strict;' ")).
- Prevent a memory leak during the processing of the SASL response ([GL!8](https://gitlab.com/irssi/irssi/merge_requests/8), [GL#5](https://gitlab.com/irssi/irssi/issues/5))

---

## 1.0.0
{:#v1-0-0 }

The Irssi team released this <abbr class="timeago" title="2017-01-03">2017-01-03</abbr> 

{% include relnews_artef_block.markdown ver="1.0.0" %}

### Changes
{:#v1-0-0-changes }

- Removed \-\-disable-ipv6 ([#408](https://github.com/irssi/irssi/issues/408 "Delete the HAVE_IPV6 ifdef.")).
- /connect Network now aborts with an error if no servers have been added to that network ([#443](https://github.com/irssi/irssi/issues/443 "Throw an error when a chatnet has no available url")).
- /dcc commands now use quotes around spaces consistently.
- bell_beeps was removed ([#524](https://github.com/irssi/irssi/issues/524 "Kill bell_beeps setting (or make it a no-op)"), [#565](https://github.com/irssi/irssi/issues/565 "Kill bell_beeps.")).
- Switch to GRegex instead of regex.h ([#412](https://github.com/irssi/irssi/issues/412 "Use GLib's regexp interface (backed by PCRE)")).

### Additions
{:#v1-0-0-additions }

- irssiproxy can now forward all tags through a single port. By Lukas Mai (mauke, [#425](https://github.com/irssi/irssi/issues/425 "irssi proxy: allow multiplexing multiple networks over a single port")).
- irssiproxy can also listen on unix sockets. By Lukas Mai ([#427](https://github.com/irssi/irssi/issues/427 "irssi proxy: allow listening on unix sockets")).
- send channel -botcmds immediately when no mask is specified ([#175](https://github.com/irssi/irssi/issues/175 "-botcmd only works on small channels"), [#399](https://github.com/irssi/irssi/issues/399 "Change when the autocmds are sent.")).
- the kill buffer now remembers consecutive kills. New bindings were added: yank_next_cutbuffer and append_next_kill By Todd A. Pratt ([#353](https://github.com/irssi/irssi/issues/353 "Allow for prepending to the cutbuffer in addition to replacing it."), [#414](https://github.com/irssi/irssi/issues/414 "add an append operation to cut buffer handling"), [#455](https://github.com/irssi/irssi/issues/455 "improved cutbuffer handling"))
- connections will avoid looking up IPv6 addresses if the machine does not have an IPv6 address assigned (exact behaviour is implementation defined, [#410](https://github.com/irssi/irssi/issues/410 "Getaddrinfo v6 flag")).
- Fix potential crash if scripts insert undef values into the completion list ([#413](https://github.com/irssi/irssi/issues/413 "completion: Fix crash when the complist provided by a script has nulls")).
- Paste warning is now also shown on pasting overlong lines. By Manish Goregaokar ([#426](https://github.com/irssi/irssi/issues/426 "Make pasting warning appear when long pastes are going to be split into many lines")).
- autolog_ignore_targets and activity_hide_targets learn a new syntax
      tag/* and * to ignore whole networks or everything. By Jari Matilainen (vague666, [#437](https://github.com/irssi/irssi/issues/437 "Use glob matching for activity_hide_targets"))
- /hilight got a -matchcase flag to hilight case sensitively. By Thibault B (isundil, [#421](https://github.com/irssi/irssi/issues/421 "Add an option to make /hilight case sensitive"), [#476](https://github.com/irssi/irssi/issues/476 "Add an option to make /hilight case sensitive")).
- Always build irssi with TLS support.
- Rename SSL to TLS in the code and add -tls_* versions of the -ssl_* options to /CONNECT and /SERVER, but make sure the -ssl_* options continue to work.
- Use TLS for Freenode, EFnet, EsperNet, OFTC, Rizon, and IRC6 in the default configuration.
- Display TLS connection information upon connect. You can disable this by setting tls_verbose_connect to FALSE.
- Add -tls_pinned_cert and -tls_pinned_pubkey for x509 and public key pinning.
  
  The values needed for -tls_pinned_cert and -tls_pinned_pubkey is shown when connecting to a TLS enabled IRC server, but you can also find the values like this: Start by downloading the certificate from a given IRC server:
  
  
      $ openssl s_client -connect irc.example.net:6697 &lt; /dev/null 2>/dev/null | \
        openssl x509 > example.cert
  
  Find the value for -tls_pinned_cert:
  
  
      $ openssl x509 -in example.cert -fingerprint -sha256 -noout
  
  Find the value for -tls_pinned_pubkey:
  
  
      $ openssl x509 -in example.cert -pubkey -noout | \
        openssl pkey -pubin -outform der | \
        openssl dgst -sha256 -c | \
        tr a-z A-Z
- Remove support for DANE validation of TLS certificates.
  
  There wasn't enough support in the IRC community to push for this on the majority of bigger IRC networks. If you believe this should be reintroduced into irssi, then please come up with an implementation that does not rely on the libval library. It is causing a lot of troubles for our downstream maintainers.
- /names and $[...] now uses utf8 string operations. By Xavier G. ([#40](https://github.com/irssi/irssi/issues/40 "/names list isn't lined up properly if nicks are in UTF-8"), [#411](https://github.com/irssi/irssi/issues/411 "width calculation not handled correctly with regards to utf8 characters in variable expansion"), [#471](https://github.com/irssi/irssi/issues/471 "Handle utf8 nicks"), [#480](https://github.com/irssi/irssi/issues/480 "Handle utf8 nicks with mk_wcwidth()")).
- New setting completion_nicks_match_case ([#488](https://github.com/irssi/irssi/issues/488 "Be smart about case-matching the nicks.")).
- /channel /server /network now support modify subcommand. By Jari Matilainen ([#338](https://github.com/irssi/irssi/issues/338 "Add MODIFY to /network, /server and /channel"), [#498](https://github.com/irssi/irssi/issues/498 "Add modify to /channel, /server and /network")).
- Irssi::signal_remove now works with coderefs. By Tom Feist (shabble, [#512](https://github.com/irssi/irssi/issues/512 "Allow Irssi::signal_remove to work properly with coderefs")).
- /script reset got an -autorun switch ([#540](https://github.com/irssi/irssi/issues/540 "/script reset can now also run the autorun scripts"), [#538](https://github.com/irssi/irssi/issues/538 "/script reset unloads all scripts, but doesn't load autorun scripts")).
- cap_toggle can now be called from Perl, and fields cap_active and cap_supported can be inspected ([#542](https://github.com/irssi/irssi/issues/542 "Expose the CAP fields to the perl scripts.")).
- Make it possible to disable empty line completion. By Lauri Tirkkonen (lotheac, [#574](https://github.com/irssi/irssi/issues/574 "add completion_empty_line setting")).
- New option sasl_disconnect_on_failure to disconnect when SASL log-in failed ([#514](https://github.com/irssi/irssi/issues/514 "Add an option to stop the connection when SASL fails.")).

### Fixes
{:#v1-0-0-fixes }

- IP addresses are no longer stored when resolve_reverse_lookup is used.
- Removed broken support for curses ([#521](https://github.com/irssi/irssi/issues/521 "remove curses terminal and ncurses macro")).
- Removed broken dummy mode ([#526](https://github.com/irssi/irssi/issues/526 "remove broken dummy mode")).
- Fix terminal state after suspend ([#450](https://github.com/irssi/irssi/issues/450 "potential terminal state not reset after 2x suspend"), [#452](https://github.com/irssi/irssi/issues/452 "Don't call terminfo_cont() twice on resume")).
- Improve Perl library path detection ([#479](https://github.com/irssi/irssi/issues/479 "improve perl @INC detection"), [#132](https://github.com/irssi/irssi/issues/132 "sometimes wrong/useless path set for perl_use_lib")).
- Reconnect now works on unix connections ([#493](https://github.com/irssi/irssi/issues/493 "servers-reconnect: pass unix_socket attribute to new connection")).
- Fix completion warnings ([#125](https://github.com/irssi/irssi/issues/125 "Some glib assertion failure warnings when tab completing "), [#496](https://github.com/irssi/irssi/issues/496 "completion fixes"), [FS#124](https://github.com/irssi-import/bugs.irssi.org/issues/124 "Assertion failure in query window when cmdchars is set to a comma, typing '',wii <tab>''")).
- Fix a crash in the \-\-more-- item ([#501](https://github.com/irssi/irssi/issues/501 "check for NULL in statusbar_more_updated")).
- Fix a display issue in /unignore ([#517](https://github.com/irssi/irssi/issues/517 "Minor cosmetic fix in /unignore error message."), [bdo#577202](https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=577202)).
- Fix a crash in some netsplits ([#529](https://github.com/irssi/irssi/issues/529 "fix nick->host == NULL crash"), [#500](https://github.com/irssi/irssi/issues/500 "Random crash")).
- Fix crashes with some invalid config ([#550](https://github.com/irssi/irssi/issues/550 "segfault / null pointer access in config file parser"), [#551](https://github.com/irssi/irssi/issues/551 "nullptr when doing module backward compat on invalid config"), [#563](https://github.com/irssi/irssi/issues/563 "Segfault caused by config file"), [#564](https://github.com/irssi/irssi/issues/564 "Segfault in config_node_first at get.c:330"), [#587](https://github.com/irssi/irssi/issues/587 "add assertion to statusbar_read_group"), [#581](https://github.com/irssi/irssi/issues/581 "Enforce the is_node_list contract in lib-config setters."), [#570](https://github.com/irssi/irssi/issues/570 "enforce check that chatnets are nodelists to handle invalid config")).
- Add support for SASL Fragmentation. By Kenny Root (kruton, [#506](https://github.com/irssi/irssi/issues/506 "SASL: handle fragmentation")).
- Improve netsplit dumping ([#420](https://github.com/irssi/irssi/issues/420 "Find a less-global method of deciding when to print netsplits/mode/joins"), [#465](https://github.com/irssi/irssi/issues/465 "Some small adjustments to the netsplit code.")).
- Improve responsibility under DCC I/O strain ([#578](https://github.com/irssi/irssi/issues/578 "add a static buffer for dcc received data"), [#159](https://github.com/irssi/irssi/issues/159 "Freezing when receiving dcc")).
- Fix query nick change on open ([#580](https://github.com/irssi/irssi/issues/580 "Private messages go to the status window when the other user changes to an equivalent nick"), [#586](https://github.com/irssi/irssi/issues/586 "Process the nick changes in queries before the PRIVMSG is handled.")).
- Correct a few help texts.

---

## 0.8.21
{:#v0-8-21 }

The Irssi team released this <abbr class="timeago" title="2017-01-03">2017-01-03</abbr> 

{% include relnews_artef_block.markdown ver="0.8.21" %}

### Fixes
{:#v0-8-21-fixes }

- Correct a NULL pointer dereference in the nickcmp function found by Joseph Bisch ([GL#1](https://gitlab.com/irssi/irssi/issues/1))
- Correct an out of bounds read in certain incomplete control codes found by Joseph Bisch ([GL#2](https://gitlab.com/irssi/irssi/issues/2))
- Correct an out of bounds read in certain incomplete character sequences found by Hanno Böck and independently by J. Bisch ([GL#3](https://gitlab.com/irssi/irssi/issues/3))
- Correct an error when receiving invalid nick message ([GL#4](https://gitlab.com/irssi/irssi/issues/4), [#466](https://github.com/irssi/irssi/issues/466 "Assertion failure when sending an invalid NICK"))

---

## 0.8.20
{:#v0-8-20 }

The Irssi team released this <abbr class="timeago" title="2016-09-16">2016-09-16</abbr> 

{% include relnews_artef_block.markdown ver="0.8.20" %}

### Fixes
{:#v0-8-20-fixes }

- Correct the name of an emitted sasl signal ([#484](https://github.com/irssi/irssi/issues/484 "Correct the name of the emitted signal."))
- Correct the prototype for the 'message private' signal ([#515](https://github.com/irssi/irssi/issues/515 "Correct the prototype for the 'message private' signal."))
- Corrections in away and hilight help text ([#477](https://github.com/irssi/irssi/issues/477 "Correct error/typo ''You''->''Your'' in help message"), [#518](https://github.com/irssi/irssi/issues/518 "Wrong order in the arguments in /hilight example, -mask doesn't take …"))
- /squery and /servlist commands have been restored ([#461](https://github.com/irssi/irssi/issues/461 "Revert ''Removed the obsolete SQUERY and SERVLIST commands''")).
- Where Irssi would previously only report "System error" on connect, it will now try harder to retrieve the system error message ([#467](https://github.com/irssi/irssi/issues/467 "net_gethosterror: Handle EAI_SYSTEM (''System error'') properly")).
- Fixed issue with +channels not working properly ([#533](https://github.com/irssi/irssi/issues/533 "Set the default STATUSMSG to @ instead of @+ if it's missing"))
- Fixed crash in optchan when item has no server ([#485](https://github.com/irssi/irssi/issues/485 "Do not crash on OPTCHAN when item has no server"), [bdo#826525](https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=826525))
- Fixed random remote crash in the nicklist handling ([#529](https://github.com/irssi/irssi/issues/529 "fix nick->host == NULL crash"))
- Fixed remote crash due to incorrect bounds checking on formats, reported by Gabriel Campana and Adrien Guinet from Quarkslab.

---

## 0.8.19
{:#v0-8-19 }

The Irssi team released this <abbr class="timeago" title="2016-03-23">2016-03-23</abbr> 

{% include relnews_artef_block.markdown ver="0.8.19" %}

If your cursor keys stopped working, try this first: `/bind meta-O key meta2`

### Fixes
{:#v0-8-19-fixes }

- Fixed regression when joining and parting channels on IRCnet ([#435](https://github.com/irssi/irssi/issues/435 "joining +channels is broken"))
- Fixed SASL EXTERNAL. By Mantas Mikulėnas (grawity, [#432](https://github.com/irssi/irssi/issues/432 "fix SASL EXTERNAL"))
- Fixed regression when not using SASL ([#438](https://github.com/irssi/irssi/issues/438 "Remove sasl timeout source when the server disconnects"))
- Fixed incorrect SSL disconnects when using SSL from modules/scripts. By Will Storey (horgh, [#439](https://github.com/irssi/irssi/issues/439 "Clear error queue before SSL I/O operations"))
- Fixed regression where proxy_string could not be configured or certain file transfers could not be accepted ([#445](https://github.com/irssi/irssi/issues/445 "/eval set proxy_string broken"), [#446](https://github.com/irssi/irssi/issues/446 "strip less whitespace from commands"))
- Fixed storing layout of !channels ([#183](https://github.com/irssi/irssi/issues/183 "/layout save stores the ''visible name'' of !-channels (safe channels) instead of the real one"), [#405](https://github.com/irssi/irssi/issues/405 "Serialize the 'name' attribute of the CHANNEL_REC."))
- Fixed restoration of bracketed paste mode on quit ([#449](https://github.com/irssi/irssi/issues/449 "bracketed paste mode not deinitialised on leaving irssi"), [#457](https://github.com/irssi/irssi/issues/457 "fix race condition in terminal init"))
- Make the usage of meta-O for cursor keys configurable with
      /set term_appkey_mode off ([#430](https://github.com/irssi/irssi/issues/430 "Binding meta-O causes arrow keys to stop working"), [#459](https://github.com/irssi/irssi/issues/459 "Make use of terminal application keys configurable"))

---

## 0.8.18
{:#v0-8-18 }

The Irssi team released this <abbr class="timeago" title="2016-02-13">2016-02-13</abbr> 

{% include relnews_artef_block.markdown ver="0.8.18" %}

### Changes
{:#v0-8-18-changes }

- Modules will now require to define a
  
  
      void MODULENAME ## _abicheck(int *version)
  
  method to ensure that they are compiled against the correct Irssi version.
- The signature of "message private" has been changed to
  
  
      5: server, message, nick, address, target
  
  in order to support "self messages". Module authors should implement this change if they are using this signal.
- Removing networks will now remove all attached servers and channels ([#45](https://github.com/irssi/irssi/issues/45 "make it easy to delete default channels, servers and networks")).
- The proxy module now has an /irssiproxy command.
- sb_search has been moved to scripts.irssi.org
- WIN32 has been completely removed (it had not been working and is lacking a maintainer.)
- Garbage Collection support has been removed. This will hardly have any effect for anyone given that it has been unsupported for several years.

### Additions
{:#v0-8-18-additions }

- CAP SASL PLAIN login is now supported natively.
- Paste bracket markers can be requested from terminal with
  
  
      /set paste_use_bracketed_mode on
- "Self messages" generated by some bouncers can now be received in the proper window.
- Try to split long lines on spaces to avoid words being splitted. Adds a new option: `split_line_on_space` which defaults to on.
- Add setting `hilight_nick_matches_everywhere` ([#56](https://github.com/irssi/irssi/issues/56 "Add an option to allow highlights of your own nick in any part of a message")).
- The config parser is more robust and prints out better diagnostics on incorrect config files.
- Ctrl+^ ([FS#721](https://github.com/irssi-import/bugs.irssi.org/issues/721 "binding ctrl-^")) and Ctrl+J can now be bound.
- Command history can be cleared with /window history -clear
- /hilight -mask -line is now supported ([FS#275](https://github.com/irssi-import/bugs.irssi.org/issues/275 "/hilight -mask -line nick!*@* fails")).
- CHANTYPES are now supported.
- Improved reload speed of ignores.
- Add -date feature to /lastlog
- irssiproxy can be more easily enabled and disabled.
- Expando for hostname ([FS#829](https://github.com/irssi-import/bugs.irssi.org/issues/829 "Special variable for a hostname [patch]")).
- UNIX sockets can now also be specified in the config file.
- Disable SSLv3 due to the POODLE vulnerability.
- SSL ciphers can now be specified per server.
- Added SNI support for SSL.

### Fixes
{:#v0-8-18-fixes }

- /ignore now respects -pattern on merge ([#78](https://github.com/irssi/irssi/issues/78 "ignore overwrites")).
- irssiproxy (BNC) module now uses correct line endings.
- Fix missing lines on large pastes ([FS#905](https://github.com/irssi-import/bugs.irssi.org/issues/905 "paste_buffer_join_lines() - Mangled text when line length exceeds 400")).
- Correctly preserve STATUSMSG prefixes ([#291](https://github.com/irssi/irssi/issues/291 "/msg +#channel (wallvoices) incorrectly shows up as Nick:@#channel")).
- Fix infinite recursion in key bindings ([FS#817](https://github.com/irssi-import/bugs.irssi.org/issues/817 "SegFault when executing bind command")).
- Fix incomplete awaylog caused by buffering.
- Fix calculation of UTF-8 string length display in some cases.
- Fix some Perl warnings related to @ISA.
- EXEC windowitems now get proper references on the Perl side.
- Incremental help file improvements.
- ANSI attributes are now properly reset.
- Fixed regression where text would blink when terminal lacks color support.
- Permit the usage of Freenode extban syntax in /ban ([#150](https://github.com/irssi/irssi/issues/150 "freenode extbans don't work in /ban"))
- Fixed regression in scriptassist on unload of scripts.
- Fixed regression in -actcolor %n

---

## 0.8.17
{:#v0-8-17 }

The Irssi team released this <abbr class="timeago" title="2014-10-11">2014-10-11</abbr> 

{% include relnews_artef_block.markdown ver="0.8.17" %}

### Additions
{:#v0-8-17-additions }

- Document that SSL connections aren't properly handled during /UPGRADE. See Github PR [#39](https://github.com/irssi/irssi/issues/39 "Document that /UPGRADE doesn't work with SSL").
- Synchronize scripts with scripts.irssi.org.
- Performance enhancement of the nicklist as well as the window_item_find function. See Github PR [#24](https://github.com/irssi/irssi/issues/24 "Speed up nicklist and window_find operations").
- Disallow unloading of static modules.
- Allow UTF-8 characters in /bind. See Github PR [#18](https://github.com/irssi/irssi/issues/18 "(from marienz, via debian) add support for utf8 chars to /bind, irssi fs#553").
- Split overlong outgoing messages instead of silently truncating them. Adds two new options: 'split_line_end' and 'split_line_start'. 'split_line_end' contains a string added to the end of line fragments. 'split_line_start' contains a string added to the beginning of line fragments. See Github PR [#29](https://github.com/irssi/irssi/issues/29 "Properly split long IRC messages").
- Added special /ignore NO_ACT level to ignore only activity (see /help ignore).
- Support for 256 and true color terminals (see Github PR [#48](https://github.com/irssi/irssi/issues/48 "256 colour support for Irssi")).
- Support for italics (see Github PR [#58](https://github.com/irssi/irssi/issues/58 "Implement italics support for Irssi")).
- Rewrote many help files.

### Fixes
{:#v0-8-17-fixes }

- Fixed various compiler warnings and use of deprecated functions.
- Fixed Perl API usage and added PERL_NO_GET_CONTEXT to reduce code size.
- Fixed format_get_text Perl API. See Github PR [#23](https://github.com/irssi/irssi/issues/23 "fix implementation of format_get_text script api").
- Fixed gui_printtext_after and term_refresh_*() visibility. See Github PR [#22](https://github.com/irssi/irssi/issues/22 "Correct the packages of the scripting API").
- Fixed issue where UTF-8 characters was corrupted once for every 32k text. See Github PR [#12](https://github.com/irssi/irssi/issues/12 "no split utf8 from the bug tracker").
- Fixed redrawing issue with right-aligned statusbar.
- Fixed use-after-free bug with cached settings values. See Github PR [#147](https://github.com/irssi/irssi/issues/147 "Fix use-after-free bug with cached settings values").

---

## 0.8.16
{:#v0-8-16 }

The Irssi team released this <abbr class="timeago" title="2014-05-28">2014-05-28</abbr> 

{% include relnews_artef_block.markdown ver="0.8.16" %}

### Additions
{:#v0-8-16-additions }

- Add -noautosendcmd to /SERVER and /CONNECT. Passing this option will force Irssi to not execute the content of the autosendcmd chatnet-setting upon connect.
- Accept names replies with nick!user@host instead of just nick, if they are enabled (see bug [FS#805](https://github.com/irssi-import/bugs.irssi.org/issues/805 "Support for userhost in NAMES reply")).
- Set window binds for channel items as sticky when re-creating window binds as part of /layout save. This fixes the bug where previously saved channel windows forgets their window number upon reconnect.
- Add experimental support for DNSSEC DANE validation of certificates.
- Strip the argument for boolean options (see bug [FS#769](https://github.com/irssi-import/bugs.irssi.org/issues/769 "[Patch] Strip leading and trailing whitespaces from /SET bool values")).
- Freenode have been readded to the list of networks in the default configuration file.
- Disabled support for the insecure SSLv2 protocol.
- Various documentation enhancements.
- Add -ssl_pass to /connect and /server (see bug [FS#305](https://github.com/irssi-import/bugs.irssi.org/issues/305 "/connect -ssl_cert password_protected.pem problem")).

### Fixes
{:#v0-8-16-fixes }

- Fix crashing bug that can happen if the terminal height decreases before the first window is created.
- Fixed minor compiler warnings.
- Fixed possible crashing bug when processing an octal escape sequence.
- Fixed the /ignore -network option (see bug [FS#748](https://github.com/irssi-import/bugs.irssi.org/issues/748 "/ignore -network bug")).
- Fixed signal handling for /exec'd commands. Irssi now sends the signal to the process group id instead of the process id.
- Fixed segfault generated by SSL disconnections (see bug [FS#752](https://github.com/irssi-import/bugs.irssi.org/issues/752 "Segfault on unclean SSL disconnections.")).
- Fix compilation when build with -Werror=format-security. Patch by Jaroslav Skarvada.

---

## 0.8.15
{:#v0-8-15 }

The Irssi team released this <abbr class="timeago" title="2010-04-03">2010-04-03</abbr> 

{% include relnews_artef_block.markdown ver="0.8.15" %}

### Additions
{:#v0-8-15-additions }

- Add active_window_ignore_refnum option With active_window_ignore_refnum ON, the current behavior for the active_window key (meta-a by default) is preserved: it switches to the window with the highest activity level that was last activated. With active_window_ignore_refnum OFF, the old behavior is used: it switches to the window with the highest activity level with the lowest refnum. (by Matt Sparks, bug [FS#667](https://github.com/irssi-import/bugs.irssi.org/issues/667 "Change in Meta+a next active window logic"))
- Show new Charybdis +q list in channel windows (numerics 728 and 729).
- Allow servers to belong to multiple networks.
- Improve paste detection. Irssi now detects a paste if it reads at least three bytes in a single read; subsequent reads are associated to the same paste if they happen before 'paste_detect_time' time since the last read. If no read occurs after 'paste_detect_time' time the paste buffer is flushed; if there is at least one complete line its content is sent as a paste, otherwise it is processed normally.
- Show "target changing too fast" messages in the channel/query window.
- Use default trusted CAs if nothing is specified. This allows useful use of -ssl_verify without -ssl_cafile/-ssl_capath, using OpenSSL's default trusted CAs.
- Show why an SSL certificate failed validation.
- Make own nick and actions use default colour instead of white (by Tim Retout).

### Fixes
{:#v0-8-15-fixes }

- Change some characters illegal in Windows filenames to underscores in logs
- Fix disconnects when sending large amounts of data over SSL
- Show all nicks instead of just the first in an /accept * listing (Bug [FS#704](https://github.com/irssi-import/bugs.irssi.org/issues/704 "server side ignore (usermode +g) ACCEPT list not fully displayed"))
- Make several signals without parameters available to perl again. In particular, this includes the "beep" signal (by Matt Sparks, bug [FS#674](https://github.com/irssi-import/bugs.irssi.org/issues/674 "src/perl/get-signals.pl does not detect beep signal."))
- Close the config file fd after saving (by Sven Wegener)
- Check if an SSL certificate matches the hostname of the server we are connecting to.
- Fix bash'isms, use command -v instead of which and use bc -l in /CALC.
- Fix a crash with handling the DCC queue.
- Fix crash when checking for fuzzy nick match when not on the channel. Reported by Aurelien Delaitre (SATE 2009).

---

## 0.8.14
{:#v0-8-14 }

The Irssi team released this <abbr class="timeago" title="2009-07-28">2009-07-28</abbr> 

{% include relnews_artef_block.markdown ver="0.8.14" %}

### Additions
{:#v0-8-14-additions }

- Make /reset an alias for /set -default.
- Make /unset an alias for /set -clear.
- Allow ctrl+home / ctrl+end to go to the beginning / end of scrollback.
- Accept WHOX reply (354 numeric) as a /who reply.
- Show numerics directed at channels in the channel window.
- The time duration parser is more strict now.

### Fixes
{:#v0-8-14-fixes }

- Fix out of bounds access in event_wallops().
- Build fix for OS X.
- Fix the autolog_ignore_targets logic to work correctly with manually opened log files (see bug [FS#673](https://github.com/irssi-import/bugs.irssi.org/issues/673 "autolog_ignore_targets affects manually opened logs")).

---

## 0.8.13
{:#v0-8-13 }

The Irssi team released this <abbr class="timeago" title="2009-04-01">2009-04-01</abbr> 

{% include relnews_artef_block.markdown ver="0.8.13" %}

### Additions
{:#v0-8-13-additions }

- Reject some obviously invalid values in /set.
- Add perl bindings for Window::get_history_lines
- Use an io channel to write the config file.
- Use memory slices instead of memory chunks for text buffer.
- Remove methods to create/destroy TextBuffer and TextBufferView and low level api to add/remove lines, scripts should be fine using Window::print_after and TextBufferView::remove_line.
- Add print_after method to Window perl object analogous to gui_printtext_after but which also expands formats and forces a full line.
- Better mapping of signal parameters to Perl. All signals used in scripts now need to be registered with Irssi::signal_register.
- Add public header with interfaces to manage statusbar items (bug [FS#535](https://github.com/irssi-import/bugs.irssi.org/issues/535 "fe-text headers & deal with statusbar in modules"))
- Recode: assume utf-8 encoding for an ascii string in which no escape character occurs (bug [FS#392](https://github.com/irssi-import/bugs.irssi.org/issues/392 "iso-2022 doesn't work with recode_autodetect_utf8")).
- Allow /BAN, /UNBAN, /KICKBAN, /KNOCKOUT if channel is not synced. Requesting ban lists from an unsynced channel will ask them from the server, banning a user whose u@h irssi does not know will ban nick!\*@\* and only bans irssi knows about can be removed.
- Allow storing multiple "other" prefixes such as +q and +a (original patch by JasonX)
- Add /set autolog_ignore_targets for cherry-picking targets that shouldn't get logged.
- Add support for 16 colors. Formats KBGCRMYW and mirc colors are now mapped to colors 8-15. fe-text translates colors 8-15 to bold/blink+0-7 if the terminal supports only 8 colors. If your theme uses one of the high color formats and you really want bold you can change %FMT&lt;string> to %fmt%_&lt;string>%_, it will work fine in all irssi versions.
- Better 005 PREFIX support (bug [FS#580](https://github.com/irssi-import/bugs.irssi.org/issues/580 "005 numeric PREFIX= value not interpreted correctly")).
- Display 407 numerics other than "duplicate channel".
- Fix display of ratbox-style operspy whois.
- Recode outgoing irc away messages (bug [FS#412](https://github.com/irssi-import/bugs.irssi.org/issues/412 "recode not handling users away message")).
- Recode outgoing irc quit messages.
- Remove scrollback_levelclear_levels setting and add a 'level' option to 'sb levelclear' to specify a comma separated list of levels.
- Add perl \_\_WARN\_\_ handler for scripts (bug [FS#427](https://github.com/irssi-import/bugs.irssi.org/issues/427 "warn() in perl script causes screen to distort")).
- Add Irssi::command_parse_options function to parse options for a command.
- Revert recode changes introduced in 0.8.12.
- Add completion for /WINDOW SERVER.
- Support for reading kicks/msgs from TARGMAX/MAXTARGETS 005 tokens.
- Enhancements to the redirections code.
- Support for RPL_WHOISACTUALLY (338 numeric) for both ratbox and ircu (bug [FS#428](https://github.com/irssi-import/bugs.irssi.org/issues/428 "numeric 338 (ircu & ratbox servers)")).
- -idle option of /notify is gone.
- /layout save now makes window-channel bindings instantly effective (bug [FS#35](https://github.com/irssi-import/bugs.irssi.org/issues/35 "/layout save needs changing")).
- /ping without arguments does not send anymore a ctcp ping to a channel (bug [FS#542](https://github.com/irssi-import/bugs.irssi.org/issues/542 "''/ping'' with no arguments CTCP PINGs the channel")).
- Track IRC operator status of nicks a bit better.
- new 'actlist_names' option to add active items names in 'act' statusbar item.
- new 'word_completion_backward' command to scroll backwards in the completion list.
- add 'list' option to /bind to print all the available commands.
- show setter/time in +I lists
- apply -usermode before -autosendcmd (bug [FS#548](https://github.com/irssi-import/bugs.irssi.org/issues/548 "change evaluation order of ''usermode'' vs. ''autosendcmd''")).
- reduce memory usage of the scrollback buffer and make the display in /sb status more accurate (higher).
- fix data getting dropped when a lot is sent at a time (e.g. when attaching to irssi-proxy, bug [FS#528](https://github.com/irssi-import/bugs.irssi.org/issues/528 "irssi-proxy doesn't send all JOIN-commands for server with a lot of open channels")).
- introduce the type Irssi::Irc::Client and signals to communicate with proxy clients to allow for scripting parts of the irssi-proxy.
- Add sb_search.pl, a script for /SCROLLBACK SEARCH

### Fixes
{:#v0-8-13-fixes }

- Fix /NOTIFY list when nick is seen joining (bug [FS#642](https://github.com/irssi-import/bugs.irssi.org/issues/642 "the notify list is broken")).
- Include hostmask in 001 event sent by proxy (bug [FS#650](https://github.com/irssi-import/bugs.irssi.org/issues/650 "irssi proxy does not send a conform RPL_welcome")).
- Be more power-friendly: don't run any always-on &lt;1s timers (bug [FS#641](https://github.com/irssi-import/bugs.irssi.org/issues/641 "irssi causes several CPU wakeups per second when completly idle")).
- Don't get confused by a failed /JOIN -window (bug [FS#644](https://github.com/irssi-import/bugs.irssi.org/issues/644 "/wjoin bug")).
- Properly initialize embedded Perl (PERL_SYS_INIT3).
- Replace invalid utf-8 bytes with U+FFFD when drawing a line.
- Properly unload the original script when using /script load to reload it. (bug [FS#525](https://github.com/irssi-import/bugs.irssi.org/issues/525 "Irssi doesnt properly release subrefs on double script load"), patch by Lukas Mai)
- Clean up script loading in general:
   * Don't leak local variables to eval'd code.
   * Set filename/line number to get better error messages from perl.
   * Use three-arg open and lexical filehandles to avoid surprises.
   * Include error reason in message for unopenable scripts.
   * Don't wrap script code in sub handler { } - this avoids spurious warnings and
     should at least allow \_\_END\_\_ to work properly. (Patch by Lukas Mai)
- Fix NETSPLIT_SERVER_REC in signals for Perl.
- Remove buggy /SCROLLBACK redraw and /SET scrollback_save_formats.
- Always preserve the active mainwindow when resizing.
- Ignore DNS not found errors when considering reconnect.
- Do not strip the comma in a mirc color if it is not followed by a digit (bug [FS#250](https://github.com/irssi-import/bugs.irssi.org/issues/250 "commas in colored messages")).
- Fix building perl module with perl-5.10 (bug [FS#630](https://github.com/irssi-import/bugs.irssi.org/issues/630 "irssi fails to build with perl")).
- fix leak with $L expando.
- fix possible crash with /script reset.
- ignore exceptions take precedence over ignores in all cases.
- honour -channels preference for ignore -replies (bug [FS#227](https://github.com/irssi-import/bugs.irssi.org/issues/227 "ignore -replies -channel ignores replies in wrong channel")).
- Fix mode display in whois with unreal (379 numeric) (bug [FS#479](https://github.com/irssi-import/bugs.irssi.org/issues/479 "IRSSI fails to format the whois info and therefor fails to display usermodes on Unreal")).
- Fix regressions that prevented external modules from building/working (bugs [FS#537](https://github.com/irssi-import/bugs.irssi.org/issues/537 "Removal of irssi-config.in breaks irssi-icb") [FS#539](https://github.com/irssi-import/bugs.irssi.org/issues/539 "fix for segfault with non-IRC protocols")).
- Fix /set hilight_level not taking effect immediately (bug [FS#598](https://github.com/irssi-import/bugs.irssi.org/issues/598 "hilighting not triggered in a /msg window")).
- Fix bold, blinking and indentation in /LASTLOG and buf.pl.

---

## 0.8.12
{:#v0-8-12 }

The Irssi team released this <abbr class="timeago" title="2007-10-06">2007-10-06</abbr> 

{% include relnews_artef_block.markdown ver="0.8.12" %}

### Additions
{:#v0-8-12-additions }

- Some changes to character set recoding.
- Rewrite SSL connection/handshake code.
- Remove support for glib 1.x.
- Do not send our hostname to the server (bug [FS#488](https://github.com/irssi-import/bugs.irssi.org/issues/488 "[PATCH] Privacy fix for USER message")).
- Add $tag to 'window' item in default configuration.
- Pick up host changes on charybdis and ircu servers (396 numeric).
- Show various errors such as "cannot send to channel" and "cannot /msg, user is +g" in the channel or query window, if possible, and always include the user or channel name.
- Channel forwarding in hyperion and charybdis is now recognized (470 numeric) and the target channel is joined in the window where the original channel would have been joined.
- Add support for the ACCEPT command, which is part of the CALLERID server side ignore system in hybrid7 and derived ircds.
- Make /WINDOW GOTO start searching at the window after the active one and stop at the one before (bug [FS#332](https://github.com/irssi-import/bugs.irssi.org/issues/332 "want /win goto <nick│channel> to start searching *past* current window")).
- Improve completion for /SET.
- Use CASEMAPPING dependent comparison to match channel names. Patch by Jon Mayo (bug [FS#436](https://github.com/irssi-import/bugs.irssi.org/issues/436 "irc-style case-insensitivity does not work for channel names")).
- Various improvements to the help files.
- Add Perl bindings for some gui_entry methods
- Make alt/meta+arrow keys work in recent versions of xterm (bug [FS#496](https://github.com/irssi-import/bugs.irssi.org/issues/496 "Alt+cursor keys do not work in recent xterm"))

### Fixes
{:#v0-8-12-fixes }

- Fix DCC get when file size is 0 (bug [FS#494](https://github.com/irssi-import/bugs.irssi.org/issues/494 "dcc stalled forever when sending 0kB files")).
- Ignore empty lines when pasting.
- Fix large file support on AIX (bug [FS#404](https://github.com/irssi-import/bugs.irssi.org/issues/404 "Large File Support on AIX")).
- Remove broken code that prevents unloading of a script in some cases.
- Fix logging lines with no target to all logs, broken in 0.8.11.
- Fix casemapping dependent nick and channel matching (bug [FS#436](https://github.com/irssi-import/bugs.irssi.org/issues/436 "irc-style case-insensitivity does not work for channel names")).
- Update chanop flag before emitting nick mode changed signal (patch by Johan Kiviniemi)
- Fix recognition of realnames starting with spaces in /WHO.
- Show "Target left IRC" error messages fully (instead of reporting no such nick "*")
- Repair channels_rejoin_unavailable. Enabled by default, this retries joins that failed because of netsplits (channel temporarily unavailable (437), duplicate channel). A few servers abuse 437 for juped channels which should not be retried, you should disable channels_rejoin_unavailable if this is a problem.
- Display 437 and 407 numerics if channels_rejoin_unavailable is not enabled (bug [FS#495](https://github.com/irssi-import/bugs.irssi.org/issues/495 "No info in status window when joining channel that is temporary unavailable (due to split)")).
- Don't add the same mask to the /KNOCKOUT list multiple times (bug [FS#510](https://github.com/irssi-import/bugs.irssi.org/issues/510 "/knockout removes bans that don't exist")).
- Use MSGLEVEL_NICKS again for printing a nick change in queries, broken in r2389.
- Fix some /LASTLOG -before/-after issues.
- Some fixes to the build system.
- Fix paste sending the first line twice (bug [FS#405](https://github.com/irssi-import/bugs.irssi.org/issues/405 "Multiline paste duplicates the first line"))
- When parsing a numeric option verify that the whole argument, rather than only the first character, is numeric.
- Some fixes for notices, actions and ctcps to @#channel and +#channel (bug [FS#46](https://github.com/irssi-import/bugs.irssi.org/issues/46 "msg/notices to prefixes (eg /msg +#chan) goes to status"))

---

## 0.8.11
{:#v0-8-11 }

The Irssi team released this <abbr class="timeago" title="2007-04-25">2007-04-25</abbr> 

{% include relnews_artef_block.markdown ver="0.8.11" %}

### Additions
{:#v0-8-11-additions }

- Add completion for /WINDOW GOTO
- New crapbuster-like "scrollback levelclear" command
- irssi now aborts a connection when, on an attempt to connect, the server returns code 432 (Erroneous Nickname), bug [FS#425](https://github.com/irssi-import/bugs.irssi.org/issues/425 "irssi is trying to change the nick to a valid one all the time tho the prefix isn't valid")
- Allow identifiers in config file to start with a digit, bug [FS#177](https://github.com/irssi-import/bugs.irssi.org/issues/177 "problems parsing config with network name like 123test").
- Modify Irssi::UI::Window::command to restore the original active window only if the command executed has not made another one active, bug [FS#403](https://github.com/irssi-import/bugs.irssi.org/issues/403 "Irssi::active_win()->command is not working properly").
- Make awaylog_file respect \-\-home, bug [FS#304](https://github.com/irssi-import/bugs.irssi.org/issues/304 "awaylog_file should default to dir specified with --home")
- Send /QUOTE immediately if server didn't send the 001 event yet
- If dcc_own_ip contains IPv4 address, listen only in IPv4
- Negative scroll_page_count scrolls screensize-n lines (Patch by Chris Moore)
- Sort nicks with custom prefix by the order defined in isupport in /NAMES
- New perl command send_raw_first, patch by ComradeP (Bug  [FS#413](https://github.com/irssi-import/bugs.irssi.org/issues/413 "Patch for new scripting command (send_raw_first)"))
- Let the module loader also check for fe_common_$protocol files
- Don't wait for all /NAMES replies before syncing if we can't combine queries anyways (Patch by jilles)
- Renamed irc.efnet.net to irc.efnet.org
- /SCROLLBACK CLEAR accepts the same arguments as /CLEAR
- Check if binary exists and can be executed before /UPGRADE
- Change default value of override_coredump_limit to OFF
- UPTIME command by Lauri Nurmi with some modifications (Bug  [FS#458](https://github.com/irssi-import/bugs.irssi.org/issues/458 "The /UPTIME alias does not work on Solaris and others + PATCH"))
- Remove CR and LF from Perl commands, to make it harder to introduce a security bug
- Remove bookmark on a line when line is removed (instead of moving it)
- Don't fallback to generic word completer if the command specific completion list is not empty.
- Recognize cursor left and cursor right sequences sent by recent xterm

### Fixes
{:#v0-8-11-fixes }

- Fix some UTF-8 issues, bugs [FS#452](https://github.com/irssi-import/bugs.irssi.org/issues/452 "Overlong topic/statusbar item (with wide character on the margin) issue") (Patch by Yi-Hsuan Hsin), [FS#459](https://github.com/irssi-import/bugs.irssi.org/issues/459 "Backspacing combining mark doesn't clear it"), [FS#460](https://github.com/irssi-import/bugs.irssi.org/issues/460 "Irssi lets (UTF-8 encoded) C1 control chars thru to terminal in UTF-8 mode")
- Fixed segfault on quit introduced in 0.8.10
- Fixed a bug where tab-completion didn't work with utf8/big5 properly
- Ignore joins without a nick from broken servers
- Fix whois_hide_safe_channel_id: only look at the beginning of a channel name, not in the middle
- Don't assume that 7bit ascii strings are encoded in UTF-8, only validate the strings when they contain octest with highest bit set (patch by Mikko Rauhala)
- Make random really random when resolving
- Don't get confused by a join command with too many arguments, keys can't have spaces in them (Bug  [FS#437](https://github.com/irssi-import/bugs.irssi.org/issues/437 "Possible channel status bug"))
- Don't crash on /QUIT with scripts causing and catching signals on UNLOAD
- Fix %k and %K mappings in curses frontend
- Fix bold on monochrome terminals in terminfo frontend
- Fixed colors with TERM=xterm-{88,256}color in terminfo frontend
- Fix crash with one line high terminal in terminfo frontend
- Fix building with srcdir != builddir
- Don't get confused and keep saying "Netsplit over" on every join for user that only rejoined some channels
- Fix crash in /EXEC (Bug  [FS#439](https://github.com/irssi-import/bugs.irssi.org/issues/439 "irssi crash when using /exec (patch included)"))
- Fix format string in printtext_dest call from Perl, patch by loafier
- Fix memory leaks in expandos_deinit by Nicolas Collignon (Bug  [FS#419](https://github.com/irssi-import/bugs.irssi.org/issues/419 "memory leak"))
- Detect off_t size using AC_CHECK_SIZEOF because it works also when cross-compiling in autoconf-2.50 and higher
- Fix failed assertion when the config file is unreadable, patch by Daniel Koning (Bug  [FS#164](https://github.com/irssi-import/bugs.irssi.org/issues/164 "failed assertion in config_parse()"))
- Removed automatic glib downloading and compiling.
- Fix /FORMAT -delete daychange so it doesn't print an empty line
- Forbid /WINDOW SHOW when the target window is sticky rather than when there is a window bound to the container of the target window.
- Improve interaction between autolog and non autolog logs
- Recognize local oper mode on ircnet (mode +O)
- Properly initialize reference count for a new setting (Bug [FS#235](https://github.com/irssi-import/bugs.irssi.org/issues/235 "Irssi::settings_remove doesn't remove settings"))

---

## 0.8.10
{:#v0-8-10 }

The Irssi team released this <abbr class="timeago" title="2005-12-11">2005-12-11</abbr> 

{% include relnews_artef_block.markdown ver="0.8.10" %}

### Changes
{:#v0-8-10-changes }

- Long delayed release, with lots of changes. Most important ones:
    + Recode support, by decadix and senneth
    + isupport (005 numeric), by David Leadbeater
    + Passive DCC support, by Francesco Fracassi
    - Many memleak fixes, by Toby Peterson

### Additions
{:#v0-8-10-additions }

- Moved to subversion
- /SET paste_join_multiline ON - When paste detection is enabled and you paste lines which look like they're being copy&pasted from irssi itself, it attempts to merge lines said originally in a single line.
  
  How this really works is that all indented lines must have the same amount of indentation. Indented lines are merged to last unindented line. If line gets longer than 400 characters, it's split.
- /SET whois_hide_safe_channel_id ON - Hides the channel ID prefix of !channels in WHOIS replies
- When reconnecting to server, say that it can be aborted with /RMRECONNS
- /WHOIS -&lt;server tag> is supported now
- /SET whois_hide_safe_channel_id - removes the ugly IDs for !channels in /WHOIS (default)
- If we can't connect to server using given own IP, show the IP to user in the error message. Should help figuring out wrong /SET hostname or /SERVER -host settings.
- If channel has more nicks than /SET channel_max_who_sync, don't ask /WHO list to avoid getting kicked out of server (Max SendQ exceeded).
- /LOAD script.pl loads the perl script
- /IGNORE -network ignores only on specified network
- /SET use_status_window and /SET use_msgs_window make the effects immediately
- Changed the confusing "ircnet" to "network" everywhere
- Don't autoget files sent to channels, unless dcc_autoget_masks is set
- Added a default "*" target which matches everything on the server, including NULL items associated with it, by jimmy
- /UPGRADE now saves server->version
- If available, send who set topic and when to irssi-proxy clients
- Cleaned up network list: removed smaller networks, added QuakeNet
- New default aliases: MANUAL-WINDOWS, EXEMPTLIST and ATAG
- Recode support: /RECODE for manipulation of the conversion database. Setting "term_type" has been renamed to "term_charset". /SET recode OFF to disable recode completely. /SET recode_out_default_charset &lt;charset> to specify the default outgoing charset. /SET recode_fallback &lt;charset> to specify a charset that will be used when the normal conversion is failing. /SET recode_transliterate ON to enable character transliteration, so unavailable characters will be transliterated into something readable &lt;charset> can be almost everything listed by 'iconv -l'
- Added transpose_words, capitalize_word, downcase_word, upcase_word key bindings
- Avoid accidentally /VER in a channel, by requiring parameter

### Fixes
{:#v0-8-10-fixes }

- Pasted lines weren't added to command history. Some other paste detection fixes
- Fixed /BIND escape_char
- Fixes for Chinese multibyte characters handling and cursor movement by Wang WenRui
- Pasting multibyte chars was buggy, patch by Kuang-che Wu
- Fixed handling WHOIS printing once and for all. Everything unknown between "beginning of whois" and "end of whois" events is now printed as whois_special. Removed whois_registered and whois_help, they're printed with whois_special as well.
- Don't replace channel key when receiving channel mode numeric. It could be a fake key there.
- Don't crash if dcc chated user changes nick
- Help files are always lowercased. Make sure /HELP COMMAND works too.
- /EXEC crashed with 64bit systems. Patch by Soren Jacobsen
- Handle 432 numeric (errorneus nickname) as "nick in use". Fixes problems with ircnet 2.11 ircd when irssi tries to reconnect using UID as nick. Patch by Petr Baudis
- /SET -default fixes
- /DCC SEND didn't actually use /SET dcc_upload_path
- Fixed /WHOIS -yes (Bug  [FS#67](https://github.com/irssi-import/bugs.irssi.org/issues/67 "-YES argument"))
- Make /JOIN -tag #channel and /JOIN #channel&lt;space> switch to that channel (Bugs  [FS#13](https://github.com/irssi-import/bugs.irssi.org/issues/13 "'/join -tag #channel' does not forward like '/join #channel'") and [FS#93](https://github.com/irssi-import/bugs.irssi.org/issues/93 "/join #channel<space> doesn't work (when switching channels)"))
- Fixed readded (changed) hilights being in config twice, resulted in duplicate hilights or removed hilights coming back (Bug  [FS#39](https://github.com/irssi-import/bugs.irssi.org/issues/39 "Duplicate hilight entries are saved to config file"))
- Fixed messages to @#channel showed **your** nickmode, not the one of the sender (part of Bug  [FS#80](https://github.com/irssi-import/bugs.irssi.org/issues/80 "@#channel and +#channel messages are printed badly"))
- Fixed /KNOCK support
- Fixed own nick changes in irssi-proxy
- Fixed /HILIGHT -actcolor -mask (Bug  [FS#131](https://github.com/irssi-import/bugs.irssi.org/issues/131 "Hilight, -actcolor doesn't work with -mask"))
- Recognise a param of signal_emit/continue in perl script if it's int
- Fixed bug 120 where proxy doesn't set the server_rec->away_reason
- Fixed /join -invite -window bug if there is no invite
- Fixed bug with time settings where hours actually returned 60*hours
- Fix multiple entries for local IP in /etc/hosts prevents connecting, patch by eridius (Bug  [FS#167](https://github.com/irssi-import/bugs.irssi.org/issues/167 "multiple entries for local IP in /etc/hosts prevents connecting"))
- Fixed a bug with /me, use the right arguments for "message irc own_action"
- Update our own nickrec->gone flag on /away &lt;reason> or on /away
- Fixed output of /hilight (add a space after -levels if any)
- Add libtool's -module flag to get built properly on all platforms, by Toby Peterson (Bug  [FS#212](https://github.com/irssi-import/bugs.irssi.org/issues/212 "modules (proxy, perl) built incorrectly [PATCH]"))
- Don't apply emphasis on _foo_^ if it's a nick (Bug  [FS#52](https://github.com/irssi-import/bugs.irssi.org/issues/52 "Underline bug on nicks"))
- Fix displaying of ctcp userinfo and clientinfo (Bug  [FS#222](https://github.com/irssi-import/bugs.irssi.org/issues/222 "irssi doesn't show ctcp userinfo requests"))
- Remember alternate_nick and max_whois on reconnect (Bug  [FS#181](https://github.com/irssi-import/bugs.irssi.org/issues/181 "server->connrec->alternate_nick not carried between reconnects"))
- Fix tr_TR locale problem for glib2 (still a bug with glib1.2) by David Pashley
- Fixed pasting not using the character translation (Bug  [FS#151](https://github.com/irssi-import/bugs.irssi.org/issues/151 "[PATCH] translate characters at paste"))
- Fixed a bug where the channel list to join/rejoin on reconnect gets too long, not all channels will be joined. (Bug  [FS#108](https://github.com/irssi-import/bugs.irssi.org/issues/108 "not rejoining all channels because line too long"))
- Print glib errors nicely, by David Pashley
- Handle ^Z better, by David Pashley
- Fixed /eval recursion crashing, by David Pashley
- Fix notify with more nicks than max_whois_in_cmd (Bug  [FS#257](https://github.com/irssi-import/bugs.irssi.org/issues/257 "issues with notify in irssi 0.8.10-rc4 (20040324 1731)")), based on patch by Krzysztof Kowalik (Borys)
- Fixed irssiproxy sometimes missing (parts of) lines
- Fixed remote /WHOWAS
- Parse negative time setting values, makes it possible again to do /SET server_reconnect_time -1 to disable reconnecting
- Compile with gcc4
- Compile with readonly srcdir
- Fixed crash if receiving broken privmsg without source (which bitlbee can send if you msg yourself)
- Fixed crash with invalid TERM and termcap
- When looking up IP addresses, return random IP instead of the first one

---

## 0.8.9
{:#v0-8-9 }

Timo Sirainen released this <abbr class="timeago" title="2003-12-11">2003-12-11</abbr> 

{% include relnews_artef_block.markdown ver="0.8.9" %}

### Changes
{:#v0-8-9-changes }

- Fixes a remote crash with:
    a) non-x86 hardware (one requiring memory alignmentation)
    b) script using "gui print text" signal (with x86 hardware too)

### Additions
{:#v0-8-9-additions }

- /SET auto_whowas OFF allows now disabling automatic /whowas when /whois doesn't find a nick (by Borys)

### Fixes
{:#v0-8-9-fixes }

- If pasted line starts with command char, treat it as command always. Paste detection can go on too easily with lagged connections.

---

## 0.8.8
{:#v0-8-8 }

Timo Sirainen released this <abbr class="timeago" title="2003-11-23">2003-11-23</abbr> 

{% include relnews_artef_block.markdown ver="0.8.8" %}

### Fixes
{:#v0-8-8-fixes }

- Just a few fixes to converting old settings automatically

---

## 0.8.7
{:#v0-8-7 }

Timo Sirainen released this <abbr class="timeago" title="2003-11-23">2003-11-23</abbr> 

{% include relnews_artef_block.markdown ver="0.8.7" %}

### Changes
{:#v0-8-7-changes }

- Settings changes - we have now "time", "size" and "level" setting types.
    - Level settings should work the same as before.
    - Time settings can have units: days, hours, mins, secs,
      milliseconds (or msecs). The units can be combined and written
      in shorter form as well, for example "5d 30m 10ms"
    - Size settings can have units: gbytes, mbytes, kbytes, bytes.
      They can be written in shorter form as well, eg. "gb" or "g".
  
  Your existing settings should be converted automatically.

### Additions
{:#v0-8-7-additions }

- Pasting detection. All keys except CR and LF are pasted as-is into prompt in pasting mode.
  
  /SET paste_detect_time controls how closely each others characters must occur for it to be considered pasting. Paste mode goes on when first pasted CR/LF is found.
  
  The first line may also contain some command characters. They are executed, but their action in entry line is reverted once pasting is detected.
  
  What this means in practise is that even if you have TABs (assuming TAB is completion key) in the first pasted line, they get pasted as TABs.
  
  This detection isn't perfect, so if it annoys you it can be disabled with /SET paste_detect_time 0
- If pasting more lines than /SET paste_verify_line_count, irssi asks if you actually want to do that. This should be useful to prevent accidental copy&paste mistakes. Setting it to 0 disables this entirely.
- Support for sending SSL certificate to server and optionally verify server's certificate. See the -ssl_* options for /SERVER and /SERVER ADD. Patch by Joel Eriksson.
- DCC SERVER support by Mark Trumbull
- Support for DCC sending larger files than 2GB if supported by operating system (ie. 64bit file support). Receiving has always been possible, but the statistics were wrong with >4GB files if 64bit support isn't enabled.
- Better displaying of DCC file transfer statistics.

### Fixes
{:#v0-8-7-fixes }

- Several other minor fixes and enhancements, see ChangeLog

---

## 0.8.6
{:#v0-8-6 }

Timo Sirainen released this <abbr class="timeago" title="2002-11-17">2002-11-17</abbr> 

{% include relnews_artef_block.markdown ver="0.8.6" %}

### Changes
{:#v0-8-6-changes }

- Tons of changes, here's only the largest that come to my mind now:

### Additions
{:#v0-8-6-additions }

- SSL support by vjt@users.sf.net
- DCC send queues by Heikki Orsila
- Better support for !channels

---

## 0.8.4
{:#v0-8-4 }

Timo Sirainen released this <abbr class="timeago" title="2002-03-13">2002-03-13</abbr> 

### Changes
{:#v0-8-4-changes }

- Continuing to fix my stupid mistakes...

### Fixes
{:#v0-8-4-fixes }

- When a queried nick did a nick change, it might have crashed irssi
- read ChangeLog for some other minor changes

---

## 0.8.3
{:#v0-8-3 }

Timo Sirainen released this <abbr class="timeago" title="2002-03-13">2002-03-13</abbr> 

### Fixes
{:#v0-8-3-fixes }

- Perl scripts handling channel parts/kicks/quits printed some errors.
- Connecting to IPv6 servers without IPv4 record didn't work
- When queries were auto-created by you using /MSG and you had /SET autoclose_query non-zero, the query was always destroyed almost immediately.
- Fix to some stupid ircds not sending us 001 numeric, but beginning from MOTD

---

## 0.8.2
{:#v0-8-2 }

Timo Sirainen released this <abbr class="timeago" title="2002-03-11">2002-03-11</abbr> 

### Changes
{:#v0-8-2-changes }

- Changed the list of scripts distributed with irssi. Separated example scripts to scripts/examples/ directory.
- Hated infobar was removed, the same info is now in topicbar in empty windows. I don't think it would disturb anyone in there. If you still preferred always-empty topicbars, use /SBAR topic REMOVE topic_empty

### Additions
{:#v0-8-2-additions }

- Added info_eol field to theme. If true, timestamp and server tag are added to end of line, not at beginning.
- If -4 or -6 option is used with /SERVER, irssi now forces the connection using the given protocol or fails.
- /SET max_wildcard_modes (default 6) - if a wildcard to /OP, /DEOP, /VOICE or /DEVOICE matches more nicks than this, -yes option is required. This is trying to prevent accidental massops. Setting it to 0 disables this check.
- Supports now correctly servers which use '.' char as channel owner character in /NAMES list. Also supports multiple mode chars, eg. @+nick (if some server actually used it).
- Never ignore kick message if you get kicked from channel.
- Sending irssi SIGHUP now does a /RELOAD - useful if you accidentally messed up something which doesn't let you do the /RELOAD inside irssi (eg. /SBAR prompt DISABLE).
- irssi-proxy: PROXY CTCP ON\|OFF - proxy clients can send this command to specify that they want to handle the received CTCP requests. Useful for specifying who gets to handle DCCs.
- Added escape_char /BIND command. The next char after that would be added as-is to input line.

### Fixes
{:#v0-8-2-fixes }

- Writing lines longers than 1024 chars to input buffer crashed irssi (stupid missing sizeof() bug :)
- Some UTF-8 fixes
- Better flood protection for lines with >100 chars
- Control characters aren't printed as-is in topicbar (or statusbars in general) anymore
- /OPER can be now aborted by giving empty password
- Netjoin messages were buggy in +channels
- Part message parameter for /CYCLE was never used.
- Don't send -autosendcmd after /UPGRADE.
- /SET autoclose_query - now only last received private message affects when the query is closed, ie. /WHOIS requests or nick changes don't reset the counter.
- Foreground ANSI colors weren't working
- Deleting one character replaced cutbuffer with that character. Also ^Y leaked memory.
- /SCRIPT LOAD looked scripts from prefix/lib dir, not prefix/share where they were actually installed.
- Highascii chars in replaces block in theme files could have crashed irssi.

---

## 0.8.1
{:#v0-8-1 }

Timo Sirainen released this <abbr class="timeago" title="2002-02-17">2002-02-17</abbr> 

### Changes
{:#v0-8-1-changes }

- Expected bugfix release :) Worst thing was that I forgot always to debug why /cat /dev/urandom crashed irssi. Well, found two ways that could make it happen.

### Fixes
{:#v0-8-1-fixes }

- Irssi was linked with -lcurses AND -lncurses
- Logging could have produced GLib errors with certain conditions
- A few compiler warnings fixes

---

## 0.8.0
{:#v0-8-0 }

Timo Sirainen released this <abbr class="timeago" title="2002-02-17">2002-02-17</abbr> 

### Changes
{:#v0-8-0-changes }

- I really should make releases more often. Once in every two weeks used to be nice. Maybe once in a month would be good now. There was many reasons why this release took this long .. first being addicted to books, then life stuff, then it took forever to figure out that irssi was crashing under solaris (and not because of one of the big changes I made while moving to IRC from solaris box).
  
  And now.. well, after this release I'll start working more with the yet another irssi rewrite :) The code is getting too ugly again, and some things need rewriting to support some new features more easily. It will take a while to get it all done, so I'll try to keep updating this "stable" irssi as well.
  
  There's too many changes since 0.7.98.3 (and .4 which was just minor bugfix), about 6600 lines in ChangeLog. I'm not going to read all that, so I'll just list the biggest changes that I can remember now.
  
  This version was supposed to be called 0.7.99, but since there were so many changes, and I originally though of putting 0.8.0 out long time ago, and 0.7.100 would look stupid, I guess it's time for 0.8.0 :)

### Additions
{:#v0-8-0-additions }

- /UPGRADE - upgrade irssi to new version on-the-fly without disconnecting from server, so other people won't even notice you quit from IRC. This ONLY executes the new binary, it does NOT download/compile/whatever irssi.
- UTF-8 support with /SET term_type UTF-8, default is "8bit". It's also automatically detected from system locale (if supported).
- Fully configurable statusbar. Yes. FULLY. Don't bother asking if something could be done with it, it can, just ask how. Well, there's a few things I didn't have time/energy to finish: window-specific statusbar groups and support for multiple input lines in screen.
- Rewritten keyboard handling. No more the CTRL-X and ALT-x handling, now you can create whatever keyboard combinations your terminal can send to irssi.
- Rewritten text buffer (scrollback) handling.
- Irssi doesn't depend on curses anymore, so it can be installed anywhere a working terminfo/termcap exists. This also allows us to use all the possible colors terminal has (curses limits to 64), so eg. %0 is now always black background, not the default terminal background (%n).
  
  Several systems have also terminfo/termcap database that doesn't support colors, so I've added /SET term_force_colors option to force ANSI-style colors. Note that eg. BitchX does this by default.
  
  Getting rid of curses allows also one great thing for you people copy&pasting long urls :) If a long word gets split to two lines, doubleclicking the word selects it from both lines.
- Rewritten server event redirections. Before it was pretty easy to mess up irssi's expectations of what server sends, and some things might have stayd in the buffer forever. Especially notify lists messed up /WHOIS requests for the notified people. Now all this should be history and it's a lot easier for scripts to use the redirections as well.
- New ICB chat protocol plugin - very basic and doesn't support nicklist, but works. :)
- \-\-home and \-\-config parameters to specify alternate ~/.irssi directory or config file.
- Scripts can be unloaded separately with /SCRIPT UNLOAD. You can get a list of runnning scripts with /SCRIPT.
- /SERVER PURGE [&lt;target>] - purge the output buffer (for given target). Useful for example if you accidentally paste 100 lines :) The buffer is automatically purged if you get kicked from channel, or if you /PART the channel and there's more than 10 lines in output buffer.

---

## 0.7.98.3
{:#v0-7-98-3 }

Timo Sirainen released this <abbr class="timeago" title="2001-03-17">2001-03-17</abbr> 

### Changes
{:#v0-7-98-3-changes }

- Highlighting changes: /HILIGHT -color, /SET hilight_color and /SET hilight_act_color don't accept the numeric color value anymore, the colors must be the %code format (see the beginning of docs/formats.txt). The color can also have background and underline/blinking set (%F%Y = blinking yellow)
- Statusbar rewrite: Statusbar should finally work well when there's not enough space for it in screen. Least important items start shrinking/disappearing before more important ones, activity list should be always fully visible now.
  
  /SET statusbar_xxx settings have been removed, everything is configurable from theme now. Even the texts in the statusbar items. See end of default.theme.
  
  FULLY configurable statusbar with possibility to create your own items and support for multiple lines will hopefully come soon.

### Additions
{:#v0-7-98-3-additions }

- /WINDOW CLOSE [&lt;first> [&lt;last>] - you can close multiple windows at once now.
- Emphasis work with actions now
- If there's any unknown settings in your configuration file, irssi asks at startup if they should be removed.
- All abstracts in theme files now default to same as in default.theme, so you may override only those you want to change leaving the rest commented out.

### Fixes
{:#v0-7-98-3-fixes }

- Irssi crashed when specifying vhost to use (not always?)
- Fixed one nasty usage of already free'd memory. Hopefully solves some weird crashes?
- Some perl fixes, Irssi::Nick and "massjoin" signal didn't work properly which broke all auto-op scripts.
- If one server fails because of DNS error, don't stop reconnecting to entire chatnet.
- Updated default config to have max_query_chans=1 in undernet to avoid those channel syncing problems.
- /SERVER didn't autojoin channels if it was used when you weren't connected to any other servers
- /CONNECT -ircnet didn't load ircnet specific settings correctly
- /SET scroll_page_count - don't crash if /0 is given. Works now properly if /0.xx is given.
- ^O did reset only colors, not underlines etc.
- Several fixes with handling blinking text
- Irssi crashed almost immediately with NetBSD/Alpha, fixed. Still not sure if it was compiler bug or is my code just non-standard C.
- Reconnecting in IPv6 server shouldn't change to IPv4
- Irssi proxy didn't work properly with systems where irssi was compiled with \-\-enable-ipv6 but OS didn't support IPv6

---

## 0.7.98.2
{:#v0-7-98-2 }

Timo Sirainen released this <abbr class="timeago" title="2001-03-04">2001-03-04</abbr> 

### Additions
{:#v0-7-98-2-additions }

- /LASTLOG: added -case option for case-sensitive matching. -force option is now required to print lastlogs longer than 1000 lines.
- /BANTYPE -> /SET ban_type. /BAN: -type option added to override default ban type.
- /NAMES: -ops -halfops -voices -normal options added. /NAMES without parameters now prints nicklist in active channel, /NAMES ** shows all nicks in all channels.
- delete_next_word key implemented, patch by Tinuk
- /SET beep_when_window_active - works with /SET beep_msg_level, should we beep when the msg is printed to active window. If msg is printed to some other window it always beeps.
- /JOIN #channel and /QUERY nick won't anymore automatically move channel/query to active window but send a notice to user how to move it. This was confusing people who did it accidentally.
- /SET autostick_split_windows (default ON) - should we do /WINDOW STICK ON to all new split windows and hidden windows that are created inside it. This hopefully makes it easier to use split windows.

### Fixes
{:#v0-7-98-2-fixes }

- All IPv6 problems are hopefully fixed. Everything now keeps both v4 and v6 addresses in memory and at connect() time it's decided which one should be used.
- /IGNORE * level printed GLib error. /RELOADing printed some unignore texts. Autoignores had some problems.
- Using /LAYOUT SAVE with split windows crashed irssi at startup when it tried to restore them..
- /WINDOW SHOW command didn't work properly
- /LAST -clear crashed if window contained only lastlog lines. Beeping after /LAST -clear also could have crashed.
- HILIGHT level didn't work with logs.
- /SET prompt - if $T (target) had %c or something in it, it shouldn't be treated as color code. So color codes can now be used in /SET prompt string itself, but in none of the $variables it uses.
- Generated help files had joined lines in chapter together but didn't add spaces between lines.
- Statusbar could have gotten to endless loop when trying to give more space to some item when there was no more available space.
- When /SET autoclose_windows is ON, don't destroy windows if they have some level set (like /join -w + /part in status window)
- If GLIB was unpacked to irssi directory, make install tried to install it also.
- Always save theme to ~/.irssi/ no matter where it was read from.
- If /SET names_max_width was too low, irssi crashed
- /CONNECT -ircnet "" - even if someone does this don't make the server tag empty :)
- /QUERYing #channel that was already /JOINed crashed irssi after a while
- /SET -clear printed GLib error when done to boolean settings

---

## 0.7.98.1
{:#v0-7-98-1 }

Timo Sirainen released this <abbr class="timeago" title="2001-02-22">2001-02-22</abbr> 

### Fixes
{:#v0-7-98-1-fixes }

- fixed stupid remote crash with nick_match_msg()

---

## 0.7.98
{:#v0-7-98 }

Timo Sirainen released this <abbr class="timeago" title="2001-02-22">2001-02-22</abbr> 

### Changes
{:#v0-7-98-changes }

- Theme files aren't fully compatible with old ones, there's a few naming changes and some new items. Added lots of comments and help to default.theme, so creating themes should be a bit easier now :)
- Perl scripts aren't compatible with old ones anymore. Biggest change is that $object->values()->{xxx} calls are now just $object->{xxx}, but there's a lot of other changes as well. docs/perl.txt is now up to date so you may want to read it.
- Several settings have changed their names:
    /SET beep_on_msg -> beep_msg_level
    /SET activity_levels -> activity_msg_level
    /SET hilight_levels -> activity_hilight_level
    /SET noact_channels -> activity_hide_targets

### Additions
{:#v0-7-98-additions }

- /SET prompt, /SET prompt_window - Specifies the text in prompt. 'prompt' is used when channel or query is active in window and 'prompt_window' is used with empty windows. You can also use % color codes in prompt.
- /EXEC - rewrote it, has now all the same features as EPIC and a few more, like "interactive shell in window" support. See /HELP exec for information.
- /SAVEWINDOWS renamed to /LAYOUT SAVE. Added /LAYOUT RESET. /LAYOUT SAVE now saves split windows and queries properly. Windows that contain saved channels are never used for anything else (ie. if the saved channel isn't joined, no other channels can be joined to the window)
- /WINDOW SERVER: added -sticky and -unsticky options. If window server is sticky, it will never be automatically changed, and it cannot be changed to anything else without -unsticky option. Should be useful for people who want status or msgs windows for each server.
- /WINDOW STICK [ON\|OFF\|&lt;ref#>] - stick window to specified split window. After setting window to sticky non-sticky windows can't replace the active sticky one. Each split window can have it's own sticky window group.
- /WINDOW LEFT, /WINDOW RIGHT - Go to previous/next window in the current sticky window group, or if there's no sticky windows go to previous/next non-sticky window. Alt-Left/Right keys default to these commands now.
- /WINDOW NUMBER: -sticky option added. Closing windows before a sticky window won't change refnum of the sticky window and windows after it.
- /SET windows_auto_renumber - should window refnums be packed when some window is destroyed in the middle
- /SET scroll_page_count - how many lines to scroll with pgup/pgdn. either an absolute value, or if the count starts with '/', it's calculated as lines_in_screen/count. The default is /2.
- /SET timestamp_format specifies the format to use with timestamps in "man strftime" format.
- Emphasis (**word**, _word_) replacing works better now. It doesn't try to change nicks or any non-words. This time people might want to actually use it :)
- Nick completion logic changes, should work better now. Changed meaning of /SET completion_keep_publics to be number of publics to keep instead of time to keep them.
- /HILIGHT: Added -priority option (deciding which color should stay in activity list), /SET hilight_level to specify the default level for /HILIGHTs. -word option renamed to -full. Added new -word option meaning to highlight only the found word in line. Removed -nonick option but added -line which means pretty much the same. -actcolor specifies what color to show in activity list, default is the same as -color or if there's no -color it defaults to /SET hilight_act_color. Colors can have background color set with fg,bg. Works with activity list too, useful for example blinking.
- DCC rewrite. File names with spaces work properly, you can have multiple dcc chats with same people (or more useful, same nick in different ircnets), /DCC CHAT\|GET\|RESUME with no arguments accepts the last request, notifies if dcc request was sent to channel, warns about connecting to lowports, /SET dcc_autoget_lowports specifies if autogetting should work with lowports, complains of invalid DCC CTCPs instead of ignoring, /SET dcc_autoresume is like dcc_autoget except resumes the files if possible.
- /NAMES can print columns with different widths now. You can change the max. width with /SET names_max_width and /SET names_max_columns settings. Default is max. 6 columns.
- /LASTLOG: Added options -file &lt;filename> for writing lastlog to file, -window &lt;ref#|name> for specifying which window's lastlog to print (output is always to active window) and -clear option to remove all lastlog lines from window.
- /OPER [&lt;nick> [&lt;password>]] - syntax changed. If password isn't given, it's asked.
- /FOREACH server\|channel\|query\|window &lt;command>
- /UNBAN &lt;ref#> works. /BAN list shows reference numbers.
- /PERL &lt;code> - runs perl code (like /PERL Irssi::print "hello")
- /CLEAR -all - clear all windows
- /KICKBAN and /KNOCKOUT accepts multiple nicks separated with commas
- /SET theme - says what theme was changed to, and complains if theme wasn't found. Setting theme's name to "xxx.theme" now works, too many people tried it with the .theme suffix :)
- /WHOIS without parameters in query does now same as /WII &lt;queried nick>
- IPv6 updates: /CONNECT, /SERVER, /SERVER ADD: added -4 and -6 options for specifying if we should connect to IPv4 or IPv6 address of the server. If -host or /SET hostname is set, irssi determines from it if it should use IPv4 or v6. If irssi still isn't sure of it, it fallbacks to /SET resolve_prefer_ipv6
- Logs and rawlogs write to files through special "write buffer". By default everything gets written immediately, but you can make it wait until there's specified amount of data in buffer or write once in a hour or so. Useful for people who want to keep hard disk at sleep at nights but still want to log. /SET write_buffer_mins and /SET write_buffer_kb specifies when to flush the buffer. /FLUSHBUFFER flushes it immediately.
- LOTS of other smaller things that should make your life easier :)

### Fixes
{:#v0-7-98-fixes }

- /SET dcc_autorename OFF didn't work before.
- Irssi compiled with IPv6 support didn't work properly with some operating systems.
- Theme saving to home dir didn't work correctly if globaldir already had the same theme.
- If log file locking failed, irssi always assumed it was locked while it could have been because filesystem didn't support locking or some other problem..

---

## 0.7.97
{:#v0-7-97 }

Timo Sirainen released this <abbr class="timeago" title="2000-12-03">2000-12-03</abbr> 

### Changes
{:#v0-7-97-changes }

- Added templates for themes - this allowed separation of the actual texts and styling/coloring. See default.theme file for more information. You should remove your old ~/.irssi/default.theme or at least merge it with the defaul.theme.
- If GLIB sources are found unpacked from some subdirectory, always compile it and use it even if GLIB is already installed somewhere else.

### Additions
{:#v0-7-97-additions }

- /SCROLLBACK REDRAW - redraw contents of current window according to active formats, ie. changing theme updates the scrollback. This requires /SET scrollback_save_formats ON.
- /SET log_theme &lt;theme> - you can specify what theme to use for writing texts to log file.
- /WAIT [-&lt;server tag>] &lt;milliseconds> - wait for &lt;milliseconds> before sending anything else to server
- /EXEC &lt;command> - execute command and print it's output (stdout only) to screen. (by Tinuk)
- Don't indent the next line when long word is split, this should help a bit when copying long URLs.
- Remember who set the topic and when, display the info when using /TOPIC.
- /SET emphasis - convert _underlined_ and **bold** words (and phrases) to use real underlines/bolds. (by tommik)
- While waiting for more netsplits/netjoins, if anything else is printed to screen, print the current netsplit/netjoin messages before that text.
- Print multiple identical mode changes in one line (mode +o nick by nick1, nick2, nick3)
- /WINDOW ITEM GOTO &lt;name> - sets &lt;name> active in current window
- /WINDOW ITEM MOVE &lt;window#>|&lt;name> - moves window item to another window.
- /SET autocreate_windows - should we create new windows for new window items or just place everything to one window
- /JOIN #already_joined_channel, /QUERY already_queried_nick - same as /WINDOW ITEM MOVE &lt;name>
- /SET activity_level, /SET hilight_level - specifies which message levels should be treated as msg/hilight activity. (by tommik)
- DCC queries are now created automatically only if /SET autocreate_query_level has DCCMSGS level
- If other side replies to our DCC CHAT request with DCC CHAT request of their own (maybe we were inside firewall and other side noticed it), connect to it immediately.
- Don't allow more than one identical DCC request, if more is received just update the port of the previous request.
- Added KILL handling - user/server kills are now printed formatted.
- If server KILLs you, connect back (almost) immediately (don't wait for the default 5 minutes)
- Nick completion now completes nicks from all channels in active window, except when completing the first word in line only nicks in active channel are completed.
- /SET show_nickmode_empty - when nick has no mode, should we display " " or ""
- /SET part_message - default message with /PART
- Added -current, -window and -level options to /ECHO
- Ctrl-T = transpose_characters
- Perl scripting supports now printformat(), ie. user can change the text format with /FORMAT just like any other formats.
- Proxy plugin now supports multiple servers, blocks CTCPs from clients behind it and if one client sends message to channel, other clients + proxy itself also receives the message.

### Fixes
{:#v0-7-97-fixes }

- Netsplit/netjoin printing fixes. Sometimes netsplits were hidden completely and some netjoins were forgotten and printed as normal joins instead.
- Lag checking broke sometimes when nick was changed
- Don't close non-autolog logs when leaving channel / closing query.
- Time formats didn't work in directory name of autologs.
- Sometimes join to channel didn't ever get synced.
- IPv6 support didn't work correctly with all non-Linux OSes.
- Lots of minor fixes and changes to make your life easier.

---

## 0.7.96
{:#v0-7-96 }

Timo Sirainen released this <abbr class="timeago" title="2000-10-19">2000-10-19</abbr> 

### Changes
{:#v0-7-96-changes }

- new configure option: \-\-disable-curses-windows. Use this if curses always redraws the window when scrolling. This is a weird problem, I'd like to know why it happens. :)
- Log settings are incompatible with previous versions. You'll need to setup them again. Or the targets are actually the only ones that irssi won't read correctly.
- Lots of moving and cleaning and rewriting stuff from irc to core so adding other IRC-like protocols (but not IRC) would be easier. This was mostly done to make SILC plugin work.
- Perl was split to Irssi and Irssi::Irc packages. You'll currently need to use both of them with perl scripts ("use Irssi; use Irssi::Irc;). This might not be needed in future :)
- Changes:
   - /SET default_nick -> /SET nick
   - /FORMAT own_me -> /FORMAT own_action
   - /FORMAT own_dcc_me -> /FORMAT own_dcc_action

### Additions
{:#v0-7-96-additions }

- Small tutorial to new irssi users - docs/startup-HOWTO.txt
- Proxy plugin works again, thanks to fuchs for fixing it :)
- You can now connect multiple times to same server and reconnections will work correctly with them.
- Support for half-ops (+h)
- Actions will now show up in window activity with hilight or message-color, not the text-color as before.
- Added tab-completion for /BIND's commands.
- Perl support is now built as runtime loadable module by default. You can still build it statically with \-\-enable-perl=static configure option.
- /SET completion_nicks_lowercase - when completing nicks always write the nick with lowercase (uppercase letters are ugly ;)
- /BIND &lt;key> /command works now directly instead of needing the "command" id in the middle
- /connect + /server server/chatnet completion by tommik.
- Keyboard should never get stuck again when receiving huge amounts of text from server that irssi doesn't handle fast enough.

### Fixes
{:#v0-7-96-fixes }

- Hopefully fixed the problem when Irssi starts eating 100% CPU
- Fixes to make irssi work with other (older and newer) perl versions than 5.005
- /MSG -servertag crashed irssi.
- /BAN could crash when showing bans
- log_day_change was never printed in logs
- /mode #channel -oooo... would deop the first 3, and then op the rest.
- When pressing down key, the command line wasn't saved to history.
- Closing or moving window didn't update the window activity list.
- Autologging with same named channels in different networks works now correctly.

---

## 0.7.95
{:#v0-7-95 }

Timo Sirainen released this <abbr class="timeago" title="2000-08-13">2000-08-13</abbr> 

### Changes
{:#v0-7-95-changes }

- Changes:
    - /LOG: Removed the -rotate option, it was pretty useless since
      adding the % formats to file name already tells that the log
      should be rotated.
    - WJOIN -> /JOIN -window and WQUERY -> /QUERY -window. Added
      WJOIN and WQUERY aliases for them in default config..

### Additions
{:#v0-7-95-additions }

- /SAVEWINDOWS saves the current layout of windows. It's automatically reloaded at startup.
- Theme fixes: /RELOAD reloads them, /SET theme changes the default theme, you can have window specific themes with /WINDOW THEME.
- Irssi uses now real curses windows, irssi should work now better with non-ncurseses.
- Autologging supports log rotating now too, just add the wanted % formats to /SET autolog_path
- /MSG nick completion now gives the nicks in right time order when using multiple irc networks.
- /SET beep_on_msg now works with all message levels, including HILIGHT.
- You can change the default line indentation with /SET indent
- /channel add -bots: You can now use @ or + before the nick mask to indicate that bot should have either ops or voices/ops.
- Perl scripting:
    - Added namespaces, you don't have to worry about if someone
      else also happens to be using event_privmsg function..
    - You can unload scripts with /UNLOAD &lt;name>.
    - Running scripts that are already loaded, destroys the old
      script from memory.
    - Added Irssi::print_window() function to print text to current
      window.

### Fixes
{:#v0-7-95-fixes }

- Don't autoclose window after part/unquery if there was still some channels/queries left in window.
- Autologging fixes: Don't log WHOIS replies by default (autolog_level = all -crap). And with /msg nick1,nick2 don't log to file nick1,nick2.log but nick1.log and nick2.log separately. It also failed if you hadn't created the base path for the logs, now irssi creates the whole directory path.

---

## 0.7.94
{:#v0-7-94 }

Timo Sirainen released this <abbr class="timeago" title="2000-07-24">2000-07-24</abbr> 

### Changes
{:#v0-7-94-changes }

- Help files! Use /HELP &lt;command> to see them. They're just very first beta versions so don't expect too much. They were written by Markus Vuori &lt;mm@vuori.net> with some help from EPIC's help files :)
- Changes:
   - /SET completion_disable_auto -> completion_auto
   - Changed the names of /BIND commands to be epic-compatible.
     Also added several new commands.
   - If \-\-prefix is used, add the default perl library directory to
     same prefix.

### Additions
{:#v0-7-94-additions }

- Implemented /WINDOW LAST for changing to last current window.
- Added DCCMSGS message level. Actions match now either MSGS or PUBLIC level as well as the ACTIONS level always.
- SET print_active_channel - if you have multiple channels in same window, should we always print the channel for each message (&lt;nick:#channel>) or only when the channel isn't active.
- Don't print nick changes and quit messages from same nick more than once in the same window (if you had joined multiple channels in same window).
- /SET settings_autosave - If set ON, settings are automatically saved when quitting and once per hour.
- Don't allow recursive aliases, ie. /alias echo echo hello does print hello instead of going to infinite loop.
- Implemented /IGNORE -time &lt;seconds>, patch by fuchs.
- /PERLFLUSH now cleans up the Perl interpreter properly (closes all the files opened in perl scripts, etc)

### Fixes
{:#v0-7-94-fixes }

- Awaylog didn't work right if you did /AWAY multiple times.
- /NOTIFY -idle sometimes printed the unidle-message even if the nick really didn't stop idling. Fixed several other notify list bugs.
- Tab-msgcompletion didn't work right after you had used /msg -ircnet nick
- Fixed the long standing text buffer bug which could sometimes crash irssi if you were unlucky.
- The channel key given in /JOIN should override the one given in setup.
- /RELOAD caused several bugs

---

## 0.7.93
{:#v0-7-93 }

Timo Sirainen released this <abbr class="timeago" title="2000-07-09">2000-07-09</abbr> 

### Additions
{:#v0-7-93-additions }

- Implemented /BIND [&lt;key> [&lt;action> [&lt;data>]]] command. &lt;key> can be CTRL-x, ALT-X or ALT-SHIFT-X The most useful action is "command", give the command in &lt;data>. You can see the rest of the actions with typing /BIND without any parameters. Some actions might have more than one word, to use them type the action in "quotation marks".
- When netsplit is over, irssi prints "Netsplit over, joins: (nicks)" and hides all the real JOIN messages.
- /^COMMAND hides the output of the command, it's not written to log either. Good for sending passwords for example.
- If you're pasting text to channel and some of it starts with /, Irssi will send the "/command" to channel if it doesn't exist (instead of just printing "unknown command").
- \-\-enable-perl[=libdir] to configure - you can specify what directory to install the perl libraries.
- Implemented runtime loadable modules. /LOAD loads a module, /UNLOAD unloads it.
- You can change statusbar colors with /SET statusbar_xxx.
- Added -clear option to /SET.
- Tab-completion for /FORMAT.
- Ctrl-Y undeletes the last line deleted with Ctrl-U.

### Fixes
{:#v0-7-93-fixes }

- Reconnecting to server had a few bugs
- /RELOADing configuration produced a few bugs
- Highlighting had several bugs
- Automatic command and option completions had some bugs
- -option tab-completion didn't work

---

## 0.7.92
{:#v0-7-92 }

Timo Sirainen released this <abbr class="timeago" title="2000-06-30">2000-06-30</abbr> 

### Changes
{:#v0-7-92-changes }

- Some changes:
    /REHASH -> /RELOAD
    /SERVER -add, -remove, -list -> /SERVER ADD, REMOVE, LIST
    /SET window_close_on_part -> /SET autoclose_windows
    /HILIGHT -nick -> /HILIGHT -mask (see below)

### Additions
{:#v0-7-92-additions }

- Automatic completion of /commands. Automatic completion of command -options. Complains about unknown -options.
- /MSG [-&lt;server tag>] &lt;nick> &lt;msg> - you can specify what server to send the message to.
- Rewrote tab-completion to be modular, it's REALLY easy to add completion to whatever you want. It now handles:
    - Command completion works better, subcommand completion works
    - Command -option completion
    - /MSG completion completes from all IRC servers, so if you had
      message from ircnet and efnet, irssi will complete with
      /MSG -ircnet nick1 -> /MSG -efnet nick2
    - #channel completion works - it completes only channels you
      have joined or have in setup
    - File name completion with /DCC SEND (and other commands)
    - /TOGGLE settings completion
    - Completion for command parameters or subcommands work right
      even if the command was typed as alias.
- /HILIGHT updates:
     - -nick highlights only the nick, not the whole line. Works
       only with public messages.
     - -mask option matches the text for nick mask (it didn't even
       work before).
     - Window numbers in activity list are colored with hilight
       color.
     - You can give real color names with -color option. All the
       "normal" colors can be given, if you want bold colors, use
       b+color name, like bgreen.
     - /SET hilight_color specifies the default highlight color
     - /SET hilight_only_nick specifies if we should highlight the
       nick or the whole line if -nick or -nonick wasn't specified
       with /HILIGHT.
- /LAST -away checks only lines that came after last time you went away.
- You can specify command(s) to be sent automatically to server after connected with /IRCNET -autosendcmd. Useful for sending your password to NickServ.
- Added /SET reuse_unused_windows setting, default is OFF. Works only when /SET autoclose_windows is ON. This specifies if new windows should be joined to new window, or if existing empty windows should be used.
- /SET lag_min_show -1 disables displaying lag entirely.

### Fixes
{:#v0-7-92-fixes }

- /SCROLLBACK HOME, END and GOTO commands weren't working right.
- Closing active window that had channels/queries could crash
- Using \n with /SET expand_escapes ON didn't work right.
- Logging HILIGHT messages didn't work
- The "max. count" parameter in /LAST didn't work right.

---

## 0.7.91
{:#v0-7-91 }

Timo Sirainen released this <abbr class="timeago" title="2000-06-14">2000-06-14</abbr> 

### Additions
{:#v0-7-91-additions }

- Ctrl-X changes IRC server in stats/msgs/empty windows.
- /JOIN -&lt;server tag> #channel joins to channel in specified server.
- /WHOIS automatically sends a /WHOWAS query if nick wasn't in IRC.
- if some unknown /command had another / in it, like /usr/bin, send it as normal message. good for copypasting paths :)
- If you're not allowed to connect to server (K-lined, no I-line), Irssi won't try to reconnect back to the server.
- You can disable window activity notifies in specified channels with /SET noact_channels #chan1 #chan2 .. The activity is displayed if window had a message to you.
- Tab-completion works now with /commands and /set variables
- /SET close_window_on_part - should we close the window too when /PARTing channel
- /SET autocreate_own_query ON - creates query window when you send message with /MSG nick.
- /SET mail_counter specifies if we should show mail counter in statusbar.
- /SET wall_format specifies the text that's sent with /WALL
- If you /SET expand_escapes ON and type \n or \t to text line, they will be expanded to newline and tab.
- Ctrl-W deletes word in left

### Fixes
{:#v0-7-91-fixes }

- Flood was detected wrong - /SET flood_timecheck's argument was supposed to be seconds, not milliseconds.
- Unignoring autoignored nicks didn't work
- Logging wrote messages to log file twice
- /WINDOW MOVE &lt;number> could put irssi to infinite loop
- ANSI blink code crashed irssi.
- Replying to DCC GET and CHAT requests didn't work
- /HILIGHT displayed levels twice, /HILIGHT -channels didn't work
- /SET ignore_signals wasn't read at startup..

---

## 0.7.90
{:#v0-7-90 }

Timo Sirainen released this <abbr class="timeago" title="2000-06-04">2000-06-04</abbr> 

### Changes
{:#v0-7-90-changes }

- On the way to 0.8.0 .. Major rewriting/rearranging code. There's some changes in behaviour because I'm trying to make Irssi compatible with EPIC as much as possible (except the scripting, perl should be enough?)
- DOCUMENTATION! See docs/manual.txt
  
  This NEWS file contains only the biggest new features, you should browse through the documentation to find the rest. Some of the parameters of commands listed in this file aren't really up to date since I got a bit bored writing them here too.. They are correct in the manual.
- Irssi isn't anymore IRC specific client, you could easily take the whole IRC part away and use some other chat protocol instead, or use both at the same time. Currently however, only IRC protocol is supported. See docs/design.txt for more information.
- libPropList isn't needed anymore - I'm using my own configuration library. This is mostly because different proplists worked a bit differently everywhere and several people had problems with it. It's also yet another extra library that you needed to compile Irssi. New configuration library has several advantages:
  
  You can add comments to configuration file and they also stay there when it's saved.
  
  It's not nearly as vulnerable as proplist. If some error occurs, instead of just not reading anything it will try to continue if possible. Also the error messages are written to irssi's text window instead of stdout.
  
  It can be managed more easily than proplist - setting/getting the configuration is a lot more easier.
- Coding style changes - I'm not using gint, gchar etc. anymore, they're just extra pain when moving code to non-glib projects and syntax hilighting doesn't work by default with most editors ;)
  
  Indentation style was also changed to K&R because of some political reasons ;) And I'm already starting to like it.. :) It forces me to split code to different functions more often and the result is that the code gets more readable.
  
  And finally I'm also using `const` all over the place.
- Signal handlers changed - you don't anymore return value 0 if you wish to stop signal. Instead use signal_stop() or signal_stop_by_name().

### Additions
{:#v0-7-90-additions }

- Flood protection when sending commands to server works now better. It allows sending first 5 messages immediately, but after that only one message is sent every 2.2 seconds.
  
  This is the same flood protection that most IRC servers use, so the only affect this protection has is that when sending a lot of commands to server you won't get kicked out from server because of "excessive flood".
  
  This can be changed from settings `cmd_max_at_once` and `cmd_queue_speed`. If you want to disable this for some reason, use /SET cmd_queue_speed 0
- Split windows in text version, all the normal ircII /WINDOW commands should work: new, kill, grow, shrink, balance, show, hide
- /EVAL &lt;commands> - Expand all the special variables from string and run it. Commands can be split with ; character. See docs/special_vars.txt for more info.
- Aliases are parsed just like /EVAL - arguments are in $0..$9.
- Text formats are also parsed like /EVAL, arguments used to be in $1..$9, now they're in $0..$8 so it messes up existing themes..
- /SET [key [value]] - no more the '=' character. Boolean values also need to be changed with ON/OFF/TOGGLE values (not yes/no).
- /SAVE [&lt;filename>] - saves the settings to file. /REHASH [&lt;filename>] - re-read the configuration file on the fly
- /TOGGLE &lt;key> [ON/OFF] - same as /SET &lt;key> TOGGLE
- /ALIAS [-]&lt;alias> [&lt;command>], /UNALIAS &lt;alias> Show, add or remove aliases. /ALIAS -alias = /UNALIAS alias
- /NOTIFY [-list] [-away] [-idle [minutes]] &lt;mask> [ircnet [ircnet...]]
    -away notifies about away-status changes
    -idle notifies if idle time is first larger than `minutes`
     (default is hour) and then it drops down.
    -list lists the notify list entries with all their settings /UNNOTIFY &lt;mask>
  
  /NOTIFY without any arguments displays if the people in notify list are online or offline.
- /HILIGHT [-nick \| -regexp \| -word] [-color &lt;color>]
           [-level &lt;level>] [-channels &lt;channels>] &lt;text>
    -nick: match only for nick
    -regexp: `text` is a regular expression
    -word: `text` must match to full words
    -color: print the reply with `color` - color can be a bold (^B),
            underline (^_) etc. too
    -level: match only for `level` messages, default is
            publics,msgs,notices,actions
    -channels: match only in `channels` /DEHILIGHT &lt;ref#> | &lt;text>
- /LASTLOG [-] [-new] [-regexp \| -word] [-&lt;level> [...]]
           [&lt;pattern>] [&lt;count> [&lt;start>]]
    -: don't print the "Lastlog:" and "End of Lastlog" messages.
    -new: show only lines since last /LASTLOG
    -regexp: `text` is a regular expression
    -word: `text` must match to full words
    -level: what levels to check, like -public -msgs (default is all)
    &lt;pattern>: text to search for, or all if empty
    &lt;count>: maximum number of lines to show
    &lt;start>: skip the last `start` lines
- /IGNORE [-regexp \| -word] [-pattern &lt;pattern>] [-except]
          [-channels &lt;channel>] &lt;mask> &lt;levels> &lt;^levels>
    -regexp: `pattern` is a regular expression
    -word: `pattern` must match to full words
    -pattern: &lt;pattern> must match to the message's text
    -except: **DON'T** ignore
    -channels: ignore only in channels
    &lt;mask>: either a nick mask or list of channels
    &lt;levels>: list of levels to ignore
    &lt;^levels>: list of levels to NOT ignore
               (/ignore -except nick notices = /ignore nick ^notices) /UNIGNORE &lt;ref#> | &lt;mask>
  
  The best match always wins, so you can have:
    /IGNORE * CTCPS
    /IGNORE -except \*!\*@host.org CTCPS
- /LOG OPEN [-noopen] [-autoopen] [-targets &lt;targets>] [-window]
            [-rotate hour\|day\|month] &lt;filename> [&lt;levels>]
    -noopen: create the entry to log list, but don't start logging
    -autoopen: automatically open this log file at startup
    -targets: log only in specified channels/nicks
    -window: Log this window
    -rotate: Reopen the log file every hour, day or month. This
             makes only sense if you specify date/time formats
             to file name.
    &lt;filename>: File name where to log, it is parsed with strftime(),
                so %d=day, etc. see "man strftime" for more info.
    &lt;levels>: Defaults to ALL /LOG CLOSE &lt;ref#> | &lt;fname> - close log and remove from log list /LOG START &lt;ref#> | &lt;fname> - start logging to file /LOG STOP &lt;ref#> | &lt;fname> - stop logging to file /LOG - display the log list NOTE: Log files are locked after opened, so two irssi's can't accidentally try to write to same log file.
- /WINDOW LOG ON\|OFF\|TOGGLE [&lt;filename>] Start/stop logging window, same as /LOG OPEN -window. If file name isn't given, it defaults to ~/irc.log.&lt;windowname> or ~/irc.log.Window&lt;ref#> if window doesn't have name. /WINDOW LOGFILE &lt;filename> Creates the entry to log list, same as /LOG OPEN -window -noopen. Also, if /WINDOW LOG ON is used it starts logging to this file.
- /SET AUTOLOG ON\|OFF\|TOGGLE /SET AUTOLOG_LEVEL &lt;level> /SET AUTOLOG_PATH &lt;path> - expandos can be used, $0 is the target. Enables automatic logging, files are automatically created as needed and after some time of inactivity, they are closed. If you are using multiple servers, it makes sense to use the server tag as part of the file name, for example ~/irclogs/$tag/$0.log (this is the default).
- /SET window_auto_change - if enabled, irssi will automatically change to automatically created windows (like queries). It will also clear your command line and put it to command history so that you don't accidentally write anything to wrong window. You'll get the command back by pressing up arrow.
- /SET show_quit_once - show quit message only once instead of in all channel windows the nick was joined.
- Server reconnections work better. It will now automatically set your previous user mode and away message (and rejoin the channels, which it already did before) after reconnected. If you use /SERVER to connect to different IRC network, none of this will be done.
- /CAT &lt;filename> - prints the file to screen
- /SET query_auto_close &lt;secs> - automatically close queries after &lt;secs> seconds. It won't close queries that have unread messages, and it won't close queries in the active window.

---

## 0.7.28
{:#v0-7-28 }

Timo Sirainen released this <abbr class="timeago" title="2000-03-11">2000-03-11</abbr> 

### Additions
{:#v0-7-28-additions }

- irssi-text: New improved "text widget". It takes less memory and if you resize the terminal horizonally, the text automatically changes to right size. Several other changes too:
  
  /CLEAR only clears the screen, you can still scroll the window up. /SCROLLBACK, or the default alias /SB:
    /SB CLEAR - Clear screen, free all memory used by texts in window.
    /SB HOME - Jump to start of the buffer
    /SB END - Jump to end of the buffer
    /SB GOTO [[-\|+]line#|time] - Jump to specified line or timestamp.
  
  
    -100 jumps back 100 lines, +100 jumps forward 100 lines, or
    100 simply jumps to 100. line in scrollback.
  
  
    Time is the format [dd.mm \| -&lt;days ago>] hh:mi[:ss]
  
  
    Examples:
      /SB GOTO 15:00 - Jump to first text that came after 15:00 today
      /SB GOTO -1 15:00 - First text after 15:00 yesterday
      /SB GOTO 1.2 - First text in 1. February
      /SB GOTO -100 - Jump back 100 lines
      /SB GOTO +100 - Jump for
- After lost connection to server and reconnected or changed the server manually with /SERVER, Irssi will rejoin back to the same channels that you were in before disconnection. They will also be placed to same windows they were, even if you were in same channel in multiple servers.
- /SERVERS and disconnect dialog displays also servers that are being currently connected and waiting reconnections. You can remove them with /DISCONNECT &lt;tag>.
- If you are in multiple irc servers and the active server of the window isn't the same as where the message came from, the message is prefixed with a [server tag].
- If you don't specify the path for Perl scripts, Irssi tries to find them from ~/.irssi/scripts/ or /usr/lib/irssi/scripts/ directories. Irssi will also run automatically scripts in ~/.irssi/scripts/autorun/ at startup. Several other updates to Perl support too.
- Support for ircII translation tables, /set translation &lt;file> See /usr/share/ircII/translation/* (at least in Debian)
- /ACTION &lt;target> &lt;text> - Send action to target (like /ME), target is either #channel, nick or =dcc_char_nick
- 5 CTRL-C's in a row quits irssi-text.
- %| in themes marks the line indentation position - works only in irssi-text for now..
- You can have several msgs/status windows, one for each server.
- Option: start GNOME panel applet at startup
- \-\-without-gtk option for configure disables building GTK frontend
- /LAST -new shows only the texts that came after latest /LAST.

### Fixes
{:#v0-7-28-fixes }

- Autojoining doesn't switch automatically to the joined channel's window (try [FS#2](https://github.com/irssi-import/bugs.irssi.org/issues/2 "/set without arguments doesn't work") :)
- Several (Perl) compilation problems fixed.
- Text hilight color was dark grey, changed to white..
- /LAST doesn't display the texts found from previous /LAST blocks
- Fixed a few memory leaks

---

## 0.7.27
{:#v0-7-27 }

Timo Sirainen released this <abbr class="timeago" title="2000-02-25">2000-02-25</abbr> 

### Changes
{:#v0-7-27-changes }

- Perl support - finally! Took only a year or so to imlement it ;) Well, I could have done it ages ago but it wouldn't have had all the flexibility it now has - you should be able to do almost anything with perl scripts. See DOCS/PERL for some documentation and examples/ directory for a couple of example scripts.
  
  This is the very first version and I haven't even tested that all functions work correctly! Any suggestions are welcome. I don't really like the values() functions so if someone knows better ways to do them I'd really like to hear.
  
  BTW. I haven't had time to learn Perl well yet, so my scripts are probably not the best examples.. :)
  
  If for some reason you don't wish to use Perl, you can disble it with giving \-\-disable-perl to configure.

### Additions
{:#v0-7-27-additions }

- /CYCLE [#channel] - parts/rejoins the channel
- Autojoining doesn't switch automatically to the joined channel's window.
- Server tag generation is a bit smarter now.
- irssi-text: Resizing terminal works now right even if your curses don't have resizeterm() function.

### Fixes
{:#v0-7-27-fixes }

- /NAMES crashed when done in a non-channel window
- irssi-text: Resizing terminal when irssi had some empty windows messed them up..
- toggle_show_nickmode didn't actually do anything :) It was always on..

---

## 0.7.26
{:#v0-7-26 }

Timo Sirainen released this <abbr class="timeago" title="2000-02-19">2000-02-19</abbr> 

### Fixes
{:#v0-7-26-fixes }

- Space (and maybe other keys) didn't work when caps/numlock was on.

---

## 0.7.25
{:#v0-7-25 }

Timo Sirainen released this <abbr class="timeago" title="2000-02-19">2000-02-19</abbr> 

### Additions
{:#v0-7-25-additions }

- /WQUERY - create query to current window
- Irssi doesn't close the window anymore when using /PART
- irssi-text also displays user's address in topic bar in queries.
- /NAMES list is now displayed sorted
- irssi-text: /WINDOW MOVE PREV\|NEXT

### Fixes
{:#v0-7-25-fixes }

- Topic bar sometimes displayed some other channel's topic if the channel didn't have a topic.
- Irssi automatically changed to auto-created query windows..
- When using /WINDOW CLOSE it didn't change to different window
- Made fontset_load() optional - it broke some fonts..
- Using Ctrl-B (bold) didn't move the cursor

---

## 0.7.24
{:#v0-7-24 }

Timo Sirainen released this <abbr class="timeago" title="2000-02-19">2000-02-19</abbr> ▪ [stable]

### Additions
{:#v0-7-24-additions }

- French translation
- Updated Brazilian Portuguese translation translation, now with the right pot file name :)
- Using fontset_load() instead of font_load(), helps with using some fonts (by hashao@telebot.com)
- /TS - display topics of all channels you're joined
- Automatically change to the created window
- Option: Show op/voice status in channel messages before nick.
- irssi-text: Displays topic bar op the top of the screen - /set toggle_show_topicbar = yes\|no
- Recognize +a (anonymous) and +r (reop when opless) modes
- Don't allow any setup file changes or log writing if another irssi session is running.
- /whois without any arguments gives a whois of yourself

### Fixes
{:#v0-7-24-fixes }

- Irc network list was still corrupted in channel dialog.
- /LIST dialog - users column is now sorted numerically (10 shows after 9, not after 1)..
- Log setup dialog: Clear all button was over Client errors toggle button.
- /LAST's output displayed some crap in log file.
- irssi-text should work better with other curses libraries than ncurses
- irssi-text should work better with non-black backgounds
- Fixed tab completion when completion char was comma
- Couple of configure bugs fixed
- Specifying source host (vhosts) didn't work.
- DCC resume had been broken quite a while

---

## 0.7.23
{:#v0-7-23 }

Timo Sirainen released this <abbr class="timeago" title="2000-01-23">2000-01-23</abbr> ▪ [stable]

### Additions
{:#v0-7-23-additions }

- channel's key (+k key) is displayed in irssi-text's statusbar if it has one.
- Nick hilight detector is a bit smarter now, for example if your nick happens to be "its", "it's blahblah" doesn't trigger it..
- colorless irssi-text (/set colors = no): activity list is split in two, Act and Det lists. Det displays list of windows where there's new messages for you.

### Fixes
{:#v0-7-23-fixes }

- /LAST without any parameters crashed
- if queried nick was changed, GUI didn't notice it.
- config file was invalid in .22
- irssi text widget didn't work in .22
- dcc transfers always displayed 0.00kB/s in .22

---

## 0.7.22
{:#v0-7-22 }

Timo Sirainen released this <abbr class="timeago" title="2000-01-16">2000-01-16</abbr> ▪ [stable]

### Additions
{:#v0-7-22-additions }

- configure displays a summary of things to compile
- /set colors = yes\|no, sets colors on/off in irssi-text
- /window goto active now finds first the window with the higest activity (msgs to you -> msgs -> rest). Alt-A is also default key shortcut for this
- When connection is lost to server, irssi will remember the channels in windows. After reconnected, (auto)joining to same channels will join the channels to the old windows.
- Improved hilighting: You can specify what color to hilight the text with, to channel field type the (mirc) color number, like "4 #blah" hilights the text with red in channel #blah, both color and channel(s) are optional. You can also hilight nicks' colors, to text field type "NICK:nick!mask", like NICK:nick, or NICK:\*!\*@*.blah.fi hilights people from blah.fi domain

### Fixes
{:#v0-7-22-fixes }

- Modeless channels (+channel) didn't get synced ever..
- Some kB/s messages displayed wrong values when resuming DCC transfers. Also, kB/s is now displayed with two decimals
- "Day changed to 00-10-2000" .. month was wrong. No Y2K bugs however ;)
- List of ircnets was displyed wrong in server dialog.
- Userhost replies didn't handle ircops right..
- Doesn't quit when receives SIGHUP - some window managers send it when restarting itself (Afterstep)
- Specifying "source host IP" didn't work (vhosts).
- Using ctrl-b etc. didn't move the cursor forward..
- Don't try to compile GTK parts of plugins if we don't even want build GTK irssi
- Doesn't crash when trying to create DCC dialog after being disconnected from IRC server
- Modeless channels (+channel) didn't get synced ever..
- Some transparency fixes, it's a lot faster now when moving the window, but it's still too slow when creating it, not sure why..

---

## 0.7.21
{:#v0-7-21 }

Timo Sirainen released this <abbr class="timeago" title="1999-12-20">1999-12-20</abbr> ▪ [unstable]

### Additions
{:#v0-7-21-additions }

- Irssi-text: Channel activities are displayed with different colors in statusbar
- Keeps track of "wanted nick", ie. the nick you specified in the setup or to /server or /nick. When reconnecting to server it always tries the wanted nick before falling back to alternate nicks.
- IRC Network specific settings: nick, username, realname, max. kicks/modes/msgs per command.
- Transparency works
- Automatic logging when you're away. Set it on/off from settings/misc
- /connect and /server changes the server in the current window if the window isn't channel or query.
- Wallop actions are displayed right
- Ctrl-N/P keys change to previous/next window
- Polish translation updated
- /channel next, /channel prev - changes to next/previous channel in the current window. Ctrl-X is by default bound to /channel next.

### Fixes
{:#v0-7-21-fixes }

- /WHO could crash irssi
- /join !!channel crashed

---

## 0.7.20.1
{:#v0-7-20-1 }

Timo Sirainen released this <abbr class="timeago" title="1999-11-28">1999-11-28</abbr> ▪ [unstable]

### Changes
{:#v0-7-20-1-changes }

- I just started #irssi in irc.openprojects.net too.. It's still in IRCNet too, don't know yet if I'll keep both or drop the other one..

### Additions
{:#v0-7-20-1-additions }

- You can use %n as current nick with aliases

### Fixes
{:#v0-7-20-1-fixes }

- Closing a window with split windows open crashed
- Channel widgets weren't being updated when joined to channel in empty window
- configure didn't check if we wanted to build MySQL plugin or not, now it's built only if you give \-\-with-mysql to configure
- Using the whois, ping, etc. buttons in queries crashed

---

## 0.7.20
{:#v0-7-20 }

Timo Sirainen released this <abbr class="timeago" title="1999-11-27">1999-11-27</abbr> ▪ [unstable]

### Additions
{:#v0-7-20-additions }

- Polish and finnish translations started
- SQL plugin which doesn't do much, currently supports MySQL only. Meant to be used by other plugins.
- Botnet to bot plugin - it should already be possible to create a big bot network with this (each bot having multiple clients + uplink). The functionality is limited only to BCAST message for now which sends a message to all bots. Read docs/botnet.txt for my plans for it :)

### Fixes
{:#v0-7-20-fixes }

- If plugins failed in initialization (plugin_init()), irssi could crash.
- Server settings (nick, realname, etc.) were saved to different place in configuration file than where they were read from.. So, saving them didn't really work.
- Plugin autoloading didn't work
- When trying to show channel's window from panel and you weren't using helvetica font (itext's internal default), irssi crashed..
- Irssi crashed if you didn't have menubar enabled and didn't compile with gnome.
- When invalid theme was found from global directory, irssi complained about it every time. Now the fixed theme is saved to ~/.irssi/ directory and used thereafter.
- Deleting ircnets didn't work right

---

## 0.7.19
{:#v0-7-19 }

Timo Sirainen released this <abbr class="timeago" title="1999-11-20">1999-11-20</abbr> ▪ [unstable]

### Changes
{:#v0-7-19-changes }

- Text formats changed - they should be compatible with epic/bx now. See docs/FORMATS for more information

### Additions
{:#v0-7-19-additions }

- Internationalization support - finally. No languages yet though..
- /window new split creates a new splitted window
- Automatic text replaces, useful for things like :9 -> :) .. This is actually almost same as completions, except they are activated with different keys..
- Nicklist popup menu is configurable
- ~/.irssi/startup - add all commands here you want to run at startup
- Much more levels for ignoring/logging/etc. See docs/COMMANDS for a list
- Ignoring joins, parts, etc. work, ignoring channels work
- Automatically loading plugins at startup works in irssi-text and irssibot too
- Autoaccept dcc get/chat from given nick/address
- /help
- Server/Links dialog, displays list of servers in tree view. Doubleclicking a hub asks the servers behind the hub (doesn't seem to work in efnet)
- /server +irc.server.net does the same as /connect irc.server.net
- Nicklist is resizeable
- Buttons for closing and moving window left/right
- Query windows display nick's address in topic widget and the address isn't displayed in every msg in query windows.
- It's possible to add bold/colors/etc to default quit message
- MIRC colors are finally displayed with right colors
- You can run multiple command in alias, separate them with &&. You can create a & character with \&
- Hilighting changes: Your own /msgs won't trigger channel activity, received private messages get the "new text" color
- /MODE accepts multiple modes at once and they're split automatically to 3 modes/command, like /MODE #chan +oooooo nick1,nick2,.. is split to two commands which are sent to server.
- /KICK, /MSG, /NOTICE, /CTCP and /NCTCP are also automatically split into multiple real commands. /KICK can kick max. 4 nicks per command, privmsg/notice can send max. 3 nicks per command.
- Option: Show timestamps in msgs.

### Fixes
{:#v0-7-19-fixes }

- Joining to channel from channels dialog that had password set didn't work.
- When scrolling, Irssi text widget sometimes left black spots in text area if some other window was overlaping it.
- DCC resumes still didn't work
- Fixed some memory leaks

---

## 0.7.18.1
{:#v0-7-18-1 }

Timo Sirainen released this <abbr class="timeago" title="1999-11-04">1999-11-04</abbr> ▪ [stable]

### Fixes
{:#v0-7-18-1-fixes }

- Window didn't scroll if you were using GtkText
- Resuming DCC transfers could mess up the existing transfers with the same nick..
- Some PONGs were displayed on screen if you were enough lagged..
- \-\-help works now without gnome (gtk/text versions)
- Sending data to irc server/dcc chats/proxy's clients/etc. won't block forever anymore - I once got it to happen with proxy..
- Some fixes for channel limit/key widgets above nicklist
- Speech plugin works now right with timestamps enabled
- irssibot (gui-none) doesn't crash at startup anymore and it doesn't link with ui-common anymore. Also added a \-\-load / -l command line option to specify what plugin to load at startup. Default = bot

---

## 0.7.18
{:#v0-7-18 }

Timo Sirainen released this <abbr class="timeago" title="1999-10-18">1999-10-18</abbr> ▪ [stable]

### Changes
{:#v0-7-18-changes }

- Finally a version I dare to call stable :) Just a bugfix release for 0.7.17 but it had only a few problems..
- Status window is now off by default

### Fixes
{:#v0-7-18-fixes }

- Sound and speech plugins weren't working.
- Proxy plugin shouldn't crash now while not connected to server
- Using some menuitems crashed when using the popup menus instead of menubar.
- Removed a Gdk-Critical warning when opening themes dialog without GNOME
- When resuming DCC transfers the average transfer rate was incorrect
- If you tried to connect to server while themes dialog was open, it crashed.
- Several problems fixed with changing background pixmaps
- Fixes for building from different directory
- Trying to save theme crashed..

---

## 0.7.17
{:#v0-7-17 }

Timo Sirainen released this <abbr class="timeago" title="1999-10-16">1999-10-16</abbr> ▪ [unstable]

### Additions
{:#v0-7-17-additions }

- Irssi text widget! (replaces zvt)
   - supports proportional fonts
   - FAST
   - background pixmaps (scaled, tiled, scrollable, shaded)
- Proxy plugin - Unlike other irc proxies, this is more than just a simple proxy. You can connect to it from multiple clients at the same time, but each client will use the _same_ irc session, so you can keep one irc client open all the time in your home, one at work, one at wc, etc. All the clients get the same "normal" messages from server, but if you request a /whois or /who or some other commands, the reply will be sent to only the client that requested it. Check README how to use it.
- Irssi is now much faster catching up things after joined to channel, it asks channels' MODE and WHO first, all with the same command (WHO #a,#b,#c), after them it asks the ban lists etc. less important things.
- Workaround for GTK themes eating X server's memory
- Command line arguments:
        -c server [-p port] : connects to server at startup
        -! : don't autoconnect to any servers
        -n : specify nick to use (override setup)
- Server lag displayed in statusbar, you can also set irssi to automatically disconnect from server if it is too lagged
- Channel limit and key is displayed above nicklist
- Number of ops and total number of nicks in channel is displayed
- Nicklist background color can be changed
- Each window can have it's own command history buffer
- Try to let the server disconnect the socket (5 sec timeout) to make sure that quit message gets through.
- Improved /gwhois dialog
- Setup dialogs are resizeable
- You can specify what port to use with DCC.

### Fixes
{:#v0-7-17-fixes }

- Channel dialog fixes: after editing channel, it was moved to the end of the list, opening multiple channels edit dialogs didn't work right
- Reconnecting to server didn't work (always)
- Giving multiple nicks for /gwhois messed up irssi

---

## 0.7.16
{:#v0-7-16 }

Timo Sirainen released this <abbr class="timeago" title="1999-09-13">1999-09-13</abbr> ▪ [unstable]

### Additions
{:#v0-7-16-additions }

- Started bot plugin, it has simple user management functions and auto-opping/voicing done (but it does it well :)
- "channel synced" text doesn't trigger channel activity anymore
- Rawlog displays where event was redirected
- /wjoin - you can join multiple channels in same window
- /window goto #channel - moves you to window with the channel, query or dcc chat
- /window goto active - moves you to first window with activity
- /list and /names complains if they're run without any arguments, -YES overrides this
- Giving -nogui parameter to /list and /who commands doesn't use the GUI dialog
- All the dialogs that have clist widget: you can resize columns and sort the list by clicking the headers
- /list and /who dialogs displays total number of items and the list is searchable
- Autojoining to channels work with irssi-text too
- /gwhois dialog has now refresh button, /gwhois is used when clicking whois from nicklist popup menu

### Fixes
{:#v0-7-16-fixes }

- Restoring saved window size didn't work very accurately, restoring position also had some problems..
- Rawlog doesn't crash anymore if not connected to server
- Notifylist and checking of who uses your nick uses WHOIS again, WHO didn't display user info unless s/he was -i or in same channels..
- You had to run /list a couple of times until it worked..
- WHO was sent to people who joined channel to find out who they were, unfortunately it had a small bug and didn't work..
- DCC didn't work with IPv6

---

## 0.7.15-3
{:#v0-7-15-3 }

Timo Sirainen released this <abbr class="timeago" title="1999-08-31">1999-08-31</abbr> ▪ [unstable]

### Changes
{:#v0-7-15-3-changes }

- _TOO_ many bugs in .15, mostly compilation problems, I really should test things better when I release them. This will be the last time, I swear :)

### Additions
{:#v0-7-15-3-additions }

- Rawlog window, /rawlog &lt;file name> also saves it.
- \-\-without-imlib configure switch

### Fixes
{:#v0-7-15-3-fixes }

- After opened themes dialog, "(none)" window appeared, after opening it, irssi crashed.
- "day changed" message was displayed at startup
- Addresses in DCC connections were displayed wrong
- Didn't compile without gnome
- The first .15 didn't compile without IPv6 support, -2 fixed it

---

## 0.7.15
{:#v0-7-15 }

Timo Sirainen released this <abbr class="timeago" title="1999-08-29">1999-08-29</abbr> ▪ [unstable]

### Changes
{:#v0-7-15-changes }

- Only week since last version, much better :) Lots of internal changes, hope they work right. No "weird crashes" found since last version, 0.8.0 can't be too far away :)
  
  CVS is also working again, no anonymous but I can give access if someone wants.

### Additions
{:#v0-7-15-additions }

- IPv6 support - yet another thing irssi is one of the first to support ;) Give \-\-enable-ipv6 switch to configure to compile it. Because of IPv6 addresses naming style (xxx:xxx:xxx..), /server server:port doesn't work anymore, you have to use /server server port instead.
- Sound plugin updates, should work much better
- Default config file is build into irssi, it's used if no other configuration file is found
- Implemented "idle queue", list of commands which should be sent to server when there's nothing else to send.. Changed CTCPs to use this.
- "massjoin" signal is sent when people join to channel, if many people join to channel quickly (netjoins), it waits for a while before everyone are joined and then sends the signal. This is used to update nicklist more quickly and some other internal stuff.
- /msg &lt;tab> completion: after you send msg to someone, the nick will go first in completion list.
- Giving \-\-with-servertest to configure now builds test irc server which you can use to try crash irc clients :)
- /sv displays system name and revision and irssi's website url
- You can give server password to /server as /server server port pass
- /unban completion, eg. /unban \*!\*@*.de unbans \*!\*@hu232hu2.blah.de
- /rmreconns removes all servers from reconnect list. I hate it when some server is down and irssi tries to reconnect it every 5 minutes and there was no way to cancel it..
- Displays day change message in all windows if you're using timestamps
- Realname is displayed in statusbar when mouse is moved over nick in nicklist
- /last displays the last buffer only from the current window
- option: beep when you receive private message
- Typing /dcc without any arguments is same as /dcc list
- Some code rearranging, moved more code to ui-common from gui-xxx
- IPv6 for /ban, it bans all the last 64k addresses .. not sure if it's THAT good idea but did it anyway.

### Fixes
{:#v0-7-15-fixes }

- DCC resume was broken.
- If someone quit from one ircnet but stayed on another, the nick was removed from both ircnets' channels.
- Irssi tried to find it's default config from $prefix/etc/irssi/irssi/config (one irssi too much :)
- You couldn't use ~/ when saving window buffer
- Trying to save window buffer twice crashed irssi
- ZVT transparency couldn't be removed on the fly
- Using find/new/close buttons in toolbar crashed
- Doesn't complain anymore about "You're not channel operator" with some irc networks that don't understand e or I modes
- /ban removed ident-character from username (~blah@ -> blah@) so bans didn't work..
- /knockout calculated the time left wrongly.
- irssi added -I/usr/include to compile parameters which broke compiling with several platforms..
- Irssibot notified about new development version when there was none
- Some problems/crashes fixed with plugin support
- \-\-without-socks didn't do anything..
- Password should first be sent to server first, not after nick/user. At least MUH (irc proxy) didn't like it.

---

## 0.7.14
{:#v0-7-14 }

Timo Sirainen released this <abbr class="timeago" title="1999-08-22">1999-08-22</abbr> ▪ [unstable]

My E-mail changed to cras@irccrew.org, don't use the old one anymore!

### Changes
{:#v0-7-14-changes }

- Hm.. Again a month since last version, 3 weeks should be max :) Hopefully this one will be bugfree, so I could finally release a "stable" version.. (somehow I think I'll end up with 0.7.14-2 anyway.. ;)
- Irssi uses now libPropList to read and save configuration file, so you need to have libPropList installed, it's also in different format so your old config file doesn't work anymore.
  
  Configuration file is located now in ~/.irssi/config file. Themes are also now stored in separate files in ~/.irssi/*.theme

### Additions
{:#v0-7-14-additions }

- Irssi can now notify you about new versions, you can also directly download them with DCC. (This will probably be changed to HTTP instead of using irssibot in IRC..)
- User interface changes (settings, menus) as suggested by James M. Cape &lt;jcape@jcinteractive.com>
- You can use ctrl-b,c,g,v,- when setting realname
- /version [server] - prints irssi version and irc server's version
- /ver [nick/channel] - sends ctcp version to nick/channel
- /sv [nick/channel] - sends irssi version text to nick/channel
- Added widget depends to several places, changed several modal dialogs to use gui_widget_depends() instead
- Added Socks5 initialization, maybe it works now?
- You can specify what host address you want to use if you have many..
- Away and kick reason dialog have history
- irssi-text option: activity list can be sorted by window number You can change this with /set toggle_actlist_moves=yes/no
- /msg &lt;text>&lt;tab> completes now people in current channel too
- You can set channel password in channel dialog
- /SET [key [=value / [key [key..]] - /SET displays all settings, /set key key2 displays values of key and key2, /set key=value sets key to value.
- DCC GET now gets all the files coming from user if file name isn't specified. DCC CLOSE also can close all dcc connections from user.
- The whole usermode is now displayed in statusbar, it used to display only the modes it knew (+iwsr)
- Ctrl-N and Ctrl-P go to next/previous window

### Fixes
{:#v0-7-14-fixes }

- When using zvt and joining to new channels, window size grew bigger
- /msg &lt;tab> completion was a bit buggy, if someone sent you multiple messages, you had to press tab multiple times until the nick changed to someone else..
- Default format for signon time in whois displayed nick instead of the signon time..
- Disconnecting server while it was still trying to connect hung irssi
- If old configuration file wasn't found, irssi (could have?) crashed on startup .. Could this really happen?!? Why did nobody tell me??
- irssi-text finally handles screen resizing right
- Gnome panel applet works with "old" (like non-cvs now :) panels too.
- If you left from channel before syncing was done, syncing stopped working after it..
- Removing ban exceptions didn't update irssi's internal list
- Rejecting dcc chat didn't work properly, when receiving reject get/send irssi didn't remove it from dcc lists
- Save/find dialogs weren't working after being closed.
- irssi-text complained about "Not enough parameters given" when pressing entry in empty line
- Mirc colors weren't removed properly for logs and could have crashed irssi
- Using /ban with mask (x!x@x) instead of nick crashed
- gui_widget_depends() wasn't working properly - didn't harm much :)

---

## 0.7.13-2
{:#v0-7-13-2 }

Timo Sirainen released this <abbr class="timeago" title="1999-07-22">1999-07-22</abbr> ▪ [unstable]

### Changes
{:#v0-7-13-2-changes }

- Again, a small bugfix release

### Additions
{:#v0-7-13-2-additions }

- You can specify what string to send to IRC proxy after connected, this lets at least some proxies work with irssi.
- Notifylist now displays which irc network nick joined/left (or if unknown, just IRC)

### Fixes
{:#v0-7-13-2-fixes }

- After closing some window, the numbers in window tabs didn't get updated
- /window next and prev didn't work properly
- status/msgs windows got destroyed a while after joining to channel.. or simply by doing "/mode (status)" command ..
- We don't try to DCC SEND file via dcc chat if the other side is using mirc ctcps.
- Default setting or autodetection of mirc ctcps weren't working.
- Actions from mirc users in dcc chat was displayed in double.

---

## 0.7.13
{:#v0-7-13 }

Timo Sirainen released this <abbr class="timeago" title="1999-07-21">1999-07-21</abbr> ▪ [unstable]

### Changes
{:#v0-7-13-changes }

- %p in text formats is changed to $, looks much cleaner :) Old formats in configuration files are automatically converted.
- I got some documentation done! :) I wrote a list of all commands irssi knows with (very) short descriptions, see COMMANDS file

### Additions
{:#v0-7-13-additions }

- Hebrew support by Ronen Tzur &lt;rtzur@shani.net> - see README-HEBREW
- Users with gone-flag are displayed with different color in nicklist List is updated with USERHOST commands in small pieces every now and then..
- Statusbar with some information in it ..
- Away message is displayed differently in /whois and /msged people who's gone
- /window goto &lt;n>, /window prev, /window next
- /window level [+/-]pub/msgs/...
    /window level msgs      - creates messages window
    /window level all -msgs - creates status window
- /bantype &lt;normal/host/domain/custom>
    - Normal - \*!user@\*.domain.net
    - Host   - \*!\*@host.domain.net
    - Domain - \*!\*@*.domain.net
    - Custom [nick] [user] [host] [domain]
        eg. /bantype custom nick domain - nick!\*@\*.domain.net
        eg. /bantype custom user host - *!user@host.domain.net
- /version - just displays version number..
- You can use different font in each channel
- Alt-q..o changes channels to 11..19
- Color configuration changes..
- irssi-text : Reading manuals help ;) Text's backgound color isn't changed to black anymore so pixmaps etc. should show up nicely :)
- /notify nick!mask@* [ircnets], /unnotify
- When trying to connect to server, you can abort it with the cancel button in statusbar
- First parameter of /disconnect is now * (current server) or server tag
- You can now use !channels with their short names (not always)
- Right clicking nick in channel pops up nicklist menu
- You can select multiple nicks from nicklist and execute the command for all of them.
- Panel applet supports panel size changes
- Window tabs have numbers now
- Ctrl-N changes to next window, Ctrl-P changes to previous window

### Fixes
{:#v0-7-13-fixes }

- Max. autoget size didn't work right, it got the file if the file was bigger than the max. size.. and it was compared as bytes, not kB's.
- Panel applet should now work right
- Hilight words feature was completely broken
- DCC Chats were displayed twice in status dialog
- Closing DCC chat still had a few problems
- After trying to join to channel where you could get in (invite only, banned, etc.) the created channel window wasn't destroyed.
- configure didn't check -lnsl right..
- Channel settings weren't read in the correct order -> autojoining to channels created the windows in reverse order every time.
- ZVT in GNOME CVS broke irssi.. Fixed.
- Quit message wasn't displayed if there was some commands waiting for transmit - quit was added to transmit queue and connection closed..
- Matching irc masks (nick!host@address) was case-sensitive..

---

## 0.7.12
{:#v0-7-12 }

Timo Sirainen released this <abbr class="timeago" title="1999-07-06">1999-07-06</abbr> ▪ [unstable]

### Changes
{:#v0-7-12-changes }

- #irssi is now started in IRCnet
- Release #2 :) The next day..
   + configure checks for -lnsl too
   + changed default font to fixed size so I wouldn't have to hear all
     the time how screen is messed up with zvt :)
   - background color couldn't be changed with zvt
   - irssi-text sometimes crashed at startup because of uninitialized
     variable..
   - you had to use \-\-without-gnome-panel even if you didn't build
     fwith gnome

### Additions
{:#v0-7-12-additions }

- Colorless theme, should be easy to start a new theme with using this. You need to copy the [theme:colorless] section to ~/.irssi.conf (or ~/.gnome/irssi whatever you happen to use..) from included irssi.conf to use this..
- You can DCC send and get files via DCC chat (don't need to be connected to server), don't know if this works with any other client or if any other client has this ability.. BitchX didn't seem to have.
- /WALL [#channel] message - Send notice to all ops in channel
- /last [-pub -msgs etc..] &lt;text> for text mode version
- Text mode version statusbar: -- more --, away (zZzZ)
- The "-!-" and "-!- Irssi:" texts and timestamp is now configurable
- Channel windows aren't destroyed anymore after getting disconnected
- /window close
- Outgoing flood protection: all commands you send to server are are queued and sent every 2 seconds. (if queue is empty, the command is sent immediately)
- Notify list popup dialogs are now optional
- /unalias (you could already do this with /alias)
- You can send Mirc style CTCPs now in DCC chat (preferences/dcc), also if mirc user first sends ctcp, it's automatically set to default for that dcc chat session.. You can also set it with /mircdcc [y\|n] or select from menu.
- Default color number in setup, this color is used if nothing else is specified.
- Server reconnection - you can add several irc servers to setup with same ircnet and autoconnect set and irssi goes through that list every time server gets disconnected unintentionally.
- irssi-text word splits the lines. also if it needs to split the line it leaves 10 empty spaces at the start of the next line.
- \-\-without-gnome-panel switch to configure

### Fixes
{:#v0-7-12-fixes }

- http://blah@a.b opened e-mail client instead of http client
- I set the socket non-blocking AFTER connect(), argh! This caused irssi to hang when trying to dcc get from bogus IPs or something.
- Background color wasn't read right
- Log dialog had some bugs
- Banning ip addresses didn't work right
- Some DCC problems fixed..
- Some irssi-text bugs fixed

---

## 0.7.11
{:#v0-7-11 }

Timo Sirainen released this <abbr class="timeago" title="1999-06-06">1999-06-06</abbr> ▪ [unstable]

### Changes
{:#v0-7-11-changes }

- Because of the color system changes, remove the [colors] section from irssi's configuration file or you will get some weird colors..
  
  The colors are pretty much taken from BitchX, IMO it looks nice :) But somehow I think many of you don't like it, so I made theme selector. Just need to make a few default themes..

### Additions
{:#v0-7-11-additions }

- Color system changed, the old one looked pretty ugly especially in text mode version.. You can now have more than one color/line by adding %fg[,bg] codes to text formats.. fg and bg are the normal 0-15 colors, in GUI version (without ZVT) you can use up to 99 user specified colors.
- Theme selector
- Text mode version: Entry line editing is working great! Command line history works, scrollback buffer works, statusbar is working (again, copying bitchx..), reads configuration file .. This is starting to become usable :)
- ZVT working better: font can be changed, transparency and background pixmap can be changed on the fly, the ugly block cursor isn't displayed anymore and wordclicking (urls, etc.) works.
- New GUI dialogs for /list, /who, /gwhois and when receiving invites to channels.
- Channels dialog changed a bit. New "Quick join" dialog where you can specify server and channel to join
- Mirc DCC resumes are working. By Trever Adams (trever_adams@bigfoot.com)
- List of text strings to hilight
- Notify dialog is created when someone in notify list joins irc.
- Nick completion improvements, /msg nick&lt;tab> works and in channels you can complete nicks anywhere in the entry.
- Window save size/position dialog
- DCC send added to popup menus
- Removing lines from GtkText is really slow, so now they're removed with several lines at a time. (default is 20)
- /window new [hidden] creates new window, /window server &lt;server tag> changes server in current channel, useful in text mode version..
- You can try to find memory leaks with giving \-\-with-memdebug switch to configure

### Fixes
{:#v0-7-11-fixes }

- Still some bugs with DCC SEND fixed..
- DCC list dialog crashed if there were dcc chats open, it also caused some random crashes when running..
- Maybe window size/position saving finally works right?
- g_(s)list_remove_link() didn't work as I had always thought .. It moves the link into separate list and doesn't free memory used by it like I thought.. So, inserted a few g_list_free_1() calls.
- When not using menubars, popup menu should have displayed all the items in it, it got broken in .10.
- signal_add_after() didn't work right.. actually it had a wrong name too, changed to signal_add_first() and made it to run these events before the normal events. This makes ignoring work again.
- /notice was buggy
- Configuration file handling (GTK version) was still a bit buggy..
- Lots of small bug fixes here and there..

---

## 0.7.10
{:#v0-7-10 }

Timo Sirainen released this <abbr class="timeago" title="1999-05-09">1999-05-09</abbr> ▪ [unstable]

### Changes
{:#v0-7-10-changes }

- ALL KNOWN CRASHES FIXED !! Weird, after changing the code with creating channels to empty windows, GtkText widget started working again, it used to crash after running the test ircserver for a while.. Maybe a few more versions and I'll release a "stable" labeled version again (08.0).

### Additions
{:#v0-7-10-additions }

- GNOME version can use ZVT widget to draw texts. This is a lot faster than GtkText and with it you can use nice non-scrolling backgrounds and transparency! However, you'll have to use the default colors with it for now and Window/Save Buffer or Find doesn't work in it. !!NOTE!! ZVT in gnome 1.0.9 is buggy, it sometimes crashes when destroying zvt widget (leaving channels). It should be fixed in next version (which doesn't currently exist..)
- DCC transfer dialog, display list of all going dcc transfers, the old dialogs can also be created.
- Channel specific background pixmaps, if you don't have Imlib you can use only .xpm images.
- /ban and /unban changed, they accept multiple arguments and channel name may be specified as the first argument
- dcc actions from mirc should work now

### Fixes
{:#v0-7-10-fixes }

- Text widget size is now saved instead of the window's size, should work better.
- Right clicking text widget created a popup menu, but select selection got broken after it
- Some potential bugs fixed after got kicked from channel
- Log dialog was buggy
- If dcc chat was closed but the query window was still there, trying to chat again with the same nick created another query window but used the old one..
- C-C, C-B, etc. add the character at the end of the entry, not at the current position
- Redirecting commands was a bit buggy, it always expected to receive the specified events. This worked with ISON command, but I forgot that WHOIS could also return "no such nick" events.. So, notifylist should now work right instead of sometimes printing whois results.
- You couldn't use the normal control-? keys (c-left, c-right, c-insert, ..)
- mirc colors were displayed with wrong colors
- Changed all isspace(), isdigit() and isalnum() calls to cast their argument as (gint) to remove warnings when compiling with IRIX.
- Speech plugin wasn't working again..
- After changing text format from setup, you couldn't change any other lines without closing setup dialog first
- Font couldn't be changed by editing the entry line
- /knockout format changed, it's now /knockout [timeout] nick reason (so the reason can have number at the start of it..), it also used to crash when unbanning
- DCC send fixed, fast send didn't work and without it it was eating all cpu.
- DCC sending files with spaces in their name didn't work (they're changed to _ now.)

---

## 0.7.9
{:#v0-7-9 }

Timo Sirainen released this <abbr class="timeago" title="1999-04-22">1999-04-22</abbr> ▪ [unstable]

### Additions
{:#v0-7-9-additions }

- Server/status dialog, displays list of all connected servers, channels, queries and dcc chats.
- Host resolving is now done in a child processes. Hopefully works better than threads which aren't used anywhere anymore..
- Window/Save window size and Save window position, next time the same window (status, msgs, channel, query) is opened the saved size and/or position will be used.
- gui_widget_depends_data(), widget will be automatically destroyed if the specified signal is called with the specified argument. Used to destroy DCC request dialogs when they're closed manually, timed out or rejected at the other end..

### Fixes
{:#v0-7-9-fixes }

- Fixed lots of memory leaks which some might have caused crashes.. src/memdebug.c has the debug functions I used ..
- DCC CLOSE closed always the last dcc connection instead of the one that matched the parameters
- Commented out all GUI_INPUT_EXCEPTIONs .. I don't even know when exceptions are sent and why (I thought that only when some error occurred..), Linux doesn't seem to send them ever? IRIX however sends them all the time which made irssi eating all cpu.
- Fixed compiling gui-text with systems that had only slang/slang.h
- gui_widget_depends() had some bugs
- adding irc networks by typing it's name when adding server didn't update the GUI of ircnets list.
- If some plugins were already loaded, and loading new plugin failed and it called plugin_deinit(), the call (might have) called some other plugin's plugin_deinit() and crash.. Some updated to change all global plugin functions to plugin_name_* calls so they wouldn't call other modules functions..
- If day changed when logging, the log file contained the day change lines before each line after that..
- Channel labels were hilighted even when the channel was selected..

---

## 0.7.8
{:#v0-7-8 }

Timo Sirainen released this <abbr class="timeago" title="1999-04-12">1999-04-12</abbr> ▪ [unstable]

### Changes
{:#v0-7-8-changes }

- This version has lots of internal changes, I haven't tried them much so hopefully everything works right..

### Additions
{:#v0-7-8-additions }

- external plugin, reads commands from named pipe and executes them
- sample plugin updated, creating new plugins should when based on this one
- gui-none is built, it tries to run bot plugin which doesn't exist..
- Moved the configuration code to the lowest level, made settings to be common with all guis.
- /set command: /set [category[/key[=value]]] [all]
- /alias, /ignore and /unignore commands work again
- Nick completion finally working, and better than ever (unless it has bugs of course ;). It tries to be smart when completing, first it checks if someone with same letters had recently written message to you, then it checks for nicks that recently wrote messages and finally for the rest of the nicks in channel. Clicking tab more scans the list. Clicking tab in empty line completes to /msg &lt;nick who sent you last message>. Before trying to complete nicks, tab completion checks if the word is in setup's completion list.
- Wrote some functions to make possible handling events in different places depending where the command which created the event was sent. This is useful for example to notify list which needs to send ISON requests but user should still be able to use /ison command normally (this has always worked btw).
- Notify list's notify event now displays user's host and real name (made with the previous functions which grabbed WHOIS). Notify list GUI also updated for this
- You can use user/host masks with notify lists, wildcards are allowed. Nick must always be specified (could be fixed but everyone is invisible anyway so it would be useless). Examples: friend!**friend\*@\*, friend_!**friend\*@\*, another!\*@\*.blah.com, altnick!\*@\*.blah.com
- "your nick is owned by blah (blah@blah.org)" when connected
- Text formats page uses now GtkText widget, it displays colors too. It's not perfect but better than before...
- There's now three different colors indicating what's happened in channel: red = some text was written there, bright red = public message, magenta = public message to you
- Ignore checking is now done by stopping the entire signal so plugins etc. don't have to deal with them.
- You can use user/host masks with ignores
- Autoraise (in window menu) window when new message comes to channel
- Channel settings: You can specify list of bots (masks) and command to send the first one found bot (nice for auto-opping ourself)

### Fixes
{:#v0-7-8-fixes }

- Changing user modes from menus didn't work. Moved the menu under server menu.
- Speech plugin problems fixed.. It didn't compile without gnome libraries and with gnome libraries it didn't say anything because for some reason one line in sources was commented out..
- IRC network things and server password didn't work because of stupid little bug
- Configuration file handling was a bit broken in GTK version
- Rewrote menu handling in GTK version, it was crashing when trying to load plugins..

---

## 0.7.7
{:#v0-7-7 }

Timo Sirainen released this <abbr class="timeago" title="1999-04-05">1999-04-05</abbr> ▪ [unstable]

### Additions
{:#v0-7-7-additions }

- speech plugin :) This is currently made to work with festival (http://www.cstr.ed.ac.uk/projects/festival/), it's not very usable but nice to play with :)
- C-b (bold), C-c (color), C-g (bell), C-v (reverse), C-- (underline) keys work now but they don't display anything in entry line.
- Beel character beeps are now optional
- Fixes and new features for plugins. Each plugin has now it's own menu under plugin menu and "Unload" menuitem there by default.

### Fixes
{:#v0-7-7-fixes }

- GTK version didn't build .. again..
- I broke DCC send in 0.7.5
- SIGPIPE is ignored, maybe fixes some "crashes" when server connection is lost (I never got this btw.)
- Using irssi with click to focus sent commands to window where mouse cursor was..
- Fixed some bugs when scrollback buffer got full (GTK's text widget seems to crash sometimes with small scrollback buffer and _lots_ of text!)
- Plugin dialog didn't show any plugins
- Plugins are now created with automake things to make them portable for compilers/linkers that don't work with -shared switch. The disadvantage is that a lot of unnecessary files are created for each plugin (.a, .la, .so.0, .so.0.0, .so.0.0.0) while irssi uses only libplugin.so, could be fixed somehow but too difficult for me..
- Joining to +k channel crashed

---

## 0.7.6
{:#v0-7-6 }

Timo Sirainen released this <abbr class="timeago" title="1999-03-29">1999-03-29</abbr> ▪ [unstable]

### Changes
{:#v0-7-6-changes }

- New default colors .. I think they're better, not the best possible but anyway, I'm not good with these :)

### Additions
{:#v0-7-6-additions }

- Text mode version working again with colors! :)
- New settings/servers dialog, changed connect and channels dialogs. You can now automatically connect to multiple servers at startup. All this made by Kari Lavikka (tuner@bdb.fi)
- Server password support
- IRC proxy support
- Right clicking the channel name in panel pops up channel menu
- private ctcp and notice messages now show up in query windows if it exists for sender

### Fixes
{:#v0-7-6-fixes }

- Fixed logging a bit, you can now log stuff from nicks without having query window for them.
- If time stamps were enabled, log files had time stamps twice in each line
- Color settings had some bugs
- GNOME version crashed if ~/.irssi.conf didn't exist .. because I read the configuration file before gnome_init() which was necessary for "create gnome panel applet" option in setup -> removed it

---

## 0.7.5
{:#v0-7-5 }

Timo Sirainen released this <abbr class="timeago" title="1999-03-17">1999-03-17</abbr> ▪ [unstable]

### Changes
{:#v0-7-5-changes }

- Text mode version is broken and isn't built.
- Configuration file has changed quite a lot, might be better if you would just erase the old one.. Server configuration is also going to change soon..

### Additions
{:#v0-7-5-additions }

- Plugins are back! But unfortunately I can't get perl plugin to work. See TODO for more information.
- I divided setup dialogs to separate windows and grouped the options to different frames so they actually make some sense now :) Also some new options:
        - Create GNOME panel applet
        - Lots of DCC options, the page looked so lonely that I had
          to put more options there :)
            - get: autorename file if it exists (currently this is
              done always..)
            - autoget: max. file size to get
            - fast send (don't wait for responses from the other
              side, just keep sending the data..)
            - upload path
            - block size
            - timeout
- Checks for slang/slang.h too ..
- Text mode version doesn't have my name/nick hardcoded in it anymore :) Uses IRCNAME and IRCNICK environment variables.
- Status window is now optional, when enabled it grabs all "status" messages there. This needed quite a lot of inner changes, hopefully works :)
- /nctcp - send ctcp reply
- Window size is now saved when quitting and it's used when creating windows in next session

### Fixes
{:#v0-7-5-fixes }

- Fixed lots of GLib-CRITICAL messages when disconnected from server while it was still trying to find ip address.
- Window/find should now scroll to right position and it doesn't corrupt the text widget with inserting new texts to found texts positions.. It's also case-insensitive now.
- Fixed compile error when building without gnome panel..

---

## 0.7.4
{:#v0-7-4 }

Timo Sirainen released this <abbr class="timeago" title="1999-03-13">1999-03-13</abbr> ▪ [unstable]

### Additions
{:#v0-7-4-additions }

- Applet for GNOME panel working again
- You don't have to specify \-\-without-gnome anymore, configure checks this for you (finally)
- Some widget packing changes and tooltips for channel mode buttons by Kari Lavikka &lt;tuner@bdb.fi>
- Window/find moves the scrollbar to position where you can actually see the found text (usually, find prev misses it sometimes..)

### Fixes
{:#v0-7-4-fixes }

- Disconnect button in disconnect dialog still wasn't working.
- Channel mode buttons didn't change if channel wasn't focused
- I added separators to menus in v0.7.3, but forgot to make GTK version work with them
- Closing DCC chat crashed
- Destroying window with WM now really destroys the window, no hide it like it used to..
- Several fixes with window handling..

---

## 0.7.3
{:#v0-7-3 }

Timo Sirainen released this <abbr class="timeago" title="1999-03-11">1999-03-11</abbr> ▪ [unstable]

### Changes
{:#v0-7-3-changes }

- Text mode version is not called irssi-text so make install can install both of them without overwriting the other..

### Additions
{:#v0-7-3-additions }

- Window menu: find text, save window buffer, close window, new, new tabbed .. And lots of fixing code to make empty windows possible.
- After kicked from channel, the window isn't destroyed

### Fixes
{:#v0-7-3-fixes }

- While connecting to server and receiving "nick is temporarily unavailable" irssi didn't try different nick but got just stuck there.

---

## 0.7.2
{:#v0-7-2 }

Timo Sirainen released this <abbr class="timeago" title="1999-03-10">1999-03-10</abbr> ▪ [unstable]

### Additions
{:#v0-7-2-additions }

- GUI for logging, /log start, /log stop
- You can drag file from GMC over to nick in nicklist to send the file with DCC
- Nicklist changed to GtkCList, ops and voices are marked with pixmaps (stolen from X-Chat, someone want to do better ones?). Had to be done because adding drag'n'drop to GtkList was too slow..

### Fixes
{:#v0-7-2-fixes }

- Pretty bad bugs with GTK version fixed, using several dialogs' buttons crashed..
- WHOIS's idle line displayed seconds wrong. Maybe I finally got it fixed right this time.. :)
- Unknown commands still didn't work. They were sent to server with the / character at start..

---

## 0.7.1
{:#v0-7-1 }

Timo Sirainen released this <abbr class="timeago" title="1999-03-08">1999-03-08</abbr> ▪ [unstable]

### Changes
{:#v0-7-1-changes }

- The 0.7.0 was actually quite stable, I thought it would crash all the time by itself and do some weird things :)
- Hopefully now that GTK 1.2 is finished more people start using it and don't ask me to continue supporting GTK 1.0. So, this version requires GTK 1.1/1.2.

### Additions
{:#v0-7-1-additions }

- Started gui-text.. Should work somehow :) Prefers SLang but should work with curses also, except in X terminals I couldn't get colors out of it.
- Logging, still lacks GUI.
  
  Syntax:
    /log create &lt;filename> [&lt;+/->level ...] [#channel/nick [
                           [&lt;+/->level ...] ...]
    /log close &lt;filename>
    /log list
  
  Example: /log create mylog -all +msgs #linux +chan +public +notices (or simply #linux +all logs everything that appears in #linux window).
  
  You can use these levels, ALL is set by default: ALL, CRAP, PUBLIC, MSGS, NOTICES, WALLOPS, SNOTES, ACTIONS, DCC, CTCP, CLIENTNOTICES, CLIENTERRORS
- Automatically create query window when received msg (option)
- No more "WHO: unknown commmand"s, all unknown commands are sent to server just like they were written
- Working again: msgs window, aliases, /kickban, /knockout
- Changed quite a lot of GString's to g_strdup_printf
- cleaned configure.in

### Fixes
{:#v0-7-1-fixes }

- Disconnect button in disconnect dialog didn't work.
- Writing to DCC chat only sent the first word..
- setting ircnet to server record was done without strdup()ing from setup server record, so after disconnecting preferences or reconnecting could have crashed.

---

## 0.7.0
{:#v0-7-0 }

Timo Sirainen released this <abbr class="timeago" title="1999-02-25">1999-02-25</abbr> ▪ [unstable]

### Changes
{:#v0-7-0-changes }

- Lots and lots and LOTS of rewriting code. Hope you like it :) At least I do, mostly. GUI still needs rewriting but.. well, it works anyway now.
  
  The [unstable] tag in this version really means that IT IS UNSTABLE. See TODO for what features that 0.6.0 have are still missing.
  
  Because of the new great signaling system :) lots of things can be done easier. Now all the dialogs should be up to date, like channel mode dialog. When you receive ops, widgets come sensitive, when you lose your ops, the widgets become unsensitive.
  
  irssi source is now also divided in to separate directories:
  
  irc-base: this shouldn't change much, it has all basic functionality
            needed to create a working IRC client.
  
  irc-extra: all kinds of extra functionality: dcc, flood detection,
             ignore lists, (logging soon), notify lists and plugins.
  
  common-ui: here's all the functions that need to print some texts to
             screen.
  
  gui-gnome: GTK/GNOME specific code
  
  These haven't been started yet: ui-none: make irssi work as a bot with plugins/scripts ui-text: text mode interface gui-kde, ...: I'm not going to do these, anyone?

---

## 0.6.0
{:#v0-6-0 }

Timo Sirainen released this <abbr class="timeago" title="1999-02-12">1999-02-12</abbr> ▪ [unstable]

### Additions
{:#v0-6-0-additions }

- Plugins! See plugins/* and src/plugin-commands.h for more information
- Small PERL plugin, anyone want to continue developing this?
- Show menubar option

### Fixes
{:#v0-6-0-fixes }

- Some fixes and changes with clicking words.
- Notify list didn't work if ircnet was specified.
- socks5 needed -DSOCKS to work (but this is still untested..)

---

## 0.5.1
{:#v0-5-1 }

Timo Sirainen released this <abbr class="timeago" title="1999-02-10">1999-02-10</abbr> 

### Changes
{:#v0-5-1-changes }

- A big bugfix release, hopefully no crashes anymore? :)
- Removed intl directory, we don't have any i18n support yet so it's not needed...

### Additions
{:#v0-5-1-additions }

- Time stamps
- Use \-\-with-pthreads=no if they don't work right
- socks4/5 support (untested), use \-\-with-socks=no if you don't want them.

### Fixes
{:#v0-5-1-fixes }

- If you got kicked from channel irssi was in quite unstable state
- Using channel mode buttons in the upper right corner crashed
- Whois displayed idle time wrong
- Adding first item to empty list (notify, completions, aliases, ignores) crashed.
- It didn't actually compile without pthreads lib..
- If any texts contained %s, %d, etc.. irssi tried to expand them
- Solaris (and probably some others) need -D_REENTRANT flag to make threads work corretly.
- gtk_container_add() should be used instead of gtk_scrolled_window_add_with_viewport() when handling clists..

---

## 0.5.0
{:#v0-5-0 }

Timo Sirainen released this <abbr class="timeago" title="1999-02-08">1999-02-08</abbr> 

### Additions
{:#v0-5-0-additions }

- DCC CHAT, SEND, GET
- pthread support, no more blocking server connections.
- Notify list
- Getting more paranoid :) Added a lot of g_return_if_fail()s. Hopefully not in wrong places :) But these surely save some crashes with buggy code..
- BUILD_DOCK, HAVE_GNOME, etc. defines are now placed in config.h instead of being in -D arguments for gcc.
- Format strings are more flexible now, you can change the order of the parameters and you don't need to specify if the argument is supposed to be string or integer or .. Should be easy to use, %p1 matches the first argument, %p2 the seconds, etc.
- /PING

### Fixes
{:#v0-5-0-fixes }

- Changing topic from topic entry widget didn't work.
- If window had only one channel, the channel widgets (topic, modes, etc) didn't show up.
- Using popup menu from status window's channel lists crashed.
- Channel menu didn't work

---

## 0.4.1
{:#v0-4-1 }

Timo Sirainen released this <abbr class="timeago" title="1999-02-04">1999-02-04</abbr> 

### Additions
{:#v0-4-1-additions }

- Preferences: completion - if you type &lt;tag> in entry field and press tab it gets completed, like setting homepage to http://blah and typing: home page is homepage&lt;tab> -> home page is http://blah
- Tab nick completion.
- ':' nick completion also changed a bit.. If it fits to more than one nick it's completed in bash style. Like if there's mynick1 and mynik2, "my:" gets completed to "myni:"
- glib 1.0.6 didn't have g_get_user_name(), g_get_real_name(), g_get_home_dir() and g_strncasecmp(), made them..

### Fixes
{:#v0-4-1-fixes }

- Using \-\-no-applet crashed..
- Using items in user modes menu crashed
- Several small bugs fixed..

---

## 0.4.0
{:#v0-4-0 }

Timo Sirainen released this <abbr class="timeago" title="1999-02-01">1999-02-01</abbr> ▪ [unstable]

### Additions
{:#v0-4-0-additions }

- **Lots** of internal changes with window handling, fixed some memory leaks also while doing them. You can now have multiple real windows with tabbed subwindows in them. It's also possible to have multiple channels in one subwindow. Commands for handling these.. :
   - /join - Works like before, creates real or subwindow depending
     if "use tabbed windows" is set in setup.
   - /wjoin - Joins channel to current window
   - /hjoin - Creates new subwindow and joins there
   - /njoin - Creates new real window and join there
- Changed URL max length from 20 to 200.. Didn't realize it was that low :)
- Shows the nick who sent wallop, you need to change the second line in format texts from "%s" to "%s: %s" to make this it work. Need to do some kind of autoupgrading for formats that change..
- Found new functions from glib :)
    - g_getenv("HOME") -> g_get_home_dir()
    - getpw() -> g_get_user_name() and g_get_real_name()
    - strcasecmp() -> g_strcasecmp()
    - strncasecmp() -> g_strncasecmp()
- GNOME version uses ~/.irssi.conf if it exists

### Fixes
{:#v0-4-0-fixes }

- Opping/deopping anyone made irssi think that you were opped/deopped
- read_line() had some pretty bad bugs...

---

## 0.3.6
{:#v0-3-6 }

Timo Sirainen released this <abbr class="timeago" title="1999-01-29">1999-01-29</abbr> ▪ [unstable]

### Additions
{:#v0-3-6-additions }

- irssi.spec to easily build .rpm
- Preferences:
   - Alternative nick which is used when default nick is in use.
   - Create own window for msgs
   - Tab orientation
   - Flood settings
   - Max lines to keep in command line history
   - Scrollback buffer size
   - Text formats
- Toolbar .. we need pixmaps .. Needs also window (channel/query) specific items.
- Using horizontal panel works right now.
- Alt-1..0 changes between windows

### Fixes
{:#v0-3-6-fixes }

- Private actions didn't show up in query windows where they should have.
- Alias and ignores lists were mixed together and didn't work.
- Setting max channels to display in panel to -1 (which is default..) displayed actually only one channel.. Also setting this to 0 works.
- Topic didn't change when changing between windows in tabbed windows mode.
- When op received +v, @ was changed to + in nick list
- Connect/disconnect/channels dialogs fixed so that they won't crash when clicking buttons with empty lists.

---

## 0.3.5
{:#v0-3-5 }

Timo Sirainen released this <abbr class="timeago" title="1999-01-26">1999-01-26</abbr> 

### Additions
{:#v0-3-5-additions }

- Finished the channels dialog, you can automatically join to channels in specific irc networks.
- Changed the look of connect and disconnect dialogs
- servertest/ directory, just a test program to try if irssi crashes with _HEAVY_ network load (ie. if there's buffer overflows or some other weird bugs). It doesn't :)
- Preferences: Maximum number of channels to display in panel

### Fixes
{:#v0-3-5-fixes }

- When leaving from channels, panel didn't redraw it's list correctly
- Leaving channels in tabbed window mode crashed
- Fixed crash if connection got lost

---

## 0.3.4
{:#v0-3-4 }

Timo Sirainen released this <abbr class="timeago" title="1999-01-24">1999-01-24</abbr> ▪ [unstable]

### Additions
{:#v0-3-4-additions }

- Tabbed windows work a lot better
- User mode menu
- Preferences: default user mode

### Fixes
{:#v0-3-4-fixes }

- Connecting to more than one server crashed...
- Nick list redrawing was broken
- Dock applet wrote the texts to pixmap but didn't draw the pixmap into screen then properly..

---

## 0.3.3
{:#v0-3-3 }

Timo Sirainen released this <abbr class="timeago" title="1999-01-23">1999-01-23</abbr> ▪ [unstable]

### Additions
{:#v0-3-3-additions }

- /ignore never - never autoignore nick
- You can hide/show channel nick list from Channel menu, default state can be set from preferences.
- Preferences: Strip styles from text, misc options
- Launching URLs work!
- More str[nnn] -> GString changes, should be no more potential buffer overflows
- Started the tabbed windows, probably quite buggy and the window_create() code is getting REALLY ugly..

### Fixes
{:#v0-3-3-fixes }

- Servers didn't display QUIT message.. Couldn't think of any better way to fix this than not to disconnect the link but let the server do it.
- ANSI colors didn't work right

---

## 0.3.2
{:#v0-3-2 }

Timo Sirainen released this <abbr class="timeago" title="1999-01-22">1999-01-22</abbr> ▪ [unstable]

### Additions
{:#v0-3-2-additions }

- Dock applet, works at least with Enlightenment..

### Fixes
{:#v0-3-2-fixes }

- GTK version tried to move temp config file to real config file with rename() .. didn't work if /tmp and home were in different partitions.
- Some servers sent a mode change before /names list, irssi didn't like that and crashed..
- No more Gtk-Critical messages if irssi is run with \-\-no-applet

---

## 0.3.1
{:#v0-3-1 }

Timo Sirainen released this <abbr class="timeago" title="1999-01-22">1999-01-22</abbr> 

### Changes
{:#v0-3-1-changes }

- 4 days since last release. too long :) I'm now starting to create "unstable" versions of irssi. They have the latest and greatest features while they might not build/work too well. Check http://www.sicom.fi/~ikioma/irssi-download.html, new versions will probably be released quite often.
- GNOME version now builds without GNOME panel applet library
- Works with GTK+ 1.0.6 now, maybe with older too.

### Additions
{:#v0-3-1-additions }

- Connect / disconnect dialogs, channel dialog also started
- Server setup dialog changed some.
- Status window has a list of channels, queries and (yet not implemented) DCC chats. Also the tiny panel window isn't displayed unless you're running irssi in panel..
- Menu bar in all windows
- Cleaned read_line() to use GStrings.
- $(sysconfdir)/irssi.conf is copied to default user file if it isn't found.
- If you get kicked from channel the channel window won't get destroyed.

### Fixes
{:#v0-3-1-fixes }

- Query was in op submenu in nicklist's popup menu .. whops.
- 0.3.0 broke server tag generation so using multiple servers didn't work.

---

## 0.3.0
{:#v0-3-0 }

Timo Sirainen released this <abbr class="timeago" title="1999-01-18">1999-01-18</abbr> 

### Changes
{:#v0-3-0-changes }

- Config changes in GTK version, delete old .irssi.conf file (or change all "tag = values" to "tag=values")
- Default set of servers and aliases can be found from irssi.conf, copy that to ~/.gnome/irssi (if build with GNOME) or ~/.irssi.conf (if build without GNOME).

### Additions
{:#v0-3-0-additions }

- servers page added to preferences. Without connect dialog this is quite useless though :) But if you set "connect to IRC server at startup" on, irssi connects you to first local server.
- aliases :
   - /ALIAS &lt;alias> &lt;command to execute>
   - alias page added to preferences
   - these codes are extracted in commands:
       %0            : alias name
       %1, %2, %3 .. : word %
       &1, &2, &3 .. : word & + the rest of the text after it
       %c            : channel name
   - typing extra / before /command (//command) ignores any aliases
- ignore list :
   - /IGNORE &lt;mask> &lt;ignore level>
   - /UNIGNORE &lt;mask> &lt;ignore level>
   - ignore page added to preferences
   - ignore levels: ALL, CRAP, CHAN, PUBLIC, MSGS, NOTICES, WALLOPS,
     SNOTES, ACTIONS, DCC, CTCP, CLIENTNOTICES, CLIENTERRORS
- autoignoring msg and ctcp flooders
- options page added to preferences
- invite lists (channel mode I)
- !channels should work now
- replaced quite a lot of g_new()'s with GStrings. fixed one buffer overflow with this also..
- /AWAYALL - sends /away to all connected servers
- /KNOCKOUT [secs] &lt;nick> &lt;reason> - kick+ban+delay (5min)+unban

### Fixes
{:#v0-3-0-fixes }

- nick completion was case-sensitive
- again some minor bugs fixed and features added

---

## 0.2.1
{:#v0-2-1 }

Timo Sirainen released this <abbr class="timeago" title="1999-01-17">1999-01-17</abbr> 

### Additions
{:#v0-2-1-additions }

- Preferences: color and font selection
- gnome-stuff.c has some gnome_* compatible functions to get GTK+ version work. They're pretty slow and dum and maybe even buggy so if you want better, just compile the gnome libs :)
- Doubleclicking in topic sets the entry editable/uneditable

### Fixes
{:#v0-2-1-fixes }

- nick completion was buggy
- some minor bugs and features fixed

---

## 0.2.0
{:#v0-2-0 }

Timo Sirainen released this <abbr class="timeago" title="1999-01-16">1999-01-16</abbr> 

### Additions
{:#v0-2-0-additions }

- CTCP VERSION returns system name and revisions
- msgs window has now autoraise set on as default
- status window is used only when there's no window active..
- Done server handing:
   /server = /disconnect + /connect
   /connect = connects to new server without disconnecting from
              any old ones
   /disconnect = disconnect from current server
- msgs and status window have a server selector menu
- clicking a server tag in msgs window changes server
- channel information box
- \-\-no-panel command line switch so you can build with GNOME support but don't need to be running it in panel.

### Fixes
{:#v0-2-0-fixes }

- some automake fixes
- If someone was kicked, the kicker was removed from nick list insted of the kicked..
- Fixed some weird situtation where snapshot window wouldn't disappear from screen..

---

## 0.1.0
{:#v0-1-0 }

Timo Sirainen released this <abbr class="timeago" title="1999-01-14">1999-01-14</abbr> 

### Changes
{:#v0-1-0-changes }

- First release

