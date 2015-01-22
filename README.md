# Symfony Cheat Sheet

Useful practical commands, code and things you will frequently need for working with Symfony framework.

## Table of contents

* [Console](#console)
  * [General](#general)
  * [Cache](#cache)
  * [Bundle](#bundle)
  * [Routing](#routing)
  * [Doctrine](#doctrine)

## Console

### General

`$ php app/console` List available commands and show the Symfony version  
`$ php app/console help [command]`  
`$ php app/console container:debug [--show-private] [service_name]` Displays all configured public services  
`$ php app/console assetic:dump [--watch] [--force] [--period=...] [write_to]` Dumps all assets to the filesystem  
`$ php app/console config:dump-reference <bundle_or_extension_alias>` Dumps the default configuration for an extension/bundle  
`$ php app/console swiftmailer:spool:send [--message-limit=...] [--time-limit=...] [--recover-timeout=...]`  
`$ php app/console translation:update [--prefix=...] [--update-format=...] [--dump-messages] [--force]  <locale> <bundle>` Extract translation strings from templates of a given bundle. It can display them or merge the new ones into the translation files  
`$ php app/console twig:lint <filename>` Lints a template and outputs to stdout the first encountered syntax error  

### Cache

`$ php app/console cache:clear [--no-warmup] [--no-optional-warmers]` Clear the cached information  
`$ php app/console cache:warmup  [--no-optional-warmers]` Warms up an empty cache  

### Bundle

`$ php app/console assets:install <target_dir> [--symlink] [--relative]` Installs bundles web assets under a public web directory  
`$ php app/console generate:bundle [--namespace=...] [--dir=...] [--bundle-name=...] [--format=...] [--structure]` Generates a bundle  

### Routing

`$ php app/console router:debug [route_name]` Displays current routes for an application  
`$ php app/console router:dump-apache [--base-uri=...] [script_name]` Dumps all routes as Apache rewrite rules  
`$ php app/console router:match <path_info>` Debug routes by simulating a path info match  
`$ php app/console fos:js-routing:debug <name>` Displays current exposed routes for an application  

### Doctrine

`$ php app/console doctrine:cache:clear-metadata [--em=...] [--flush]` Clears all metadata cache for an entity manager  
`$ php app/console doctrine:cache:clear-query [--em=...] [--flush]` Clears all query cache for an entity manager  
`$ php app/console doctrine:cache:clear-result [--em=...] [--flush]` Clears all result cache for an entity manager  
`$ php app/console doctrine:database:create [--connection=...]` Creates the configured databases  
`$ php app/console doctrine:database:drop [--connection=...] [--force]` Drops the configured databases  
`$ php app/console doctrine:mapping:convert [--filter=...] [--force] [--from-database] [--extend=...] [--num-spaces=...] [--namespace=...] [--em=...] <to-type> <dest-path>` Converts mapping information between supported formats  
`$ php app/console doctrine:mapping:import [--em=...] [--filter=...] [--force] <bundle> <mapping-type>` Imports mapping information from an existing database  
`$ php app/console doctrine:mapping:info [--em=...]` Shows basic information about all mapped entities  
`$ php app/console doctrine:generate:entity [--entity=...] [--fields=...] [--format=...] [--with-repository]` Generates a new Doctrine entity inside a bundle  
`$ php app/console doctrine:generate:entities [--path=...] [--no-backup] <name>` Generates entity classes and method stubs from your mapping information  
`$ php app/console doctrine:generate:form <entity>` Generates a form class based on a Doctrine entity  
`$ php app/console doctrine:generate:crud [--entity=...] [--route-prefix=...] [--with-write] [--format=...]` Generates a CRUD based on a Doctrine entity  
`$ php app/console doctrine:query:dql [--hydrate=...] [--first-result=...] [--max-result=...] [--depth=...] [--em=...] <dql_to_execute>` Executes arbitrary DQL directly from the command line  
`$ php app/console doctrine:query:sql [--depth=...] [--connection=...] <sql_to_execute>` Executes arbitrary SQL directly from the command line  
`$ php app/console doctrine:schema:create [--dump-sql] [--em=...]` Executes (or dumps) the SQL needed to generate the database schema  
`$ php app/console doctrine:schema:drop [--dump-sql] [--force] [--full-database] [--em=...]` Executes (or dumps) the SQL needed to drop the current database schema  
`$ php app/console doctrine:schema:update [--complete] [--dump-sql] [--force] [--em=...]` Executes (or dumps) the SQL needed to update the database schema to match the current mapping metadata  
`$ php app/console doctrine:schema:validate [--em=...]` Validates the Doctrine mapping files  
`$ php app/console doctrine:ensure-production-settings [--complete] [--em=...]` Ensures that Doctrine is properly configured for a production environment  
`$ php app/console doctrine:fixtures:load [--fixtures=...] [--append] [--em=...] [--purge-with-truncate]` Load data fixtures to your database  


## License

This content is published under the [Creative Commons Attribution 4.0 International License](LICENSE).