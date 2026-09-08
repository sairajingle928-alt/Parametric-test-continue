# Parametric-test-continue
<br>
these is for practice purpose for becoming expert in this field
<br>
#One-sample t-test
from scipy import stats
weights = [502, 498, 501, 503, 499, 500, 500, 504, 497]
t_stat, p_value = stats.ttest_1samp(weights, 500)
print("t-statistic:", t_stat)
print("p-value:", p_value)
<br> result
t-statistic: 0.5803810000880257
p-value: 0.5776352324548429
<br>
# Independent two-sample t-test
from scipy import stats
formulation_A = [80, 82, 79, 81, 83]
formulation_B = [85, 87, 86, 88, 84]
<br>
t_stat, p_value = stats.ttest_ind(formulation_A, formulation_B)
print("t-statistic:", t_stat)
print("p-value:", p_value)
<br>result
t-statistic: -5.0
p-value: 0.0010528257933665399
<br>
# Paired t-test
before = [120, 130, 125, 140, 135]
after =  [115, 125, 120, 130, 128]
t_stat, p_value = stats.ttest_rel(before, after)
print("t-statistic:", t_stat)
print("p-value:", p_value)
<br>result
t-statistic: 6.531972647421809
p-value: 0.0028378459267344473
<br>
#Pearson correlation coefficient
from scipy import stats
polymer = [1, 2, 3, 4, 5]
release = [90, 85, 80, 75, 70]
r_value, p_value = stats.pearsonr(polymer, release)
print("correlation coefficient:", r_value)
print("p-value:", p_value)
<br>result
correlation coefficient: -1.0
p-value: 0.0
<br>
#One-Way ANOVA 
from scipy import stats
group1 = [80, 82, 81, 79]
group2 = [85, 86, 87, 84]
group3 = [90, 92, 91, 89]
f_stat, p_value = stats.f_oneway(group1, group2 , group3)
print("F-statistic:", f_stat)
print("P-value:", p_value)
<br>result
F-statistic: 60.0
P-value: 6.2580293569917225e-06
<br>
# Mann-Whitney U test
# Alternative to t test
# non parametric equivalent of independent t test
from scipy.stats import mannwhitneyu
group1 = [5, 7, 8, 6, 9]
group2 = [10, 12, 11, 13, 14]
u_stat, p_value = mannwhitneyu(group1, group2)
print("U-statistic:", u_stat)
print("p-value:", p_value)
<br>result
U-statistic: 0.0
p-value: 0.007936507936507936
<br>
# Wilcoxon Signed-Rank Test
# Alternative to t test
# non parametric equivalent of paied t test
from scipy.stats import wilcoxon
before = [120, 130, 125, 140, 135]
after =  [115, 125, 120, 130, 128]
stat, p_value = wilcoxon(before, after)
print("Statistic:", stat)
print("p-value:", p_value)
<br>result
Statistic: 0.0
p-value: 0.0625
<br>
#Shapiro-wilk Normality Test
from scipy.stats import shapiro
data = [12, 15, 14, 16, 13, 18, 17]
stat, p_value = shapiro(data)
print("Statistic:", stat)
print("p-value:",p_value)
<br>result
#Shapiro-wilk Normality Test
from scipy.stats import shapiro
data = [12, 15, 14, 16, 13, 18, 17]
stat, p_value = shapiro(data)
print("Statistic:", stat)
print("p-value:",p_value)
<br>
Statistic: 0.9780016294121008
p-value: 0.9492885623536165




