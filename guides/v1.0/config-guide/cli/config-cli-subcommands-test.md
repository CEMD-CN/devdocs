---
layout: default
group: config-guide
subgroup: CLI
title: Run tests
menu_title: Run tests
menu_node: 
menu_order: 60
github_link: config-guide/cli/config-cli-subcommands-test.md
---


#### Contents

*	<a href="#config-cli-before">First steps</a>
*	<a href="#config-cli-subcommands-tests-prereq">Prerequisites</a>
*	<a href="#config-cli-subcommands-tests-overview">Overview of unit tests</a>

<h2 id="config-cli-before">First steps</h2>
{% include install/first-steps-cli.html %}

<h2 id="config-cli-subcommands-tests-prereq">Prerequisites</h2>
Before you run this command, all of the following must be true:

*	The `Magento_Developer` module must be enabled. You can enable it as follows:

		magento module:enable [--force] Magento_Developer

	Use the `--force` option only if it's necessary.

*	Your system must be set up to run the desired tests.

	For example, to run integration tests, you should copy `dev/tests/integration/etc/install-config-mysql.php.dist` to `dev/tests/integration/etc/install-config-mysql.php` and modify it to suit your environment.

<h2 id="config-cli-subcommands-tests-overview">Overview of unit tests</h2>
This command runs a set of unit tests defined in the Magento 2 code base. You can either run all tests or tests you select.

Whenever a not supported type is specified, the program terminates and lists all available types.

Following execution, a detailed report displays showing the test run and results.

<h2 id="config-cli-subcommands-tests-run">Run unit tests</h2>
Command usage:

	php magento dev:tests:run [--all] <test>

To list the available tests, enter

	php magento dev:tests:run --help

For example, to run integration tests, enter

	php magento dev:tests:run integration

#### Related topics

*	<a href="{{ site.gdeurl }}config-guide/cli/config-cli-subcommands-cache.html">Manage the cache</a>
*	<a href="{{ site.gdeurl }}config-guide/cli/config-cli-subcommands-index.html">Manage the indexers</a>
*	<a href="{{ site.gdeurl }}config-guide/cli/config-cli-subcommands-compiler-multi.html">Multi-tenant compiler</a>
*	<a href="{{ site.gdeurl }}config-guide/cli/config-cli-subcommands-compiler-single.html">Single-tenant compiler</a>
*	<a href="{{ site.gdeurl }}config-guide/cli/config-cli-subcommands-log.html">Clean the logs</a>
*	<a href="{{ site.gdeurl }}config-guide/cli/config-cli-subcommands-i18n.html">Translation dictionaries and language packages</a>
*	<a href="{{ site.gdeurl }}config-guide/cli/config-cli-subcommands-static-view.html">Deploy static view files</a>
*	<a href="{{ site.gdeurl }}config-guide/cli/config-cli-subcommands-less-sass.html">Create LESS from CSS</a>
