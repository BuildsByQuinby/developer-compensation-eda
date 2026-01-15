project:
  name: developer-compensation-eda
  title: Developer Compensation EDA
  description: >
    Exploratory data analysis of global developer compensation, work experience,
    and job satisfaction using real Stack Overflow survey data.

dataset:
  source: Stack Overflow Developer Survey
  host: IBM Cloud Object Storage
  access_method: Public URL
  load_example:
    language: python
    code: |
      file_url = "https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/n01PQ9pSmiRX6520flujwQ/survey-data.csv"
      df = pd.read_csv(file_url)

tools:
  - Python
  - Pandas
  - Matplotlib
  - Seaborn

analysis:
  objectives:
    - Analyze distribution of yearly compensation
    - Remove extreme salary outliers
    - Calculate correlations between compensation, experience, and satisfaction
    - Visualize salary trends across countries

  methods:
    - Histogram analysis
    - Boxplot comparisons
    - Quantile-based outlier trimming
    - Pearson correlation analysis
    - Scatter plot visualization
    - Heatmap visualization

findings:
  experience_vs_salary:
    correlation: moderate_positive
    interpretation: Experience is a meaningful predictor of compensation

  satisfaction_vs_salary:
    correlation: negligible
    interpretation: Job satisfaction does not significantly correlate with salary

  country_variation:
    variation: high
    interpretation: Compensation differs significantly between countries

visuals:
  - title: Salary Distribution
    file: images/salary_distribution.png

  - title: Salary by Country (Top 10)
    file: images/salary_by_country.png

  - title: Correlation Heatmap
    file: images/correlation_heatmap.png

  - title: Salary vs Experience
    file: images/salary_vs_experience.png

  - title: Salary vs Satisfaction
    file: images/salary_vs_satisfaction.png

conclusion: >
  Professional experience is a stronger predictor of salary than job satisfaction.
  Compensation increases with experience, but satisfaction remains largely independent
  of income.

credits:
  original_authors:
    - Ayushi Jain

  contributors:
    - Rav Ahuja
    - Lakshmi Holla
    - Malika

  analysis_by: William Quinby
