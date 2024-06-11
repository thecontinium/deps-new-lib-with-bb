# {{raw-name}}

{{description}}

## Usage

Invoke a library API function from the command-line:

    $ clojure -X {{top/ns}}.{{main/ns}}/foo :a 1 :b '"two"'
    {:a 1, :b "two"} "Hello, World!"

All commands can be run either directly as clojure commands or by using babashka.

Run the project's tests (they'll fail until you edit them):

    $ clojure -T:build test
    $ bb test

Run the project's CI pipeline and build a JAR (this will fail until you edit the tests to pass):

    $ clojure -T:build ci
    $ bb ci

This will produce an updated `pom.xml` file with synchronized dependencies inside the `META-INF`
directory inside `target/classes` and the JAR in `target`. You can update the version (and SCM tag)
information in generated `pom.xml` by updating `build.clj`.

Install it locally (requires the `ci` task be run first):

    $ clojure -T:build install
    $ bb install


Deploy it to Clojars -- needs `CLOJARS_USERNAME` and `CLOJARS_PASSWORD` environment
variables (requires the `ci` task be run first):

    $ clojure -T:build deploy
    $ bb deploy

Your library will be deployed to {{group/id}}/{{artifact/id}} on clojars.org by default.

Delete the locally deployed jar using

    $ clojure -T:build clean
    $ bb clean

Run an nrepl using

    bb repl

Run an nrepl for use with conjre


    bb conjure

## License

Copyright © {{now/year}} {{developer}}

_EPLv1.0 is just the default for projects generated by `deps-new`: you are not_
_required to open source this project, nor are you required to use EPLv1.0!_
_Feel free to remove or change the `LICENSE` file and remove or update this_
_section of the `README.md` file!_

Distributed under the Eclipse Public License version 1.0.