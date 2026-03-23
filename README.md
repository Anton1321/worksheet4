# Week 4 Worksheet Repository: Exploratory Data Analysis

This repository is the starter repository for the week 4 exploratory data analysis activity.

## Repository Structure

- `README.md`: this file
- `requirements.txt`: Python packages for the activity
- `data/clean/store_week_clean.csv`: cleaned sample data for the activity
- `code/worksheet4_eda_student.ipynb`: notebook for you to complete
- `code/worksheet4_eda_sample_answers.ipynb`: sample answers notebook
- `output/`: save any figures or exported outputs here

## Getting Started

1. Create and activate a Python environment.
2. Install the required packages with `pip install -r requirements.txt`.
3. Open `code/worksheet4_eda_student.ipynb` in VS Code.
4. Work through the notebook and save any figures you want to keep in `output/`.
5. Update this `README.md` with what you find in the data.

## Analysis Notes

### Dataset
The cleaned dataset (`data/clean/store_week_clean.csv`) contains 400 rows representing 20 stores tracked over 20 weeks (starting January 2025). Each row is one store in one week. Key numeric variables are `total_hours`, `avg_hourly_pay`, and `weekly_sales`. Categorical variables include `store_type`, `region`, `promotion_flag`, and `staffing_model`.

### Distributions
- `total_hours` is spread out with no single clear peak, reflecting different staffing levels across store types.
- `avg_hourly_pay` is slightly right-skewed, with most values clustered together but a few higher-paying outliers.
- `weekly_sales` is right-skewed and bunched — most stores earn in a similar range, but some earn considerably more.

### Categorical Composition
- `store_type` and `region` are perfectly balanced (100 observations each), since the data is a fixed panel.
- `promotion_flag` shows that promotions are relatively rare compared to non-promotion weeks.

### Scatter Plots and Correlations
- There is a strong positive relationship between `total_hours` and `weekly_sales` (Pearson = 0.747, Spearman = 0.737). More hours worked corresponds to higher weekly sales.

### Scale and Group Analysis
- Using a log scale on the y-axis revealed that the positive hours–sales relationship holds across the full range of sales, not just among high-earning outliers.
- Splitting by group showed that CBD stores earn more sales for the same hours worked than Campus or Neighbourhood stores. The hours–sales correlation is strong across all regions but weaker in the East (0.67) compared to North (0.81), suggesting other factors matter more in some regions.

## Git Reminder

All relevant changes should be committed and pushed back to your own GitHub repository.
