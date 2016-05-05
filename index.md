---
layout: page
---


<h2>Workflow of RTCGA package</h2>
<img src='https://raw.githubusercontent.com/RTCGA/RTCGA/master/RTCGA_workflow_ver3.png'> 

> The Cancer Genome Atlas (TCGA) is a comprehensive and coordinated effort to accelerate our understanding of the molecular basis of cancer through the application of genome analysis technologies, including large-scale genome sequencing. 

We converted selected datasets from this study into few separate packages that are hosted on Bioconductor. These R packages make selected datasets easier to access and manage. Data sets in RTCGA.data packages are large and cover complex relations between clinical outcomes and genetic background.

These packages will be useful for at least three audiences: biostatisticians that work with cancer data; researchers that are working on large scale algorithms, for them RTGCA will be a perfect blasting site; teachers that are presenting data analysis method on real data problems.


<p>Data packages submitted to Bioconductor</p>
<ul>
<li><a href="http://bioconductor.org/packages/3.2/data/experiment/html/RTCGA.mutations.html">RTCGA.mutations</a></li>
<li><a href="http://bioconductor.org/packages/3.2/data/experiment/html/RTCGA.rnaseq.html">RTCGA.rnaseq</a></li>
<li><a href="http://bioconductor.org/packages/3.2/data/experiment/html/RTCGA.clinical.html">RTCGA.clinical</a></li>
<li><a href="http://bioconductor.org/packages/RTCGA.PANCAN12/">RTCGA.PANCAN12</a></li>
<li><a href="http://bioconductor.org/packages/RTCGA.mRNA/">RTCGA.mRNA</a></li>
<li><a href="http://bioconductor.org/packages/RTCGA.miRNASeq/">RTCGA.miRNASeq</a></li>
<li><a href="http://bioconductor.org/packages/RTCGA.RPPA/">RTCGA.RPPA</a></li>
<li><a href="http://bioconductor.org/packages/RTCGA.CNV/">RTCGA.CNV</a></li>
<li><a href="http://bioconductor.org/packages/RTCGA.methylation/">RTCGA.methylation</a></li>
</ul>
<div id="installation-of-packages-from-the-rtcga-family" class="section level3">
<h3>Installation of packages from the <code>RTCGA</code> family:</h3>
<p>Windows users: 

> Make sure you have <a href="http://cran.r-project.org/bin/windows/Rtools/">rtools</a> installed on your computer.
</p>
<pre class="r"><code># packages that are published to devel version of Bioconductor
BiocInstaller::useDevel() 
# swiches to devel branchof Bioconductor 
# - don't use this line if you are interested in release vers
source(&quot;https://bioconductor.org/biocLite.R&quot;) 
# downloads bioClite function</code></pre>
<table style="width:126%;">
<colgroup>
<col width="26%"></col>
<col width="45%"></col>
<col width="22%"></col>
<col width="31%"></col>
</colgroup>
<thead>
<tr class="header">
<th align="left">package</th>
<th align="left">installation</th>
<th align="left">help</th>
<th align="left">browseVignettes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">RTCGA.rnaseq</td>
<td align="left"><code>biocLite('RTCGA.rnaseq')</code></td>
<td align="left"><code>?rnaseq</code></td>
<td align="left"><code>'RTCGA.rnaseq'</code></td>
</tr>
<tr class="even">
<td align="left">RTCGA.clinical</td>
<td align="left"><code>biocLite('RTCGA.clinical')</code></td>
<td align="left"><code>?clinical</code></td>
<td align="left"><code>'RTCGA.clinical'</code></td>
</tr>
<tr class="odd">
<td align="left">RTCGA.mutations</td>
<td align="left"><code>biocLite('RTCGA.mutations')</code></td>
<td align="left"><code>?mutations</code></td>
<td align="left"><code>'RTCGA.mutations'</code></td>
</tr>
<tr class="even">
<td align="left">RTCGA.mRNA</td>
<td align="left"><code>biocLite('RTCGA.mRNA')</code></td>
<td align="left"><code>?mRNA</code></td>
<td align="left"><code>'RTCGA.mRNA'</code></td>
</tr>
<tr class="odd">
<td align="left">RTCGA.miRNASeq</td>
<td align="left"><code>biocLite('RTCGA.miRNASeq')</code></td>
<td align="left"><code>?miRNASeq</code></td>
<td align="left"><code>'RTCGA.miRNASeq'</code></td>
</tr>
<tr class="even">
<td align="left">RTCGA.PANCAN12</td>
<td align="left"><code>biocLite('RTCGA.PANCAN12')</code></td>
<td align="left"><code>?pancan12</code></td>
<td align="left"><code>'RTCGA.PANCAN12'</code></td>
</tr>
<tr class="odd">
<td align="left">RTCGA.RPPA</td>
<td align="left"><code>biocLite('RTCGA.RPPA')</code></td>
<td align="left"><code>?RPPA</code></td>
<td align="left"><code>'RTCGA.RPPA'</code></td>
</tr>
<tr class="even">
<td align="left">RTCGA.CNV</td>
<td align="left"><code>biocLite('RTCGA.CNV')</code></td>
<td align="left"><code>?CNV</code></td>
<td align="left"><code>'RTCGA.CNV'</code></td>
</tr>
<tr class="odd">
<td align="left">RTCGA.methylation</td>
<td align="left"><code>biocLite('RTCGA.methylation')</code></td>
<td align="left"><code>?methylation</code></td>
<td align="left"><code>'RTCGA.methylation'</code></td>
</tr>
</tbody>
</table>
<pre class="r"><code># version of packages held at github.com/RTCGA - I try to keep them with the same state as devel versions of Bioconductor
library(RTCGA)
installTCGA(&quot;RTCGA.PANCAN12&quot;)
installTCGA(&quot;RTCGA.CNV&quot;)
installTCGA(&quot;RTCGA.RPPA&quot;)
installTCGA(&quot;RTCGA.mRNA&quot;)
installTCGA(&quot;RTCGA.miRNASeq&quot;)
installTCGA(&quot;RTCGA.methylation&quot;)
# or for all just type installTCGA()</code></pre>
</div>
<div id="rtcga" class="section level1">
<h1>RTCGA</h1>
<p>Packages from the <code>RTCGA.data</code> - family/factory are based on the <code>RTCGA</code> package</p>
<div id="installation-of-the-rtcga-package" class="section level3">
<h3>Installation of the <a href="https://github.com/RTCGA/RTCGA"><code>RTCGA</code></a> package:</h3>
<p>To get started, install the latest version of <strong>RTCGA</strong> from Bioconductor:</p>
<pre class="r"><code>BiocInstaller::useDevel() # swiches to devel branch of Bioconductor
source(&quot;https://bioconductor.org/biocLite.R&quot;) # downloads bioClite function
biocLite(&quot;RTCGA&quot;) # installs a package</code></pre>
<p>or use below code to download the development version which is like to be less bugged than the release version on Bioconductor:</p>
<pre class="r"><code>if (!require(devtools)) {
    install.packages(&quot;devtools&quot;)
    require(devtools)
}
install_github(&quot;RTCGA/RTCGA&quot;, build_vignettes = TRUE)</code></pre>
<p>To check Use Cases run</p>
<pre class="r"><code>browseVignettes(&quot;RTCGA&quot;)</code></pre>
<h4>
Authors:
</h4>
<blockquote>
<p>Marcin Kosiński, <a href="mailto:m.p.kosinski@gmail.com">m.p.kosinski@gmail.com</a></p>
<p>Przemysław Biecek, <a href="mailto:przemyslaw.biecek@gmail.com">przemyslaw.biecek@gmail.com</a></p>
<p>Witold Chodor, <a href="mailto:witoldchodor@gmail.com">witoldchodor@gmail.com</a></p>
</blockquote>
</div>
</div>


