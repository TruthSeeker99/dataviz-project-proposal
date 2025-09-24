# Data Visualization Project

## Data

For this project, I propose to explore **three datasets** that represent different types of data and support diverse visualization methods:

1. **UCI Student Performance Dataset** ([link](https://archive.ics.uci.edu/dataset/320/student+performance))  
   This dataset contains demographic information (gender, age, parental education), lifestyle factors (study time, alcohol consumption, family support), and academic records (grades G1, G2, and G3). It is widely used in educational data analysis and offers many opportunities to explore correlations and subgroup differences.  
   *(Replaces the earlier Car Sales dataset, which appeared simulated and less meaningful.)*

2. **Bitcoin OTC Trust Network** ([link](https://snap.stanford.edu/data/soc-sign-bitcoinotc.html))  
   This is a signed network dataset of user-to-user trust ratings. Each edge includes a source, target, rating (–10 to +10), and timestamp. It provides a rich context for analyzing social trust structures, network centrality, and dynamics over time.  

3. **Average Monthly Temperature by U.S. State (1950–2022)** ([source: NOAA/NCEI](https://www.ncei.noaa.gov/))  
   This dataset contains spatio-temporal climate information with monthly average temperatures for each U.S. state, along with latitude and longitude. It is suitable for geographic and temporal visualizations of climate change patterns.  

---

## Questions & Tasks

The following questions will drive the visualization and interaction designs:

**Student Performance**  
* How do grades vary across demographic factors (age, gender, school)?  
* Is there a correlation between study time and final performance (G3)?  
* How do early grades (G1, G2) relate to final outcomes (G3)?  

**Bitcoin OTC Trust Network**  
* Which users are the most trusted or distrusted in the network?  
* What structures emerge from positive vs. negative edges?  
* How does trust evolve over time?  

**U.S. Temperature**  
* How have average temperatures changed over time at the state level?  
* Which regions show the strongest warming trends?  
* Are there seasonal or geographic patterns in climate variation?  

---

## Sketches

I drafted sketch ideas for each dataset:

1. **Student Performance**  
   * Scatter plot: Age vs. final grade (G3), color by school.  
   * Line chart: Average G3 vs. age, split by school.  
   * Bar chart: Average scores (G1–G3) grouped by study time.  
   * Population pyramid: Male vs. female distribution of G3 scores.  

2. **Bitcoin OTC Trust Network**  
   * Force-directed network graph with nodes sized by in-degree trust and colored by average rating.  
   * Edge width encodes trust magnitude, and edge color encodes positive vs. negative ratings.  
   * Advanced idea: time slider to animate trust network evolution.  

3. **U.S. Temperature**  
   * Choropleth map of the U.S. with color encoding average monthly temperature.  
   * Line chart for each state’s temperature trend over time.  
   * Advanced idea: interactive time slider to animate climate changes from 1950–2022.  

---

## Prototypes

I’ve created a first prototype visualization for the **Student Performance dataset**.  
It includes a scatter plot, line chart, grouped bar chart, and back-to-back bar chart (population pyramid), which address some of the core questions for this dataset.  

Prototype screenshot:  

[![prototype](prototype.png)](prototype.png)

This prototype serves as an initial dashboard for **multi-dimensional data visualization**. It combines four fundamental chart types to represent different aspects of the dataset and provide complementary perspectives on student performance.

### Future Directions
- **Flexible chart replacement**: expand beyond the initial four types  
- **Customizable attributes**: allow users to choose which data fields to visualize  
- **Interactive features**: enable cross-chart linking and coordinated highlighting for deeper insight  

---

## Open Questions

* For the trust network, how best to visualize large graphs without losing clarity?  
* For the climate data, which geographic base map format is best suited for integration (TopoJSON vs. GeoJSON)?  
* For categorical-heavy attributes in the student dataset, which encoding best avoids overlap and ensures readability?  

---

## Milestones

* **Week 1–2**: Clean and preprocess all three datasets. Create static plots for Student Performance.  
* **Week 3–4**: Build interactive prototype for Student Performance. Start Bitcoin network visualization.  
* **Week 5–6**: Add U.S. Temperature spatio-temporal visualization with time slider.  
* **Week 7 (Final)**: Polish all visualizations into one interactive portfolio piece. Prepare final video presentation.  
