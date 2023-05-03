Download Link: https://assignmentchef.com/product/solved-cs2040s-recitation-5
<br>
<h1>Problem 1.          (Heights and Grades)</h1>

Suppose you are given a set of students with heights and grades as follows:

<table width="286">

 <tbody>

  <tr>

   <td width="64"><strong>Name</strong></td>

   <td width="106"><strong>Height (cm)</strong></td>

   <td width="116"><strong>Grade (CAP)</strong></td>

  </tr>

  <tr>

   <td width="64">Charles</td>

   <td width="106">176</td>

   <td width="116">4.2</td>

  </tr>

  <tr>

   <td width="64">Bob</td>

   <td width="106">162</td>

   <td width="116">4.5</td>

  </tr>

  <tr>

   <td width="64">Mary</td>

   <td width="106">180</td>

   <td width="116">3.6</td>

  </tr>

  <tr>

   <td width="64">John</td>

   <td width="106">155</td>

   <td width="116">4.1</td>

  </tr>

  <tr>

   <td width="64">Wick</td>

   <td width="106">186</td>

   <td width="116">5.0</td>

  </tr>

  <tr>

   <td width="64">Alice</td>

   <td width="106">170</td>

   <td width="116">3.9</td>

  </tr>

 </tbody>

</table>

Your goal is to implement an Abstract Data Type (ADT) to efficiently answer the question: “What is the average grade of all students taller than ?”. For instance, the average grade of all students taller than John is (4<em>.</em>2 + 4<em>.</em>5 + 3<em>.</em>6 + 5<em>.</em>0 + 3<em>.</em>9)<em>/</em>5 = 4<em>.</em>24.

More specifically, the ADT specifications are as follows:

<table width="623">

 <tbody>

  <tr>

   <td width="249"><strong>Operation</strong></td>

   <td width="374"><strong>Behaviour</strong></td>

  </tr>

  <tr>

   <td width="249">insert(name, height, grade)</td>

   <td width="374">Inserts student into the dataset.</td>

  </tr>

  <tr>

   <td width="249">findAverageGrade(name)</td>

   <td width="374">Returns the average grade among all the students that are taller than the given student.</td>

  </tr>

 </tbody>

</table>

<strong>Problem 1.a. </strong>How do you capture the information of each student? What should the data type for each of their attributes be?

<strong>Problem 1.b.    </strong>How do you design a Data Structure (DS) that serves as an efficient implementation of the given ADT? You may assume that name and height are unique.

<strong>Problem 1.c. </strong>What if height is now not unique? What issue(s) will arise from this? How might you modify your solution in the previous part to resolve the issue(s)?

<h1>Problem 2.           (A Game of Cards)</h1>

Suppose you have a deck of <em>n </em>cards and they are spread out in front of you on the table from left to right with each card indexed from <em>i </em>to <em>n</em>. Each card can either be facing up or down. We are tasked to implement an ADT for a magic trick with the following specification:

<table width="623">

 <tbody>

  <tr>

   <td width="133"><strong>Operation</strong></td>

   <td width="491"><strong>Behaviour</strong></td>

  </tr>

  <tr>

   <td width="133">query(i)</td>

   <td width="491">Return whether card at index i is facing up or down.</td>

  </tr>

  <tr>

   <td width="133">turnOver(i, j)</td>

   <td width="491">Turn over all cards in the subsequence specified by the index range [i<em>,</em>j].</td>

  </tr>

 </tbody>

</table>

<strong>Problem 2.a. </strong>Given <em>n </em>cards already laid out on the table, how do you design a DS that implements such an ADT? Can you achieve turnOver in <em>O</em>(log<em>n</em>) time <em>regardless </em>of the length of subsequence to be turned over? What a magic trick indeed to be able to achieve that!

<h1>Problem 3.          (Drug Discovery)</h1>

In the bid to find a potential cure for the <a href="https://en.wikipedia.org/wiki/2019_novel_coronavirus">COVID-19</a><a href="https://en.wikipedia.org/wiki/2019_novel_coronavirus">,</a> research labs around the world are racing to study the effects different drugs have on the coronavirus. Viruses respond to drugs via <em>mutations</em>. A mutation occurs when there are changes (often small subsequences) along the original genome sequence. Suppose you now work for an international bioinformatics organization which maintains a huge open-access and canonical DNA databank (e.g. <a href="https://www.ncbi.nlm.nih.gov/genbank/">GenBank</a><a href="https://www.ncbi.nlm.nih.gov/genbank/">)</a>. Your organization is supporting the drug discovery effort by not only releasing the canonical sequence of the virus to labs all over the world, but also delivering it in a special format that would efficiently facilitate the comparisons between different mutations. In this way, all a research lab needs to do is to first download a local copy of the canonical unmutated sequence (in the special format), update it with the mutations from their experimental results, then quickly compare it with the mutated sequence from another lab which ran a different drug experiment. The mutational differences and similarities of the virus in response to different drugs reveal important drug properties to scientists, which in turn help them formulate more effective drugs.

In its raw format (i.e. before special formatting), a virus genome sequence is presented as a list of records where each record contains a subsequence of 60 characters with each character representing a nitrogenous base (e.g. Adenine, Guanine, Cytosine, Thymine). This is illustrated in Table 1 below.

<table width="595">

 <tbody>

  <tr>

   <td width="82"><strong>Record#</strong></td>

   <td width="513"><strong>Subsequence</strong></td>

  </tr>

  <tr>

   <td width="82">1</td>

   <td width="513">AAAGGTTTAT ACCTTCCCAG GTAACAAACC AACCAACTTT CGATCTCTTG TAGATCTGTT</td>

  </tr>

  <tr>

   <td width="82">2</td>

   <td width="513">CTCTAAACGA ACTTTAAAAT CTGTGTGGCT GTCACTCGGC TGCATGCTTA GTGCACTCAC</td>

  </tr>

  <tr>

   <td width="82">3</td>

   <td width="513">GCAGTATAAT TAATAACTAA TTACTGTCGT TGACAGGACA CGAGTAACTC GTCTATCTTC</td>

  </tr>

  <tr>

   <td width="82">4</td>

   <td width="513">TGCAGGCTGC TTACGGTTTC GTCCGTGTTG CAGCCGATCA TCAGCACATC TAGGTTTCGT</td>

  </tr>

  <tr>

   <td width="82">5</td>

   <td width="513">CCGGGTGTGA CCGAAAGGTA AGATGGAGAG CCTTGTCCCT GGTTTCAACG AGAAAACACA</td>

  </tr>

  <tr>

   <td width="82"><em>…</em></td>

   <td width="513"><em>… … … … … …</em></td>

  </tr>

 </tbody>

</table>

<strong>Table 1: </strong>Source: <a href="https://www.ncbi.nlm.nih.gov/nuccore/LC522972">Severe acute respiratory syndrome coronavirus 2 2019-nCoV/Japan/KY/V-029/2020 </a><a href="https://www.ncbi.nlm.nih.gov/nuccore/LC522972">RNA, complete genome</a>

As the chief of data in the organization, you are tasked to design the special format which would make comparisons between 2 genome sequences efficient. Having been a former student of CS2040S, you know that the “special format” necessarily entails a clever DS that is well-suited for the comparison operation.

<strong>Problem 3.a. </strong>Design a tree-based DS that can capture a list of <em>n </em>records (i.e a genome sequence) such that when given the tree for another list (i.e a mutated sequence), you can <em>efficiently </em>(read: better than <em>O</em>(<em>n</em>) time) determine which are their records that differ from one another.