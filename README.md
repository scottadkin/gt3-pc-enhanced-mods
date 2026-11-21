# gt3-pc-enhanced-mods

# Make backups of the original files before using.

## All Cars 1 Credit
```
UPDATE CAR set price=1
```

## Remove AI Max Throttle Limits
```
UPDATE EVENT SET EnemySkillA_RWD=100,
EnemySkillA_FWD=100,
EnemySkillA_4WD=100,
EnemySkillA_GTR=100,
EnemySkillB_RWD=100,
EnemySkillB_FWD=100,
EnemySkillB_4WD=100,
EnemySkillB_GTR=100,
EnemySkillC_RWD=100,
EnemySkillC_FWD=100,
EnemySkillC_4WD=100,
EnemySkillC_GTR=100,
EnemySkillC2_RWD=100,
EnemySkillC2_FWD=100,
EnemySkillC2_4WD=100,
EnemySkillC2_GTR=100
```

## Give AI Extreme Slow Down
- If you fall behind the AI cars too much they will slow down to 1% speed.
```
UPDATE EVENT SET FastEnemyRestrainMax=99;
```

## Give AI Extreme Catch Up(buggy with racing cars)
- Make the AI cars up to 500% faster if they fall too far behind.
```
UPDATE EVENT SET SlowEnemyBoostMax=500;
```

## Like The Wind
- Give All AI Cars Dodge Viper Engine, drivetrain, gearing and remove turbos and mufflers.(Changing racing modifier changes the car model)
```
UPDATE ENEMY_CARS SET Engine='en_viper_gts_00_a',TurbineKit='na',Drivetrain='dt_viper_gts_00_a',Clutch='cl_viper_gts_00_a',LSD='ls_viper_gts_00_a',Gear='ge_viper_gts_00_a',Muffler=NULL,FinalGear=3070 where Label LIKE 'ltw_h_%'
```

- Give All AI cars Escudo Engine, Alto Works Stage 3 Turbo, and leftovers from viper video.
```
UPDATE ENEMY_CARS SET Engine='en_escudo_pikespeak_00_a',TurbineKit='tk_altoworks_sport_ltd_97_d',Drivetrain='dt_viper_gts_00_a',Clutch='cl_viper_gts_00_a',LSD='ls_viper_gts_00_a',Gear='ge_viper_gts_00_a',Muffler=NULL,FinalGear=2070 where Label LIKE 'ltw_h_%'
```


## TVR Speed 12 Extra Upgrades
- Mufflers
```
INSERT INTO MUFFLER ('Label', 'Car', 'Kind', 'TorqueTopRate', 'TorqueBottomRate', 'Price') VALUES ('mu_cerbera_speed12_00_a', 'cerbera_speed12_00', 1, 104, 104, 4800);
INSERT INTO MUFFLER ('Label', 'Car', 'Kind', 'TorqueTopRate', 'TorqueBottomRate', 'Price') VALUES ('mu_cerbera_speed12_00_b', 'cerbera_speed12_00', 2, 107, 107, 5555);
INSERT INTO MUFFLER ('Label', 'Car', 'Kind', 'TorqueTopRate', 'TorqueBottomRate', 'Price') VALUES ('mu_cerbera_speed12_00_c', 'cerbera_speed12_00', 3, 122, 122, 6666);
```
- Racing Chip
```
INSERT INTO COMPUTER ('Label', 'Car', 'Kind', 'TorqueTopRate', 'TorqueBottomRate', 'Price') VALUES ('nt_cerbera_speed12_00_a', 'cerbera_speed12_00', 1, 104, 104, 1234);
```
- Engine Balancing 
```
INSERT INTO 'main'.'ENGINEBALANCE' ('Label', 'Car', 'Kind', 'CurveRpmAdd', 'RevLimitAdd', 'TorqueTopRate', 'TorqueBottomRate', 'Price') VALUES ('eb_cerbera_speed12_00_a', 'cerbera_speed12_00', 1, 1, 1, 102, 102, 12333);
```

- NA Tune
```
INSERT INTO NATUNE ('Label', 'Car', 'Kind', 'CurveRpmAdd', 'RevLimitAdd', 'TorqueTopRate', 'TorqueBottomRate', 'Price') VALUES ('nt_cerbera_speed12_00_b', 'cerbera_speed12_00', 2, 3, 2, 251, 248, 24000);
INSERT INTO NATUNE ('Label', 'Car', 'Kind', 'CurveRpmAdd', 'RevLimitAdd', 'TorqueTopRate', 'TorqueBottomRate', 'Price') VALUES ('nt_cerbera_speed12_00_c', 'cerbera_speed12_00', 3, 5, 3, 457, 456, 676767);

```