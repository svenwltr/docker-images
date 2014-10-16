haskell docker image
====================

Usage example:

    docker run --rm -it --volume "$PWD:/cwd" svenwltr/haskell ghci
    docker run --rm -it --volume "$PWD:/cwd" svenwltr/haskell ghc

or add command to `.bashrc`:

	function ghci() {
        docker run --rm -it --volume "$PWD:/src" svenwltr/haskell \
        ghci "$@"
    }



### Disclaimer

I am a haskell noob, so this image may not fit anyone elses needs.

