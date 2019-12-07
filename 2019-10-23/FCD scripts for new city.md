### FCD scripts for new city







```sql
INSERT INTO FCD_ALL_HIGHWAYS_EAST (SegmentId, Lengthmm, RoadClass, OptimalSpeedKph, SpeedLimitKph, WKT) SELECT SegmentId, Lengthmm, RoadClass, OptimalSpeedKph, SpeedLimitKph, WKT FROM FCD_EAST WHERE RoadClass=1 ON DUPLICATE KEY UPDATE FCD_ALL_HIGHWAYS_EAST.SegmentId = FCD_ALL_HIGHWAYS_EAST.SegmentId;


INSERT INTO FCD_ALL_HIGHWAYS_WEST (SegmentId, Lengthmm, RoadClass, OptimalSpeedKph, SpeedLimitKph, WKT) SELECT SegmentId, Lengthmm, RoadClass, OptimalSpeedKph, SpeedLimitKph, WKT FROM FCD_WEST WHERE RoadClass=1 ON DUPLICATE KEY UPDATE FCD_ALL_HIGHWAYS_WEST.SegmentId = FCD_ALL_HIGHWAYS_WEST.SegmentId;


CREATE TABLE `tkm_fcd`.`mun_segment`  (
  `segment_id` int(11) NOT NULL,
  `lengthmm` int(11) NOT NULL,
  `link_id` int(11) NULL DEFAULT NULL,
  `link_sequence` int(11) NULL DEFAULT NULL,
  `next` varchar(255) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL,
  `optimal_speed` int(11) NOT NULL,
  `previous` varchar(255) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL,
  `roadclass` smallint(6) NOT NULL,
  `section_id` varchar(255) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL,
  `speed_limit` int(11) NOT NULL,
  `wkt` varchar(255) CHARACTER SET utf8 COLLATE utf8_general_ci NOT NULL,
  `organization_id` varchar(100) CHARACTER SET utf8 COLLATE utf8_general_ci NOT NULL,
  `speed` double NULL DEFAULT NULL,
  `speed_15` double NULL DEFAULT NULL,
  `speed_30` double NULL DEFAULT NULL,
  `speed_60` double NULL DEFAULT NULL,
  `speed_update_time` datetime(0) NULL DEFAULT NULL,
  `update_time_predicted` datetime(0) NULL DEFAULT NULL,
  PRIMARY KEY (`segment_id`, `organization_id`) USING BTREE,
  INDEX `FK_qqg6v62tc5vti3eeuf6mkwpkl`(`organization_id`) USING BTREE,
  CONSTRAINT `mun_segment_ibfk_1` FOREIGN KEY (`organization_id`) REFERENCES `tkm_fcd`.`municipality` (`organization_id`) ON DELETE CASCADE ON UPDATE CASCADE
) ENGINE = InnoDB CHARACTER SET = utf8 COLLATE = utf8_general_ci ROW_FORMAT = Compact;


CREATE TABLE `tkm_fcd`.`municipality`  (
  `organization_id` varchar(100) CHARACTER SET utf8 COLLATE utf8_general_ci NOT NULL,
  `basemap` varchar(10) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL,
  `city` varchar(30) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL,
  `favicon` varchar(20) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL,
  `img` varchar(20) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL,
  `latitude` decimal(20, 17) NULL DEFAULT NULL,
  `longitude` decimal(20, 17) NULL DEFAULT NULL,
  `mapserviceurl` varchar(255) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL,
  `mapsrc` varchar(255) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL,
  `maptype` varchar(10) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL,
  `munlink` varchar(100) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL,
  `name` varchar(50) CHARACTER SET utf8 COLLATE utf8_general_ci NOT NULL,
  `proxyurl` varchar(50) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL,
  `region` varchar(255) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL,
  PRIMARY KEY (`organization_id`) USING BTREE
) ENGINE = InnoDB CHARACTER SET = utf8 COLLATE = utf8_general_ci ROW_FORMAT = Compact;


---


INSERT INTO tkm_fcd.mun_segment (
    segment_id,
    lengthmm,
    roadclass,
    optimal_speed,
    speed_limit,
    wkt,
    organization_id
) SELECT
    SegmentId,
    Lengthmm,
    RoadClass,
    OptimalSpeedKph,
    SpeedLimitKph,
    WKT,
    '5ce13d549932f53389f36936'
FROM
    vieroc.FCD_ALL_HIGHWAYS_WEST ON DUPLICATE KEY UPDATE tkm_fcd.mun_segment.segment_id = tkm_fcd.mun_segment.segment_id;


INSERT INTO tkm_fcd.mun_segment (
    segment_id,
    lengthmm,
    roadclass,
    optimal_speed,
    speed_limit,
    wkt,
    organization_id
) SELECT
    SegmentId,
    Lengthmm,
    RoadClass,
    OptimalSpeedKph,
    SpeedLimitKph,
    WKT,
    '5ce13d609932f53389f36937'
FROM
    vieroc.FCD_ALL_HIGHWAYS_EAST ON DUPLICATE KEY UPDATE tkm_fcd.mun_segment.segment_id = tkm_fcd.mun_segment.segment_id;

```
