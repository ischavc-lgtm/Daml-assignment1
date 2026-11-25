Film Ratings Dataset
This dataset is the Alternative that assignment1 describes as there are no seperate files.
a) Dataset description

This dataset contains my 40 most recently rated films from Letterboxd, a film logging application. Each rating represents one item in the dataset.
The dataset contains the following information for each film: a unique identifier (Film_ID), the date on which I rated the film, the film's title, the film's original release year, a link to the film on Letterboxd and my personal rating.
I added unique identifiers to each film, starting with film_001.
The dataset consists of my own personal data, which I downloaded from my Letterboxd account. I have chosen to share this data for this assignment.

b) Motivation

I chose to use my own personal data because I wanted to make sure I was allowed to use and share the data for this assignment.
Although my personal film-watching history cannot answer many broader research questions on its own, it is interesting to explore my own viewing habits. For example, the dataset can be used to calculate my average film rating, examine how many films I have watched and investigate which decades the films I watch come from.
If similar data from multiple users were available, it could also be used for broader research. For example, researchers could investigate whether the time at which someone watches a film influences their rating or their feelings about the film.

c) Selection criteria

The assignment required a dataset containing approximately 20–50 items. Therefore, I selected my 40 most recently rated films.
I only included films that I had rated. Letterboxd also allows users to export other information, such as watchlists and written reviews. Although written reviews could have provided interesting additional information, I decided not to include them because I have not written many reviews.
Consequently, this dataset represents my 41 most recently rated films and does not represent all films I have watched or added to my Letterboxd account.

d) Data collection process

I collected the data from my personal Letterboxd account. Letterboxd provides an option to export account data as a ZIP file containing several CSV files, including information about films, ratings, reviews and lists.
I downloaded the export and selected the CSV file containing my film ratings. I then added unique identifiers to the films and saved the original and cleaned versions separately.

e) Cleaning and preprocessing

I made one change to the original dataset.
One of the film titles contained a comma: Crouching Tiger, Hidden Dragon. When I tried to read the CSV file in a Jupyter Notebook using Pandas, I encountered a parsing error.
The error occurred because the quotation marks around the film title were not formatted correctly. As a result, Pandas interpreted the comma in the title as a column separator and expected five fields but found six.
I experimented with the quotechar parameter in Pandas and changing double quotation marks (") to single quotation marks ('). However, this did not solve the underlying formatting problem in the original CSV file.
To resolve the issue, I removed the comma from the film title. After this change, Pandas could read the CSV file correctly.
I saved the cleaned dataset in a separate folder called cleaned-data and kept the original, unchanged export in the data folder.

f) Structure and codebook

The project contains the following files and folders:
data/: Contains the original CSV export from Letterboxd.
cleaned-data/: Contains the cleaned CSV file used for analysis.
README.md: Contains the dataset description, methodology and codebook.

The following table describes the variables in data.csv.

Film_ID
Data type: String
Description: Unique identifier assigned to each film.
Expected format: film_001, film_002, etc.
Example: film_001

Date
Data type: Date
Description: Date on which the film was rated.
Expected format: YYYY-MM-DD.
Example: 2026-04-12

Name
Data type: String
Description: Full title of the film.
Expected format: Text.
Example: Punch-Drunk Love

Year
Data type: Integer
Description: Original release year of the film.
Expected format: Four-digit year.
Example: 2002

Source
Data type: String
Description: URL linking to the film on Letterboxd.
Expected format: Valid URL.
Example: https://boxd.it/20E4

Rating
Data type: Float
Description: Personal rating given to the film.
Expected values: 0.5–5.0 stars, every half star.
Example: 4.5

g) Uses and limitations

The dataset can be used to explore personal film-watching habits and calculate basic descriptive statistics. Possible analyses include calculating the average rating of the films, investigating which decades the films were released in, examining the distribution of my film ratings and exploring changes in my film-watching activity over time.
However, the dataset also has several limitations.
First, it only contains 40 recently rated films and therefore does not represent my complete film-watching history. Second, the ratings are subjective and reflect only my personal opinions. Finally, the dataset contains information from only one user, so the results cannot be generalised to other Letterboxd users or film audiences.
The dataset does not contain written reviews or other textual information. Therefore, it cannot be used to perform sentiment analysis or investigate the language people use when discussing films.

h) Data ownership and permission

The data was downloaded from my own personal Letterboxd account. Letterboxd provides an export function that allows users to retrieve data they have provided to the platform.

The exported data contains my own film ratings and associated information. I have chosen to share my personal data for this assignment.

i) Licence

The dataset is shared under the Creative Commons Attribution 4.0 International (CC BY 4.0) licence.

Ai statement: 
I used AI to try and solve the issue with the title that included a comma, but that did not help. I also used AI to correct my spelling as this README.md does not have a spellingcheck.