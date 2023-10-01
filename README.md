# Date Reconstruction for Cuneiform Documents

This repository includes a Jupyter Notebook that assess the plausibility of using prosopography to assign dates to documents in which the dating formula is broken.

An important digital prospographical resource for ancient cuneiform documents is the [Prosobab project and Database](https://prosobab.leidenuniv.nl/)[^1]. It is an open access prosopography of individuals who appear in cuneiform documents from 678-325 BCE. These documents are daily texts, primarily legal documents. For the tablets available in the database, every person attested in a document is a case, and different attestations of the same person are linked via a common ID (termed PID in the database columns). This database allows for a large quantitative evaluation of the wide-spread methodology of using prosopography - disambiguated individuals - for reconstructing missing dates in historical documents.

In order to assess this, I take the following steps:
- filter the cases in the database to keep only those with fully preserved dates
- store all the years of activity for each disambiguated individual in the database in a dictionary. Remove ranges that are above a certain limit that is not realistic or not indicative
- for each document, find the overlap in the years of activity between all the individuals, without taking into consideration the date of the current document
- create a range (a list) of the shared years, and calculate the mean and median of that range
- measure the distance from the range, mean, and median to the real date of the document

This work was done as part of a final project in the course "YData - Introduction to Data Science" at Yale University, department of Statistics & Data Science, Spring 2023.

[^1]: C. Waerzeggers, M. Groß, et al., Prosobab: Prosopography of Babylonia (c. 620-330 BCE) (Leiden University, 2019).
