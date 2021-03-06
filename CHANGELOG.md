# Changes

* 1.0.199 -- 2020-04-10
  * Add documentation on how to find 3rd party templates (PR #37, @holyjak).
  * Update to `depstar` 1.0.94 and `test.check` 1.0.0 in templates.
  * Move to MAJOR.MINOR.COMMITS versioning scheme.
* 0.9.0 -- 2020-02-13
  * Remove Jackson dependencies since `tools.deps.alpha` no longer brings in a version (after the S3 Transporter change), so there's no longer a potential conflict with templates.
  * Various documentation improvements.
* 0.8.6 -- 2020-01-24
  * Attempt to fix #33 by bumping dependencies across the board. Note: we still pin Jackson to 2.7.5 to reduce transitive version conflicts in (Leiningen) templates.
* 0.8.5 -- 2020-01-17
  * Add `install`/`deploy` aliases to `lib`/`template` project generators.
* 0.8.4 -- 2020-01-02
  * Update to `depstar` 0.5.1 for bug fix to main namespaces containing `-`.
* 0.8.3 -- 2020-01-02
  * Update to `depstar` 0.5.0 and remove `classes` folder since `depstar` manages that automatically now.
* 0.8.2 -- 2019-12-31
  * Addresses #30 by updating `depstar` to 0.4.1 and relying on its `-C` option for AOT in `app`'s `:uberjar` alias.
  * Fixes #29 by changing group/artifact in `template` project.
  * Ensure `.keep` is a file, not a directory.
* 0.8.1 -- 2019-12-29
  * Adds `pom.xml` generation to `app` built-in template.
  * Adds `:uberjar` alias to `app` built-in template and `:jar` alias to `lib` and `template` built-in templates.
  * Expand documentation for built-in templates, including environment variables used in `pom.xml` files.
* 0.8.0 -- 2019-12-25
  * Fixes #28 by adding `-?` / `--query` option to explain what `clj-new` will attempt to do.
  * Fixes #27 by adding `-e` / `--env` option to add "environment variables" that will be available to templates via the new `project-data` function; also standardizes the data passed to the `app`, `lib`, and `template` built-in templates.
  * Fixes #25 by adding `pom.xml` to `lib` and `template` built-in templates.
  * Fixes some issues with the `template` project generator.
  * Update `seancorfield/clj-new` coordinates in generated projects (to use current version).
  * Update Cognitect's `test-runner` to latest SHA in generated projects.
* 0.7.8 -- 2019-08-24
  * Fixes `-v` / `--verbose` option handling (again!).
  * Updates `org.clojure/test.check` to `"0.10.0"` and `tools.deps.alpha` to 0.7.541 (and add `slf4j-nop` as a dependency now that t.d.a has removed it).
  * Pins Jackson libraries in `deps.edn` to avoid potential version conflicts (such as when generating a Luminus template).
* 0.7.7 -- 2019-08-07
  * Fixed #23 by pinning versions in the templates (`org.clojure/clojure "1.10.1"` and `org.clojure/test.check "0.10.0-RC1"`).
  * Also updates `tools.deps.alpha` to 0.7.527.
* 0.7.6 -- 2019-07-04
  * Fixes #20 by allowing more complex Git URLs (and documenting them in the README).
  * Fixes #15 by allowing (and ignoring) `nil` paths to `->files`.
* 0.7.5 -- 2019-06-29
  * Fixes #21 by updating `tools.deps.alpha` (to 0.7.516) and switching from `clojure-env` to `default-deps`.
  * Fixes #19 by expanding the explanation of qualified/dotted project names in the README.
  * Fixes #18 by supporting dotted names in templates.
  * Fixes #14 by adding `root-ns` to the `template` setup (renamed to `namespace` in 0.8.0).
  * Fixes `-v` / `--verbose` option handling.
* 0.5.5 -- 2018-11-12
  * Update `tools.deps.alpha` version.
* 0.5.4 -- 2018-10-24
  * Initial version that "matches" `tools.deps.alpha` versioning.
