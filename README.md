<h1> predicting-admission-UCPH-OLS </h1>
<p>
En effort to predict the upcoming(2020) admission rates at UCPH with a simple OLS regression. By scraping UCPH website for data regarding; number of applicants, number of accepted students. The current general consensus regarding creation of admission rates is that originates directly from the ratio between number of applicants and number of accepted students, noted as ratio, if this notion were to be correct we should find a linear relationship between the ratio and admission rate. 

</p>

<h3> The model </h3>
<p>
As stated in the intro the model is a simple OLS model build with the following relationship.  
</p>

<a href="https://www.codecogs.com/eqnedit.php?latex=kvotient_{i}=\beta_0&plus;\beta_1(\frac{\text{ansoegere}_{t}}{\text{optaget}x_{t-1}})_{i})&plus;\beta_2(\frac{(\text{1.&space;prioritets&space;ansoegere}_{t}}{\text{optaget}_{t-1}})_{i}&plus;\beta_3\text{ansoegere}_{i}&plus;\beta_4(\text{1.&space;prioritets&space;ansoegere})_{i}&plus;X_{i}" target="_blank">
 <img src="https://latex.codecogs.com/png.latex?kvotient_{i}=\beta_0&plus;\beta_1(\frac{\text{ansoegere}_{t}}{\text{optaget}x_{t-1}})_{i})&plus;\beta_2(\frac{(\text{1.&space;prioritets&space;ansoegere}_{t}}{\text{optaget}_{t-1}})_{i}&plus;\beta_3\text{ansoegere}_{i}&plus;\beta_4(\text{1.&space;prioritets&space;ansoegere})_{i}&plus;X_{i}" title="kvotient_{i}=\beta_0+\beta_1(\frac{\text{ansoegere}_{t}}{\text{optaget}x_{t-1}})_{i})+\beta_2(\frac{(\text{1. prioritets ansoegere}_{t}}{\text{optaget}_{t-1}})_{i}+\beta_3\text{ansoegere}_{i}+\beta_4(\text{1. prioritets ansoegere})_{i}+X_{i}" /></a>


<a href="https://www.codecogs.com/eqnedit.php?latex=X_{i}=\beta_5human_{i}&plus;\beta_6jura_{i}&plus;\beta_7natur_{i}&plus;\beta_8samf_{i}&plus;\beta_9sund_{i}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?X_{i}=\beta_5human_{i}&plus;\beta_6jura_{i}&plus;\beta_7natur_{i}&plus;\beta_8samf_{i}&plus;\beta_9sund_{i}" title="X_{i}=\beta_5human_{i}+\beta_6jura_{i}+\beta_7natur_{i}+\beta_8samf_{i}+\beta_9sund_{i}" /></a>

<p>
The OLS results are as follow:
</p>


![ols_results](https://user-images.githubusercontent.com/35741586/88041756-23184400-cb4b-11ea-8d55-9e2cd43035fe.png)


<h3> The conclusion </h3>

<h5> Predicting the admission rates for this year, 2020 </h5>
<p>
As noted in the former section there appears to not be a directly linear relationship between the ratio and admission rates. But the model does still explaing approximately 72 percent of the variance and can therefore be used as proxy for the upcomming admission rates, 2020. The model shows the following admission rates for 2020:
<p/>

| studie                        |   kvo_2020(predicted) |   kvo_2019(empirical) |   change, pct. |
|:------------------------------|-----------:|-----------:|---------------:|
| AudiologopÃ¦di                |       8.74 |        9.2 |             -5 |
| EuropÃ¦isk etnologi           |       7.56 |        7.2 |              5 |
| Film- og medievidenskab       |       9.7  |       10.1 |             -4 |
| Filosofi                      |       8.91 |        9.5 |             -6 |
| Forhistorisk arkÃ¦ologi       |       8.18 |        7   |             17 |
| Historie                      |       7.05 |        7.3 |             -3 |
| Klassisk arkÃ¦ologi           |       8.45 |        7.7 |             10 |
| Kommunikation og it           |       7.37 |        8.3 |            -11 |
| Kunsthistorie                 |       8.39 |        9.1 |             -8 |
| Lingvistik                    |       8.57 |        9.8 |            -13 |
| Litteraturvidenskab           |       8.73 |       10.3 |            -15 |
| PÃ¦dagogik                    |       8.1  |        9.3 |            -13 |
| Religionsvidenskab            |       7.71 |        6.4 |             20 |
| Retorik                       |       8.02 |        8.6 |             -7 |
| Teater- og performancestudier |       8.98 |        9   |             -0 |
| Jura                          |       9.6  |        9.7 |             -1 |
| Biokemi                       |       8.1  |        6.6 |             23 |
| Datalogi                      |       7.87 |        7   |             12 |
| Forsikringsmatematik          |      10.35 |       11.5 |            -10 |
| Matematik-Ã¸konomi            |       9.13 |        9.8 |             -7 |
| MolekylÃ¦r biomedicin         |       9.87 |       11.2 |            -12 |
| Antropologi                   |      10.72 |       11.1 |             -3 |
| Psykologi                     |      12.92 |       11.8 |              9 |
| Samfundsfag                   |      10.43 |       10.4 |              0 |
| Sociologi                     |       9.71 |       10.7 |             -9 |
| Statskundskab                 |       9.9  |       11.1 |            -11 |
| Ãkonomi                               |       8.36 |        7.9 |              6 |
| Farmaci                       |       7.62 |        8.3 |             -8 |
| Folkesundhedsvidenskab        |       9.71 |        9.6 |              1 |
| Medicin                       |       9.96 |       11.1 |            -10 |
| Odontologi                    |      11.52 |       10.8 |              7 |
| VeterinÃ¦rmedicin             |      11.28 |       11   |              3 |

A few notes should be added to the table. First and foremost, the added bonus "hurtig start bonus" is removed from 2020, this will most likely have an enormous impact on the admission rates and will, everything else equal, lower the admission rates compared to former years. Furthermore, the model assumes stationarity in the general level of grades, so if the mean grade of all students applying to UCPH is higher, it will have an increasing effect on the admission rates. 


