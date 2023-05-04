Download Link: https://assignmentchef.com/product/solved-csci3003-lab3-hsp90-chaperone-protein-analysis-main
<br>



<ul>

 <li>Practice Python syntax rules.</li>

 <li>Use numeric and string operations to manipulate variables.</li>

 <li>Practice file input/output operations.</li>

 <li>Combine all of the above to write your first Python script to accomplish a task.</li>

</ul>




<strong>Writing your first Python program</strong>

A protein’s biological function is determined by its physical structure, which is in turn determined by its sequence of amino acids encoded in the genome. Amino acid sequences naturally fold to form 3D structures, but this process is not perfect – misfolded proteins are sometimes created that can pose a risk to the cell. Many diseases including Huntington’s, ALS, and Alzheimer’s are associated with either genetic or environmental factors that result in an accumulation of misfolded proteins. To battle this, some genomes encode special proteins called chaperones that help proteins fold into their correct conformations and stabilize them during environmental stresses like heat shock. One of these chaperone proteins, Hsp90 (Heat shock protein 90), is extremely well conserved across the tree of life from bacteria to higher eukaryotes.

Chaperone proteins such as Hsp90 contain stretches of amino acids that are nearly perfectly conserved across large evolutionary times. Whether you look in humans, gorillas, dogs, chicken, fish, worms, or even yeast, you will find stretches of the Hsp90 protein with almost exactly the same amino acid sequence. These highly conserved regions typically include <em>domains</em>, which are short stretches of amino acids that fold into well-characterized, stable structures with specific biochemical functions. However, in addition to these highly conserved sequences associated with stable physical structure, some proteins also contain regions that take on many different conformations and do not fold into a fixed shape. These intriguing regions are called ‘disordered’, and they have been an intense area of research over the past decade as researchers try to understand the sequence properties that result in disorder and the biochemical properties that are enabled by protein disorder. The Hsp90 protein is unique in that it contains two extremely well conserved domains linked by a region that is extremely disordered. In addition to a lack of fixed structure and sequence conservation, these disordered regions have been found to have high occurrences of amino acids with special chemical properties.




The above protein model demonstrates the domain and ‘disordered’ linker regions of Hsp90. Domains are shown in green and red, and they are ‘linked’ together by the disordered region shown in gray. Notice that while the certain parts of the gene may change between organisms, there are specific regions that are highly conserved.

In this lab, we will write a program to read and analyze amino acid sequences from 268 Hsp90 orthologs across a diverse set of organisms. You will perform sequence analysis on these proteins to show that while the linker sequence between the two structural domains in Hsp90 seems to be disordered, some biochemical properties are conserved. For more background on the motivation for today’s lab, please check out the references listed at the end of the assignment.

<strong>Your task:   </strong>

We would like to measure the proportion of amino acids that are charged in the linker region of each Hsp90 ortholog. The position of this region varies in each ortholog sequence, but can be identified based on the well-conserved sequences, EYLEE and LNKTKP, near the start and the end of the disordered region, respectively. Write a script that reads in each of the 268 Hsp90 protein sequences, extracts the subsequence associated with the disordered regions, and computes the fraction of negatively and positively charged amino acids in the disordered region. Then, compute the fraction of both positively and negatively charged amino acids across the whole sequence for comparison. Finally, print all of this information to an output file and perform any necessary clean up.

We have provided a skeleton script for you with comments outlining the specific tasks for which you need to write code.

<strong>Your script should do all of the following: </strong>

<ul>

 <li>Open the sequence file and an output file called <em>txt</em>.</li>

</ul>

Note: from (2) to (8), in the skeleton script, we suggest you write the codes for processing the first sequence and then put it in “for loop”.)

<ul>

 <li>Read in the provided sequence file, <em>txt,</em> line by line, being careful to remove any newline characters.</li>

 <li>Use built in string methods to split the line by tabs into two variables: name and seq.</li>

 <li>Calculate the indices for the conserved domains: EYLEE and LNKTKP and extract the sequence between them (i.e. disordered linker sequence).</li>

 <li>One characteristic of disordered regions is that they have a high occurrence of amino acids with ‘charged’ side chains. The charge on a side chain can either be positive, negative, or neutral. Look up the Side Chain Charges for positive and negative amino acids here: <a href="https://en.wikipedia.org/wiki/Amino_acids">http://en.wikipedia.org/wiki/Amino_acids</a></li>

 <li>Calculate the percentage of amino acids <u>in the disordered region</u> that are either positively or negatively charged.</li>

 <li>For comparison, calculate the percentage of amino acids <u>in the entire sequence</u> that are either positively or negatively charged.</li>

 <li>Print out the following information about each sequence into the output file:

  <ol>

   <li>The name of the amino acid sequence taken from file.</li>

   <li>Percentage of positively charged amino acids in the disordered region.</li>

   <li>Percentage of negatively charged amino acids in the disordered region.</li>

   <li>Length of disordered region.</li>

   <li>Percentage of positively charged amino acids in the whole sequence.</li>

   <li>Percentage of negatively charged amino acids in the whole sequence.</li>

  </ol></li>

</ul>

<strong>Please output one line of information per sequence, separating the properties of the sequence with tabs (a tab-delimited table). In addition, the first line of the file should contain the column titles. </strong>

<ul>

 <li>Perform any necessary I/O cleanup.</li>

</ul>







<strong>Follow-up questions: </strong>(please include answers in your script or in a separate document)

<ul>

 <li>Are there differences in the fraction of charged amino acids in the linker region relative to the rest of the protein? What are they?</li>

 <li>How consistent is this property across the 268 Hsp90 orthologs?</li>

</ul>

<strong>Optional extension: (1 extra credit point)</strong>

When reading data in from an outside source, it isn’t always guaranteed to be “clean”. For example, in the case above, one thing that might have gone wrong would be a sequence that did not contain the conserved domains. Add a statement in your script above that will catch this case and skip over sequences not containing the conserved domains.


