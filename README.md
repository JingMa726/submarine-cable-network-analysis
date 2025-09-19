# submarine-cable-network-analysis
Complex network analysis of global submarine cable infrastructure. Studying network topology, centrality metrics, community detection, and vulnerability assessment across 129 countries connected by 144 international cables.
<img width="1344" height="960" alt="image" src="https://github.com/user-attachments/assets/53314286-8b19-4c6a-9c8f-a1d04aa5398b" />
## What I Found
The global submarine cable network is surprisingly sparse - with only 7.16% of possible connections actually existing, yet it maintains strong connectivity with an average path length of just 3.44 steps between any two countries. France and the United States emerge as the most critical hubs, with France having 62 cable connections and the US having 50.

Community detection revealed 7 distinct clusters that aren't purely geographic - while regional patterns exist (like European and Asian clusters), economic and historical relationships also shape connectivity patterns. The network shows significant vulnerability to targeted attacks - removing just the top few countries by centrality can fragment the entire network into isolated components.
<img width="1367" height="969" alt="image" src="https://github.com/user-attachments/assets/ba0b6c95-4c18-4fd3-899e-fe6e28576393" />
## How It Works
The analysis uses R with several key packages:
1. igraph for network analysis and centrality calculations
2. sf for handling spatial data and country boundaries
3. leaflet for interactive mapping
4. ggplot2 for visualizations

The data comes from TeleGeography’s submarine cable database and GeoBoundaries’ country shapes. I converted the cable routes into a network with countries as nodes and cable connections as edges, and then applied standard network analysis techniques.
## Key Files
1. Full interactive report：reports/submarine-cable-network-analysis.html
2. All generated charts and maps： results/figures/
3. Raw cable and country boundary data：data/

## Running the Analysis
Clone the repository and open the RMarkdown file in RStudio. You'll need these R packages:

install.packages(c("igraph", "sf", "leaflet", "ggplot2", "dplyr", "knitr"))

The HTML report shows all results with interactive maps and reports.

## Why This Matters 
Understanding submarine cable networks is crucial for telecommunications planning, cybersecurity risk assessment, and international policy. These cables carry 99% of international data traffic, making them critical infrastructure. The analysis reveals how dependent global communications are on a small number of key countries and transit points.

-Analysis completed as part of Geographic Data Science coursework at University of Bristol
