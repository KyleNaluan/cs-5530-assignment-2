# Part A - Single Sample - Glucose
Although the sample taken in this step was relatively small, the sample mean and max glucose weren't too far off from the population. Maybe I had just picked a lucky seed - I would expect the results to very greatly if I experimented with other seeds. The sample mean was relatively larger than population mean (130.32 vs 120.89), but the max glucose levels were very close (197 vs 199). The distributions were somewhat similar in shape, with the center of the sample distribution being shifted more to the right and a having a higher proportion of larger glucose values. I would expect the sample distribution to become closer in shape to the population as sample size increases.

# Part B - Single Sample - BMI
Once again, the sample statistic and the population statistic were very close. The sample 98th percentile of BMI was 49.324, while the population percentile was 47.526. The boxplot below shows that the sample 98th percentile is higher than that of the population, however the population distribution has a few outliers (above the sample distribution's 98th percentile and max), which do not significantly affect its percentiles.

<img src="..\visualizations\part_b_bmi_boxplot.png" width="50%" />

# Part C - Bootstrap
Quick Note:
* From my interpretation of the assignment instructions, the Bootstrap samples and observations were to be taken directly from the poulation.
* This differs from my understanding of the bootstrap, where the bootstrapping is done on a single original sample taken from the population.
* I wasn't sure which method we were expected to use, so I just followed my direct interpretation of the assignment.
* Due to this, we may be overestimating the performance of the bootstrap since repeated samples are taken directly from the population.
* However, I think using an original sample would provide similar results.
   * Examples in class have shown this to be true.

Direct comparison of the average bootstrap statistics and the true population statistics through the use of bar charts show that the bootstrap estimates were very close to the actual population statistics. 

<img src="..\visualizations\part_c_blood_pressure_barcharts.png" width="50%" />

The mean blood pressure is the most similar statistic, then the standard deviation, and the 98th percentile value is where they differ the most, although they are still close in value.

The bootstrap distributions provide even more information:

<img src="..\visualizations\part_c_bootstrap_distributions.png" width="50%" />

* Vertical lines were added to each bootstrap distribution, representing the avg of the bootstrap statistic and the actual population statistic. This allowed me to see where the population statistic lies in the bootstrap distribution and provided a direct comparision with the averaged bootstrap statistic.
* The distribution of the mean blood pressure and standard deviation have mostly normal curves. This tracks with the Central Limit Theorem as the number of bootstrap samples is moderately high. The spread of values around the means of those distributions is also fairly tight. I would expect it to become more narrow as the number of samples increases.
* The bootstrap distribution of 98th percentile values is very interesting. It doesn't follow a bell curve, but instead has a second, smaller peak. I'm not sure what caused this to happen, but it appears that there are two large groups of bootstrap samples that had their 98th percentile at different blood pressure values. The larger peak occurs between 95-97 and the secondary peak is at around 105. The interesting thing is that the average of the bootstrap's percentile is still very close to the population's percentile value. The bootstrap had an average 98th percentile of 98.19 and the population's 98th percentile was 99.32. They were still within 2 units of each other.
* The avg of the mean and the standard deviation were even closer. The bootstrap avg mean was only 0.06 higher than the population mean (69.16 vs 69.11). The bootstrap avg std had a slightly higher gap of 0.21 (19.15 vs 19.36). I would consider these very good estimates.
* The obtained bootstrap approximations were all very reasonable. Even for the worse performing bootstrap statistic estimate, the difference was less than 2 units from the population value.
* This shows that with a large number of samples (and sample size), the bootstrap can be very useful and reliable for estimating certain sample statistics.
   * I would still be cautious as samples were all taken from the population itself, though it has already been proven that the bootstrap works.
   * I am curious and will test how well a bootstrap performs on a single, original sample will perform in a separate space.
