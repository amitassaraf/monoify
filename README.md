Monify
=
A bash 4.0+ script that creates a mono-repo from multiple repositories.

Creates a new repository named *uni[my_repo_name_here]* and in it are all the requested repositories with their git commit history included (and prefixed with the repo names).

the **unirepo** history will look like so:

    [API-MODULE] Added new route for login
    [WEB-MODULE] Removed logo from left panel
    [API-MODULE] New SSL enrcyption of traffic
    [MOBILE-MODULE] Added index.ios.js for iOS

Example usage:
-
monify create [new_repo_name] [repos_seperated_by_spaces] [git_project_url]

    monify create repo "api-module web-module mobile-module" git@bitbucket.org:project

This will create a mono repo like so

    megarepo (Build folder generated)
	--- api-module
	--- web-module
	--- mobile-module
	--- unirepo (This is the mono-repo)
	------ api-module
	------ web-module
	------ mobile-module

Mono-Repo vs Multi-Repo
-
If you are wondering why this exists then you should read some of the following posts to see the benefits of a mono-repo and what it is.
* https://medium.com/@patrickleet/mono-repo-or-multi-repo-why-choose-one-when-you-can-have-both-e9c77bd0c668
* http://www.gigamonkeys.com/mono-vs-multi/
* https://hackernoon.com/one-vs-many-why-we-moved-from-multiple-git-repos-to-a-monorepo-and-how-we-set-it-up-f4abb0cfe469

Requirements
-
* bash 4.0 and above
* If on OSX then **gsed** is required

Notes
-
This script was tested on OSX only but should work just fine with any Linux box.