# dotnet-monorepo-microservices-template

Project structure of monorepo microservices using Git Submodules

#### Add submodule with subservice repository
run `git submodule add -b <subservice branch> <subservice repository url> <path to store subservice>`.
	ex. `git submodule add -b main https://github.com/ciizo/dotnet-subservice-template.git ./src/Services/SubrepoService`.

#### Clone submodule repository
run
	* `git submodule init`.
	* `git submodule update`.

#### Pull change of submodule repository
track remote branch (if not done yet) `git config -f .gitmodules submodule.<submodule>.branch <branch name> [--merge] [--rebase]`.
	ex. `git config -f .gitmodules submodule.src/Services/SubrepoService.branch develop`.
run `git submodule update --remote`.

or cd and fetch/merge at submodule repository directory.

#### Remove submodule repository
run `git submodule deinit -f <submodule>`.
	ex. `git submodule deinit -f src/Services/SubrepoService`.
