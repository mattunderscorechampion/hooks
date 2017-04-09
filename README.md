
# Git hooks

Git hooks provide a way to script behaviour that takes
place during certain git commands.
They can be used to provide additional verification of the
changes being made.

## fixup-pre-push

This git hook runs before pushing local changes to a remote
repository.
It checks that no commit messages contain the word 'fixup'
or some variation of it.
It is assumed that commits with such messages are intended
to be combined with other commits using rebase.
If such a commit is found it is reported through standard
output and the push prevented.
