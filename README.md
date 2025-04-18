# ActionSpeedKeeper
Class for Project Zomboid to prevent resetting the game speed while performing multiple actions

## How to use:

-- Creates a new instance of the ActionSpeedKeeper class  
-- The 'playerObj' argument represents the player object that the speed keeper will manage  
-- ie getPlayer() or getSpecificPlayer(playerIndex)  
  
`local actionSpeedKeeper = ActionSpeedKeeper:new(playerObj)`  
  
-- Adds a stop condition to the instance of ActionSpeedKeeper  
-- The condition is a function that returns true or false  
-- "true to stop actions and reset game speed" is a placeholder; in practice, the condition should evaluate a specific gameplay state  
  
`actionSpeedKeeper:AddStopCondition(function(playerObj)
    return "true to stop actions and reset game speed"
end)`  

-- Starts the speed management process for the player object  
-- This method sets up the event listener to monitor and control game speed based on the defined conditions  
  
`actionSpeedKeeper:KeepSpeed()`  
