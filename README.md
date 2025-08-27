Engage-Integrate: Gym Member Exercise Data Exploration

Author: Kristi Wu
Date: October 2024

📝 Project Overview

  This project analyzes a gym member exercise dataset from Kaggle. It explores         various aspects of gym member characteristics, behaviors, and outcomes, including:
  
  - Gender distribution
  - Workout session durations
  - Experience levels
  - Associations between workout duration and calories burned
  - A linear regression model to predict calories burned based on session duration
  
  The project is written in R Markdown, utilizing the tidyverse and moderndive         packages to wrangle, visualize, and model the data.

📂 Data Source

  Dataset: Gym Members Exercise Dataset on Kaggle
  
  File used: gym_members_exercise_tracking.csv
  
  Each observation in the dataset represents a single gym member's workout session     and includes variables related to their physical attributes, workout habits, and     performance metrics.

🔢 Data Variables (Selected)

  Gender: Categorical (Male/Female)
  
  Age: Numeric (years)
  
  Weight, Height: Numeric (kg, m)
  
  Max_BPM, Average_BPM, Resting_BPM: Heart rate metrics
  
  Session_Duration (hours): Numeric (Workout session duration)
  
  Calories_Burned: Numeric
  
  Workout_Type: Categorical (Cardio, HIIT, Strength, Yoga)
  
  Body_Fat (%): Numeric
  
  Water_Intake (L): Numeric
  
  Workout_Frequency (days/week): Ordinal
  
  Experience_Level: Ordinal (1 = Beginner, 2 = Intermediate, 3 = Expert)
  
  BMI: Body Mass Index

📊 Key Visualizations
1. Gender Distribution

  Majority of gym members are male.

  No missing data for Gender.

2. Session Duration

  Most workouts fall between 1–1.5 hours.

  Expert gym members tend to work out longer.

  Session duration varies slightly by workout type.

3. Experience Level

  Most members are beginner or intermediate.

  Experts tend to go to the gym more frequently (4–5 days/week).

  No strong patterns by age or gender.

4. Calories Burned vs. Session Duration

  Positive relationship between workout time and calories burned.

  Linear model fitted to quantify this relationship.

📈 Regression Model
  lm(Calories_Burned ~ `Session_Duration (hours)`)
  
  Intercept: -1.446 (not practically meaningful)
  
  Slope: 721.786 → For each additional hour spent working out, the model predicts an   average increase of ~722 calories burned.
  
  Interpretation: This result aligns reasonably with expectations, though the high     calorie count suggests intense workout sessions or possible overestimation in the    dataset.

📁 Project Structure

  Engage-Integrate.Rmd – R Markdown source file for analysis and report
  
  gym_members_exercise_tracking.csv – Raw dataset (from Kaggle)
  
  README.md – This documentation file

💻 Requirements

  R (version 4.0+)

  R packages:

    tidyverse
    
    moderndive
    
    knitr
    
    ggplot2
    
    readr

  Install required packages using: 
    install.packages(c("tidyverse", "moderndive", "knitr"))

✅ Usage

  Download the dataset from Kaggle
  
  Place gym_members_exercise_tracking.csv in your working directory
  
  Open and knit the Engage-Integrate.Rmd file in RStudio to generate the HTML or PDF   report

📌 Notes

  All visualizations are built using ggplot2.
  
  Some variables (e.g., Age, Water Intake) were explored but not included in final     plots due to limited insights.
  
  The regression model is univariate but can be extended to include multiple           predictors.
