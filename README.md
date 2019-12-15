# Baseball-stats-project
A project-in-progress using RStudio and Sqlite to create a database.

The original four files:
  Main file: game_log. This file contains data on baseball games played from 1871 to 2016. Definitions: putouts: the number of times a defensive player got an offensive player out. def_pos: Stands for defensive position. Indicates which defense position the player takes. The position list follows: 
  1. Pitcher 
  2. Catcher 
  3. First base 
  4. Second base 
  5. Third base 
  6. Shortstop 
  7. Left field 
  8. Center field 
  9. Right field 

The player’s number does not necessarily correspond to their defensive position.

Helper files: 
  1. person_codes: contains the IDs, names, and start date for players, coaches, and umpires referenced in the game_log. Primary key is id. Various correlations in the game_log: _umpire_id, _manager_id, _player_id; _pitcher_name, _manager_name, _umpire_name. 
  2. park_codes: Contains name, location, league, and usage dates. Primary key is park_id, which corresponds to park_id in the game_log file. 
  3. team_codes: Lists the team information, such as league and location. Primary key is team_id, which is contained in game_log/v_name and game_log/h_name. Following is a guide to the league abbreviations.
  AA = American Association (1882-1891)
  AL = American League (est. 1901)
  FL = Federal League (1914-1915)
  NL = National League (est. 1876)
  PL = Player's League (1890)
  UA = Union Association (1884)
	4. appearance_type: Lists the various positions (offensive, defensive, manager, umpire, etc.) with their respective codes and categories. Primary key is appearance_type_id.

The new tables are as follows:
  1. person = contains the id, last name, and first name of individual named in each game.
  2. league = lists just the id and league name based on the league information above.
  3. appearance_type = describes the job each person had in the game, i.e. pitcher, manager, left field umpire.]
  4. team_info = contains all the team information.
  5. game = derived mainly from the game_log table, it contains the game-specific information.
  
The database name is bb.db.
