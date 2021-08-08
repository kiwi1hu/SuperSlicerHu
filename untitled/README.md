---
title: SuperSlicer változók listája
order: 8
---

# 0

Ezen az oldalon a SuperSlicer változók listáját találja, amelyek a G-kód egyéni beállításaiban használhatók.

Egyszerre több változót is használhat, például :

```text
M109 T[next_extruder] S[first_layer_temperature[next_extruder]]
```

valami olyasmit generálna, mint :

```text
M109 T1 S190
```

Ne feledje, hogy a SuperSlicer GUI-ban szereplő értékeket használja, és nem azokat, amelyeket a firmware elvár. Ez különösen igaz például azokra a sebességekre, amelyek a szeletelő interfészeken mm/s-ban vannak megadva, míg a G-kód fájlokban általában m/min-ben vannak megadva.

## Leghasznosabb változók

[bed\_temperature](variable_list/bed_temperature.md)

```text
M140 S[bed_temperature]
```

megjegyzés: Mindig az extruder\_0-ba töltött szál értékét veszi fel.

[current\_extruder](current_extruder.md)

```text
M104 S[first_layer_temperature[current_extruder]]
```

megjegyzés: ez nem fog működni az indító G-kódban, mert a \[current\_extruder\] hely az utoljára használt extruder számával van kitöltve, ami az indításkor még nincs beállítva, és véletlenszerű más, esetleg nyomtatandó alkatrészek számára.

[first\_layer\_temperature](first_layer_temperature.md)

```text
M104 S[first_layer_temperature_0] M104 S[first_layer_temperature[next_extruder]]
```

[first\_layer\_bed\_temperature](first_layer_bed_temperature.md)

```text
M140 S[first_layer_bed_temperature]
```

megjegyzés: Mindig az extruder\_0-ba töltött szál értékét veszi fel.

[layer\_num](layer_num.md)

```text
M117 printing layer [layer_num]
```

[layer\_z](layer_z.md)

```text
M117 printing layer [layer_num] at [layer_z]mm
```

[total\_layer\_count](total_layer_count.md)

```text
M117 printing layer {layer_num+1}/[total_layer_count]
```

[next\_extruder](next_extruder.md)

```text
M104 S[first_layer_temperature[next_extruder]]
```

Megjegyzés: ez csak az eszközváltás G-kódjában működik.

[previous\_extruder](previous_extruder.md)

```text
M104 S[first_layer_temperature[previous_extruder]]
```

Megjegyzés: ez csak az eszközváltás G-kódjában működik.

[temperature](temperature.md)

```text
M109 S[temperature_0] M109 S[temperature[previous_extruder]]
```

[extrusion\_role](extrusion_role.md)

## További változók a kimeneti fájlnév formátumban

* [print\_time](print_time.md)
* [normal\_print\_time](normal_print_time.md)
* [silent\_print\_time](silent_print_time.md)
* [used\_filament](used_filament.md)
* [extruded\_volume](extruded_volume.md)
* [total\_cost](total_cost.md)
* [total\_weight](total_weight.md)
* [total\_wipe\_tower\_cost](total_wipe_tower_cost.md)
* [total\_wipe\_tower\_filament](total_wipe_tower_filament.md)

## Kevésbé hasznos változók

* [printer\_technology](printer_technology.md)
* [layer\_height](layer_height.md)
* [initial\_layer\_height](initial_layer_height.md)
* [max\_print\_height](max_print_height.md)
* [preset\_name](preset_name.md)

## Nyomtatóágy

* [bed\_shape](bed_shape.md)
* [bed\_custom\_texture](bed_custom_texture.md)
* [bed\_custom\_Modell](bed_custom_model.md)
* [bed\_texture](bed_texture.md)
* [bed\_Módl](bed_Módl.md)

## Miniatűrök

* [thumbnails](thumbnails.md)
* [thumbnails\_color](thumbnails_color.md)
* [thumbnails\_color\_int](thumbnails_color_int.md)
* [thumbnails\_custom\_color](thumbnails_custom_color.md)
* [thumbnails\_with\_bed](thumbnails_with_bed.md)
* [thumbnails\_with\_support](thumbnails_with_support.md)

## Printhost

* [print\_host](print_host.md)
* [printhost\_apikey](printhost_apikey.md)
* [printhost\_port](printhost_port.md)
* [printhost\_cafile](printhost_cafile.md)
* [printhost\_user](printhost_user.md)
* [printhost\_password](printhost_password.md)
* [printhost\_authorization\_type](printhost_authorization_type.md)
* [allow\_empty\_layers](allow_empty_layers.md)
* [before\_layer\_gcode](before_layer_gcode.md)
* [between\_objects\_gcode](between_objects_gcode.md)
* [bottom\_solid\_layers](bottom_solid_layers.md)
* [bottom\_solid\_min\_thickness](bottom_solid_min_thickness.md)
* [bridge\_acceleration](bridge_acceleration.md)
* [bridge\_angle](bridge_angle.md)
* [bridge\_fan\_speed](bridge_fan_speed.md)

  `M106 S[bridge_fan_speed]`

Ez a ténylegesen beírt érték \(0-100\), nem pedig 0-255 .

* [top\_fan\_speed](top_fan_speed.md)
* [bridge\_flow\_ratio](bridge_flow_ratio.md)
* [over\_bridge\_flow\_ratio](over_bridge_flow_ratio.md)
* [bridge\_overlap](bridge_overlap.md)
* [bridge\_speed](bridge_speed.md)
* [bridge\_speed\_internal](bridge_speed_internal.md)
* [brim\_inside\_holes](brim_inside_holes.md)
* [brim\_width](brim_width.md)
* [brim\_width\_interior](brim_width_interior.md)
* [brim\_ears](brim_ears.md)
* [brim\_ears\_max\_angle](brim_ears_max_angle.md)
* [brim\_ears\_pattern](brim_ears_pattern.md)
* [brim\_offset](brim_offset.md)
* [chamber\_temperature](chamber_temperature.md)
* [clip\_multipart\_objects](clip_multipart_objects.md)
* [colorprint\_heights](colorprint_heights.md)
* [compatible\_printers](compatible_printers.md)
* [compatible\_printers\_condition](compatible_printers_condition.md)
* [compatible\_prints](compatible_prints.md)
* [compatible\_prints\_condition](compatible_prints_condition.md)
* [compatible\_printers\_condition\_cummulative](compatible_printers_condition_cummulative.md)
* [compatible\_prints\_condition\_cummulative](compatible_prints_condition_cummulative.md)
* [complete\_objects](complete_objects.md)
* [complete\_objects\_one\_skirt](complete_objects_one_skirt.md)
* [complete\_objects\_sort](complete_objects_sort.md)
* [cooling](cooling.md)
* [cooling\_tube\_retraction](cooling_tube_retraction.md)
* [cooling\_tube\_length](cooling_tube_length.md)
* [default\_acceleration](default_acceleration.md)
* [default\_filament\_profile](default_filament_profile.md)
* [default\_print\_profile](default_print_profile.md)
* [disable\_fan\_first\_layers](disable_fan_first_layers.md)
* [duplicate\_distance](duplicate_distance.md)
* [end\_gcode](end_gcode.md)
* [end\_filament\_gcode](end_filament_gcode.md)
* [ensure\_vertical\_shell\_thickness](ensure_vertical_shell_thickness.md)
* [top\_fill\_pattern](top_fill_pattern.md)
* [bottom\_fill\_pattern](bottom_fill_pattern.md)
* [solid\_fill\_pattern](solid_fill_pattern.md)
* [enforce\_full\_fill\_volume](enforce_full_fill_volume.md)
* [external\_infill\_margin](external_infill_margin.md)
* [bridged\_infill\_margin](bridged_infill_margin.md)
* [external\_perimeter\_extrusion\_width](external_perimeter_extrusion_width.md)
* [external\_perimeter\_cut\_corners](external_perimeter_cut_corners.md)
* [external\_perimeter\_fan\_speed](external_perimeter_fan_speed.md)
* [external\_perimeter\_overlap](external_perimeter_overlap.md)
* [perimeter\_overlap](perimeter_overlap.md)
* [perimeter\_bonding](perimeter_bonding.md)
* [external\_perimeter\_speed](external_perimeter_speed.md)
* [external\_perimeters\_first](external_perimeters_first.md)
* [external\_perimeters\_vase](external_perimeters_vase.md)
* [external\_perimeters\_nothole](external_perimeters_nothole.md)
* [external\_perimeters\_hole](external_perimeters_hole.md)
* [perimeter\_loop](perimeter_loop.md)
* [perimeter\_loop\_seam](perimeter_loop_seam.md)
* [extra\_perimeters](extra_perimeters.md)

## Kerület és héj

### Minőség

* [only\_one\_perimeter\_top](only_one_perimeter_top.md)
* [min\_width\_top\_surface](min_width_top_surface.md)
* [extra\_perimeters\_overhangs](extra_perimeters_overhangs.md)
* [extra\_perimeters\_odd\_layers](extra_perimeters_odd_layers.md)
* [avoid\_crossing\_perimeters](avoid_crossing_perimeters.md)
* [avoid\_crossing\_not\_first\_layer](avoid_crossing_not_first_layer.md)
* [avoid\_crossing\_perimeters\_max\_detours](avoid_crossing_perimeters_max_detours.md)
* [extruder](extruder.md)
* [extruder\_clearance\_height](extruder_clearance_height.md)
* [extruder\_clearance\_radius](extruder_clearance_radius.md)
* [extruder\_colour](extruder_colour.md)
* [extruder\_colour\_int](extruder_colour_int.md)
* [extruder\_offset](extruder_offset.md)
* [extruder\_temperature\_offset](extruder_temperature_offset.md)
* [extruder\_fan\_offset](extruder_fan_offset.md)
* [extrusion\_axis](extrusion_axis.md)
* [extrusion\_multiplier](extrusion_multiplier.md)
* [print\_extrusion\_multiplier](print_extrusion_multiplier.md)
* [extrusion\_width](extrusion_width.md)
* [fan\_always\_on](fan_always_on.md)
* [fan\_below\_layer\_time](fan_below_layer_time.md)
* [filament\_colour](filament_colour.md)
* [filament\_colour\_int](filament_colour_int.md)
* [filament\_notes](filament_notes.md)
* [filament\_max\_speed](filament_max_speed.md)
* [filament\_max\_volumetric\_speed](filament_max_volumetric_speed.md)
* [filament\_max\_wipe\_tower\_speed](filament_max_wipe_tower_speed.md)
* [filament\_loading\_speed](filament_loading_speed.md)
* [filament\_enable\_toolchange\_temp](filament_enable_toolchange_temp.md)
* [filament\_use\_fast\_skinnydip](filament_use_fast_skinnydip.md)
* [filament\_enable\_toolchange\_part\_fan](filament_enable_toolchange_part_fan.md)
* [filament\_toolchange\_part\_fan\_speed](filament_toolchange_part_fan_speed.md)
* [filament\_use\_skinnydip](filament_use_skinnydip.md)
* [filament\_melt\_zone\_pause](filament_melt_zone_pause.md)
* [filament\_cooling\_zone\_pause](filament_cooling_zone_pause.md)
* [filament\_dip\_insertion\_speed](filament_dip_insertion_speed.md)
* [filament\_dip\_extraction\_speed](filament_dip_extraction_speed.md)
* [filament\_toolchange\_temp](filament_toolchange_temp.md)
* [filament\_skinnydip\_distance](layefilament_skinnydip_distancer_height.md)
* [filament\_loading\_speed\_start](filament_loading_speed_start.md)
* [filament\_unloading\_speed](filament_unloading_speed.md)
* [filament\_unloading\_speed\_start](filament_unloading_speed_start.md)
* [filament\_toolchange\_delay](filament_toolchange_delay.md)
* [filament\_cooling\_moves](filament_cooling_moves.md)
* [filament\_cooling\_initial\_speed](filament_cooling_initial_speed.md)
* [filament\_minimal\_purge\_on\_wipe\_tower](filament_minimal_purge_on_wipe_tower.md)
* [filament\_cooling\_final\_speed](filament_cooling_final_speed.md)
* [filament\_load\_time](filament_load_time.md)
* [filament\_ramming\_parameters](filament_ramming_parameters.md)
* [filament\_unload\_time](filament_unload_time.md)
* [filament\_diameter](filament_diameter.md)
* [filament\_retract\_length](filament_retract_length.md)
* [filament\_retract\_lift](filament_retract_lift.md)
* [filament\_retract\_lift\_above](filament_retract_lift_above.md)
* [filament\_retract\_lift\_below](filament_retract_lift_below.md)
* [filament\_retract\_speed](filament_retract_speed.md)
* [filament\_deretract\_speed](filament_deretract_speed.md)
* [filament\_retract\_restart\_extra](filament_retract_restart_extra.md)
* [filament\_retract\_before\_travel](filament_retract_before_travel.md)
* [filament\_retract\_layer\_change](filament_retract_layer_change.md)
* [filament\_wipe](filament_wipe.md)
* [filament\_wipe\_extra\_perimeter](filament_wipe_extra_perimeter.md)
* [filament\_retract\_before\_wipe](filament_retract_before_wipe.md)
* [filament\_shrink](filament_shrink.md)
* [filament\_density](filament_density.md)
* [filament\_type](filament_type.md)
* [filament\_soluble](filament_soluble.md)
* [filament\_cost](filament_cost.md)
* [filament\_settings\_id](filament_settings_id.md)
* [filament\_vendor](filament_vendor.md)
* [fill\_angle](fill_angle.md)
* [fill\_angle\_increment](fill_angle_increment.md)
* [fill\_density](fill_density.md)
* [fill\_pattern](fill_pattern.md)
* [fill\_top\_flow\_ratio](fill_top_flow_ratio.md)
* [fill\_smooth\_width](fill_smooth_width.md)
* [fill\_smooth\_distribution](fill_smooth_distribution.md)
* [first\_layer\_flow\_ratio](first_layer_flow_ratio.md)
* [first\_layer\_size\_compensation](first_layer_size_compensation.md)
* [first\_layer\_acceleration](first_layer_acceleration.md)
* [first\_layer\_bed\_temperature](first_layer_bed_temperature.md)
* [first\_layer\_extrusion\_width](first_layer_extrusion_width.md)
* [first\_layer\_height](first_layer_height.md)
* [first\_layer\_speed](first_layer_speed.md)
* [first\_layer\_infill\_speed](first_layer_infill_speed.md)
* [first\_layer\_temperature](first_layer_temperature.md)
* [full\_fan\_speed\_layer](full_fan_speed_layer.md)
* [gap\_fill](gap_fill.md)
* [gap\_fill\_min\_area](gap_fill_min_area.md)
* [gap\_fill\_overlap](gap_fill_overlap.md)
* [gap\_fill\_speed](gap_fill_speed.md)
* [gcode\_comments](gcode_comments.md)
* [gcode\_flavor](gcode_flavor.md)
* [gcode\_label\_objects](gcode_label_objects.md)
* [high\_current\_on\_filament\_swap](high_current_on_filament_swap.md)
* [infill\_acceleration](infill_acceleration.md)
* [infill\_every\_layers](infill_every_layers.md)
* [infill\_dense](infill_dense.md)
* [infill\_connection](infill_connection.md)
* [infill\_dense\_algo](infill_dense_algo.md)
* [infill\_extruder](infill_extruder.md)
* [infill\_extrusion\_width](infill_extrusion_width.md)
* [infill\_first](infill_first.md)
* [infill\_only\_where\_needed](infill_only_where_needed.md)
* [infill\_overlap](infill_overlap.md)
* [infill\_speed](infill_speed.md)
* [inherits](inherits.md)
* [inherits\_cummulative](inherits_cummulative.md)
* [interface\_shells](interface_shells.md)
* [ironing](ironing.md)
* [ironing\_type](ironing_type.md)
* [ironing\_flowrate](ironing_flowrate.md)
* [ironing\_spacing](ironing_spacing.md)
* [ironing\_speed](ironing_speed.md)
* [layer\_gcode](layer_gcode.md)
* [feature\_gcode](feature_gcode.md)
* [exact\_last\_layer\_height](exact_last_layer_height.md)
* [remaining\_times](layerremaining_times_height.md)
* [silent\_Mód](silent_Mód.md)
* [fan\_speedup\_time](fan_speedup_time.md)
* [fan\_speedup\_overhangs](fan_speedup_overhangs.md)
* [fan\_kickstart](fan_kickstart.md)
* [machine\_limits\_usage](machine_limits_usage.md)
* [machine\_min\_extruding\_rate](machine_min_extruding_rate.md)
* [machine\_min\_travel\_rate](machine_min_travel_rate.md)
* [machine\_max\_acceleration\_extruding](machine_max_acceleration_extruding.md)
* [machine\_max\_acceleration\_retracting](machine_max_acceleration_retracting.md)
* [machine\_max\_acceleration\_travel](machine_max_acceleration_travel.md)
* [max\_print\_speed](max_print_speed.md)
* [max\_speed\_reduction](max_speed_reduction.md)
* [max\_volumetric\_speed](max_volumetric_speed.md)
* [max\_volumetric\_extrusion\_rate\_slope\_positive](max_volumetric_extrusion_rate_slope_positive.md)
* [max\_volumetric\_extrusion\_rate\_slope\_negative](max_volumetric_extrusion_rate_slope_negative.md)
* [min\_fan\_speed](min_fan_speed.md)

`M106 S[min_fan_speed]`

Ez a ténylegesen beírt érték \(0-100\), nem pedig 0-255 .

[max\_fan\_speed](max_fan_speed.md)

```text
M106 S[max_fan_speed]
```

Ez a ténylegesen beírt érték \(0-100\), nem pedig 0-255 .

* [min\_layer\_height](min_layer_height.md)
* [max\_layer\_height](max_layer_height.md)
* [min\_length](min_length.md)
* [min\_print\_speed](min_print_speed.md)
* [min\_skirt\_length](min_skirt_length.md)
* [notes](notes.md)
* [nozzle\_diameter](nozzle_diameter.md)
* [host\_type](host_type.md)
* [printhost\_apikey](printhost_apikey.md)
* [printhost\_cafile](printhost_cafile.md)
* [print\_host](print_host.md)
* [only\_retract\_when\_crossing\_perimeters](only_retract_when_crossing_perimeters.md)
* [ooze\_prevention](ooze_prevention.md)
* [output\_filename\_format](output_filename_format.md)
* [overhangs\_speed](overhangs_speed.md)
* [overhangs\_width\_speed](overhangs_width_speed.md)
* [overhangs\_width](overhangs_width.md)
* [overhangs\_reverse](overhangs_reverse.md)
* [overhangs\_reverse\_threshold](overhangs_reverse_threshold.md)
* [no\_perimeter\_unsupported\_algo](no_perimeter_unsupported_algo.md)
* [parking\_pos\_retraction](parking_pos_retraction.md)
* [extra\_loading\_move](extra_loading_move.md)
* [perimeter\_acceleration](perimeter_acceleration.md)
* [perimeter\_extruder](perimeter_extruder.md)
* [perimeter\_extrusion\_width](perimeter_extrusion_width.md)
* [perimeter\_speed](perimeter_speed.md)

`G1 F[perimeter_speed]`

Ez a kitöltött tényleges értéket \(mm/sec\) fogja mutatni, nem pedig a mm/perc értéket.

* [perimeters](perimeters.md)
* [post\_process](post_process.md)
* [printer\_Módl](printer_Módl.md)
* [printer\_notes](printer_notes.md)
* [printer\_vendor](printer_vendor.md)
* [printer\_variant](printer_variant.md)
* [print\_settings\_id](print_settings_id.md)

### Szeletelési pontosság

* [resolution](resolution.md)
* [Módl\_precision](Módl_precision.md)
* [slice\_closing\_radius](slice_closing_radius.md)

### Támaszok és tutajok

* [support\_material\_solid\_first\_layer](support_material_solid_first_layer.md)
* [raft\_layers](raft_layers.md)

### Támaszok és tutajok

* [retract\_before\_travel](retract_before_travel.md)
* [retract\_before\_wipe](retract_before_wipe.md)
* [retract\_layer\_change](retract_layer_change.md)
* [retract\_length](retract_length.md)
* [print\_retract\_length](print_retract_length.md)
* [retract\_length\_toolchange](retract_length_toolchange.md)
* [retract\_lift](retract_lift.md)
* [retract\_lift\_above](retract_lift_above.md)
* [retract\_lift\_below](retract_lift_below.md)
* [retract\_lift\_first\_layer](retract_lift_first_layer.md)
* [retract\_lift\_top](retract_lift_top.md)
* [retract\_restart\_extra](retract_restart_extra.md)
* [retract\_restart\_extra\_toolchange](retract_restart_extra_toolchange.md)
* [retract\_speed](retract_speed.md)
* [deretract\_speed](deretract_speed.md)
* [seam\_position](seam_position.md)
* [seam\_angle\_cost](seam_angle_cost.md)
* [seam\_travel\_cost](seam_travel_cost.md)
* [seam\_preferred\_direction](seam_preferred_direction.md)
* [seam\_preferred\_direction\_jitter](seam_preferred_direction_jitter.md)
* [skirts](skirts.md)
* [skirt\_distance](skirt_distance.md)
* [skirt\_height](skirt_height.md)
* [skirt\_extrusion\_width](skirt_extrusion_width.md)
* [draft\_shield](draft_shield.md)
* [slowdown\_below\_layer\_time](slowdown_below_layer_time.md)
* [small\_perimeter\_speed](small_perimeter_speed.md)
* [small\_perimeter\_min\_length](small_perimeter_min_length.md)
* [small\_perimeter\_max\_length](small_perimeter_max_length.md)

### Rétegek módosítása

* [curve\_smoothing\_angle\_convex](curve_smoothing_angle_convex.md)
* [curve\_smoothing\_angle\_concave](curve_smoothing_angle_concave.md)
* [curve\_smoothing\_precision](curve_smoothing_precision.md)
* [curve\_smoothing\_cutoff\_dist](curve_smoothing_cutoff_dist.md)
* [solid\_infill\_below\_area](solid_infill_below_area.md)
* [solid\_infill\_extruder](solid_infill_extruder.md)
* [solid\_infill\_every\_layers](solid_infill_every_layers.md)
* [solid\_infill\_extrusion\_width](solid_infill_extrusion_width.md)
* [solid\_infill\_speed](solid_infill_speed.md)
* [solid\_layers](solid_layers.md)
* [solid\_min\_thickness](solid_min_thickness.md)
* [spiral\_vase](spiral_vase.md)
* [standby\_temperature\_delta](standby_temperature_delta.md)
* [start\_gcode](start_gcode.md)
* [start\_filament\_gcode](start_filament_gcode.md)
* [color\_change\_gcode](color_change_gcode.md)
* [pause\_print\_gcode](pause_print_gcode.md)
* [template\_custom\_gcode](template_custom_gcode.md)
* [single\_extruder\_multi\_material](single_extruder_multi_material.md)
* [single\_extruder\_multi\_material\_priming](single_extruder_multi_material_priming.md)
* [wipe\_tower\_no\_sparse\_layers](wipe_tower_no_sparse_layers.md)
* [support\_material](support_material.md)
* [support\_material\_auto](support_material_auto.md)
* [support\_material\_xy\_spacing](support_material_xy_spacing.md)
* [support\_material\_angle](support_material_angle.md)
* [support\_material\_buildplate\_only](support_material_buildplate_only.md)
* [support\_material\_contact\_distance\_type](support_material_contact_distance_type.md)
* [support\_material\_contact\_distance\_top](support_material_contact_distance_top.md)
* [support\_material\_contact\_distance\_bottom](support_material_contact_distance_bottom.md)
* [support\_material\_enforce\_layers](support_material_enforce_layers.md)
* [support\_material\_extruder](support_material_extruder.md)
* [support\_material\_extrusion\_width](support_material_extrusion_width.md)
* [support\_material\_interface\_contact\_loops](support_material_interface_contact_loops.md)
* [support\_material\_interface\_extruder](support_material_interface_extruder.md)
* [support\_material\_interface\_layers](support_material_interface_layers.md)
* [support\_material\_interface\_spacing](support_material_interface_spacing.md)
* [support\_material\_interface\_speed](support_material_interface_speed.md) 
* [support\_material\_pattern](support_material_pattern.md) 
* [support\_material\_interface\_pattern](support_material_interface_pattern.md)
* [support\_material\_spacing](support_material_spacing.md)
* [support\_material\_speed](support_material_speed.md)
* [support\_material\_synchronize\_layers](support_material_synchronize_layers.md)
* [support\_material\_threshold](support_material_threshold.md)
* [support\_material\_with\_sheath](support_material_with_sheath.md)
* [dont\_support\_bridges](dont_support_bridges.md)
* [temperature](temperature.md)
* [print\_temperature](print_temperature.md)
* [print\_retract\_lift](layeprint_retract_liftr_height.md)
* [thin\_perimeters](thin_perimeters.md)
* [thin\_perimeters\_all](thin_perimeters_all.md)
* [thin\_walls](thin_walls.md) 
* [thin\_walls\_min\_width](thin_walls_min_width.md) 
* [thin\_walls\_overlap](thin_walls_overlap.md)
* [thin\_walls\_merge](thin_walls_merge.md) 
* [thin\_walls\_speed](thin_walls_speed.md) 
* [threads](threads.md)
* [time\_estimation\_compensation](time_estimation_compensation.md)
* [toolchange\_gcode](toolchange_gcode.md)
* [tool\_name](tool_name.md)
* [top\_infill\_extrusion\_width](top_infill_extrusion_width.md)
* [top\_solid\_infill\_speed](top_solid_infill_speed.md)
* [top\_solid\_layers](top_solid_layers.md)
* [top\_solid\_min\_thickness](top_solid_min_thickness.md) 
* [travel\_speed](travel_speed.md) 
* [use\_firmware\_retraction](use_firmware_retraction.md)
* [use\_relative\_e\_distances](use_relative_e_distances.md)
* [use\_volumetric\_e](use_volumetric_e.md)
* [variable\_layer\_height](variable_layer_height.md)

### Tisztítótorony

* [wipe](wipe.md)
* [wipe\_tower](wipe_tower.md)
* [wiping\_volumes\_extruders](wiping_volumes_extruders.md)
* [wiping\_volumes\_matrix](wiping_volumes_matrix.md)
* [wipe\_advanced](wipe_advanced.md)
* [wipe\_advanced\_nozzle\_melted\_volume](wipe_advanced_nozzle_melted_volume.md)
* [filament\_wipe\_advanced\_pigment](filament_wipe_advanced_pigment.md)
* [wipe\_advanced\_multiplier](wipe_advanced_multiplier.md)
* [wipe\_advanced\_algo](wipe_advanced_algo.md)
* [wipe\_tower\_brim](wipe_tower_brim.md)
* [wipe\_tower\_x](wipe_tower_x.md)
* [wipe\_tower\_y](wipe_tower_y.md)
* [wipe\_tower\_width](wipe_tower_width.md)
* [wipe\_tower\_rotation\_angle](wipe_tower_rotation_angle.md)
* [wipe\_into\_infill](wipe_into_infill.md)
* [wipe\_into\_objects](wipe_into_objects.md)
* [wipe\_extra\_perimeter](wipe_extra_perimeter.md)
* [wipe\_tower\_bridging](wipe_tower_bridging.md)

### Méretkompenzáció

* [xy\_size\_compensation](xy_size_compensation.md)
* [xy\_inner\_size\_compensation](xy_inner_size_compensation.md)
* [hole\_size\_compensation](hole_size_compensation.md)
* [hole\_size\_threshold](hole_size_threshold.md)
* [hole\_to\_polyhole](hole_to_polyhole.md)
* [z\_offset](z_offset.md)
* [z\_step](z_step.md)

### Marás

* [milling\_cutter](milling_cutter.md)
* [milling\_diameter](milling_diameter.md)
* [milling\_offset](milling_offset.md)
* [milling\_z\_offset](milling_z_offset.md)
* [milling\_z\_lift](milling_z_lift.md)
* [milling\_toolchange\_start\_gcode](milling_toolchange_start_gcode.md)
* [milling\_toolchange\_end\_gcode](milling_toolchange_end_gcode.md)
* [milling\_post\_process](milling_post_process.md)
* [milling\_extra\_size](milling_extra_size.md)
* [milling\_after\_z](milling_after_z.md)
* [milling\_speed](milling_speed.md)
* [display\_width](display_width.md)
* [display\_height](display_height.md)
* [display\_pixels\_x](display_pixels_x.md)
* [display\_pixels\_y](display_pixels_y.md)
* [display\_mirror\_x](display_mirror_x.md)
* [display\_mirror\_y](display_mirror_y.md)
* [display\_orientation](display_orientation.md)
* [fast\_tilt\_time](fast_tilt_time.md)
* [slow\_tilt\_time](slow_tilt_time.md)
* [area\_fill](area_fill.md)
* [relative\_correction](relative_correction.md)
* [absolute\_correction](absolute_correction.md)
* [elephant\_foot\_min\_width](elephant_foot_min_width.md)

### SLA paraméterek

* [gamma\_correction](gamma_correction.md)
* [material\_type](material_type.md)
* [bottle\_volume](bottle_volume.md)
* [bottle\_weight](bottle_weight.md)
* [material\_density](material_density.md)
* [bottle\_cost](bottle_cost.md)
* [faded\_layers](faded_layers.md)
* [min\_exposure\_time](min_exposure_time.md)
* [max\_exposure\_time](max_exposure_time.md)
* [exposure\_time](exposure_time.md)
* [initial\_exposure\_time](initial_exposure_time.md)
* [min\_initial\_exposure\_time](min_initial_exposure_time.md)
* [max\_initial\_exposure\_time](max_initial_exposure_time.md)
* [material\_correction](material_correction.md)
* [material\_notes](material_notes.md)
* [material\_vendor](material_vendor.md)
* [default\_sla\_material\_profile](default_sla_material_profile.md)
* [sla\_material\_settings\_id](sla_material_settings_id.md)
* [default\_sla\_print\_profile](default_sla_print_profile.md)
* [sla\_print\_settings\_id](sla_print_settings_id.md)

### SLA támaszték és bázis

* [supports\_enable](supports_enable.md)
* [support\_head\_front\_diameter](support_head_front_diameter.md)
* [support\_head\_penetration](support_head_penetration.md)
* [support\_head\_width](support_head_width.md)
* [support\_pillar\_diameter](layer_height.md)
* [support\_small\_pillar\_diameter\_percent](support_small_pillar_diameter_percent.md)
* [support\_max\_bridges\_on\_pillar](support_max_bridges_on_pillar.md)
* [support\_pillar\_connection\_Mód](support_pillar_connection_Mód.md)
* [support\_buildplate\_only](support_buildplate_only.md)
* [support\_pillar\_widening\_factor](support_pillar_widening_factor.md)
* [support\_base\_diameter](support_base_diameter.md)
* [support\_base\_height](support_base_height.md)
* [support\_base\_safety\_distance](support_base_safety_distance.md)
* [support\_critical\_angle](support_critical_angle.md)
* [support\_max\_bridge\_length](support_max_bridge_length.md)
* [support\_max\_pillar\_link\_distance](support_max_pillar_link_distance.md)
* [support\_object\_elevation](support_object_elevation.md)
* [support\_points\_density\_relative](support_points_density_relative.md)
* [support\_points\_minimal\_distance](support_points_minimal_distance.md)
* [pad\_enable](pad_enable.md)
* [pad\_wall\_thickness](pad_wall_thickness.md)
* [pad\_wall\_height](pad_wall_height.md)
* [pad\_brim\_size](pad_brim_size.md)
* [pad\_max\_merge\_distance](pad_max_merge_distance.md)
* [pad\_wall\_slope](pad_wall_slope.md)
* [pad\_around\_object](pad_around_object.md)
* [pad\_around\_object\_everywhere](pad_around_object_everywhere.md)
* [pad\_object\_gap](pad_object_gap.md)
* [pad\_object\_connector\_stride](pad_object_connector_stride.md)
* [pad\_object\_connector\_width](pad_object_connector_width.md)
* [pad\_object\_connector\_penetration](pad_object_connector_penetration.md)

### Természetesen SLA

* [hollowing\_enable](hollowing_enable.md)
* [hollowing\_min\_thickness](hollowing_min_thickness.md)
* [hollowing\_quality](hollowing_quality.md)
* [hollowing\_closing\_distance](hollowing_closing_distance.md)

### Változó nem hozzáférhető

[export\_obj](export_obj.md) [export\_svg](export_svg.md) [export\_sla](export_sla.md) [export\_3mf](export_3mf.md) [export\_amf](export_amf.md) [export\_stl](export_stl.md) [export\_gcode](export_gcode.md) [gcodeviewer](laygcodeviewerer_height.md) [slice](slice.md) [help](help.md) [help\_fff](help_fff.md) [help\_sla](help_sla.md) [info](info.md) [save](save.md) [align\_xy](align_xy.md) [cut](cut.md) [cut\_grid](cut_grid.md) [cut\_x](cut_x.md) [cut\_y](cut_y.md) [center](center.md) [dont\_arrange](dont_arrange.md) [duplicate](duplicate.md) [duplicate\_grid](duplicate_grid.md) [merge](merge.md) [repair](repair.md) [rotate](rotate.md) [rotate\_x](rotate_x.md) [rotate\_y](rotate_y.md) [scale](scale.md) [split](split.md) [scale\_to\_fit](scale_to_fit.md) [ignore\_nonexistent\_config](ignore_nonexistent_config.md) [load](load.md) [output](output.md) [single\_instance](single_instance.md) [autosave](autosave.md) [datadir](datadir.md) [loglevel](loglevel.md) [sw\_renderer](sw_renderer.md)

