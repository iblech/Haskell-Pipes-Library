# Pipes v3.3.0

`pipes` is an easy, elegant, and powerful framework for describing streaming
behaviors.

## Quick start

* Install the [Haskell Platform](http://www.haskell.org/platform/)
* `cabal install pipes`

Then fire up ` ghci`:

    $ ghci
    Prelude> import Control.Proxy as P

... and echo standard input to standard output until you enter `quit`.

    Prelude P> runProxy $ stdinS >-> takeWhileD (/= "quit") >-> stdoutD
    Test[Enter]
    Test
    Apple[Enter]
    Apple
    quit[Enter]
    Prelude P> -- Done!

Now read [the official tutorial](http://hackage.haskell.org/packages/archive/pipes/3.3.0/doc/html/Control-Proxy-Tutorial.html).

## Features

* *Concise API*: Use three simple commands: `(>->)`, `request`, and `respond`

* *Bidirectionality*: Implement duplex channels 

* *Blazing fast*: Implementation tuned for speed 

* *Elegant semantics*: Use practical category theory

* *Extension Framework*: Mix and match extensions and create your own

* *ListT*: Correct implementation of `ListT` that interconverts with pipes 

* *Lightweight Dependency*: `pipes` depends only on `transformers` and `mmorph`
  and compiles rapidly

* *Extensive Documentation*: Second to none!

## Community Resources

* [Haskell wiki page](http://www.haskell.org/haskellwiki/Pipes)

* [Mailing list](haskell-pipes@googlegroups.com) ([Google Group](https://groups.google.com/forum/?fromgroups#!forum/haskell-pipes))

## How to contribute

* Contribute code

* Build derived libraries

* Write `pipes` tutorials

## Copyright

Copyright (c) 2012, 2013 Gabriel Gonzalez
All rights reserved.

Redistribution and use in source and binary forms, with or without modification,
are permitted provided that the following conditions are met:

* Redistributions of source code must retain the above copyright notice, this
  list of conditions and the following disclaimer.

* Redistributions in binary form must reproduce the above copyright notice, this
  list of conditions and the following disclaimer in the documentation and/or
  other materials provided with the distribution.

* Neither the name of Gabriel Gonzalez nor the names of other contributors may
  be used to endorse or promote products derived from this software without
  specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR
ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
(INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON
ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
