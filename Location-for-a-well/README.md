# Description of the project

*Let's say you work for the mining company GlavRosGosNeft. We need to decide where to drill a new well.
I was provided with oil samples in three regions: in each of 10,000 fields, where they measured the quality of oil and the volume of its reserves. Build a machine learning model to help determine the region where mining will bring the most profit. It is necessary to analyze the possible profit and risks using the Bootstrap* technique

*Steps for choosing a location:*
-
- In the selected region, they are looking for deposits, for each, the values of the signs are determined;
- Build a model and estimate the volume of reserves;
- Select the deposits with the highest value estimates. The number of fields depends on the company's budget and the cost of developing one well;
- The profit is equal to the total profit of the selected deposits.


1. Loading and preparing data
2. Train and validate the model for each region:
    - Splitting the data into training and validation samples in the ratio of 75:25.
    - Model training and predictions on the validation set.
    - Saving the prediction and correct answers on the validation set.
    - Print on the screen the average stock of the predicted raw material and the RMSE of the model.
    - Analyze results.
3. Preparation for profit calculation:
    - Save all key values for calculations in separate variables.
    - Calculate sufficient volume of raw materials for break-even development of a new well. Comparison of the received volume of raw materials with the average stock in each region.
    - Conclusions on the stage of preparation of the profit calculation.
4. Function for calculating profit for selected wells and model predictions:
    - Select wells with maximum prediction values.
    - Sum the target value of the volume of raw materials corresponding to these predictions.
    - Calculate the profit for the received volume of raw materials.
5. Calculate the risks and profits for each region:
    - Apply the Bootstrap technique with 1000 samples to find the profit distribution.
    - Find the average profit, 95% confidence interval and risk of loss. Loss is negative profit.
    - Write conclusions: Region for well development.

- `id` — unique identifier of the well;
- `f0`, `f1`, `f2` - three signs of dots (it doesn't matter what they mean, but the signs themselves are significant);
- `product` — volume of reserves in the well (thousand barrels).

***Conditions of the problem:***
- Only linear regression is suitable for training the model (the rest are not predictable enough).
- When exploring the region, 500 points are explored, from which, using machine learning, the best 200 are selected for development.
- The budget for the development of wells in the region is 10 billion rubles.
- At current prices, one barrel of raw materials brings 450 rubles of income. The income from each unit of the product is 450 thousand rubles, since the volume is indicated in thousands of barrels.
- After assessing the risks, you need to leave only those regions in which the probability of losses is less than 2.5%. Among them, choose the region with the highest average profit.
- Synthetic data: details of contracts and characteristics of deposits were not disclosed.
