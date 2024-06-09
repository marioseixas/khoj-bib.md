Process Mining-Enabled Jurimetrics

Analysis of a Brazilian Court’s Judicial Performance in the Business Law Processing

Adriana Jacoto Unger
José Francisco dos Santos Neto
Marcelo Fantinato
Sarajane Marques Peres
{ajacoto,jose.francisco.neto,m.fantinato,sarajane}@usp.br
University of Sao Paulo
Sao Paulo, Brazil

Julio Trecenti
Renata Hirota
{jtrecenti,rhirota}@abj.org.br
Brazilian Jurimetrics Association
Sao Paulo, Brazil

ABSTRACT
Improving judicial performance has become increasingly relevant
to guarantee access to justice for all, worldwide. In this context,
technology-enabled tools to support lawsuit processing emerge as
powerful allies to enhance the justice efficiency. Using electronic
lawsuit management systems within the courts of justice is a widespread
practice, which also leverages production of big data within
judicial operation. Some jurimetrics techniques have arisen to evaluate
efficiency based on statistical analysis and data mining of data
produced by judicial information systems. In this sense, the process
mining area offers an innovative approach to analyze judicial
data from a process-oriented perspective. This paper presents the
application of process mining in a event log derived from a dataset
containing business lawsuits from the Court of Justice of the State
of Sao Paulo, Brazil – the largest court in the world – in order to
analyze judicial performance. Although the results show these lawsuits
have an ad hoc sequence flow, process mining analysis have
allowed to identify most frequent activities and process bottlenecks,
providing insights into the root causes of inefficiencies.

CCS CONCEPTS
• Applied computing → Law; Business process management; Business
intelligence; • Information systems → Data mining.

KEYWORDS
Process mining, jurimetrics, judicial performance, administration of
justice, legal informatics, business process management, procedural
law, business law.
ACM Reference Format:
Adriana Jacoto Unger, José Francisco dos Santos Neto, Marcelo Fantinato,
Sarajane Marques Peres, Julio Trecenti, and Renata Hirota. 2021. Process
Mining-Enabled Jurimetrics: Analysis of a Brazilian Court’s Judicial Performance
in the Business Law Processing. In Eighteenth International Conference
for Artificial Intelligence and Law (ICAIL’21), June 21–25, 2021, São

Permission to make digital or hard copies of all or part of this work for personal or
classroom use is granted without fee provided that copies are not made or distributed
for profit or commercial advantage and that copies bear this notice and the full citation
on the first page. Copyrights for components of this work owned by others than the
author(s) must be honored. Abstracting with credit is permitted. To copy otherwise, or
republish, to post on servers or to redistribute to lists, requires prior specific permission
and/or a fee. Request permissions from permissions@acm.org.
ICAIL’21, June 21–25, 2021, São Paulo, Brazil
© 2021 Copyright held by the owner/author(s). Publication rights licensed to ACM.
ACM ISBN 978-1-4503-8526-8/21/06. . .$15.00
https://doi.org/10.1145/3462757.3466137

Paulo, Brazil. ACM, New York, NY, USA, 5 pages. https://doi.org/10.1145/
3462757.3466137

1 INTRODUCTION
Within the administration of justice, electronic lawsuits and management
information systems emerged to control lawsuit processing
in the courts of justice. These systems allow the practice of
procedural acts by magistrates and other participants in lawsuits in
a fully digital environment. Since 2015, the Court of Justice of the
State of Sao Paulo (TJSP1
), Brazil, is 100% digital, i.e., all new lawsuits
born digital. TJSP is considered the largest court in the world in
terms of volume of lawsuits2
, with over 19 million ongoing lawsuits,
managed by the Justice Automation System (e-SAJ3
). Data-centric
analysis techniques, such as jurimetrics [11] and machine learning
[14], take advantage of the increasing availability of judicial data.
Jurimetrics supports statistics-based analysis on justice big data. In
this sense, process mining [20] emerges as an approach to bridge
data mining to Business Process Management (BPM), providing a
process-oriented perspective which turns out to be more valuable
when analyzing phenomena distinguished by procedural behaviour,
such as in lawsuit processing ruled by procedural law.
This paper presents an innovative application of process mining
to analyze judicial performance based on a lawsuit dataset, as a
proof of concept for process mining-enabled jurimetrics. The experiment
was restricted to business law, as it is an area of law that
commonly presents poor judicial performance and difficulties in
diagnosis due to its high heterogeneity. This study raises and highlights
contributions of process mining showing the benefits of a
process-oriented approach to analyzing legal data for performance
diagnostics. The paper is divided as follows: background, presenting
the theoretical framework of this work; related work, pointing
out prior research related to this topic; research method, describing
the stages of this research study; results, showing results of the
process mining application; analysis of the results, presenting process
mining-enabled analysis of lawsuit processing; and conclusion,
which highlights the research findings.

2 BACKGROUND
This section introduces the main theoretical concepts related to
this work, contextualized in the Brazilian setting.

1Tribunal de Justiça de São Paulo (in Portuguese)
2http://www.tjsp.jus.br/QuemSomos
3
Sistema de Automação da Justiça (in Portuguese)

240
ICAIL’21, June 21–25, 2021, São Paulo, Brazil Unger et al.

2.1 Judicial Performance
Judicial performance is a field of study dedicated to evaluate performance
of judicial systems and courts of justice [8]. Some international
organizations conducted studies to measure and compare
judicial performance worldwide [10, 17]. In Brazil, the National
Council of Justice provides the Justice in Numbers annual report
[5], offering an overview of the judiciary productivity.
Current models for judicial performance evaluation contributed
substantially to the continuous measurement, monitoring and comparison
of judicial performance. However, such evaluation models
have done little to guide improvement actions. Identifying the root
causes of inefficiencies is often limited due to the asymmetry of
information among the courts’ information systems, as well as the
lack of detailed data on the activities of lawsuit processing [1].

2.2 Jurimetrics
Jurimetrics [11] is defined as ‘statistics applied to the law’. Although
it emerged decades ago, recent advances in computing and data
storage capabilities have enabled alternative ways of observing
patterns in data-based and hence statistics-based court decisions.
In the USA, the application of statistics to law has been developed
under alternative nomenclature, such as Empirical Legal Studies
[7] and, more recently, Judicial Analytics [4]. In Brazil, jurimetrics
has received growing interest [12].
When analyzing alternative ways of managing the lawsuit processing,
the analysis of the lawsuit throughput time using jurimetrics
techniques may present quality issues, as it eventually considers
inadequate time intervals for the object of analysis [3]. Procedural
viscosity [16], defined as “a set of structural characteristics of a
lawsuit that is able to affect the speed of its processing”, may apply.
Specifically in business law, processing of lawsuits may require
about twice as much effort as a common lawsuit [2]. The same
authors suggest “future research focused on process flow analysis,
i.e., the study of the stochastic process that generates all events and
timestamps of lawsuit processing”.

2.3 Process Mining
Process mining [20] emerged as a set of techniques for mining
business process-related information from event data logged by
information systems. A business process is a chain of activities that
produces an outcome that adds value to an organization and its
customers [6]. Business process models play a dominant role during
BPM life cycle, leading in achieving organizational improvement
goals, including reducing costs, lead times, and error rates. By using
real event data to discover process models, process mining leverages
data mining to understand operational processes in organizations.
Table 1 shows the mapping of the basic elements of event logs
from the process mining perspective to their counterparts in the
procedural law domain.

3 RELATED WORK
Process mining should be seen as an analytical tool naturally suitable
for lawsuits due to their inherently procedural nature. It is
cited as a promising approach to suggest improvements for lawsuit
processing [15]. Lawsuit digitization is presented as not being an

Table 1: Process mining in procedural law

Process mining Procedural law

Activity Name of the lawsuit procedural movement.
Event Occurrence of a procedural movement, i.e., occurrence
of a lawsuit’s procedural progress.
Timestamp Date of occurrence of the lawsuit’s procedural
movement.
Case Lawsuit.
Case ID Lawsuit identifier.
Event attributes General attributes related to the movement.
Case attributes General attributes related to the lawsuit.

end in itself, so that process mining can enhance the way the judiciary
treats its digital data through the application of algorithms for
process discovery, compliance and predictive analysis [9]. A technical
report with suggested actions to improve judicial efficiency
highlights the use of process mining as one of these actions [3].
Nevertheless, few studies on this topic were found in the literature.
Empirical studies were performed using lawsuit data from
Brazilian courts[19, 22] though focused on comparison of lawsuit
throughput times. Attempts to apply data mining to extract information
from lawsuit data were made [13, 18], but these studies do
not directly address process mining on that data.

4 RESEARCH METHOD
This study applied the Process Mining Project Methodology [21] to
guide the application of process mining to analyze judicial performance
in a specific context. Only the first five stages of the method
were carried out: planning, extraction, data processing, mining and
analysis, and evaluation. The project was finished with the insights
generated by the evaluation stage. Besides restricting the scope to
business law, a period of analysis was defined to consider only the
TJSP’s lawsuits distributed between January 1, 2018 and July 21,
2020. All lawsuits with a procedural movement published in that
time interval were considered. Full progress data for each lawsuit
was retrieved until July 31, 2020, including lawsuits opened before
and lawsuits not yet closed.
The data were extracted in two steps. First, the identifiers of
lawsuits of interest were obtained. For this, all issues of the TJSP’s
Electronic Journals of Justice (DJE4
) were downloaded from the DJE
website5
, considering the defined analysis period. DJE publishes information
on provisional or final decisions for all ongoing lawsuits
at TJSP, daily. An automated scraping of these files was carried out
using keywords associated with business law litigation. Second,
the lawsuit identifiers obtained were used to retrieve data from
the e-SAJ website6
, where information on lawsuits is published. A
web scraping was carried out to retrieve information on lawsuits
attributes and progress events including their respective dates. In
TJSP, there are four filing court departments dedicated to business

4Diário da Justiça Eletrônico (in Portuguese)
5http://www.dje.tjsp.jus.br
6http://esaj.tjsp.jus.br

241
Process Mining-Enabled Jurimetrics ICAIL’21, June 21–25, 2021, São Paulo, Brazil

law; as a result, the lawsuits not filed at these four court departments
were discarded. Data from both DJE and e-SAJ websites are
publicly available7
.
The process knowledge transfer with domain experts was carried
out, resulting in a mapping between the elements of the dataset
and the concepts of event log used by process mining, presented
in Table 2. Event data from lawsuits were used to create the event
log to be used in process mining. The lawsuit dataset was filtered
to remove columns with missing values or data not relevant to the
scope of this study. The judge column was made anonymous for
protecting personal data. The additional column order was added
to the movement database, and hence to the event log, to allow the
process mining discovery algorithm to identify the correct order of
activities within a case occurring on the same date.

5 RESULTS
The resulting event log contains data on lawsuits referring to 4,795
cases and 266,834 events, with procedural movements dating back
to 2008, and 10 case attributes, as described in Table 2. The event log
file8 was imported using the EverFlow9 process mining tool, which
produced the business process maps and the main process metrics,
such as number of cases, number of events, and average duration,
as presented in Figure 1 and Figure 3. Process map views are userinteractive,
so that activities, transitions, and the time interval can
be selected and filtered for drill-down analysis. Detailed views on
specific metrics are presented on dedicated dashboards and panels,
as shown in Figure 2, Figure 4, Figure 5 and Figure 6.

Figure 1: Process map of the lawsuit processing

6 ANALYSIS OF THE RESULTS
As a proof of concept for process mining-enabled jurimetrics, the
results were analyzed considering each of the following process
mining perspectives: control-flow, time, resource, and case [20].

6.1 Control-flow Perspective
The control flow is the main perspective considered in process
mining discovery, adding process-oriented value to the data mining
7The right of access to judicial data in Brazil is guaranteed by the constitutional
principle of judicial publicity, except in lawsuits protected by the secrecy of justice.
8The event log file is available in the repository: https://doi.org/10.4121/14593857
9http://everflow.ai

Figure 2: Histogram of procedural movements by lawsuit

Figure 3: Process map based on average duration metrics

Figure 4: Slow transition analysis panel

analysis of the event log, as shown in Figure 1. The complexity
and procedural viscosity of lawsuits in business law can be verified
by the process metrics, i.e., average rate of 55.6 events per case
and average case duration of 334 days. As shown in Figure 2, over
10% of lawsuits have over 100 events per case, which corresponds
to procedural movements during lawsuit processing. In addition,
one can verify that lawsuit processing in business law has an ad

242
ICAIL’21, June 21–25, 2021, São Paulo, Brazil Unger et al.

Table 2: Judicial data mapped to process mining event log

Dataset column Data description Event log role

lawsuit_id Lawsuit identifier. Case ID.
movement Name of the lawsuit procedural movement. Event activity.
date Date of occurrence of the lawsuit’s procedural movement. Event timestamp.
order Sequential order of occurrence of the lawsuit’s procedural movement. Event attribute.
area Law area to which the lawsuit refers. Case attribute.
claim_amount Lawsuit claim amount. Case attribute.
class Procedural class (refers to specific law or claim reason). Case attribute.
control Internal control number. Case attribute.
court_department Filing court department. Case attribute.
digital It shows whether the process is digital (born digital or scanned) or on paper. Case attribute.
distribution_date Date and time when the lawsuit was distributed. Case attribute.
judge Name of the ruling judge for the lawsuit. Case attribute.
status Lawsuit status. Case attribute.
subject_matter Main topic of the lawsuit. Case attribute.

Figure 5: Lawsuits by judge dashboard

Figure 6: Comparative analysis between on-paper and digital
lawsuits

hoc sequence flow, characterized by the large number of process
variants. The most frequent control-flow is shared among 155 cases,
which represents only 3% of all lawsuits. The extended process map
in Figure 1 shows the process control-flow considering only 4.19%
of cases. Figure 1 also highlights the most frequent activities and
event counting for each transition.

6.2 Time Perspective
The analysis of the lawsuit throughput time using process mining
techniques is favored by the easy handling of incomplete cases,
considering the activities carried out in the sequence flow. Since
the full progress data for each lawsuit was retrieved, there is no
issue related to the beginning of the process (i.e., lawsuit opening).
However, the lawsuit processing time evaluation can be affected by
cases that did not ended (i.e., lawsuits not yet closed). The Definitely
Archived activity is the most frequent final activity, which confirms
the natural behaviour of lawsuit processing within the court. It is
the final activity in 20% of the cases, which represents the number of
closed lawsuits in the dataset. By filtering all cases that go through
this activity, the lawsuit throughput time for closed lawsuits can
be calculated as 312 days.
Furthermore, based on the process map in Figure 3, one can
identify highlighted slow transitions and activity bottlenecks. These
transitions are also listed in the slow transition analysis panel
in Figure 4, which offers a detailed diagnostics on each of them.
Comments on some slow transitions of the lawsuit processingrelated
business process are presented in the following:

• Transition between Issued Publication Certificate and Issued
Judicial Office Certificate activities, with duration of 18 days
and effort of 121 years and 209 days, affecting 38% of cases:
this is a clear bottleneck within the court department. After
the publication certificate is issued, the judicial office publication
certificate must be issued. However, there is a long
waiting time due to the lack of human resources on the court.
This bottleneck has a high impact on lawsuit processing time
and the use of court resource, suggesting that this activity is
a good candidate for automation solutions.
• Transition between Issued Publication Certificate and Suspension
of the Term activities, with duration of 21 days and effort
of 164 years and 258 days, affecting 42% of cases: bottleneck
possibly due to litigant issues, such as lack of required documentation.
Figure 4 shows that this transition causes the
average duration of the case to increase by 77%.

243
Process Mining-Enabled Jurimetrics ICAIL’21, June 21–25, 2021, São Paulo, Brazil

• Transition between Suspension of the Term and Conclusions
for Decision activities, with duration of 13 days and effort of
19 years and 298 days, affecting 10% of cases: this bottleneck
is related to the previous one, possibly due to the judge being
unable to evaluate the case for proper decision making.

6.3 Resource Perspective
The resource perspective analysis allows process maps and metrics
to be evaluated considering the resources (people or devices) that
execute the process activities. In addition, the values of the process
execution effort can be evaluated based on the average duration
and event counting for each activity. Performance and comparative
analysis of lawsuit processing from the resource perspective were
carried out based on the judge attribute, as shown in Figure 5.

6.4 Case Perspective
The case perspective allows performance diagnostics to be carried
out considering specific case attributes. Considering the digital case
attribute, a side-by-side comparison was carried out to analyze how
this attribute impacts process flow and metrics. Surprisingly, Figure
6 shows that digital lawsuits are 6% slower than the on-paper ones.
Some considerations on these findings are as follows:

• The definition of the digital attribute includes both the born
digital lawsuits and the scanned ones, although the scanned
ones usually require more time and effort to be processed.
It is not possible to distinguish them by the value of this
attribute, but further investigation on procedural movements
may confirm this assumption, if scan activities are logged.
• Procedural viscosity in business law might hide inefficiencies
usually associated with on-paper lawsuits, which means
that the main process bottlenecks in business law might
be related to internal activities that are independent of the
digital nature of lawsuits. However, this statement requires
further investigation, since digital lawsuit management is
often associated with performance gains.
• A data selection bias may have occurred due to the analysis
period, as it is not uncommon for dedicated task forces to
occur within court departments to reduce the backlog of
on-paper lawsuits.

7 CONCLUSION
The analysis of the results revealed a comprehensive set of diagnostic
metrics, insights into the root causes of inefficiencies, and
ideas for improvement, which would hardly be discovered without
a process-oriented analysis approach. The prospects for using process
mining in the Brazilian judiciary include the use of process
mining tools to provide online dashboards for judicial performance
monitoring by the State Internal Affairs Divisions of Justice, which
monitors the performance on the provision of jurisdictional services.
These dashboards can be used to identify inefficiencies in
near real time and define targets for resolving them.

ACKNOWLEDGMENTS
The authors thank the EverFlow company for kindly supporting
this research.

REFERENCES
[1] Bruna Armonas Colombo, Pedro Buck, and Vinicius Miana Bezerra. 2017. Challenges
When Using Jurimetrics in Brazil—A Survey of Courts. Future Internet 9,
4 (10 2017), 68. https://doi.org/10.3390/fi9040068
[2] Associação Brasileira de Jurimetria. 2016. Estudo sobre varas empresariais na
Comarca de São Paulo. Technical Report. Associação Brasileira de Jurimetria. 20
pages. https://abj.org.br/pdf/ABJ_varas_empresariais_tjsp.pdf (in Portuguese).
[3] Associação Brasileira de Jurimetria. 2020. Justiça Pesquisa - Formas Alternativas
de Gestão Processual: a especialização de varas e a unificação de
serventias. Technical Report. Conselho Nacional de Justiça, Brasília. 126
pages. https://www.cnj.jus.br/wp-content/uploads/2020/08/Justica-Pesquisa_
Relatorio_ABJ_2020-08-21_1.pdf (in Portuguese).
[4] Daniel L. Chen. 2019. Judicial analytics and the great transformation of American
Law. Artificial Intelligence and Law 27, 1 (3 2019), 15–42. https://doi.org/10.1007/
s10506-018-9237-x
[5] Conselho Nacional de Justiça. 2020. Justiça em Números 2020: anobase
2019. Technical Report. Conselho Nacional de Justiça, Brasília. 267
pages. https://www.cnj.jus.br/wp-content/uploads/2020/08/WEB-V3-Justiçaem-Números-2020-atualizado-em-25-08-2020.pdf
(in Portuguese).
[6] Marlon Dumas, Marcello La Rosa, Jan Mendling, and Hajo A. Reijers. 2018. Fundamentals
of Business Process Management (2 ed.). Springer, Berlin. 527 pages.
https://doi.org/10.1007/978-3-662-56509-4
[7] Theodore Eisenberg. 2011. The origins, nature, and promise of empirical legal
studies and a response to concerns. University of Illinois Law Review 2011, 5
(2011), 1713–1738. https://doi.org/10.2139/ssrn.1727538
[8] Adalmir de Oliveira Gomes and Tomás de Aquino Guimarães. 2013. Desempenho
no judiciário. Conceituação, estado da arte e agenda de pesquisa. Revista de
Administracao Publica 47, 2 (3 2013), 379–401. https://doi.org/10.1590/S0034-
76122013000200005 (in Portuguese).
[9] Bráulio Gusmão. 2021. Mineração de processos e gestão de casos no judiciário.
In Inteligência Artificial e Direito Processual: os impactos da virada tecnológica no
direito processual (2 ed.), Dierle Nunes, Paulo Henrique dos Santos Lucon, and
Erik Navarro Workart (Eds.). JusPodivm, Salvador, 589–594. (in Portuguese).
[10] International Consortium for Court and Excellence. 2020. Global Measures of
Court Performance. Technical Report. Secretariat for the International Consortium
for Court Excellence, Sydney, Australia. 112 pages. http://www.courtexcellence.
com/resources/global-measures
[11] Lee Loevinger. 1948. Jurimetrics–The Next Step Forward. Minnesota Law Review
33, 5 (1948), 455–493.
[12] Marcos Maia and Cicero Aparecido Bezerra. 2020. Bibliometric analysis of scientific
articles on jurimetry published in Brazil. Revista Digital de Biblioteconomia e
Ciência da Informação 18 (2020). https://doi.org/10.20396/RDBCI.V18I0.8658889
[13] Oleg Metsker, Egor Trofimov, Sergey Sikorsky, and Sergey Kovalchuk. 2019. Text
and data mining techniques in judgment open data analysis for administrative
practice control. In Communications in Computer and Information Science, Vol. 947.
Springer, Cham, 169–180. https://doi.org/10.1007/978-3-030-13283-5_13
[14] Tom M. Mitchell. 1997. Machine Learning. McGraw-Hill Science/Engineering/Math.
432 pages.
[15] Dierle Nunes. 2021. A technological shift in procedural law (from automation
to transformation): Can legal procedure be adapted through technology? In
Inteligência Artificial e Direito Processual: os impactos da virada tecnológica no
direito processual (2 ed.), Dierle Nunes, Paulo Henrique dos Santos Lucon, and
Erik Navarro Workart (Eds.). JusPodivm, Salvador, 55–78.
[16] Marcelo Guedes Nunes. 2019. Jurimetria: como a estatística pode reinventar o
Direito (2 ed.). Revista dos Tribunais, São Paulo. 192 pages. (in Portuguese).
[17] Giuliana Palumbo, Giulia Giupponi, Luca Nunziata, and Juan Mora-Sanguinetti.
2013. Judicial performance and its determinants: a cross-country perspective.
OECD Economic Policy Papers 5 (2013), 1–38. https://doi.org/10.1787/
5k44x00md5g8-en
[18] Shahmin Sharafat, Zara Nasar, and Syed Waqar Jaffry. 2019. Data mining for
smart legal systems. Computers and Electrical Engineering 78 (9 2019), 328–342.
https://doi.org/10.1016/j.compeleceng.2019.07.017
[19] Universidade de São Paulo. 2019. Justiça Pesquisa - Mediações e Conciliações
Avaliadas Empiricamente: jurimetria para proposição de ações eficientes. Technical
Report. Conselho Nacional de Justiça, Brasília. 193 pages. https://www.cnj.
jus.br/wp-content/uploads/2011/02/e1d2138e482686bc5b66d18f0b0f4b16.pdf (in
Portuguese).
[20] Wil M. P. van der Aalst. 2016. Process mining: Data science in Action (2 ed.).
Springer, Berlin. 467 pages. https://doi.org/10.1007/978-3-662-49851-4
[21] Maikel L. van Eck, Xixi Lu, Sander J. J. Leemans, and Wil M. P. van der Aalst.
2015. PM2: A process mining project methodology. In Lecture Notes in Computer
Science, Vol. 9097. Springer, Cham, 297–313. https://doi.org/10.1007/978-3-319-
19069-3_19
[22] Caio Castelliano de Vasconcelos, Eduardo Watanabe de Oliveira, Henrique Pais da
Costa, and Tomas de Aquino Guimaraes. 2018. Tempo de Processos Judiciais
na Justiça Federal do Brasil. In XLII Encontro da ANPAD. Curitiba, 1–16. http:
//www.anpad.org.br/abrir_pdf.php?e=MjQ1NzA= (in Portuguese).

244