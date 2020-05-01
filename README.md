<p align="center">
<a href="https://laravel.com" target="_blank" rel="noopener"><img src="https://user-images.githubusercontent.com/3679080/79393326-6758de80-7f75-11ea-9196-8ecf990b40fd.png" width="300"></a>
</p>

<p align="center">
<a href="https://www.npmjs.com/package/vtec-admin"><img src="https://img.shields.io/npm/v/vtec-admin.svg?style=flat-square" alt="Latest Version on NPM"></a>
<a href="https://www.npmjs.com/package/vtec-admin"><img src="https://img.shields.io/npm/l/vtec-admin.svg?style=flat-square" alt="License"></a>
</p>

# About Vtec Admin

SPA admin library for Vue.js running on top of REST APIs, built on top of Vuetify and come with dedicated Vue CLI plugin. Ready to use on top of Laravel API backend by using official [Vtec Laravel Crud](https://github.com/okami101/vtec-laravel-crud) composer package, but can be used on every backend of your choice with your own data and authentication providers.

> See [full documentation](https://vtec.okami101.io)  
> Check [online demo](https://vtec-bookstore-demo.okami101.io/admin) -> use prefilled login (read only)  
> Note : this project is heavily inspired by [React Admin](https://github.com/marmelab/react-admin/) made by awesome [Marmelab Team](https://marmelab.com/)

[![sc](https://user-images.githubusercontent.com/3679080/80732263-58913080-8b0c-11ea-9074-56668c44a876.png)](https://vtec-bookstore-demo.okami101.io/admin)

## Features

* Powered by Vuetify, and come with nice [Material Theme by Creative Tim](https://github.com/creativetimofficial/vuetify-material-dashboard).
* Full standalone UI SPA admin that can be adapted to any backend (REST, GraphQL, SOAP, etc.) by writing your own data and auth providers by following specific contracts which ensure compatibility.
* Bare minimal Vue.js code needed to get your CRUD pages working, while allowing limitless customization.
* If using Vue CLI project (heavily recommended), [Vue CLI plugin](https://www.npmjs.com/package/vue-cli-plugin-vtec-admin) will be your ideal companion by installing all minimal boilerplate code for insane quick start. Can be used on any Vue.js based application as well.
* 100% Vue CLI friendly. Vtec Admin is simply a plugin which integrates within all of your existing plugins, notably Vue Router, Vuex and Vuetify. Keep total control of your Vue app by adding your own routes with custom pages, custom store modules, and full Vuetify theming as you are used to on Vue CLI base project.
* Ready to use data and auth providers for Laravel.
* Cookie based authentication auth provider for [Laravel Sanctum](https://github.com/laravel/sanctum). If you prefer JWT instead, simply write your own provider that follow specific auth contract.
* Advanced permissions.
* Official [Vtec Laravel Crud](https://github.com/okami101/vtec-laravel-crud) provided for insane quick start from top to bottom. Provide many backend features as spa authentication, profile editing, users management, impersonation, [translatable fields](https://github.com/spatie/laravel-translatable), [media support](https://github.com/spatie/laravel-medialibrary), [file manager](https://github.com/Studio-42/elFinder) with Wysiwyg bridges, etc.
* Associate to Laravel Crud and CLI plugin, Vtec Admin allows you immediate start developement from backend to UI with already basic functional admin.
* Stay as little magic as possible by fully respecting each backend and frontend development environnement. If you know well Laravel and Vue CLI basics, so you're ready to go !
* CRUD code generators are offered on both Laravel backend and Vue frontend for even quicker ready-to-go API and UI with basic CRUD boilerplate code generation. Each can be totally used separatly.
* With combination of Vtec Admin DSL, code generators as well as Vue.js power, feel the better mix between productivity and limitless customization.
* Full featured bookstore demo application, with [Laravel backend](examples/laravel) running on Docker and his associated [Vue CLI admin project](examples/demo) using [Vtec Admin](packages/admin).
* Complete documentation.
* Internationalization support via Vue I18n, with full english and french translations provided. Can be easily configured by taking user browser language.
* Translatable resource fields by contextual language selection on each crud page.
* Unique v-model context by form for minimal boilerplate code.
* Server-side form validation support.
* Autocomplete input with entity reference support.
* TinyMCE 5 as default Wysiwyg with elFinder bridge, can be replaced by your own.
* Full-featured datagrid, including multi-sort, pagination, global search, advanced filters, basic CSV export, live query string context. And of course with possibility of cell templating.
* Data iterator decoupled from datagrid which allows you total customization of list layout.
* Advanced filters as-you-type with many inputs: select, boolean, autocomplete for search by relations, with multiple, etc.
* Customizable by-row, bulk and global actions.
* Direct aside create/edit from list instead of separate crud page.
* Many fields and inputs components for various data types: select, enums, boolean, number, rich text, etc.
* To finish, for what it's worth, it's completely free.

## But why another admin panel again

Main goals :

* Nice ready-to-go Vuetify UI theme.
* SPA admin which deliver complete Vue.js power admin development.
* Full backend independence by using low-level auth and data providers.
* [DSL](https://en.wikipedia.org/wiki/Domain-specific_language) approach, minimal boilerplate code for best development experience with as little magic as possible.
* Powerful code generators for highest productivity.
* Best balance between productivity and customization.
* Maximize usage by thoughtful combination of many opensource projects.

The main goal of Vtec Admin is to get you rid off all CRUD boilerplate code that can be very nasty on full SPA Admin. Very bare minimal Vue.js code is needed to get your Vue CRUD pages working with standard nice basic layout. On another side, with combination of Vue.js component power development, you have limitless customization at hand. This is sort a Vue.js equivalent to [React Admin](https://github.com/marmelab/react-admin/), which uses [DSL](https://en.wikipedia.org/wiki/Domain-specific_language) approach.

So many admin panel are generaly tightly coulpled with backend framework and prevent us to switch easily. Besides most of the time it stays classic server-side templating engine oriented associated to good old jQuery plugins, with no usage of a powerfull UI framework as Vue.js. I think notably on [Backpack](https://backpackforlaravel.com/) on Laravel (not free) and free [EasyAdmin](https://github.com/EasyCorp/EasyAdminBundle) for symfony world. The main advantage of this admin panels is to be highest productive as possible (and plently featured in case of Backpack) but tends to come with her own logic and stay first of all very configuration oriented.

On another side, the official [Laravel Nova](https://nova.laravel.com/) is a very productive Vue SPA admin, with obviously big community, but not free, still Laravel-coupled and come with his own caveats (you tend to follow the "Nova" way for specifics needs with not really natural mix of coupled PHP and Vue development).

[React Admin](https://github.com/marmelab/react-admin/) is by far the most cool and customizable admin panel i ever seen. Besides it's totally free and independent of any backend. Althought it isn't the more efficient way to build administrable app from top to bottom with backend included, this is in my opinion the true way to build admin apps as LEGO&copy; !

It seem's there is no really equivalent on Vue.js world which is my preferred UI library and this i why i wanted to try a make one just for fun (and hard training).

By its nature, React Admin doesn't propose any helpers for backend framework, although [Api Platform Demo](https://github.com/api-platform/demo) try to do awesome work for Symfony. I choose to make a [complete helper package](https://github.com/okami101/vtec-laravel-crud) for Laravel in order to have the best quick start experience possible, while respecting highly standard code.

The goal of this project is to get use full power of each server and client world for admin app development, on keep it theme totally separated and with minimal boilerplate code and code generators for the quickest development as possible.

## State

I tried to as close as possible to RA features, without some of them as client-side data cache, the optimistic UI wich necessit many work for something i don't really need (besides it kills server-side validation which i'm not really a fan of it).  
Contrary to RA, no specific relationships is included on list and show views for fields, because seems more logical on server-side to me.

This is a really alpha state package, use it only for adventure !

This app is of course far to be as sharp as React Admin which the admin panel i highly recommended you to use. Morever RA has really fast growing contributions and tends to be the "de facto" UI-oriented SPA admin.

More backend showcase examples as Symfony / NestJS / Spring Boot / ASP.NET Core in addition to existing Laravel would be nice but it asks really too much work for now, especially when if i must develop a dedicated composer / npm / maven / NuGet packages for each...

> As this project was made on my free time and is totally free and open-source, don't expect any support of anything. This project was just mainly a personal challenge and only aims to satisfy my own needs on personal projects. For real production on essential sites I strongly advise you to go with [React Admin](https://github.com/marmelab/react-admin/) which is far more mature.

## Note on this main repo

This main repo contains all necessary projects to develop Vtec admin and run demo :

* [Vtec Admin Library](packages/admin), the main admin library.
* [Vtec Admin Vue CLI Plugin](packages/cli), the associate Vue CLI plugin which contains all base code boilerplate and commands generator.
* [Vtec Laravel Crud](vtec-laravel-crud), git submodule of composer package to use on fresh Laravel project which facilitates Vtec Admin integration and includes server-side commands generator.
* [Bookstore Admin Demo](examples/demo), full-features admin sample which is build on top of main Vtec Admin Library.
* [Bookstore Admin Demo](examples/laravel), suitable API backend for bookstore admin demo based on Laravel.
* [Tutorial Admin Demo](examples/tutorial), finished tutorial after following [dedicated docs](https://vtec.okami101.io/tutorial).
* [Vtec Docs](packages/docs), vuepress docs.

All of this projects are automatically linked together by symlinks (thanks to yarn workspaces and composer) for best library development experience in this project. HMR from demo to admin library side-by-side is fully supported !

## Usage

### How to run demo locally

Be sure to have clone this repo with git submodules.  
If not use `git submodule init && git submodule update`. [Vtec Laravel Crud](vtec-laravel-crud) should be cloned.

Docker is required for quick-start run backend API. If you don't want it, follow [boring way instructions](examples/laravel#the-boring-way).

Use Makefile for easy starting all necessery tools.
For Windows users just install [scoop](https://scoop.sh/) and `scoop install make`

Use `make help` for all detail commands.

In order to run demo :

```bash
make install # intall all yarn dependencies
make run-laravel-demo # run server api through docker (take a coffee if 1st time...)
make prepare-laravel-demo # initialize laravel app and inject dummy data (use it only for 1st launch)
make run-demo # compile all bookstore demo admin with HMR dev mode enabled
```

Admin panel should be autostart to [http://localhost:8080](http://localhost:8080)

### Run and build docs

Docs are build with VuePress. Use `make run-docs` to launch it and `make build-docs` for build it info static files inside "docs" repo root folder.

## Similar inspiring projects

### Backend-free admin panel builder

* [React Admin](https://github.com/marmelab/react-admin/), by far the most cool and customizable SPA admin panel, and totally free and independent of any backend. Just build admin panel as LEGO&copy; ! But not the most productive as is (no backend helpers), and highest learning curve compare to the others

### Free Symfony classic admin panel

* [EasyAdmin](https://github.com/EasyCorp/EasyAdminBundle), simple classic admin builder, not many widgets by default but very efficient and 100% configurable by YML config files and extendable with twig templates
* [Sonata Admin](https://github.com/sonata-project/SonataAdminBundle), super massive admin builder, maybe the most powerful and full featured free admin panel on the market, but not really a seamless development experience

### Some Laravel admin panels

* [Backpack](https://backpackforlaravel.com/), not free for commercial projects, classic HTML jQuery but stay one of the most productive admin panel with a tons of widgets
* [Official Laravel Nova](https://nova.laravel.com/), not free, full featured and very efficient SPA admin builder for Laravel with Vue.js. Code as fast as Backpack but with modern UI Framework
* [Voyager](https://voyager.devdojo.com/), free admin panel available for Laravel

## License

This project is open-sourced software licensed under the [MIT license](https://adr1enbe4udou1n.mit-license.org).
