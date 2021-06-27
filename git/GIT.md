# Git Repository Configuration Guide

All necessary setup steps for a new Git repository will be documented here.

The best practices here are based on empirical evidence and are subject to change.

## New Project Initialization

1. Create a new directory, where `<PATH_TO_DIRECTORY>` is the relative (or absolute) file path of the new project.
   ```shell
   mkdir -p <PATH_TO_DIRECTORY>
   ```
1. Initialize the directory for a Git repository.
   ```shell
   cd <PATH_TO_DIRECTORY> && git init
   ```
1. Add a `.gitignore` based on the project framework(s).
   ```shell
   touch .gitignore
   ```
   - See: [GitHub's collection of .gitignore templates](https://github.com/github/gitignore)
1. Choose a license that best fits the project.
   ```shell
   touch LICENSE
   ```
   - See: [choosealicense.com](https://choosealicense.com/) for guidance.
1. Start a changelog. See [keepachangelog.com](https://keepachangelog.com/en/1.0.0/) for examples and formats.
1. Add a `README.md` where <PROJECT_NAME> is the human-readable name of the project (Final style pending).
   ```shell
   echo "# <PROJECT_NAME>" >> README.md
   ```
   - See: [18F's "Making READMEs readable](https://github.com/18F/open-source-guide/blob/18f-pages/pages/making-readmes-readable.md)
   - See: [Matias Singers's Curated list of awesome READMEs](https://github.com/matiassingers/awesome-readme)
1. Configure a git commit messages template where `<PATH/TO/GITMESSAGE>` is the relative (or absolute) file path to the [.gitmessage](.gitmessage) file.
   ```shell
   git config --global commit.template <PATH/TO/GITMESSAGE>
   ```
   - See: [Chris Beam's "How to Write a Git Commit Message"](https://chris.beams.io/posts/git-commit/)
1. Create the first commit for the project where `<URL_TO_GITHUB_REPOSITORY>` is the link to the new project repository on GitHub.
   ```shell
   git add . # Use IFF changed files are solely those listed above
   git commit -m "chore: Initialize project"
   git branch -M main
   git remote add origin <URL_TO_GITHUB_REPOSITORY>
   git push -u origin main
   ```

## Future Additions

- [ ] CLI Configuration
- [ ] SSH Configuration
- [ ] Fork Configuration
- [ ] Tags/Releases
