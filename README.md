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

## Remove Rubberband
```
UPDATE EVENT SET FastEnemyRestrainMax=0;
UPDATE EVENT SET SlowEnemyBoostMax=0;
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


## Like The Wind AI Gearing Fixes
- Uses same as my pcsx2 patch found here https://github.com/scottadkin/Gran-Turismo-3-NTSC-Patches/blob/main/LikeTheWind/AI%20Gear%20Fixes%202/8AA991B0.pnach
```
UPDATE ENEMY_CARS SET FinalGear=2100 WHERE Label='ltw_h_zonda_c12s_00';
UPDATE ENEMY_CARS SET FinalGear=2700 WHERE Label='ltw_h_esprit_sport350_00';
UPDATE ENEMY_CARS SET FinalGear=2400 WHERE Label='ltw_h_supra_rz_97';
UPDATE ENEMY_CARS SET FinalGear=3250 WHERE Label='ltw_h_arta_nsx_00';
UPDATE ENEMY_CARS SET FinalGear=3200 WHERE Label='ltw_h__787b_91';
UPDATE ENEMY_CARS SET FinalGear=3550 WHERE Label='ltw_h_gt_one_race_99';
UPDATE ENEMY_CARS SET FinalGear=2800 WHERE Label='ltw_h_cerbera_speed12_00';
UPDATE ENEMY_CARS SET FinalGear=2750 WHERE Label='ltw_h_castrol_supra_00';
UPDATE ENEMY_CARS SET FinalGear=3000 WHERE Label='ltw_h_r34_gtr_v_99';
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

