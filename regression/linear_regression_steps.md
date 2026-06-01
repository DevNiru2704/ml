# 1. Enable Data Analysis ToolPak

1. Open **Excel**.
2. Click **File → Options**.
3. Select **Add-ins**.
4. At the bottom, in **Manage**, select **Excel Add-ins** and click **Go**.
5. Check **Analysis ToolPak**.
6. Click **OK**.
7. A **Data Analysis** button should now appear in the **Data** tab.

---

# 2. Perform Linear Regression

1. Arrange your data:
   - Independent Variable (**X**) in one column (e.g., YearsExperience).
   - Dependent Variable (**Y**) in another column (e.g., Salary).

2. Go to **Data → Data Analysis**.

3. Select **Regression** and click **OK**.

4. Fill in:
   - **Input Y Range** → Select the dependent variable column (Salary).
   - **Input X Range** → Select the independent variable column (YearsExperience).
   - Check **Labels** if column headers are included.
   - Choose an **Output Range** or **New Worksheet Ply**.

5. Click **OK**.

Excel will generate the regression output.

---

# 3. Highlight the P-Value

Highlight all **P-values less than 0.05**.

- **P-value < 0.05** → Significant relationship.
- **P-value ≥ 0.05** → Not statistically significant.

# 4. Write the Regression Equation

1. Locate the **Coefficients** table in the regression output.
2. Note the values of:
   - **Intercept**
   - **X Variable 1** (coefficient of the independent variable)
3. Now write the equation