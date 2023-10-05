## Project description: "Evaluating the results of AB testing and verifying the correctness of its implementation."
My task is to evaluate the results of the A/B test. I have a dataset with user actions, technical specifications and several auxiliary datasets. It is necessary to evaluate the correctness of the test and analyze its results.

## General conclusion
### As a result of the analysis of the test, the following conclusions can be drawn:

- Conducting the test during the holidays was an incorrect choice, since during this period user behavior may differ significantly from usual.
- Conducting two tests simultaneously and the overlap of users between groups makes it impossible to assess the impact of tests on each other and obtain clear results.
- Promotions carried out during the test could distort the results, as they affect user behavior.
- Uneven sampling, a significantly smaller size of test group B compared to control group A, creates an imbalance and may affect the test results.
- After filtering the dataset in accordance with the technical specifications, the total number of active users becomes less than the requirements of the technical specifications. In this regard, it was decided not to carry out filtering, so as not to reduce the power of the test.


### Based on the above findings, it is recommended:

- Review the test period and select a more representative period that excludes factors that may distort the results.
- Carry out tests separately to eliminate mutual influence between them and get clearer results.
- Eliminate promotions during the test to reduce distortion of results and get a clearer picture.
- Ensure uniform selection of samples to eliminate imbalance between the test and control groups.
- Pay attention to user activity in the test and increase efforts to attract active participants to obtain more reliable results.
- In general, given the identified problems and shortcomings in the test, the results obtained cannot be used as a basis for decision-making. It is necessary to re-test, eliminating the identified problems, in order to obtain reliable and adequate results for decision-making.
