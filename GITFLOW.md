# Git Flow

- **git clone https://….git** used for cloning a repository onto your local machine
- **git branch {branch}** used to create a new branch on your local machine
- **git checkout {branch}** used to switch to the new branch.
- **git add {file}** add a file to the staging area ready to commit.
- **git commit -am “commit comment goes here"** commit your changes to the branch.
- **git push -u origin {branch}** used to push your changes to the remote server.
- **git pull** used to pull down other people’s changes from that branch.

## GitHub flow strategy branches

main, features

### GitHub flow howto

1. With the GitHub flow, you only ever have 2 branches: main, features.
2. As with Git Flow, an empty main branch is created at the start of a new project.
3. Every change that is worked on is branched directly off of main into a feature branch.
4. Once a feature is ready it is tested on the feature branch and the code is reviewed before being merged to main.
5. Once the feature has been merged to main it should be released to production immediately.
6. Hotfixes are treated the same as feature branches as they branch off of main already.

## Git flow strategy branches

main, hotfix, release, develop, feature, feature-sub

### Git flow howto

1. Create new feature from develop branch. Once the feature implementation is complete, the feature branch should be merged back into the develop branch.
2. A release branch is created from the develop branch when the develop branch reaches the desired state for the new release. It is used to prepare for a new production release, only incorporating bug fixes and last-minute changes. The release branch is eventually merged into both the main and develop branches, and a tag is added to the main branch to mark the release. Merging the release branch into the develop branch ensures that the develop branch includes any last-minute changes made in the release branch. This ensures that future releases and feature implementations will also incorporate these changes.
3. The hotfix branches are created to immediately address critical bugs in the main branch, which represents the live production version. They are created from the tagged commit on the main branch corresponding to the production version. Once the hotfix is complete, it should be merged into both the main and develop branches. The reason for merging it into the develop branch is to ensure that future releases also include the bugfix.
4. The hotfix branches are created to immediately address critical bugs in the main branch, which represents the live production version. They are created from the tagged commit on the main branch corresponding to the production version. Once the hotfix is complete, it should be merged into both the main and develop branches. The reason for merging it into the develop branch is to ensure that future releases also include the bugfix.
5. However, if a release branch exists, the hotfix changes should be merged into that specific release branch instead of the develop branch because the fixes will eventually be merged into the develop branch when the release branch is finished. Meanwhile, the upcoming release can also include the changes to fix the issues in the next production version.


