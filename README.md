@prefix : <http://www.cs.ccsu.edu/MounikaMendu/University.owl#> .
@prefix owl: <http://www.w3.org/2002/07/owl#> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix xml: <http://www.w3.org/XML/1998/namespace> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@base <http://www.cs.ccsu.edu/MounikaMendu/University.owl> .

<http://www.cs.ccsu.edu/MounikaMendu/University.owl> rdf:type owl:Ontology ;
                                                      rdfs:comment """Name: Mounika Mendu
Course: CS407
Domain: University
Overview: This project contains major aspects of University domain including super class and subclass hierarchy.""" .

#################################################################
#    Object Properties
#################################################################

###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#has_Appeared
:has_Appeared rdf:type owl:ObjectProperty ;
              rdfs:subPropertyOf owl:topObjectProperty ;
              rdfs:domain :Student ;
              rdfs:range :Examination .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#has_Attended
:has_Attended rdf:type owl:ObjectProperty ;
              rdfs:subPropertyOf owl:topObjectProperty ;
              owl:inverseOf :is_Attended_By ;
              rdfs:domain :School_Activities ;
              rdfs:range :Person .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#has_Enrolled_In
:has_Enrolled_In rdf:type owl:ObjectProperty ;
                 rdfs:subPropertyOf owl:topObjectProperty ;
                 rdfs:domain :Student ;
                 rdfs:range :Programs .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#has_Grade
:has_Grade rdf:type owl:ObjectProperty ;
           rdfs:subPropertyOf owl:topObjectProperty .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#has_Prerequisite
:has_Prerequisite rdf:type owl:ObjectProperty ;
                  rdfs:subPropertyOf owl:topObjectProperty ;
                  owl:inverseOf :is_Prerequisite_Of ;
                  rdfs:domain :Programs ;
                  rdfs:range :Programs .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#is_Attended_By
:is_Attended_By rdf:type owl:ObjectProperty ;
                rdfs:subPropertyOf owl:topObjectProperty ;
                rdfs:domain :School_Activities ;
                rdfs:range :Person .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#is_Offered_By
:is_Offered_By rdf:type owl:ObjectProperty ;
               rdfs:subPropertyOf owl:topObjectProperty ;
               owl:inverseOf :offers ;
               rdfs:domain :Programs ;
               rdfs:range :Teaching_Staff .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#is_Prerequisite_Of
:is_Prerequisite_Of rdf:type owl:ObjectProperty ;
                    rdfs:subPropertyOf owl:topObjectProperty ;
                    rdfs:domain :Programs ;
                    rdfs:range :Programs .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#is_Used_By
:is_Used_By rdf:type owl:ObjectProperty ;
            rdfs:subPropertyOf owl:topObjectProperty ;
            owl:inverseOf :uses ;
            rdfs:domain :Library ;
            rdfs:range :Programs .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#offers
:offers rdf:type owl:ObjectProperty ;
        rdfs:subPropertyOf owl:topObjectProperty ;
        rdfs:domain :Teaching_Staff ;
        rdfs:range :Programs .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#studies
:studies rdf:type owl:ObjectProperty ;
         rdfs:subPropertyOf owl:topObjectProperty .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#teaches
:teaches rdf:type owl:ObjectProperty ;
         rdfs:subPropertyOf owl:topObjectProperty ;
         rdfs:domain :Staff ;
         rdfs:range :Programs .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#uses
:uses rdf:type owl:ObjectProperty ;
      rdfs:subPropertyOf owl:topObjectProperty ;
      rdfs:domain :Library ;
      rdfs:range :Programs .


#################################################################
#    Data properties
#################################################################

###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Activity_Date
:Activity_Date rdf:type owl:DatatypeProperty ;
               rdfs:subPropertyOf owl:topDataProperty ;
               rdfs:domain :School_Activities ;
               rdfs:range xsd:string .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Activity_Place
:Activity_Place rdf:type owl:DatatypeProperty ;
                rdfs:subPropertyOf owl:topDataProperty ;
                rdfs:domain :School_Activities ;
                rdfs:range xsd:string .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Admitted_Year
:Admitted_Year rdf:type owl:DatatypeProperty ;
               rdfs:subPropertyOf owl:topDataProperty ;
               rdfs:domain :Student ;
               rdfs:range xsd:integer .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Email_Id
:Email_Id rdf:type owl:DatatypeProperty ;
          rdfs:subPropertyOf owl:topDataProperty ;
          rdfs:domain :Person ;
          rdfs:range xsd:string .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Gender
:Gender rdf:type owl:DatatypeProperty .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Graduated_Year
:Graduated_Year rdf:type owl:DatatypeProperty ;
                rdfs:subPropertyOf owl:topDataProperty ;
                rdfs:domain :Student ;
                rdfs:range xsd:integer .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Qualification
:Qualification rdf:type owl:DatatypeProperty ;
               rdfs:subPropertyOf owl:topDataProperty ;
               rdfs:domain :Person ;
               rdfs:range xsd:string .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#age
:age rdf:type owl:DatatypeProperty ;
     rdfs:subPropertyOf owl:topDataProperty ;
     rdfs:domain :Person ;
     rdfs:range xsd:integer .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#author
:author rdf:type owl:DatatypeProperty ;
        rdfs:subPropertyOf owl:topDataProperty ;
        rdfs:domain :Books ;
        rdfs:range xsd:string .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#first_Name
:first_Name rdf:type owl:DatatypeProperty ;
            rdfs:subPropertyOf owl:topDataProperty ;
            rdfs:domain :Person ;
            rdfs:range xsd:string .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#high_Score
:high_Score rdf:type owl:DatatypeProperty ;
            rdfs:subPropertyOf owl:topDataProperty ;
            rdfs:domain :Examination ;
            rdfs:range xsd:integer .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#last_Name
:last_Name rdf:type owl:DatatypeProperty ;
           rdfs:subPropertyOf owl:topDataProperty ;
           rdfs:domain :Person ;
           rdfs:range xsd:string .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#passing_Score
:passing_Score rdf:type owl:DatatypeProperty ;
               rdfs:subPropertyOf owl:topDataProperty ;
               rdfs:domain :Examination ;
               rdfs:range xsd:integer .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#phone
:phone rdf:type owl:DatatypeProperty ;
       rdfs:subPropertyOf owl:topDataProperty ;
       rdfs:domain :Person ;
       rdfs:range xsd:string .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#staff_Id
:staff_Id rdf:type owl:DatatypeProperty ;
          rdfs:subPropertyOf owl:topDataProperty ;
          rdfs:domain :Person ;
          rdfs:range xsd:integer .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#student_Id
:student_Id rdf:type owl:DatatypeProperty ;
            rdfs:subPropertyOf owl:topDataProperty ;
            rdfs:domain :Person ;
            rdfs:range xsd:integer .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#title
:title rdf:type owl:DatatypeProperty ;
       rdfs:subPropertyOf owl:topDataProperty ;
       rdfs:domain :Books ;
       rdfs:range xsd:string .


#################################################################
#    Classes
#################################################################

###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Activity_List
:Activity_List rdf:type owl:Class ;
               rdfs:subClassOf :School_Activities .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Administration
:Administration rdf:type owl:Class ;
                rdfs:subClassOf :Departments .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Administrative
:Administrative rdf:type owl:Class ;
                rdfs:subClassOf :Non_Teaching_Staff .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Afternoon
:Afternoon rdf:type owl:Class ;
           rdfs:subClassOf :ScheduledTimings .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Arts
:Arts rdf:type owl:Class ;
      rdfs:subClassOf :Undergraduate .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Books
:Books rdf:type owl:Class ;
       rdfs:subClassOf :Library .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#CCSU
:CCSU rdf:type owl:Class ;
      rdfs:subClassOf :University .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Class_Type
:Class_Type rdf:type owl:Class ;
            rdfs:subClassOf :Semister .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Club_Activities
:Club_Activities rdf:type owl:Class ;
                 rdfs:subClassOf :Activity_List .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Computer_Information_Technology
:Computer_Information_Technology rdf:type owl:Class ;
                                 rdfs:subClassOf :MastersDegreeProgram .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Computer_Science
:Computer_Science rdf:type owl:Class ;
                  rdfs:subClassOf :Computer_Information_Technology ;
                  owl:disjointWith :Networking .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Conference_Activities
:Conference_Activities rdf:type owl:Class ;
                       rdfs:subClassOf :Activity_List .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Departments
:Departments rdf:type owl:Class ;
             rdfs:subClassOf :CCSU .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Evening
:Evening rdf:type owl:Class ;
         rdfs:subClassOf :ScheduledTimings .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Examination
:Examination rdf:type owl:Class ;
             owl:equivalentClass [ rdf:type owl:Restriction ;
                                   owl:onProperty :has_Appeared ;
                                   owl:someValuesFrom :Examination
                                 ] ;
             rdfs:subClassOf :CCSU .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Fall
:Fall rdf:type owl:Class ;
      rdfs:subClassOf :Terms .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Fees
:Fees rdf:type owl:Class ;
      rdfs:subClassOf :Registrar .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Files
:Files rdf:type owl:Class ;
       rdfs:subClassOf :Library .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Final
:Final rdf:type owl:Class ;
       rdfs:subClassOf :Examination .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Fulltime
:Fulltime rdf:type owl:Class ;
          rdfs:subClassOf :Teaching_Staff .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Grading
:Grading rdf:type owl:Class ;
         rdfs:subClassOf :Registrar .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Graduate
:Graduate rdf:type owl:Class ;
          rdfs:subClassOf :Programs ;
          owl:disjointWith :Undergraduate .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Homework
:Homework rdf:type owl:Class ;
          rdfs:subClassOf :Examination .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Junior_Student
:Junior_Student rdf:type owl:Class ;
                rdfs:subClassOf :Student .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Library
:Library rdf:type owl:Class ;
         rdfs:subClassOf :Departments .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Maintainance
:Maintainance rdf:type owl:Class ;
              rdfs:subClassOf :Non_Teaching_Staff .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#MastersDegreeProgram
:MastersDegreeProgram rdf:type owl:Class ;
                      rdfs:subClassOf :Graduate .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Midterm
:Midterm rdf:type owl:Class ;
         rdfs:subClassOf :Examination .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Morning
:Morning rdf:type owl:Class ;
         rdfs:subClassOf :ScheduledTimings .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Music
:Music rdf:type owl:Class ;
       rdfs:subClassOf :Undergraduate .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Networking
:Networking rdf:type owl:Class ;
            rdfs:subClassOf :Computer_Information_Technology .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Non_Teaching_Staff
:Non_Teaching_Staff rdf:type owl:Class ;
                    rdfs:subClassOf :Staff ;
                    owl:disjointWith :Teaching_Staff .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#OnCampus
:OnCampus rdf:type owl:Class ;
          rdfs:subClassOf :Class_Type .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Online
:Online rdf:type owl:Class ;
        rdfs:subClassOf :Class_Type .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Parttime
:Parttime rdf:type owl:Class ;
          rdfs:subClassOf :Teaching_Staff .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Person
:Person rdf:type owl:Class ;
        rdfs:subClassOf :CCSU .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Programs
:Programs rdf:type owl:Class ;
          rdfs:subClassOf :CCSU .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Projects
:Projects rdf:type owl:Class ;
          rdfs:subClassOf :Examination .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Quiz
:Quiz rdf:type owl:Class ;
      rdfs:subClassOf :Examination .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Registrar
:Registrar rdf:type owl:Class ;
           rdfs:subClassOf :Departments .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#ScheduledTimings
:ScheduledTimings rdf:type owl:Class ;
                  owl:equivalentClass [ rdf:type owl:Class ;
                                        owl:unionOf ( :Afternoon
                                                      :Evening
                                                      :Morning
                                                    )
                                      ] ;
                  rdfs:subClassOf :Timings .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#School_Activities
:School_Activities rdf:type owl:Class ;
                   rdfs:subClassOf :CCSU .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Science
:Science rdf:type owl:Class ;
         rdfs:subClassOf :Undergraduate .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Semister
:Semister rdf:type owl:Class ;
          rdfs:subClassOf :CCSU .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Senior_Student
:Senior_Student rdf:type owl:Class ;
                rdfs:subClassOf :Student .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Software_Engineering
:Software_Engineering rdf:type owl:Class ;
                      rdfs:subClassOf :MastersDegreeProgram .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Spring
:Spring rdf:type owl:Class ;
        rdfs:subClassOf :Terms .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Staff
:Staff rdf:type owl:Class ;
       rdfs:subClassOf :Person .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Student
:Student rdf:type owl:Class ;
         rdfs:subClassOf :Person .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Summer
:Summer rdf:type owl:Class ;
        rdfs:subClassOf :Terms .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Supporting
:Supporting rdf:type owl:Class ;
            rdfs:subClassOf :Non_Teaching_Staff .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Teaching_Staff
:Teaching_Staff rdf:type owl:Class ;
                rdfs:subClassOf :Staff .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Terms
:Terms rdf:type owl:Class ;
       rdfs:subClassOf :Semister .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Timings
:Timings rdf:type owl:Class ;
         rdfs:subClassOf :CCSU .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Undergraduate
:Undergraduate rdf:type owl:Class ;
               rdfs:subClassOf :Programs .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#University
:University rdf:type owl:Class .


#################################################################
#    Individuals
#################################################################

###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#ART_130
:ART_130 rdf:type owl:NamedIndividual ,
                  :Arts .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#ART_210
:ART_210 rdf:type owl:NamedIndividual ,
                  :Arts .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#ART_215
:ART_215 rdf:type owl:NamedIndividual ,
                  :Arts .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#ART_224
:ART_224 rdf:type owl:NamedIndividual ,
                  :Arts ;
         :has_Prerequisite :ART_130 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#ART_230
:ART_230 rdf:type owl:NamedIndividual ,
                  :Arts .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Accounting
:Accounting rdf:type owl:NamedIndividual ,
                     :Books ;
            :author "Joe B.Hoyle" ;
            :title "Advanced Accounting" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Accounting_Theory
:Accounting_Theory rdf:type owl:NamedIndividual ;
                   :author "Kimberly Ferlauto" ;
                   :title "Contemporary Issues In Accounting" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Asynchronous
:Asynchronous rdf:type owl:NamedIndividual ,
                       :Online .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#B_Above_Average
:B_Above_Average rdf:type owl:NamedIndividual ,
                          :Grading .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#CET_501
:CET_501 rdf:type owl:NamedIndividual ,
                  :Networking ;
         :has_Enrolled_In :Synchronous ;
         :is_Offered_By :Lecture2 ,
                        :Parttime_Lecture3 ;
         :is_Prerequisite_Of :CET_569 ,
                             :CET_594 ,
                             :CET_596 ,
                             :CS_501 ,
                             :CS_502 ;
         :uses :Networking ;
         :title "Applied Networking Technology I" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#CET_569
:CET_569 rdf:type owl:NamedIndividual ,
                  :Networking ;
         :has_Enrolled_In :Synchronous ;
         :has_Prerequisite :CET_501 ;
         :is_Offered_By :Lecture2 ,
                        :Lecture3 ,
                        :Parttime_Lecture1 ,
                        :Parttime_Lecture3 ;
         :title "Network Security Management" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#CET_594
:CET_594 rdf:type owl:NamedIndividual ,
                  :Networking ;
         :has_Enrolled_In :InPerson ;
         :has_Prerequisite :CET_501 ;
         :is_Offered_By :Lecture2 ,
                        :Parttime_Lecture1 ;
         :title "Research Design" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#CET_596
:CET_596 rdf:type owl:NamedIndividual ,
                  :Networking ;
         :has_Enrolled_In :Asynchronous ;
         :has_Prerequisite :CET_501 ;
         :is_Offered_By :Lecture2 ,
                        :Lecture3 ,
                        :Parttime_Lecture1 ;
         :title "Technological Problems and Issues" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#CS_407
:CS_407 rdf:type owl:NamedIndividual ,
                 :Computer_Science ;
        :has_Enrolled_In :Synchronous ;
        :has_Prerequisite :CS_501 ,
                          :CS_502 ;
        :is_Offered_By :Lecture1 ;
        :uses :Semantics ;
        :title "Semnatics Web Technology" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#CS_500
:CS_500 rdf:type owl:NamedIndividual ,
                 :Computer_Science ;
        :has_Enrolled_In :InPerson ;
        :is_Offered_By :Lecture1 ;
        :is_Prerequisite_Of :CS_501 ,
                            :CS_502 ;
        :title "Computer Science for Computer Information Technology" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#CS_501
:CS_501 rdf:type owl:NamedIndividual ,
                 :Computer_Science ;
        :has_Enrolled_In :InPerson ;
        :has_Prerequisite :CS_500 ;
        :is_Offered_By :Lecture1 ;
        :is_Prerequisite_Of :CS_407 ,
                            :CS_560 ,
                            :CS_570 ,
                            :CS_575 ,
                            :CS_595 ;
        :uses :Data_Structures_And_Algorithms ;
        :title "Foundations of Computer Science" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#CS_502
:CS_502 rdf:type owl:NamedIndividual ,
                 :Computer_Science ;
        :has_Enrolled_In :Asynchronous ;
        :has_Prerequisite :CET_501 ,
                          :CS_500 ;
        :is_Offered_By :Lecture3 ,
                       :Parttime_Lecture3 ;
        :title "Computing and Communications Technology" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#CS_530
:CS_530 rdf:type owl:NamedIndividual ,
                 :Computer_Science ;
        :has_Enrolled_In :Synchronous ;
        :has_Prerequisite :CS_501 ,
                          :CS_502 ,
                          :CS_560 ;
        :is_Offered_By :Lecture3 ,
                       :Parttime_Lecture3 ;
        :title "Advanced Software Engineering" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#CS_560
:CS_560 rdf:type owl:NamedIndividual ,
                 :Computer_Science ;
        :has_Enrolled_In :Asynchronous ;
        :has_Prerequisite :CS_501 ,
                          :CS_502 ;
        :is_Offered_By :Lecture3 ;
        :title "Topics in Software Engineering" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#CS_570
:CS_570 rdf:type owl:NamedIndividual ,
                 :Computer_Science ;
        :has_Enrolled_In :InPerson ;
        :has_Prerequisite :CS_501 ,
                          :CS_502 ;
        :is_Offered_By :Lecture1 ;
        :title "Topics in Artificial Intelligence" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#CS_575
:CS_575 rdf:type owl:NamedIndividual ,
                 :Computer_Science ;
        :has_Prerequisite :CS_501 ,
                          :CS_502 ;
        :is_Offered_By :Lecture1 ,
                       :Parttime_Lecture3 ;
        :title "Linked Data Engineering" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#CS_595
:CS_595 rdf:type owl:NamedIndividual ,
                 :Computer_Science ;
        :has_Prerequisite :CS_501 ,
                          :CS_502 ;
        :is_Offered_By :Parttime_Lecture1 ;
        :title "Capstone in Software Engineering" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#CS_Club_Activity
:CS_Club_Activity rdf:type owl:NamedIndividual ,
                           :Club_Activities ;
                  :is_Attended_By :Student1 ,
                                  :Student10 ,
                                  :Student4 ,
                                  :Student5 ,
                                  :Student6 ,
                                  :Student7 ,
                                  :Student9 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#C_Average
:C_Average rdf:type owl:NamedIndividual ,
                    :Grading .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Course_Project
:Course_Project rdf:type owl:NamedIndividual ,
                         :Projects .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#D_Passing_Below_Average
:D_Passing_Below_Average rdf:type owl:NamedIndividual ,
                                  :Grading .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Data_Structures_And_Algorithms
:Data_Structures_And_Algorithms rdf:type owl:NamedIndividual ;
                                :is_Used_By :CS_501 ;
                                :author "Robert Lafore" ;
                                :title "Data Structures And Algorithms in Java" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#EPS_700
:EPS_700 rdf:type owl:NamedIndividual ;
         :is_Offered_By :Parttime_Lecture3 ;
         :title "The Purposes of Education in America" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Employee1
:Employee1 rdf:type owl:NamedIndividual ,
                    :Non_Teaching_Staff ,
                    :Registrar ;
           :Email_Id "jamesonduke"@my.ccsu.edu ;
           :Gender "Male" ;
           :Qualification "MBA" ;
           :first_Name "Jameson" ;
           :last_Name "Duke" ;
           :staff_Id 91359581 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Employee2
:Employee2 rdf:type owl:NamedIndividual ,
                    :Administration ,
                    :Non_Teaching_Staff ;
           :Email_Id "chrisgale"@my.ccsu.edu ;
           :Gender "Female" ;
           :Qualification "MBA" ;
           :first_Name "Chris" ;
           :last_Name "Gayle" ;
           :staff_Id 93818325 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Employee3
:Employee3 rdf:type owl:NamedIndividual ,
                    :Administration ,
                    :Non_Teaching_Staff ;
           :Email_Id "stefenrobert"@my.ccsu.edu ;
           :Gender "Male" ;
           :Qualification "MBA" ;
           :first_Name "Stefen" ;
           :last_Name "Robert" ;
           :phone "938-134-2245" ;
           :staff_Id 92613109 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#FIN_300
:FIN_300 rdf:type owl:NamedIndividual ;
         :is_Offered_By :Parttime_Lecture2 ;
         :title "Personal Finance" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#F_Failure
:F_Failure rdf:type owl:NamedIndividual ,
                    :Grading .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Fall_Finals
:Fall_Finals rdf:type owl:NamedIndividual ,
                      :Final .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Fall_Midterm
:Fall_Midterm rdf:type owl:NamedIndividual ,
                       :Midterm .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Fall_Quizzes
:Fall_Quizzes rdf:type owl:NamedIndividual ,
                       :Quiz .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Homework
:Homework rdf:type owl:NamedIndividual ,
                   :Homework .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#InPerson
:InPerson rdf:type owl:NamedIndividual ,
                   :OnCampus .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Java_Software_Solutions
:Java_Software_Solutions rdf:type owl:NamedIndividual ,
                                  :Books ;
                         :is_Offered_By :Lecture1 ;
                         :is_Used_By :CS_500 ;
                         :author "Lewis Loftus" ;
                         :title "Foundations of Program Design" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Lecture1
:Lecture1 rdf:type owl:NamedIndividual ,
                   :Fulltime ,
                   :Teaching_Staff ;
          :teaches :CS_407 ,
                   :CS_500 ,
                   :CS_501 ,
                   :CS_570 ,
                   :CS_575 ;
          :Email_Id "nelizlatareva"@my.ccsu.edu ;
          :Gender "Female" ;
          :Qualification "PhD" ;
          :first_Name "Neli" ;
          :last_Name "Zlatareva" ;
          :phone "893-397-2635" ;
          :staff_Id 97234243 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Lecture2
:Lecture2 rdf:type owl:NamedIndividual ,
                   :Fulltime ,
                   :Teaching_Staff ;
          :teaches :CET_501 ,
                   :CET_569 ,
                   :CET_594 ,
                   :CET_596 ;
          :Email_Id "williamsmith"@my.ccsu.edu ;
          :Gender "Male" ;
          :Qualification "PhD" ;
          :first_Name "William"^^xsd:string ;
          :last_Name "Smith" ;
          :phone "894-183-0185" ;
          :staff_Id 96243111 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Lecture3
:Lecture3 rdf:type owl:NamedIndividual ,
                   :Fulltime ,
                   :Teaching_Staff ;
          :teaches :CET_569 ,
                   :CET_596 ,
                   :CS_502 ,
                   :CS_530 ,
                   :CS_560 ;
          :Email_Id "rohithsharma"@my.ccsu.edu ;
          :Gender "Male" ;
          :Qualification "PhD" ;
          :first_Name "Rohith" ;
          :last_Name "Sharma" ;
          :phone "847-302-3948" ;
          :staff_Id 62810333 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Lecture4
:Lecture4 rdf:type owl:NamedIndividual ,
                   :Fulltime ,
                   :Teaching_Staff ;
          :Email_Id "siljapandaran"@my.ccsu.edu ;
          :Gender "Female" ;
          :Qualification "PhD" ;
          :first_Name "Silja" ;
          :last_Name "Pandaran" ;
          :phone "219-242-2315" ;
          :staff_Id 63024525 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Lecture5
:Lecture5 rdf:type owl:NamedIndividual ,
                   :Fulltime ,
                   :Teaching_Staff ;
          :Email_Id "harrisjohnson"@my.ccsu.edu ;
          :Gender "Female" ;
          :Qualification "PhD" ;
          :first_Name "Harris" ;
          :last_Name "Johnson" ;
          :phone "860-712-5777" ;
          :staff_Id 62222478 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Librarian
:Librarian rdf:type owl:NamedIndividual ,
                    :Library .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#MUS_121
:MUS_121 rdf:type owl:NamedIndividual ,
                  :Music .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#MUS_122
:MUS_122 rdf:type owl:NamedIndividual ,
                  :Music .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#MUS_235
:MUS_235 rdf:type owl:NamedIndividual ,
                  :Music ;
         :has_Prerequisite :MUS_121 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#MUS_236
:MUS_236 rdf:type owl:NamedIndividual ,
                  :Music ;
         :has_Prerequisite :MUS_122 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Networking
:Networking rdf:type owl:NamedIndividual ,
                     :Books ;
            :is_Used_By :CET_501 ;
            :author "Mark A. Dye" ;
            :title "Introductions to Networks" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Parttime_Lecture1
:Parttime_Lecture1 rdf:type owl:NamedIndividual ,
                            :Parttime ,
                            :Teaching_Staff ;
                   :teaches :CET_596 ,
                            :CS_595 ;
                   :Email_Id "mohinruba"@my.ccsu.edu ;
                   :Gender "Female" ;
                   :Qualification "PhD" ;
                   :first_Name "Mohin" ;
                   :last_Name "Ruba" ;
                   :phone "860-293-1112" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Parttime_Lecture2
:Parttime_Lecture2 rdf:type owl:NamedIndividual ,
                            :Parttime ,
                            :Teaching_Staff ;
                   :teaches :EPS_700 ,
                            :FIN_300 ;
                   :Email_Id "stevestepena"@my.ccsu.edu ;
                   :Gender "Male" ;
                   :Qualification "PhD" ;
                   :first_Name "Steve" ;
                   :last_Name "Stepena" ;
                   :phone "860-239-2923" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Parttime_Lecture3
:Parttime_Lecture3 rdf:type owl:NamedIndividual ,
                            :Parttime ,
                            :Teaching_Staff ;
                   :teaches :CET_501 ,
                            :CET_569 ,
                            :CS_502 ,
                            :CS_530 ,
                            :CS_575 ;
                   :Email_Id "markdemaio"@my.ccsu.edu ;
                   :Gender "Male" ;
                   :Qualification "PhD" ;
                   :first_Name "Mark" ;
                   :last_Name "Demaio" ;
                   :phone "860-198-1138" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#SCI_211
:SCI_211 rdf:type owl:NamedIndividual ,
                  :Science .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#SCI_412
:SCI_412 rdf:type owl:NamedIndividual ,
                  :Science ;
         :has_Prerequisite :SCI_211 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Semantics
:Semantics rdf:type owl:NamedIndividual ;
           :is_Used_By :CS_407 ;
           :author "Pascal Hitzler" ;
           :title "Founadtions Of Semantic Web Technologies" .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Spring_Finals
:Spring_Finals rdf:type owl:NamedIndividual ,
                        :Final .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Spring_Midterm
:Spring_Midterm rdf:type owl:NamedIndividual ,
                         :Midterm .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Spring_Quizzes
:Spring_Quizzes rdf:type owl:NamedIndividual ,
                         :Quiz .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Student1
:Student1 rdf:type owl:NamedIndividual ,
                   :Student ;
          :has_Appeared :Spring_Finals ,
                        :Spring_Midterm ,
                        :Spring_Quizzes ;
          :has_Attended :CS_Club_Activity ;
          :has_Enrolled_In :CS_500 ,
                           :CS_530 ,
                           :CS_575 ,
                           :Synchronous ;
          :has_Grade :B_Above_Average ;
          :studies :CS_407 ,
                   :CS_501 ,
                   :CS_502 ;
          :Admitted_Year 2021 ;
          :Email_Id "mounikamendu"@my.ccsu.edu ;
          :Gender "Female" ;
          :Graduated_Year 2022 ;
          :age 24 ;
          :first_Name "Mounika" ;
          :last_Name "Mendu" ;
          :phone "860-912-5772" ;
          :student_Id 30420542 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Student10
:Student10 rdf:type owl:NamedIndividual ,
                    :Student ;
           :has_Appeared :Homework ,
                         :Summer_Finals ;
           :has_Attended :CS_Club_Activity ;
           :has_Grade :B_Above_Average ;
           :Admitted_Year 2018 ;
           :Email_Id "kavithareddy"@my.ccsu.edu ;
           :Gender "Female" ;
           :Graduated_Year 2019 ;
           :age 28 ;
           :first_Name "Kavitha" ;
           :last_Name "Reddy" ;
           :phone "821-334-3385" ;
           :student_Id 30488766 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Student2
:Student2 rdf:type owl:NamedIndividual ,
                   :Student ;
          :has_Appeared :Summer_Finals ,
                        :Summer_Midterm ;
          :has_Attended :CS_Club_Activity ;
          :has_Enrolled_In :CET_501 ,
                           :CS_560 ,
                           :CS_575 ,
                           :InPerson ;
          :studies :CS_500 ;
          :Admitted_Year 2020 ;
          :Email_Id "kanewilliams"@my.ccsu.edu ;
          :Gender "Female" ;
          :Graduated_Year 2021 ;
          :age 25 ;
          :first_Name "Kane" ;
          :last_Name "Williams" ;
          :phone "860-312-4833" ;
          :student_Id 30412366 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Student3
:Student3 rdf:type owl:NamedIndividual ,
                   :Student ;
          :has_Appeared :Course_Project ;
          :has_Attended :CS_Club_Activity ;
          :has_Enrolled_In :CET_594 ,
                           :CS_502 ,
                           :CS_595 ,
                           :InPerson ;
          :studies :CET_501 ,
                   :CS_501 ;
          :Admitted_Year 2020 ;
          :Email_Id "bairstowgonny"@my.ccsu.edu ;
          :Gender "Male" ;
          :Graduated_Year 2022 ;
          :age 32 ;
          :first_Name "Bairstow" ;
          :last_Name "Gonny" ;
          :phone "860-285-2232" ;
          :student_Id 30423411 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Student4
:Student4 rdf:type owl:NamedIndividual ,
                   :Student ;
          :has_Appeared :Homework ,
                        :Spring_Finals ,
                        :Spring_Midterm ;
          :has_Attended :CS_Club_Activity ;
          :has_Enrolled_In :CS_560 ,
                           :CS_575 ,
                           :CS_595 ,
                           :InPerson ;
          :studies :CS_500 ,
                   :MUS_122 ;
          :Admitted_Year 2019 ;
          :Email_Id "viratkohli"@my.ccsu.edu ;
          :Gender "Male" ;
          :Graduated_Year 2020 ;
          :age 27 ;
          :first_Name "Kohli" ;
          :last_Name "Virat" ;
          :phone "829-214-2245" ;
          :student_Id 30423411 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Student5
:Student5 rdf:type owl:NamedIndividual ,
                   :Student ;
          :has_Appeared :Spring_Finals ,
                        :Spring_Midterm ;
          :has_Attended :CS_Club_Activity ;
          :has_Enrolled_In :CET_596 ,
                           :CS_570 ,
                           :CS_595 ,
                           :Synchronous ;
          :studies :CS_407 ;
          :Admitted_Year 2021 ;
          :Email_Id "spoorthyreddy"@my.ccsu.edu ;
          :Gender "Female" ;
          :Graduated_Year 2022 ;
          :age 26 ;
          :first_Name "Spoorthy" ;
          :last_Name "Reddy" ;
          :phone "866-223-1232" ;
          :student_Id 30423455 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Student6
:Student6 rdf:type owl:NamedIndividual ,
                   :Student ;
          :has_Appeared :Course_Project ,
                        :Homework ,
                        :Spring_Finals ,
                        :Spring_Midterm ,
                        :Spring_Quizzes ;
          :has_Attended :CS_Club_Activity ;
          :has_Enrolled_In :CS_502 ;
          :studies :CS_407 ,
                   :CS_501 ,
                   :MUS_236 ;
          :Admitted_Year 2019 ;
          :Email_Id "nareshkancharla"@my.ccsu.edu ;
          :Gender "Male" ;
          :Graduated_Year 2021 ;
          :age 23 ;
          :first_Name "Naresh" ;
          :last_Name "Kancharla" ;
          :phone "860-122-4553" ;
          :student_Id 30410233 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Student7
:Student7 rdf:type owl:NamedIndividual ,
                   :Student ;
          :has_Appeared :Course_Project ,
                        :Homework ,
                        :Summer_Finals ;
          :has_Attended :CS_Club_Activity ;
          :has_Grade :B_Above_Average ;
          :Admitted_Year 2020 ;
          :Email_Id "ramaanusha"@my.ccsu.edu ;
          :Gender "Female" ;
          :Graduated_Year 2022 ;
          :age 26 ;
          :first_Name "Anusha" ;
          :last_Name "Rama" ;
          :phone "849-201-3984" ;
          :student_Id 30412345 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Student8
:Student8 rdf:type owl:NamedIndividual ,
                   :Student ;
          :has_Appeared :Homework ,
                        :Spring_Finals ,
                        :Spring_Midterm ;
          :has_Grade :D_Passing_Below_Average ;
          :Admitted_Year 2018 ;
          :Email_Id "chandrakeshav"@my.ccsu.edu ;
          :Gender "Male" ;
          :Graduated_Year 2019 ;
          :age 21 ;
          :first_Name "Keshava" ;
          :last_Name "Chandra" ;
          :phone "860-288-9986" ;
          :student_Id 30415678 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Student9
:Student9 rdf:type owl:NamedIndividual ,
                   :Student ;
          :has_Appeared :Course_Project ;
          :has_Attended :CS_Club_Activity ;
          :has_Grade :C_Average ;
          :Admitted_Year 2016 ;
          :Email_Id "harshithkumar"@my.ccsu.edu ;
          :Gender "Male" ;
          :Graduated_Year 2018 ;
          :age 23 ;
          :first_Name "harshith" ;
          :last_Name "Kumar" ;
          :phone "219-223-5567" ;
          :student_Id 30499833 .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Summer_Finals
:Summer_Finals rdf:type owl:NamedIndividual ,
                        :Final .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Summer_Midterm
:Summer_Midterm rdf:type owl:NamedIndividual ,
                         :Midterm .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Summer_Quizzes
:Summer_Quizzes rdf:type owl:NamedIndividual ,
                         :Quiz .


###  http://www.cs.ccsu.edu/MounikaMendu/University.owl#Synchronous
:Synchronous rdf:type owl:NamedIndividual ,
                      :Online .


#################################################################
#    General axioms
#################################################################

[ rdf:type owl:AllDisjointClasses ;
  owl:members ( :Final
                :Midterm
                :Quiz
              )
] .


###  Generated by the OWL API (version 4.5.9.2019-02-01T07:24:44Z) https://github.com/owlcs/owlapi
