Exploring a set of 100,000 Wikipedia documents, in which each line consists of the plain text extracted from an individual Wikipedia document. On AWS VM instances:

1. Configure and run a stable release of Apache Hadoop in the pseudo-distributed mode.
2. Develop a MapReduce-based approach in your Hadoop system to compute the relative frequencies of each word that occurs in all the documents in 100KWikiText.txt, and output the top 100 word pairs sorted in a decreasing order of relative frequency. The relative frequency (RF) of word B given word A is defined as RF(B|A) = count(A,B) / count(A), where count(A,B) is the number of times A and B co-occur in the entire document collection, and count(A) is the number of times A occurs with anything else. Intuitively, given a document collection, the relative frequency captures the proportion of time the word B appears in the same document as A.
3. Repeat the above steps using at least 2 VM instances in your Hadoop system running in the fully-distributed mode.

   
**It is not meaningful to consider a word (A) that appears rarely in the entire document. Hence, you need to first rank all words according to their use frequencies (using WordCount) and then consider only top 100 words for the RF calculation of their pairs.


Commands.txt - text file that lists all the commands you used to run your code and produce the required results in both pseudo and fully distributed modes
Top100.txt - text file that stores the final results (only the top 100 word pairs sorted in a decreasing order of relative frequency)
CalculateRelativeFrequency Java.txt, CalculateTop100 Java.txt, wc.jar  -The source code of your MapReduce solution (including the JAR file)
Algorithm.txt - text file that describes the algorithm you used to solve the problem
Settings.txt - text file that describes:
  the input/output format in each Hadoop task, i.e., the keys for the mappers and reducers
  the Hadoop cluster settings you used, i.e., number of VM instances, number of mappers and reducers, etc.
  the running time for your MapReduce approach in both pseudo and fully distributed modes


