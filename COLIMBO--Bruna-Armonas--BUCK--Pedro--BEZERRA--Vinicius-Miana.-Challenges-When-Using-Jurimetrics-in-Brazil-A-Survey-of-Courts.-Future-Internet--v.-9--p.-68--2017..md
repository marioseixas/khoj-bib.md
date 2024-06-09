future internet

Article
Challenges When Using Jurimetrics in Brazil—A
Survey of Courts

Bruna Armonas Colombo 1
, Pedro Buck 1 and Vinicius Miana Bezerra 2,*
ID

1 Law School, Mackenzie University, São Paulo, SP 01302-907, Brazil; bruna.armonas@gmail.com (B.A.C.);
pedrobuck@gmail.com (P.B.)
2
Informatics and Computing Department, Mackenzie University, São Paulo, SP 01302-907, Brazil
* Correspondence: vinicius@miana.com.br; Tel.: +55-11-2114-8301
Received: 1 October 2017; Accepted: 16 October 2017; Published: 25 October 2017

Abstract: Jurimetrics is the application of quantitative methods, usually statistics, to law.
An important step to implement a jurimetric analysis is to extract raw data from courts and organize
that data in a way that can be processed. Most of the raw data is unstructured and written in natural
language, which stands as a challenge to Computer Science experts. As it requires expertise in law,
statistics, and computer science, jurimetrics is a multidisciplinary field. When trying to implement
a jurimetric system in Brazil, additional challenges were identified due to the heterogeneity of the
different court systems, the lack of standards, and how the open data laws in Brazil are interpreted
and implemented. In this article, we present a survey of Brazilian courts in terms of readiness to
implement a jurimetric system. Analyzing a sample of data, we have found, in light of Brazil’s open
data regulation, privacy issues and technical issues. Finally, we propose a roadmap that encompasses
both technology and public policy to meet those challenges.

Keywords: jurimetrics; legal informatics; public policy; open data; computacional law; e-government

1. Introduction

Jurimetrics is the application of quantitative methods, usually statistics, to law. By using a
quantitative approach to analyze judicial decisions, it is possible to identify patterns and outliers,
making it possible to forecast the outcome of a court decision and thus making the law more predictable.
Due to its nature Jurimetrics requires a multidisciplinary approach in which statistics and computer
science and law experts work together to solve framework and access problems [1]. Such an approach
also requires computer systems able to store and process the judicial decision, but mostly important an
online access to such decisions are required.
In Brazil, judicial process has been required to implement a digital mandatory procedure by 2006,
when Federal Act n. 11.419/06 [2] fostered the use of electronic documents in the proceedings of a
court of law. The law allowed the courts to implement systems to handle the judicial processes, but it
did not require them to do so and did not define any standards for its format. It recommended the use
of standards, open source, and that it should be accessible through the internet, but the courts were not
legally required to do so. Slowly, many courts adopted the use of electronic documents but followed
different paths. The Brazilian Freedom of Information Act (FIA)—Federal Act n. 12.527/2011 [3]—gave
the courts the obligation to make the data available to every citizen, but the implementation of this law
also varied widely.
Empirical research in law is not a new field: jurimetric was defined in 1949 [1]. However, in Brazil,
due to the late arrival of electronic documents and the difficulty to access information from courts,
quantitative-driven research agendas gained some visibility only in 2011, when first papers were
published in local journals. They were mainly focused in reviewing jurimetrics state of art and

Future Internet 2017, 9, 68; doi:10.3390/fi9040068 www.mdpi.com/journal/futureinternet
Future Internet 2017, 9, 68 2 of 14

mostly did not use statistics or computational techniques. The use of statistical analysis and the use
of computational techniques for access and analysis of judicial decisions became more frequent by
2013 [4]. For instance, Castro [4] uses descriptive statistics in order to identify the percentage of use of
protective measures different from imprisonment by the judiciary, and Nunes and Trecenti [5] made
use of computational techniques to capture, processing, and analyze 157,379 court rulings.
This paper presents an exploratory study of the Brazilian courts through which we address the
subject from a legal and technological point of view. The paper is composed of five parts. In the next
section, we present the methodology used in the survey. Then we present the Brazilian Freedom of
Information Act (FIA) [3] and all the legal framework in which we are inserted and how the laws are
helping or hampering the implementation of jurimetric systems. Following that, we present the survey
results and finally, the conclusions of this study.

2. Methodology

This work aims to determine the readiness of Brazilian courts for the implementation of jurimetric
systems. In order to assess that, we started with the following hypothesis:

• Hypothesis 1: The legal framework is not enough;
• Hypothesis 2: Current systems are preventing progress in this area as they do not follow any
standard and many have implemented measures that do now allow automated data gathering
(robots);
• Hypothesis 3: Courts are not prepared and neither abide by the current laws.

In order to validate these hypothesis, this paper uses a multimethod approach. To validate
hypothesis 1, we promote a review of the methodological literature regarding access to judicial
data and the current laws in Brazil. To validate hypothesis 2, we evaluated courts website. Finally,
to validate hypothesis 3, we employed a tool regulated by the Brazilian Freedom of Information Act
(FIA) [3], entitled as Access to Information Procedure (AIP).
The aforementioned tool allows citizens or researchers to contact public agencies either to obtain
answers concerning their routines or to have access to whatever data sets they are responsible for.
Once provoked, the agency has a 20-day period to provide an answer (which can be extended to a
30-day response time deadline) [3].
Due to this tool, we have addressed a court website survey before the 26 state courts, the DC court,
and two national courts (Supreme Court of Justice and Superior Court of Justice), a set comprised of
29 observations.
With the results of the survey, we have organized the information into an analytical framework.

3. Brazil’s Freedom of Information Act

3.1. Legal Framework

Access to information is a universal right, and the legal framework for it dates back to the
Universal Declaration of Human Rights [6], where article 19 declares that every human being has the
right to freedom of opinion and expression. The United Nations Convention against Corruption [7],
in articles 10 and 13, also recommends that each state party shall take the necessary measures and
actions to improve the transparency of public administration, thus providing access to information
about your organization, operation, and, above all, of its decision-making processes. Finally, the fourth
item of the Inter-American Declaration of Principles of Freedom of Speech [8] reaffirms the need for
access to information and proclaims this as a fundamental right of the individual.
In Brazil, the guarantee of access to information is ensured by item XXXIII of article 5 of the
Brazilian Federal Constitution (1988) [9], which says: “everyone has the right to receive information
from public information bodies of one’s particular, or collective or general interest.” However, despite
the existence of this provision, formal and structured access only become nationally enforceable in
Future Internet 2017, 9, 68 3 of 14

2011 due to the enacting of a bill that regulated the forms of access to information [3], establishing that
the information produced by the state is public and its secrecy the exception.
This bill is the Federal Act 12,527/2011—Brazilian Freedom of Information Act (FIA) [3]—which
establishes that the activity of agencies throughout the public administration shall be available to the
public by default. In addition, sets forth a minimum list of information to be included in the agency
internet sites, for example, institutional information, records of expenditure values and transfers, bids,
contracts, general data allowing the monitoring of programs and projects, among others.
In this context, the transparency of information can be divided into two categories: active and
passive transparency. The first relates to the publication of information on the agency internet site.
The second category relates to information that is not published and therefore there is a need to request
it to the holder of the information. To make sure that information in the second category was made
available, the law established a mechanism—the Access to Information Procedure (AIP) to request it
as well as the duty of the agency to provide it when requested [3].
Since 2009, the Brazilian National Council of Justice (CNJ) established the need for dissemination
of information about the activities performed by Brazilian courts. Examples include the issue of
Resolutions 79 [10] and 102 [11], both from 2009, which advocate for the dissemination of budget,
management, governance, revenues, expenses and payroll. When the FIA was issued [3], the CNJ
published a new resolution in order to clarify the need for dissemination of information on the amount
spent with travel expenses, bonuses and reimbursements—Resolution 151/2012-CNJ [12].
Finally, in 2015, the CNJ edited new Resolution 215/2015 [13], which incorporated the legal
concepts of the previous regulations and compiled them in a single instrument that regulates the
access to information. This normative instrument reaffirmed the guidelines and principles of FIA
and, among other measures, determined the dissemination of information on the functioning of the
Brazilian Justice in plain and accessible language, presented the minimum information that needs
to be published, established which types of information will not be given and what information is
restricted, and defined which trials should be publicized, establishing the need of live video stream for
such sessions and that the recording and minutes should be available on the internet.

3.2. Judicial Courts and the Access to Information Procedure (AIP)

Despite the legal framework, which aims to ensure access to information, whenever one is willing
to access information that goes beyond a query to a single process, the user finds many barriers,
as computer systems to access data are not available for most information, and there are anti-robot
barriers, including captchas that make downloading data in bulk, advanced searches, and other tasks
important in a research a tedious, repetitive, and error prone task [14].
The Open Society Justice Initiative [15], by analyzing this subject in countries of the Americas,
stressed that the development of access to judicial information must follow the same purposes adopted
by the Executive power: the guarantee of transparency, greater efficiency and effectiveness, and greater
confidence in the Judiciary, and the concern about the exposure of sensitive information and how to
curtain it without censorship. In this context, judicial information systems should be able to ensure:
the independence of the judiciary; fair and efficient administration of Justice; protecting the privacy of
the judges, the parties and other participants in the judicial process; ensure the safety of parties, judges
and other participants in the process and guarantee the public and media access to the proceedings,
in order to ensure the right of society to know what occurs in the Justice system.
The study “Access to information and Transparency in the Judiciary developed by the World
Bank Institute” [16] suggests that, with regard to the judicial function, access to information in the
courts includes topics such as the publishing of rulings, access to proceedings in cases of corruption
involving public officials, information on the operation of Upper Courts, transparency in the judicial
sessions, and mechanisms for the participation of the civil society. According to this study, it is up to
the Judiciary to ensure the transparency of the information while it is executing its core activities [16].
Future Internet 2017, 9, 68 4 of 14

Artigo 19, a Brazilian watchdog NGO concerned about the FIA [3] implementation, draws
attention to the gray area that exists between the administrative and judicial information. This is
because some court decisions go beyond individual conflicts and impact society as a whole, as for
example in conflicts involving freedom of expression and information. In this regard, it is suggested
that the observance of the FIA, in fact, is only one aspect of transparency in the judiciary [14].
Therefore, the actions of the judiciary can only be considered transparent if the dissemination
of information goes far beyond those determined by FIA. According to Artigo 19, the Judiciary must
also publish information produced as result of its main activities, such as information about access to
the judicial system and jurisprudence, information about an ongoing case progress, forms of social
participation, disclosure of agendas and schedules of hearings of the magistrate,; information about
the election of the Presidents of the courts and magistrate assignments, and information about the
process of nomination and appointment of Ministers to the Supreme Court [14].

3.3. Jurimetrics in the Context of the Fredoom of Information Act (FIA)

Research in Law, as an applied social science, tends to produce qualitative studies, which is why
quantitative research in this field is not common. The doctrine says that the quantitative method,
although not very usual in this field, can be of great value when you want to understand legal
phenomena of greater complexity [17].
The advent of law 11.419/06 [2], which rules on the digitalization of the judicial process and the
consequent use of integrated systems to handle the legal process, improved it productivity and it
allowed for the registration, storage, and retrieval of information quickly and reliably, making room
for the collection and analysis of judicial decisions to become systemic. This fact creates the possibility
of a new analytical approach, where the jurimetric approach becomes feasible and can come into play.
It allows for fast and objective gathering of data about how the law is being applied by querying
massive amounts of rulings and other jurisprudence from the legal court databases.
In 1971, Loevinger [1], in the article “Jurimetrics the Next Step Forward” published by the
Minnesota Law Review, coined the term “jurimetrics” to conceptualize the union of legal theory
with the computational and statistical methods with the purpose of analyzing jurisprudence in order
to make use of the law more predictable. Brazilian authors such as Nunes [18] defined the study
of jurimetrics as a form of empirical research that relies on a statistical approach. Nunes also says
that jurimetrics is the discipline that aims to investigate the law through the application of statistics.
Its purpose is to understand what the real causes that lead to the creation of standards that make up
the legal system are and what effects they produce in society [18].
In this context, the quantitative method depends on data collection and analysis to respond
to research questions and test the assumptions laid down previously and relies on numerical
measurement, counting of occurrences and in the use of statistics to establish with accuracy the
behavior patterns of a given population [19].
The legal system adopted in Brazil is civil law, and its legal system comprises ordinary justice,
which is divided into State and Federal courts, and special justice, which is divided into Labor, Electoral,
and Military specialties. Anything that falls outside the jurisdiction of the Federal or the Special Justice
is handled by the State System. The organizational standards of the judicial branch are defined in the
Federal Constitution [9,20].
Currently, the Brazilian judicial system has the following courts: the Federal Supreme Court
(STF), the Superior Court of Justice (STJ), the Superior Military Court (STM), the Superior Labor Court
(TST), the Superior Electoral Court (TSE), five Federal regional courts (TRFs), 24 Regional Labor Courts
(TRTs), 27 Regional Electoral Courts, three State Military Courts of Justice (TJMs), and 27 State Courts
of Justice (TJs) [20].
The Brazilian judiciary has 74 million litigations pending trial, where the State Courts are
responsible for 69.3% of all the claims presented before the Judicial Branch, nonetheless being
Future Internet 2017, 9, 68 5 of 14

responsible for 79.8% of the pending courts’ docket [21]. For this reason, this research focuses its
analysis on the 27 State Courts of Justice.

3.4. Jurimetrics in the Context of Data Access

Implementing jurimetric studies presents technological challenges, as the data is usually in a
free form text, and a variety of techniques need to be applied to extract the requested information.
Typically, a jurimetric study involves establishing a hypothesis and then gathering and processing the
data that could corroborate or refute the hypothesis. Some other studies are meant to provide statistical
information. In this case, instead of a hypothesis, we start with the definition of the data that we want
to consolidate, but in the end, it boils down to gathering and processing data. In order to gather the
data, information can be manually collected and typed in, or a script can be developed to gather the
data. Needless to say, data gathering will be more effective when it can be automated by a script [22].
To automate data gathering, one must create queries to get this data from its sources. Depending on
how the data is organized and what interfaces are available to the source, this task may be simple or nearly
impossible. Many sources impose blocks to automated querying, requiring human intervention. The most
common implementation of this blocks are CAPTCHAS, where before delivering the results, a challenge
that a machine would normally not be able to answer must be responded to [23]. These blocks are usually
implemented for two reasons: to prevent data theft and to prevent the server from being overloaded from
excessive queries. In the case of the courts, data theft is not an issue. However, there are some cases where
allowing someone to download the entire court database might become an issue. For example, it is illegal
for a potential employer to search for the labor lawsuits of a candidate. The Labor Court handles that by
only allowing users to query data from the process number. Also, the second reason is relevant, as it may
not be the best use of public money to finance servers that can handle automated queries.
To allow automated queries, some companies adopt an API (Application Program Interface),
which is a set of routines, protocols, and tools that allows software applications to talk to each other.
In order to avoid excessive use and therefore extra costs, an API requires the user to register before
using and imposes limits on hourly, daily, and/or monthly number of queries per user [24].
When an API is not available, automated queries will likely resort to web-scraping, a technique
that involves emulate a human browsing a web-site to gather the data. This process requires much more
programming effort and consumes more client and server process and data-transfer, as most of the data
is to make the information visually appealing to humans. To make matters worse, whenever a website
layout changes, even if the same information is displayed, the web-scraping program likely stops
working and needs to be updated. When a CAPTCHA is present, it is sometimes possible to implement
some routine to automatically “break” the CAPTCHA. In most cases, the process becomes partially
automatic, and the program halts for a human to answer the challenge to then resume web-scraping [25].
Another important barrier to automate data gathering is the lack of standards. To make computer
processing easier, the data should be organized and available in the same format in order to avoid
expensive ETL (Extract, Transform, Load) processes. The FIA [3] makes no provision in this sense,
and neither does any other regulation that followed it.

4. Results and Discussion

In order to verify if it was possible to gather judicial data from the Brazilian courts and its
readiness for jurimetric research, we developed an exploratory survey encompassing 29 Brazilian
courts of which two are Supreme Courts (STF and STJ) and 27 are the State Court of Justice belonging
to of each one of the States and the Federal District and Territories of Brazil.
The present study was divided into two parts. The first looked for official websites/search
engines/APIs available for each court included in this study. They were evaluated regarding
(1) standardization of systems available to search jurisprudence data, (2) standardization in relation to
the data returned by search, (3) difference in attributes returned by the search, (4) use of CAPTCHA,
and (5) possibility to download the full text of decisions.
Future Internet 2017, 9, 68 6 of 14

The second part was concerned with how the Access of Information Procedure (AIP) [3] was being
implemented in the researched courts in terms of law abiding and information management. The survey
looked into how each court handled the AIP requests sent, checking if they issue control number for the
requests, if all the court cases were available in digital format, which cases are published, if the documents
are universally accessible, and how often they update their public jurisprudence database. In total,
145 requests were sent to request this information using the FIA [3] as the legal base for the request.

4.1. Court Web Systems Survey

After looking into each of the 27 State Courts and two Supreme Courts, we found that no API
is provided to gather jurisprudence data, which means that any jurimetric study has to rely on
web-scraping of the court website. By reviewing each court website, it was found that there are no
standards in terms of search engine, search fields, and data shown as result of a search. Many courts
had a CAPTCHA in place, making automated queries harder to implement. Also, not all of the courts
allowed the download of the full court decision for a given case.
During the research, we found that the courts of the States of Santa Catarina and Rio de Janeiro are
changing their systems and provide two search engines for court cases, thus raising the total number
of court case search engines to 31 systems.
Regarding the development of these systems, the most commonly found option was in-house
development by the information technology staff member of the courts. Twenty-two of the 31 systems
were developed by the court’s own staff. As each one of these 22 systems were developed by a
different team, one would end up with 22 different proprietary systems to interface with and to build
a web-scraper for. In the case of the Rio de Janeiro State Court, the original system was developed
in-house, and in the case of the second one, called GSA, we could not identify whether it was in-house
or not. The remaining eight courts adopted the same system, called e-SAJ (Electronic System of
Automated Justice), developed by Softplan, one of the largest software development companies in
Brazil in the Justice, Infrastructure, and e-government segments (Figure 1). They did that regardless
of the fact that the National Justice Council (CNJ) determined that the courts should adopt another
system the Judicial Process Electronic System (PJe) [3,25].

Future Internet 2017, 9, 68 6 of 14

4.1. Court Web Systems Survey

After looking into each of the 27 State Courts and two Supreme Courts, we found that no API is
provided to gather jurisprudence data, which means that any jurimetric study has to rely on webscraping
of the court website. By reviewing each court website, it was found that there are no
standards in terms of search engine, search fields, and data shown as result of a search. Many courts
had a CAPTCHA in place, making automated queries harder to implement. Also, not all of the courts
allowed the download of the full court decision for a given case.
During the research, we found that the courts of the States of Santa Catarina and Rio de Janeiro
are changing their systems and provide two search engines for court cases, thus raising the total
number of court case search engines to 31 systems.
Regarding the development of these systems, the most commonly found option was in-house
development by the information technology staff member of the courts. Twenty-two of the 31 systems
were developed by the court’s own staff. As each one of these 22 systems were developed by a
different team, one would end up with 22 different proprietary systems to interface with and to build
a web-scraper for. In the case of the Rio de Janeiro State Court, the original system was developed inhouse,
and in the case of the second one, called GSA, we could not identify whether it was in-house
or not. The remaining eight courts adopted the same system, called e-SAJ (Electronic System of
Automated Justice), developed by Softplan, one of the largest software development companies in
Brazil in the Justice, Infrastructure, and e-government segments (Figure 1). They did that regardless
of the fact that the National Justice Council (CNJ) determined that the courts should adopt another
system the Judicial Process Electronic System (PJe) [3,25].

Figure 1. Distribution of jurisprudential search engines regarding how they were developed.

As to how one can search for information, the present study showed that there are no standards
in the number and type of fields available to find court cases. Two courts offer only one field, namely
search text, while there are courts that provide up to 20 fields. The same applies to the search results:
there are no standards in what is displayed as result, and the number and type of attributes vary
widely, as it can be seen in Figure 2.

Figure 1. Distribution of jurisprudential search engines regarding how they were developed.

As to how one can search for information, the present study showed that there are no standards
in the number and type of fields available to find court cases. Two courts offer only one field, namely
search text, while there are courts that provide up to 20 fields. The same applies to the search results:
there are no standards in what is displayed as result, and the number and type of attributes vary
widely, as it can be seen in Figure 2.
Future Internet 2017, 9, 68 7 of 14

Future Internet 2017, 9, 68 7 of 14

Figure 2. Number of fields available in the search engine per court and corresponding number of
attributes shown in results.

That difference between court data available and search parameters carries significant impact
on any research that involves a nationwide view of a comparison between Courts, as the search
methodology may not be available or the desired attribute may not be in the result data. This finding
corroborates with a report from Artigo 19 [14], which strongly advocates for standards in the
jurisprudence search engines, as they see it as fundamental for judicial transparency.
In relation to the use of CAPTCHA (Figure 3), which hinders the information requests that are
made by a machine, it was found that of the 29 surveyed, nine courts use it, and six of the courts that
use e-SAJ force the user to go through the challenge before have effective access to the content of
decisions. Finally, with respect to access and download of the full text of the decisions, the courts of
Justice of Espírito Santo and Goiás do not have this feature in their search engines. Another four
courts, namely Pará, Pernambuco, Rio de Janeiro (both systems), and Tocantins have the feature in
their web-system, but the feature does not work, which for practical terms is no different than the
former. This is not in compliance with the second article of resolution 121/2010-CNJ [26], which
ensures, to any person, the right to access to procedural information and the basic data of the
processes, such as the number, class and process issues, name of the parties, and their lawyers,
procedural timelines in lawsuits, and full text of the decisions, sentences, rulings, and votes, all of
which should be available at any time. The consolidated results can be seen in Figure 3.

Figure 2. Number of fields available in the search engine per court and corresponding number of
attributes shown in results.

That difference between court data available and search parameters carries significant impact
on any research that involves a nationwide view of a comparison between Courts, as the search
methodology may not be available or the desired attribute may not be in the result data. This
finding corroborates with a report from Artigo 19 [14], which strongly advocates for standards in the
jurisprudence search engines, as they see it as fundamental for judicial transparency.
In relation to the use of CAPTCHA (Figure 3), which hinders the information requests that are
made by a machine, it was found that of the 29 surveyed, nine courts use it, and six of the courts
that use e-SAJ force the user to go through the challenge before have effective access to the content of
decisions. Finally, with respect to access and download of the full text of the decisions, the courts of
Justice of Espírito Santo and Goiás do not have this feature in their search engines. Another four courts,
namely Pará, Pernambuco, Rio de Janeiro (both systems), and Tocantins have the feature in their
web-system, but the feature does not work, which for practical terms is no different than the former.
This is not in compliance with the second article of resolution 121/2010-CNJ [26], which ensures,
to any person, the right to access to procedural information and the basic data of the processes, such as
the number, class and process issues, name of the parties, and their lawyers, procedural timelines in
lawsuits, and full text of the decisions, sentences, rulings, and votes, all of which should be available at
any time. The consolidated results can be seen in Figure 3.
Future Internet 2017, 9, 68 8 of 14

Future Internet 2017, 9, 68 8 of 14

Figure 3. Number of courts using CAPTCHA compared with the number of courts that allows
download of the entire content of a case.

4.2. Access Information Procedure Survey

Law 12,527/11 [3] brings fundamental rules to ensure that a citizen can find information on
government websites (active transparency) and is able to request information not previously
provided by the government (passive transparency) through the Access Information Procedure (AIP)
[27]. Thus, the second part of the study sought to assess how the courts comply with the AIP and (i)
assess the information websites, (ii) map the procedure to be followed by a citizen if you want to
formulate request under the AIP, (iii) identify whether the courts searched have information
management policy, and (iv) analyze empirically the compliance by the courts that composed the
sample surveyed.
The study evaluated 29 Brazilian courts, the Courts of Justice of 27 States and Federal District
and Territories, and two superior courts. Thus, 145 requests for access to information were
formulated and sent from a single identity, through the internet, using the most relevant system in
each court: platforms dedicated to FIA, Ombudsman, contact us tools, email, or any other means
identified on their websites. For each court in the survey, we issued five requests under the AIP. All
requests were submitted in a single day, 5 September 2017.
The access requests had the following questions: (1) Does the Court have an information
management policy? If so, please specify the normative instrument that defines it and where it can
be found? (2) Are all court cases available in digital format? If so, are they available in the Court
website? (3) What procedural parts of a Court case are published (application, contestation,
dispatches, sentence, etc.)? (4) Are these documents universally accessible? In case of negative
answer, what was the reason for such restriction? (5) How often is the court case database available
in the Court website is updated?
Once the requests were sent, we waited for the replies until 25 September 2017, which is the last
day according to the AIP for the court to reply, in accordance with paragraph 1, article 11 of the LAI
[3], which states that under the AIP, it shall not take longer than twenty days to provide a response
or request for an extension of deadline.

4.2.1. Comparative Analysis of Information Access Platforms

The data contained in the Table 1 below refer to the platforms of all 29 courts that were object of
analysis. The first column identifies whether the court possesses specific platform for submissions of
applications for access to information request, in addition to the columns confirmation email,
registration required, email notification, and if it was possible to make an appeal. These attributes
were selected because they must be present in good transparency passive platforms, according to the
Brazilian State and Transparency-Evaluating the implementation of the Freedom of Information Act

Figure 3. Number of courts using CAPTCHA compared with the number of courts that allows
download of the entire content of a case.

4.2. Access Information Procedure Survey

Law 12,527/11 [3] brings fundamental rules to ensure that a citizen can find information on
government websites (active transparency) and is able to request information not previously provided
by the government (passive transparency) through the Access Information Procedure (AIP) [27]. Thus,
the second part of the study sought to assess how the courts comply with the AIP and (i) assess the
information websites, (ii) map the procedure to be followed by a citizen if you want to formulate
request under the AIP, (iii) identify whether the courts searched have information management policy,
and (iv) analyze empirically the compliance by the courts that composed the sample surveyed.
The study evaluated 29 Brazilian courts, the Courts of Justice of 27 States and Federal District
and Territories, and two superior courts. Thus, 145 requests for access to information were formulated
and sent from a single identity, through the internet, using the most relevant system in each court:
platforms dedicated to FIA, Ombudsman, contact us tools, email, or any other means identified on
their websites. For each court in the survey, we issued five requests under the AIP. All requests were
submitted in a single day, 5 September 2017.
The access requests had the following questions: (1) Does the Court have an information management
policy? If so, please specify the normative instrument that defines it and where it can be found? (2) Are all
court cases available in digital format? If so, are they available in the Court website? (3) What procedural
parts of a Court case are published (application, contestation, dispatches, sentence, etc.)? (4) Are these
documents universally accessible? In case of negative answer, what was the reason for such restriction?
(5) How often is the court case database available in the Court website is updated?
Once the requests were sent, we waited for the replies until 25 September 2017, which is the last
day according to the AIP for the court to reply, in accordance with paragraph 1, article 11 of the LAI [3],
which states that under the AIP, it shall not take longer than twenty days to provide a response or
request for an extension of deadline.

4.2.1. Comparative Analysis of Information Access Platforms

The data contained in the Table 1 below refer to the platforms of all 29 courts that were object of
analysis. The first column identifies whether the court possesses specific platform for submissions of
applications for access to information request, in addition to the columns confirmation email, registration
required, email notification, and if it was possible to make an appeal. These attributes were selected
because they must be present in good transparency passive platforms, according to the Brazilian State and
Future Internet 2017, 9, 68 9 of 14

Transparency-Evaluating the implementation of the Freedom of Information Act (FIA) [27]. The authors
highlight that international best practices of transparency advocate that government agencies, including
courts, making use of technology and adopt digital platforms to requests for access to information, as it
already occurs in Mexico, Chile, Canada, and other countries [27].

Table 1. Comparative analysis of information access platforms.

Court Name Web Interface Issues Control
Number
Sends E-mail
Confirmation Registered Users
TJ do Acre No Yes Yes No
TJ de Alagoas No Yes Yes No
TJ do Amapá No Yes Yes Yes
TJ do Amazonas No Yes Yes Yes
TJ da Bahia No Yes Yes Yes
TJ do Ceará No No No No
TJ do Distrito Federal e Territórios No No Yes No
TJ do Espírito Santo No Yes Yes No
TJ de Goiás No Yes No Yes
TJ do Maranhão No Yes Yes Yes
TJ do Mato Grosso No Yes Yes No
TJ do Mato Grosso do Sul No No Yes No
TJ de Minas Gerais No Yes Yes No
TJ do Pará No No No No
TJ da Paraíba No No Yes No
TJ do Paraná No Yes Yes Yes
TJ de Pernambuco No Yes Yes No
TJ do Piauí No Yes Yes No
TJ do Rio de Janeiro No Yes Yes Yes
TJ do Rio Grande do Norte No No No No
TJ do Rio Grande do Sul Yes Yes Yes Yes
TJ de Rondônia No Yes Yes Yes
TJ de Roraima No No No No
TJ de Santa Catarina No Yes Yes No
TJ de São Paulo Yes Yes Yes No
TJ de Sergipe No Yes Yes Yes
TJ de Tocantins No Yes Yes No
Superior Tribunal de Justiça Yes Yes Yes Yes
Supremo Tribunal Federal Yes Yes Yes No

Whereas the FIA [3] aims to guarantee constitutional right of access to information, the definition
and use of a web-based platform different from the traditionally used channels for other purposes
assumes importance in the implementation of law [27]. In this respect, it was found that 86.2% of
the courts searched do not have their own platform to meet the requests for access to information,
and make use of communication channels designed for other purposes, such as Ombudsman and
Contact Us.
There is, therefore, a misuse of communication channels that were meant for another purpose in
order to provide a means to reply to information access requests, which many times does not comply
with the FIA [3] and compromises the rights guaranteed by the Constitution [9]. As an example,
the response sent by the Ombudsman of the Court Justice of Bahia informed us that the request was
beyond their competence and forwarded the request to the Modernization and Information Secretary
(SETIM), which then said that such request should be sent to the Information and Documentation
Agency (NDI), without giving the NDI’s address or contact, which is clearly against what is stated in
the AIP [3].
Regarding the issuance of a control number for requests and a confirmation email, 24.1% and
17.2% courts surveyed, respectively, do not provide a request control number nor a confirmation email.
This practice does not allow citizens to check whether your demand was in fact received and registered
by the Court and whether the necessary measures have been taken to respond to the request, making
any attempt to follow up more difficult.
Future Internet 2017, 9, 68 10 of 14

In the study, transparency in the Brazilian State [27] that evaluated the application of FIA [3] by
the Brazilian State, it was found that the various platforms used only allowed the citizen to access the
response to request for information after inserting the control number generated at the moment of the
request. They warn, however, that the platforms do not offer alternate means to access the response in
the case of a loss of that number. In this context, the situation found by this survey verified that some
platforms allow user registration to implement this alternative means. However, 62% of the analyzed
platforms do not make use of the Login.
Also, we found that the Court of Justice of the States of Ceará, Pará, Rio Grande do Norte, and
Roraima are really behind because they do not provide a control number, do not send confirmation
email, nor have a platform with Login or any other mean to follow up on the request for information.

4.2.2. Analysis of Information Access Request Responses

Once the deadline for the responses to the information access requests passed, analysis started
including (i) response rate, (ii) response time, and (iii) quality of the answers. For each court surveyed,
five requests for access to information were sent, totaling 145 requests, all sent from the same
citizen, through the internet, using the most relevant system in each court dedicated to the AIP [3]:
Ombudsman, Contact Us form, email, or any other mean available identified in their respective
websites. The results were summarized on Table 2.

Table 2. Information access request responses.

Court Name Respected
Deadline
E-mail
Notification
Requested Deadline
Extension Justified Allows Appeal

TJ do Acre No No No - -
TJ de Alagoas Yes Yes No - No
TJ do Amapá No No No - -
TJ do Amazonas No No No - -
TJ da Bahia Yes Yes No - No
TJ do Ceará No No No - No
TJ do Distrito Federal e
Territórios Yes Yes No - No
TJ do Espírito Santo No No No - -
TJ de Goiás No No No - -
TJ do Maranhão No No No - -
TJ do Mato Grosso Yes Yes No - No
TJ do Mato Grosso do Sul No No No - -
TJ de Minas Gerais No No No - -
TJ do Pará No No No - -
TJ da Paraíba No No No - -
TJ do Paraná No No No - -
TJ de Pernambuco Not Yet 1 Not Yet 1 Yes No -
TJ do Piauí No No No - -
TJ do Rio de Janeiro Partial Answer No No - No
TJ do Rio Grande do Norte No No No - -
TJ do Rio Grande do Sul Yes Yes No - No
TJ de Rondônia No No No - No
TJ de Roraima No No No - -
TJ de Santa Catarina Yes Yes No - No
TJ de São Paulo Yes Yes No - No
TJ de Sergipe Partial Answer Yes No - No
TJ de Tocantins Yes Yes No - No
Superior Tribunal de Justiça Not Yet 1 Not Yet 1 Yes Yes -
Supremo Tribunal Federal Yes Yes No - No
1 These courts requested an10-day extension, as provided by the FIA [3].

In terms of response rate, from a quantitative perspective, only 53 of the 145 requests were
answered, which means that 63.4% of requests were unanswered. Of the 29 courts surveyed, only nine
of them answered the five requests, and two courts responded to four of the five requests. The response
rate found in this study concurs with the Transparency in the Brazilian State Study [27], which found
similar numbers of unanswered requests (61%).
Future Internet 2017, 9, 68 11 of 14

It was noted also that the courts surveyed did not take advantage of requesting an extension to
reply, which allowed than to extend their deadline by 10 days, as stated in the paragraph 1, Article
11 of the FIA [3]. Only two courts requested an extension: the Court of the State of Pernambuco
(TJPE) and the Superior Court of Justice (STJ). However, only the Superior Court of Justice offered the
mandatory justification for the request for an extension.
Thus, the fact that only two courts requested the extension shows that most of the courts either
ignore that is possible to extend the deadline or do not care about complying with the FIA [3]. It also
reinforces the fact that, on average, two in every three requests for information have been completely
ignored and that, after two years of development of the Transparency in the Brazilian State study [27],
nothing has changed.
Furthermore, paragraph 4 of article 11 of the FIA [3] establishes the possibility of requesting an
appeal in case of the denial of access to the request made by the Court, which remains impaired, since
92 requests went unanswered. However, it should be noted that none of the surveyed platforms has a
field for sending of an appeal. The Court of Justice of Santa Catarina denied the request for information
to identify whether the Court possesses an information management policy, reasoning that the AIP
request was incomprehensible or generic (art. 12, I, Resolution CNJ 215/2015) [13]. In spite of having
been informed in the response that we could appeal to an authority that is hierarchically superior,
it was not clarified how or where the appeal may be filed.
In regard to the quality of the responses forwarded by the courts, the 53 responses were analyzed,
and these are the findings:
The first question asked about the court information management policy and the availability of
the normative that defined it. It was identified that the theme of information management is still not
properly understood in the context of the Brazilian judiciary, as most responses were confusing and
mixed the concepts of information management and document management.
Information management, broadly, can be understood as the management of processes and systems
that create, acquire, organize, store, distribute and use information. The objective of information
management is to help people and organizations to access, process and use information efficiently
and effectively [28]. On the other hand, document management is the set of procedures and
technical operations regarding the production, processing, use, evaluation, archiving, and disposal of
documents [29]. Therefore, it represents first step towards the establishment of information management.
In this context, the Court of Justice of the Federal District and Territories is the most advanced on
the topic of information management. It has several regulatory norms on the subject outlining how the
policy on the management of information security and has established a Corporate Information Security
Policy that aims to establish, implement, maintain, and improve controls and mechanisms to promote the
management of information security. To do so, they claim to have three norms that regulates this subject.
The Court of the State of São Paulo and the Brazilian Supreme Court replied to the first question
with classification of document rules and rules for disposal of the documents, which means that they
can be considered in the first stage of information management.
The most extreme case that confirms the difficulty of the courts to act in the subject was the
denial of request for access by the Court of Justice of Santa Catarina, who argued that the concept of
information management is very complex that such a request for access was not sufficiently clear to be
responded to by the Court.
The second question was about whether the court cases were available in the digital form and if so,
if they are publicly available for consultation. It was found that after 11 years of the law 11,419/2006 [2],
which established the electronic process in the Brazilian courts, physical processes on paper still coexist.
There is thus a hybrid situation, since the courts still allow paper processes, where some courts are still
scanning paper processes to convert it to digital format and comply with the law, while others only
scan it after the case is closed.
The third question asked about which procedural parts of the court case are published (petition
initial dispute, dispatches, sentence, etc.). In this sense, it was identified that the courts follow the
Future Internet 2017, 9, 68 12 of 14

resolution 121/2010-CNJ [26], which determines the publication of the full text of the decisions,
sentences, rulings and votes.
The fourth question asked whether documents are universally accessible. If they were not, we also
asked what criteria motivated the restricted access. The courts stated that documents were restricted
only when demanded by confidentiality or secrecy of justice and that there was no technical issue
preventing the universal access.
Finally, the fifth question sought to identify the frequency of updating the database of judicial
proceedings. With the exception to the Court of the Federal District and Territories that updates their
database weekly, all others stated that the update occurs on a daily basis.

5. Conclusions

The survey found that doing quantitative research [30] or jurimetrics by querying jurisprudential
databases of the Brazilian courts faces technical barriers and other non-technical barriers, as despite
the legal framework provided by the FIA [3] and subsequent resolutions from the CNJ [10–13,25,26],
few Courts comply with the law to its full extent. Also, the lack of standards to access those courts
makes querying this information more resource intensive, requiring more programmer-hours to be
implemented. The use of CAPTCHA in many search engines also makes the automation of the queries
even harder. That did not prevent the growth of jurimetrics in Brazil, and some interesting results
have been published since the enactment of the FIA [3–5,16,18,30]. Nevertheless, it is an important
barrier and slows progress in this area. It would be of great value if the courts defined a common API
to access their jurisprudential databases, where limits could be imposed per user, as it is done by many
software companies.
From the point of view of the access of information process (AIP) requests, when the researcher
needs to address the court in search of an answer that is not published, even with the establishment
of FIA [3] and the development of platform for the sending of requests, the courts in general do not
comply with the regulations. There is also a great deficiency in the platforms used for the submission
of requests for access to information that sometimes come with the minimum requirements set out in
FIA (for example, the frequent absence of the field to appeal). At this point, the unification of platforms
between the courts would represent a great gain.
Also, it was found that is the courts are really behind in the application of current information
management practices, since there is a confusion between the concepts of information management
and document management.
Regarding our initial hypothesizes:

• Hypothesis 1: The legal framework is not enough—The framework provided by the FIA [3] is
a great first step, and the resolutions from the CNJ [10–13] provided some progress in the right
direction, but as it was pointed out by Artigo 19 [14], and comparing our current framework
with international references as the Inter-American Declaration of Principles on Freedom of
Expression [8], that we still have a long way to go;
• Hypothesis 2: Current systems are preventing progress in this area—As the survey showed,
current systems are heterogeneous, many prevent automated queries, lots of processes are not
digital, but digitized as paper scans, making the progress harder;
• Hypothesis 3: Courts are not prepared and neither abide by the current laws—As the AIP survey
showed, 63% of the courts did not reply the AIP [3] and there are no mechanisms for appealing to
denied requests even if the law says so.

Based on this results, we made the following recommendations as the next steps to a more
transparent system:

• Amend the FIA [3] by making digital process mandatory and defining standards based on best
Open Data practices [16,17,22] to make this data available;
Future Internet 2017, 9, 68 13 of 14

• Ban the use of CAPTCHA, favoring the imposition of number of requests per user as a way to
avoid server overloads, and have mechanisms for a user to request an increase on these limits
upon justification (research for instance);
• Adopt a common API for all courts;
• Increase the supervision and establish mechanisms to punish courts that are not abiding by laws;
• Increase resources, training, and provision of technical expertise to the courts that are lacking that
to be compliant.

Even though our gloomy hypothesis were confirmed by our research, we see a positive future for
our society, as some progress was made, and watchdogs NGO like Artigo 19 [14] are putting more
pressure on our judiciary. As a next step, our research will continue trying to determine what are the
barriers to the implementation of jurimetric systems by developing our own legal database, as was
done at Washington University with the implementation of the US Supreme Court Database [31]. Also,
we want to look in how to generalize these findings from the Brazil’s example and how other countries
are dealing with it. Finally, we want to get deeper when researching a given court, trying to find
explanations for why the different states apply the law in different ways.

Author Contributions: B.A.C., P.B., and V.M.B. conceived and designed the experiments; B.A.C. performed the
experiments; B.A.C., P.B., and V.M.B. analyzed the data; B.A.C., P.B., and V.M.B. wrote the paper.
Conflicts of Interest: The authors declare no conflict of interest.

References

1. Loevinger, L. Jurimetrics the Next Step Forward. Jurimetr. J. 1971, 12, 3–41.
2. Lei n. 11.419. Available online: http://www.planalto.gov.br/ccivil_03/_ato2004-2006/2006/lei/l11419.htm
(accessed on 15 September 2017).
3. Lei n. 12.527. Available online: http://www.planalto.gov.br/ccivil_03/_ato2011-2014/2011/lei/l12527.htm
(accessed on 2 September 2017).
4. Castro, P.M.d.A. Law 12.402/2011—A jurisprudential study of application of the precautionary measures
different from prison under the Superior Courts: A jurimetrics approach. Revista Brasileira de Ciências
Criminais 2015, 109–140, Revista dos Tribunais on line.
5. Nunes, M.G.; Trecenti, J. Reformas de Decisão nas Câmaras de Direito Criminal em São Paulo. Available
online: http://s.conjur.com.br/dl/estudo-camaras-criminais-tjsp.pdf (accessed on 8 August 2017).
6. The United Nations. Universal Declaration of Human Rights; The United Nations: New York, NY, USA, 1948.
7. The United Nations. United Nations Convention against Corruption; Treaty Series 2349; The United Nations:
New York, NY, USA, 2003; Volume 41.
8. Organization of American States. Inter-American Declaration of Principles on Freedom of Expression; Organization
of American States, District of Columbia: Washington, DC, USA, 2000.
9. Constitution of Brazil (Brazil), 5 October 1988. Available online: http://www.refworld.org/docid/4c4820bf2.
html (accessed on 28 September 2017).
10. Conselho Nacional de Justiça. Resolução n. 79. Available online: http://www.cnj.jus.br/images/stories/
docs_cnj/resolucao/rescnj_79.pdf (accessed on 1 September 2017).
11. Conselho Nacional de Justiça. Resolução n. 102. Available online: http://www.cnj.jus.br/busca-atos-adm?
documento=2788 (accessed on 1 September 2017).
12. Conselho Nacional de Justiça. Resolução n. 151. Available online: http://www.cnj.jus.br/busca-atos-adm?
documento=2537 (accessed on 1 September 2017).
13. Conselho Nacional de Justiça. Resolução n. 215. Available online: http://www.cnj.jus.br/busca-atos-adm?
documento=3062 (accessed on 1 September 2017).
14. Artigo 19. Caminhos da Transparência (Livro Eletrônico): A Lei de Acesso à Informação e os Tribunais
de Justiça. Available online: http://artigo19.org/wp-content/blogs.dir/24/files/2016/06/Caminhosda-transpare%CC%82ncia-a-Lei-de-Acesso-a%CC%80-Informac%CC%A7a%CC%83o-e-os-Tribunais-deJustic%CC%A7a-2.pdf
(accessed on 12 September 2017).
Future Internet 2017, 9, 68 14 of 14

15. Open Society Justice Initiative (OSJI). Report on Access to Judicial Information. Available
online: http://www.right2info.org/resources/publications/publications/Access%20to%20Judicial%
20Information%20Report%20R-G%203.09.DOC (accessed on 20 September 2017).
16. Lopez, G.; Alvaro, J.H. Access to Information and Transparency in the Judiciary: A Guide to Good Practices
from Latin America. Available online: http://documents.worldbank.org/curated/en/563721467991021917/
Access-to-information-and-transparency-in-the-judiciary-a-guide-to-good-practices-from-Latin-America
(accessed on 20 September 2017).
17. Lettieri, N.; Faro, S. Computational Social Science and Its Potential Impact upon Law. Eur. J. Law Technol.
2012, 3, 1–17.
18. Barbosa, C.M.; Menezes, D.; Nagão, F. Jurimetria—Buscando um Referencial Teórico. Revista Acadêmica
Digital da Faculdade de Jaguariúna 2013, 172–175.
19. Sampieri, R.H.; Collado, C.F.; Lucio, M.d.P.B. Metodologia de Pesquisa; MacGraw-Hill: São Paulo, Brazil, 2006.
20. Gomes, A.O.; Guimarães, T.A.; Akutsu, L. The Relationship between Judicial Staff and Court Performance:
Evidence from Brazilian State Courts. Int. J. Court Adm. 2016, 8, 12–19. [CrossRef]
21. Conselho Nacional de Justiça. Justiça em Números. Available online: http://www.cnj.jus.br/files/conteudo/
arquivo/2016/10/b8f46be3dbbff344931a933579915488.pdf (accessed on 10 August 2017).
22. Cartilha Técnica Para Publicação de Dados Abertos No Brasil v1.0—Portal Brasileiro de Dados Abertos. Available
online: http://dados.gov.br/pagina/cartilha-publicacao-dados-abertos (accessed on 30 September 2017).
23. Von Ahn, L.; Blum, M.; Hopper, N.J.; Langford, J. CAPTCHA: Using Hard AI Problems for Security.
In Advances in Cryptology—EUROCRYPT; Lecture Notes in Computer Science; Springer: Berlin/Heidelberg,
Germany, 2003; pp. 294–311. [CrossRef]
24. Bernstein, P.A. Middleware: A Model for Distributed System Services. Commun. ACM 1996, 39, 86–98.
[CrossRef]
25. Conselho Nacional de Justiça. Resolucao 185. Available online: http://www.cnj.jus.br/busca-atos-adm?
documento=2492 (accessed on 30 September 2017).
26. Conselho Nacional de Justiça. Resolução n◦ 121. Available online: http://www.cnj.jus.br/atos-normativos?
documento=92 (accessed on 22 September 2017).
27. Michener, G.; Moncau, L.F.; Velasco, R.B. Estado Brasileiro e Transparência Avaliando a Aplicação da Lei de
Acesso à Informação. Fundação Getulio Vargas. Available online: http://bibliotecadigital.fgv.br/dspace/
handle/10438/17936 (accessed on 17 September 2017).
28. Deltor, B. Information Management. Int. J. Inf. Manag. 2010, 30, 103–108.
29. Martins, S.d.C. Gestão da Informação: Estudo Comparativo de Modelos sob a Ótica Integrativa dos Recursos de
Informação; Dissertação de Mestrado, Universidade Federal Fluminense: Niterói/Rio de Janeiro, Brazil, 2014.
30. Gustin, M.B.d.S.; Lara, M.A.; Costa, M.B.L.C. Pesquisa Quantitativa na Produção de Conhecimento Jurídico;
Revista Faculdade de Direito UFMG: Minas Gerais, Brazil, 2012; pp. 291–316.
31. Spaeth, H.; Epstein, L.; Ruger, T.; Whittington, K.; Segal, J.; Martin, A.D. Supreme Court Database Code Book;
Washington University Law: St. Louis, MO, USA, 2014.

© 2017 by the authors. Licensee MDPI, Basel, Switzerland. This article is an open access
article distributed under the terms and conditions of the Creative Commons Attribution
(CC BY) license (http://creativecommons.org/licenses/by/4.0/).