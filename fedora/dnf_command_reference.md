# DNF Command Reference Guide

## Core Package Management
*   **install:** Install software.
*   **remove:** Remove (uninstall) software.
*   **upgrade:** Upgrade software.
*   **downgrade:** Downgrade software.
*   **reinstall:** Reinstall software.
*   **swap:** Remove software and install another in one transaction.
*   **autoremove:** Remove all unneeded packages originally installed as dependencies.
*   **builddep:** Install build dependencies for a package or spec file.
*   **debuginfo-install:** Install debuginfo packages.
*   **mark:** Change the reason for an installed package.

## Search and Information
*   **search:** Search for software matching all specified strings.
*   **info:** List packages depending on their relation to the system with additional details.
*   **list:** List packages depending on their relation to the system.
*   **provides:** Find what package provides the given value.
*   **repoquery:** Search for packages matching various criteria.
*   **leaves:** List groups of installed packages not required by other installed packages.
*   **changelog:** Show package changelogs.
*   **repoclosure:** Print a list of unresolved dependencies for repositories.

## System Updates and Upgrades
*   **check-upgrade:** Check for available package upgrades.
*   **distro-sync:** Upgrade or downgrade installed software to the latest available versions.
*   **system-upgrade:** Prepare the system for an upgrade to a new release.
*   **needs-restarting:** Determine whether the system or systemd services need restarting.

## Offline Operations
*   **offline:** Manage offline transactions.
*   **offline-upgrade:** Store an upgrade transaction to be performed offline.
*   **offline-distrosync:** Store a distro-sync transaction to be performed offline.

## Repository and Configuration Management
*   **repo:** Manage repositories.
*   **config-manager:** Manage configuration.
*   **copr:** Manage Copr repositories (add-ons provided by users/community/third-party).
*   **reposync:** Synchronize a remote DNF repository to a local directory.
*   **repomanage:** Manage a directory with repodata or with rpm packages.
*   **makecache:** Generate the metadata cache.
*   **clean:** Remove or expire cached data.

## Transactions and History
*   **do:** Do transaction.
*   **history:** Manage transaction history.
*   **replay:** Replay a transaction that was previously stored in a directory.

## Group and Module Management
*   **group:** Manage comps groups.
*   **environment:** Manage comps environments.
*   **module:** Manage modules.

## Advanced Management
*   **advisory:** Manage advisories.
*   **check:** Check for problems in the packagedb.
*   **download:** Download software to the current directory.
*   **versionlock:** Manage versionlock configuration.

## Common Aliases
*   **check-update:** Alias for `check-upgrade`.
*   **grp:** Alias for `group`.
*   **repoinfo:** Alias for `repo info`.
*   **repolist:** Alias for `repo list`.
*   **updateinfo:** Alias for `advisory`.
*   **upgrade-minimal:** Alias for `upgrade --minimal`.
