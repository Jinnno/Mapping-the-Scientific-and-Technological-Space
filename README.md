# Mapping Firms’ Scientific and Technological Spaces:  

This repository contains our existing implementation of Hierarchical Dirichlet Processes (HDP; Teh et al., 2006), an unsupervised topic modeling algorithm that identifies latent knowledge areas in large-scale text corpora. The algorithm represents each document as a weighted distribution across topics, enabling researchers to map the knowledge landscape and construct empirical measures of knowledge diversity, positions, distances, and movements.

Building on this implementation, we plan to extend our framework using embedding- and LLM-based topic modeling approaches, including BERTopic, the Embedded Topic Model (ETM), and TopicGPT. We aim to apply these methods to firms’ scientific publications and patents to map their positions and movements within scientific and technological knowledge spaces, as well as the relationships between them.

Our existing HDP implementation uses USPTO patent data from PatentsView (data download). The proposed extension will also incorporate scientific publication data from OpenAlex.

**Output files:**

(1) assignee_hhi_diversification_measures.csv (available at https://www.dropbox.com/scl/fi/gp5hfsyl0dcvffg8omc7n/assignee_hhi_diversification_measures.csv?rlkey=kk122ijyndp0b80zsoniep8z1&st=9sznxubh&dl=0): This file contains the HDP- and CPC-based Herfindahl-Hirschman index (HHI) diversification measures for each USPTO assignee in each year between 1976 and 2019 
- hhi_hdp: the HDP-based HHI concentration measure
- hhi_diversity_hdp: the HDP-based HHI diversification measure (i.e., 1-hhi_hdp)
- hhi_cpc: the CPC-based HHI concentration measure
- hhi_diversity_cpc: the CPC-based HHI diversification measure (i.e., 1-hhi_cpc)

(2) doc_topics.csv (available at https://www.dropbox.com/scl/fi/wgu93pqf34428u929lb5z/doc_topics.csv?rlkey=8ey9l6c64uxj5tcinep2gulhg&st=k0r7c70l&dl=0): This file contains the topic distribution for USPTO patents between 1976 and 2019
- Document ID: USPTO patent id
- Topic No: HDP-generated topics assigned to each patent
- Probability: Topic probability 

(3) topics.csv (available at: https://www.dropbox.com/scl/fi/wr6am5xcz5g6yqmj1l5wf/topics.csv?rlkey=np2fonamtymz8a35l6u0iecg8&st=flwkryow&dl=0): This file contains the word distribution for the HDP-generated topics

(4) topic_similarity.csv (available at https://www.dropbox.com/scl/fi/qh9l02cd5hrc0w2pzkjid/topic_similarity.csv?rlkey=3czvvi0famebxx580qae0cfxm&st=he55k4sw&dl=0): This file contains the pairwise weighted cosine similarity between the HDP topics
