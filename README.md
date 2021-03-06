Afrikaans and German: `apertium-afr-deu`
===============================================================================

This is an Apertium language pair for translating between Afrikaans and
German. What you can use this language package for:

* Translating between Afrikaans and German
* Morphological analysis of Afrikaans and German
* Part-of-speech tagging of Afrikaans and German

For information on the latter two points, see subheading "For more
information" below.

Requirements
-------------------------------------------------------------------------------

You will need the following software installed:

* lttoolbox (>= 3.3.0)
* apertium (>= 3.3.0)
* vislcg3 (>= 0.9.9.10297)
* apertium-afr
* apertium-deu

If this does not make any sense, we recommend you look at: apertium.org.

Compiling
-------------------------------------------------------------------------------

Given the requirements being installed, you should be able to just run:

    $ ./configure
    $ make
    # make install

You can use `./autogen.sh` instead of `./configure` you're compiling from
source. If you installed any prerequisite language packages using a `--prefix`
to `./configure`, make sure to give the same `--prefix` to `./configure` here.

Testing
-------------------------------------------------------------------------------

If you are in the source directory after running make, the following
commands should work:

    $  echo "Skryf" | apertium -d . afr-deu
    Schreiben

    $  echo "Schreiben" | apertium -d . deu-afr
    Skryf

After installing somewhere in `$PATH`, you should be able to do e.g.

    $  echo "Nodig" | apertium -d . afr-deu
    Brauchen

Files and data
-------------------------------------------------------------------------------

* `apertium-afr-deu.afr-deu.dix`  - Bilingual dictionary
* `apertium-afr-deu.afr-deu.t1x`  - Chunking rules for translating into German
* `apertium-afr-deu.deu-afr.t1x`  - Chunking rules for translating into Afrikaans
* `apertium-afr-deu.afr-deu.t2x`  - Interchunk rules for translating into German
* `apertium-afr-deu.deu-afr.t2x`  - Interchunk rules for translating into Afrikaans
* `apertium-afr-deu.afr-deu.t3x`  - Postchunk rules for translating into German
* `apertium-afr-deu.deu-afr.t3x`  - Postchunk rules for translating into Afrikaans
* `apertium-afr-deu.afr-deu.lrx`  - Lexical selection rules for translating into German
* `apertium-afr-deu.deu-afr.lrx`  - Lexical selection rules for translating into Afrikaans
* `modes.xml`                     - Translation modes

For more information
-------------------------------------------------------------------------------

* https://wiki.apertium.org/wiki/Installation
* https://wiki.apertium.org/wiki/apertium-afr-deu
* https://wiki.apertium.org/wiki/Using_an_lttoolbox_dictionary

Help and support
-------------------------------------------------------------------------------

If you need help using this language pair or data, you can contact:

* Mailing list: apertium-stuff@lists.sourceforge.net
* IRC: `#apertium` on `irc.oftc.net`

See also the file AUTHORS included in this distribution.

Errors
-------------------------------------------------------------------------------

Sometimes when translating, you will notice that a particular word gets translated
with a hash sign in front of it.
This is because of the current lack of transfer rules, which will be fixed in 
an upcoming update.
You did not do anything wrong; it was all me.

Additionally, if a word is (not) translated with an asterisk in front of it,
it means that that word is currently not supported and will be added soon.

