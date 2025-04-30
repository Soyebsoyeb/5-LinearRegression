# (1) OLS vs Ridge Regression with Outliers


This Python script demonstrates how Ordinary Least Squares (OLS) and Ridge Regression handle outliers differently, using a simple linear dataset with artificially added extreme outliers.

## Key Features
- Generates a linear dataset with noise (`y = 2x + 1 + noise`)
- Adds three extreme outliers at x=15, 18, 20
- Compares OLS and Ridge (L2-regularized) regression fits
- Visualizes how Ridge regression is more robust to outliers

## Requirements
- Python 3.x
- NumPy
- Matplotlib

## Code Highlights
1. **Data Generation**:
   - 30 baseline samples with linear relationship + Gaussian noise
   - 3 extreme outliers added to test robustness

2. **Model Comparison**:
   - OLS: `beta = (XᵀX)⁻¹Xᵀy`
   - Ridge: `beta = (XᵀX + λI)⁻¹Xᵀy` (λ=1000)

3. **Visualization**:
   - Shows data points in blue
   - OLS fit as red line (highly affected by outliers)
   - Ridge fit as green line (more resistant to outliers)

## Expected Output
The plot will show:
- The OLS line pulled dramatically upward by outliers
- The Ridge line maintaining a slope closer to the true relationship (slope=2)
- Clear demonstration of Ridge's outlier resistance due to L2 penalty


#  (2) (i) Ridge Regression 3D Visualization

This script demonstrates ridge regression on perfectly correlated features using an interactive 3D plot with Plotly.

## Key Features
- Visualizes ridge regression with perfectly correlated features (X2 = 2*X1)
- Shows data points and regression hyperplane in 3D space
- Demonstrates how ridge regression handles multicollinearity
- Interactive 3D plot with zoom, rotate, and pan capabilities

(a)  Data Points: Red markers showing original (X1, X2, y) observations
(b) Regression Plane: Semi-transparent surface showing predicted values



# (ii) Ridge Regression 3D Hyperplane Visualization

An optimized interactive 3D visualization demonstrating ridge regression with perfectly correlated features.

## Key Features
- 🚀 **Performance Optimized**: Reduced mesh resolution and rendering settings for faster display
- 📊 **Interactive 3D Plot**: Rotate, zoom, and explore the regression hyperplane
- 🔍 **Multicollinearity Demo**: Perfectly correlated features (X2 = 2*X1)
- ⚡ **Efficient Rendering**: Uses Plotly's offline mode for quicker display

# Optimized Ridge Regression Calculation
beta_ridge = np.linalg.inv(X_with_intercept.T @ X_with_intercept + lambda_ridge*I) @ X_with_intercept.T @ y

# Performance Optimizations:
x1_range = np.linspace(0,5,10)  # Reduced grid resolution
showscale=False  # Disabled color scale for faster rendering
aspectmode='manual'  # Fixed aspect ratio improves performance

