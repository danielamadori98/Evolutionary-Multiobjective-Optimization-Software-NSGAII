# Commands
./nsga2r 0.92 input_ztd4/P040_M005.in && mv *.out output_zdt4/P040_M005/
./nsga2r 0.92 < input_ztd4/P040_M005.in && mv *.out output_zdt4/P040_M005/
./nsga2r 0.92 < input_ztd4/P040_M015.in && mv *.out output_zdt4/P040_M015/
./nsga2r 0.92 < input_ztd4/P040_M010.in && mv *.out output_zdt4/P040_M010/
./nsga2r 0.92 < input_ztd4/P100_M010.in && mv *.out output_zdt4/P100_M010/
./nsga2r 0.92 < input_ztd4/P100_M015.in && mv *.out output_zdt4/P100_M015/
./nsga2r 0.92 < input_ztd4/P100_M005.in && mv *.out output_zdt4/P100_M005/
./nsga2r 0.92 < input_ztd4/P200_M005.in && mv *.out output_zdt4/P200_M005/
./nsga2r 0.92 < input_ztd4/P200_M015.in && mv *.out output_zdt4/P200_M015/
./nsga2r 0.92 < input_ztd4/P200_M010.in && mv *.out output_zdt4/P200_M010/
# Same population different mutation rate
plot "P040_M005/hyperstats.out" u 1:2 w lp, "P040_M010/hyperstats.out" u 1:2 w lp, "P040_M015/hyperstats.out" u 1:2 w lp
plot "P100_M005/hyperstats.out" u 1:2 w lp, "P100_M010/hyperstats.out" u 1:2 w lp, "P100_M015/hyperstats.out" u 1:2 w lp
plot "P200_M005/hyperstats.out" u 1:2 w lp, "P200_M010/hyperstats.out" u 1:2 w lp, "P200_M015/hyperstats.out" u 1:2 w lp

Result:
-P040: M010
-P100: M005
-P200: M005

# Different population (rescaling number of evaluation)
plot "P100_M005/hyperstats.out" u ($1*2.5):2 w lp, "P040_M010/hyperstats.out" u 1:2 w lp, "P200_M005/hyperstats.out" u ($1*5):2 w lp

Result:
-P040: M010

plot "P040_M005/hyperstats.out" u 1:2 w lp