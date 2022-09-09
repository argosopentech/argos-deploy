#!/bin/bash

ARGOS_GIT_DIR="$HOME/git"

# Install git repositories
for gitrepository in $(cat git-repositories)
do
	cd $ARGOS_GIT_DIR
	git clone $gitrepository 2>/dev/null
done

# Run Argos Deploy
ARGOS_DEPLOY_DIR="$ARGOS_GIT_DIR/argos-deploy"
cd $ARGOS_DEPLOY_DIR
for s in $(ls s)
do
	. "s/$s/init.sh"
done

