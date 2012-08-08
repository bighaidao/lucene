Apache Lucene Maven Build
=========================
This is a version of Apache Lucene, the text search engine library written in Java, with Maven as build system.

To build Lucene, install Maven und issue the command

	mvn install

The following multi-module structure has been chosen:

	lucene-analyzers-common
	lucene-analyzers-kuromoji
	lucene-analyzers-phonetic
	lucene-analyzers-smartcn
	lucene-analyzers-stempel
	lucene-benchmark
	lucene-core
	lucene-core-test
	lucene-facet
	lucene-grouping
	lucene-highlighter
	lucene-icu
	lucene-instantiated
	lucene-join
	lucene-memory
	lucene-misc
	lucene-queries
	lucene-queryparser
	lucene-remote
	lucene-spatial
	lucene-spellchecker
	lucene-test-framework
	lucene-tools
	lucene-xml-query-parser


``lucene-core`` is the Lucene library, with a separate split-out test module ``lucene-core-test`` that uses ``lucene-test-framework`` as dependency. The other modules are the Lucene contrib packages.

In the multimodule build, the benchmark module is not included. It is only needed in specific cases. Add it if you like and take care of downloading the wikipedia test case, which is not automatically activated, you have to do it at yourself. 

In the directory layout, the java docs are a little bit stripped. All ``package.html`` and ``overview.html`` files under java source directories has been removed. Sorry. If you need full javadocs, refer to the original version.

Furthermore, a Sonar (with mysql) maven plugin configuration is included with Cobertura. For myself I use it via Jenkins. Have fun!

