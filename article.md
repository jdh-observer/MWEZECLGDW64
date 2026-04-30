---
jupyter:
  jupytext:
    formats: ipynb,md
    text_representation:
      extension: .md
      format_name: markdown
      format_version: '1.3'
      jupytext_version: 1.19.1
  kernelspec:
    display_name: Python 3 (ipykernel)
    language: python
    name: python3
---

<!-- #region tags=["title"] -->
# Aligning Technology with Pedagogical Goals: Digital Public History, Content Management Systems, and Minimalist Frameworks
<!-- #endregion -->

<!-- #region tags=["contributor"] -->
 ### Christopher Thomas Goodwin [![orcid](https://orcid.org/sites/default/files/images/orcid_16x16.png)](https://orcid.org/0000-0003-0723-6369) 
University of Florida
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["copyright"] -->
[![cc-by](https://licensebuttons.net/l/by/4.0/88x31.png)](https://creativecommons.org/licenses/by/4.0/) 
©<Christopher Thomas Goodwin>. Published by De Gruyter in cooperation with the University of Luxembourg Centre for Contemporary and Digital History. This is an Open Access article distributed under the terms of the [Creative Commons Attribution License CC-BY](https://creativecommons.org/licenses/by/4.0/)

<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["keywords"] -->
Pedagogy, Scalar, ScholarMinPub, minimalist, CMS
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["abstract"] -->
This article examines how platform choice shapes digital public history pedagogy by comparing two semester-long teaching experiments. The first used Scalar, a feature-rich content management system (CMS) offering polished, public-facing projects but requiring about 43% of class time for technical training. The second used ScholarMinPub, a minimalist framework adapted from SourceLab’s MinDoc, which trades aesthetic flexibility for transparency, lower infrastructure costs, and broader accessibility. It required only 20% of class time and fostered stronger student ownership while introducing transferable web skills. The study argues tool selection should align with course goals, student backgrounds, and institutional constraints, balancing technical skill development with historical content. It highlights ethical and practical considerations, advocating intentional, critical adoption of digital tools to enhance both pedagogy and inclusivity in historical scholarship.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} -->
## Introduction
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} -->
More than ever, new job postings for history faculty in the United States emphasize applicants’ digital skills. Few call specifically for “digital historians,” but rather couch the preference as a significant complement to traditional areas of expertise. Hiring committees still prioritize historians with expertise in a specific nation-state or thematic area, yet digital skills are now widely recognized as a strategic imperative for two reasons. First, the changing American political landscape has intensified the need for public outreach, serving audiences eager for history but vulnerable to oversimplified political narratives. Second, declining humanities enrollments have placed some departments in struggles for their very existence. Building a faculty cohort with digital skills allows departments to demonstrate relevance in terms familiar to STEM disciplines: graduates leave with tangible, marketable competencies. The ability to critically think or closely read texts, the mainstays of history pedagogy, are appreciated, but without accompanying digital skills are a hard-sell to employers in a world where nearly every workplace runs on computer networks, databases, and applications. Pedagogical potential rather than digitally-focused research agendas drives much of the hiring in the field of digital history in the American academy.
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"meuwe": [{"id": "4951909/48VB3VBE", "source": "zotero"}], "spof5": [{"id": "4951909/ICSTWWRP", "source": "zotero"}]}} editable=true slideshow={"slide_type": ""} -->
Only recently has pedagogy occupied such a preeminent position in the hiring process. A little over a decade ago, Katherine D. Harris’s call for pedagogy to be central to the digital humanities, delivered at the seminal 2011 Modern Language Association Convention, barely registered a blip compared to discussions of cultural criticism or, especially, the prestige of coding (<cite id="spof5"><a href="#zotero%7C4951909%2FICSTWWRP">(Croxall and Jakacki 2023)</a></cite>). The humanities—and especially the digital humanities—has not been immune to the prestige of code and the “engineer” figure that dazzles with distant reading and machine learning toolsets, though a number of historians have critiqued many of these techniques, especially when they have originated from disciplines such as Information Science (<cite id="meuwe"><a href="#zotero%7C4951909%2F48VB3VBE">(Guldi 2023)</a></cite>). To some historians, machine learning models resemble opaque “black boxes” where statistics displaces close-reading and operates at a scale that defies comprehension. Given the historical misuse of statistics, many historians are wary of layers—human, code, and machine—that push them further from primary sources. The discipline has long defended the integrity of direct, critical engagement with evidence.
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"a208h": [{"id": "4951909/ZVWDRAGM", "source": "zotero"}], "aqc0x": [{"id": "4951909/B99NN5IV", "source": "zotero"}], "bdmr6": [{"id": "4951909/WJYK4N8X", "source": "zotero"}], "diz59": [{"id": "4951909/I2BN9IN6", "source": "zotero"}], "h9yyt": [{"id": "4951909/4TG9B4GK", "source": "zotero"}], "oaddn": [{"id": "4951909/ICSTWWRP", "source": "zotero"}], "pcjan": [{"id": "4951909/IE66EGIT", "source": "zotero"}], "rp309": [{"id": "4951909/EDFDI9UE", "source": "zotero"}]}} editable=true slideshow={"slide_type": ""} -->
Curiously—or perhaps not—far fewer works have appeared in the area in which digital history can prove most transformative and positively affect the largest number of people. Digital pedagogy in practice remains an understudied area in 2025 despite a number of recent notable interventions such as Johanna Drucker’s _The Digital Humanities Coursebook_, Jennifer Guilianos’s _A Primer for Teaching Digital History_, and Brian Croxall’s and Diane Jakacki’s _What We Teach When We Teach DH_ (<cite id="diz59"><a href="#zotero%7C4951909%2FI2BN9IN6">(Drucker 2021)</a></cite>, <cite id="aqc0x"><a href="#zotero%7C4951909%2FB99NN5IV">(Guiliano 2022)</a></cite>, <cite id="oaddn"><a href="#zotero%7C4951909%2FICSTWWRP">(Croxall and Jakacki 2023)</a></cite>). The coding side of pedagogy has also recently flourished with articles from _Programming Historian_, Brian Kokensparger’s _Guide to Programming for the Digital Humanities_, Folgert Karsdorps’s _Humanities Data Analysis_, and William Mattingly’s _Introduction to Python for Digital Humanists_, although these all double as self-study manuals for researchers themselves in addition to pre-packaged lessons for the classroom (<cite id="bdmr6"><a href="#zotero%7C4951909%2FWJYK4N8X">(Kokensparger 2018)</a></cite>, <cite id="pcjan"><a href="#zotero%7C4951909%2FIE66EGIT">(Karsdorp, Kestmont, and Riddell 2021)</a></cite>, <cite id="h9yyt"><a href="#zotero%7C4951909%2F4TG9B4GK">(Mattingly 2023)</a></cite>). The recent artificial intelligence boom also inspired José Antonio Bowen’s and C. Edward Watson’s _Teaching with AI_, a timely intervention aimed at instructors confronting the disruptive potential of large language models (<cite id="rp309"><a href="#zotero%7C4951909%2FEDFDI9UE">(Bowen and Watson 2024)</a></cite>). Though this recent spate of books on educational practice bodes well for those looking to integrate the digital and the history, Maria Georgopoulou noted in her systematic study of digital humanities research literature that “there is a noticeable lack of reviews in the field of DH educational practice” and that “teaching may often be relegated to an afterthought in DH discourse.” (<cite id="a208h"><a href="#zotero%7C4951909%2FZVWDRAGM">(Georgopoulou et al. 2025)</a></cite>) The field is maturing, but not nearly at the pace of technological change.
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"093hk": [{"id": "4951909/B99NN5IV", "source": "zotero"}]}} editable=true slideshow={"slide_type": ""} -->
At least part of the issue boils down to finding concrete ways to integrate digital practices in history courses. Computationally intensive methods remain difficult to teach because both students and instructors often lack backgrounds in statistics or programming. Staying abreast of the developments in digital history has become a full time area of research, which is an impossibility for most time-strapped historians working in a field that continues to privilege the monograph and traditional subject expertise. Digital methods now form a specialized field requiring sustained effort to master, yet professional incentives remain aligned with conventional outputs. On the teaching side, historians who do emphasize the “digital” half of digital history often find that computational approaches require a two- or three-course sequence to build disciplinary skills and apply them to historical work—possible only with sustained student engagement and strong institutional support. Introductory courses can showcase what is possible, but are often “tightly controlled and limit students to approaches that do not require coding, programming, or too much under-the-hood poking around” (<cite id="093hk"><a href="#zotero%7C4951909%2FB99NN5IV">(Guiliano 2022)</a></cite>).
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"37inl": [{"id": "4951909/B99NN5IV", "source": "zotero"}], "nwslr": [{"id": "4951909/SU2NHYZG", "source": "zotero"}]}} editable=true slideshow={"slide_type": ""} -->
Digital public history offers a different balance, integrating technical skills, pedagogical goals, and the core competencies of the historical discipline. It provides space in the classroom for the “fundamentals of historical scholarship, evidence, and argument” along with important areas of scholarship such as “access, audience, output, and privacy” that receive less attention (<cite id="37inl"><a href="#zotero%7C4951909%2FB99NN5IV">(Guiliano 2022)</a></cite>). The aim is not to treat digital history pedagogy as a humanistic offshoot of computer science that trains students in particular tools or platforms, but as a “pedagogical approach that enables them to envision a relationship between themselves and knowledge production” (<cite id="nwslr"><a href="#zotero%7C4951909%2FSU2NHYZG">(Risam 2019)</a></cite>). As useful as the traditional academic essay is for teaching critical thinking and argumentation, students sometimes find it hard to shake the knowledge that only the instructor will ever read their words. Digital public history, however, produces something tangible that a student—and friends, family, the public—can visit, scroll, and interact with. Suddenly the student’s words, design choices, and multimedia selection have power and influence. Crucially, the low-bar of technical skills required, at least in the classroom, make a public-facing digital history project very suitable for a semester-long course that scaffolds technical and historical skills to create sustained engagement over several months and results in a tangible project they can carry with them after the semester ends.
<!-- #endregion -->

Pedagogical practice in digital public history, however, is not as simple as selecting a platform and turning students loose. Broad pronouncements on the importance of digital history fill the pages of pedagogy literature, but in far shorter supply are concrete pedagogical techniques and how an instructor can successfully wade through the myriad of options available to arrive at suitable tools. This article argues that there is no universal, ready-made solution for integrating digital history into the classroom. Instead, instructors must make deliberate choices based on their own and their students’ technical skills, the amount of class time available for skill development, and the broader learning objectives.


This study compares two such choices. The first involves using a conventional comprehensive Content Management System approach in the form of Scalar, a popular open-source system primarily focused on a “What-You-See-Is-What-You-Get” (WYSIWYG) editing and publishing environment with a polished final product. The second uses ScholarMinPub, an open-source minimalist framework that introduces students to Markdown and YAML, trading aesthetic flexibility for greater transparency and technical engagement. Drawing on classroom experience with both approaches, the article concludes with guidance for aligning technological choices with pedagogical and student goals, and reflects on how the subsequent end of support for Scalar underscores the importance of long-term sustainability in platform selection


### The Pedagogical Context


The two case studies examined here emerged from four upper-division undergraduate history courses taught at two institutions. The first approach, using Scalar, was implemented in Digital Documentary Publishing at the University of Illinois in Fall 2023 (20 students) and in Digital Public History at the University of Florida in Spring 2025 (21 students). The second approach, using ScholarMinPub, was implemented in Nineteenth-Century Europe (35 students) and The Second World War through Digital History (41 students), both at the University of Florida. In all four courses, students were primarily history undergraduates and virtually all entered the class with technical experience largely limited to standard office software such as Microsoft Office. In each case, students worked collaboratively in groups of four to five to produce digital exhibits based on course material and historical research.


The technical environment differed between the two approaches. In the Scalar courses, students worked on their own laptops, as the platform did not offer adequate mobile support. In the ScholarMinPub courses, students edited projects through GitHub’s web-based Markdown editor and file system; most used laptops, though some also worked on iPads and occasionally made minor edits on smartphones. All coursework was completed in ordinary classrooms rather than computer labs. Although these courses shared the pedagogical aim of having students create digital exhibits from historical research and course material, their differing technical conditions make them comparable case studies in teaching digital public history. In each case, students successfully completed public-facing digital exhibits.


## Case Study 1: Comprehensive Content Management System

<!-- #region citation-manager={"citations": {"1z16r": [{"id": "4951909/ZVWDRAGM", "source": "zotero"}]}} editable=true slideshow={"slide_type": ""} -->
The most widely studied and frequently adopted classroom tools are freely available Open Educational Resources (OER), designed specifically for educators and students. These include both digitized and “born-digital” primary source collections and Content Management Systems (CMS) (<cite id="1z16r"><a href="#zotero%7C4951909%2FZVWDRAGM">(Georgopoulou et al. 2025)</a></cite>). Wordpress is the most famous example of a CMS and is known for its ease of use such that even someone with zero previous web development experience can publish a website. At the same time, more advanced users have the option to work with underlying code if they so choose and thousands of ready-made plugins exist to extend powerful features to a website. Such plugins allow webmasters to create full e-commerce stores and design complex and visually appealing site layouts without touching code. Amongst academics, Omeka and Scalar are the most well-known and both come packed with features geared toward scholarly digital publication.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} -->
CMSs achieved popularity in the classroom precisely because they lowered the threshold of technical proficiency for web development. The platforms combine the two halves of web development, front-end (what you see when you visit a website) and the back-end (everything in the background that provides functionality). Suddenly, designing a visually appealing website no longer required intimate knowledge of Hypertext Markup Language (HTML), Cascading Style Sheets (CSS), or JavaScript (JS) and powerful back-end features could be installed with a plugin rather than weeks of programming in Python, Java, PHP, Ruby, or numerous other languages used in backend web development. With CMSs students, instructors, and researchers can create visually appealing websites with powerful features and minimal friction, without ever seeing a line of code. User interfaces resemble Microsoft Word much more than a traditional code editor such as Visual Studio. Moreover, the workflow follows a straightforward process: users simply define their desired pages, specify required features, and construct their sites accordingly. This accessibility has democratized web development within academic contexts, removing technical barriers that once limited digital scholarship and pedagogical innovation.
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"h84cu": [{"id": "4951909/WMB658F8", "source": "zotero"}]}} editable=true slideshow={"slide_type": ""} -->
However, these advantages carry significant limitations. CMSs operate as predetermined systems in which developers establish all available functionalities for end users. Extending these pre-built capabilities demands substantial technical expertise that contradicts the platforms' promise of accessibility. For non-technical users, CMSs foreclose the vast array of technological possibilities. Johanna Drucker has characterized the relationship between user and pre-built platform as “requiring submission, not invention,” and that intellectual engagement suffers as these “platforms have their protocols, and the user must follow them, disciplining mind and imagination in a practice of alignment with what is possible in the program” (<cite id="h84cu"><a href="#zotero%7C4951909%2FWMB658F8">(O’Sullivan 2023)</a></cite>). 
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} -->
This tension underscores a central paradox in digital history pedagogy. CMSs both standardize digital history practices by contributing to the field’s methodological maturation while also shielding students from the computational processes that underlie digital scholarship. The very ease of use that makes these platforms pedagogically attractive may also limit students’ capacity to understand how technological choices shape and constrain digital arguments.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
### Choosing and Using Scalar
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
These strengths and limits framed my own classroom use of Scalar. In both Digital Documentary Publishing (University of Illinois at Urbana-Champaign, Fall 2023) and Digital Public History (University of Florida, Spring 2025), I opted to use Scalar. Both upper-division history courses adapted historian John Randolph’s pedagogical model for collaborative digital documentary publishing developed at the University of Illinois, in which students work in small groups to investigate understudied yet historically significant primary sources, conduct historical research, and present their findings through public-facing digital exhibits. Students worked in groups of four to five to investigate understudied yet historically significant primary sources, conduct research, and develop digital exhibits for public audiences. The point of the courses was not to become an expert in Scalar, but to learn historical principles such as primary source analysis, argumentation, and the tenets of public history, while using technology to bring historical knowledge production to digital spaces. The course consisted of four main units:
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
1. History and Its Sources, Yesterday and Today: This introductory unit examined the theoretical foundations of primary source production and the ways digital technologies have transformed both their creation and preservation. Students analyzed the processes through which primary sources reach the present, focusing on the deliberate choices and historical contingencies that shaped their survival. Written assignments critically assessed these transmission processes and considered their implications for historical interpretation. (3 weeks)
2. Publishing the Past in the Digital Age: Documentary publishing was a key component in these courses and this unit introduced concepts of scholarly editions. Students were also introduced to the final project through a bird’s eye overview so that they knew “where” the course was taking them. Writing assignments consisted of comparing analogue and digital scholarly editions with a specific emphasis on benefits and drawbacks between both methods. (2.5 weeks)
3. Studying Your Source and Imaging Its Place in History: Students conducted intensive research on their assigned primary sources, tracing their sources’ biographical trajectories from creation through digitization while situating them within broader historical contexts. Each student produced a substantial contextual research essay. Individual contributions provided the foundational content for the digital exhibits. (2.5 weeks)
4. Creating Your Prototype Edition: The final unit emphasized the translation of scholarly research into digital public history. Class sessions included Scalar tutorials, discussions of presentation design and accessibility standards, instruction in metadata conventions, collaborative workshops, and project presentations. (6 weeks)
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
This scaffolded progression moved deliberately from theoretical foundations to practical application: beginning with traditional historical inquiry, to addressing digital transformation's opportunities and challenges, then developing critical source analysis skills, and finally culminating in public-facing digital scholarship.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
Scalar held several advantages for these courses. An abundance of tutorials already existed that could supplement my in-class demonstrations for using the system. Randolph’s open-source and peer-reviewed journal _SourceLab_ already showed the possibilities of using Scalar to create born-digital scholarly works. The figures below show polished and refined versions of a student project eventually published through _SourceLab_.
<!-- #endregion -->

```python editable=true slideshow={"slide_type": ""} tags=["figure-intro-page-scalar-exhibit-*"]
from IPython.display import Image, display
metadata={
    "jdh": {
        "module": "object",
        "object": {
            "type":"image",
            "source": [
                "The introduction page to a Scalar exhibit"
            ]
        }
    }
}
display(Image("media/ScalarIntroPage.png", width=1000), metadata=metadata)
```

```python editable=true slideshow={"slide_type": ""} tags=["figure-intro-page-scalar-*"]
from IPython.display import Image, display
metadata={
    "jdh": {
        "module": "object",
        "object": {
            "type":"image",
            "source": [
                "The layout of the introduction page on Scalar"
            ]
        }
    }
}
display(Image("media/ScalarIntroductionLayout.png", width=1000), metadata=metadata)
```

```python editable=true slideshow={"slide_type": ""} tags=["figure-historical-sources-scalar-*"]
from IPython.display import Image, display
metadata={
    "jdh": {
        "module": "object",
        "object": {
            "type":"image",
            "source": [
                "Presenting historical sources in Scalar"
            ]
        }
    }
}
display(Image("media/ScalarSourcePresentation.png", width=1000), metadata=metadata)
```

<!-- #region citation-manager={"citations": {"r2jwv": [{"id": "4951909/WMB658F8", "source": "zotero"}]}} editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
Beyond web design aesthetics, Scalar integrated with numerous academic repositories to easily import media, but also contained easy-to-use methods to upload media or import media from other, non-academic sites. Scalar supports most major media formats for images, videos, and audio so that students could use almost anything they found to supplement their writing. The software can as easily drive a book-length work as it can an undergraduate essay. And, although I provided a very linear structure for my students to follow in their projects, the Scalar team’s born-digital mantra “is an indication of a different approach… ‘to take advantage of the unique capabilities of digital writing, including nested, recursive, and non-linear formats’” (<cite id="r2jwv"><a href="#zotero%7C4951909%2FWMB658F8">(O’Sullivan 2023)</a></cite>) This architectural flexibility allowed students to experiment with multi-layered historical narratives even within structured assignments, introducing them to the unique strengths and distinctive possibilities of digital scholarship that move beyond traditional linear structures.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
Scalar's limitations, however, revealed the critical importance of institutional investment in digital pedagogy.  At the time, the platform did not have a footnote feature that aligned with what practicing historians expected or that provided a suitable digital version compared to analogue publications. This deficiency typically presents instructors with two unsatisfactory options: abandon the platform entirely or undertake the technically demanding task of developing custom tools. Fortunately, the Digital Humanities team at the University of Illinois had ported over their own Scalar installation several years before, created their own reusable template, and integrated a suitable footnote feature. Rather than using the standard version of Scalar hosted for free on University of Southern California’s (USC) servers, I was able to use the modified version at the University of Illinois. The customized installation represented a significant institutional investment by UIUC: information technology expertise to install Scalar on a server, coding expertise and time to create a customized version of Scalar, and all the expenditures to host past and future Scalar sites created on the server along with maintaining subject matter experts. Few universities can afford such an investment and most who ultimately choose Scalar will be working with the standard template on USC servers.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
Scalar functioned as a no-code platform that met all functional requirements of the course and accommodated the features students sought for their projects. The examples in the Data Layer below show HTML code for textual elements and footnotes generated automatically by the CMS; students worked exclusively within the WYSIWYG editor. The University of Illinois digital humanities team managed all CSS in the background.
<!-- #endregion -->

```python editable=true slideshow={"slide_type": ""}
<a data-annotations="" class="inline wrap" data-caption="description" data-size="medium" data-align="right" resource="media/nettie-hunt-and-daughter-after-brown-v-board" name="scalar-inline-media" href="https://iopn-sandbox.library.illinois.edu/scalar/zora-neale-hurston-letter/media/Nettie%20Hunt%20and%20Daughter.jpg"\>\</a\>&nbsp;&nbsp; &nbsp; &nbsp;Student project example text.\<sup data-footnote-id="2nw2q"\>\<a href="#footnote-1" id="footnote-marker-1-1" rel="footnote"\>1\</a\>\</sup\>&nbsp;Addiontal student sample text.\<sup data-footnote-id="obqdb"\>\<a href="#footnote-2" id="footnote-marker-2-1" rel="footnote"\>2\</a\>\</sup\>&nbsp;Final student sample text with footnote.\<sup data-footnote-id="lwohc"\>\<a href="#footnote-3" id="footnote-marker-3-1" rel="footnote"\>3\</a\>\</sup\>
```

```python editable=true slideshow={"slide_type": ""}
<div class="scalarfootnotes"\>
	  <hr aria-label="scalarfootnotes below" />
	  <header>
	    <h2>Footnotes
	    </h2>
	  </header>
	  <ol><li id="footnote-1" data-footnote-id="2nw2q"><cite>Darlene Clark Hine et al.,&nbsp;<em>The African-American Odyssey</em>, Vol. 2, 7th ed. (New York: Pearson, 2018), 621.</cite><a href="#footnote-marker-1-1">&crarr;</a></li><li id="footnote-2" data-footnote-id="obqdb"><cite>Ibid, 621.</cite><a href="#footnote-marker-2-1">&crarr;</a></li><li id="footnote-3" data-footnote-id="lwohc"><cite>Wim Roefs, &quot;Civil Rights Movement,&quot; In&nbsp;<em>Black Women in America</em>, (Oxford: Oxford University Press, 2005). https://www.oxfordreference.com/display/10.1093/acref/9780195156775.001.0001/acref-9780195156775-e-0069?rskey=4PIf9B.</cite><a href="#footnote-marker-3-1">&crarr;</a></li><li id="footnote-4" data-footnote-id="z1jvd"><cite>Hurston, Z.N. TLS to Mary Holland, Merritt Island, Fla. (3p. 8 1/2 x 11). Thoughts on Pepper and Zora&#39;s termination at the library, 1957, June 27, Box: 2, Folder: 90. Zora Neale Hurston Papers, MS Group 006. Special and Area Studies Collections, George A. Smathers Libraries, University of Florida, 1.</cite><a href="#footnote-marker-4-1">&crarr;</a></li><li id="footnote-5" data-footnote-id="g6g8y"><cite>Andrew Delbanco, &ldquo;The Political Incorrectness of Zora Neale Hurston,&rdquo; <em>The Journal of Blacks in Higher Education</em>, no. 18 (1997): 103, https://doi.org/10.2307/2998779; Oneka LaBennett, &ldquo;Zora Neale Hurston,&rdquo; in Oxford Bibliographies: Anthropology, last modified November 28, 2016, https://doi.org/10.1093/obo/9780199766567-0160; Olivia Marcucci, &ldquo;Zora Neale Hurston and the Brown Debate: Race, Class, and the Progressive Empire,&rdquo; <em>The Journal of Negro Education </em>86, no. 1 (Winter, 2017): 15, https://doi.org/10.7709/jnegroeducation.86.1.0013.</cite><a href="#footnote-marker-5-1">&crarr;</a></li><li id="footnote-6" data-footnote-id="gbjkt"><cite>Marcucci, &quot;Hurston and the Brown Debate&quot;, 13.</cite><a href="#footnote-marker-6-1">&crarr;</a></li><li id="footnote-7" data-footnote-id="uj3e1"><cite>Hurston, Z.N. TLS to Mary Holland, 3. &nbsp;</cite><a href="#footnote-marker-7-1">&crarr;</a></li>
	  </ol>
	</div>
```

<!-- #region editable=true slideshow={"slide_type": ""} -->
### Case Study 1 Results
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} -->
Scalar proved itself a powerful content management system that allowed students to write text, maintain scholarly conventions of footnotes and metadata, import or link to media, and present their work in a visually appealing format for an educated public. Functionality came at a high cost. Although Scalar’s WYSIWYG environment resembles Wordpress and its text editing tools operate much like Microsoft Word or Google Docs that students are already familiar with, many features required explicit documentation, instructor demonstration, and time for students to practice and implement. Though theory balanced practice, the technical aspects of the final project consumed 6 of 14 weeks of the semester, approximately 43% of course time. Professors often bemoan the massive amount of material to cover in a single semester; a feature-rich CMS intensifies this pressure, effectively requiring that the digital project—its epistemological framing, technical execution, and methodological rationale—become central to the course.
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"5t3ng": [], "g73i4": []}} editable=true slideshow={"slide_type": ""} -->
It is true that an instructor could shave time off from students achieving technical proficiency. Yet this risks leading to “buttonology,” or introducing software to students in a cursory manner without a real understanding of the wider context (<cite id="5t3ng"><a href="#zotero%7C4951909%2FWVH3WVAE">(Russell and Hensley 2017)</a></cite>). Students learn that pressing a button produces a particular result, but never develop the adaptability to respond when a software update alters functionality or when they transition to a different platform. Buttonology produces students who can proficiently use one version of one software package, but not necessarily any other digital tools. Such cursory acquaintances ensure that the “operations of the algorithms remain unseen, taken for granted, unexamined, and out of range of intervention” which “result in students very well versed in a single platform but ignorant of the underlying issues that it addresses” (<cite id="g73i4"><a href="#zotero%7C4951909%2FWMB658F8">(O’Sullivan 2023)</a></cite>). Learning widely-used CMSs such as Omeka or Scalar is beneficial, but given the rapid pace of technological change, adaptability is often more valuable and more sought after in the non-academic workforce than deep specialization. Achieving this adaptability requires dedicating class time beyond the initial “button-pressing” phase to help students grasp the developers’ design decisions and understand how the software approaches real-world problems.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} -->
At the same time, Scalar’s familiar interfaces ensured accessibility to the platform. No student was “left behind” because the technical aspects of web development were abstracted away. If a student could use a word processor (and they were required to in order to write their papers in the first 8 weeks of class), it was only marginally more difficult to create and publish pages in Scalar. Although digital historians should always be wary of the “black-box” effect of software, Scalar pushed aside the more difficult technical aspects of web development that allowed students to continue to critically engage with their primary and secondary sources and development their historical argumentation.  In this way, Scalar functioned as a sophisticated presentation tool that kept the course centered on historical knowledge production and communication rather than turning it into a computer science class.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} -->
Student experience reflected these same strengths and limits. Scalar’s familiar editing environment helped students begin building pages with relatively little fear, and many responded positively to seeing their research take shape in a polished public-facing format. At the same time, functions beyond basic text entry often required repeated demonstration and troubleshooting, especially when students moved from drafting content to structuring pages and integrating media. After the course, one student noted that they suggest "having classes be 80 minutes instead of 50 minutes to provide students with more in class work time with their group and instructor present" while another suggested that the course could be "improved by allowing more time for hands–on learning with Scalar The result was that Scalar made digital publication feel achievable, but not always intuitive enough to significantly reduce the instructional burden that accompanied the project.
<!-- #endregion -->

Although it was not a factor in my original course design or in the initial drafting of this article, Scalar’s subsequent loss of support underscores an issue that this case study already brings into view. The platform’s polished interface and ease of use made it attractive in the classroom, but that convenience also depended on an external system whose long-term maintenance remained outside the control of both instructor and students. This point extends beyond Scalar itself. Choosing a digital platform for the classroom is not simply a matter of present usability or visual polish; it is also a question of sustainability. Considerations for platform sustainability is an integral part of pedagogy.


While Scalar offered polished presentations and a familiar development environment, its demands on class time and risk of superficial technical engagement already suggested the value of a different approach. Subsequent developments surrounding the platform only reinforce the importance of considering sustainability alongside pedagogy. The second case study therefore focuses on a minimalist framework, ScholarMinPub, that trades visual refinement for deeper technological transparency, reduced time investment, and greater portability.

<!-- #region editable=true slideshow={"slide_type": ""} -->
## Case Study 2: Minimalist Computing Frameworks
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"ciqfu": [{"id": "4951909/DUB54MKG", "source": "zotero"}], "k10o6": [{"id": "4951909/DUB54MKG", "source": "zotero"}]}} editable=true slideshow={"slide_type": ""} -->
Digital history specialists associate minimalist computing with smaller, simpler, and more transparent technologies: Jekyll instead of Omeka, WordPress, or Scalar; Markdown or plain text rather than XML; CSV files instead of SQL databases; static websites rather than dynamic web apps; and GitHub Pages over costly cloud hosting. But Roopika Risam and Alex Gil note that minimalist computing is more a “mode of thinking about digital humanities praxis” than a specific set of tools (<cite id="k10o6"><a href="#zotero%7C4951909%2FDUB54MKG">(Risam and Gil 2022)</a></cite>). The digital historian always operates within constraints: time, money, resources, technical skills, computing power. The minimalist mindset “advocates for using _only_ the technologies that are necessary and sufficient for developing digital humanities scholarship in such constrained environments” (<cite id="ciqfu"><a href="#zotero%7C4951909%2FDUB54MKG">(Risam and Gil 2022)</a></cite>). The following is not an exhaustive list, but highlights some of the core principles that define minimalist computing to aid the digital historian in navigating these constraints:
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} -->
1. Simplicity: choosing tools that are easy to understand, maintain, and teach
2. Sustainability: prioritizing long-term preservation and low energy use
3. Accessibility: ensuring that tools and outputs are usable across devices and internet speeds, especially in under-resourced contexts.
4. Transparency: preferring open-source software and non-proprietary formats that allow for full user control and future migration.
5. Minimal dependencies: avoiding heavy software stacks or proprietary platforms where possible.
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"mnswz": [], "xh6rl": []}} editable=true slideshow={"slide_type": ""} -->
Adherents of minimalist computing are aware of a fact that surprises many, namely that when an article, image, or other content is posted to the internet, it does not automatically enter any kind of long-term storage. In the absence of sustained preservation efforts and funding, the internet content is inherently ephemeral. In academia, it “is also becoming increasingly clear that the existing body of highly specialized and idiosyncratic publications of the last twenty years is no longer sustainable, and publishers (including academic centers) are increasingly being forced to make difficult decisions around closing down publications even when in some cases they are still important and in regular use” (<cite id="xh6rl"><a href="#zotero%7C4951909%2FWMB658F8">(O’Sullivan 2023)</a></cite>). We already confront a “legacy corpus” from the 1990s and 2000s—that uses the deprecated technologies of those decades—that requires preservation as well as resources just to remain accessible (<cite id="mnswz"><a href="#zotero%7C4951909%2FKSHIHATD">(Smithies et al. 2019)</a></cite>). Digital decay affects not only older projects but also threatens contemporary work that relies on complex technical infrastructures and ongoing institutional support. Digital historians who practice minimalist computing build low-maintenance, cost-effective projects designed to remain functional, readable, and accessible for decades.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} -->
From a pedagogical point of view, bringing minimalist frameworks to students in the classroom can result in greater equity in technological accessibility, a deeper understanding of the underlying technology, and a closer connection between knowledge production and technology. Many available CMSs are open-source and free to use. For example, the Alliance for Networking Visual Culture provides Scalar free of charge and the University of Southern California charges nothing to host digital projects built on their Scalar template. Ironically, it is precisely CMSs’ excellent presentation capabilities that also hinder their accessibility. The sophisticated presentation capabilities that make CMSs attractive create unexpected accessibility challenges. These platforms assume users possess relatively powerful, modern devices capable of rendering complex HTML, JavaScript, and CSS. This assumption may hold for many students at well-resourced American universities, but it excludes both international students with limited technological access and the broader publics these digital exhibits strive to reach. Community members accessing student projects encounter rendering failures, slow load times, or complete inaccessibility on older devices or slow internet connections. 
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} -->
Minimalist frameworks address these equity concerns through deliberate technical restraint. By prioritizing simple HTML and minimal styling over dynamic features, these approaches ensure projects remain accessible across diverse technological contexts. This accessibility extends beyond viewing to creation. Students can develop minimalist projects on virtually any computer capable of running a basic text editor. Working within such frameworks also brings students closer to the underlying technologies that CMSs typically abstract away. They observe immediate connections between their code and its output, understanding how each technical decision influences the presentation of their argument. This transparency demystifies digital knowledge production, revealing technology not as a neutral container for historical content but as a shaping force in constructing historical narratives. 
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
### Developing ScholarMinPub and Its Pedagogy
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
Although I observed the pedagogical benefits of using a CMS such as Scalar in the classroom, I wanted some way to bring more digital history and digital tools to my courses without the significant overhead costs in time that a full platform required. How could I increase digital pedagogy without affecting students building traditional historical skillsets? How could I use digital technology to enhance students’ historical understanding, as a supplement rather than a centerpiece of the course?
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
In early 2024 I became one of the lead developers on John Randolph’s MinDoc project, a framework that transferred _SourceLab_’s digital documentary publishing template from Scalar to minimalist technologies using GitHub, Jekyll, and Markdown. CSS, HTML, and JavaScript occupied a deeper layer within the framework that would be accessible to students with more technical proficiency, but no student would need to touch more than MarkDown to complete a fully functional digital project. After completing the first beta version of MinDoc, I realized the framework could be modified to work with general digital history presentations. It could be suitable in instances where instructors seek to incorporate digital methods without restructuring their entire curriculum around technical instruction. 
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
I forked the MinDoc project, modified it for generalized use, and provided it as an open-source framework titled ScholarMinPub. Students used the framework for their final projects in my course Nineteenth-Century European History (University of Florida, Fall 2024), a class not focused on digital history. The final projects consisted of extended historical analysis essays supplemented with digital media and digitized primary sources. Although the resulting projects lacked the polished aesthetic flair of Scalar, the minimalist framework contained most of the important features of Scalar (text, media presentation, a zooming functionality for viewing primary source details, footnotes capabilities). This feature parity emerged naturally from MinDoc's origins as a minimalist interpretation of Scalar's core functionality. The figures below illustrate these structural similarities, showing how ScholarMinPub preserves Scalar's fundamental presentation logic while eliminating its technical complexity.
<!-- #endregion -->

```python editable=true slideshow={"slide_type": ""} tags=["hermeneutics", "figure-intro-page-scholarminpub-*"]
from IPython.display import Image, display
metadata={
    "jdh": {
        "module": "object",
        "object": {
            "type":"image",
            "source": [
                "The introductory page for ScholarMinPub"
            ]
        }
    }
}
display(Image("media/ScholarMinPubIntroPage.png", width=1000), metadata=metadata)
```

```python editable=true slideshow={"slide_type": ""} tags=["figure-layout-intro-page-scholarminpub-*"]
from IPython.display import Image, display
metadata={
    "jdh": {
        "module": "object",
        "object": {
            "type":"image",
            "source": [
                "Layout of introductory pages in ScholarMinPub"
            ]
        }
    }
}
display(Image("media/ScholarMinPubIntroductionLayout.png", width=1000), metadata=metadata)
```

```python editable=true slideshow={"slide_type": ""} tags=["figure-zoom-feature-images-scholarminpub-*"]
from IPython.display import Image, display
metadata={
    "jdh": {
        "module": "object",
        "object": {
            "type":"image",
            "source": [
                "Zoom in feature for images on ScholarMinPub"
            ]
        }
    }
}
display(Image("media/ScholarMinPubZoomInFeature.png", width=1000), metadata=metadata)
```

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
Like CMSs, ScholarMinPub abstracts away the most powerful, but also the most difficult aspects of web development. It made little sense to cram crash courses on CSS, HTML, or JavaScript into a history course, but spending twenty minutes on Markdown and thirty minutes on file system structures seemed a worthwhile time commitment. Both provided crucial tech skills without overwhelming students. The figures below depict the file structure environment students encountered, the `media files` directory they directly interacted with, the `configuration files` directory they were instructed not to alter, and the GitHub Markdown editing environment in which they worked on their projects. The Data Layer below shows the extent of student coding in Markdown with a YAML header.
<!-- #endregion -->

```python editable=true slideshow={"slide_type": ""} tags=["hermeneutics", "figure-github-repo-schohlarminpub-*"]
from IPython.display import Image, display
metadata={
    "jdh": {
        "module": "object",
        "object": {
            "type":"image",
            "source": [
                "The main GitHub repository of a ScholarMinPub project"
            ]
        }
    }
}
display(Image("media/ScholarMinPubMainRepository.png", width=1000), metadata=metadata)
```

```python editable=true slideshow={"slide_type": ""} tags=["figure-student-file-management-scholarminpub-*"]
from IPython.display import Image, display
metadata={
    "jdh": {
        "module": "object",
        "object": {
            "type":"image",
            "source": [
                "Student file management in ScholarMinPub"
            ]
        }
    }
}
display(Image("media/ScholarMinPubStudentFileManagement.png", width=1000), metadata=metadata)
```

```python editable=true slideshow={"slide_type": ""} tags=["figure-config-files-scholarminpub-*"]
from IPython.display import Image, display
metadata={
    "jdh": {
        "module": "object",
        "object": {
            "type":"image",
            "source": [
                "Configuration files for ScholarMinPub"
            ]
        }
    }
}
display(Image("media/ScholarMinPubConfigFiles.png", width=1000), metadata=metadata)
```

```python editable=true slideshow={"slide_type": ""} tags=["figure-text-editing-environment-scholarminpub-*"]
from IPython.display import Image, display
metadata={
    "jdh": {
        "module": "object",
        "object": {
            "type":"image",
            "source": [
                "The text editing environment in ScholarMinPub"
            ]
        }
    }
}
display(Image("media/ScholarMinPubEditingEnvironment.png", width=1000), metadata=metadata)
```

```python editable=true slideshow={"slide_type": ""}
---
	layout: default
	title: Introduction
	number: 1
	---
	# Introduction
	
	This is where you introduce your project to your audience. You should summarize briefly the topic you are working on. (250-350 words)
	
	The following is sample text to show the capabilities of presenting text with various formatting (such as bold), different languages, adding footnotes, and images.[^1]
	
	
	[^1]: First example footnote. View other pages to see sample methods of working with Markdown.
```

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
Some aspects were impossible to completely abstract away. While a CMS offers a button to import and place an image on a page, ScholarMinPub uses Liquid, an open-source template written in Ruby. I wrote explicit instructions for students on copying-and-pasting the Liquid template to place an image, video, or audio file on a page. Students needed only modify the file name. They might see and “work with” scary code, but copying and pasting is the only skill they actually needed. The Data Layer below shows the Liquid code students copied and pasted when they needed to include a media file. Students needed only to substitute “PrussianInfantryHohenfriedberg,” the stock image with their media file of choice.
<!-- #endregion -->

```python editable=true slideshow={"slide_type": ""}
% assign media = site.media_metadata | where_exp: "item", "item.name == 'PrussianInfantryHohenfriedberg'" %
	{% include media.html pages=media %}
```

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
Students also interacted with the configuration YAML file, but only to change the “baseurl” to the name of their projects. Many students reflected that the YAML file’s esoteric nature initially frightened them that they might alter a line and break their entire project. But all students persisted, followed instructions closely, and successfully altered the line correctly.
<!-- #endregion -->

```python editable=true slideshow={"slide_type": ""}
title: Title
	email: your-email@example.com
	description: by Authors
	
	baseurl: "/ScholarMinPub" # the subpath of your site. Change it if the name of your repository is other than "ScholarMinPub"
	
	twitter_username: jekyllrb
	github_username:  jekyll
	
	# Custom directory structure
	layouts_dir: configuration_files/_layouts
	includes_dir: configuration_files/_includes
	
	sass:
	  load_paths:
	    - configuration_files/_sass
	
	assets:
	  sources:
	    - configuration_files/assets/images
	    - configuration_files/assets/js
	    - configuration_files/assets/css
	    - media_files/images
	    - media_files/audio
	    - media_files/video
	    - media_files/pdfs
	
	collections_dir: media_files
	
	
	# Build settings
	
	plugins:
	  - jekyll-feed
	
	collections:
	  media_metadata:
	    output: true
	    layout: 'image_description'
```

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
Sample code also existed in all projects to include a required TimelineJS presentation. Students only needed to alter the URL in the block of code while the TimelineJS presentation required entering data into a spreadsheet.
<!-- #endregion -->

```python editable=true slideshow={"slide_type": ""}
from IPython.display import IFrame
IFrame('https://cdn.knightlab.com/libs/timeline3/latest/embed/index.html?source=12ZNkEbnN4RnsWLrW2Ekpz2cQV_2QA-3WgJTP4WUKduk&font=Default&lang=en&initial_zoom=2&height=650', width='100%', height='650')

```

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
Experience with creating Markdown links occurred through uploading PDF files directly to the media files folder in the correct location and altering the filename.
<!-- #endregion -->

```python editable=true slideshow={"slide_type": ""}
[Download PDF file](#)({ site.baseurl }/media_files/pdfs/newspaper1942.pdf)
```

Overall, ScholarMinPub shifted the learning curve from the student to the instructor. For students accustomed to word processors, the initial encounter with Markdown, YAML, GitHub’s file-and-folder structure, and a less visually intuitive editing environment could be intimidating. In practice, however, students only needed to master a narrow and carefully bounded set of tasks: editing text in Markdown, modifying a small number of metadata fields, navigating a simple folder structure, and uploading or linking images. The approach remained manageable because the technical environment was deliberately constrained. Students were not asked to install software, use the command line, build pages from scratch, or understand the full underlying architecture of the site. That simplicity, however, depended on substantial instructor preparation in advance. The instructor had to configure the template, determine which files students could safely edit, troubleshoot formatting problems, and translate the underlying structure of the site into a small set of repeatable classroom procedures. On the instructor side, this implementation of minimal computing was not inherently easier than a conventional content management system. Its pedagogical value depended on careful scaffolding, a tightly limited range of student tasks, and an instructor able to prepare and maintain the framework before students ever began their work. At the same time, this burden can be mitigated. Reusable frameworks such as ScholarMinPub can be copied and adapted rather than built from scratch, which lowers the threshold for adoption. Even so, the instructor must still understand the structure of the site more fully than the students do in order to configure the template, limit the editable components, and resolve routine problems as they arise.

<!-- #region editable=true slideshow={"slide_type": ""} -->
### Case Study 2 Results
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} -->
For the most part, the two-course experiment with ScholarMinPub in Fall 2024 successfully integrated digital tools into history courses not specifically designed as digital history classes. The classes spent approximately three weeks on the digital component, compared to six weeks in my courses that used Scalar. This represented roughly 20 percent of total class time rather than 43 percent. Much of this time, moreover, was not devoted solely to the technical aspects of web publishing, but to the broader work of researching topics, organizing evidence, and coordinating group responsibilities. In that sense, ScholarMinPub allowed the digital project to remain part of the course without requiring it to dominate the semester.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} tags=["hermeneutics"] -->
Student responses suggested both challenge and reward. Although the minimalist framework initially appeared less intuitive than Scalar’s WYSIWYG environment, students were often more likely to express pride and satisfaction in the final products they created. When asked about their experience, they most often described the project as difficult but rewarding: getting the site to function, organizing content successfully, and seeing their work appear in public-facing form produced a visible sense of accomplishment. One student noted that they learned that they “could participate in creating digital/public history.” Although this evidence remains anecdotal rather than formally assessed, student reactions suggested that the greater technical transparency of the project often translated into a stronger sense of ownership over the final result.
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"232gr": []}} -->
The experiment was a qualified success. GitHub is a powerful platform for teamwork, but it requires version control through Git’s pulling, pushing, and committing files, either through an integrated development environment (IDE) or the command line. In contrast, the students worked on their files through the Markdown editor and the file management GUI built into the GItHub site. Git seemed beyond the purview of the course and its goals, and creating one GitHub account per group raised the specter of students losing access at crucial moments. Given these constraints, I decided that each group should have a dedicated “webmaster” who would actually fill the role of working with GitHub, interacting with the files, and adding content. Other group members wrote their historical analyses in Markdown and submitted media files to the webmaster who would then upload files and ensure functionality. All students, however, created a GitHub account with the ScholarMinPub template and worked through the class lectures on how to use the technologies in addition to learning Markdown through writing their analyses. The “three-speed problem” presents a persistent problem for integrating digital history into the classroom as “the instructor is always and inexorably going too quickly for some, too slowly for others, and at just the right speed for a few students” (<cite id="232gr"><a href="#zotero%7C4951909%2FICSTWWRP">(Croxall and Jakacki 2023)</a></cite>). Allowing the groups to select their own webmaster stacked the deck to ensure webmasters were more likely than the average student to find digital technologies interesting and exciting. Nonetheless, a minority of students suggsted that "students begin working in groups on their final project a few more weeks in advance than during this semester." In the case of ScholarMinPub, the goal was not to remove technical friction altogether, but to manage it within a set of tasks that supported rather than overwhelmed the course’s historical objectives.
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"e2elu": []}} -->
Further iterations of this group digital project must confront the issue of speed. At least part of it can be resolved through a more seamless ability to collaborate that does not require technical skills on the level of Git. Google Docs provides such a seamless experience and meets the requirement for equity and accessibility through free use, though it runs up against other aspects of the minimalist paradigm and does not integrate particularly well with GitHub. And, despite the self-selection nature of the “webmaster” position, the groups as a whole felt strongly that they had all contributed in meaningful ways to their final projects—indeed, the team structure mimicked many real-life projects in which every team member plays roles of varying levels of technological sophistication. More so than Scalar, ScholarMinPub met the needs of average college students who pursue roles with non-academic entities in which a “significant number of employers (n=59) prefer applicants to have front-end web development and design skills, which was often stated as ‘understanding of web design standards using HTML, CSS, and JavaScript, and web development platforms’” (<cite id="e2elu"><a href="#zotero%7C4951909%2FKM5SR3PC">(Walsh et al. 2022)</a></cite>). One student found career prospects a justification for the exercise by nothing that "my digital participation in this course has helped prepare me for future career projects, introducing me to the concept of website building." ScholarMinPub and other minimalist platforms provide students an early introduction, a stepping stone to meeting their goals for employability.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} -->
Taken together, these two teaching experiments reveal how tool selection directly shapes what students learn, how they engage, and what skills they take from the course. The final section reflects upon the Scalar and ScholarMinPub pedagogical experiences and draws out broader guidance for history instructors.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} -->
## Conclusion
<!-- #endregion -->

The final projects produced through Scalar and ScholarMinPub differed less in their seriousness as historical work than in the forms of learning required to produce them. Scalar tended to yield more polished and visually refined exhibits, but it also required greater investment of class time and more instructional support. ScholarMinPub produced simpler final presentations, yet it reduced the time spent on platform training and gave students a more direct encounter with the underlying structure of digital publication. These differences point to distinct pedagogical tradeoffs rather than a single best solution: Scalar favored polish and immediacy, while ScholarMinPub favored transparency and technical adaptability. Scalar projects tended to be visually stronger, while ScholarMinPub projects more clearly exposed the methods of digital publication.

<!-- #region editable=true slideshow={"slide_type": ""} -->
Pedagogy should be a core identity of digital history, not an afterthought. Both platforms such as feature-rich CMSs and minimalist frameworks play important roles in making this goal a reality. Student outcomes in one style of my classes or the other were neither better nor worse. The courses had different overarching goals, even if increasing digital literacy and skillsets formed a significant component of each. Digital literacy was a major component of both, but the rationale for tool choice varied. Those differences offer lessons for history instructors seeking to align technology with pedagogy.
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"feewo": []}} editable=true slideshow={"slide_type": ""} -->
The tool an instructor chooses to use should always match the goal. That goal almost certainly possesses a strong pedagogical component tied into academia. The dearth of tenure-track positions ensures that a large number of graduate students must look beyond academia for employment. Positions in museums and heritage institutions where CMSs such as Scalar and Omeka dominate rank highly in many graduate students’ goals as academy-adjacent work. Museums often use established CMS systems such as Scalar and Omeka. Training in these platforms directly supports employability. The calculus is different for undergraduate students. Most will not pursue a doctorate in history and many come to college not just for analytical and writing skills that are the bread and butter of history coursework, but also to develop skills useful to gain and sustain employment. As Bowen and Watson note, as technological advances rapidly increase, “the job market changes more quickly” and “core skills and the ability to adapt increase in value,” causing employers to search out employees who “prioritize the ability to ask new questions, connect and interrogate new ideas, evaluate, iterate, and adapt to new responses” (<cite id="feewo"><a href="#zotero%7C4951909%2FEDFDI9UE">(Bowen and Watson 2024)</a></cite>). They wrote these lines regarding the advent of artificial intelligence, but the concept holds true for the centrality of computing in our lives more generally. Minimalist frameworks prioritize learning underlying computing concepts rather than fixed workflows. Students can more readily translate computing concepts to new platforms or frameworks than they can the locked-down designs of CMSs.
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"3fuvg": [], "8s4gr": []}} editable=true slideshow={"slide_type": ""} -->
Beyond matching goal with tool, instructors should adopt a more critical, intentional approach to technology selection, framed by the core questions of minimal computing—even if the instructor does not ultimately decide to use a minimalist framework. All instructors operate within certain constraints, whether it is institutional digital infrastructure, available class time, financial limitations, or the background skills with which students enter the classroom. Risam and Gil remind us that for all digital humanities projects, we should question: what we need; what we have; what we must prioritize; and, what we are willing to give up (<cite id="3fuvg"><a href="#zotero%7C4951909%2FDUB54MKG">(Risam and Gil 2022)</a></cite>). These questions lead to what technologies instructors should use in the classroom, but also when not to use technologies: “Digital Pedagogy is precisely not about using digital technologies for teaching and, rather, about approaching those tools from a critical pedagogical perspective. So, it is as much about using digital tools thoughtfully as it is about deciding when not to use digital tools, and about paying attention to the impact of digital tools on learning” (<cite id="8s4gr"><a href="#zotero%7C4951909%2FICSTWWRP">(Croxall and Jakacki 2023)</a></cite>). This is a powerful idea in an age defined by the digital and in which university administrations pursue the integration of technology with all aspects of pedagogy. Instructors should ask whether there is anything to be gained in bringing into the classroom a particular digital history assignment or tool. Does it serve learning objectives or the goals of the instructor and students? Sometimes the answer is no.
<!-- #endregion -->

<!-- #region citation-manager={"citations": {"68vq5": []}} editable=true slideshow={"slide_type": ""} -->
Beyond technical and pedagogical fit, tool selection carries ethical weight. Platform choice can expand—or narrow—the inclusivity of the digital record, influencing whose voices and histories are preserved. Some proponents of minimal computing have made ethical considerations a central goal of their philosophy by attempting to “create a more level playing field for the future of a digital cultural record where the voices of those who have been excluded can be heard and valued through a more equitable, collaborative approach to the labor of knowledge production” (<cite id="68vq5"><a href="#zotero%7C4951909%2FDUB54MKG">(Risam and Gil 2022)</a></cite>). It is not the case, however, that only minimal computing leads to ethical outcomes. The digital humanities and digital history can take up these considerations more broadly both as discussions in the classroom and in choosing technologies that fit the needs of students and instructors.
<!-- #endregion -->

<!-- #region editable=true slideshow={"slide_type": ""} -->
How we teach and what technologies we use or do not use in the classroom define in many ways the parameters, the limits, the possibilities of digital history. These are not peripheral concerns, but central to the question of what digital history is and what it will become.
<!-- #endregion -->
