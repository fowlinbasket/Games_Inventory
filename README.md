1) Requirements Specification
    An app that shows an inventory of videogames alongside their cover art and several checkboxes
    The checkboxes will indicate if the game is owned, played, finished, completed, etc.
    Clicking on the game takes user into a new activity with more information on the game, including
    an option to rate the game.
    User is awarded with some sort of medal or something for different tiers of completion in games
    There can also be a screen to show statistics
    There should be a button somewhere to add new games to the database

2) Design
    Models:
        VideoGame
            Boolean owned
            Boolean played
            Boolean finished
            Boolean completed
            String name
            String imageURI
            String iconURI
            double id
        BoardGame
            Boolean owned
            Boolean played
            String name
            String imageURI
            String iconURI
            double id

    Views:
        gamesView (overview of games with names, icons, and checkboxes all laid out on a scrollView)
        statsView (overview of game statistics/percentages)
        createNewGameView (create a new game)
        gameView (individual view of a game with cover art and all checkboxes, and a review option)

    Presenters:
        gamesPresenter (presents the entire database of games to the view layer)
        statsPresenter (analyzes the entire database and gets the stats)
            double percentageOwned()
            double percentagePlayed()
            double percentageFinished()
            double percentageCompleted()

    View Components:
        clickableGameCard (contains icon, name, and checkboxes all wrapped up in an elegant MaterialCardView)
        MaterialInput (an editable, elegant text box)
