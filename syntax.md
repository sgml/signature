BEST SYNTAXES
XSLT - Template portability
Autohotkey - Desktop automation
Awk - text search
Scheme - game engine
Elisp - IDE customization
Excel - Data transformation
Logo - Game programming
Lua - Macro programming
Matlab - Data visualization
Powershell - Shell scripting
Vim Script - Editor customization


ERROR OBJECTS

Ruby: 
* RegExpError *
SystemStackError
SystemCallError (returns POSIX ErrNo constant)
SecurityError
NoMemoryError
NotImplementedError
NoMethodError
EncodingError 
Errno

PHP: 
* UnderflowException *
UnexpectedValueException
InvalidArgumentException 
posix-get-last-error() (returns POSIX ErrNo constant)

Python:
StopIteration 
EOFError 
IOError
AttributeError 
* UnicodeError *
AssertionError
os.strerror(code)

Perl: 
Insecure dependency in %s
Insecure directory in %s
Insecure user-defined property %s
Can't find string terminator %s anywhere before EOF
Out of memory during %s extend
Malformed UTF-8 character (%s)
Self-ties of arrays and hashes are not supported
* Range iterator outside integer range *
Use of each() on hash after insertion without resetting hash iterator results in undefined behavior
Argument "%s" isn't numeric%s
delete argument is index/value array slice, use array slice
delete argument is key/value hash slice, use hash slice
delete argument is not a HASH or ARRAY element or slice
Deep recursion on anonymous subroutine
Deep recursion on subroutine "%s"
Delimiter for here document is too long
Quantifier unexpected on zero-length expression in regex m/%s/
Unexpected ')' in regex; marked by <-- HERE in m/%s/
Unicode surrogate U+%X is illegal in UTF-8
POSIX::ErrNo

LOGGING APIS
ruby Logger.new(STDOUT)
python logging.getLogger
perl Log::Message::Simple
php error_log("Oracle database not available!", 0)

COMMAND LINE APIS
python [-bBdEhiOqsSuvVWx?] [-c command | -m module-name | script | - ] [args]
assoc .py=Python.File
ftype Python.File=C:\Path\to\pythonw.exe "%1" %*
https://docs.python.org/2/using/cmdline.html

php [--interactive-aRun PHP interactively. This lets you enter snippets of PHP code that directly get executed. When readline support is enabled you can edit the lines and also have history support.--bindpath address:port|port-b address:port|portBind Path for external FASTCGI Server mode (CGI only).--no-chdir-CDo not chdir to the script's directory (CGI only).--no-header-qQuiet-mode. Suppress HTTP header output (CGI only).--timing count-T countMeasure execution time of script repeated count times (CGI only).--php-ini path|file-c path|fileLook for php.ini file in the directory path or use the specified file--no-php-ini-nNo php.ini file will be used--define foo[=bar]-d foo[=bar]Define INI entry foo with value bar-eGenerate extended information for debugger/profiler--file file-f fileParse and execute file--global name-g nameMake variable name global in script.--help-hThis help--hide-args-HHide script name (file) and parameters (args...) from external tools. For example you may want to use this when a php script is started as a daemon and the command line contains sensitive data such as passwords.--info-iPHP information and configuration--syntax-check-lSyntax check only (lint)--modules-mShow compiled in modules--run code-r codeRun PHP code without using script tags '<?..?>'--process-begin code-B codeRun PHP code before processing input lines--process-code code-R codeRun PHP code for every input line--process-file file-F fileParse and execute file for every input line--process-end code-E codeRun PHP code after processing all input lines--syntax-highlight-sOutput HTML syntax highlighted source--version-vVersion number--stripped-wOutput source with stripped comments and whitespace--zend-extension file-z fileLoad Zend extension fileargs...Arguments passed to script. Use '--' args when first argument starts with '-' or script is read from stdin--rfunctionname--rfname Shows information about function name--rclassname--rcname Shows information about class name--rextensionname--rename Shows information about extension name--rextinfoname--riname Shows configuration for extension name--ini] 
assoc .php=phpfile
ftype phpfile="C:\PHP5\php.exe" -f "%1" -- %~2

ruby [--copyright] [--version] [-Sacdlnpswvy] [-0[octal]] [-C directory] [-F pattern] [-I directory] [-K c] [-T[level]] [-e command] [-i[extension]] [-r library] [-x[directory]] [--] [program_file] [argument ...] 
$ ftype RubyScript="c:\ruby\bin\ruby.exe" "%1" %*
$ assoc .rb=RubyScript
RubyScript="c:\ruby\bin\ruby.exe" "%1" %

perl[ -sTtuUWX ][ -hv ] [ -V[:configvar] ][ -cw ] [ -d[t][:debugger] ] [ -D[number/list] ][ -pna ] [ -Fpattern ] [ -l[octal] ] [ -0[octal/hexadecimal] ][ -Idir ] [ -m[-]module ] [ -M[-]'module...' ] [ -f ][ -C [number/list] ][ -P ][ -S ][ -x[dir] ][ -i[extension] ][ [-e|-E] 'command' ] [ -- ] [ programfile ] [ argument ]... 
ftype Perl=perl.exe "%1" %*
assoc .pl=Perl

BREAKPOINT DEBUGGING
python import pdb
perl perl -d
php phpdbg -e/path/to/my/script.php apd_set_pprof_trace();
ruby require 'debug'

DISABLE OUTPUT ESCAPING
php <<<'EOT' My name is "$name". 'EOT'
perl __DATA__
ruby __END__
python sys.exit(0) 

DEPRECATION WARNING
php E_DEPRECATED
python FutureWarning
perl warnings::warn("deprecated", "open is deprecated, use new instead");
ruby require 'rubygems/deprecate'

TEMPDIR
php fopen("php://temp:'hello'", 'r+');
python tempfile.tempdir
ruby Tempfile.new('hello', '/home/aisaka')
perl $tmpdir = File::Spec->tmpdir(); $tempfile = File::Temp->newdir();


VERSION STRING
python  sys.version
php phpversion()
perl PERL_VERSION
ruby RUBY_VERSION

BYTECODE COMPILATION
perl       perlcc myperlprogram.pl
ruby       RubyVM::InstructionSequence.compile("a = 1 + 2")
php        bcompiler_write_functions_from_file($fh,'module.php');
python     import compileall compileall.compile_file('module.py', force=True)

UNIVERSAL APIS
dom 
sax
regex
syslog
datetime
math
cgi
tk
trace
posix
glob
pack(c structs)
gdbm
MIME
csv

UNIT TESTS
python: https://github.com/python/cpython/tree/origin/master/Lib/test
ruby: https://github.com/rubygems/rubygems/tree/master/test/rubygems
perl: https://github.com/metacpan/metacpan-api/tree/master/t
php: https://github.com/php/php-src/tree/master/tests

AMBIGUITY
- A hash key has the same name as a reserved word
- % , & , and * are both infix operators (modulus, bitwise and, and multiplication) and
pass by reference/value flags
- foo[2] may be an array index, or a hash with the key '2'
- [ can delimit an array index, hash reference, or regexp range
- { can delimit a function scope, a conditional scope, or a regexp subset
- When switch to DST, the same local time happens twice on the same day
- Arbitrary expressions in a list comprehension allows for circular references
- Using setters allows for circular references $(foo).html(foo.replace("1","2")
- Using mixed tabs and spaces creates ambiguous scope in Python
- Using = for assignment and testing creates ambiguous statements in VBScript

OUTPUT BUFFERING 

Perl:
open my $fh, "<", "foo" or die $!;
local $/; # enable localized slurp mode
my $content = <$fh>;
close $fh;

OUTPUT FLUSHING

Perl:
open(LOG,">>$log");
LOG->autoflush(1);

SHORT CIRCUIT EVALUATION

PHP:
$realchoice = $userchoice or $realchoice = $systemchoice or $realchoice = $defaultchoice;

TEMPLATE INCLUDE

Perl:
require "test.pl";

PARAMETERIZED QUERY /PREPARED STATEMENT

Ruby:

require 'dbi'

dbh = DBI.connect('DBI:Oracle:sid', 'user', 'password')

sth = dbh.prepare('select table_name, tablespace_name from user_tables 
                   where table_name like ?')

sth.execute('foo')

require 'dbi'
class Quoter ; include DBI::SQL::BasicQuote ; end
st = DBI::SQL::PreparedStatement.new(Quoter.new, "Select * from table where x = ?")
st.bind(['test'])

STRUCT EXISTENCE
Python:

def isstruct(node):
  return isinstance(node, dict)

JSONify
JavaScript:
JSON.parse(JSON.stringify(foo))

ARRAY CLONE
JavaScript:
function arrayClone(arr)
  {
  return Array.apply(undefined, arr);
  }

STRING REVERSE
JavaScript
function reverseString(str)
  {
  return String(str).split("").reverse().join("");
  }

WORD REVERSE
JavaScript
function reverseWord(str)
  {
  return String(str).split(" ").reverse().join(",")
  }

STRING REPEAT
JavaScript
function Repeat(char, times)
  {
  return Array(times).join(char);
  }

ERROR LOGGING
JavaScript:
window.onerror = function(message, url, lineNumber) {
	var params = [];
	params[0] = 'location=' + url || document.location.origin;
	params[1] = 'data=' + navigator.userAgent + '|' + navigator.vendor + '|' + navigator.platform;
	params[2] = 'lineNumber=' + lineNumber;
	params[3] = 'message=' + message;
	params[4] = 'os=' + Core.Client.OS;
	params[5] = 'url=' + Core.Client.url;
	params[6] = 'version=' + Core.Client.version;
	};


UPPERCASING
JavaScript:
//Local
foo = [];
foo.toUpperCase = String(foo).toUpperCase;
foo.push("a");
foo.toUpperCase();

//Global
foo = [];
window.toUpperCase = function (obj) {return String(obj).toUpperCase();}
foo.push("a")
toUpperCase(foo)

//Constructor
var toUpperCase = Function("obj","return String.prototype.toUpperCase.call(obj)")

//Bind
var toUpperCase = Function.call.bind(String.prototype.toUpperCase);

HTML HEAD TAG INSERTION
Ruby:

saved_stdout = $stdout
begin
    output = File.open("report.lout","w")
    $stdout = output
    ERuby::import('report.rl')
    output.close
end
$stdout = saved_stdout

ARRAY JOIN
Write a function that takes two arrays of integers and returns a list that contains the set intersection of the arrays.n
JavaScript:
function foo(bar, baz)
  {
  foo.boo = new List();
  foo.hash = {};
  bar.map(function(index, value){
    foo.hash[value] = appender;    
  }
  
  baz.map(function(index, value){
    if typeof foo.hash[value] == Function
      foo.hash[value](value)
  }
  
  function appender(value)
      {
      List.append(value);
      }
     
  
  foo([1,2,3],[2,2,3]) // returns [2,3]
  foo([1,1,1],[1,1,1]) // returns [1,1,1]
  

PROBLEMS
perl - boolean 
python - yield 
ruby - nil 
php - $this
tcl - concat
lua - stringify

EXAMPLES
http://php.net/manual/en/indexes.examples.php


UNIQUE FEATURES
lua - object literal, regexp, OpenGL, queue, method dispatch table, synchronous concurrency, keyword overloading
perl - file streams, higher order functions
python - tuple, decorator, global functions, sys.exc_info, py_compile, from foo import bar
ruby - variable interpolation in heredocs, Fiber(generator), $LOADED_FEATURES, $LOAD_PATH, $PROGRAM_NAME
PHP - strings are byte arrays, print_r
Node - require.cache, closures have private variables, file scoped variables via let

References
http://rigaux.org/language-study/syntax-across-languages.html
http://t-a-w.blogspot.com/2007/02/right-to-criticize-programming.html
http://www.cs.colorado.edu/~siek/pubs/pubs/2003/comparing_generic_programming03.pdf
https://en.wikipedia.org/wiki/Pure_(programming_language)
https://en.wikipedia.org/wiki/POCO_C%2B%2B_Libraries
https://en.wikipedia.org/wiki/Falcon_(programming_language)
https://msdn.microsoft.com/en-us/library/aa480201.aspx
  http://ruby-php.org/thesis/translating-ruby-to-php-view.pdf

 * [IDL API](http://www.w3.org/TR/DOM-Level-2-Core/idl-definitions.html)
 * [Java API](http://www.w3.org/2003/01/dom2-javadoc/index.html)
 * [ANSI C API](http://freecode.com/projects/domc)
 * [C++ API](http://xerces.apache.org/xerces-c/program-dom-3.html)
 * [.Net API](http://msdn.microsoft.com/en-us/library/6kza7w4k.aspx)
 * [Ada API](http://docs.adacore.com/xmlada-docs/dom.html)
 * [Haskell API](http://hackage.haskell.org/package/ghcjs-dom)
 * [PHP API](http://www.php.net/manual/en/book.dom.php)
 * [Python API](http://docs.python.org/3/library/xml.dom.html)
 * [Perl API](http://search.cpan.org/~tjmather/XML-DOM-1.44/lib/XML/DOM.pm)
 * [Ruby API](http://yard.ruby-doc.org/stdlib-2.0/Microsoft_XMLDOM_1_0.html)
 * [Tcl API](http://tdom.github.io/)
 * [Lua API](https://launchpad.net/lua-dom)
 * [Haxe API](http://api.haxe.org/js/html/Document.html)
 * [FreePascal API](http://wiki.freepascal.org/XML_Tutorial)
 * [Delphi API](http://docwiki.embarcadero.com/Libraries/XE5/en/Xml.Win.msxmldom)
 * [Qt API](https://qt-project.org/doc/qt-4.8/xml-dom-tml.html)
 * [WSH API](http://msdn.microsoft.com/en-us/library/aa923288.aspx)
 * [Emacs API](http://www.emacswiki.org/emacs/dom.el)
 * [Eiffel API](http://eiffel-edom.sourceforge.net/)
 * [JavaScript API](http://www.w3.org/TR/DOM-Level-2-Core/ecma-script-binding.html)
 * [ActionScript API](https://github.com/stickupkid/as3-dom)
 * [Visual Basic API](http://msdn.microsoft.com/en-us/library/ms766564)
 * [AutoHotKey API](https://www.autoitscript.com/autoit3/docs/functions/ObjCreate.htm)
 * [PowerShell API](http://msdn.microsoft.com/en-us/magazine/cc337896.aspx)

as would SAX:

 * [IDL API](http://www.exelisvis.com/docs/IDLffXMLSAX.html)
 * [Java API](http://www.saxproject.org/apidoc/)
 * [.Net API](http://sourceforge.net/p/saxdotnet/code/)
 * [C++ API](http://www.jezuk.co.uk/cgi-bin/view/arabica)
 * [Qt API](http://doc.qt.digia.com/4.6/xml-sax.html)
 * [Haskell API](http://hackage.haskell.org/package/libxml-sax-0.2)
 * [Erlang API](http://www.erlang.org/documentation/doc-1/man/xmerl_sax_parser.html)
 * [Eiffel API](http://www.gobosoft.com/eiffel/gobo/xml/using.html)
 * [Ada API](http://docs.adacore.com/xmlada-docs/sax.html)
 * [Objective-C API](http://expatobjc.sourceforge.net/)
 * [ActionScript API](https://github.com/lyokato/as3saxparser)
 * [JavaScript API](https://github.com/isaacs/sax-js)
 * [Visual Basic API](http://msdn.microsoft.com/en-us/library/ms765394)
 * [Delphi API](http://saxforpascal.sourceforge.net/)
 * [Perl API](https://metacpan.org/pod/XML::SAX::Base)
 * [Ruby API](http://www.rubydoc.info/gems/sax-machine/1.2.0/SAXMachine/SAXAbstractHandler)
 * [Python API](https://docs.python.org/2/library/xml.sax.html)
 * [PHP API](http://php.net/manual/en/book.xml.php)
 * [Lua API](https://github.com/Phrogz/SLAXML)
 * [Tcl API](http://wiki.tcl.tk/4786)

KEYWORDS/BAREWORDS/RESERVED WORDS
http://php.net/manual/en/reserved.keywords.php
https://docs.ruby-lang.org/en/2.2.0/keywords_rdoc.html
https://docs.python.org/3/reference/lexical_analysis.html#keywords
http://learn.perl.org/docs/keywords.html#barewords

LOGGERS
http://ruby-doc.org/stdlib-2.1.1/libdoc/logger/rdoc/Logger.html
http://ruby-doc.org/stdlib-2.1.1/libdoc/syslog/rdoc/Syslog.html
https://docs.python.org/3.2/howto/logging-cookbook.html
http://perldoc.perl.org/Log/Message/Simple.html
http://php.net/manual/en/function.error-log.php
http://php.net/manual/en/errorfunc.configuration.php

TRACERS
https://msdn.microsoft.com/en-us/library/system.diagnostics.trace
http://perldoc.perl.org/perldtrace.html
http://php.net/manual/en/features.dtrace.introduction.php
