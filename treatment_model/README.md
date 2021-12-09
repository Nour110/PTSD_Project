# Description #

This is a simple agent based model of the treatment of PTSD.
The model is a very idealistic model of the treatment. It simulates people looking for and receiving treatment for PTSD. The model will run for 104 weeks. Patients who are in treatment will go to a session of therapy every week.
The model will visualize certain attributes of the patients. You'll see a bar graph of the number of people who have accessed treatment and those who have not. Next, there will be a chart which will graph three things:
1) The percentage of people who have dropped out of treatment.
2) The percentage of people who have achieved remission
3) The percentage of people who have lost their housing
There will then be a bar graph that will illustrate the people's current severity of illness. Finally there will be a chart with two graphs, the first being the percentage of people who are employable and second, the percentage of people who are not employable.

# Running the model #

To run the model:
1) run the command `mesa runserver` in the directory of the model.
2) Open https://127.0.0.1:8521/ in your browser
3) Set your desired parameters and hit the Reset button then Run.

Using the default parameters would mean that you have 1 trained psychotherapist per 50 patients with PTSD.
Realistically, if we look at the US alone, the estimated one year prevalence is according to low estimates 3.5%. Currently, there are about 106 000 practicing psychotherapists who are not necessarily trained to treat PTSD but assuming that they all were able to then we would have 1 trained psychotherapist per 100 people with PTSD.

# Assumptions made for the model #

These are the assumptions of the model:


First, and probably most importantly, we will not consider the risk for revictimization and retraumatization. Additionally, PTSD can be totally debilitating but we will assume that every person in our model has the capacity to adhere to treatment if they choose to. We will not consider comorbidities.
Our model will only consider psychotherapy as possible treatment options.

Suicide: We will not factor in the risk of suicide as there doesn't seem to be any reliable data.

Assumptions of severity:
The severity of an individual's symptoms will be determined randomly between 1-3.
1 indicates mild PTSD
2 indicates moderate PTSD
3 indicates severe PTSD
The probability of each will be 30.2% for mild, 33.2% for moderate and 36.6% for severe.

Assumption of providers: 
Our model will assume that each provider can see patients 4 days a week for 8 hours per day.
We will assume that each session with a therapist spans one hour and a half. Therefore, each therapist can see 21 patients every week. We will also assume that each therapist has qualification in trauma therapy of each kind. There will be no variation among therapists and as such we will only be tracking the number of slots available. 


Assumption of treatment:
Each session will cost a person a set amount of money.
There will be 4 different treatments offered. Each one will have the same effectiveness as the others.
We will not consider the possibility of worsening symptoms, instead we will lump in the probability of worsening symptoms with the probability of no changes.
If a person improves then we will assume that 75% drop one severity scale, 20% drop two severity scales and 5% drop three severity scales.
The probability that someone improves after treatment will be set to 30.5%

Assumption of dropping out:
The likelihood of dropping out each week will be estimated at 0.72%. If a person drops out then we will assume they no longer will seek treatment.


Assumptions of employability:
We will not track employment but rather if the person is able to maintain employment or not

1) For those who have mild PTSD, we will assume that they all can hold a job.
2) For those with moderate PTSD, we will assume that 60% of them cannot hold a job and 40% can hold a job.
3) For those with severe PTSD, we will assume that 80% are not employable/cannot hold a job
==> Given a sample of 100 people, this would mean that we expect 49 of them to be unable to hold a job. We will assume that if someone is employable then they are immediately employed for simplicity.


Each person will start with savings. These amount will be random with a minimum of 10,000 and a maximum of 100,000.
We assume that if a person is employable then they will not spend their savings to live or seek treatment.
If a person is not employable then they will incur a weekly cost of living and if they are in treatment then they will have to pay for each session. If a person cannot pay for a session then they will drop out. If they have no savings left and are still not employable then they will be considered homeless.

These assumptions were made by referencing some established researched on the subject. Additionally, I've decided to exclude psychiatric treatment for PTSD as its effects seem to be very mild.
If you'd like to learn more then I've included some of the material below.

https://www.mountsinai.org/about/newsroom/2014/unemployment-biggest-predictor-of-ptsd-symptom-severity
https://iamresearch.org/how-does-ptsd-affect-employability/
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7144189/ 
https://www.nimh.nih.gov/health/statistics/post-traumatic-stress-disorder-ptsd
https://www.uptodate.com/contents/approach-to-treating-posttraumatic-stress-disorder-in-adults
http://file.lacounty.gov/SDSInter/dmh/1060782_LACPEITF-CBTAggregateReportJuly2012.pdf
https://www.ncchildtreatmentprogram.org/impact/tf-cbt-cohort-14/ucla-posttraumatic-stress-disorder-reaction-index-for-dsm-5-ptsd-ri-child-adolescent-version/
https://pubmed.ncbi.nlm.nih.gov/24681171/#:~:text=Remission%20varied%20between%208%20and,than%20five%20months%20following%20trauma.
https://www.uptodate.com/contents/posttraumatic-stress-disorder-in-adults-epidemiology-pathophysiology-clinical-manifestations-course-assessment-and-diagnosis
https://psycnet.apa.org/fulltext/2019-01033-009.html


