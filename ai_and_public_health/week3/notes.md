# week content
- Week main task: designing and implementing your air quality mapping product

# First problem
- Missing data is a significant issue for the air pollution sensor network in Bogota
    - ![baseline_solution](images/baseline_solution.png)
- Solution idea:
    - Because in many cases, whether a missing values for one pollutant, there are still valid records for other pollutants
    - Some of the different pollutant levels appear to be correlated
    - The pollutant levels seem to depend on the time of day, day of week, and sensor station location.
    - Idea: There might be a role to play for AI in using the rest of the data to make somewhat accurate estimates of these missing values. 
- Simple solutions for filling missing data:
    - take last value: past measurement, same location
    - take nearest station: current measurement, different location
    - use nearest neighbor method with MAE

# Baseline usage
- At first stage, rather than taking a sort of AI first approach, it's always a good idea to spend some time experimenting with the simplest possible solution that you can imagine.
- Reasons to to that:
    - Reason 1: If a simple solution turns out to be good enough to meet your goals, you might want to stop there. Because by choosing a simple route, you might get your solution faster, maybe at a lower cost, and it might be easier to interpret the results.
    - Reason 2: If you move on to implementing a more complex model, then you will need to be able to quantify the relative performance improvements of your model relative to a simple baseline, such as this.
