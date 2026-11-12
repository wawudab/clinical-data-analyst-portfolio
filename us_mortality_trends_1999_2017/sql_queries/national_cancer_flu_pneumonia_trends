SELECT 
    Year,
    Cause_Name,
    SUM(Deaths) AS Total_deaths,
    AVG(Age_adjusted_Death_Rate) AS avg_age_adjusted_rate
FROM nchs_leading_causes_of_death_united_states
WHERE Cause_Name IN ('Influenza and pneumonia','Cancer')
GROUP BY Year, Cause_Name
ORDER BY Year, Cause_Name;
