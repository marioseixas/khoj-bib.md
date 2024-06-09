Electronic copy available at: https://ssrn.com/abstract=2477006

In the normal course of business, companies are involved in various disputes that must be
resolved by the courts. The administration of these legal actions involves assessing the risk
to which these companies are exposed. This text proposes that such actions can be
grouped and treated as a portfolio. Legal techniques can be used to assess and manage
the risk in these actions.

This differentiation between risk and uncertainty is made by Frank Knight in Risk, Uncertainty, and Profit, Boston New
York: Houghton Mifflin Company, 1921. According to the author "But Uncertainty must be taken in a sense radically
distinct from the familiar notion of Risk, from which it has never been properly separated. The term "risk," as loosely used
in everyday speech and in economic discussion, really covers two things which, functionally at least, in their causal
relations to the phenomena of economic organization, are categorically different. The nature of this confusion will be
addressed with at length in chapter VII, but the essence of it may be stated in a few words at this point. The essential

Text presented at the VII Congress of Legal Administration, Legal Informatics and Jurimetry, São Paulo, Othon Hotel,
October 7, 1998.

Summary

Consultant and business administrator from the University of São Paulo. Email ivan_ribeiro@dialdata.com.br.

According to Eduardo Leopoldino de Andrade, Introduction to Operations Research, Technical and Scientific Books,
São Paulo, 1990, page 261.
3

1

two

4

A Jurimetric Approach1

Lawsuit Portfolio Risk Assessment

Ivan César Ribeiro2

A company, in the normal exercise of its activities, becomes involved in conflicts that eventually
flow into the Judiciary. These are labor actions filed by former employees, customer actions
supported by the recently enacted Consumer Protection Code (Law 8,078 of 1990), debt
enforcement charging defaulting customers and several other possibilities. Sometimes,
companies create internal legal departments, or hire law firms to monitor and defend these
actions.

Risk is normally defined as an estimated degree of uncertainty with respect to the achievement
of desired future outcomes. The wider the range of predictable values for the return on an
investment (or, in our case, for the outcome of a lawsuit), the greater the degree of risk of the
investment3. .

The result of each of these actions, sometimes occurring at a very distant point in the future, can
have important impacts on the company's revenues, expenses and results. Condemnations in
amounts higher than expected in those actions in which the company is the defendant, or an
unfavorable decision frustrating the receipt of amounts in an action in which the company acts
as the plaintiff, therefore imposes a risk for the company.

In the case of legal actions, a portion of the possible values for their result may not be easy to
assess, that is, it would not be possible to assign probabilities to all values in the spectrum of
possible results. We are, in this case, dealing with the difference between risk and uncertainty4 .

1. Introduction

Machine Translated by Google
Electronic copy available at: https://ssrn.com/abstract=2477006

5

6
In order to correctly assess the risks and returns of this said portfolio of lawsuits, therefore, we
need to find ways to assess the risk involved in each lawsuit, as well as the possible amounts
involved.

Due to its uncertain nature, a lawsuit that has not yet been closed can be classified as a
contingency. According to the FASB (1975)6 , a contingency involves a condition, situation or set
of circumstances involving uncertainty in relation to a gain (assets) or loss (liabilities) whose
resolution depends on future events. These regulations have been in constant evolution, with
contingent liabilities, specifically, first disciplined by IAS-10 (International Accounting Standards),
from 1978, with the most recent amendment in 1994.

A company's lawsuits can be viewed and managed as a whole, in the form of a portfolio. Thus,
more than the risk in a specific lawsuit, the company is interested in performance in all lawsuits.
While the company may face adverse results in some of these actions, in others the result may
be positive – what is expected is that there is not a perfect correlation between all the issues that
the company discusses in the Judiciary. Portfolio Theory has been examined for a long time in
the area of finance, and this property, of different correlations between legal actions, ends up
mitigating the total risk to which the company is subjected, making results more predictable5 .

A contingent liability, still according to the FASB, must be classified according to the probability
of occurrence, being classified as probable, possible or remote. In the case of lawsuits, we
observe in the balance sheets of publicly-held companies a reserve in the income statement
accounts for these expenses (provisions), in the case of those classified as probable. Lawsuits
classified as only possible or even remote are informed in the notes

Assessing the likely outcome of legal actions in companies is normally the responsibility of
lawyers and, occasionally, accountants. The so-called due diligence procedures, through a
detailed examination of the documents of each legal action, seek to determine the values involved
in the legal discussions and the chances of victory. It should be noted that legal actions are
evaluated in at least two dimensions – first in relation to the chance of gain or loss, and, once
this stage has been completed, in relation to the possible value of conviction (or value recovered,
in the case of actions promoted by the company ).

2. Provisions and Contingencies

“A contingency is defined as an existing condition, situation, or set of circumstances involving as uncertainty to
possible gain (hereinafter a "gain contingency") or loss 1 (hereinafter a "loss contingency") to an enterprise that will
ultimately be resolved when one or more future events occur or fail to occur. Resolution of the uncertainty may
confirm the acquisition of an asset or the reduction of a liability or the loss or impairment of an asset or the incurrence
of a liability”.

See, for an approach to portfolio theory, Campbell, Lo, and MacKinley, 1997, Chapter 5.

fact is that "risk" means in some cases a susceptible quantity of measurement, while at other times it is something
distinctly not of this character; and there are far-reaching and crucial differences in the bearings of the phenomenon
depending on which of the two is really present and operating. There are other ambiguities in the term "risk" as well,
which will be pointed out; but this is the most important. It will appear that a measurable uncertainty, or "risk" proper,
as we shall use the term, is so far different from an unmeasurable one that it is not in effect an uncertainty at all. We
shall accordingly restrict the term "uncertainty" to cases of the non-quantitive type. It is this "true" uncertainty, and
not risk, as has been argued, which forms the basis of a valid theory of profit and accounts for the divergence
between actual and theoretical competition."

Machine Translated by Google
9

7

8

3. The Econometric Approach

closed in three large companies, with the dual objective of i) providing better forecasts for these

contingencies and ii) guiding legal strategies or amicable composition, in order to better manage

what we call a portfolio of lawsuits. These models were initially developed with an econometric

approach, described in the next section. After facing problems with what we call the phenomenon

of case selection, we began to develop a jurimetric approach to creating such models.

The practice in most companies has been to request these assessments as to the likelihood of

gain or loss (whether probable, possible or remote) and estimates of the amounts involved from

the attorneys in these actions, whether these are company lawyers or external offices. More often

than not, these predictions are made in a non-systematic way, with little adherence between the

final outcome and the predictions offered by the lawyers.

The development of predictive models began with data collection and preparation of a database

with lawsuits both from the company and from other litigants. This information is available in the

various services for querying information from the judiciary, through services supported by

RENPAC (National Package Network), Videotext (Telesp) and proprietary projects.

the development of process-based forecasting models has already

explanations of the financial statements, although not all companies bring this information in their
balance sheets7 .

The creation of these databases proved to be challenging, as each judiciary body uses different

standards in its computers. Accessing information requires the access program to emulate different

terminals, such as the IBM 3270, Digital terminals (especially the VT 100) and others. Since 1993,

we have developed technology for these consultations, through our Telejuris® software, a terminal

emulator capable of automatically collecting this data.

,

In a second step, with these data in hand, econometric models were developed that sought to

determine the chance of gain or loss in these actions9 , as well as estimators of the amounts

involved in court decisions. In addition to basic information such as the order value,

This is the discipline required by Ibracon (1994, p. 151), which provides that a condition that may

generate a contingent loss “shall be provisioned, through a debit to income for the year when it is

considered probable and its amount can be estimated” .

We started, from 19918

Electronic copy available at: https://ssrn.com/abstract=2477006

Companies inform, above all, the so-called passive contingencies in the labor, tax and civil areas.

These are projects that involve contractual secrecy, and for such reasons the names and details of the lawsuits will not
be declined in this article.
See Berndt (1991, especially Chapter 11) for win-loss prediction models, called dichotomous models. Regarding the use
of econometric techniques for predicting results in legal actions in a more general way, see Nagel (1965) – “[t] his article
illustrates and systematically compares three methods for quatitatively predicting case outcomes. The three methods are
correlation, regression, and discriminant analysis, all of which involve standard social science research techniques.”

Companies with activities that produce high environmental impact, such as mining companies, have also reported
information on actions in the environmental area, especially when these are consequences of Public Civil Actions.

Machine Translated by Google
10

4. The Selection of Disputes for Litigation

In the case of labor actions, it was detected that a policy of agreements, aiming to eliminate the labor

liabilities of a subsidiary of one of the companies, was apparently leading to the filing of an increasing

number of actions.

The action will only be filed if there is a margin of doubt that justifies this proposition.

It is noted, from the content of the previous sections, that the management of legal actions in the form

of a portfolio requires the determination of the risk and values involved in each action. Similar to what

is done with other assets, this assessment could be made using the historical values of these shares.

However, unlike financial assets, legal actions have a more dynamic characteristic, which makes their

prediction a little more difficult.

area of litigation, lawyer, place of action and others, variables were included that sought to provide

guidance for defense strategies or for proposing agreements. The estimators of the parameters of

these models were obtained through OLS and probit regressions made using the EViews 2.010
software.

If the plaintiff assesses that the chances of winning are minimal, he will not propose the action,

accepting a possible agreement, with the situation being similar for the defendant. Priest and Klein's

proposal is that the proportion of decisions favoring each side tends to 50%, regardless of any bias

on the part of the court in favor of either party.

For the management of a portfolio of legal actions, not only the actions currently litigated are important,

but also those that could potentially go to court. What works such as Priest and Klein (1984),

Siegelman and Donohue (1995) and Steven Shavell (1996) show is that the actions that actually go

to trial are not representative of all potential conflicts. Put another way, the litigated actions are not a

random sample of the underlying conflicts, and the majority of these conflicts are resolved by

agreement.

The models did not seek to determine litigation or settlement strategies, but rather to provide support

for legal teams, with these strategies being chosen exclusively by lawyers with mandate in legal

actions. Each chosen strategy was then monitored and validated, especially in the labor and consumer

rights areas.

What these projects seem to show so far is that it is not enough to just observe the actions already

proposed, but also to take into account disputes with the potential to reach the judiciary. This possibility

has been the subject of research in the United States since the end of the seventies.

What these authors propose is that potential litigants take into account the chances of success before

deciding whether or not to propose an action (and, consequently, whether to refuse an eventual

agreement). Judges will grant a favorable decision to the author if the total evidence of the proposed

action reaches or exceeds what the court understands as necessary evidence to justify it. Each party,

plaintiff and defendant, makes an assessment of the merits of the case, weighing their assessment

against the evidence considered to be the standard required by the court.

Electronic copy available at: https://ssrn.com/abstract=2477006

It is a software released by QMS in March 1994, replacing MicroTSP. The version used, 2.0, is the first for
the Windows environment, an operating system developed by Microsoft for compatible PC environments.

Machine Translated by Google
5. Jurimetry and Selection Bias

Source: Adapted from Santos et al (1995).

The phenomenon can be better understood through an example. Suppose that the Consumer

Defense Code, edited in 1990, generated a bias against large companies. For this reason judges in

90% of cases would tend to favor the consumer. Companies, aware of this bias, will take to the

judiciary only those actions in which they are absolutely certain they will win, where the evidence in

their favor is strongest. As a result, although the bias against companies disadvantages them in

90% of cases, we could, in the end, observe that companies win, say, 80% of cases. What happens

is that these companies end up making agreements in the actions in which they would be harmed,

and thus the examination, even econometric, of the results of the actions proposed in the judiciary

would be useless to determine the risk and values involved.

At the base of this pyramid we have social relations with the possibility of injury and, at the top, the

result of the trial with the possibility of a previous agreement. At each stage the parties decide

whether to move to the next stage. Figure 1 below presents a variation that we propose for this

pyramid, showing that the next stage does not “fit” perfectly into the previous one. What this

representation seeks to show is that there is a selection at each stage. At the base, for example,

humble litigants or those with little access to justice can resign themselves to the injury. At the upper

reaches of the pyramid, a party that fears being biased may prefer settlement to litigation.

What the selection bias hypothesis shows is that, as the cases litigated are not a representative

sample of the total number of disputes in society, it would not be possible to carry out any

assessment of the chances of winning in an action based on these cases. What researchers

suggest is that this bias be taken into account when analyzing the results of these cases – for example, Heisenberg and

Santos et al (1995), examining litigation in Portugal, suggest a pyramid for litigation.

Electronic copy available at: https://ssrn.com/abstract=2477006

Figure 1

Machine Translated by Google
11

6. The Jurimetric Approach

Farber (1996) suggest that the heterogeneity of litigants can explain differences in success
rates, when selection bias is taken into account.

In fact, there is no impediment for econometrics to face specific issues such as self-selection
– see, for example, the work of James Heckman in this regard (1974, 1976, 1979). We
believe, however, that just as the creation of sociometry11, psychometrics, biometrics and
others helped to boost the use of quantitative approaches in specific fields, the same is true
of jurimetrics.

In the end, what we found is that the analysis of judicial decisions in such a way is not, when
taking into account Priest and Klein's hypothesis, an easy task within the narrow framework
of econometric analysis. That is why there is a need for a specific field for quantitative
analysis in law, which we call jurimetry.

Positive Jurimetry is the branch of knowledge that carries out the scientific investigation of
legal phenomena through the proposition of hypotheses and their empirical test. The
hypotheses formulated by positive jurimetry seek to explain and establish the causal links of
these phenomena, but do not intend to explain a specific course of action for law practitioners.
This last approach would be more typical of traditional jurimetry, as defined by Loevinger
(1949, 1963) and his followers, and which could be more properly called Normative Jurimetry.

Positive Jurimetry proposes hypotheses about the regularities observed in the legal
phenomenon and also about variations around these regularities. These hypotheses will be,
as far as necessary to define the empirical tests, defined in mathematical formulations or at
least formulations that can be quantified. Empirical tests will seek to test the validity of these
propositions through the use of statistics, especially statistical inference and probability
theory, dealing with problems of identification, causality, significance and robustness of
results.

An additional challenge is to accurately quantify the extent of this bias. Zatz and Hagan
(1985) show in an empirical exercise how much the coefficients in a regression analysis of
this nature can vary as a function of selection bias. In fact, Priest and Klein's proposition is
theoretical, and does not provide econometric or other methods for estimating the bias. An
extensive literature, also mentioned by Zatz and Hagan, suggests strategies for these
estimations, all of which are challenging to implement.

As a field specifically focused on law, jurimetrics would be particularly capable of dealing with
specific problems in Law and the administration of Justice. The existence of a field of its own
does not exclude interdisciplinary action, especially dialogue with disciplines such as
mathematics, statistics and econometrics. The existence of a field of its own would allow
even better dealing with problems such as self-selection of cases and its impact on the inference from

Electronic copy available at: https://ssrn.com/abstract=2477006

In the case of Social Sciences, Berk (1983) is one of the pioneering works to show the impact of selection bias
based on the econometric literature mentioned. His proposition gave rise to an extensive literature applying selection
models to the area of criminology, including the examination of judicial decisions.

Machine Translated by Google
12

7. Conclusions

8. Bibliography

Electronic copy available at: https://ssrn.com/abstract=2477006

Since the end of the 1980s, there has been some research, especially in the area of Political Science, which

focuses on judicial decisions. These analyses, however, are only descriptive, consisting of frequency tables
and the use of questionnaires. Inference analysis, especially that using regression models, still seems far from
our scientists' research agenda. Facing problems such as self-selection of cases and other challenges such as
calculating risk and determining agent behavior models, essential for effectively understanding the nature of
litigation in our country, is even further away.

This risk assessment can benefit from the tools and techniques provided by the expansion of
access to information technology resources, especially from the popularization of personal
computers in the 90s and access to information networks such as RENPAC and others. In
addition to the possibility of setting up databases with information on lawsuits by the company
itself and others, econometric models and software such as Micro TSP and EViews allow for
a better assessment of this risk.

The confluence of these techniques and, above all, the action of private agents, consultants
and developers in conjunction with the university and public authorities should advance the
research and production of new technologies and products aimed at managing legal actions,
especially through the development of a new field of research, Jurimetrics.

litigated cases, or the development of specific decision models, aimed at analyzing agents
such as judges, lawyers, parties to legal actions, legislators and others

The management of lawsuits in companies can benefit from a more technical treatment, with
the development of predictive models and a better assessment of risks and amounts involved
in conflicts, whether they reach the judiciary or are resolved extrajudicially. This better
assessment and control of lawsuits would allow for portfolio treatment of the set of disputes
faced by each company, allowing for better risk diversification and better financial management.

The use of these techniques and tools occurs, in Brazil, exclusively in companies and the
private sector, and there is no news, to date, of research and development activities led by
public bodies, universities or research centers12. Outside the country, especially in the United
States, there is a large amount of academic production examining the conditions for judicial
decisions, with the development of important theories such as the case selection hypothesis
for litigation and others.

CAMPBELL, John Y.; L.O., Andrew W.; MACKINLAY, A. Craig; The Econometrics of Financial Markets,
Princeton University Press, 1997.

ANDRADE, Eduardo L.; Introduction to Operational Research, Technical and Scientific Books, São Paulo, 1990.

BERNDT, Ernst R.; The Practice of Econometrics: Classic and Contemporary, New York: Addison-Wesley
Publishing, 1991.

EISENBERG, Theodore, and Henry S. FARBER. The litigious plaintiff hypothesis: Case selection and resolution,
mimeo, WP 5649, National Bureau of Economic Research - NBER, July 1996, 34 pages.

BERK, Richard A. "An introduction to sample selection bias in sociological data." American sociological review
(1983): 386-398.

Machine Translated by Google
Electronic copy available at: https://ssrn.com/abstract=2477006

SIEGELMAN, P.; DONOHUE, JJ; The Selection of Employment Discrimination Disputes for Litigation: Using
Business Cycle Effects to Test the Priest-Klein Hypothesis; Journal of Legal Studies, 24(2), 427-

IBRACON – Brazilian Institute of Accountants. Accounting Principles. 2nd ed. São Paulo: Atlas, 1994.

SHAVELL, S.; Any Frequency of Plaintiff Victory at Trial is Possible, Journal of Legal Studies, 25(2), 1996,
pp. 493-501.

462.

HECKMAN, James J. "Sample selection bias as a specification error." Econometrica: Journal of the
econometric society (1979): 153-161.

LOEVINGER, L.; Jurimetrics - The Next Step Forward. Minnesota Law Review, 33, 1949, 455.
KNIGHT, Frank; Risk, Uncertainty, and Profit, Boston New York: Houghton Mifflin Company, 1921.

ZATZ, Marjorie S., and John HAGAN. Crime, time, and punishment: An exploration of selection bias in
sentencing research, Journal of Quantitative Criminology 1.1, 1985, pp. 103-126.

EViews, User Guide. "Version 2.0." QMS Quantitative Micro Software, Irvine, California (1995).

NAGEL, Stuart. Predicting court cases quantitatively, Michigan Law Review, 63.8 (1965): 1411-1422.

LOEVINGER, L.; Jurimetrics: The methodology of legal inquiry; Law and contemporary problems. 28(1),
1963, pp. 5-35.

HECKMAN, James. "Shadow prices, market wages, and labor supply." Econometrica: journal of the
econometric society (1974): 679-694.

SANTOS, Boaventura S.; MARQUES, Maria ML; PEDROSO, John; FERREIRA, Pedro L.; Courts in
Contemporary Societies: The Portuguese Case. Porto: Afrontamento, 2nd edition, 1996.

HECKMAN, James J. "The common structure of statistical models of truncation, sample selection and limited
dependent variables and a simple estimator for such models." Annals of economic and social measurement,
volume 5, number 4. NBER, 1976. 475-492.

Financial Accounting Standards Board (FASB), Statement of Financial Accounting Standards No. 5 -
Accounting For Contingencies, Norwalk (CT), March 1975.

PRIEST, GL; KLEIN, B.; The Selection of Disputes for Litigation, Journal of Legal Studies, 13(1), 1984, pp.
1-55.

Machine Translated by Google