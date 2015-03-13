### Aptitude search terms

Long form | Short form | Description
----------|------------|-------------
?=variable | |Select the package bound to variable; see the section called “Explicit search targets”.
?not(pattern) |!pattern	| Select any package that does not match pattern.
?action(action)	| ~aaction | Select packages that have been marked for the given action (e.g., “install” or “upgrade”).
?all-versions(pattern) | | Select packages whose versions all match pattern.
?and(pattern1, pattern2) || pattern1 pattern2	Select any package that matches both pattern1 and pattern2.
?any-version(pattern) |	| Select packages for which at least one version matches pattern.
?architecture(architecture)	| ~rarchitecture | Select packages for the given architecture (such as “amd64”, or “all”). Special values: native and foreign.
?archive(archive) | ~Aarchive| Select packages from the given archive (such as “unstable”).
?automatic | ~M | Select packages that were automatically installed.
?bind(variable, pattern) | ?variable:term-name[(args)] | Selects anything if variable matches pattern; see the section called “Explicit search targets”.
?broken	~b | | Select packages that have a broken dependency.
?broken-depType | ~BdepType | Select package that have a broken dependency of the given depType.
?broken-depType(pattern) | ~DB[depType:]pattern | Select packages that have a broken dependency of the given depType matching pattern.
?broken-reverse-depType(pattern) | ~RBdepType:pattern| Select packages that a package matching pattern declares a broken dependency of type depType.
?conflicts(pattern) | ~Cpattern | Select packages that conflict with a package matching pattern.
?config-files | ~c | Select packages that were removed but not purged.
?depType(pattern) | ~D[depType:]pattern | Match packages that declare a dependency of type depType on a package matching pattern.
?description(description) | ~ddescription | Select packages whose description matches description.
?essential | ~E | Select essential packages, those with Essential: yes in their control files.
?exact-name(name)| | Select packages named name.
?false | ~F | Select no packages.
?for variable: pattern | | Select packages that match pattern with variable bound to the package being matched; see the section called “Explicit search targets”.
?garbage | ~g | Select packages that are not required by any manually installed package.
?installed | ~i | Select installed packages.
?maintainer(maintainer) | ~mmaintainer | Select packages maintained by maintainer.
?multiarch(multiarch) | | Select packages with a multi-arch capability of multiarch (that is, either “foreign”, “same”, “allowed”, or “none”).
?narrow(filter, pattern) | ~S filter pattern | Select packages for which a single version matches both filter and pattern.
?name(name) | ~nname, name | Select packages with the given name.
?new | ~N | Select new packages.
?obsolete | ~o | Match installed packages that cannot be downloaded.
?or(pattern1, pattern2)	| pattern1 or pattern2 | Select packages that match pattern1, pattern2, or both.
?origin(origin) | ~Oorigin | Select packages with the given origin.
?provides(pattern) | ~Ppattern | Select packages that provide a package matching pattern.
?priority(priority) | ~ppriority | Select packages with the given priority.
?reverse-depType(pattern) | ~R[depType:]pattern | Select packages that are the targets of a dependency of type depType declared by a package matching pattern.
?reverse-broken-depType(pattern) | ~RBdepType:pattern| Select packages that are the targets of a broken dependency of type depType declared by a package matching pattern.
?section(section) | ~ssection | Select packages in the given section.
?source-package(name) | | Select packages whose source package name matches the regular expression name.
?source-version(version)| | Select packages whose source version matches the regular expression version.
?tag(tag) | ~Gtag | Select packages that have the given debtags tag.
?term(keyword)| | Full-text search for packages that contain the given keyword.
?term-prefix(keyword) | | Full-text search for packages that contain a keyword that begins with the given keyword.
?true | ~T | Select all packages.
?task(task) | ~ttask | Select packages that are in the given task.
?upgradable | ~U | Select packages that are installed and can be upgraded.
?user-tag | | Select packages that are marked with a user-tag matching the regular expression user-tag.
?version(version) | ~Vversion | Select packages whose version matches version (special values: CURRENT, CANDIDATE, and TARGET).
?virtual | ~v | Select virtual packages.
?widen(pattern) | ~Wpattern | Select versions for which pattern matches any version of the corresponding package, discarding local version restrictions.


Source: https://aptitude.alioth.debian.org/doc/en/ch02s04s05.html