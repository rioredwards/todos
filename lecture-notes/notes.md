## Alchemy Notes: ToDo’s (CRUD)

Demo code (Cat Tracker)

Update:

-   in displayCats() addEventListener for each cat
    -   in event listener: call updateLives()
    -   in updateLives(): client call with .update()
    -   check for error
    -   no error: get index of cat in cats[], then replace with updated cat

Remove:

-   addEventListener on remove button
    -   in event listener: call removeDeadCats()
        -   in removeDeadCats():
            -   call getUser()
            -   call client.delete with .lte('lives', 0)
                ++ lte is a filter. "less than/equal to"
        -   Check for error
        -   Else:
            -   const aliveCats = []
            -   for cats:
                -   if (lives > 0) push to aliveCats
            -   displayCats()
