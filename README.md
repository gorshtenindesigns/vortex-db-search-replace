=== Vortex Advanced DB Search & Replace ===
Contributors: yan
Donate link:
Tags: search, replace, database, migration, tools
Requires at least: 5.0
Tested up to: 6.5
Stable tag: 2.1
License: GPLv2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html

A modern, safe search-and-replace plugin for WordPress with multi-table support, dry-run, and optional backups.

== Description ==
Vortex Advanced DB Search & Replace provides a simple admin UI to run multi-table and multi-field search/replace operations across your WordPress database. It includes:
Developed by Yan Jason Gorshtenin
Free To Use
Not For Profit
Just Acknowledge the good work.

- Multiple search/replace pairs
- Selective table targeting
- Dry-run mode (no changes)
- Optional per-table backups
- Sanitized inputs, nonce protection, and escaped outputs

Note: Replacing inside serialized data structures can corrupt serialized strings. This release adds a "Serialized-safe mode" which detects serialized values, unserializes them, performs replacements recursively, and re-serializes — preserving complex data structures. Serialized-safe mode is slower but recommended when working with `options`, `postmeta`, or other fields that may contain serialized PHP.

== Installation ==
1. Upload the `vortex-db-search-replace` folder to the `/wp-content/plugins/` directory.
2. Activate the plugin through the 'Plugins' screen in WordPress.
3. Visit Settings → Vortex Search & Replace to configure and run searches.

== Frequently Asked Questions ==
= Will this handle serialized data? =
Not currently by default. The plugin performs SQL-level REPLACE which can break serialized PHP strings. Use Dry Run to preview changes. Serialized-safe routines are available on request.

= How are backups stored? =
Backups are created as copies of tables in the same database with the suffix `_vortex_backup_{timestamp}`. If you prefer SQL dumps to the uploads folder, request that change.

== Screenshots ==
1. Admin settings and Execute Search & Replace UI.

== Changelog ==
= 2.1 =
* Sanitization and escaping improvements, nonce protection, per-table backups, dry-run support.
* Added Serialized-safe mode (batch processing) to safely replace strings inside serialized arrays/objects.
* Added per-run backup option and batch size control for large tables.
* Added Run History and CSV export: audit logs of each run stored in the database with downloadable CSVs.

== Upgrade Notice ==
= 2.1 =
Security hardening: settings sanitization and nonce checks. No breaking changes.

== Credits ==
Developed by Yan Gorshtenin – Vortex Solutions

