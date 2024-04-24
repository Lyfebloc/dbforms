

<img src="https://raw.githubusercontent.com/servequery/dbforms/master/app/icon.png" width="64" align="right"/>

# DbForms 

Dbfroms is cross-platform database crud form builder & database manager. 
It's designed to be simple to use and effective, when working with more databases simultaneously.
But there are also many advanced features like schema compare, visual query designer, chart visualisation or batch export and import.

## Supported databases
* MySQL
* PostgreSQL
* SQL Server
* Oracle (experimental)
* MongoDB
* Redis
* SQLite
* Amazon Redshift
* CockroachDB
* MariaDB

## Features
* Table data editing, with SQL change script preview
* Edit table schema, indexes, primary and foreign keys
* Compare and synchronize database structure
* ER diagram
* Light and dark theme
* Master/detail views, foreign key lookups
* Query designer
* Form view for comfortable work with tables with many columns
* JSON view on MongoDB collections
* Explore tables, views, procedures, functions, MongoDB collections
* SQL editor
  * execute SQL script
  * SQL code formatter
  * SQL code completion
  * Add SQL LEFT/INNER/RIGHT join utility
* Mongo JavaScript editor, execute Mongo script (with NodeJs syntax)
* Redis tree view, generate script from keys, run Redis script
* Runs as application for Windows, Linux and Mac. Or in Docker container on server and in web Browser on client.
* Import, export from/to CSV, Excel, JSON, NDJSON, XML
* Free table editor - quick table data editing (cleanup data after import/before export, prototype tables etc.)
* Archives - backup your data in NDJSON files on local filesystem (or on DbGate server, when using web application)
* Charts, export chart to HTML page
* Extensible plugin architecture
* Perspectives - nested table view over complex relational data, query designer on MongoDB databases


## Extra features

* Works everywhere - Windows, Linux, Mac, Web browser (+mobile web is planned), without compromises in features
* Many data browsing functions based using foreign keys - master/detail, expand columns, expandable form view

## Design

* Minimal dependencies
    * Frontend - Svelte
    * Backend - NodeJs, ExpressJs, database connection drivers
    * JavaScript + TypeScript
    * App - electron
* Platform independent - runs as web application in single docker container on server, or as application using Electron platform on Linux, Windows and Mac



## How to run development environment

Simple variant - runs WEB application:
```sh
yarn
yarn start
```

If you want more control, run WEB application:
```sh
yarn # install NPM packages
```

And than run following 3 commands concurrently in 3 terminals:
```
yarn start:api # run API on port 3000
yarn start:web # run web on port 5001
yarn lib # watch typescript libraries and plugins modifications
```
This runs API on port 3000 and web application on port 5001  
Open http://localhost:5001 in your browser

If you want to run electron app:
```sh
yarn # install NPM packages
cd app
yarn # install NPM packages for electron
```

And than run following 3 commands concurrently in 3 terminals:
```
yarn start:web # run web on port 5001 (only static JS and HTML files)
yarn lib # watch typescript libraries and plugins modifications
yarn start:app # run electron app
```

## How to run built electron app locally
This mode is very similar to production run of electron app. Electron doesn't use localhost:5001.

```sh
cd app
yarn
```

```sh
yarn
yarn build:app:local
yarn start:app:local
```

