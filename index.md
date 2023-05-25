# The "grep" command  
## option 1
**for the first command that uses "-r":**  
`grep -r "password" ./technical`  
**the output is:**  
```
./technical/biomed/1471-2105-3-2.txt:            then email an initial password to the user at the
./technical/biomed/1471-2105-3-2.txt:            pieces of information (username and password) necessary   
./technical/biomed/1471-2105-3-2.txt:            user may change the password and update the user
./technical/biomed/1471-2350-4-6.txt:          from this study into the password-protected STOP II
./technical/biomed/1472-6920-1-3.txt:            not use usernames and passwords to track individual       
./technical/government/Gen_Account_Office/InternalControl_ai00021p.txt:persons; and frequent changes of passwords and deactivation of
./technical/government/Gen_Account_Office/InternalControl_ai00021p.txt:former employees' passwords.        
./technical/government/Gen_Account_Office/May1998_ai98068.txt:creating new system user accounts, issuing new passwords, and
./technical/government/Gen_Account_Office/May1998_ai98068.txt:and promptly or controls, such as passwords and related access
./technical/government/Gen_Account_Office/May1998_ai98068.txt:warnings against password disclosure by including prohibitions
./technical/government/Gen_Account_Office/May1998_ai98068.txt:standard at the same institution was a prescribed minimum password
./technical/government/Gen_Account_Office/May1998_ai98068.txt:disclosing sensitive information or passwords.
./technical/government/Gen_Account_Office/May1998_ai98068.txt:passwords in response to seemingly innocent requests from strangers
./technical/government/Gen_Account_Office/May1998_ai98068.txt:of backing up files and protecting passwords;./technical/government/Gen_Account_Office/ai2132.txt:codes and passwords provide less control over data than do
./technical/government/Gen_Account_Office/ai2132.txt:Traditional user identification codes and passwords, while
./technical/government/Gen_Account_Office/ai9868.txt:creating new system user accounts, issuing new passwords, and
./technical/government/Gen_Account_Office/ai9868.txt:and promptly or controls, such as passwords and related access
./technical/government/Gen_Account_Office/ai9868.txt:warnings against password disclosure by including prohibitions
./technical/government/Gen_Account_Office/ai9868.txt:standard at the same institution was a prescribed minimum password
./technical/government/Gen_Account_Office/ai9868.txt:disclosing sensitive information or passwords.        
./technical/government/Gen_Account_Office/ai9868.txt:passwords in response to seemingly innocent requests from strangers
./technical/government/Gen_Account_Office/ai9868.txt:of backing up files and protecting passwords;
./technical/government/Gen_Account_Office/d01186g.txt:password and user identification based systems, used 
to
./technical/plos/pmed.0020206.txt:        has developed a password-protected Web site, PatientWeb (https://fisher.mgh.harvard.edu/),
```

the command recursively search for the word `password` and is useful for not having to go through different files and directories to search for the one word. 

**the second use of -r goes as:**
`grep -r "uncanny" ./technical`  
**the output is:**  
`./technical/government/Media/Lindsays_legacy.txt:understanding, a maturity of judgment and an uncanny ability to`  
the command recursively searches for the word uncanny in all files, and is useful for finding a word without looking through every single file and directory. 


This command will recursively search for the word "password" in all files under the ./technical directory and output the matching lines. I found this use of grep using ChatGPT.   

**GPT PROMPT**:  
`give me four different examples of "-" commands being used under grep commands, and tell me what they mean.`  
**GPT OUTPUT**:  
```
Option 1: -r or --recursive
This option allows grep to search recursively in all files under a directory. It is useful when searching for a pattern in a large number of files in a directory and its subdirectories.
```  



## option 2  
**the next command uses -i which searches for words that ignores case sensitivity:**  
`grep -i "faa:" ./technical/911report/chapter-1.txt`  
I found this command using ChatGPT.  
**GPT PROMPT**:  
`give me four different examples of "-" commands being used under grep commands, and tell me what they mean.`  
**GPT OUTPUT**:  
```
Option 2: -i or --ignore-case
This option makes grep search case-insensitively for the given pattern. It is useful when the pattern can have different cases.
```  


**the output is:** 
```
FAA: Hi. Boston Center TMU [Traffic Management Unit], we have a problem here. We have a hijacked aircraft headed towards New York, and we need you guys to, we need someone to scramble some F-16s or something up there, help us out.
    FAA: No, this is not an exercise, not a test.
    FAA: UAL 175 go ahead.
    FAA: Oh, okay. I'll pass that along over here.
    At 9:21, NEADS received a report from the FAA: FAA: Military, Boston Center. I just had a report that American 11 is still in the air, and it's on its way towards-heading towards Washington. NEADS: Okay. American 11 is still in the air?
    FAA: Yes.
    FAA: That was another-it was evidently another aircraft that hit the tower. That's the latest report we have.
    FAA: I'm going to try to confirm an ID for you, but I would assume he's somewhere over, uh, either New 
Jersey or somewhere further south.
    NEADS: Okay. So American 11 isn't the hijack at all then, right? FAA: No, he is a hijack.
    FAA: Yes.
    FAA: Yes. This could be a third aircraft.
    NEADS: United nine three, have you got information on that yet? FAA: Yeah, he's down.
    FAA: Yes.
    NEADS: When did he land? 'Cause we have got confirmation- FAA: He did not land.
    FAA: Yes. Somewhere up northeast of Camp David.
    FAA: That's the last report. They don't know exactly where.
```  
The command above search for `faa:` in the file `chapter-1.txt` and ignores case sensitivity. This is useful for simply finding the word without a restriction like case sensitivity that could keep you from finding the word. 
**second use:**  
`grep -i "AppRopRiate" ./technical/911report/chapter-1.txt`  
**output:**  
```
there would be time to address the problem through the appropriate FAA and NORAD chains of command; and    
    NORAD officials have maintained consistently that had the passengers not caused United 93 to crash, the military would have prevented it from reaching Washington, D.C. That conclusion is based on a version of events that we now know is incorrect. The Langley fighters were not scrambled in response to United 93; NORAD did not have 47 minutes to intercept the flight; NORAD did not even know the plane was hijacked until after it had crashed. It is appropriate, therefore, to reconsider whether United 93 would have been intercepted.
```  
The command us searching for `appropriate` in the file `chapter-1.txt` under the director `./technical/911report`, it is important becuase the file is very big and could be case sensitive so it's easier to search for the word.  
## option 3  
**command:**  
`grep -v "password" ./technical/biomed/rr166.txt`  
this command search through the file and simply returns every single line that does not contain the word password. I found this using ChatGPT.   
**GPT PROMPT**:  
`give me four different examples of "-" commands being used under grep commands, and tell me what they mean.`  
**GPT OUTPUT**:  
```
Option 3: -v or --invert-match
This option makes grep output the non-matching lines. It is useful when searching for lines that do not match a pattern.
```  

**output:**  
```
Introduction
        The concept of lung fibroblasts as effector cells in the
        pathogenesis of idiopathic pulmonary fibrosis (IPF) has
        recently evolved [ 1 2 ] . Lung fibroblasts respond,
        in vitro , to inflammatory cytokines
        by producing growth factors and collagen, resulting in
        fibroblast proliferation and extracellular matrix
        deposition [ 2 3 4 ] . In addition, activated lung
        fibroblasts have been shown to produce large amounts of
        inflammatory cytokines and chemokines,
        in vitro , and hence, these cells may
        also have a role as effector-inflammatory cells [ 1 2 ] .
        This capacity to produce both inflammatory and fibrotic
        factors could mean that phenotypically altered lung
        fibroblasts act simultaneously as effector and target
        cells, via paracrine and autocrine mechanisms, perpetuating
        the fibrotic process [ 2 ] .
        Prostanoids are important regulators of fibroblast
        function [ 5 6 7 8 9 ] . Prostaglandin (PG)E
        2 is thought to have antifibrotic
        properties
        in vitro , but also can have
        proinflammatory effects both
        in vivo and
        in vitro [ 10 11 12 ] . Thromboxane
        (TX)A
        2 increases proliferation, and DNA and
        RNA synthesis in several cell types, including fibroblasts
        and smooth muscle like glomerular mesangial cells [ 13 14
        15 16 ] . Conversely, prostacyclin (PGI
        2 ) decreases smooth muscle cell
        proliferation and collagen synthesis [ 17 18 ] .
        Many cell types, including lung fibroblasts, contain
        cyclooxygenase (COX), a proximal enzyme in prostanoid
        production, and can generate prostanoids [ 19 ] . It has
        been previously reported that IPF lung fibroblasts have
        decreased COX-2 expression compared to normal lung
        fibroblasts and, hence, have decreased PGE
        2 production [ 12 20 21 ] . Because of
        these findings and the fact that PGs are important
        fibroblast regulators, we sought to investigate whether
        abnormalities in COX-2 expression could be associated with
        an altered balance between profibrotic and antifibrotic
        PGs. We hypothesized that fibroblasts from the lungs of
        patients with IPF (HF-IPF) have an altered PG balance
        compared to normal lung fibroblasts (HF-NL). This
        phenotypical abnormality could be an important factor in
        the pathogenesis of IPF.
```  
**second use of command:**  
`grep -v "Alcohol" ./technical/government/Media/Farm_workers.txt`  
this command searches for the word Alcohol in the file `Farm_workers.txt`, and prints out every single line that does NOT match the searched word.  

**output:**  
```
Report: Farm workers plagued by pesticides Legal aid group
alleges laws violated
Coleman Cornelius
The farm workers said they knew they had breathed poison moments
after a crop-duster buzzed nearby, spraying a field of sweet corn
with pesticides to kill mites and worms.
Most of the 20 migrant farm workers, in an adjacent lettuce
field in Olathe, said they felt sick immediately: They gasped for
breath, had pounding headaches, irritated eyes and swollen, numb
tongues. Some vomited as a cloud of white chemicals settled on
fields around them.
The farm workers in the western Colorado community said they
left the lettuce field when sprayed, but a foreman ordered them to
continue working, saying the crop-duster had released a harmless
solution of soap and water.
A new study by Colorado Legal Services, the first of its kind in
the Rocky Mountain region, says such migrant workers at farms
statewide are regularly exposed to hazardous pesticides in
violation of federal laws.
The company that hired the workers for the Olathe farm and the
farmer whose land they were working have denied any role in making
the workers sick.
The lettuce workers, talking about their incident last week,
said their experience illustrates the problems.
'We were cutting lettuce, and we saw the plane coming. It was
spraying, and the wind was blowing, so it blew toward us,' said
Blanca Chavez, 44, who sought shelter in a portable toilet. 'We
ingested it. It was like a fog.'
Another farm worker, 22-year-old Marcelina Lopez, was five
months pregnant during the reported Olathe spraying incident on
June 29. She developed stomach cramps and a rash on her belly and
arms, Lopez said as she and six others on the lettuce crew
discussed the incident last week.
Lopez saw a doctor three days after the spraying, but that
heightened her concern.
'The doctor couldn't tell if the baby was affected,' her husband
said in Spanish. 'We worry a lot because we don't know if the baby
will be affected.'
Jim Dorsey, an officer of Cactus Produce - the Scottsdale,
Ariz., farm-labor contractor that employs the crew - said company
policy requires that incidents of pesticide exposure be reported
immediately. He said crew supervisors did not report what workers
described. Lacking field or physician reports, he questioned
whether the incident occurred.
Grower Tom Humphrey also was skeptical.
'I think this is a crock,' said Humphrey, a vegetable farmer for
30 years. 'You're listening to somebody who wants money for
nothing.'
Nevertheless, Chavez took her case to Colorado Legal Services, a
nonprofit law firm that represents low-income clients in civil
cases around the state. She and the other farm workers said they
agreed to publicly discuss the Olathe incident to illustrate the
hazards laborers face in the fields and to push growers to abide by
pesticide-safety laws.
Chavez's case mirrors the findings of the survey by Colorado
Legal Services, which reports that migrant workers at farms
statewide are regularly exposed to hazardous pesticides in
violation of federal laws.
The exposure comes from chemical residue on plants in farm
fields and from pesticide drift, such as the incidents lettuce
workers described, according to the survey.
Legal Services conducted interviews with 88 farm workers in some
of Colorado's most abundant agricultural regions last year and
found that half of those surveyed had experienced symptoms of
pesticide exposure. The symptoms included skin rash, inflamed eyes,
headaches and irritation of the nose and throat.
Those surveyed worked in Weld County, the Arkansas Valley, the
San Luis Valley and the Western Slope and took part in 30-minute
interviews at farm-labor housing in those regions.
Kimi Jackson, author of the Colorado Legal Services study, said
the surveys were detailed and the responses consistent across the
state.
'It's striking that so many farm workers report experiencing
symptoms of pesticide exposure,' said Jackson, director of the
agency's pesticide project. 'Imagine in your own office if half the
workers had experienced symptoms like that. That's very high.'
Ray Christensen, executive vice president of the Colorado Farm
Bureau, said growers on the state's 20,000 farms consider pesticide
safety important for themselves and their employees, in part
because they want to maintain a productive workforce and avoid
liability.
'Pesticides can be very injurious if they are not handled
properly. I think farmers across the United States realize that,'
Christensen said.
Yet the Legal Services report faults growers, farm-labor
contractors and crop-dusters for routinely failing to abide by
federal regulations meant to protect worker health.
The study also demands that the U.S. Environmental Protection
Agency and Colorado Department of Agriculture better enforce the
10- year-old laws, collectively called the Worker Protection
Standard.
The laws require that farm workers be prevented from entering
fields treated with pesticides until recommended times have
elapsed. The laws also mandate that workers be trained in pesticide
safety, are notified of fields that have been sprayed, have fresh
water to wash chemicals from their skin and receive emergency
medical help in cases of pesticide exposure or illness.
EPA records show employers regularly fail to follow the
rules.
Last year, the agency's regional office inspected 23 Colorado
farms, and 20 failed to fully comply with federal laws meant to
protect farm workers from pesticides, said Tim Osag, an enforcement
coordinator. Those farms got warning letters and will be inspected
again, he said.
'Workers were not being trained. There was no central location
where the required information was being posted, and several of
them did not have decontamination supplies,' said Britta Campbell,
an EPA enforcement officer who conducted most of the farm
inspections.
'Obviously we have a regulation which is not being followed,'
Osag said. 'There is a potential that we're exposing workers to
increased health risks.'
Migrant farm workers - 16,000 to 40,000 in Colorado, according
to the U.S. Department of Labor - are critical to the state's $1.23
billion agriculture industry. They travel from farm to farm,
tending and harvesting fruits and vegetables.
Farm workers earn an average of $5.15 an hour for jobs that
often require fieldwork from sunup to sundown during the growing
season, Jackson said.
Many migrant farm workers are reluctant to report pesticide
problems because they fear they will lose their jobs, laborers
said.
'We do the work in the fields because we don't have a lot of
education, and in this country you need to have an education to
have a good job. We don't feel like we have any options,' said
Maria Figeroa, 54, a member of the lettuce crew reportedly overcome
by pesticide drift in Olathe.
She and other crew members spoke in Spanish through an
interpreter.
Pesticides, widely used to increase crop yields, have become a
leading health concern among migrant farm workers. Coloring books
distributed to the children of farm workers in Weld County warn
youngsters to run when they see crop-dusters spraying
'pesticidas.'
In 1998, Cesar Chavez fasted for 36 days in California to
underscore the dangers of pesticides to farm workers and their
children. It was the last and longest fast for the 61-year-old
civil-rights activist.
The following year, Chavez's organization, United Farm Workers,
released a seminal study addressing the health effects of
pesticides on farmworkers. The report, 'Fields of Poison,' found
that California farmworkers face greater risk of pesticide
poisoning than any other segment of the population and are not
adequately protected.
Like the Colorado report, it called for stronger enforcement of
existing laws.
Little research has been conducted on the long-term health
effects of pesticides on farm workers.
But some research points to danger: A study published earlier
this year in the American Journal of Industrial Medicine found that
migrant farm workers in California, most of them Hispanic, have a
59 percent higher risk of developing leukemia than other Hispanics
in the state.
Field laborers have a 69 percent higher risk for stomach cancer.
Male workers also have a higher chance of developing brain cancer,
while female workers have a higher risk for uterine cancer,
according to the study, which linked the risks to pesticide
exposure.
Researchers compared farm worker data from United Farm Workers
with that from the California Cancer Registry.
It is hard to prove that worker illness is a result of pesticide
exposure in the field because other things, both on and off the
job, can trigger physical symptoms, said Dr. Suzanne Wuerthele, an
EPA toxicologist in Denver.
Yet dozens of chemicals commonly used to kill weeds, fungus and
insects on agricultural crops can cause immediate sickness in
people who inhale, swallow or absorb them through skin contact,
Wuerthele said.
Recent research raises questions about the connection between
pesticide exposure and long-term health problems, such as chronic
headaches, sleep disorders, vision problems, nerve damage, cancer
and birth defects, Wuerthele said.
'These chemicals are always dangerous to humans. That's why they
have to be used correctly,' she said. 'They are designed to kill
things, and they can be toxic to humans.'
Chavez said she called Colorado Legal Services because she felt
sick and did not know where to turn.
'They're not worms,' said Guierrmo Othon, Chavez's husband, who
is also a lettuce worker. 'These are human lives.'
```  
## option 4  
The last command which returns the amount of times the given "value" appears:  
`grep -c "password" ./technical/government/Alcohol_Problems/Session2-PDF.txt`  
it's important because you don't have to go in the files manually and ctrl+f your way into finding how many times it actually appears, it's just easier this way.  
**the output:**  
`0`  
**second command:**  
`grep -c "Alcohol" ./technical/government/Alcohol_Problems/Session4-PDF.txt`  
The command is useful for searching for acohol in an related file and counting how many times it actually comes up, and since they are related topics it is more even more beneficial, I found bouth uses of the command -c through ChatGPT.  
**second output**:  
`31`  

**GPT PROMPT**:  
`give me four different examples of "-" commands being used under grep commands, and tell me what they mean.`  
**GPT OUTPUT**:  
``` 
Option 4: -c or --count
This option makes grep output the number of matching lines instead of the lines themselves. It is useful when counting the number of occurrences of a pattern in a file or set of files.
```  


















