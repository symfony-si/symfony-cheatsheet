# Symfony Cheat Sheet

Useful practical commands, code and things you will frequently need for working with Symfony framework.

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

### Routing

`$ php app/console router:debug [route_name]` Displays current routes for an application
`$ php app/console router:dump-apache [--base-uri=...] [script_name]` Dumps all routes as Apache rewrite rules
`$ php app/console router:match <path_info>` Debug routes by simulating a path info match
`$ php app/console fos:js-routing:debug <name>` Displays current exposed routes for an application
