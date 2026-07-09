Bluff Detection Model — Salary Prediction using Regression
  Predicting whether a candidate's claimed salary is genuine or a "bluff" by comparing Linear Regression vs Polynomial Regression on position-level salary data.
  
 Dataset
 position - job title(Business analyst-CEO)
 level-x(variable) - Numeric position Level(1-10)
 salary-y(variables) - corresponding annual salary
 The dataset has 10 rows, capturing a non-linear salary progression across the corporate hierarchy — from $45,000 at entry level to $1,000,000 at the CEO level.  

 Four regression models were built and compared to find the best fit for this non-linear salary trend:
 
 1️⃣ Linear Regression
A simple straight-line fit — used as a baseline to show why a linear model underfits this kind of exponential salary growth.

2️⃣ Polynomial Regression (Degree 2)
Introduces curvature, improving the fit over the straight line but still not capturing the sharp jump at senior levels.

3️⃣ Polynomial Regression (Degree 3)
A closer fit to the data — captures more of the curve, though small deviations remain at the extremes.

4️⃣ Polynomial Regression (Degree 4)
The best-fitting curve — closely follows every data point, giving the most realistic prediction.

All models were trained using scikit-learn, and their predictions at level 6.5 were compared:
The candidate's claimed salary of $160,000 is closest to the Degree-4 Polynomial Regression prediction (~$158,862) — within about 1% of the claim. Linear Regression overestimates by more than double, while degrees 2 and 3 undershoot or overshoot the curve at the extremes. Degree 4 gives the tightest fit to all 10 data points, making it the most reliable model here — and confirming the candidate's claim is credible, not a bluff.

Tech Stack:
Python — core language
Pandas — data loading & manipulation
NumPy — numerical operations
Matplotlib — data visualization
scikit-learn — LinearRegression, PolynomialFeatures
