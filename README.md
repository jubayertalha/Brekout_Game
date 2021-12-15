# brekout_game_opengl
This is a console break out game using opengl and c++ for Computer Graphics final project.

https://user-images.githubusercontent.com/64648244/146201252-c5054599-8755-430a-a3be-8c4f1195d099.mp4

The purpose of the project is to design and implement a 2-dimensional game written in C++. The project includes different levels of the game with documentation. In this game, a high score saves in a txt file. The high score depends on the highest score and time. The game will be a single-player game. The goal of this project is to create an easy to play game that could be played by all ages.

CONTROLS:

  Collision Control:
		
    There are different types of collision that needed to detect and update the next movement of the game. The main three types of collision are, wall collision, bar collision and brick collision.

			1. Bar Collision:
 
  ![bar_collision](https://user-images.githubusercontent.com/64648244/146200908-fb31de35-f36b-41d8-b002-dc2e673f6172.png)

			2. Brick Collision: 

 ![brick_collision](https://user-images.githubusercontent.com/64648244/146200972-bfd6d13a-e4bb-4111-8c6c-1bacd62fece1.png)

			3. Wall Collision:

 ![wall_collision](https://user-images.githubusercontent.com/64648244/146201006-c4a20ede-101a-4592-b766-ef9fd0c82a8e.png)

	Movement Control:
  
		There are two different types of ball movement and one brick movement in this game.

 ![movement](https://user-images.githubusercontent.com/64648244/146201069-d7d4f8ae-f322-40a7-93b7-1b9f56a76b65.png)

SYSTEM IMPLEMENTATION METHOD
	
	State Control:
  
		1. Start State: This is initial state. At this state time, score and level initialized with default value. One left mouse button click invoked play state.
    
		2. Play State: In this state all elements of the game are visible. Game paddle and ball is in middle of x-axis and the ball is on the top of the paddle. Both paddle and ball move with the mouse point on x-axis. One left mouse button click invoked running state.
    
		3. Running State: The game start running on this state. Ball start to moves initial 40-degree angle to right. Time starts to increase. Score increase with every bounce with the bricks. One left mouse button click invoked pause state. Breaking all breaks invoked level state. Dropping the ball to the bottom wall invoked over state.
    
		4. Pause State: In this state the game is off for some certain moment. Noting changes on the game. One left mouse button click invoked running state.
    
		5. Level State: Time stops and level increased in this state. It shows the new level. One left mouse button click invoked play state of the new level.
    
		6. Over State: In this state the game is over and player need to start all over again. If the new score is greater than high score then it shows it and changed the high 			score. One left mouse button invoked start state.
    
		7. Complete State: If all level is completed then this state is invoked. In this state the game is complete and player need to start the game again. If the new score is greater than high scorer then it shows it  and changed the high score. One left mouse button invoked start state.
