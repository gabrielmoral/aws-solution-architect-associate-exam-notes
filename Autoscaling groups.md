#### Auto scaling groups

With an auto scaling group we can define rules to scale out/in based on metrics.

Options:

**Target tracking scaling -** Increase or decrease the current capacity of the group based on a target value  for a specific metric. This is similar to the way that your thermostat maintains the temperature of your home – you select a temperature and  the thermostat does the rest.

**Step scaling -** Increase or decrease the current capacity of the group based on a set of scaling adjustments, known as *step adjustments*, that vary based on the size of the alarm breach.

**Simple scaling -** Increase or decrease the current capacity of the group based on a single scaling adjustment.



The first thing we need to create an auto scaling group is a Launch Configuration.

It ensures that it does not launch or terminate any additional instances before the previous scaling activity takes effect.

The default cool down value is 300 seconds.

