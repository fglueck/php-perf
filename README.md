# perf
PHP performance comparing measuring class.

To generate a benchmark report:

    $p = new perf();
    $p->start();
    for($i=100000;$i;$i--) { -- checking performance of strrpos
        if(strrpos($string, ':'));
    }
    $p->stop('strrpos()');
    $p->report();


## ->start() 
init a new time measuring

## ->stap('label')
stop measuring and set label for it

## ->report()
generates the output

Output sample:


    100.0% 0.37274s str_contains()
    104.6% 0.38981s strpos(+pos)
    105.1% 0.39162s strrpos(+pos)
    108.7% 0.40509s strrpos()
    112.6% 0.41980s [x]===':'
    120.4% 0.44880s strpos()
    143.9% 0.53623s substr_compare()
    247.6% 0.92283s preg_match
