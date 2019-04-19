# krillspace

Mono Style Multi Repo for those who wants to use multiple repository under a common structure.  Uses Yarn workspaces and git under the hood. Using krillspace you can add multi repository and treat it like mono repo.

1. Each repository lives in its own git repo
2. Each repository has it's own versions.
3. Since the each repository has it's own git, they are added to .gitignore by default.  

Commands

syntax
krillspace command options

Commands
init - creates new krillspace (Yarn workspace in disguise), sets the yarn's workspaces-experimental flag to true and create's a package.json file with private field set to true and workspace field set to ["packages/*"].

add - Adds new repository to krillspace. It takes git repo path as a parameter and usuall git clone internally to download the repo.

example to add a repo named "Repo A" whose github url is https://github.com/username/repo.git to your project do the following

"krillspace add https://github.com/username/repo.git"
The above command will download the repo to a folder called packages and do a yarn install.

remove - removes the repository.

To add nodejs modules use yarn workspace commands.
