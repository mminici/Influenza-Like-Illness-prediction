# Influenza-Like-Illness prediction

This project aims to implement a prediction model for Influenza-like illness in Italy.

## Brief history in the literature

Detecting epidemics using digital data is an hot topic in modern literature. For what regards influenza epidemics, the research paper "Detecting influenza epidemics using search engine query data" by Ginsberg, Mohebbi, Patel, Brammer, Smolinski & Brilliant published by Nature(2009) has been a milestone which brought the CDC to use Google FluTrend as gold standard for Influenza-Like Illness. All went good untile "GFT overestimated the prevalence of flu in the 2012–2013 season and overshot the actual level in 2011–2012 by more than 50%" as Lazer, Kennedy, King, Vespignani reported in the article "The Parable of Google Flu: Traps in Big Data Analysis" on Science(2014). This thing pushed the research community to go further in the prediction analysis of Influenza-Like-Illness from digital data


### Why influenza is important to estimate?

It could seem that in developed countries the influenza epidemics is well controlled but if we see the real data "Seasonal influenza epidemics result in an estimated 3 to 5 million cases of severe illness and 250,000 to 500,000 deaths worldwide each year" from https://www.who.int/en/news-room/fact-sheets/detail/influenza-(seasonal).


### General pattern for digital disease detection

1. Ground truth data from official source, this will be your gold standard.
2. Proxy data from digital source.
3. **Problem**: Predict ground truth data(target) from proxy data (features).
4. Train a statistical/learning model to solve the problem.
5. Validate model performance.


## Addressed problem: predict Influenza-like illness in Italy

1. Ground truth: The data comes from the epidemiologic surveillance by the ISS(**I**stituto **S**uperiore di **S**anità) on influenza. The data are available [here](https://old.iss.it/site/RMI/influnet/pagine/stagioni.aspx).
2. Proxy data: The digital data comes from the Wikipedia page view rate on pages related to Influenza. The data were scraped from the [PageView service](https://tools.wmflabs.org/pageviews/?project=it.wikipedia.org&platform=all-access&agent=user&range=all-time&pages=Influenza|Febbre) from the Wikimedia Toolforge.

The adopted methodology is inspired by the work > D.J. McIver & J. S. Brownstein (2014), "Wikipedia Usage Estimates Prevalence of Influenza-Like Illness in the United States in Near Real-Time", PLoS Comput Biol 10(4): e1003581 http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003581


Further discussion can be found into the Jupyter Notebook inside the repository.



## Built With

* [Selenium](https://www.seleniumhq.org/) - Used to scrape dynamic web data
* [Scikit-learn](https://scikit-learn.org/) - For the setup of most of the machine learning models
* [H2O](https://github.com/h2oai) - For create the GLM used in the McIver & Brownstein paper.

## Final Results

All the results can be found on the Jupyter Notebook in the repository

## Authors

* **Valerio Guarrasi** - *M.Sc. in Data Science student* - [guarrasi1995](https://github.com/guarrasi1995)

* **Andrea Marcocchia** - *M.Sc. in Data Science student* - [andreamarco](https://github.om/andremarco)

* **Marco Minici** - *M.Sc. in Data Science student* - [mminici](https://github.com/mminici)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* All the work is inspired by the course lectures held by Professor Ciro Cattuto in "Digital Epidemiology"
