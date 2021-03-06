voice-dfki-ot
=============

A male Turkish unit selection voice for [MaryTTS], built from the [dfki-ot-data]

Prerequisites
-------------

You will need to have [Java], [Praat], [SoX], and the [Edinburgh Speech Tools] installed.

On OSX with [Homebrew], do

    brew cask install java praat
    brew install sox speech-tools

as needed.

On Debian-based Linux (including Ubuntu), do

    sudo apt-get install default-jdk praat sox speech-tools

accordingly.

Building the voice
------------------

To assemble, test, and package the voice for a [MaryTTS] installation, do

    ./gradlew build

The packaged files will be placed under `build/distributions`.
Copy the zip file and XML descriptor into your MaryTTS installation's `download` directory, then run the `marytts-component-installer` to install the voice.

Running the voice
-----------------

To build the voice and run it in an ad-hoc [MaryTTS] server, do

    ./gradlew run

Then, go to <http://localhost:59125>.

[dfki-ot-data]: https://github.com/marytts/dfki-ot-data
[Edinburgh Speech Tools]: http://www.cstr.ed.ac.uk/projects/speech_tools/
[Homebrew]: https://brew.sh/
[Java]: https://www.java.com/
[MaryTTS]: http://mary.dfki.de/
[Praat]: http://praat.org/
[SoX]: http://sox.sourceforge.net/
