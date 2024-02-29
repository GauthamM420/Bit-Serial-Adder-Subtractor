transcript on
if {[file exists gate_work]} {
	vdel -lib gate_work -all
}
vlib gate_work
vmap work gate_work

vlog -vlog01compat -work work +incdir+. {BSAS_6_1200mv_85c_slow.vo}

vlog -vlog01compat -work work +incdir+C:/Users/Gautham/Desktop/EEE120/Labs/BSAS5B_student-25Jul2022_restored {C:/Users/Gautham/Desktop/EEE120/Labs/BSAS5B_student-25Jul2022_restored/BSAS5B_test.v}

vsim -t 1ps +transport_int_delays +transport_path_delays -L altera_ver -L cycloneive_ver -L gate_work -L work -voptargs="+acc"  test

add wave *
view structure
view signals
run -all
