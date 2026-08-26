# Angular style — throughline source

This document is **generated from the graph** by `tl docs`; `tl docs --check` gates it in CI. The prose headings are hand-owned — everything between `tl:*` markers is injected from the YAML items, so the published spec can never drift from the graph.

This source re-expresses the official **Angular Style Guide** as a grounded IDD graph: each major section is a `user_requirement`, and every individual rule is a `system_requirement` that `implements` its section. The guide reference lives in `attrs.source_ref`; the throughline UIDs are this source's own and immutable — a consumer cites a rule as `angular:SR-0001`, never by section name.

It carries
<!-- tl:count type == 'user_requirement' -->
9
<!-- tl:end --> sections and
<!-- tl:count type == 'system_requirement' -->
36
<!-- tl:end --> style rules.

## Purpose

<!-- tl:item INT-0001 -->
**INT-0001 — Angular applications are structured and written in one consistent style** — `intent`, status `approved`

> The Angular Style Guide exists so that Angular applications across teams read as though written by one author: a consistent way to name files and symbols, to structure an application, and to write components, directives and services, so that any engineer can locate, identify and change code they did not write, and keep responsibilities cleanly separated.

**source_ref**: Angular Style Guide
<!-- tl:end -->

## Single Responsibility

<!-- tl:item UR-0001 -->
**UR-0001 — Single Responsibility** — `user_requirement`, status `approved`

> Rules governing keeping each file and function focused on a single responsibility.

*Derives from:* INT-0001

**source_ref**: Angular Style Guide: Single Responsibility
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Angular Style Guide: Single Responsibility') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0001 | system_requirement | approved | Apply the single responsibility principle per file |
| SR-0002 | system_requirement | approved | Keep functions small |
<!-- tl:end -->

## Naming

<!-- tl:item UR-0002 -->
**UR-0002 — Naming** — `user_requirement`, status `approved`

> Rules governing file names, symbol names, selectors and test file names.

*Derives from:* INT-0001

**source_ref**: Angular Style Guide: Naming
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Angular Style Guide: Naming') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0003 | system_requirement | approved | Follow the feature-then-type naming pattern |
| SR-0004 | system_requirement | approved | Separate file names with dots and dashes |
| SR-0005 | system_requirement | approved | Name symbols and files consistently |
| SR-0006 | system_requirement | approved | Suffix service names appropriately |
| SR-0007 | system_requirement | approved | Put bootstrapping logic in main.ts |
| SR-0008 | system_requirement | approved | Name component element selectors in dashed case |
| SR-0009 | system_requirement | approved | Prefix component selectors with a custom prefix |
| SR-0010 | system_requirement | approved | Name directive selectors in lower camel case |
| SR-0011 | system_requirement | approved | Prefix directive selectors with a custom prefix |
| SR-0012 | system_requirement | approved | Name pipes consistently |
| SR-0013 | system_requirement | approved | Name unit test files after the tested file |
<!-- tl:end -->

## Application Structure and NgModules

<!-- tl:item UR-0003 -->
**UR-0003 — Application Structure and NgModules** — `user_requirement`, status `approved`

> Rules governing how an application is organised into folders and modules.

*Derives from:* INT-0001

**source_ref**: Angular Style Guide: Application Structure and NgModules
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Angular Style Guide: Application Structure and NgModules') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0014 | system_requirement | approved | Apply the LIFT principle |
| SR-0015 | system_requirement | approved | Organise folders by feature |
| SR-0016 | system_requirement | approved | Group shared declarables in a shared module |
<!-- tl:end -->

## Components

<!-- tl:item UR-0004 -->
**UR-0004 — Components** — `user_requirement`, status `approved`

> Rules governing how components are declared, decorated and kept lean.

*Derives from:* INT-0001

**source_ref**: Angular Style Guide: Components
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Angular Style Guide: Components') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0017 | system_requirement | approved | Give components an element selector |
| SR-0018 | system_requirement | approved | Extract non-trivial templates and styles to files |
| SR-0019 | system_requirement | approved | Decorate input and output properties |
| SR-0020 | system_requirement | approved | Avoid aliasing inputs and outputs |
| SR-0021 | system_requirement | approved | Delegate complex logic to services |
| SR-0022 | system_requirement | approved | Do not prefix output properties |
| SR-0023 | system_requirement | approved | Order component members consistently |
<!-- tl:end -->

## Directives

<!-- tl:item UR-0005 -->
**UR-0005 — Directives** — `user_requirement`, status `approved`

> Rules governing when and how attribute directives are written.

*Derives from:* INT-0001

**source_ref**: Angular Style Guide: Directives
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Angular Style Guide: Directives') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0024 | system_requirement | approved | Use an attribute directive for template-free behaviour |
| SR-0025 | system_requirement | approved | Prefer HostListener and HostBinding decorators |
<!-- tl:end -->

## Services

<!-- tl:item UR-0006 -->
**UR-0006 — Services** — `user_requirement`, status `approved`

> Rules governing services, their responsibilities and how they are provided.

*Derives from:* INT-0001

**source_ref**: Angular Style Guide: Services
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Angular Style Guide: Services') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0026 | system_requirement | approved | Treat services as singletons |
| SR-0027 | system_requirement | approved | Give a service a single responsibility |
| SR-0028 | system_requirement | approved | Provide a service at the root injector |
| SR-0029 | system_requirement | approved | Use the Injectable class decorator |
<!-- tl:end -->

## Data Services

<!-- tl:item UR-0007 -->
**UR-0007 — Data Services** — `user_requirement`, status `approved`

> Rules governing isolating server communication behind a data service.

*Derives from:* INT-0001

**source_ref**: Angular Style Guide: Data Services
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Angular Style Guide: Data Services') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0030 | system_requirement | approved | Talk to the server through a data service |
<!-- tl:end -->

## Lifecycle Hooks

<!-- tl:item UR-0008 -->
**UR-0008 — Lifecycle Hooks** — `user_requirement`, status `approved`

> Rules governing the use of lifecycle hook interfaces.

*Derives from:* INT-0001

**source_ref**: Angular Style Guide: Lifecycle Hooks
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Angular Style Guide: Lifecycle Hooks') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0031 | system_requirement | approved | Implement lifecycle hook interfaces |
<!-- tl:end -->

## Coding Conventions

<!-- tl:item UR-0009 -->
**UR-0009 — Coding Conventions** — `user_requirement`, status `approved`

> Rules governing class, constant, interface, member and import conventions.

*Derives from:* INT-0001

**source_ref**: Angular Style Guide: Coding Conventions
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Angular Style Guide: Coding Conventions') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0032 | system_requirement | approved | Name classes in upper camel case |
| SR-0033 | system_requirement | approved | Use const for values that do not change |
| SR-0034 | system_requirement | approved | Name interfaces without an I prefix |
| SR-0035 | system_requirement | approved | Do not underscore-prefix private members |
| SR-0036 | system_requirement | approved | Order and group import lines |
<!-- tl:end -->

