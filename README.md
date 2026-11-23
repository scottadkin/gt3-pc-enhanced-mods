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

## Like The Wind Adding Different AI Cars
- R390 From the GT All Star Event, a stock Escudo and one with a torque modifier to try and match what a player can tune.
```
INSERT INTO ENEMY_CARS ('Label', 'Car', 'Brake', 'BrakeController', 'Steer', 'Chassis', 'Lightweight', 'RacingModify', 'Engine', 'PortPolish', 'EngineBalance', 'Displacement', 'Computer', 'NATune', 'TurbineKit', 'Drivetrain', 'Flywheel', 'Clutch', 'PropellerShaft', 'LSD', 'Gear', 'Suspension', 'Intercooler', 'Muffler', 'FrontTire', 'RearTire', 'ASCC', 'TCSC', 'Wheel', 'LSDInitialF', 'LSDAccelF', 'LSDDecelF', 'LSDInitialR', 'LSDAccelR', 'LSDDecelR', 'MaxSpeed', 'Bound1F', 'Bound2F', 'Rebound1F', 'Rebound2F', 'Bound1R', 'Bound2R', 'Rebound1R', 'Rebound2R', 'DownforceF', 'DownforceR', 'CamberF', 'CamberR', 'ToeF', 'ToeR', 'StabilizerF', 'StabilizerR', 'RideHeightF', 'RideHeightR', 'SpringRateF', 'SpringRateR', 'TCSCLevel', 'ASCCLevel', 'TorqueGain', 'FinalGear') VALUES ('ltw_h_r390_race_98', 'r390_race_98', 'br_r390_race_98_a', 'a', 'n1', 'ch_r390_race_98_a', NULL, 'rm_r390_race_98_a', 'en_r390_race_98_a', NULL, NULL, NULL, NULL, NULL, 'tk_r390_race_98_a', 'dt_r390_race_98_a', NULL, 'cl_r390_race_98_a', NULL, 'ls_r390_race_98_a', 'ge_r390_race_98_a', 'su_r390_race_98_a', NULL, 'mu_r390_race_98_a', 'ft_r390_race_98_a', 'rt_r390_race_98_a', 'a', 'a', NULL, 0, 0, 0, 10, 40, 20, 40, 7, 7, 7, 7, 7, 7, 7, 7, 74, 91, 20, 10, 128, 128, 4, 4, 85, 85, 158, 138, 6, 11, 1810, 3429);
INSERT INTO ENEMY_CARS ('Label', 'Car', 'Brake', 'BrakeController', 'Steer', 'Chassis', 'Lightweight', 'RacingModify', 'Engine', 'PortPolish', 'EngineBalance', 'Displacement', 'Computer', 'NATune', 'TurbineKit', 'Drivetrain', 'Flywheel', 'Clutch', 'PropellerShaft', 'LSD', 'Gear', 'Suspension', 'Intercooler', 'Muffler', 'FrontTire', 'RearTire', 'ASCC', 'TCSC', 'Wheel', 'LSDInitialF', 'LSDAccelF', 'LSDDecelF', 'LSDInitialR', 'LSDAccelR', 'LSDDecelR', 'MaxSpeed', 'Bound1F', 'Bound2F', 'Rebound1F', 'Rebound2F', 'Bound1R', 'Bound2R', 'Rebound1R', 'Rebound2R', 'DownforceF', 'DownforceR', 'CamberF', 'CamberR', 'ToeF', 'ToeR', 'StabilizerF', 'StabilizerR', 'RideHeightF', 'RideHeightR', 'SpringRateF', 'SpringRateR', 'TCSCLevel', 'ASCCLevel', 'TorqueGain', 'FinalGear') VALUES ('ltw_h_escudo_pikespeak_00', 'escudo_pikespeak_00', 'br_escudo_pikespeak_00_a', 'n', 'n1', 'ch_escudo_pikespeak_00_a', NULL, 'rm_escudo_pikespeak_00_a', 'en_escudo_pikespeak_00_a', NULL, NULL, NULL, NULL, NULL, 'tk_escudo_pikespeak_00_a', 'dt_escudo_pikespeak_00_a', NULL, 'cl_escudo_pikespeak_00_a', NULL, 'ls_escudo_pikespeak_00_a', 'ge_escudo_pikespeak_00_a', 'su_escudo_pikespeak_00_a', NULL, 'mu_escudo_pikespeak_00_a', 'ft_escudo_pikespeak_00_a', 'rt_escudo_pikespeak_00_a', 'a', 'a', NULL, 10, 20, 10, 10, 40, 20, 0, 5, 5, 5, 5, 5, 5, 6, 7, 24, 35, 20, 10, 128, 128, 4, 4, 140, 140, 137, 65, 6, 11, 1800, 1500);
INSERT INTO ENEMY_CARS ('Label', 'Car', 'Brake', 'BrakeController', 'Steer', 'Chassis', 'Lightweight', 'RacingModify', 'Engine', 'PortPolish', 'EngineBalance', 'Displacement', 'Computer', 'NATune', 'TurbineKit', 'Drivetrain', 'Flywheel', 'Clutch', 'PropellerShaft', 'LSD', 'Gear', 'Suspension', 'Intercooler', 'Muffler', 'FrontTire', 'RearTire', 'ASCC', 'TCSC', 'Wheel', 'LSDInitialF', 'LSDAccelF', 'LSDDecelF', 'LSDInitialR', 'LSDAccelR', 'LSDDecelR', 'MaxSpeed', 'Bound1F', 'Bound2F', 'Rebound1F', 'Rebound2F', 'Bound1R', 'Bound2R', 'Rebound1R', 'Rebound2R', 'DownforceF', 'DownforceR', 'CamberF', 'CamberR', 'ToeF', 'ToeR', 'StabilizerF', 'StabilizerR', 'RideHeightF', 'RideHeightR', 'SpringRateF', 'SpringRateR', 'TCSCLevel', 'ASCCLevel', 'TorqueGain', 'FinalGear') VALUES ('ltw_h_escudo_pikespeak_00_stock', 'escudo_pikespeak_00', 'br_escudo_pikespeak_00_a', 'n', 'n1', 'ch_escudo_pikespeak_00_a', NULL, 'rm_escudo_pikespeak_00_a', 'en_escudo_pikespeak_00_a', NULL, NULL, NULL, NULL, NULL, 'tk_escudo_pikespeak_00_a', 'dt_escudo_pikespeak_00_a', NULL, 'cl_escudo_pikespeak_00_a', NULL, 'ls_escudo_pikespeak_00_a', 'ge_escudo_pikespeak_00_a', 'su_escudo_pikespeak_00_a', NULL, 'mu_escudo_pikespeak_00_a', 'ft_escudo_pikespeak_00_a', 'rt_escudo_pikespeak_00_a', 'a', 'a', NULL, 10, 20, 10, 10, 40, 20, 0, 5, 5, 5, 5, 5, 5, 6, 7, 24, 35, 20, 10, 128, 128, 4, 4, 140, 140, 137, 65, 6, 11, 1000, 1900);
INSERT INTO EVENT ('Opponent12') VALUES ('ltw_h_r390_race_98');
INSERT INTO EVENT ('Opponent13') VALUES ('ltw_h_escudo_pikespeak_00');
INSERT INTO EVENT ('Opponent14') VALUES ('ltw_h_escudo_pikespeak_00_stock');
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

