# Nexus Designer

## Pre-requisites

-   Git and Github

-   Docker Desktop 4.23.0

-   The development and runtime environment specific to your work, along with any other tools

## Setup

-   Rename `.env.sample` to `.env`. Edit any variables inside if needed
-   Run `git submodule update --init --recursive --remote`

-   Open `the module you would like to work on in your IDE`

## Workflow

### Getting updates from all modules

-   Change into the super-directory (the directory where nexus-designer/nd_all was cloned)

-   Run the command `git submodule update --init --recursive --remote to get updates from all modules`

> Setup an alias for this command with:
> `git config --local --add alias.supdate 'submodule update --init --recursive --remote'`

Then, you can run git supdate to do the same thing as above

### Getting updates from one specific module

This is the same as how one would control a single repository. Simply run `git fetch and git merge or just git pull`

### Publishing updates

This is the same as how one would control a single repository. Simply commit your changes and run `git push`

### Testing modules

We use Docker to orchestrate module builds and testing.

Change into the super-directory (the directory where `nexus-designer/nd_all` was cloned)

**To test a single module in isolation:** Run `docker compose up <service-name>` where \<service-name> is the service name assigned to the module you want to execute.

**To test a multiple modules:** Run `docker compose up <service1-name> <service2-name>` where \<serviceX-name> is the service name assigned to the module you want to execute.

**To test all modules:** Run `docker compose up`
