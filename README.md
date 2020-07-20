<h1> predicting-admission-UCPH-OLS </h1>
<p>
En effort to predict the upcoming(2020) admission rates at UCPH with a simple OLS regression. By scraping UCPH website for data regarding; number of applicants, number of accepted students. The current general consensus regarding creation of admission rates is that originates directly from the ratio between number of applicants and number of accepted students, noted as ratio, if this notion were to be correct we should find a linear relationship between the ratio and admission rate. 

</p>

<h3> The model </h3>
<p>
As stated in the intro the model is a simple OLS model consisting of  
</p>
<img src="https://latex.codecogs.com/svg.latex?\Large&space;kvotient_{i}=\beta_0+\beta_1(\frac{ansøgere_{t}}{optaget_{t-1})_{i}+1)^2+\beta_2(\frac{(1. prioritets ansøgere_{t}}{optaget_{t-1}+1)^2_{i}+\beta_3ansøgere_{i}+\beta_4(1.prioritets ansøgere)_{i}" title="\Large kvotient_{i} = \beta_0 + \beta_1 (\frac{ansøgere_{t}}{optaget_{t-1})_{i}+1)^2 + \beta_2 (\frac{(1. prioritets ansøgere_{t}}{optaget_{t-1}+1)^2_{i} + \beta_3 ansøgere_{i} + \beta_4 (1.prioritets ansøgere)_{i}"/>



<h3> The results </h3>

<p>
As noted in the former section there appears to not be a directly linear relationship between the ratio and admission rates. But the model does still explaing approximately 56 percent of the variance and can therefor be used as proxy for the upcomming admission rates, 2020. The model shows the following admission rates for 2020:
<p/>

| studie                                                               |   admission rates |
|:---------------------------------------------------------------------|-------------:|
| AudiologopÃ¦di                                                       |      8.73897 |
| Dansk                                                                |      6.95246 |
| Engelsk                                                              |      6.94058 |
| EuropÃ¦isk etnologi                                                  |      7.56384 |
| Film- og medievidenskab                                              |      9.69613 |
| Filosofi                                                             |      8.90979 |
| Forhistorisk arkÃ¦ologi                                              |      8.17731 |
| Fransk sprog og kultur                                               |      7.90387 |
| GrÃ¦sk, klassisk                                                     |     10.6252  |
| Historie                                                             |      7.05007 |
| Indianske sprog og kulturer                                          |      8.34162 |
| Italiensk sprog og kultur                                            |      7.71798 |
| Klassisk arkÃ¦ologi                                                  |      8.45023 |
| Kommunikation og it                                                  |      7.3677  |
| Kunsthistorie                                                        |      8.38844 |
| Latin                                                                |      8.33277 |
| Lingvistik                                                           |      8.57471 |
| Litteraturvidenskab                                                  |      8.73261 |
| MellemÃ¸stens sprog og samfund (arabisk, hebraisk, persisk, tyrkisk) |      8.06727 |
| Musikvidenskab                                                       |      8.15898 |
| PÃ¦dagogik                                                           |      8.09836 |
| Religionsvidenskab                                                   |      7.71062 |
| Retorik                                                              |      8.0173  |
| Spansk sprog og kultur                                               |      7.96412 |
| Teater- og performancestudier                                        |      8.98272 |
| Tysk sprog og kultur                                                 |      8.14623 |
| Jura                                                                 |      9.59742 |
| Biokemi                                                              |      8.09904 |
| Biologi                                                              |      8.37898 |
| Datalogi                                                             |      7.87353 |
| Forsikringsmatematik                                                 |     10.3529  |
| FÃ¸devarer og ernÃ¦ring                                              |      9.0388  |
| Geografi og geoinformatik                                            |      9.23657 |
| Geologi-geoscience                                                   |      9.59957 |
| Husdyrvidenskab                                                      |      8.26925 |
| JordbrugsÃ¸konomi                                                    |      9.20827 |
| Kemi                                                                 |      9.1938  |
| Matematik                                                            |      8.55714 |
| Matematik-Ã¸konomi                                                   |      9.13271 |
| MolekylÃ¦r biomedicin                                                |      9.87298 |
| Nanoscience                                                          |      9.37023 |
| Naturressourcer                                                      |      9.23724 |
| Antropologi                                                          |     10.7202  |
| Psykologi                                                            |     12.9229  |
| Samfundsfag                                                          |     10.435   |
| Sociologi                                                            |      9.71184 |
| Statskundskab                                                        |      9.89544 |
| Økonomi                                                             |      8.36085 |
| Farmaci                                                              |      7.62468 |
| Folkesundhedsvidenskab                                               |      9.70841 |
| Medicin                                                              |      9.96285 |
| Odontologi                                                           |     11.5232  |
| Sundhed og informatik                                                |      9.03463 |
| VeterinÃ¦rmedicin                                                    |     11.279   |

A few notes should be added to the table. First and foremost, the added bonus "hurtig start bonus" is removed from 2020, this will most likely have an ernomous impact on the admission rates and will, everything else equal, lower the admission rates compared to former years. Furthermore, the model assumes stationarity in the general level of grades, so if the mean grade of all students applying to UCPH is higher, it will have an increasing effect on the admission rates. 


