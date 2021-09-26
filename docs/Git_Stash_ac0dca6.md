<!-- loioac0dca68c13642dcbd787f5885615520 -->

# Git Stash

Use *Stash* to record the current state to the working directory and then go back to a clean working directory. Your local changes are saved and the directory reverts to match the HEAD commit.



<a name="loioac0dca68c13642dcbd787f5885615520__section_tg1_slt_f4b"/>

## Pop Stash

Removes a single entry from the stash list and applies it on top of the current working tree state. This is the inverse operation of stash push.

If there are conflicts, the entry is not removed from the stash list. You need to resolve the conflicts and perform stash drop manually afterwards.



<a name="loioac0dca68c13642dcbd787f5885615520__section_irq_rlt_f4b"/>

## Pop Latest Stash

Removes the latest entry from the stash list and applies it on top of the current working tree state.



<a name="loioac0dca68c13642dcbd787f5885615520__section_twh_dlt_f4b"/>

## Apply Stash

Takes a single entry from the stash list and applies it on top of the current working tree state. This functionality is like Pop Stash, but without removing the entry from the stash list.



<a name="loioac0dca68c13642dcbd787f5885615520__section_cyg_dlt_f4b"/>

## Apply Latest Stash

Takes the latest entry from the stash list and applies it on top of the current working tree state.



<a name="loioac0dca68c13642dcbd787f5885615520__section_zs3_dlt_f4b"/>

## Drop Stash

Removes a single stash entry from the list of stash entries.



