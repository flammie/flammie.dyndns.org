# Finding out autooconf configure options of current autoconfed dir

It happens ever so often when configuring more complex less standard projects,
that you need a lot of `./configure` parameters. When you work with things like
scientific projects that are autoconfiscated, like mine are nowadays, there's 
a long list things to define and just one to wiggle around, the parameter to
test. To recall the parameters you used last time you can do:

    $ head config.log 
    This file contains any messages produced by compilers while
    [...]
    $ ./configure --with-moses=/home/flammie/Koodit/mosesdecoder --with-irstlm=/usr/local/irstlm --with-giza-tools=/home/flammie/Koodit/mgizapp/bin --with-mgizapp=/home/flammie/Koodit/mgizapp/bin

Presto. This can be now copypasted and changed. If you don't need to change the
parameters though, running make should do the trick, and update stuffs if
they've changed. But just in case, you may probably run `./config.status` by
hand too. At least for now, `config.status filename-without.in` will generate a
single file like that.

<!-- vim: set ft=markdown: -->
