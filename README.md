          GEN, a powerfull editor, inspired by GNU nano
          
History

    Compound word *genano* means “born of nano”, with command gen.
    This repository displays a full customisation of nano for Linux,
    without any internationalisation (code editor is in English US).
    
    *gen* is an Old Welsh and Medieval Breton word associated with
    “family, birth, origin, born of”, ultimately related to the
    reconstructed Proto-Celtic word *genos*, “kin, family, birth”.
    The word also naturally evokes *genesis* and *genetics*, and
    both cognates are seemingly connected to the historically and
    broader Indo-European root concerning birth and (re)generation.


    The original content of the nano README file is displayed below:
    ---------------------------------------------------------------


          GNU nano -- a simple editor, inspired by Pico

Purpose

    Nano is a small and simple text editor for use on the terminal.
    It copied the interface and key bindings of the Pico editor but
    added several missing features: undo/redo, syntax highlighting,
    line numbers, softwrapping, multiple buffers, selecting text by
    holding Shift, search-and-replace with regular expressions, and
    several other conveniences.

Appearance

    In rough ASCII graphics, this is what nano's screen looks like:

   ____________________________________________________________________
  |  GNU nano 9.2                  filename                  Modified  |
   --------------------------------------------------------------------
  | This is the text window, displaying the contents of a 'buffer',    |
  | the contents of the file you are editing.                          |
  |                                                                    |
  | The top row of the screen is the 'title bar'; it shows nano's      |
  | version, the name of the file, and whether you modified it.        |
  | The two bottom rows display the most important shortcuts; in       |
  | those lines ^ means Ctrl.  The third row from the bottom shows     |
  | some feedback message, or gets replaced with a prompt bar when     |
  | you tell nano to do something that requires extra input.           |
  |                                                                    |
   --------------------------------------------------------------------
  |                       [ Some status message ]                      |
  |^G Help       ^O Write Out  ^F Where Is   ^K Cut        ^T Execute  |
  |^X Exit       ^R Read File  ^\ Replace    ^U Paste      ^J Justify  |
   --------------------------------------------------------------------

Origin

    The nano project was started in 1999 because of a few "problems"
    with the wonderfully easy-to-use and friendly Pico text editor.

    First and foremost was its license: the Pine suite does not use
    the GPL, and (before using the Apache License) it had unclear
    restrictions on redistribution.  Because of this, Pine and Pico
    were not included in many GNU/Linux distributions.  Furthermore,
    some features (like go-to-line-number or search-and-replace) were
    unavailable for a long time or require a command-line flag.  Yuck.

    Nano aimed to solve these problems by: 1) being truly free software
    by using the GPL, 2) emulating the functionality of Pico as closely
    as is reasonable, and 3) including extra functionality by default.

    Nowadays, nano wants to be a generally useful editor with sensible
    defaults (linewise scrolling, no automatic line breaking).

    The nano editor is an official GNU package.  For more information
    on GNU and the Free Software Foundation, see https://www.gnu.org/.

License

    Nano's code and documentation are covered by the GPL version 3 or
    (at your option) any later version, except for two functions that
    were copied from busybox which are under a BSD license.  Nano's
    documentation is additionally covered by the GNU Free Documentation
    License version 1.2 or (at your option) any later version.  See the
    files COPYING and COPYING.DOC for the full text of these licenses.

    When in any file of this package a copyright notice mentions a
    year range (such as 1999-2011), it is a shorthand for a list of
    all the years in that interval.

How to compile and install nano

    Download the latest nano source tarball, and then:

        tar -xvf nano-x.y.tar.gz
        cd nano-x.y
        ./configure
        make
        make install

    You will need the header files of ncurses installed for ./configure
    to succeed -- get them from libncurses-dev (Debian) or ncurses-devel
    (Fedora) or a similarly named package.  Use --prefix with ./configure
    to override the default installation directory of /usr/local.  And
    use --sysconfdir=/etc when you want your self-compiled nano to read
    the /etc/nanorc file.

    After installation you may want to copy the doc/sample.nanorc file
    to your home directory, rename it to ".nanorc", and then edit it
    according to your taste.

Web Page

    https://nano-editor.org/

Mailing Lists

    There are three nano-related mailing-lists.

    * <info-nano@gnu.org> is a very low traffic list used to announce
      new nano versions or other important info about the project.

    * <help-nano@gnu.org> is for those seeking to get help without
      wanting to hear about the technical details of its development.

    * <nano-devel@gnu.org> is the list used by the people that make nano
      and a general development discussion list, with moderate traffic.

    To subscribe, send email to <name>-request@gnu.org with a subject
    of "subscribe", where <name> is the list you want to subscribe to.

    The archives of the development and help mailing lists are here:

        https://lists.gnu.org/archive/html/nano-devel/
        https://lists.gnu.org/archive/html/help-nano/

Bug Reports

    If you find a bug, please file a detailed description of the problem
    on nano's issue tracker: https://savannah.gnu.org/bugs/?group=nano
    (you will need an account to be able to do so), or send an email
    to the nano-devel list (no need to subscribe, but mention it if
    you want to be CC'ed on an answer).
    

##########################################################################

                                 AUTHORS

Below section lists people who have made significant contributions to the
nano editor, and it was previously located on a single file named AUTHORS,
in GNU nano. Please see the ChangeLog for specific changes by author.
--------------------------------------------------------------------------


Chris Allegretta <chrisa@asty.org>
	* Original program author and long-time maintainer.

Benno Schulenberg <bensberg@telfort.nl>
	* An array of small bug fixes, the cut-word and block-jump
	  routines, text selection by holding Shift, macro recording
	  and replay, extra key bindings, the --indicator, --minibar,
	  and --zero options, and braced functions in string binds.
	  Current maintainer.

David Lawrence Ramsey <pooka109@gmail.com>
	* Multiple-buffer support, operating-dir option (-o), bug fixes
	  for display routines, wrapping code, spelling fixes, parts of
	  UTF-8 support, softwrap overhaul, constantshow mode, undoable
	  indentations, undoable justifications, justifiable regions,
	  and numerous other fixes.  Former stable-series maintainer.

Jordi Mallach <jordi@gnu.org>
	* Debian package maintainer, fellow bug squasher, translator
	  for Catalan.  Former head of internationalization support.

Adam Rogoyski <rogoyski@cs.utexas.edu>
	* New write_file() function, read_file() optimization, mouse
	  support, resize support, nohelp (-x) option, justify function,
	  follow symlink option and bugfixes, and much more.

Robert Siemborski <rjs3@andrew.cmu.edu>
	* Miscellaneous cut, display, replace, and other bug fixes,
	  original and new "magic line" code, read_line() function,
	  new edit display routines.

Rocco Corsi <rocco.corsi@sympatico.ca>
	* Internal spelling code, many optimizations and bug fixes
	  for findnextstr() and search-related functions, various
	  display and file-handling fixes.

David Benbennick <dbenbenn@math.cornell.edu>
	* Wrap and justify bugfixes/enhancements, new color syntax
	  code, memleak fixes, parts of the UTF-8 support, and other
	  miscellaneous fixes.

Mike Frysinger <vapier@gentoo.org>
	* Whitespace display mode, --enable-utf8/--disable-utf8 configure
	  options for ncurses, many new color regexes and improvements to
	  existing ones in syntax/*.nanorc, the move from svn to git, the
	  conversion to gnulib, and miscellaneous bug fixes.  Former
	  Gentoo package maintainer.

Mark Majeres <mark@engine12.com>
	* A functional undo/redo system, and coloring nano's interface.

Mahyar Abbaspour <mahyar.abaspour@gmail.com>
	* Improved handling of SIGWINCH.

Mike Scalora <mike@scalora.org>
	* The comment/uncomment feature.

Faissal Bensefia <faissaloo@gmail.com>
	* Line numbers.

Sumedh Pendurkar <sumedh.pendurkar@gmail.com>
	* The word-completion feature.

Rishabh Dave <rishabhddave@gmail.com>
	* Searchable help.

Marco Diego Aurélio Mesquita <marcodiegomesquita@gmail.com>
	* Filtering text through an external command.
	* Placing anchors (bookmarks) and jumping to them.

Brand Huntsman <alpha@qzx.com>
	* The delayed parsing of syntax files.


##########################################################################

                               TRANSLATIONS

Below section lists people who have made translations for the nano editor,
and it was previously located on a single file named THANKS, in GNU nano.

--------------------------------------------------------------------------

Pedro Albuquerque <palbuquerque73@gmail.com>          Portuguese
Zayed Al-Saidi <zayed.alsaidi@gmail.com>              Arabic
Josef Andersson <josef.andersson@fripost.org>         Swedish
Mario Blättermann <mario.blaettermann@gmail.com>      German
Besnik Bleta <besnik@programeshqip.org>               Albanian
Laurențiu Buzdugan <buzdugan@voyager.net>             Romanian
Ricardo Cárdenes Medina <ricardo@conisys.com>         Spanish
Antonio Ceballos <aceballos@gmail.com>                Spanish
Wei-Lun CHAO <chaoweilun@pcmail.com.tw>               Chinese (traditional)
Seong-ho Cho <darkcircle.0426@gmail.com>              Korean
Yuri Chornoivan <yurchor@ukr.net>                     Ukrainian
Marco Colombo <magicdice@inwind.it>                   Italian
Mihai Cristescu <mihai.cristescu@archlinux.info>      Romanian
Yavor Doganov <yavor@doganov.org>                     Bulgarian
Karl Eichwalder <keichwa@gmx.net>                     German
A. Murat EREN <meren@comu.edu.tr>                     Turkish
Sveinn í Felli <sv1@fellsnet.is>                      Icelandic
Marek Felšöci <marek@felsoci.sk>                      Slovak
Doruk Fisek <dfisek@fisek.com.tr>                     Turkish
Rafael Fontenelle <rffontenelle@gmail.com>            Brazilian Portuguese
Pavel Fric <pavelfric@seznam.cz>                      Czech
Jorge González <aloriel@gmail.com>                    Spanish
Jean-Philippe Guérard <jean-philippe.guerard@laposte.net>  French
Václav Haisman <V.Haisman@sh.cvut.cz>                 Czech
Takeshi Hamasaki <hmatrjp@users.sourceforge.jp>       Japanese
Geir Helland <pjallabais@users.sourceforge.net>       Norwegian Bokmål
Tedi Heriyanto <tedi_h@gmx.net>                       Indonesian
Kjetil Torgrim Homme <kjetilho@linpro.no>             Norwegian Nynorsk
Szabolcs Horvath <horvaths@janus.gimsz.sulinet.hu>    Hungarian
Jorma Karvonen <karvonen.jorma@gmail.com>             Finnish
Mehmet Kececi <mkececi@mehmetkececi.com>              Turkish
Gabor Kelemen <kelemeng@gnome.hu>                     Hungarian
Kalle Kivimaa <kalle.kivimaa@iki.fi>                  Finnish
Eivind Kjørstad <ekj@vestdata.no>                     Norwegian Nynorsk
Florian König <floki@bigfoot.com>                     German
Klemen Košir <klemen913@gmail.com>                    Slovenian
Wojciech Kotwica <wkotwica@post.pl>                   Polish
Clement Laforet <clem_laf@wanadoo.fr>                 French
Ask Hjorth Larsen <asklarsen@gmail.com>               Danish
LI Daobing <lidaobing@gmail.com>                      Chinese (simplified)
Jordi Mallach <jordi@gnu.org>                         Catalan
João Victor Duarte Martins <jvdm@sdf.lonestar.org>    Brazilian Portuguese
Pavel Maryanov <acid@jack.kiev.ua>                    Russian
Daniele Medri <madrid@linux.it>                       Italian
Baurzhan Muftakhidinov <baurthefirst@gmail.com>       Kazakh
Gergely Nagy <algernon@debian.org>                    Hungarian
Claudio Neves <cneves@nextis.com>                     Brazilian Portuguese
Kalle Olavi Niemitalo <kon@iki.fi>                    Finnish
Мирослав Николић <miroslavnikolic@rocketmail.com>     Serbian
Lauri Nurmi <lanurmi@iki.fi>                          Finnish
Daniel Nylander <po@danielnylander.se>                Swedish
Mikel Olasagasti <hey_neken@mundurat.net>             Basque
Yi-Jyun Pan <pan93412@gmail.com>                      Chinese (traditional)
Michael Piefel <piefel@informatik.hu-berlin.de>       German
Sergey Poznyakoff <gray@gnu.org>                      Polish
Božidar Putanec <bozidarp@yahoo.com>                  Croatian
Trần Ngọc Quân <vnwildman@gmail.com>                  Vietnamese
Sharuzzaman Ahmat Raslan <sharuzzaman@excite.com>     Malay
Sergey A. Ribalchenko <fisher@obu.ck.ua>              Ukrainian and Russian
Michel Robitaille <robitail@IRO.UMontreal.CA>         French
Christian Rose <menthos@menthos.com>                  Swedish
Dimitriy Ryazantcev <DJm00n@mail.ru>                  Russian
Stig E Sandø <stig@ii.uib.no>                         Norwegian Bokmål
Kevin Patrick Scannell <kscanne@gmail.com>            Irish
Benno Schulenberg <benno@vertaalt.nl>                 Dutch and Esperanto
Danilo Segan <dsegan@gmx.net>                         Serbian
Clytie Siddall <clytie@riverland.net.au>              Vietnamese
Keld Simonsen <keld@dkuug.dk>                         Danish
Guus Sliepen <guus@nl.linux.org>                      Dutch
Cezary Sliwa <sliwa@cft.edu.pl>                       Polish
Johnny A. Solbu <johnny@solbu.net>                    Norwegian Bokmål
Pierre Tane <tanep@bigfoot.com>                       French
Yasuaki Taniguchi <yasuakit@gmail.com>                Japanese
Jacobo Tarrío <jtarrio@trasno.net>                    Galician
Andika Triwidada <andika@gmail.com>                   Indonesian
Francisco Javier Tsao Santín <tsao@members.fsf.org>   Galician
Balázs Úr <urbalazs@gmail.com>                        Hungarian
Luca Vercelli <luca.vercelli.to@gmail.com>            Italian
Miquel Vidal <miquel@sindominio.net>                  Catalan
Phan Vinh Thinh <teppi82@gmail.com>                   Vietnamese
Pauli Virtanen <pauli.virtanen@saunalahti.fi>         Finnish
Aron Xu <happyaron.xu@gmail.com>                      Chinese (simplified)
Boyuan Yang <073plan@gmail.com>                       Chinese (simplified)
Peio Ziarsolo <peio@sindominio.net>                   Basque
Anton Zinoviev <zinoviev@debian.org>                  Bulgarian


Other stuff:
===========
Ben Armstrong <synrg@sanctuary.nslug.ns.ca>    Negative -r value idea, code
Thomas Dickey <dickey@herndon4.his.com>        Curses help and advice
Kamil Dudka <kdudka@redhat.com>                Several small bug fixes
Sven Guckes <guckes@math.fu-berlin.de>         Advice and advocacy
Thijs Kinkhorst <thijs@kinkhorst.com>          rnano.1 manpage
Jim Knoble <jmknoble@pobox.com>                Pico compat for browser
Ryan Krebs <fluffy@highwire.stanford.edu>      Many bug fixes and testing
Roy Lanek <lanek@ranahminang.net>              Advice and advocacy
Chuck Mead <csm@MoonGroup.com>                 Feedback and RPM stuff
Mike Melanson <melanson@pcisys.net>            Bug reports
Neil Parks <nparks@acsmail.com>                Bug reports and fixes
Jeremy Robichaud <robicj@yahoo.com>            Beta tester
Bill Soudan <wes0472@rit.edu>                  Regex code, etc
Ken Tyler <kent@werple.net.au>                 Search fixes and more


