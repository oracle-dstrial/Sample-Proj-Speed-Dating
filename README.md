# Speed Dating

# Data Overview
The dataset in this project was collected during a series of speed dating events.  It contains participant demographics, answers to survey questions regarding their interests, their lifestyles, how they rate themselves and others on a number of different attributes, and many other interesting fields.  It also contains a column on participant decisions about whether they liked each of their dating partners (yes / no), as well as whether two dating partners matched (both decided 'yes'). The Data Dictionary below describes the contents of each of the many available fields.

### Insights
What insights can we gleam from this data?  There are many interesting fields, from people's interests, their ratings of themselves and their partners, the stated vs. the actual value they place on attributes, a number of demographics, etc.  The notebook [speed_dating_insights.ipynb](https://github.com/datascienceinc/dating_insights/blob/master/speed_dating_insights.ipynb) contains a few interesting analyses to get you started.  What other interetsting questions can you answer from this data?

### Model
Can you predict if two people are a good match?  Your goal is to build a classifier to predict whether two participants matched (`match` field) using features in sections 1 and 2 in the Data Dictionary below.  Be careful, as sections 3 and later may contain fields with **target leakage** that should not be used!  You may also wish to use the existing features to engineer new features, such as age difference, an interest similarity index, etc.


# Data Dictionary

### 1. General Information
**iid:**
> unique subject number, group(wave id gender)
<br>

**id:**
> subject number within wave
<br>

**gender:**
> Female=0<br>
> Male=1
<br>

**idg:**
> subject number within gender, group(id gender)
<br>

**condtn:**
> 1=limited choice<br>
> 2=extensive choice
<br>

**wave:** 
> Wave #.  Each wave happened on a different day with different sets of people, and included several rounds of speed dating.  Note that different waves had different speed dating conditions and data
<br>

**round:**
> number of people that met in wave
<br>

**position:**
> station number where met partner 
<br>

**positin1:**
> station number where started 
<br>

**order:**
> the number of date that night when met partner
<br>

**partner:**
> partner’s id number the night of event
<br>

**pid:**
> partner’s iid number
<br>

**match:**
> Whether the participatns matched<br>
> 1=yes<br>
> 0=no
<br>

**int_corr:**
> correlation between participant’s and partner’s ratings of interests
<br>

**samerace:**
> participant and the partner were the same race<br>
> 1= yes<br>
> 0=no
<br>

**age_o:**
> age of partner
<br>

**race_o:**
> race of partner
<br>

**pf_o_att, pf_o_sin, pf_o_int, pf_o_fun, pf_o_amb, pf_o_sha:**
> partner’s stated preference for 6 attributes<br>
> Attractive, Sincere, Intelligent, Fun, Ambitious, Has shared interests/hobbies
<br>


**attr_o, sinc_o, int_o, fun_o, amb_o, shar_o:**
> rating by partner the night of the event, for 6 attributes
> Attractive, Sincere, Intelligent, Fun, Ambitious, Has shared interests/hobbies
<br>


### 2. Survey filled out when registering / signing up for the speed dating event.

**age:**
> Age of participant
<br>

**field:**
> field of study  
<br>

**field_cd:**
> field of study codes <br>
> 1= Law<br>
> 2= Math<br>
> 3= Social Science, Psychologist<br>
> 4= Medical Science, Pharmaceuticals, and Bio Tech<br>
> 5= Engineering<br>
> 6= English/Creative Writing/ Journalism<br>
> 7= History/Religion/Philosophy<br>
> 8= Business/Econ/Finance<br>
> 9= Education, Academia<br>
> 10= Biological Sciences/Chemistry/Physics<br>
> 11= Social Work<br>
> 12= Undergrad/undecided<br>
> 13=Political Science/International Affairs<br>
> 14=Film<br>
> 15=Fine Arts/Arts Administration<br>
> 16=Languages<br>
> 17=Architecture<br>
> 18=Other
<br>

**undergrd:**
> school attended for undergraduate degree
<br>

**mn_sat:**
> Median SAT score for the undergraduate institution where attended.
<br>

**tuition:**
> Tuition listed for each response to undergrad in Barron’s 25th Edition college profile book.
<br>

**race:**
> Black/African American=1<br>
> European/Caucasian-American=2<br>
> Latino/Hispanic American=3<br>
> Asian/Pacific Islander/Asian-American=4<br>
> Native American=5<br>
> Other=6
<br>

**imprace:**
> How important is it to you (on a scale of 1-10) that a person you date be of the same racial/ethnic background?
<br>

**imprelig:**
> How important is it to you (on a scale of 1-10) that a person you date be of the same religious background?
<br>

**from:**
> Where are you from originally (before coming to Columbia)? 
<br>

**zipcode:**
> What was the zip code of the area where you grew up? 
<br>

**income:**
> Median household income based on zipcode using the Census Bureau website:<br>
> http://venus.census.gov/cdrom/lookup/CMD=LIST/DB=C90STF3B/LEV=ZIP <br>
> When there is no income it means that they are either from abroad or did not enter their zip code.
<br>

**goal:**
> What is your primary goal in participating in this event?<br>
> Seemed like a fun night out=1<br>
> To meet new people=2<br>
> To get a date=3<br>
> Looking for a serious relationship=4<br>
> To say I did it=5<br>
> Other=6
<br>

**date:**
> In general, how frequently do you go on dates? <br>
> Several times a week=1<br>
> Twice a week=2<br>
> Once a week=3<br>
> Twice a month=4<br>
> Once a month=5<br>
> Several times a year=6<br>
> Almost never=7
<br>

**go out:**
> How often do you go out (not necessarily on dates)?<br>
> Several times a week=1<br>
> Twice a week=2<br>
> Once a week=3<br>
> Twice a month=4<br>
> Once a month=5<br>
> Several times a year=6<br>
> Almost never=7
<br>

**career:**
> What is your intended career?
<br>

**career_c:**
> career codes <br>
> 1= Lawyer <br>
> 2= Academic/Research <br>
> 3= Psychologist <br>
> 4= Doctor/Medicine <br>
> 5=Engineer <br>
> 6= Creative Arts/Entertainment <br>
> 7= Banking/Consulting/Finance/Marketing/Business/CEO/Entrepreneur/Admin <br>
> 8= Real Estate <br>
> 9= International/Humanitarian Affairs <br>
> 10= Undecided <br>
> 11=Social Work<br>
> 12=Speech Pathology<br>
> 13=Politics<br>
> 14=Pro sports/Athletics<br>
> 15=Other<br>
> 16=Journalism<br>
> 17=Architecture
<br>

**_Activity interests, on a scale of 1-10?_**<br>
<hr width=300px, height=1px>

**sports:** 
> Interest in Playing sports/ athletics (1-10)
<br>

**tvsports:**
> Interest in  Watching sports (1-10)
<br>

**excersice:**
> Interest in  Body building/exercising (1-10)
<br>

**dining:**
> Interest in Dining out (1-10)
<br>

**museums:**
> Interest in  Museums/galleries (1-10)
<br>

**art:** 
> Interest in Art (1-10)
<br>

**hiking:**
> Interest in  Hiking/camping (1-10)
<br>

**gaming:**
> Interest in  Gaming (1-10)
<br>

**clubbing:** 
> Interest in  Dancing/clubbing (1-10)
<br>

**reading:** 
> Interest in  Reading (1-10)
<br>

**tv:** 
> Interest in Watching TV (1-10)
<br>

**theater:** 
> Interest in Theater (1-10)
<br>

**movies:** 
> Interest in Movies (1-10)
<br>

**concerts:** 
> Interest in Going to concerts (1-10)
<br>

**music:** 
> Interest in Music (1-10)
<br>

**shopping:** 
> Interest in Shopping (1-10)
<br>

**yoga:** 
> Interest in Yoga/meditation (1-10)
<hr width=300px, height=1px>
<br>

**exphappy:**
> Overall, on a scale of 1-10, how happy do you expect to be with the people you meet during the speed-dating event?
<br>

**expnum:** 
> Out of the 20 people you will meet, how many do you expect will be interested in dating you? 
<br>


**attr1_1, sinc1_1, intel1_1, fun1_1, amb1_1, shar1_1:**
> Importance rating of the following attributes in a potential date<br>
> Attractive, Sincere, Intelligent, Fun, Ambitious, Has shared interests/hobbies<br><br>
> For Waves 6-9: Scale of 1-10 (1=not at all important, 10=extremely important)<br>
> For Waves 1-5, 10-21: Distribute 100 points among attributes, with more points to more important attributes.
<br>

**attr4_1, sinc4_1, intel4_1, fun4_1, amb4_1, shar4_1:**
> Rating of what participant believs MOST fellow men/women look for in the opposite sex.<br>
> Attractive, Sincere, Intelligent, Fun, Ambitious, Has shared interests/hobbies<br><br>
> For Waves 6-9: Scale of 1-10 (1=not at all important, 10=extremely important)<br>
> For Waves 10-21 : Distribute 100 points among attributes, with more points to more important attributes
<br>

**attr2_1, sinc2_1, intel2_1, fun2_1, amb2_1, shar2_1:**
> Rating of what participant thinks the opposite sex looks for in a date<br>
> Attractive, Sincere, Intelligent, Fun, Ambitious, Has shared interests/hobbies<br><br>
> For Waves 6-9: Scale of 1-10 (1=not at all important, 10=extremely important)<br>
> For Waves 1-5 and 10-21: Distribute 100 points among attributes, with more points to more important attributes.
<br>

**attr3_1, sinc3_1, intel3_1, fun3_1, amb3_1:**
> Participant self rating of participant's own attributes, on a scale of 1-10 (1=awful, 10=great)<br>
> Attractive, Sincere, Intelligent, Fun, Ambitious
<br>

**attr5_1, sinc5_1, intel5_1, fun5_1, amb5_1:**
> Participant's ratings of how he or she thinks is perceived by otherson a scale of 1-10 (1=awful, 10=great)<br>
> Attractive, Sincere, Intelligent, Fun, Ambitious

### 3. Date Scorecard - Filled out by subjects after each "date" during the event.

**dec:**  
> Decision on whether you would like to see this person again (a match occurs when both people on the date say yes)
> 1 = Yes
> 0 = No
<br>

**attr, sinc, intel, fun, amb, shar:** 
> Rating of attributes of participant's dating partner, scale of 1-10 (1=awful, 10=great, N/A = no opinion)<br>
> Attractive, Sincere, Intelligent, Fun, Ambitious, Shared Interests/Hobbies
<br>

**like:**
> How much participant liked the person on the date? (1=don't like at all, 10=like a lot)
<br>

**prob:**
> How probable participant thought the person on the date would say 'yes' to participant?  (1=not probable, 10=extremely probable)
<br>

**met:**
> Whether or not participant had met the person on the date before (1 = yes, 2 = no)
<br>

**match_es:**
> Participant's estimate on how many matches he or she would get (a match occurs when the participant and the dating partner both check “Yes” next to decision)?
<br>

### 4. Half way through meeting all potential dates during the night of the speed dating event, participants were asked to rate the importance of attributes:

**attr1_s sinc1_s, intel1_s, fun1_s, amb1_s, shar1_s:**
> Rating of importance of the following attributes in a potential date on a scale of 1-10: (1=not at all important, 10=extremely important)<br>
> Attractive, Sincere, Intelligent, Fun, Ambitious, Has shared interests/hobbies
<br>

**attr3_s, sinc3_s, intel3_s, fun3_s, amb3_s:**
> Self rating of participant's own attributes, on a scale of 1-10 (1=awful, 10=great)<br>
> Attractive, Sincere, Intelligent, Fun, Ambitious
<br>

### 5. Survey filled out the day after participating in the event but before receiving their matches.  Subjects must submit this in order to be sent their matches.

**satis_2:**
> Overall, how satisfied were you with the people you met? (1=not at all satisfied, 10=extremely satisfied)
<br>

**length:**
> Evaluate the length of the speed date.  Four minutes is:
> Too little=1
> Too much=2
> Just Right=3
<br>

**numdat_2:**
> The number of Speed "Dates" you had was:	
> Too few=1
> Too many=2
> Just right=3
<br>

**attr7_2, sinc7_2, intel7_2, fun7_2, amb7_2, shar7_2:**
> Importance rating of the following attributes in a potential date (distribute 100 points among six attributes based on importance).  When assigning points, participant was instructed to think about how he or she actually made yes/no decisions on date partners<br>
> Attractive, Sincere, Intelligent, Fun, Ambitious, Has shared interests/hobbies
<br>

**attr4_2, sinc4_2, intel4_2, fun4_2, amb4_2, shar4_2:**
> Rating of what participant believs MOST fellow men/women look for in the opposite sex (distribute 100 points among six attributes based on importance)<br>
> Attractive, Sincere, Intelligent, Fun, Ambitious, Has shared interests/hobbies
<br>

**attr2_2, sinc2_2, intel2_2, fun2_2, amb2_2, shar2_2:**
> Rating of what participant thinks the opposite sex looks for in a date (distribute 100 points among six attributes based on importance)<br>
> Attractive, Sincere, Intelligent, Fun, Ambitious, Has shared interests/hobbies
<br>

**attr3_2, sinc3_2, intel3_2, fun3_2, amb3_2:**
> Participant self rating of participant's own attributes, on a scale of 1-10 (1=awful, 10=great)<br>
> Attractive, Sincere, Intelligent, Fun, Ambitious
<br>

**attr5_2, sinc5_2, intel5_2, fun5_2, amb5_2:**
> Participant's ratings of how he or she thinks is perceived by otherson a scale of 1-10 (1=awful, 10=great)<br>
> Attractive, Sincere, Intelligent, Fun, Ambitious
<br>

### 6. Subjects filled out 3-4 weeks after they had been sent their matches

**you_call:**
> Number of matches contacted by participant to set up a date
<br>

**them_cal:**
> Number of matches who contacted the participant to set up a date
<br>

**date_3:**
> Whether the participant had been on a date with any of the matches
> Yes=1
> No=0
<br>

**num_in_3:**
> Number of matches participant has gone on dates with.
<br>

**numdat_3:**
> Number of dates with patches a participant went on (can be multiple dates for each match)
<br>

**attr1_3, sinc1_3, intel1_3, fun1_3, amb1_3, shar1_3:**
> Importance rating of the following attributes in a potential date (distribute 100 points among six attributes based on importance).  When assigning points, participant was instructed to think about how he or she actually made yes/no decisions on date partners<br>
> Attractive, Sincere, Intelligent, Fun, Ambitious, Has shared interests/hobbies
<br>
 
**attr7_3, sinc7_3, intel7_3, fun7_3, amb7_3, shar7_3:**
> Importance rating of the following attributes in how people actually made yes/no decisions on date partners. (Unclear how this is different from the above, but data is different)<br>
> Attractive, Sincere, Intelligent, Fun, Ambitious, Has shared interests/hobbies
<br>

**attr4_3, sinc4_3, intel4_3, fun4_3, amb4_3, shar4_3:**
> Rating of what participant believs MOST fellow men/women look for in the opposite sex on a scale of 1-10 (1=not at all important, 10=extremely important)<br>
> Attractive, Sincere, Intelligent, Fun, Ambitious, Has shared interests/hobbies
<br>

**attr2_3, sinc2_3, intel2_3, fun2_3, amb2_3, shar2_3:**
> Rating of what participant thinks the opposite sex looks for in a date on a scale of 1-10 (1=not at all important, 10=extremely important)<br>
> Attractive, Sincere, Intelligent, Fun, Ambitious, Has shared interests/hobbies
<br>

**attr3_3, sinc3_3, intel3_3, fun3_3, amb3_3:**
> Participant self rating of participant's own attributes, on a scale of 1-10 (1=awful, 10=great)<br>
> Attractive, Sincere, Intelligent, Fun, Ambitious
<br>

**attr5_3, sinc5_3, intel5_3, fun5_3, amb5_3:**
> Participant's ratings of how he or she thinks is perceived by otherson a scale of 1-10 (1=awful, 10=great)
> Attractive, Sincere, Intelligent, Fun, Ambitious
<br>

### 7. Other

**dec_o:**
> decision of partner the night of event
<br>
