### DATA MINING-Transmission Problems

**Siyu Lu**

#### Abstract


#### Rationale

* **Raw materials are the starting point of production**: Without timely ordering and transportation of raw materials, the production line cannot operate, and the company will face the risk of suspension of production, breach of contract, and even customer loss
* **Raw material shortage directly affects capacity utilization**: Once the supply is not timely, the capacity cannot be fully utilized, affecting the company's revenue and competitiveness.
* **Ordering decisions affect procurement costs**: Choosing the wrong supplier and unbalanced ordering plans can easily lead to high-priced purchases or inventory backlogs, which directly eat up profits.
* **Transportation involves losses and costs**: The loss rate and capacity differences of different forwarders determine the actual arrival volume and transportation costs, which cannot be ignored.
* **The procurement prices of the three types of materials are different** (A is 20% higher than C, and B is 10% higher than C), and the material structure also determines the cost structure.

#### Research Question

1. Conduct a quantitative analysis of the supply characteristics of 402 suppliers, establish a mathematical model reflecting the importance of ensuring enterprise production, and on this basis, determine 50 of the most important suppliers and list the results in the paper.
2. Reference question 1: How many suppliers should the enterprise select at least to supply raw materials in order to meet the production requirements? For these suppliers, formulate the most economical raw material ordering plan for the enterprise every week for the next 24 weeks, and accordingly develop the transfer plan with the least loss. Try to analyze the implementation effects of the ordering plan and the transfer plan.
3. How can we build a forecasting model based on historical data to predict the weekly supply of raw materials for the next 24 weeks, so as to help companies make more accurate ordering and transshipment plans in advance?

#### Data Sources

1. Appendix 1 Data of 402 suppliers in the past five years
2. Appendix 2 Data of 8 forwarders in the past 5 years

#### Methodology

1. TOPSIS（Technique for Order Preference by Similarity to Ideal Solution）
2. ARIMA(time feature)
3. greedy algorithm

#### Results

1. The top 50 most important suppliers were obtained and Top_50_Suppliers was generated. It was found that the selection of the top 50 paid more attention to the stability of supply. Large supply is not necessarily more important than small supply.
2. The company should select at least 167 suppliers to supply raw materials to meet production needs. For these suppliers, the company formulates the most economical raw material ordering plan for the next 24 weeks, and formulates a transshipment plan with the least loss based on this. The original calculation, Linear Programming, and Random Forest are used to generate documents on the transshipment plan: 24_week_order_plan.xlsx, 24_week_forwarder_plan.xlsx, 24_week_forwarder_plan_LP.xlsx, 24_week_forwarder_plan_ML_with_limit.xlsx
3. The future trend of S005 was predicted with MAE: 9.07 and RMSE: 12.23.

#### Next steps

1. **Validation and Testing**

- **Data Validation**: Ensure that the data used for the analysis is accurate and up-to-date. Verify the correctness of the supply and demand data.
- **Model Testing**: Test the model with different scenarios to ensure robustness. For example, vary the weekly demand or the supply capacity to see how the model performs under different conditions.

2. **Optimization and Improvement**

- **Algorithm Optimization**: Explore more sophisticated optimization algorithms for supplier and forwarder selection. For example, consider using linear programming or other optimization techniques to minimize costs or maximize efficiency.
- **Capacity Management**: Implement a more dynamic capacity management system that can handle real-time changes in supply and demand.

3. **Integration and Automation**

- **System Integration**: Integrate the model into the existing supply chain management system to automate the planning process.
- **Dashboard Development**: Develop a dashboard to visualize the supply chain planning results, including order plans and forwarder assignments.

4. **Cost Analysis**

- **Cost-Benefit Analysis**: Conduct a detailed cost-benefit analysis to evaluate the financial impact of the proposed supply chain plan.
- **Sensitivity Analysis**: Perform sensitivity analysis to understand how changes in key parameters (e.g., demand, supply capacity, forwarder costs) affect the overall plan.

5. **Feedback Loop**

- **Stakeholder Feedback**: Gather feedback from stakeholders (e.g., suppliers, forwarders, procurement team) to identify areas for improvement.
- **Continuous Improvement**: Establish a feedback loop to continuously refine the model based on real-world performance and feedback.

#### Conclusion

**Positive Results**

- **Efficient Allocation**: The model successfully allocates orders and forwarders based on supply capacity and demand, ensuring efficient use of resources.
- **Optimized Supply Chain**: The approach helps in optimizing the supply chain by selecting the best suppliers and forwarders, potentially reducing costs and improving delivery times.
- **Data-Driven Decisions**: The model provides a data-driven approach to supply chain planning, reducing the reliance on manual decision-making.

**Negative Results**

- **Capacity Constraints**: There may be instances where the supply or forwarder capacity is insufficient to meet demand, leading to potential bottlenecks.
- **Data Quality Issues**: Inaccurate or incomplete data can lead to suboptimal planning results.
- **Complexity**: The model's complexity may require significant computational resources and expertise to implement and maintain.

**Recommendations**

- **Data Quality**: Ensure high-quality data to improve the accuracy of the model.
- **Scalability**: Consider scalability when integrating the model into the existing system to handle larger datasets and more complex scenarios.
- **Flexibility**: Build flexibility into the model to adapt to changing supply chain conditions, such as sudden changes in demand or supply disruptions.

#### Caveats/Cautions

- **Real-World Constraints**: Be aware of real-world constraints that may not be captured in the model, such as supplier reliability, forwarder availability, and geopolitical factors.
- **Model Limitations**: Understand the limitations of the model and be prepared to make manual adjustments when necessary.
- **Stakeholder Engagement**: Engage with all stakeholders to ensure buy-in and to gather valuable insights that can improve the model.
