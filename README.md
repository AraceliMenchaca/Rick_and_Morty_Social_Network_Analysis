# Rick &amp; Morty: A Social Network Analysis and Propagation Simulation
## Seasons 1 to 3

![SmithFamilyandRick](https://static1.colliderimages.com/wordpress/wp-content/uploads/2022/03/rick-and-morty-smith-family.jpg?q=50&fit=contain&w=1140&h=&dpr=1.5 "scale=0.25% max-width=10px")

## Table of Contents
- [About the Project]
- [Objective]
- [State of the Art]
- [Metodology]
- [Results]
- [Conclusion]

## About the Project
The American adult animated television series "Rick and Morty," created by Justin Roiland and Dan Harmon in 2013 for Adult Swim, has captivated a wide audience with its unique blend of science fiction, humor, and exploration of human relationships. The series follows the misadventures of Rick Sanchez, an eccentric scientist, and his impressionable grandson, Morty, as they embark on adventures across dimensions, time, and intergalactic space. This repository presents a project that uses this series as inspiration to create a social network that reflects the relationships between its characters based on their interactions and dialogues in the first three seasons. Additionally, the article simulates the unexpected spread of a virus within this network, focusing on the intricately connected secondary characters within the network structure. The project illustrates how social network analysis techniques can be applied to understand relationships and patterns in a fictional context, combining elements of data science, narrative, and entertainment.

## Objective
The main objective of the project is to create a social network that reflects the relationships between the characters of "Rick and Morty" based on their interactions and dialogues in the first three seasons. Additionally, the spread of a virus is simulated within this network, focusing on the secondary characters connected within the network structure.

## State of the Art
In the context of this project, two notable works in social network analysis were taken as references. First, it was based on the video "Network of The Witcher — Relationship Extraction Network Analysis with Spacy and NetworkX" presented by Thu Vu, which explores the relationships between the characters of the "The Witcher" saga. The analysis uses centrality measures and community detection techniques to delve deeper into the interactions within the network. Second, inspiration was taken from the project "GOTNetwork Analysis" by Harsh Jobanputra, which created a network for the characters of the series "A Song of Ice and Fire" and simulated the spread of rumors based on independent cascades. This project also explored the relevance and importance of the characters throughout the saga using specific analysis methods.

<p align="center">
  <a >
    <img alt= title= src="thuvuHarsh.png" width="450">
  </a>
</p>

## Methodology
### Dataset
The dataset is composed of three main variants: Source, Target, and Value. Source represents the characters with dialogues (speakers) in each episode of the first three seasons of "Rick and Morty". Target includes the characters mentioned in the dialogues of a speaker, while Value indicates the number of interactions between the speaker (source) and the mentioned character (target).

The dataset was obtained through web scraping from the website (http://rickandmorty.newtfire.org/transcripts.html) that hosted episode scripts from the first three seasons of "Rick and Morty". Natural language processing techniques were applied to label the characters mentioned in the dialogues. Subsequently, a network was built and centrality, closeness, intermediation, and eigenvector analyses were performed.

<p align="center">
  <a >
    <img alt= title= src="webscraping.png" width="350">
    <img alt= title= src="value.png" width="350">
    <img alt= title= src="target.png" width="350">
  </a>
</p>

### Network Construction
The network was built using the NetworkX library from the Pandas edgelist containing the three variants (source, target, value) collected in the previous phase, especially the Edge attribute that represents the connections between nodes. The Kamada-Kawai layout algorithm was selected to visualize the graph in two or three dimensions, with the aim of distributing the nodes in a way that minimizes edge crossings and system energy.

<p align="center">
  <a >
    <img alt= title= src="network.png" width="350">
  </a>
</p>

## Analysis
### Degree Centrality
The degree centrality of a node is the number of connections it has with other nodes in the network. Nodes with a high degree are considered central because they have many connections. Rick is the most central character in the "Rick and Morty" network, with the highest degree centrality (0.77). Morty, despite being the second main character, has fewer connections within the network (0.24). Surprisingly, Jerry has the second highest degree centrality (0.47) followed by Summer (0.37) and Beth (0.31).

### Closeness Centrality
The Closeness Centrality is a measure that evaluates the relative importance of a node based on its accessibility and proximity to other nodes in the network. Rick has the best closeness (0.81) in the "Rick and Morty" network, indicating his high accessibility and proximity to other characters. The rest of the Smith-Sanchez family follows, with Jerry (0.65), Summer (0.61), Beth  (0.59), and Morty (0.56)in decreasing order.

### Betweenness Centrality
Betweenness Centrality is a measure used in network analysis to evaluate the relative importance of a node as an intermediary in communication or information flows between nodes in the network. In the "Rick and Morty" network, Rick, Jerry, Summer, Beth, and Morty have the highest Betweenness Centrality, acting as important intermediaries in communication and information flows. Principal follows, with other secondary characters and Jessica trailing behind.

### Eigenvector Centrality
Eigenvector centrality is a measure used in network analysis to evaluate the relative importance of a node based on its connections to other influential nodes in the network.In the "Rick and Morty" network, Rick, Jerry, Summer, Beth, and Morty have the highest eigenvector centrality, indicating their importance based on connections to influential characters. Goldenfold, Jessica, and Principal follow as the secondary characters with the best connections to the main characters.

<p align="center">
  <a >
    <img alt= title= src="goldenfold.png" width="350">
    <img alt= title= src="principal.png" width="350">
    <img alt= title= src="jessica.png" width="350">
  </a>
</p>
