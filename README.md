#README.md

An insanely simple color generating tool for `Python`, because `matplotlib` is awesome, but not worth importing the elephant, and `colour`'s functionality is terrific, but for some ungodly reason adds colors to its gradients.

##Installation

There's no install, so you're going to have to either:
1. Throw it into your `$PYTHONPATH` via `~/.bash_profile` or
2. Hack it into one of your `.pth` files (if you're not sure how to do this, email me)

##Usage

###Quick RBG to hex (and vice versa)

    import color_gen
    import numpy
    import pandas
    
    #make some random rgb colors
    rgb = pandas.DataFrame(numpy.random.random_integers(low = 0, high = 255, size = (100, 3)), 							columns = ['r', 'g', 'b'])
    hex_colors = color_gen.RGB_to_hex(rgb)
    
    
###Make a two stop gradient

	two_stop = color_gen.linear_gradient(start_hex = '#7ecba2', finish_hex = '#d0ef37', n = 20)
	
###make a three stop with white in the middle

    three_stop = color_gen.three_stop_gradient(start_hex = '#7ecba2', finish_hex = '#d0ef37', 
    											n = 20)
	
    
