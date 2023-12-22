## Replication of Labour Supply Elasticity in Malawi

The data used for the project has been added to the repository. 

The citation to the paper for the project is as follows: 
Goldberg, J. (2016) “Kwacha Gonna Do? Experimental Evidence About Labor Supply In Rural Malawi.” American Economic Journal: Applied Economics, Vol. 8, No. 1, pp. 129–149. 

### <a href="https://d396qusza40orc.cloudfront.net/exdata%2Fdata%2Fhousehold_power_consumption.zip](http://econweb.umd.edu/~goldberg/docs/Goldberg_AEJ2016.pdf)http://econweb.umd.edu/~goldberg/docs/Goldberg_AEJ2016.pdf">Link To The Paper</a>

The paper studies the wage elasticity of employment in the day labor market in rural Malawi. And attempts to answer the following empirical question. 

***Empirical question:  What is the probability of pursuing casual employment for a given wage?***

***Policy question: Are public employment programs able to self-target and help mitigate the socioeconomic and gender disparity in developing agrarian countries?***

Understanding the impact of tailored public employment programs in developing agrarian countries is crucial for addressing socioeconomic and gender disparities.  
These programs offer stable income sources for a workforce largely engaged in self-employment or casual labor.  
Studying such experiments helps policymakers set wages that balance participation incentives with program costs.

Recognizing that participants' decisions are influenced by immediate needs underscores the importance of timely payments.  
By incorporating these insights, policymakers can design more effective and inclusive interventions, promoting poverty reduction, gender equality, and overall socioeconomic development in a targeted manner. 

Furthermore, the previous literature shows a higher elasticity of labor for women than men in both developed and developing countries.  
However, the author, post the experiment has identified a characteristic of Malawi’s labor market, where we see equality in labor supply elasticity between men and women in the agricultural off-season. 
Developing agrarian countries with a defined wet and dry season have different gender and socioeconomic patterns than the previous literature and need to be further explored when informing policy design.


### Hypothesis For Potential Testing

As a part of this study, the independent variable is the wage offered for the particular work period.  With β1 measuring the impact of X1  on the independent variable, we can define the following hypothesis:

Hypothesis 1 (H0: β1 = 0):  The null hypothesis suggests that changes in wages have no significant impact on the fraction of individuals employed.

Hypothesis 2 (Alternative: β1 < 0):  A negative coefficient (β1 < 0) would indicate that an increase in wages leads to a decrease in the fraction of individuals employed.
        
Hypothesis 3 (Alternative: β1 > 0):  A positive coefficient (β1 > 0) would suggest that an increase in wages leads to an increase in the fraction of individuals employed.


### Regression Equation

Initial simple bivariate regression that serves as the centerpiece of our project:

Yi = β0 + β1X1i + ui

laborₜᵥ =α + βln(wage ₜᵥ) + v ₜᵥ  

Where,

labortv  = Fraction of individuals in village ‘v’ who are employed in week ‘t’

ɑ = intercept term

ꞵ = coefficient term associated with ln (wagetv)

ln(wagetv) = Natural log of wages in village ‘v’ in week ‘t’

vtv = Error term: capturing unobserved factors that affect employment in village ‘v’ in week ‘t’

### Labour Elasticity Calculation

Dr Goldberg has taken the definition of ‘elasticity’ to be the change in labor supply for a given wage and differentiated the labor supply regression for wage. 

laborₜᵥ =α + βln(wageₜᵥ) + vₜᵥ  

∂labor/∂wage  = α + βln(wageₜᵥ) + νtv

∂labor/∂wage  =  β/((wage))

ϵ =∂labor/∂wage  *  wage/labor  	

ϵ =β/((wage))*((wage))/(mean(labor))  

ϵ = β/(mean(labor))

To the best of our understanding, we have used the elasticity formula that Dr. Goldberg has used after having understood the formula above.


### Interpretation

The regression findings offer valuable insights into the determinants of labor supply within this study.  Household size shows a positive but statistically insignificant effect.  
Education, although displaying a negative impact on labor, doesn't reach statistical significance at conventional levels.  Marital status and various housing characteristics present mixed effects, with some variables demonstrating significant relationships.  
Having a metal roof is associated with decreased labor participation, whereas having no previous work experience is linked to increased labor participation.  
Additionally, village-specific attributes play a notable role, influencing varying levels of labor supply across different villages.  
These results collectively underscore the complex interplay of individual, household, and village-level factors in shaping labor decisions.
The correlation matrix further elucidates the relationships between average labor supply, wages, and the wage at which individuals are willing to accept work.  
The correlation between average labor supply and wages stands at approximately 0.34, indicating a modest yet positive correlation. 
Similarly, the correlation between average labor supply and accepted wages is stronger at 0.54, suggesting a more pronounced relationship between these variables.


#### Comparing Labor Supply Elasticity At Predicted Labor Force Participation 

From the initial regression, we can develop a predictor for the given dataset.  We used the existing labor and wage data and ran the regression predictor on the same to get predicted values of labor force participation at given wages offered. 
Further, to calculate the elasticity of predicted labor participation at offered wage levels, we created a new variable and used the above formula to generate individual elasticities at different predicted levels of labor participation. 

#### Replicating The Counterfactual

I am taking the observed labor participation rate at the level of MK 30 and testing the counterfactual that the labor market is fully employed at MK 140.  
For this counterfactual, we are only interested in the values of labor at MK30 and MK140, hence all other observations have been dropped. 

I am successfully able to replicate her counterfactual and verify that the highest possible labor elasticity when I have given employment at the lowest wage levels and full employment at the highest possible wage levels is 0.20.
The given elasticity without the counterfactual is 0.15 (0.16 with fixed effects) and the highest elasticity possible elasticity is 0.20, 
a difference of 0.04 in the elasticity of labor supply is not very high in real-world terms and further strengthens the hypothesis that the labor supply in Malawi is highly inelastic owing to the low levels of income in the dry season. 


### Scope For Further Research

1.	Extending the study over a period of time

A follow-up project could be conducted over a longer duration that looks into the temporal aspect of labor supply elasticity, exploring how variations over time affect the observed patterns. 
Investigating how changes in seasons or economic conditions impact labor supply would provide valuable insights.  
Examining the dynamics of elasticities across different periods could enhance our understanding of the factors influencing labor behavior in rural settings, informing the design of effective public employment programs in developing countries.

2.	Adding 	a minimum support level 

We see that the population is willing to gain employment at the lowest wages and that during the dry season, the availability of gainful employment is limited.
We wanted to consider a public assistance program consisting of a minimum support endowment that is given to the participants for their daily sustenance. 
With the minimum endowment taking care of daily needs, we believe that we will be able to see variance in the acceptable levels of wage at which employment is generated.  
We may see labor force participation reduced at the lowest wage and potentially see dispersion in the data to be able to make further conclusions about elasticity. 
This would also give us insight into the savings behavior of the population.  Given that the daily needs are being taken care of, whether the population considers savings from the potential wages received. 

4.	Testing with a formal or informal credit system

Dr. Goldberg briefly mentions that the presence of credit constraints generates inefficient labor supply given that they are too poor to select out of employment opportunities. 
Introducing a formal or informal credit sector would influence the population to rely on lending to generate other forms of employment during the dry season.  
This would potentially result in lower levels of elasticity for employment offered as a part of the ‘ganyu’.
 
