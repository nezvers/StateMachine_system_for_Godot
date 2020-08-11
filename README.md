# State Machine System for Godot
Flexible and lightweight StateMachine for Godot and each system related code row is commented.
States are plain scripts without extending any class except default Reference what GDScript is. States are added to StateMachine through exported script Array. Decision on default State choice must be implemented per use case (Player, Camera, Pickup, Enemy).

Project is also simple use case for platformer (Idle, Walk, Jump)

## Usage
* Create StateMachine inherited script for different types of use cases (example - PlayerStateMachine);
* Create State inherited state scripts (example - PlayerState -> PlayerIdle);
* Use virtual functions inheritted from State (_unhandled_input, _physics_process, _process, state_check);
* Add State scripts into StateMachine exported script_array. PlayerStateMachine implements default state choice, you can change it to script_array[0] instead of String key.

## IMPORTANT
* Each new state needs to implement:
```
func _init(_sm).(_sm)->void:
	name = "Idle"
```
## Walkthrough
<div align="center">
      <a href="https://www.youtube.com/watch?v=Dpf2f31zKic">
     <img 
      src="https://img.youtube.com/vi/Dpf2f31zKic/0.jpg" 
      alt="State machine walkthrough" 
      style="width:100%;">
      </a>
    </div>
