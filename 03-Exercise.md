# EXERCISE 3 – THE EVOLUTIONARY HISTORY OF YEAST

Saccharomyces is a genus of fungi that has been cultivated extensively by humans. They are used in fermentations, such as in pastry and bread dough, as well as in alcohol production, such as beer. Its most prominent species, *Saccharomyces cerevisiae*, is one of the most well-researched organisms on the planet. As such, this genus has been thoroughly studied, and genomic data exist for many of its species.

Here, we will evaluate the phylogeny of yeast species using a 18S rRNA phylogeny, and using bootstrap pseudoreplicates as a methodology to assess the robustness of the results.

**Bootstrap pseudoreplicates.** To illustrate how this method works, find below a multiple sequence alignment (MSA) consisting of protein sequences from 7 species with a length of 16 amino acids. Next to it, the phylogenetic tree made from this alignment. Below, ten reshuffled versions (bootstrap pseudoreplicates) of the MSA, and the corresponding trees.

&lt;img&gt;Multiple sequence alignment and phylogenetic tree&lt;/img&gt;

<table>
  <thead>
    <tr>
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
      <th>E</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>&lt;img&gt;Tree A&lt;/img&gt;</td>
      <td>&lt;img&gt;Tree B&lt;/img&gt;</td>
      <td>&lt;img&gt;Tree C&lt;/img&gt;</td>
      <td>&lt;img&gt;Tree D&lt;/img&gt;</td>
      <td>&lt;img&gt;Tree E&lt;/img&gt;</td>
    </tr>
    <tr>
      <td>&lt;img&gt;Sequence A&lt;/img&gt;</td>
      <td>&lt;img&gt;Sequence B&lt;/img&gt;</td>
      <td>&lt;img&gt;Sequence C&lt;/img&gt;</td>
      <td>&lt;img&gt;Sequence D&lt;/img&gt;</td>
      <td>&lt;img&gt;Sequence E&lt;/img&gt;</td>
    </tr>
  </tbody>
</table>

<table>
  <thead>
    <tr>
      <th>F</th>
      <th>G</th>
      <th>H</th>
      <th>I</th>
      <th>J</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>&lt;img&gt;Tree F&lt;/img&gt;</td>
      <td>&lt;img&gt;Tree G&lt;/img&gt;</td>
      <td>&lt;img&gt;Tree H&lt;/img&gt;</td>
      <td>&lt;img&gt;Tree I&lt;/img&gt;</td>
      <td>&lt;img&gt;Tree J&lt;/img&gt;</td>
    </tr>
    <tr>
      <td>&lt;img&gt;Sequence F&lt;/img&gt;</td>
      <td>&lt;img&gt;Sequence G&lt;/img&gt;</td>
      <td>&lt;img&gt;Sequence H&lt;/img&gt;</td>
      <td>&lt;img&gt;Sequence I&lt;/img&gt;</td>
      <td>&lt;img&gt;Sequence J&lt;/img&gt;</td>
    </tr>
  </tbody>
</table>

These trees indicate that some groupings are more robust than others. For instance, all trees agree that clades (s1,s2,s3) and (s4,s5,s6,s7) are separate. But topologies within these clades are less clear. For example, 5 trees indicate that s2 and s3 cluster together, 4 that s1 and s2 cluster together, and 1 that s1 and s3 cluster together.

---


## Page 6

a. A group of researchers used a protein sequence from five *Saccharomyces* species to perform a phylogenetic analysis, including a bootstrap analysis such as the one above. Find below the different topologies that were obtained. Draw the most likely tree with bootstrap values based on these results.

&lt;img&gt;Phylogenetic trees showing different topologies for five Saccharomyces species. The first tree has 72 trees, the second has 19 trees, the third has 8 trees, and the fourth has 1 tree.&lt;/img&gt;

b. Let’s now perform a phylogenetic reconstruction of 18S rRNA sequences. First, take a look at the alignment. How many sequences are there? How many positions? Is there any sequence with less information than the rest? How conserved is the alignment?

c. Now, let’s reconstruct a tree. To do this, use the software IQTree. Download the Linux (or Mac) version of the software from http://www.iqtree.org/#download. After decompressing, you should be able to run the software directly, or you may need to change the ‘mode’ of this file so your computer recognises it as an executable (use the command “chmod u+x $FILE” by replacing “$FILE” with the name of the executable file within the bin folder. Now you can reconstruct your own tree. We will use the following command (replace “$ALIGNMENT” with your alignment file):

```
iqtree -s $ALIGNMENT -m GTR+G -b 100 -wbt -pre yeast
```

This reconstruction will use the evolutionary model “GTR+G”, run 100 bootstrap pseudorreplicates, which it will write to a file (-wbt = write bootstrap), and generate files with the prefix “yeast”.

i. Why are we using the evolutionary model “GTR+G”?

ii. Look at the iqtree file (“yeast.iqtree”). What information can you extract from the “Sequence alignment” section?

iii. Now look at the tree in the “Maximum likelihood tree” section. First, is this tree rooted or unrooted?

iv. How does this tree compare with the consensus tree obtained above? Are the trees compatible?

v. Assuming that the root in your trees lie in the same location as in the tree above (between the group formed by *S. bayanus* and *S. uvarum*, and everything else), and based on bootstrap values, how often do *S. cerevisiae*, *S. cariocanus* and *S. paradoxus* form a monophyletic group?

vi. How many bootstrap trees contain the monophyletic group formed by these three species, but with a different topology for this clade? What are the possible alternative topologies?
