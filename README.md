# Primary Immunodeficiency in Brazil

## The project
This project’s goal was to clarify the amount of unregistered and undiagnosed primary immunodeficient patients that exists in Brazil. </br>

Primary immunodeficiency diseases (PID) are rare conditions that often get left aside due to lack of visibility. In Brazil, there is no national PID registry making it almost impossible to precisely describe the number of diagnosed patients, which is stated as 4,000[^1]. As for the number of undiagnosed patients, it is said to be around 160,000[^1].</br>

Such statements never refer to any published scientific paper and are most likely based on firsthand experience, hence this project aims to validate or refute these overly reproduced assumptions using the most reliable data source for patients’ registry in Brazil, the Latin American Society for Immunodeficiencies (LASID) registry.</br>

## Data processing
LASID’s database comprises information on 18 countries, therefore the first step was to filter out every institution with Spanish or English names, then search if the remaining were located in Brazil, and ultimately relate every institution with its location by Brazilian state. This process allowed the identification of 150 registries that weren’t assigned to any particular organization nor state but belonged to ‘several doctors from different institutions in Brazil'.</br>

The next step was to acquire data on the population of every Brazilian state which was done by accessing the Brazilian Institute of Geography and Statistics (IBGE) database, filtering for each individual state, and populating a new datasheet.</br>

Then the expected frequency for PID in the population was obtained by reviewing several scientific studies[^2][^3][^4] and the value was fixed as this project’s most important parameter.</br>

Ultimately, data on the population of the other 17 countries members of LASID was acquired by accessing worldometers.info for residents’ number.</br>

The created datasets were merged through full outer joins and right joins in Tableau to enable the creation of new variables, parameters definition, and the data visualization itself.</br>

## Results
The analysis shows that Brazil lacks a structured and efficient manner of registering diagnosed PID patients, as does other Latin-American countries.</br>

According to scientific literature, there should be 50 times more registered patients than there currently are in Brazil. This is not only related to insufficient registration, but also to the difficulty of diagnosing patients and unavailability of a national registry.</br>

Another possibility is that Brazil in fact has significantly less incidence of PID in its population than the rest of the world, but that doesn’t seem to be the case because 12 of the 27 Brazilian states have not a single registered patient. Therefore, it is more accurate to say the there are still missing registries.</br>

As neo-natal testing and new diagnosis techniques become ever more accessible, it is expected that the number of diagnosed PID patients will rise in the following years. Such trend ultimately affects medicine supplies and Brazil has already seen how the shortage of immunoglobulin – the most common medicine to treat PID – in the world market left patients uncertain about the continuity of their treatment from 2020 onward[^5].</br>

It is time for patient and medical associations to join forces and promote the importance of patients’ registration for medicine supply planning by using the expertise and experience from states as Distrito Federal that has achieved a registration rate bigger than Argentina’s.</br>

## Main challenges
LASID’s database is only fully accessible for MD, so my own access was really limited to a patient’s point of view which doesn’t show the types of PID per institution. This is a huge drawback for data analysis on the PID field because data privacy limits the study’s scope. Nevertheless, I chose to treat every subgroup of PID equally and applied the frequency rate of 50:100,000 to all of them.</br>

Furthermore, the input that constitutes LASID’s database is written by MD or patients themselves. That being the case, many institutions’ names have spelling errors which made it difficult to relate the organization and their location.</br>

Finally, displaying the frequency rate for PID was tricky because this project’s goal is to make the LASID data available for any patient, and to do so the information must be clear and easy to compare. Frequently, incidence rates maintain the nominator as one and change the denominator to match the frequency, but I chose to do the opposite and fixed the denominator as 100,000. This allows the reader to easily compare expected and assessed numbers by looking at the first integer.</br>

## Toolkits
Softwares: Tableau, and Microsoft Excel.</br>

Databases: [Latin American Society for Immunodeficiencies (LASID) registry](https://lasidregistry.org/), [Brazilian Institute of Geography and Statistics (IBGE)](https://cidades.ibge.gov.br/brasil/panorama), and [worldometers.info](https://www.worldometers.info/world-population/).</br>


[^1]: Sampaio, M. (2014). Brasil pode ter 160 mil pessoas com imunodeficiência primária, diz especialista. Source: agênciaBrasil: https://agenciabrasil.ebc.com.br/geral/noticia/2014-11/brasil-pode-ter-160-mil-pessoas-com-imunodeficiencia-primaria-diz-especialista</br>
[^3]: Dantas, E. d. (2013). Medical awareness concerning primary immunodeficiency. Source: https://www.scielo.br/j/eins/a/XLrwSfrQkFkF6M4LRBmV4pH/?lang=en&format=pdf</br>
[^2]: Júnior, P. R. (2009). Primary immunodeficiency diseases: relevant aspects for pulmonologists.' Source: Scielo Brasil: https://www.scielo.br/j/jbpneu/a/6hX59DkcRNRmQZ5x5CPKxpm/?lang=en</br>
[^4]: Pereira, D. H. (2020). Primary Immunodeficiencies in a Mesoregion of São Paulo, Brazil: Epidemiologic, Clinical, and Geospatial Approach. Source: National Library of Medicine: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7235164/</br>
[^5]: Teófilo, S. (2024). Ministério da Saúde diz em documento que estoque no SUS de remédio para imunidade só vai até começo de julho. Source: https://oglobo.globo.com/saude/noticia/2024/06/28/ministerio-da-saude-diz-em-documento-que-estoque-no-sus-de-remedio-para-imunidade-so-vai-ate-comeco-de-julho.ghtml</br>
