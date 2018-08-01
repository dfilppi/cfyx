## CFYX - A pragmatic utility wrapper for the Cloudify CLI

### Installation

Put the cfyx file in a directory of your choice, and add it to the beginning of your PATH variable ( via .bash_profile, etc...).  Also add an alias for complete transparency, e.g. alias cfy=cfyx

### Theory of operation

The goal _cfyx_ is to simplify life for those who use the Cloudify CLI a lot.  It does this by storing some state in your $HOME/.cfyx directory.  All commmands to _cfyx_ get ultimately passed through to _cfy_, but potential changed or enhanced.  For the execution/deployment tracking to work, you need to use _cfyx_ for all Cloudify CLI interactions.  Note that currently _cfyx_ is not tenant aware, IOW it doesn't have separate state for each tenant.  Note also that partial commands work, e.g. _cfyx can_ will trigger a cancel of the last execution.


### Commands

* _cfyx context_ - Prints current context
* _cfyx cancel_ - Cancels the last execution
* _cfyx uninstall_ - Uninstalls the last deployment
* _cfyx cuninstall_ - Cancels and uninstalls the last deployment
* _cfyx dd__ - Deletes current deployment, offers uninstall if needed
* _cfyx elist_ - Lists executions for last deployment
* _cfyx dlist_ - Lists deployments
* _cfyx evlist_ - Lists events for last execution
