# gt3-pc-enhanced-mods

## Like The Wind
- Give All AI Cars Dodge Viper Engine, drivetrain, gearing and remove turbos and mufflers.(Changing racing modifier changes the car model)
```
UPDATE ENEMY_CARS SET Engine='en_viper_gts_00_a',TurbineKit='na',Drivetrain='dt_viper_gts_00_a',Clutch='cl_viper_gts_00_a',LSD='ls_viper_gts_00_a',Gear='ge_viper_gts_00_a',Muffler=NULL,FinalGear=3070 where Label LIKE 'ltw_h_%'
```

- Give All AI cars Escudo Engine, Alto Works Stage 3 Turbo, and leftovers from viper video.
```
UPDATE ENEMY_CARS SET Engine='en_escudo_pikespeak_00_a',TurbineKit='tk_altoworks_sport_ltd_97_d',Drivetrain='dt_viper_gts_00_a',Clutch='cl_viper_gts_00_a',LSD='ls_viper_gts_00_a',Gear='ge_viper_gts_00_a',Muffler=NULL,FinalGear=2070 where Label LIKE 'ltw_h_%'
```