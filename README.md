# i24_evaluation

Unsupervised metrics|Description
:---|:---
acceleration_score|Percentage of timestamps that the acceleration is legel (within +/-10ft/sec2) for each trajectory. 1=legal acceleration all the time, 0=illegal acceleration all the time
all_feasible_id|A list of IDs whose feasibility scores for (distance, acceleration, rotation, backwards and conflicts) are all 1s
any_infeasible_id|A list of IDs in a complementary set of all_feasible_ids.
backward_id|Trajectory IDs whose finite-difference of x is negative at any instance.
backward_score|Percentage of timestamps each car travels backward. 1=no backward travel, 0.8=20% of the time it travels backwards.
conflict_score|Percentage of timestamps each trajectory overlaps with another. 1=no overlaps, 0.8=20% of the time it overlaps with another one.
conflict_score|Percentage of distance traveled for each trajectory over the total distance covered by the entire collection. 1=travels the entire distance, 0.8=travels 80% of the distance.
duration|Length of the collection in sec.
feasibility_score|The product of acceleration_score, distance_score, backward_score, conflict_score, and rotation_score
id|A list of IDs with the same order as other lists
overlaps|(dict) key: a pair of ids that overlaps, val: the cumulated time (in sec) that they overlap
rotation_score|Percentage of timestamps that the rotation of the vehicle body is legel (within +/-30 degrees from the parallel lane lines) for each trajectory. 1=legal rotation all the time, 0=illegal acceleration all the time
theta|Rotation angle arctan(vy/vx)
collection|Name of collection to evaluate.
traj_count|Total number trajectory documents.
timestamp_count|Total number of unique timestamp (resampled at 25Hz).
x_traveled|xmax - xmin for each trajectory.
