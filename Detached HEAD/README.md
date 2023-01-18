# Detached HEAD
You are currently in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this state
without impacting any branches by performing another checkout.


If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

 git switch -c <new-branch-name>

Or undo this operation with:

git switch -

----------------------------------------------------------------

O commit mais recente aponta para o commit anterior.
A branch main ou master referencia o ultimo commit da branch principal.
Head aponta onde voce esta entre os commits dentro das branches.
Quando voce faz checkout de um commit anterior de uma branch, voce esta em detached HEAD. quer dizer esta fora da ultimo commit da branch.
Voce pode criar uma nova branch para manter os commits que voce criou, git switch -c <new-branch-name>.