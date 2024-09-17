# HeavenFight Project

## Description

**HeavenFight** est une application conteneurisée avec Docker. Ce projet comprend une configuration pour exécuter un backend ainsi que divers services. Le backend doit être téléchargé séparément et intégré au même répertoire.

## Prérequis

Avant de commencer, assurez-vous d'avoir installé les éléments suivants :

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Installation

Suivez ces étapes pour configurer le projet :

### 1. Cloner le backend

Le backend n'est pas inclus dans ce dépôt. Vous devez d'abord le cloner dans le même répertoire que ce projet.

```bash
git clone https://github.com/example/backend.git
```

### 2. Construire les images Docker

Après avoir téléchargé le backend, exécutez la commande suivante pour construire les images Docker sans utiliser le cache :

```bash
docker compose build --no-cache
```

### 3. Lancer les conteneurs
Une fois la construction terminée, démarrez les services avec Docker Compose :

```bash
docker compose up
```

Cela démarrera tous les services nécessaires pour faire tourner l'application.

### Utilisation
Une fois les conteneurs démarrés, l'application sera accessible selon la configuration définie dans le fichier docker-compose.yml. Généralement, vous pouvez accéder à l'application à l'adresse suivante :

```bash
http://localhost/
https://localhost/
```

### Structure du projet
Voici un aperçu rapide de la structure des dossiers :

```bash
.
├── Docker
│   ├── Redis
│   └── frankenphp
│       └── conf.d
├── backend
│   ├── bin
│   ├── config
│   │   ├── packages
│   │   └── routes
│   ├── public
│   ├── src
│   │   └── Core
│   │       ├── Action
│   │       ├── Controller
│   │       ├── Domain
│   │       │   ├── Enums
│   │       │   ├── Models
│   │       │   ├── Services
│   │       │   └── Traits
│   │       └── Infrastructure
│   ├── templates
│   ├── tests
│   ├── var
│   │   ├── cache
│   │   │   └── dev
│   │   │       ├── ContainerWrWQaGq
│   │   │       ├── ContainerXLewtsu
│   │   │       ├── Symfony
│   │   │       │   └── Config
│   │   │       │       ├── Framework
│   │   │       │       │   ├── Assets
│   │   │       │       │   ├── Cache
│   │   │       │       │   ├── Form
│   │   │       │       │   ├── HtmlSanitizer
│   │   │       │       │   ├── HttpClient
│   │   │       │       │   │   ├── DefaultOptions
│   │   │       │       │   │   │   └── RetryFailed
│   │   │       │       │   │   └── ScopedClientConfig
│   │   │       │       │   │       └── RetryFailed
│   │   │       │       │   ├── Mailer
│   │   │       │       │   ├── Messenger
│   │   │       │       │   │   ├── BusConfig
│   │   │       │       │   │   ├── Serializer
│   │   │       │       │   │   └── TransportConfig
│   │   │       │       │   ├── Notifier
│   │   │       │       │   ├── RateLimiter
│   │   │       │       │   │   └── LimiterConfig
│   │   │       │       │   ├── Serializer
│   │   │       │       │   ├── Translator
│   │   │       │       │   ├── Validation
│   │   │       │       │   ├── Webhook
│   │   │       │       │   └── Workflows
│   │   │       │       │       └── WorkflowsConfig
│   │   │       │       └── Twig
│   │   │       ├── pools
│   │   │       │   ├── app
│   │   │       │   │   └── 5++k7zjEPC
│   │   │       │   └── system
│   │   │       │       ├── 5+kVdRroxu
│   │   │       │       ├── OwsxDPcjnb
│   │   │       │       ├── RYUcXJbKrA
│   │   │       │       └── cVLZSRtkX-
│   │   │       ├── profiler
│   │   │       │   ├── 1e
│   │   │       │   │   └── d8
│   │   │       │   ├── 4b
│   │   │       │   │   └── 1b
│   │   │       │   ├── 6d
│   │   │       │   │   └── 04
│   │   │       │   ├── 85
│   │   │       │   │   └── 2f
│   │   │       │   ├── d3
│   │   │       │   │   └── d9
│   │   │       │   └── ef
│   │   │       │       └── c8
│   │   │       └── twig
│   │   │           ├── 08
│   │   │           ├── 0b
│   │   │           ├── 0c
│   │   │           ├── 0f
│   │   │           ├── 12
│   │   │           ├── 14
│   │   │           ├── 23
│   │   │           ├── 25
│   │   │           ├── 2d
│   │   │           ├── 31
│   │   │           ├── 33
│   │   │           ├── 34
│   │   │           ├── 35
│   │   │           ├── 3b
│   │   │           ├── 3e
│   │   │           ├── 45
│   │   │           ├── 47
│   │   │           ├── 5b
│   │   │           ├── 5f
│   │   │           ├── 6b
│   │   │           ├── 6c
│   │   │           ├── 7c
│   │   │           ├── 81
│   │   │           ├── 87
│   │   │           ├── 8d
│   │   │           ├── 97
│   │   │           ├── 98
│   │   │           ├── 9d
│   │   │           ├── ad
│   │   │           ├── b0
│   │   │           ├── b1
│   │   │           ├── b4
│   │   │           ├── b7
│   │   │           ├── ba
│   │   │           ├── c6
│   │   │           ├── c7
│   │   │           ├── cf
│   │   │           ├── d1
│   │   │           ├── d5
│   │   │           ├── d6
│   │   │           ├── dd
│   │   │           ├── df
│   │   │           ├── e4
│   │   │           ├── e7
│   │   │           └── ee
│   │   └── log
│   └── vendor
│       ├── bin
│       ├── composer
│       ├── doctrine
│       │   ├── deprecations
│       │   │   └── lib
│       │   │       └── Doctrine
│       │   │           └── Deprecations
│       │   │               └── PHPUnit
│       │   ├── inflector
│       │   │   ├── docs
│       │   │   │   └── en
│       │   │   └── lib
│       │   │       └── Doctrine
│       │   │           └── Inflector
│       │   │               └── Rules
│       │   │                   ├── English
│       │   │                   ├── French
│       │   │                   ├── NorwegianBokmal
│       │   │                   ├── Portuguese
│       │   │                   ├── Spanish
│       │   │                   └── Turkish
│       │   └── instantiator
│       │       ├── docs
│       │       │   └── en
│       │       └── src
│       │           └── Doctrine
│       │               └── Instantiator
│       │                   └── Exception
│       ├── masterminds
│       │   └── html5
│       │       ├── bin
│       │       └── src
│       │           └── HTML5
│       │               ├── Parser
│       │               └── Serializer
│       ├── myclabs
│       │   └── deep-copy
│       │       └── src
│       │           └── DeepCopy
│       │               ├── Exception
│       │               ├── Filter
│       │               │   └── Doctrine
│       │               ├── Matcher
│       │               │   └── Doctrine
│       │               ├── Reflection
│       │               ├── TypeFilter
│       │               │   ├── Date
│       │               │   └── Spl
│       │               └── TypeMatcher
│       ├── nikic
│       │   └── php-parser
│       │       ├── bin
│       │       └── lib
│       │           └── PhpParser
│       │               ├── Builder
│       │               ├── Comment
│       │               ├── ErrorHandler
│       │               ├── Internal
│       │               ├── Lexer
│       │               │   └── TokenEmulator
│       │               ├── Node
│       │               │   ├── Expr
│       │               │   │   ├── AssignOp
│       │               │   │   ├── BinaryOp
│       │               │   │   └── Cast
│       │               │   ├── Name
│       │               │   ├── Scalar
│       │               │   │   └── MagicConst
│       │               │   └── Stmt
│       │               │       └── TraitUseAdaptation
│       │               ├── NodeVisitor
│       │               ├── Parser
│       │               └── PrettyPrinter
│       ├── phar-io
│       │   ├── manifest
│       │   │   ├── src
│       │   │   │   ├── exceptions
│       │   │   │   ├── values
│       │   │   │   └── xml
│       │   │   └── tools
│       │   │       └── php-cs-fixer.d
│       │   └── version
│       │       └── src
│       │           ├── constraints
│       │           └── exceptions
│       ├── phpdocumentor
│       │   ├── reflection-common
│       │   │   └── src
│       │   ├── reflection-docblock
│       │   │   └── src
│       │   │       ├── DocBlock
│       │   │       │   └── Tags
│       │   │       │       ├── Factory
│       │   │       │       ├── Formatter
│       │   │       │       └── Reference
│       │   │       └── Exception
│       │   └── type-resolver
│       │       └── src
│       │           ├── PseudoTypes
│       │           └── Types
│       ├── phpstan
│       │   ├── extension-installer
│       │   │   └── src
│       │   ├── phpdoc-parser
│       │   │   └── src
│       │   │       ├── Ast
│       │   │       │   ├── ConstExpr
│       │   │       │   ├── NodeVisitor
│       │   │       │   ├── PhpDoc
│       │   │       │   │   └── Doctrine
│       │   │       │   └── Type
│       │   │       ├── Lexer
│       │   │       ├── Parser
│       │   │       └── Printer
│       │   ├── phpstan
│       │   │   └── conf
│       │   └── phpstan-symfony
│       │       ├── src
│       │       │   ├── Rules
│       │       │   │   └── Symfony
│       │       │   ├── Symfony
│       │       │   └── Type
│       │       │       └── Symfony
│       │       │           ├── Config
│       │       │           │   └── ValueObject
│       │       │           └── Form
│       │       └── stubs
│       │           ├── Psr
│       │           │   └── Cache
│       │           ├── Symfony
│       │           │   ├── Bundle
│       │           │   │   ├── FrameworkBundle
│       │           │   │   │   ├── Controller
│       │           │   │   │   └── Test
│       │           │   │   └── SecurityBundle
│       │           │   │       └── DependencyInjection
│       │           │   │           └── Security
│       │           │   │               └── Factory
│       │           │   ├── Component
│       │           │   │   ├── Console
│       │           │   │   │   ├── Exception
│       │           │   │   │   ├── Helper
│       │           │   │   │   └── Output
│       │           │   │   ├── DependencyInjection
│       │           │   │   │   └── Extension
│       │           │   │   ├── EventDispatcher
│       │           │   │   ├── Form
│       │           │   │   │   ├── ChoiceList
│       │           │   │   │   │   └── Loader
│       │           │   │   │   └── Exception
│       │           │   │   ├── HttpFoundation
│       │           │   │   ├── Messenger
│       │           │   │   ├── OptionsResolver
│       │           │   │   │   └── Exception
│       │           │   │   ├── Process
│       │           │   │   ├── PropertyAccess
│       │           │   │   │   └── Exception
│       │           │   │   ├── Security
│       │           │   │   │   ├── Acl
│       │           │   │   │   │   └── Model
│       │           │   │   │   └── Core
│       │           │   │   │       ├── Authentication
│       │           │   │   │       │   └── Token
│       │           │   │   │       ├── Authorization
│       │           │   │   │       │   └── Voter
│       │           │   │   │       └── User
│       │           │   │   ├── Serializer
│       │           │   │   │   ├── Encoder
│       │           │   │   │   ├── Exception
│       │           │   │   │   └── Normalizer
│       │           │   │   └── Validator
│       │           │   │       └── Constraints
│       │           │   └── Contracts
│       │           │       ├── Cache
│       │           │       └── Service
│       │           └── Twig
│       │               └── Node
│       ├── phpunit
│       │   ├── php-code-coverage
│       │   │   ├── build
│       │   │   │   └── scripts
│       │   │   └── src
│       │   │       ├── Driver
│       │   │       ├── Exception
│       │   │       ├── Node
│       │   │       ├── Report
│       │   │       │   ├── Html
│       │   │       │   │   └── Renderer
│       │   │       │   │       └── Template
│       │   │       │   │           ├── css
│       │   │       │   │           ├── icons
│       │   │       │   │           └── js
│       │   │       │   └── Xml
│       │   │       ├── StaticAnalysis
│       │   │       └── Util
│       │   ├── php-file-iterator
│       │   │   └── src
│       │   ├── php-invoker
│       │   │   └── src
│       │   │       └── exceptions
│       │   ├── php-text-template
│       │   │   └── src
│       │   │       └── exceptions
│       │   ├── php-timer
│       │   │   └── src
│       │   │       └── exceptions
│       │   └── phpunit
│       │       ├── schema
│       │       └── src
│       │           ├── Framework
│       │           │   ├── Assert
│       │           │   ├── Constraint
│       │           │   │   ├── Boolean
│       │           │   │   ├── Cardinality
│       │           │   │   ├── Equality
│       │           │   │   ├── Exception
│       │           │   │   ├── Filesystem
│       │           │   │   ├── Math
│       │           │   │   ├── Object
│       │           │   │   ├── Operator
│       │           │   │   ├── String
│       │           │   │   ├── Traversable
│       │           │   │   └── Type
│       │           │   ├── Error
│       │           │   ├── Exception
│       │           │   └── MockObject
│       │           │       ├── Api
│       │           │       ├── Builder
│       │           │       ├── Exception
│       │           │       ├── Generator
│       │           │       ├── Rule
│       │           │       └── Stub
│       │           ├── Runner
│       │           │   ├── Extension
│       │           │   ├── Filter
│       │           │   └── Hook
│       │           ├── TextUI
│       │           │   ├── CliArguments
│       │           │   ├── Exception
│       │           │   └── XmlConfiguration
│       │           │       ├── CodeCoverage
│       │           │       │   ├── Filter
│       │           │       │   └── Report
│       │           │       ├── Filesystem
│       │           │       ├── Group
│       │           │       ├── Logging
│       │           │       │   └── TestDox
│       │           │       ├── Migration
│       │           │       │   └── Migrations
│       │           │       ├── PHP
│       │           │       ├── PHPUnit
│       │           │       └── TestSuite
│       │           └── Util
│       │               ├── Annotation
│       │               ├── Log
│       │               ├── PHP
│       │               │   └── Template
│       │               ├── TestDox
│       │               └── Xml
│       ├── psr
│       │   ├── cache
│       │   │   └── src
│       │   ├── container
│       │   │   └── src
│       │   ├── event-dispatcher
│       │   │   └── src
│       │   └── log
│       │       └── src
│       ├── sebastian
│       │   ├── cli-parser
│       │   │   └── src
│       │   │       └── exceptions
│       │   ├── code-unit
│       │   │   └── src
│       │   │       └── exceptions
│       │   ├── code-unit-reverse-lookup
│       │   │   └── src
│       │   ├── comparator
│       │   │   └── src
│       │   │       └── exceptions
│       │   ├── complexity
│       │   │   └── src
│       │   │       ├── Complexity
│       │   │       ├── Exception
│       │   │       └── Visitor
│       │   ├── diff
│       │   │   └── src
│       │   │       ├── Exception
│       │   │       └── Output
│       │   ├── environment
│       │   │   └── src
│       │   ├── exporter
│       │   │   └── src
│       │   ├── global-state
│       │   │   └── src
│       │   │       └── exceptions
│       │   ├── lines-of-code
│       │   │   └── src
│       │   │       └── Exception
│       │   ├── object-enumerator
│       │   │   └── src
│       │   ├── object-reflector
│       │   │   └── src
│       │   ├── recursion-context
│       │   │   └── src
│       │   ├── resource-operations
│       │   │   ├── build
│       │   │   └── src
│       │   ├── type
│       │   │   └── src
│       │   │       ├── exception
│       │   │       └── type
│       │   └── version
│       │       └── src
│       ├── symfony
│       │   ├── browser-kit
│       │   │   ├── Exception
│       │   │   └── Test
│       │   │       └── Constraint
│       │   ├── cache
│       │   │   ├── Adapter
│       │   │   ├── DataCollector
│       │   │   ├── DependencyInjection
│       │   │   ├── Exception
│       │   │   ├── Marshaller
│       │   │   ├── Messenger
│       │   │   └── Traits
│       │   ├── cache-contracts
│       │   ├── config
│       │   │   ├── Builder
│       │   │   ├── Definition
│       │   │   │   ├── Builder
│       │   │   │   ├── Configurator
│       │   │   │   ├── Dumper
│       │   │   │   ├── Exception
│       │   │   │   └── Loader
│       │   │   ├── Exception
│       │   │   ├── Loader
│       │   │   ├── Resource
│       │   │   └── Util
│       │   │       └── Exception
│       │   ├── console
│       │   │   ├── Attribute
│       │   │   ├── CI
│       │   │   ├── Command
│       │   │   ├── CommandLoader
│       │   │   ├── Completion
│       │   │   │   └── Output
│       │   │   ├── DataCollector
│       │   │   ├── Debug
│       │   │   ├── DependencyInjection
│       │   │   ├── Descriptor
│       │   │   ├── Event
│       │   │   ├── EventListener
│       │   │   ├── Exception
│       │   │   ├── Formatter
│       │   │   ├── Helper
│       │   │   ├── Input
│       │   │   ├── Logger
│       │   │   ├── Messenger
│       │   │   ├── Output
│       │   │   ├── Question
│       │   │   ├── Resources
│       │   │   │   └── bin
│       │   │   ├── SignalRegistry
│       │   │   ├── Style
│       │   │   └── Tester
│       │   │       └── Constraint
│       │   ├── css-selector
│       │   │   ├── Exception
│       │   │   ├── Node
│       │   │   ├── Parser
│       │   │   │   ├── Handler
│       │   │   │   ├── Shortcut
│       │   │   │   └── Tokenizer
│       │   │   └── XPath
│       │   │       └── Extension
│       │   ├── dependency-injection
│       │   │   ├── Argument
│       │   │   ├── Attribute
│       │   │   ├── Compiler
│       │   │   ├── Config
│       │   │   ├── Dumper
│       │   │   ├── Exception
│       │   │   ├── Extension
│       │   │   ├── LazyProxy
│       │   │   │   ├── Instantiator
│       │   │   │   └── PhpDumper
│       │   │   ├── Loader
│       │   │   │   ├── Configurator
│       │   │   │   │   └── Traits
│       │   │   │   └── schema
│       │   │   │       └── dic
│       │   │   │           └── services
│       │   │   └── ParameterBag
│       │   ├── deprecation-contracts
│       │   ├── dom-crawler
│       │   │   ├── Field
│       │   │   └── Test
│       │   │       └── Constraint
│       │   ├── dotenv
│       │   │   ├── Command
│       │   │   └── Exception
│       │   ├── error-handler
│       │   │   ├── Error
│       │   │   ├── ErrorEnhancer
│       │   │   ├── ErrorRenderer
│       │   │   ├── Exception
│       │   │   ├── Internal
│       │   │   └── Resources
│       │   │       ├── assets
│       │   │       │   ├── css
│       │   │       │   ├── images
│       │   │       │   └── js
│       │   │       ├── bin
│       │   │       └── views
│       │   ├── event-dispatcher
│       │   │   ├── Attribute
│       │   │   ├── Debug
│       │   │   └── DependencyInjection
│       │   ├── event-dispatcher-contracts
│       │   ├── filesystem
│       │   │   └── Exception
│       │   ├── finder
│       │   │   ├── Comparator
│       │   │   ├── Exception
│       │   │   └── Iterator
│       │   ├── flex
│       │   │   └── src
│       │   │       ├── Command
│       │   │       ├── Configurator
│       │   │       ├── Event
│       │   │       ├── Unpack
│       │   │       └── Update
│       │   ├── framework-bundle
│       │   │   ├── CacheWarmer
│       │   │   ├── Command
│       │   │   ├── Console
│       │   │   │   ├── Descriptor
│       │   │   │   └── Helper
│       │   │   ├── Controller
│       │   │   ├── DataCollector
│       │   │   ├── DependencyInjection
│       │   │   │   └── Compiler
│       │   │   ├── EventListener
│       │   │   ├── HttpCache
│       │   │   ├── Kernel
│       │   │   ├── Resources
│       │   │   │   ├── bin
│       │   │   │   └── config
│       │   │   │       ├── routing
│       │   │   │       └── schema
│       │   │   ├── Routing
│       │   │   │   └── Attribute
│       │   │   ├── Secrets
│       │   │   ├── Test
│       │   │   └── Translation
│       │   ├── http-foundation
│       │   │   ├── Exception
│       │   │   ├── File
│       │   │   │   └── Exception
│       │   │   ├── RateLimiter
│       │   │   ├── RequestMatcher
│       │   │   ├── Session
│       │   │   │   ├── Attribute
│       │   │   │   ├── Flash
│       │   │   │   └── Storage
│       │   │   │       ├── Handler
│       │   │   │       └── Proxy
│       │   │   └── Test
│       │   │       └── Constraint
│       │   ├── http-kernel
│       │   │   ├── Attribute
│       │   │   ├── Bundle
│       │   │   ├── CacheClearer
│       │   │   ├── CacheWarmer
│       │   │   ├── Config
│       │   │   ├── Controller
│       │   │   │   └── ArgumentResolver
│       │   │   ├── ControllerMetadata
│       │   │   ├── DataCollector
│       │   │   ├── Debug
│       │   │   ├── DependencyInjection
│       │   │   ├── Event
│       │   │   ├── EventListener
│       │   │   ├── Exception
│       │   │   ├── Fragment
│       │   │   ├── HttpCache
│       │   │   ├── Log
│       │   │   ├── Profiler
│       │   │   └── Resources
│       │   ├── maker-bundle
│       │   │   └── src
│       │   │       ├── Command
│       │   │       ├── Console
│       │   │       ├── DependencyInjection
│       │   │       │   └── CompilerPass
│       │   │       ├── Docker
│       │   │       ├── Doctrine
│       │   │       ├── Event
│       │   │       ├── Exception
│       │   │       ├── Maker
│       │   │       │   ├── Common
│       │   │       │   └── Security
│       │   │       ├── Renderer
│       │   │       ├── Resources
│       │   │       │   ├── bin
│       │   │       │   ├── config
│       │   │       │   ├── doc
│       │   │       │   ├── help
│       │   │       │   │   └── security
│       │   │       │   └── skeleton
│       │   │       │       ├── authenticator
│       │   │       │       ├── command
│       │   │       │       ├── controller
│       │   │       │       ├── crud
│       │   │       │       │   ├── controller
│       │   │       │       │   ├── templates
│       │   │       │       │   └── test
│       │   │       │       ├── doctrine
│       │   │       │       ├── event
│       │   │       │       ├── form
│       │   │       │       ├── message
│       │   │       │       ├── middleware
│       │   │       │       ├── registration
│       │   │       │       ├── resetPassword
│       │   │       │       ├── scheduler
│       │   │       │       ├── security
│       │   │       │       │   ├── custom
│       │   │       │       │   └── formLogin
│       │   │       │       ├── serializer
│       │   │       │       ├── stimulus
│       │   │       │       ├── test
│       │   │       │       ├── twig
│       │   │       │       ├── validator
│       │   │       │       ├── verifyEmail
│       │   │       │       └── webhook
│       │   │       ├── Security
│       │   │       │   └── Model
│       │   │       ├── Test
│       │   │       └── Util
│       │   │           └── ClassSource
│       │   │               └── Model
│       │   ├── phpunit-bridge
│       │   │   ├── DeprecationErrorHandler
│       │   │   ├── Legacy
│       │   │   ├── TextUI
│       │   │   └── bin
│       │   ├── polyfill-intl-grapheme
│       │   ├── polyfill-intl-normalizer
│       │   │   └── Resources
│       │   │       ├── stubs
│       │   │       └── unidata
│       │   ├── polyfill-mbstring
│       │   │   └── Resources
│       │   │       └── unidata
│       │   ├── polyfill-php83
│       │   │   └── Resources
│       │   │       └── stubs
│       │   ├── process
│       │   │   ├── Exception
│       │   │   ├── Messenger
│       │   │   └── Pipes
│       │   ├── property-access
│       │   │   └── Exception
│       │   ├── property-info
│       │   │   ├── DependencyInjection
│       │   │   ├── Extractor
│       │   │   ├── PhpStan
│       │   │   └── Util
│       │   ├── routing
│       │   │   ├── Annotation
│       │   │   ├── Attribute
│       │   │   ├── DependencyInjection
│       │   │   ├── Exception
│       │   │   ├── Generator
│       │   │   │   └── Dumper
│       │   │   ├── Loader
│       │   │   │   ├── Configurator
│       │   │   │   │   └── Traits
│       │   │   │   └── schema
│       │   │   │       └── routing
│       │   │   ├── Matcher
│       │   │   │   └── Dumper
│       │   │   └── Requirement
│       │   ├── runtime
│       │   │   ├── Internal
│       │   │   │   ├── Console
│       │   │   │   │   ├── Command
│       │   │   │   │   ├── Input
│       │   │   │   │   └── Output
│       │   │   │   ├── HttpFoundation
│       │   │   │   └── HttpKernel
│       │   │   ├── Resolver
│       │   │   └── Runner
│       │   │       └── Symfony
│       │   ├── serializer
│       │   │   ├── Annotation
│       │   │   ├── Attribute
│       │   │   ├── CacheWarmer
│       │   │   ├── Command
│       │   │   ├── Context
│       │   │   │   ├── Encoder
│       │   │   │   └── Normalizer
│       │   │   ├── DataCollector
│       │   │   ├── Debug
│       │   │   ├── DependencyInjection
│       │   │   ├── Encoder
│       │   │   ├── Exception
│       │   │   ├── Extractor
│       │   │   ├── Mapping
│       │   │   │   ├── Factory
│       │   │   │   └── Loader
│       │   │   │       └── schema
│       │   │   │           └── dic
│       │   │   │               └── serializer-mapping
│       │   │   ├── NameConverter
│       │   │   └── Normalizer
│       │   ├── service-contracts
│       │   │   ├── Attribute
│       │   │   └── Test
│       │   ├── stopwatch
│       │   ├── string
│       │   │   ├── Exception
│       │   │   ├── Inflector
│       │   │   ├── Resources
│       │   │   │   ├── bin
│       │   │   │   └── data
│       │   │   └── Slugger
│       │   ├── translation-contracts
│       │   │   └── Test
│       │   ├── twig-bridge
│       │   │   ├── Attribute
│       │   │   ├── Command
│       │   │   ├── DataCollector
│       │   │   ├── ErrorRenderer
│       │   │   ├── EventListener
│       │   │   ├── Extension
│       │   │   ├── Form
│       │   │   ├── Mime
│       │   │   ├── Node
│       │   │   ├── NodeVisitor
│       │   │   ├── Resources
│       │   │   │   └── views
│       │   │   │       ├── Email
│       │   │   │       │   ├── default
│       │   │   │       │   │   └── notification
│       │   │   │       │   └── zurb_2
│       │   │   │       │       └── notification
│       │   │   │       └── Form
│       │   │   ├── Test
│       │   │   │   └── Traits
│       │   │   ├── TokenParser
│       │   │   └── Translation
│       │   ├── twig-bundle
│       │   │   ├── CacheWarmer
│       │   │   ├── Command
│       │   │   ├── DependencyInjection
│       │   │   │   ├── Compiler
│       │   │   │   └── Configurator
│       │   │   └── Resources
│       │   │       └── config
│       │   │           └── schema
│       │   ├── type-info
│       │   │   ├── Exception
│       │   │   ├── Type
│       │   │   ├── TypeContext
│       │   │   └── TypeResolver
│       │   ├── var-dumper
│       │   │   ├── Caster
│       │   │   ├── Cloner
│       │   │   │   └── Internal
│       │   │   ├── Command
│       │   │   │   └── Descriptor
│       │   │   ├── Dumper
│       │   │   │   └── ContextProvider
│       │   │   ├── Exception
│       │   │   ├── Resources
│       │   │   │   ├── bin
│       │   │   │   ├── css
│       │   │   │   ├── functions
│       │   │   │   └── js
│       │   │   ├── Server
│       │   │   └── Test
│       │   ├── var-exporter
│       │   │   ├── Exception
│       │   │   └── Internal
│       │   ├── web-profiler-bundle
│       │   │   ├── Controller
│       │   │   ├── Csp
│       │   │   ├── DependencyInjection
│       │   │   ├── EventListener
│       │   │   ├── Profiler
│       │   │   ├── Resources
│       │   │   │   ├── config
│       │   │   │   │   ├── routing
│       │   │   │   │   └── schema
│       │   │   │   ├── fonts
│       │   │   │   └── views
│       │   │   │       ├── Collector
│       │   │   │       ├── Icon
│       │   │   │       ├── Profiler
│       │   │   │       ├── Router
│       │   │   │       └── Script
│       │   │   │           └── Mermaid
│       │   │   └── Twig
│       │   └── yaml
│       │       ├── Command
│       │       ├── Exception
│       │       ├── Resources
│       │       │   └── bin
│       │       └── Tag
│       ├── theseer
│       │   └── tokenizer
│       │       └── src
│       ├── twig
│       │   └── twig
│       │       └── src
│       │           ├── Attribute
│       │           ├── Cache
│       │           ├── Error
│       │           ├── Extension
│       │           ├── Loader
│       │           ├── Node
│       │           │   └── Expression
│       │           │       ├── Binary
│       │           │       ├── Filter
│       │           │       ├── FunctionNode
│       │           │       ├── Test
│       │           │       └── Unary
│       │           ├── NodeVisitor
│       │           ├── Profiler
│       │           │   ├── Dumper
│       │           │   ├── Node
│       │           │   └── NodeVisitor
│       │           ├── Resources
│       │           ├── Runtime
│       │           ├── RuntimeLoader
│       │           ├── Sandbox
│       │           ├── Test
│       │           ├── TokenParser
│       │           └── Util
│       └── webmozart
│           └── assert
│               └── src
└── symfony-docker
    ├── docs
    └── public
```

### Contribution
Nous accueillons les contributions au projet. Pour contribuer, suivez ces étapes :

Forkez ce dépôt.
Créez une branche (git checkout -b feature/nouvelle-fonctionnalité).
Faites un commit avec vos modifications (git commit -am 'Ajout de fonctionnalité').
Poussez vos changements (git push origin feature/nouvelle-fonctionnalité).
Ouvrez une Pull Request.

### Problèmes connus
Assurez-vous que Docker et Docker Compose sont correctement installés.
Si vous rencontrez des problèmes lors de la construction des images, essayez de nettoyer le cache Docker avec docker system prune.
Licence
Ce projet est sous licence MIT License.

@Alexandre AMBIEHL aka @Nestate or @Elajhi


## Liens supplémentaires

- **Backend Repo**: [https://github.com/example/backend.git](https://github.com/example/backend.git)
- **Documentation Docker**: [https://docs.docker.com](https://docs.docker.com)
