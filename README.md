# Symfony Cheat Sheet

Useful practical commands, code and things you will frequently need for working with Symfony framework.

## Table of contents

* [Console](#console)
  * [General](#general)
  * [Cache](#cache)
  * [Bundle](#bundle)
  * [Routing](#routing)
  * [Doctrine](#doctrine)

## Console<a name="console"></a>

### General<a name="general"></a>

```bash
# List available commands and show the Symfony version
php app/console
```

```bash
# Display help for given command
php app/console help [command]
```

```bash
# Display all configured public services
php app/console container:debug [--show-private] [service_name]
```

```bash
# Dump all assets to the filesystem
php app/console assetic:dump [--watch] [--force] [--period=...] [write_to]
```

```bash
# Dump the default configuration for an extension/bundle
php app/console config:dump-reference <bundle_or_extension_alias>
```

```bash
# Send messages from spool
php app/console swiftmailer:spool:send [--message-limit=...] [--time-limit=...] [--recover-timeout=...]
```

```bash
# Extract translation strings from templates of a given bundle.
# It can display them or merge the new ones into the translation files
php app/console translation:update [--prefix=...] [--update-format=...] [--dump-messages] [--force]  <locale> <bundle>
```

```bash
# Lint a template and outputs to stdout the first encountered syntax error
php app/console twig:lint <filename>`
```

### Cache<a name="cache"></a>

```bash
# Clear the cached information
php app/console cache:clear [--no-warmup] [--no-optional-warmers]
```

```bash
# Warm up an empty cache
php app/console cache:warmup  [--no-optional-warmers]`
```

### Bundle<a name="bundle"></a>

```bash
# Install bundles web assets under a public web directory
php app/console assets:install <target_dir> [--symlink] [--relative]
```

```bash
# Generate a bundle
php app/console generate:bundle [--namespace=...] [--dir=...] [--bundle-name=...] [--format=...] [--structure]
```

### Routing<a name="routing"></a>

```bash
# Display current routes for application
php app/console router:debug [route_name]
```

```bash
# Dump all routes as Apache rewrite rules
php app/console router:dump-apache [--base-uri=...] [script_name]
```

```bash
# Debug routes by simulating a path info match
php app/console router:match <path_info>
```

```bash
# Display current exposed routes for an application
php app/console fos:js-routing:debug <name>  
```

### Doctrine<a name="doctrine"></a>

```bash
# Clear all metadata cache for an entity manager
php app/console doctrine:cache:clear-metadata [--em=...] [--flush]
```

```bash
# Clear all query cache for an entity manager
php app/console doctrine:cache:clear-query [--em=...] [--flush]
```

```bash
# Clear all result cache for an entity manager
php app/console doctrine:cache:clear-result [--em=...] [--flush]
```

```bash
# Create the configured databases
php app/console doctrine:database:create [--connection=...]
```

```bash
# Drop the configured databases
php app/console doctrine:database:drop [--connection=...] [--force]
```

```bash
# Convert mapping information between supported formats
php app/console doctrine:mapping:convert [--filter=...] [--force] [--from-database] [--extend=...] [--num-spaces=...] [--namespace=...] [--em=...] <to-type> <dest-path>
```

```bash
# Import mapping information from an existing database
php app/console doctrine:mapping:import [--em=...] [--filter=...] [--force] <bundle> <mapping-type>
```

```bash
# Show basic information about all mapped entities
php app/console doctrine:mapping:info [--em=...]
```

```bash
# Generate a new Doctrine entity inside a bundle
php app/console doctrine:generate:entity [--entity=...] [--fields=...] [--format=...] [--with-repository]
```

```bash
# Generate entity classes and method stubs from your mapping information
php app/console doctrine:generate:entities [--path=...] [--no-backup] <name>
```

```bash
# Generate a form class based on a Doctrine entity
php app/console doctrine:generate:form <entity>
```

```bash
# Generate a CRUD based on a Doctrine entity
php app/console doctrine:generate:crud [--entity=...] [--route-prefix=...] [--with-write] [--format=...]
```

```bash
# Execute arbitrary DQL directly from the command line
php app/console doctrine:query:dql [--hydrate=...] [--first-result=...] [--max-result=...] [--depth=...] [--em=...] <dql_to_execute>
```

```bash
# Execute arbitrary SQL directly from the command line
php app/console doctrine:query:sql [--depth=...] [--connection=...] <sql_to_execute>
```

```bash
# Executes (or dumps) the SQL needed to generate the database schema
php app/console doctrine:schema:create [--dump-sql] [--em=...]
```

```bash
# Execute (or dump) the SQL needed to drop the current database schema
php app/console doctrine:schema:drop [--dump-sql] [--force] [--full-database] [--em=...]
```

```bash
# Executes (or dumps) the SQL needed to update the database schema to match the current mapping metadata
php app/console doctrine:schema:update [--complete] [--dump-sql] [--force] [--em=...]
```

```bash
# Validate the Doctrine mapping files
php app/console doctrine:schema:validate [--em=...]
```

```bash
# Ensure that Doctrine is properly configured for a production environment
php app/console doctrine:ensure-production-settings [--complete] [--em=...]
```

```bash
# Load data fixtures to your database
php app/console doctrine:fixtures:load [--fixtures=...] [--append] [--em=...] [--purge-with-truncate]
```
