# Is Pluto a Planet? A Clustering Analysis of Solar System Bodies

This project uses clustering techniques to explore whether Pluto belongs with the planets or more closely resembles other solar system objects. It combines astronomy, data science, and interpretability using machine learning tools.

## Dataset
A self-curated dataset of 29 solar system bodies orbiting the Sun, collected from Wikipedia. All bodies for which all of the features are listed on Wikipedia were selected. They include features such as:
- Mass
- Eccentricity
- Semi-major axis
- Inclination
- Rotational period

## Objective
Determine whether Pluto clusters more with the planets or with other bodies such as TNOs and asteroids using:
- KMeans clustering
- Silhouette and Elbow methods
- Decision tree classification

## Methods
- Removed collinear features
- Log-transformed, then normalized data
- Used silhouette and elbow scores to determine optimal `k`
- Ran clustering with multiple seeds and cluster numbers to test Pluto's stability
- Visualized clusters and decision trees

## Results
- Optimal `k=5` based on silhouette and elbow tradeoff
- Pluto consistently clustered with TNOs
- Across 400 randomized trials, Pluto was in the same cluster as a planet:
  - 18% of the time with 2 clusters
  - 0-4% of the time with 3-5 clusters
  - 0% with 6-9 clusters
  - Those clusters including Pluto with the planets had additional bodies classed as planets as well

## Insights
- The clustering generally matched known categories: terrestrial planets, gas giants, TNOs, asteroid belt
- Pluto's physical and orbital properties place it firmly with other TNOs
- The findings support the IAU's decision to reclassify Pluto

## How to Run
Install dependencies:
```bash
pip install -r requirements.txt
```

Place `SolarSystemBodies.csv` in the same directory as the notebook, and run:

```bash
jupyter notebook
```

## Files
- `PlutoClustering.ipynb` - Main notebook
- `SolarSystemBodies.csv` - Dataset
- `README.md`, `requirements.txt`, `LICENSE`

## License
MIT License
