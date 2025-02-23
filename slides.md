---
theme: apple-basic
title: Introduction to Bioinformatics
transition: slide-left
author: Manish Datt
browserExporter: dev
download: false
layout: statement 
---

# Introduction to Bioinformatics
<style>
h1 {
    background: linear-gradient(to right, #8b5cf6, #06b6d4, #ec4899);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
	}
</style>

<div  class="pt-8">
<h2 class="text-gray-500">Manish Datt</h2>
</div>
<div class="place-items-center">
<img class="pt-20" src="./images/logo_final_transparent.png" width=5% />
</div>

---
transition: fade-out
---

# What is Bioinformatics

<div class="grid grid-cols-2 grid-rows-[auto,1fr] h-full">
  <div class="p-4">
  <figure>
<img src="./images/paulien.jpg" width=65% />
<figcaption><a href="https://ubc.uu.nl/introduction-50-years-bioinformatics/">Paulien Hogeweg</a></figcaption>
</figure>
</div>
  <div class="p-4">
  <figure>
<img src="./images/ben_hesper.jpg" width=30% />
<figcaption><a href="https://ubc.uu.nl/introduction-50-years-bioinformatics/">Ben Hesper</a></figcaption>
</figure>
</div>

</div>

<div v-click class="text-center">
<h2> The study of informatic processes in biotic systems. </h2>
</div>

<div>
<p v-click>
Life is information processing in its various forms, e.g., information accumulation during evolution, information transmission from DNA to intra- and intercellular processes, and the interpretation of such information at multiple levels. 
</p>
<p v-click>
<span v-mark.box.orange="4"> Information processing </span>could serve as a useful metaphor for understanding living systems. Therefore, in addition to <span v-mark.underline.orange="5">bio</span>physics and <span v-mark.underline.orange="5">bio</span>chemistry, it was useful to distinguish <span v-mark.highlight.orange="6">bioinformatics</span> as a research field.
</p>
</div>

---
transition: slide-left
---

# What is Bioinformatics

<br>

<br>

<p v-click class="text-3xl" style="line-height:1.5em;"> Put simply, bioinformatics is the science of <span v-mark.underline.orange="2">storing, retrieving</span> and <span v-mark.underline.blue="3">analyzing</span> <span v-mark.underline.green="4">large amounts</span> of <span v-mark.underline.purple="5">biological information.</span></p>

<br>

<p v-after class="text-sm text-right"><a href="https://www.ebi.ac.uk/training/online/courses/bioinformatics-terrified/what-bioinformatics/">ebi.ac.uk</a></p>
<!-- <img src="https://media.springernature.com/w440/springer-static/cover-hires/journal/41586/409/6822" width=30% /> -->

---
transition: fade-out
hide: true
---

# Central Dogma

<div class="items-center text-center text-2xl">
<button class="border-2 border-blue-500 rounded-lg px-2" @click="showDiv('CD_DNA')">DNA</button> <carbon:arrow-right /> <button class="border-2 border-blue-500 rounded-lg px-2" @click="showDiv('CD_RNA')">RNA</button> <carbon:arrow-right /> <button class="border-2 border-blue-500 rounded-lg px-2" @click="showDiv('CD_PROTEIN')">Protein</button>
</div>

<div :class="{ hidden: activeDiv !== 'CD_DNA' }" class="CD_DNA">
<div v-click>
Genomics
</div>
<div v-click>
Genome annotation, Comparative genomics, Genome-wide association studies
</div>
</div>

<div :class="{ hidden: activeDiv !== 'CD_RNA' }" class="CD_RNA">
<div v-click>
Transcriptomics
</div>
<div v-click>
RNA-seq, DGE, ncRNA, RNA structure prediction, RNA design
</div>
</div>

<div :class="{ hidden: activeDiv !== 'CD_PROTEIN' }" class="CD_PROTEIN">
<div v-click>
Proteomics
</div>
<div v-click>
functional annotation, structure prediction, PPI, PTMs,
</div>
</div>

<div v-click>
sequencing, phylogenetics, metagenomics, epigenomics,
</div>

<script setup>
import { ref } from 'vue';

const activeDiv = ref(null);

function showDiv(divId) {
  activeDiv.value = divId;
}
</script>

---
transition: fade-out
---

# Central Dogma

<div class="items-center text-center text-2xl">
<button class="border-2 border-blue-600 rounded-lg px-2">DNA</button> <carbon:arrow-right /> <button class="border-2 border-cyan-600 rounded-lg px-2">RNA</button> <carbon:arrow-right /> <button class="border-2 border-green-600 rounded-lg px-2">Protein</button>
</div>

<div class="grid grid-cols-3 h-full">
<div class="CD_DNA">
<p v-click class="text-blue-600 text-3xl pt-4 text-center">
Genomics
</p>
<p v-click class="text-xl pt-2">
Genome annotation, Comparative genomics, Genome-wide association studies
</p>
</div>

<div class="CD_RNA">
<p v-click class="text-cyan-600 text-3xl pt-4 text-center">
Transcriptomics
</p>
<p v-click class="text-xl pt-2">
RNA-seq, DGE, ncRNA, RNA structure prediction, RNA design
</p>
</div>

<div class="CD_PROTEIN">
<p v-click class="text-green-600 text-3xl pt-4 text-center">
Proteomics
</p>
<p v-click class="text-xl pt-2">
functional annotation, structure prediction, PPI, PTMs,
</p>
</div>

</div>

<div v-click class="text-3xl pt-2 text-center font-bold">
Sequencing
</div>

<div v-click class="text-2xl pt-2 text-center">
Phylogenetics
</div>

<div v-click class="text-2xl pt-2 text-center">
Metagenomics, Epigenomics, ...
</div>


---
transition: fade-out
hide: true
---


# Why study Bioinformatics

For research
<img src="./images/Human_Genome_Science.png" width=30% />

---
transition: slide-left
---

# Biological Databases

<br>

## Online libraries that contain <span v-mark.underline.orange="1">structured information</span> about living organisms.

<v-click at="2">

<p class="text-2xl p-4" style="line-height:1.25em;">
Convenient, computable access to prior knowledge that is vital for planning <span v-mark.underline.orange="3">future experiments</span> and for discovering new knowledge through <span v-mark.box.purple="4">data mining</span>. 
</p>

</v-click>

<v-click at="5">

<p class="text-2xl p-4">
Databases can be of different types depending upon their information content.
</p>

</v-click>

<v-click at="6">

<p class="text-2xl p-4">
<a href="https://www.ncbi.nlm.nih.gov/">NCBI</a> and <a href="https://www.ebi.ac.uk/">EMBL-EBI</a> host several databases and web-servers.
</p>

</v-click>


---
transition: slide-left
---

# Biological Databases --- Nucleic Acid Research


<!-- ## <p class="text-blue-500">Nucleic Acid Research --- Databases</p>  -->


<iframe src="https://www.oxfordjournals.org/nar/database/c/" width="800" height="400"></iframe>

---
transition: slide-left
---

# Biological Databases --- Development

<figure class="text-right text-sm">
<img src="./images/Database_commons_2.jpg" />
<figurecaption><a href="https://academic.oup.com/gpb/article/21/5/1054/7632866">Database Commons</a></figurecaption>
</figure>

<br>

<p class="pt-8 text-2xl text-center" v-click>
Ten Simple Rules for Developing Public Biological Databases. <a class="text-sm" href="https://doi.org/10.1371/journal.pcbi.1005128" target="_blank">PLOS One</a>
</p>

---
transition: slide-left
hide: true
---
# NGS

https://pmc.ncbi.nlm.nih.gov/articles/PMC4633438/pdf/40142_2015_Article_76.pdf

https://web.natur.cuni.cz/~muncling/Metzker%202010%20Next%20generation%20sequencing.pdf

<button bg="blue-400" p="y-2 x-4" rounded @click="greet">Greet</button> 

<script setup>
function greet(){
	alert("HI");
}
</script>

---
transition: slide-left
---
# Next-Generation Sequencing

<div class="flex justify-center">
<iframe width="700" height="394" src="https://www.youtube.com/embed/mZA3fdKijHY?si=l_zIFbCLxS7W_1JT" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

---
transition: slide-left
---
# Next-Generation Sequencing 

<br> 

## Sequencing technology is the <span v-mark.underline.orange="1">engine</span> that powers the car that allows us to navigate the human genome roadmap.

<v-click at="+2">
<p class="text-2xl pt-8" style="line-height:1.25em;">We need the raw materials, such as <span v-mark.line.orange="3">fuel (DNA)</span>, sparks to ignite the fuel <span v-mark.line.orange="4">(reagents)</span>, mechanical parts to translate fuel and ignition into movement <span v-mark.line.orange="5">(robotics)</span> and <span v-mark.box.purple="6"> direction (bioinformatics)</span>, all working in a carefully engineered balance, and a driver (genome centre) to steer the automobile quickly and efficiently to the desired <span v-mark.line.purple="7">destination (biological understanding)</span>.
 </p>
</v-click>


<p class="text-sm text-right"><a href="https://doi.org/10.1038/nature09796">Nature (2011)</a></p>

---
transition: slide-left
hide: true
---
# Next-Generation Sequencing -- Applications

<div class="flex justify-center">
<img src="./images/NGS_applications.jpg" width=70% />
</div>
<p class="text-sm text-right"><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC10376292/">PubMed</a></p>

---
transition: slide-left
---

# Bioinformatics Education 

<p class="text-2xl">Important challenges</p>

<img v-click src="./images/Bioinfo_edu_barrier_1.png" />

<p v-after class="text-sm text-right"><a href="https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0224288">PLOS One, 2019</a></p>

---
transition: slide-left
---

# Bioinformatics Education 

<img src="./images/Bioinfo_edu_barrier_2.png" width=95% />

<p class="text-sm text-right"><a href="https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0224288">PLOS One, 2019</a></p>

---
transition: slide-left
---

# Bioinformatics Skills

<div class="flex justify-center">
<img src="./images/Bioinfo_edu_skill_1_1.png" width=80%/>
</div>

<p v-click class="text-2xl"> S1 (Role) — Understand the role of computation and data mining in hypothesis-driven processes within the life sciences </p>

<p v-click class="text-2xl"> S2 (Concepts) — Understand computational concepts used in bioinformatics, e.g., meaning of algorithm, bioinformatics file formats </p>

<p v-click class="text-2xl"> S3 (Statistics) — Know statistical concepts used in bioinformatics, e.g., E-value, z-scores, t test, type-1 error, type-2 error, employ R </p>

<p class="text-sm text-right"><a href="https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0196878">PLOS One, 2018</a></p>

---
transition: slide-left
---

# Bioinformatics Skills

<div class="flex justify-center">
<img src="./images/Bioinfo_edu_skill_1_2.png" width=40%/>
</div>
<img src="./images/Bioinfo_edu_skill_2.png"/>

<p v-click class="text-2xl">S4, S6, S8, S10 — Know how to <span v-mark.underline.orange="1">access</span> relevant data.</p>

<p v-click class="text-2xl">S5, S7, S9 — Be able to use bioinformatics tools to <span v-mark.underline.orange="2">analyze</span> relevant data.</p>

<p class="text-sm text-right"><a href="https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0196878">PLOS One, 2018</a></p>

---
transition: slide-left
---

# Bioinformatics Skills

<img src="./images/Bioinfo_edu_skill_3.png"/>

<p v-click class="text-xl">S11—Be able to use bioinformatics tools to examine the flow of molecules within pathways/networks, e.g., Gene Ontology, KEGG</p>
<p v-click class="text-xl">S12—Be able to use bioinformatics tools to examine metagenomics data, e.g., MEGA, MUSCLE</p>
<p v-click class="text-xl">S13—Know how to write short computer programs as part of the scientific discovery process, e.g., write a script to analyze sequence data</p>
<p v-click class="text-xl">S14—Be able to use software packages to manipulate and analyze bioinformatics data, e.g., Geneious, Vector NTI Express, spreadsheets</p>
<p v-click class="text-xl">S15—Operate in a variety of computational environments e.g., Mac OS, Windows, web- or cloud-based, Linux command line</p>

<p class="text-sm text-right"><a href="https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0196878">PLOS One, 2018</a></p>

---
transition: slide-left
---

# Bioinformatics Skills

<img src="./images/Bioinfo_edu_skills.png" width=80%/>

<p class="text-sm text-right"><a href="https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0196878">PLOS One, 2018</a></p>


---
transition: slide-left
---

# Bioinformatics -- Programming

<div class="grid grid-cols-2 grid-rows-[auto,1fr] h-full p-4">
  <div class="flex justify-center">
<img src="https://www.python.org/static/community_logos/python-logo-master-v3-TM.png" width=65% />
</div>
  <div class="flex justify-center">
<img src="https://www.r-project.org/logo/Rlogo.png" width=25% />
</div>
</div>

<div v-click class="grid grid-cols-2 grid-rows-[auto,1fr] h-full p-2">
  <div class="flex justify-center text-2xl">
A high-level, object-oriented programming language.
</div>
  <div class="flex justify-center text-2xl">
A language and environment for statistical computing and graphics.
</div>
</div>

<div v-click class="grid grid-cols-2 grid-rows-[auto,1fr] h-full p-2">
  <div class="text-2xl">
Libraries like Biopython for Bioinformatics analysis.
</div>
  <div class="text-2xl">
Packages like Bioconductor for bioinformatics analysis.
</div>
</div>

<div v-click class="grid grid-cols-2 grid-rows-[auto,1fr] h-full p-4">
  <div class="flex justify-center">
Ebook:&nbsp; <a href="https://pythonbook.bioinfo.guru" target="_blank"> pythonbook.bioinfo.guru</a>
</div>
  <div class="flex justify-center">
Ebook: &nbsp; <a href="https://rbook.bioinfo.guru" target="_blank"> rbook.bioinfo.guru</a>
</div>
</div>

---
transition: slide-left
---

# What is Bioinformatics

<br>

<br>

<p v-click class="text-3xl p-8" style="line-height:1.5em;">
It is a highly interdisciplinary field involving many different types of specialists, including biologists, molecular life scientists, computer scientists and mathematicians.
</p>

<br>

<p v-after class="text-sm text-right"><a href="https://www.ebi.ac.uk/training/online/courses/bioinformatics-terrified/what-bioinformatics/">ebi.ac.uk</a></p>

---
transition: slide-left
layout: statement
---

# Thank you!

<p class="text-2xl pt-8">manish@<span style="font-family: 'Geo', sans-serif; color:#9c51e0;">bioinfo.guru</span></p>
