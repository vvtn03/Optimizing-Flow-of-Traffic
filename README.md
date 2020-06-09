# Optimizing-Flow-of-Traffic USing Vehicle Density

phase 1:Traffic Density Detection Using Color Detection algorithm
Phase 2:Implementing Slab Based Algorithm To Optimize The Flow of Traffic


SLAB BASED ALGORITHM

A Slab consists of a set of numbers with a lower and upper bound. Making
slabs and dividing the number of cars on the basis of slabs and allocating appropriate
time can be done to make the congested traffic flow more smoothly.
SLABS
Congestion_0 - 00-10 – Light Traffic (Blue) --> 20 seconds
Congestion_1 - 10-40 – Medium Traffic (Orange) --> 40 seconds
Congestion_2 - 40-60 – Heavy Traffic (Red) --> 60 seconds


Once the number of cars on each side of the intersection is calculated, slabs
can be used to allot timings to different sides with the maximum number of cars given
the priority of crossing the intersection, taking care of the above conditions so as to
keep the flow of traffic efficient, smooth and fair . Timers to the slabs are allotted so
as to make the maximum number of cars in that slab half, by letting half of the cars
pass the intersection, considering the contribution of a single car in a three-lane road
is 2 second.

As per our observation and by studying the data set that we have obtained over
a period of time, the average time taken by a vehicle to pass through an intersection
once the vehicle ahead of it passes through is generally 2 seconds. We use this metric
to approximate the total time duration for which the traffic signal should be “Green”
Optimizing the Flow of Traffic based on Vehicle Density
and when it should turn “Red”. We follow the same pattern in a Round Robin manner
so as to ensure every lane gets equal priority and there is no partiality in prioritizing
the lanes while allowing traffic to flow.
Through this method, we unsure that every lane gets its turn once before
moving to the next subsequent lanes. No lane is skipped or jumped regardless of the
presence of traffic in that lane or not in order to provide a small buffer for any incoming
traffic and to ensure that there are no accidents caused when vehicles are approaching
at high speeds.
The vehicle density obtained is tabulated and stored in a list which is then used
to manipulate the time required to clear the congestion. Considering a single car's
contribution on one side of the road is 2 seconds to cross the intersection, if the density
of cars is less, i.e. in the blue region, then the normal clockwise flow of the traffic is
maintained else the congested traffic algorithm comes in play and handles the
situation.

Example of Slab Division Algorithm
List = [10,20,30,40]
- Contains three elements of slab 1 and one of slab 2 initially
and will later change according to the values
- Variance-based algorithm calculates the time according to
the value of a single index.
Slab Division Algorithm results in a scenario which is comparatively lesser
dynamic than compared to the Variance Based Algorithm. This helps us assess the
scenario to a macro level which much greater detail and accordingly vary the flow of
traffic efficiently

