# Procedure

## Step 1: Load the Dataset

1. Open the Excel workbook containing the three modalities:
   - Touchpad
   - Leap Motion
   - Eye Gaze

2. Store the original data in the sheet named **original_dataset**.

---

## Step 2: Outlier Detection and Removal

1. Sort the values of each modality in descending order.

2. Create a table containing:
   - Mean
   - Standard Deviation
   - First Quartile (Q1)
   - Third Quartile (Q3)
   - Outlier Threshold

3. Calculate the mean using:

   ```excel
   =AVERAGE(range)
   ```

4. Calculate the standard deviation using:

   ```excel
   =STDEV(range)
   ```

5. Calculate the first quartile (Q1):

   ```excel
   =QUARTILE(range,1)
   ```

6. Calculate the third quartile (Q3):

   ```excel
   =QUARTILE(range,3)
   ```

7. Calculate the outlier threshold using:

   ```excel
   =Q3 + 3*(Q3-Q1)
   ```

8. Highlight all values greater than or equal to the outlier threshold.

9. Remove the identified outliers and store the cleaned dataset in the **outliers** sheet.

---

## Step 3: Mean Analysis

1. Copy the cleaned dataset to the **mean_analysis** sheet.

2. Create a table containing only:
   - Mean
   - Standard Deviation

3. Calculate the mean and standard deviation for all three modalities.

4. Insert a bar chart:
   - Select the mean values.
   - Go to **Insert → Recommended Charts → Bar Chart**.

5. Add:
   - Chart Title
   - X-axis Label
   - Y-axis Label

6. Add error bars:
   - Select the bars.
   - Click **Chart Elements (+)**.
   - Select **Error Bars → More Options**.
   - Choose **Custom**.
   - Specify the Standard Deviation values as the error amounts.

7. Compare the average task completion times of the three modalities using the graph.

---

## Step 4: One-Way ANOVA

1. Copy the cleaned dataset to the **anova** sheet.

2. Go to:

   **Data → Data Analysis → ANOVA: Single Factor**

3. Select the range containing Touchpad, Leap Motion, and Eye Gaze data.

4. Enable **Labels in First Row** if headers are present.

5. Generate the ANOVA table.

6. Record the following values:
   - Sum of Squares (SS)
   - Degrees of Freedom (df)
   - Mean Square (MS)
   - F-statistic
   - P-value

7. Calculate the effect size (η²) using:

   \[
   \eta^2 = \frac{SS_{Between}}{SS_{Total}}
   \]

8. Determine whether a significant difference exists among the three modalities by checking whether:

   - P-value < 0.05

---

## Step 5: Pairwise t-Tests

1. Copy the cleaned dataset to the **t-test** sheet.

2. Perform the following comparisons using:

   **Data → Data Analysis → t-Test: Two-Sample Assuming Equal Variances**

3. Conduct three separate t-tests:

   - Touchpad vs Leap Motion
   - Touchpad vs Eye Gaze
   - Leap Motion vs Eye Gaze

4. For each t-test, record:
   - t Statistic
   - P(T<=t) one-tail
   - P(T<=t) two-tail

5. Highlight all p-values less than:

   ```text
   0.05
   ```

6. Determine which modality pairs show statistically significant differences.

---

## Step 6: Result Interpretation

1. Compare the mean completion times of the three modalities.

2. Analyze the ANOVA result to determine whether an overall significant difference exists.

3. Analyze the t-test results to identify which modality pairs differ significantly.

4. Report:
   - Mean and Standard Deviation
   - ANOVA F-value and P-value
   - Effect Size (η²)
   - Pairwise t-test results
   - Final conclusion regarding the best-performing modality.
