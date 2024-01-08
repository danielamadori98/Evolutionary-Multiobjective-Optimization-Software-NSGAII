# Evolutionary Multiobjective Optimization Software NSGAII


plot "output_zdt1_P100_M033/hyperstats.out" u ($1*2.5):2 w lp, "output_zdt1_P040_M033/hyperstats.out" u 1:2 w lp, "output_zdt1_P200_M033/hyperstats.out" u ($1*5):2 w lp

./nsga2r 0.92 < input_ztd4/P040_M005.in && mv *.out output_zdt4/P040_M005/
plot "P100_M010/hyperstats.out" u ($1*2.5):2 w lp, "P040_M010/hyperstats.out" u 1:2 w lp, "P200_M010/hyperstats.out" u ($1*5):2 w lp
